---
title: 'Dataset'
date: 2023-10-24
type: landing

design:
  spacing: '3rem'

# Note: `username` refers to the user's folder name in `content/authors/`

# Page sections
sections:
  - block: markdown
    content:
      text: |
        {{< test margin="625px" bg="#ffffff" >}}
        ## Sub-dataset 1
        The **Sub-dataset 1** contains 75,707 images with 189 classes, which is the largest and main sub-dataset. The images in **Sub-dataset 1** are collected from WHU-RS19, NWPU-RESISC45, RSD46-WHU, AID, MillionAID, MLRSNet, RSI-CB256, BigEarthNet, fMoW, TreeSatAI, FAIR1M, FGSC-23, FGSCR-42 and NaSC-TG2. The Class Incremental Learning (CIL) is mainly benchmarked in this sub-dataset. The file structure of the dataset is as follows:
        ```text
        sub-dataset1-RGB-domain1/
        ├── ALL/
        │   ├── train/ (Train set)
        │   │   ├── BareLand/ (Class XXX)
        │   │   │   ├──xxxxx.jpg (Images of class XXX)
        │   │   │   └──......
        │   │   ├── Apartment/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/ (Test set)
        │   │   ├── BareLand/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Apartment/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── DIL-RGB/ (Including 50 classes, used for Domain Incremental Learning (DIL))
        │   ├── train/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID/ (Including 94 in-distribution (ID) classes, used for Semantic Shift Out-of-Distribution Detection (OOD) & Open-set Recognition 
        │   │         or Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Apartment/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Apartment/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── OOD_Easy/ (Including 48 easy OOD classes, used for Semantic Shift Out-of-Distribution Detection & Open-set Recognition 
        │   │         or Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Bus/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Railway/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Bus/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Railway/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── OOD_Hard/(Including 47 Hard OOD classes, used for Semantic Shift Out-of-Distribution Detection & Open-set Recognition 
        │   │         or Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Bus/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Railway/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Pond/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Playground/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── CIL_split/
        │   ├── CIL_coarse_split.json (Coarse CIL split, with the classnames of each sessions.)
        │   └── CIL_scale_split.json (Scale CIL split, with the classnames of each sessions.)
        ├── OOD_split/
        │   ├── ID_94.txt (94 ID classnames.)
        │   ├── OOD_Easy_48.txt (48 Easy OOD classnames.)
        │   ├── OOD_Hard_47.txt (47 Hard OOD classnames.)
        │   ├── OOD_all.txt (95 OOD classnames.)
        │   └── classname_189.txt (189 all classnames.)
        ```

        ## Sub-dataset 2
        The **Sub-dataset 2** images are colleccted from FAIR1M, MillionAID, MLRSNet, Optimal-31, PatternNet, UCMLandUse, RSI-CB128 and RSD46-WHU, which does not overlap at all with the data sources in **Sub-dataset 1**. There are 26,777 images with 65 classes in this sub-dataset. Due to the varying capture conditions, there exists a significant domain shift between **Sub-dataset 1** and **Sub-dataset 2**, even though they both originate from satellite imagery. The file structure of the dataset is as follows:
        ```text
        sub-dataset2-RGB-domain2/
        ├── ALL/
        │   ├── train/ (Train set)
        │   │   ├── BareLand/ (Class XXX)
        │   │   │   ├──xxxxx.jpg (Images of class XXX)
        │   │   │   └──......
        │   │   ├── Bridge/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/ (Test set)
        │   │   ├── BareLand/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Bridge/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID/ (Including 43 in-distribution (ID) classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── BareLand/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── BareLand/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── OOD/ (Including 22 resampling bias OOD classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Baseball field/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Playground/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Baseball field/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Playground/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID.txt (43 ID classnames.)
        ├── OOD.txt (22 OOD classnames.)
        └── classname.txt (65 all classnames.)
        ```

        ## Sub-dataset 3
        The data from **Sub-dataset 3** is sourced from CC3M and RS5M. To expand the diversity included in the dataset, we consider retrieving **aerial** images with the same semantics or categories from above web datasets. **Sub-dataset 3** contains 11,037 images with 137 classes, which are included in the 187 classes in **Sub-dataset 1**. The file structure of the dataset is as follows:
        ```text
        sub-dataset3-Aerial-domain3/
        ├── ALL/
        │   ├── train/ (Train set)
        │   │   ├── BareLand/ (Class XXX)
        │   │   │   ├──xxxxx.jpg (Images of class XXX)
        │   │   │   └──......
        │   │   ├── Bridge/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/ (Test set)
        │   │   ├── BareLand/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Bridge/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID/ (Including 71 in-distribution (ID) classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── BareLand/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── BareLand/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── OOD/ (Including 66 resampling bias OOD classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Baseball field/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Playground/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Baseball field/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Playground/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── DIL-Aerial/ (Including 50 classes, used for Domain Incremental Learning (DIL))
        │   ├── train/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID.txt (71 ID classnames.)
        ├── OOD.txt (66 OOD classnames.)
        └── classname.txt (137 all classnames.)
        ```

        ## Sub-dataset 4
        **Sub-dataset 4** contains 22,153 multi-spectral fusion images with 56 classes, which is collected from fMoW, USTC SmokeRS and MRSSC2.0. There exists a domain gap between **Sub-dataset 4** and **Sub-dataset 1/2**, which only contain RGB images. The file structure of the dataset is as follows:
        ```text
        sub-dataset4-MSRGB-domain4/
        ├── ALL/ 
        │   ├── train/ (Train set)
        │   │   ├── Cloud/ (Class XXX)
        │   │   │   ├──xxxxx.jpg (Images of class XXX)
        │   │   │   └──......
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/ (Test set)
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID/ (Including 34 in-distribution (ID) classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Coast/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Coast/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── OOD/ (Including 22 modal-shift OOD classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Dam/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Tower/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Dam/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Tower/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── DIL-MSRGB/ (Including 50 classes, used for Domain Incremental Learning (DIL))
        │   ├── train/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID.txt (34 ID classnames.)
        ├── OOD.txt (22 OOD classnames.)
        └── classname.txt (56 all classnames.)
        ```

        ## Sub-dataset 5
        **Sub-dataset 5** contains 23,374 infrared images with 62 classes from fMoW, BigEarthNet, VisDrone, MRSSC2.0 and NaSC-TG2. The file structure of the dataset is as follows:
        ```text
        sub-dataset5-IR-domain5/
        ├── ALL/ 
        │   ├── train/ (Train set)
        │   │   ├── Cloud/ (Class XXX)
        │   │   │   ├──xxxxx.jpg (Images of class XXX)
        │   │   │   └──......
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/ (Test set)
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID/ (Including 38 in-distribution (ID) classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Coast/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Coast/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── OOD/ (Including 26 modal-shift OOD classes, used for Covariate Shift OOD Detection & Generalization.)
        │   ├── train/
        │   │   ├── Dam/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Tower/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Dam/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── Tower/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── DIL-IR/ (Including 50 classes, used for Domain Incremental Learning (DIL))
        │   ├── train/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        │   ├── test/
        │   │   ├── Desert/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   ├── cloud/
        │   │   │   ├──xxxxx.jpg
        │   │   │   └──......
        │   │   └──......
        ├── ID.txt (36 ID classnames.)
        ├── OOD.txt (36 OOD classnames.)
        └── classname.txt (62 all classnames.)
        ```
        {{< /test >}}
      design:
        spacing:
          padding: ["0px", "0px", "0px", "0px"]  # 垂直30px/水平0.
        design:
            width: full

---
