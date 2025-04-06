---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

Hello there! 

Welcome to Kunjun Li's website!
I'm currently a third-year Computer Engineering student at [National University of Singapore](https://nus.edu.sg/) from August 2022. My research focuses on Efficient Generative AI.


# 🔥 News
- *2025.04*: &nbsp; 🚀 [TinyFusion](https://arxiv.org/abs/2412.01199) is selected as CVPR 2025 Highlight.
  
- *2025.01*: &nbsp; 🥳 Our team won the Second Place of [2025 SkiTB Visual Tracking Challenge](https://sites.google.com/unitn.it/cv4ws-wacv2025/skitb-challenge?authuser=0).

- *2024.05*: &nbsp; 🎉  PixelGen wins [ACM/IEEE IPSN 2024](https://ipsn.acm.org/2024/awards.html) Best Demonstration Runner-Up award. 

# 📝 Publications 


<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2025</div><img src='https://github.com/VainF/TinyFusion/raw/main/assets/framework.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**TinyFusion: Diffusion Transformers Learned Shallow**  
CVPR’25 Highlight (3%) | Tiny DiTs at 7% Training Costs | 2x Faster Inference

Gongfan Fang<span style="font-size:smaller;">*</span>, <strong>Kunjun Li<span style="font-size:smaller;">*</span></strong>, Xinyin Ma, Xinchao Wang <em>(Equal-first author)</em>
- Directly optimizes the recoverability of the pruned model, which ensures better performance after fine-tuning.
- Achieveing a 2x speedup using less than 7% of the original pre-training cost with a FID score of 2.86.

<div style="display: inline">
    <a href="https://arxiv.org/abs/2412.01199"> <strong>[paper]</strong></a>
    <a href="https://github.com/VainF/TinyFusion"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> Diffusion Transformers have demonstrated remarkable capabilities in image generation but often come with excessive parameterization, resulting in considerable inference overhead in real-world applications. In this work, we present TinyFusion, a depth pruning method designed to remove redundant layers from diffusion transformers via end-to-end learning. The core principle of our approach is to create a pruned model with high recoverability, allowing it to regain strong performance after fine-tuning. To accomplish this, we introduce a differentiable sampling technique to make pruning learnable, paired with a co-optimized parameter to simulate future fine-tuning. While prior works focus on minimizing loss or error after pruning, our method explicitly models and optimizes the post-fine-tuning performance of pruned models. Experimental results indicate that this learnable paradigm offers substantial benefits for layer pruning of diffusion transformers, surpassing existing importance-based and error-based methods. Additionally, TinyFusion exhibits strong generalization across diverse architectures, such as DiTs, MARs, and SiTs. Experiments with DiT-XL show that TinyFusion can craft a shallow diffusion transformer at less than 7% of the pre-training cost, achieving a 2times speedup with an FID score of 2.86, outperforming competitors with comparable efficiency. </p>
    </div>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">MobiCom 2024</div><img src='https://github.com/weiserlab/PixelGen/raw/main/assets/banner.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**PixelGen: Rethinking Embedded Camera Systems for Mixed-Reality**  
| *Novel embedded camera system for mixed reality*

<strong>Kunjun Li</strong>, Manoj Gulati, Dhairya Shah, Steven Waskito, Shantanu Chakrabarty and Ambuj Varshney
- Generate High Resolution RGB images from Monochrome and sensor data.
- Novel representation of the surroundings from invisible signal.

<div style="display: inline">
    <a href="https://dl.acm.org/doi/10.1145/3636534.3696216"><strong>[paper]</strong></a>
    <a href="https://github.com/weiserlab/PixelGen"><strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> A confluence of advances in several fields has led to the emergence of mixed-reality headsets. They can enable us to interact with and visualize our environments in novel ways. Nonetheless, mixed-reality headsets are constrained today as their camera systems only capture a narrow part of the visible spectrum. Our environment contains rich information that cameras do not capture. It includes phenomena captured through sensors, electromagnetic fields beyond visible light, acoustic emissions, and magnetic fields. We demonstrate our ongoing work, PixelGen, to redesign cameras for low power consumption and to be able to visualize our environments in a novel manner, making some of the invisible phenomena visible. Pixel-Gen combines low-bandwidth sensors with a monochrome camera to capture a rich representation of the world. This design choice ensures information is communicated energy-efficiently. This information is then combined with diffusion-based image models to generate unique representations of the environment, visualizing the otherwise invisible fields. We demonstrate that together with a mixed reality headset, it enables us to observe the world uniquely. </p>
    </div>
</div>

</div>
</div>
