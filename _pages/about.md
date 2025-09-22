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
I'm a final-year undergraduate student at [National University of Singapore (NUS)](https://nus.edu.sg/). Currently, I am a research intern at Princeton University, supervised by [Prof. Zhuang Liu](http://liuzhuang13.github.io). I also work closely with [Prof. Jenq-Neng Hwang](https://people.ece.uw.edu/hwang/) from UW and [Prof. Xinchao Wang](https://sites.google.com/site/sitexinchaowang/) from NUS.

My research focuses on **Efficient Deep Learning**, particularly optimizing training and inference of **LLMs, Diffusion and Multimodal
Models**. I have been working on sparse attention, network pruning and efficient architectures. My work strives to
achieve computational breakthroughs, making deep learning affordable and accessible to everyone, everywhere.


# 🔥 News
- *2025.09*: &nbsp;  🥳 [ScaleKV](https://arxiv.org/pdf/2505.19602) is accepted to NeurIPS 2025!

- *2025.04*: &nbsp; 🚀 [TinyFusion](https://openaccess.thecvf.com/content/CVPR2025/papers/Fang_TinyFusion_Diffusion_Transformers_Learned_Shallow_CVPR_2025_paper.pdf) is selected as CVPR 2025 Highlight.
  
- *2025.01*: &nbsp; 🌟 Our team won the Second Place of [2025 SkiTB Visual Tracking Challenge](https://sites.google.com/unitn.it/cv4ws-wacv2025/skitb-challenge?authuser=0).

- *2024.05*: &nbsp; 🎉  PixelGen wins [ACM/IEEE IPSN 2024](https://ipsn.acm.org/2024/awards.html) Best Demonstration Runner-Up award. 

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">NeurIPS 2025</div><img src='https://github.com/StargazerX0/ScaleKV/raw/main/assets/teaser.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**Memory-Efficient Visual Autoregressive Modeling with Scale-Aware KV Cache**  

<strong>Kunjun Li</strong>, Zigeng Chen, Cheng-Yen Yang, Jenq-Neng Hwang
- Scale-Aware KV cache tailored for next-scale prediction paradigm in VAR
- Lossless Compression while reducing inference memory from 85 GB to 8.5 GB

<div style="display: inline">
    <a href="https://arxiv.org/abs/2505.19602"> <strong>[paper]</strong></a>
    <a href="https://github.com/StargazerX0/ScaleKV"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> Visual Autoregressive (VAR) modeling has garnered significant attention for its innovative next-scale prediction approach, which yields substantial improvements in efficiency, scalability, and zero-shot generalization. Nevertheless, the coarse-to-fine methodology inherent in VAR results in exponential growth of the KV cache during inference, causing considerable memory consumption and computational redundancy. To address these bottlenecks, we introduce ScaleKV, a novel KV cache compression framework tailored for VAR architectures. ScaleKV leverages two critical observations: varying cache demands across transformer layers and distinct attention patterns at different scales. Based on these insights, ScaleKV categorizes transformer layers into two functional groups: drafters and refiners. Drafters exhibit dispersed attention across multiple scales, thereby requiring greater cache capacity. Conversely, refiners focus attention on the current token map to process local details, consequently necessitating substantially reduced cache capacity. ScaleKV optimizes the multi-scale inference pipeline by identifying scale-specific drafters and refiners, facilitating differentiated cache management tailored to each scale. Evaluation on the state-of-the-art text-to-image VAR model family, Infinity, demonstrates that our approach effectively reduces the required KV cache memory to 10% while preserving pixel-level fidelity. </p>
    </div>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">CVPR 2025</div><img src='https://github.com/VainF/TinyFusion/raw/main/assets/framework.png' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

**TinyFusion: Diffusion Transformers Learned Shallow**  
<span style="color: red; font-weight: bold;">CVPR 2025 Highlighted Paper (3%)</span>

Gongfan Fang<span style="font-size:smaller;">*</span>, <strong>Kunjun Li<span style="font-size:smaller;">*</span></strong>, Xinyin Ma, Xinchao Wang <em>(Equal-first author)</em>
- Directly optimizes the recoverability of the pruned model, which ensures better performance after fine-tuning.
- Achieveing a 2x speedup using less than 7% of the original pre-training cost with a FID score of 2.86.

<div style="display: inline">
    <a href="https://openaccess.thecvf.com/content/CVPR2025/papers/Fang_TinyFusion_Diffusion_Transformers_Learned_Shallow_CVPR_2025_paper.pdf"> <strong>[paper]</strong></a>
    <a href="https://github.com/VainF/TinyFusion"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> Diffusion Transformers have demonstrated remarkable capabilities in image generation but often come with excessive parameterization, resulting in considerable inference overhead in real-world applications. In this work, we present TinyFusion, a depth pruning method designed to remove redundant layers from diffusion transformers via end-to-end learning. The core principle of our approach is to create a pruned model with high recoverability, allowing it to regain strong performance after fine-tuning. To accomplish this, we introduce a differentiable sampling technique to make pruning learnable, paired with a co-optimized parameter to simulate future fine-tuning. While prior works focus on minimizing loss or error after pruning, our method explicitly models and optimizes the post-fine-tuning performance of pruned models. Experimental results indicate that this learnable paradigm offers substantial benefits for layer pruning of diffusion transformers, surpassing existing importance-based and error-based methods. Additionally, TinyFusion exhibits strong generalization across diverse architectures, such as DiTs, MARs, and SiTs. Experiments with DiT-XL show that TinyFusion can craft a shallow diffusion transformer at less than 7% of the pre-training cost, achieving a 2times speedup with an FID score of 2.86, outperforming competitors with comparable efficiency. </p>
    </div>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">IPSN 2024</div><img src='https://github.com/weiserlab/PixelGen/raw/main/assets/banner.png' alt="sym" width="100%"></div></div>
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
