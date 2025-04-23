---
title: 'Task'
date: 2023-10-24
type: landing

design:
  spacing: '0rem'

# Note: `username` refers to the user's folder name in `content/authors/`
# Page sections
sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      # username: admin
      text: ""
    design:
      spacing:
        padding: ["310px", "0px", "290px", "0px"]  # 垂直30px/水平0
      css_class: dark
      background:
        color: white
        image:
          # Add your image background to `assets/media/`.
          filename: ICCV.png
          filters:
            brightness: 1.0
          size: actual
          position: center
          parallax: false  
          
  - block: markdown
    content:
      text: |
        {{< test margin="625px" bg="#ffffff" >}}
        <style>code {font-family: monospace;background-color: #f0f0f0;padding: 0.2em 0.4em;border-radius: 3px;color: #c7254e;}code::before, code::after {content: none !important;}</style>
        ## Full-spectrum Out-of-Distribution (OOD) Detection
        ### Semantic Shift OOD Detection & OSR
        Recent work highlights a strong correlation between OOD detection and OSR in both settings and performance. Both tasks detect new categories with shifted semantics, while OSR also requires maintaining in-distribution (ID) accuracy. OES supports evaluation of a model's ability to handle semantic shifts. Unlike existing remote sensing benchmarks that randomly split ID and OOD samples, OES consider the semantic shift degree between coarse and fine classes, aligning the setup with real-world deployment scenarios.

        We unify the tasks of semantic shift OOD detection and open-set recognition (OSR) into a single test task to evaluate the model's ability to handle semantic shifts.

        - **ID Classes**: We use the 94 classes as ID classes, defined in `./sub-dataset1-RGB-domain1/OOD_split/ID_94.txt`.
        
        - **Training/Test Sets**: Organized in `./sub-dataset1-RGB-domain1/ID/train` and `./sub-dataset1-RGB-domain1/ID/test`.

        ### Covariate Shift OOD Detection & Generalization
        Covariate shift OOD detection emphasizes robustness to covariate shifts, also referred to as full-spectrum OOD detection, where the ID data remain semantically consistent, while covariates vary. Given the practical needs of remote sensing, we focus on the following shifts:
        - **Resampling bias**, requiring model generalization across varying acquisition parameters (angle, height, resolution, time) within the same modality; 
        - **Modal shift**, demanding generalization across different modalities (satellites, aerial images) for the same semantic categories.

        For each dataset exhibiting domain shift relative to Sub-Dataset 1, we define the following test tasks:

        #### 1. Resampling Bias Scenario
        - **ID Test Set**: Resampled from Sub-Dataset 2 (`./sub-dataset2-RGB-domain2/ID/test`).
        - **ID Train Set**: Unchanged from Sub-Dataset 1 (`./sub-dataset1-RGB-domain1/ID/train`).

        ##### OOD Datasets:
        - **`OOD-Easy`**: 48 classes from Sub-Dataset 1 (minor shifts).
        - **`OOD-Hard`**: 47 classes from Sub-Dataset 1 (significant shifts).
        - **`Bias-OOD`**: 22 classes from Sub-Dataset 2 (shifts). Path: `./sub-dataset2-RGB-domain2/OOD/test`.
        - **`SUN`**: As above.

        #### 2. Aerial Modality-Shift Scenario
        - **ID Test Set**: Aerial data from Sub-Dataset 3 (`./sub-dataset3-Aerial-domain3/ID/test`).
        - **Train Set**: Unchanged (Sub-Dataset 1).

        ##### OOD Datasets:
        - **`Bias-OOD`**: 66 classes from Sub-Dataset 3. Path: `./sub-dataset3-Aerial-domain3/OOD/test`.
        - **`SUN`**: As above.

        #### 3. MSRGB Modality-Shift Scenario
        - **ID Test Set**: MSRGB data from Sub-Dataset 4 (`./sub-dataset4-MSRGB-domain4/ID/test`).
        - **Train Set**: Unchanged.

        ##### OOD Datasets:
        - **`Bias-OOD`**: 22 classes from Sub-Dataset 4. Path: `./sub-dataset4-MSRGB-domain4/OOD/test`.
        - **`SUN`**: As above.

        #### 4. IR Modality-Shift Scenario
        - **ID Test Set**: IR data from Sub-Dataset 5 (`./sub-dataset5-IR-domain5/ID/test`).
        - **Train Set**: Unchanged.

        ##### OOD Datasets:
        - **`Bias-OOD`**: 26 classes from Sub-Dataset 5. Path: `./sub-dataset5-IR-domain5/OOD/test`.
        - **`SUN`**: As above.

        ## Incremental Learning
        ### Class Incremental Learning (CIL)
        The rapid advancement of remote sensing generates vast amounts of high-quality images daily, necessitating models to recognize novel classes in open-world scenarios. However, existing CIL benchmarks in remote sensing are constrained by limited category diversity, restricted coarse-grained coverage, and uniform data scales, inadequately capturing real-world complexities. To address these limitations, we evaluate existing CIL methods using three benchmarks:
        - **Random**, which follows the widely-used CIL setting and randomly assign classes to 10 sessions equally.
        - **Coarse**, setting each session to contain fine classes of one coarse category to simulate the continuous learning from data captured by different types of dedicated satellites by the model. We divide all the classes into 10 coarse categories corresponding to 10 sessions. The detailed information of the dataset split is defined in `./sub-dataset1-RGB-domain1/CIL_split/CIL_coarse_split.json`.
        - **Scale**, which aims to replicate the continual process from large to small scales. The 10 sessions are evenly distributed categories based on a progression from large to small scales. The detailed information of the dataset split is defined in `./sub-dataset1-RGB-domain1/CIL_split/CIL_scale_split.json`.
        ### Domain-Incremental Learning (DIL)
        To assess the model's adaptability to data from different domains, we benchmark DIL on OES. We select 50 categories containing the same semantic classes from RGB satellite (**Sub-dataset 1**), RGB aerial (**Sub-dataset 3**), MSRGB (**Sub-dataset 4**) and IR images (**Sub-dataset 5**). 
        ### Coarse-to-Fine Few-shot Class-Incremental Learning (C2FSCIL)
        In C2FSCIL, we provide the model with all training samples accompanied by coarse labels in the base session, including 10 coarse-grained classes and 189 fine-grained classes. In the subsequent incremental sessions, we introduce samples with fine labels for each of the 10 coarse classes, supplying only 5 samples per class at each session, which is consistent with the few-shot setting. The initial training phase learns all 10 coarse classes, while each subsequent incremental phase introduces 20 fine-grained classes.
        {{< /test >}}
    design:
      spacing:
        padding: ["0px", "0px", "0px", "0px"]  # 垂直30px/水平0.
        

#   - block: markdown
#     content:
#       text: |
#         `./sub-dataset2-RGB-domain2/ID/test`
#     design:
#       spacing:
#         padding: ["0px", "0px", "0px", "0px"]  # 垂直30px/水平0.
  
      

#   - block: markdown
#     content:
#       title: |
#         <style> .no-wrap-center {white-space: nowrap; text-align: center;}</style><div class="no-wrap-center">Semantic Shift OOD Detection & OSR</div>

#         <style>.text {font-size: 18px;line-height: 1.6;font-weight: normal;}strong {font-weight: bold;color: red;}</style><div class="text">Home page of the large-scale fine-grained open-world remote-sensing datasets and benchmark <strong>OpenEarthSensing (OES)</strong> for various open-world remote-sensing downstream tasks, mainly including evaluating the ability of models to detect semantic shifts, adapt to covariate shifts, and continuously update the parameters without forgetting learned knowledge. OES includes 189 scene and object categories, covering the vast majority of potential semantic shifts that may occur in the real world. To provide a more comprehensive testbed for evaluating the generalization performance, OES encompasses five data domains with significant covariate shifts, including two RGB satellite domains, one RGB aerial domain, one multi-spectral RGB domain, and one infrared domain.  </div>

#         <style> .no-wrap-center {white-space: nowrap; text-align: center;}</style><div class="no-wrap-center">Covariate Shift OOD Detection & Generalization</div>

#         <style>.text {font-size: 18px;line-height: 1.6;font-weight: normal;}strong {font-weight: bold;color: red;}</style><div class="text">Home page of the large-scale fine-grained open-world remote-sensing datasets and benchmark <strong>OpenEarthSensing (OES)</strong> for various open-world remote-sensing downstream tasks, mainly including evaluating the ability of models to detect semantic shifts, adapt to covariate shifts, and continuously update the parameters without forgetting learned knowledge. OES includes 189 scene and object categories, covering the vast majority of potential semantic shifts that may occur in the real world. To provide a more comprehensive testbed for evaluating the generalization performance, OES encompasses five data domains with significant covariate shifts, including two RGB satellite domains, one RGB aerial domain, one multi-spectral RGB domain, and one infrared domain.  </div>

#         <style> .no-wrap-center {white-space: nowrap; text-align: center;}</style><div class="no-wrap-center">Class Incremental Learning</div>

#         <style>.text {font-size: 18px;line-height: 1.6;font-weight: normal;}strong {font-weight: bold;color: red;}</style><div class="text">Home page of the large-scale fine-grained open-world remote-sensing datasets and benchmark <strong>OpenEarthSensing (OES)</strong> for various open-world remote-sensing downstream tasks, mainly including evaluating the ability of models to detect semantic shifts, adapt to covariate shifts, and continuously update the parameters without forgetting learned knowledge. OES includes 189 scene and object categories, covering the vast majority of potential semantic shifts that may occur in the real world. To provide a more comprehensive testbed for evaluating the generalization performance, OES encompasses five data domains with significant covariate shifts, including two RGB satellite domains, one RGB aerial domain, one multi-spectral RGB domain, and one infrared domain.  </div>

#         <style> .no-wrap-center {white-space: nowrap; text-align: center;}</style><div class="no-wrap-center">Domain-Incremental Learning</div>

#         <style>.text {font-size: 18px;line-height: 1.6;font-weight: normal;}strong {font-weight: bold;color: red;}</style><div class="text">Home page of the large-scale fine-grained open-world remote-sensing datasets and benchmark <strong>OpenEarthSensing (OES)</strong> for various open-world remote-sensing downstream tasks, mainly including evaluating the ability of models to detect semantic shifts, adapt to covariate shifts, and continuously update the parameters without forgetting learned knowledge. OES includes 189 scene and object categories, covering the vast majority of potential semantic shifts that may occur in the real world. To provide a more comprehensive testbed for evaluating the generalization performance, OES encompasses five data domains with significant covariate shifts, including two RGB satellite domains, one RGB aerial domain, one multi-spectral RGB domain, and one infrared domain.  </div>

#         <style> .no-wrap-center {white-space: nowrap; text-align: center;}</style><div class="no-wrap-center">Coarse-to-Fine Few-shot Class-Incremental Learning</div>

#         <style>.text {font-size: 18px;line-height: 1.6;font-weight: normal;}strong {font-weight: bold;color: red;}</style><div class="text">Home page of the large-scale fine-grained open-world remote-sensing datasets and benchmark <strong>OpenEarthSensing (OES)</strong> for various open-world remote-sensing downstream tasks, mainly including evaluating the ability of models to detect semantic shifts, adapt to covariate shifts, and continuously update the parameters without forgetting learned knowledge. OES includes 189 scene and object categories, covering the vast majority of potential semantic shifts that may occur in the real world. To provide a more comprehensive testbed for evaluating the generalization performance, OES encompasses five data domains with significant covariate shifts, including two RGB satellite domains, one RGB aerial domain, one multi-spectral RGB domain, and one infrared domain.  </div>
#       text: |-
#       design:
#         spacing:
#           padding: ["0px", "0px", "0px", "0px"]  # 垂直30px/水平0.

#   - block: markdown
#     content:
#       text: |
#         <!DOCTYPE html><html lang="en"><head><meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0"><title>调整文字与网页左侧的间距</title><style>body {font-family: Arial, sans-serif;line-height: 1.6;margin: 0;padding-left: 20px; /* 设置左侧间距为20px */}.content {max-width: 800px;margin: 0 auto;padding: 20px;background-color: #f9f9f9;}</style></head><body><div class="content"><h1>这是标题</h1><p>这是一段文字，通过设置CSS中的padding属性，您可以调整文字与网页左侧的间距。</p></div></body></html>
#       design:
#         spacing:
#           padding: ["0px", "0px", "0px", "0px"]  # 垂直30px/水平0.

---
