---
title: 'People'
date: 2025-04-03
type: landing

design:
  # Section spacing
  spacing: '0rem'

# Page sections
sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      # username: admin
      text: ""
    design:
      spacing:
        padding: ["165px", "0px","170px","0px"]  # 垂直30px/水平0
      css_class: dark
      background:
        color: white
        image:
          # Add your image background to `assets/media/`.
          filename: people.jpg
          filters:
            brightness: 1.0
          size: 1100px 500px
          position: center
          parallax: false


  - block: markdown
    content:
      #title: '<span style="font-size: 24px;">Team Member</span>'
      text: |
        {{< test margin="625px" bg="#ffffff" >}}
        {{< center >}}
        ## Team Member
        {{< /center >}}

        <!-- markdownlint-disable -->
        <div class="team-grid" style="
          display: grid;
          grid-template-columns: repeat(2, 1fr);
          gap: 20px;
          margin-top: 30px;
        "> 

          <!-- Member 1 -->
          <div class="member-card" style="
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
          ">
            <img src="/test_temp/cutegirl.jpg" style="width: 120px; height: 120px; object-fit: cover;">
            <h3 style="margin: 0 0 10px 0">Xiang Xiang</h3>
            <p style="margin: 0; color: #000">Huazhong University of Science and Technology</p>
          </div>

          <!-- Member 2 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px ;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">
           <img src="/test_temp/xz.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */
           ">
            <h3 style="margin: 0 0 10px 0">Zhuo Xu</h3>
            <p style="margin: 0; color: #000">Huazhong University of Science and Technology</p>
          </div>

          <!-- Member 3 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px ;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">

           <img src="/test_temp/dy.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */  
           ">
            <h3 style="margin: 0 0 10px 0">Yao Deng</h3>
            <p style="margin: 0; color: #000">Huazhong University of Science and Technology</p>
          </div>

          <!-- Member 4 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px ;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">
           <img src="/test_temp/zqh.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            border: 3px solid #4a89dc ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */ 
           ">

            <h3 style="margin: 0 0 10px 0">Qinhao Zhou</h3>
            <p style="margin: 0; color: #000;">Huazhong University of Science and Technology</p>
          </div>

          <!-- Member 5 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px ;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">
           <img src="/test_temp/lyf.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            border: 3px solid #4a89dc ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */  
           ">
            <h3 style="margin: 0 0 10px 0">Yifan Liang</h3>
            <p style="margin: 0; color: #000;">Huazhong University of Science and Technology</p>
          </div>
          <!-- Member 6 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">
           <img src="/test_temp/media/flower.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            border: 3px solid #4a89dc ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */
           ">
            <h3 style="margin: 0 0 10px 0">Ke Chen</h3>
            <p style="margin: 0; color: #000;">Huazhong University of Science and Technology</p>
          </div>

          <!-- Member 7 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">

           <img src="/test_temp/media/flower.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            border: 3px solid #4a89dc ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */
           ">
            <h3 style="margin: 0 0 10px 0">Qingfang Zheng</h3>
            <p style="margin: 0; color: #000;">Huazhong University of Science and Technology</p>
          </div>  

          <!-- Member 8 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px ;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">
           <img src="/test_temp/media/flower.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            border: 3px solid #4a89dc ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */ 
           ">
            <h3 style="margin: 0 0 10px 0">Yaowei Wang</h3>
            <p style="margin: 0; color: #000;">Huazhong University of Science and Technology</p>
          </div>

          <!-- Member 9 -->
          <div class="member-card" style="
            background: white ;
            padding: 20px ;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1) ;
          ">
           <img src="/test_temp/media/flower.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            border: 3px solid #4a89dc ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */
           ">
            <h3 style="margin: 0 0 10px 0">Xilin Chen</h3>
            <p style="margin: 0; color: #000;">Huazhong University of Science and Technology</p>
          </div>

           <!-- Member 10 -->
          <div class="member-card" style="
            background: white;
            padding: 20px ;
            border-radius: 8px ;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
          ">
           <img src="/test_temp/media/flower.jpg" style="
            width: 160px ;
            height: 160px ;
            object-fit: cover ;
            border-radius: 0 ;
            border: 3px solid #4a89dc ;
            flex-shrink: 0 ;       /* 防止图片被压缩 */ 
           ">
            <h3 style="margin: 0 0 10px 0">Wen Gao</h3>
            <p style="margin: 0; color: #000;">Huazhong University of Science and Technology</p>
          </div>
        </div>
        {{< /test >}}
---
