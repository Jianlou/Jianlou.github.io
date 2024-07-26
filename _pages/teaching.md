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


<h3>Academic Services</h3>
<div>
    <ul>
        <li>Conference Reviewer of CVPR, ICCV, ECCV, IJCAI, AAAI, BMVC, WACV, ACMM, ICME, NeurIPS, and so on</li>
        <li>Journal Reviewer of Neurocomputing, TMM, TPAMI, and so on</li>
        <li>Menmber of CCF and CSIG</li>
    </ul>    
</div>

<h3>Thesis, Technical Reports and Slids</h3>
<div>
    <ul>
        <li>
            <img src="../assets/pdf/PostdoctoralFellowshipCompletionReport.png" alt="Thumbnail" width="100" height="100" onclick="openModal()">
            "<a href="../assets/pdf/PostdoctoralFellowshipCompletionReport.pdf">基于辅助知识的图像/视频分割算法研究</a>", 
            报告, 2021.
        </li>
        <li>
            <img src="../assets/pdf/DoctoralDissertation.png" alt="Thumbnail" width="100" height="100" onclick="openModal()">
            "<a href="../assets/pdf/DoctoralDissertation.pdf">智能视觉监控中行人再识别技术研究</a>", 
            学位论文, 2018.
        </li>
        <li>
            <img src="../assets/pdf/DoctoralPresentation.png" alt="Thumbnail" width="100" height="100" onclick="openModal()">
            "<a href="../assets/pdf/DoctoralPresentation.pdf">智能视觉监控中行人再识别技术研究</a>", 
            学位报告, 2018.
        </li>
    </ul>    
</div>

<!-- Modal -->
<div id="imageModal" style="display:none;">
    <span onclick="closeModal()" style="cursor:pointer;">&times;</span>
    <img id="modalImage" style="width:100%;">
</div>

<script>
function openModal() {
    var modal = document.getElementById('imageModal');
    var modalImg = document.getElementById("modalImage");
    modalImg.src = '../assets/pdf/PostdoctoralFellowshipCompletionReport.png';
    modal.style.display = "block";
}

function closeModal() {
    var modal = document.getElementById('imageModal');
    modal.style.display = "none";
}
</script>

<!-- <h3>Selected Publicity</h3>
<div>
    <ul>
        <li>Weights & Biases: <a href="https://wandb.ai/telidavies/ml-news/reports/StyleGAN-Human-More-Accurate-Generation-Of-Full-Body-Humans--VmlldzoxODgxOTky">StyleGAN-Human: More Accurate Generation of Full-Body Humans.</a> 2022</li>
        <li>MarkTechPost: <a href="https://www.marktechpost.com/2022/05/02/researchers-sensetime-develop-gnr-generalizable-neural-performer-for-human-novel-view-synthesis/">Researchers Develop the Generalizable Neural Performer for Human Novel View Synthesis.</a> 2022</li>
		<li>Vice: <a href="https://www.vice.com/en/article/g5xvk7/researchers-created-a-way-to-make-realistic-deepfakes-from-audio-clips">New Deepfake Method Can Put Words In Anyone’s Mouth.</a> 2020</li>
		<li>DIW: <a href="https://www.digitalinformationworld.com/2020/01/latest-deepfake-technology-create-more-convincing-videos-based-on-audio-source-than-ever-before.html">Latest Deepfake Technology Create More Convincing Videos Based on Audio Than Ever Before.</a> 2020</li>
		<li>QBitAI: <a href="https://www.qbitai.com/2020/01/10911.html">SenseTime Join in the Suppression of DeepFake with World’s Largest Forgery Detection Dataset.</a> 2020</li>
		<li>VentureBeat: <a href="https://venturebeat.com/2020/01/15/sensetime-face-forgery-research-deepfakes/">SenseTime Researchers Create a Benchmark to Test Face Forgery Detectors.</a> 2020</li>
    </ul>    
</div> -->
















