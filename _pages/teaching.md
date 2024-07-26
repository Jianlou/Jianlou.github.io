---
layout: page
permalink: /Others/
title: Others
description: 
nav: true
nav_order: 6
---

<head>
<style>
h3 {
  display: block;
  font-size: 1.17em;
  margin-top: 1em;
  margin-bottom: 1em;
  margin-left: 0;
  margin-right: 0;
  font-weight: bold;
}
</style>
</head>

<body>
<h3>Academic Services</h3>
<div>
    <ul>
        <li>Conference Reviewer of CVPR, ICCV, ECCV, IJCAI, AAAI, BMVC, WACV, ACMM, ICME, NeurIPS, and so on</li>
        <li>Journal Reviewer of Neurocomputing, TMM, TPAMI, and so on</li>
        <li>Member of CCF and CSIG</li>
    </ul>    
</div>

<h3>Thesis, Technical Reports and Slids</h3>
<div>
    <ul>
        <li>
            <img src="../assets/pdf/PostdoctoralFellowshipCompletionReport.png" alt="Thumbnail" width="auto" height="100" onclick="openModal('../assets/pdf/PostdoctoralFellowshipCompletionReport.png')" style="cursor: pointer;">
            "<a href="../assets/pdf/PostdoctoralFellowshipCompletionReport.pdf">基于辅助知识的图像/视频分割算法研究</a>", 
            报告, 2021.
        </li>
        <li>
            <img src="../assets/pdf/DoctoralDissertation.png" alt="Thumbnail" width="auto" height="100" onclick="openModal('../assets/pdf/DoctoralDissertation.png')" style="cursor: pointer;">
            "<a href="../assets/pdf/DoctoralDissertation.pdf">智能视觉监控中行人再识别技术研究</a>", 
            学位论文, 2018.
        </li>
        <li>
            <img src="../assets/pdf/DoctoralPresentation.png" alt="Thumbnail" width="auto" height="100" onclick="openModal('../assets/pdf/DoctoralPresentation.png')" style="cursor: pointer;">
            "<a href="../assets/pdf/DoctoralPresentation.pdf">智能视觉监控中行人再识别技术研究</a>", 
            学位报告, 2018.
        </li>
    </ul>    
</div>

<!-- Modal -->
<div id="imageModal" style="display:none; position: fixed; z-index: 1; left: 0; top: 0; width: 100%; height: 100%; overflow: auto; background-color: rgba(0,0,0,0.9);">
    <span onclick="closeModal()" style="position: absolute; top: 15px; right: 35px; color: #f1f1f1; font-size: 40px; font-weight: bold; cursor: pointer;">&times;</span>
    <img id="modalImage" style="margin: auto; display: block; max-width: 90%; max-height: 90%;">
</div>

<script>
function openModal(imgSrc) {
    var modal = document.getElementById('imageModal');
    var modalImg = document.getElementById("modalImage");
    modalImg.src = imgSrc;
    modal.style.display = "block";
}

function closeModal() {
    var modal = document.getElementById('imageModal');
    modal.style.display = "none";
}
</script>
</body>

















