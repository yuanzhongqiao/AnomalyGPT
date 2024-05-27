<div class="Box-sc-g0xbh4-0 bJMeLZ js-snippet-clipboard-copy-unpositioned" data-hpc="true"><article class="markdown-body entry-content container-lg" itemprop="text"><p align="center" width="100%" dir="auto">
<a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/logo.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/logo.png" alt="AnomalyGPT_logo" style="width: 40%; max-width: 100%;"></a>
</p>
<div class="markdown-heading" dir="auto"><h1 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AnomalyGPT：使用大型视觉语言模型检测工业异常</font></font></h1><a id="user-content-anomalygpt-detecting-industrial-anomalies-using-large-vision-language-models" class="anchor" aria-label="永久链接：AnomalyGPT：使用大型视觉语言模型检测工业异常" href="#anomalygpt-detecting-industrial-anomalies-using-large-vision-language-models"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer nofollow" href="https://camo.githubusercontent.com/bdffb4fd6e34d5df6dab982e72e6e222286110c7a842ee019dbe3b468421837a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d434325323042592d2d4e432d2d5341253230342e302d7265642e737667"><img src="https://camo.githubusercontent.com/bdffb4fd6e34d5df6dab982e72e6e222286110c7a842ee019dbe3b468421837a/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4c6963656e73652d434325323042592d2d4e432d2d5341253230342e302d7265642e737667" alt="执照" data-canonical-src="https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-red.svg" style="max-width: 100%;"></a></p>
<p align="left" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">
   🌐</font></font><a href="https://anomalygpt.github.io" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">项目页面</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">• 🤗</font></font><a href="https://huggingface.co/spaces/FantasticGNU/AnomalyGPT" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在线演示</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">• 📃</font></font><a href="https://arxiv.org/abs/2308.15366" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">论文</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">• 🤖</font></font><a href="https://huggingface.co/FantasticGNU/AnomalyGPT" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">模型</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">• 📹</font></font><a href="https://www.youtube.com/watch?v=lcxBfy0YnNA" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">视频</font></font></a>
</p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">顾兆鹏、朱兵科、朱桂波、陈莹莹、唐明、王金桥</font></font></p>
<hr>
<span id="user-content-all_catelogue">
<div class="markdown-heading" dir="auto"><h2 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录：</font></font></h2><a id="user-content-catalogue" class="anchor" aria-label="永久链接： 目录：" href="#catalogue"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<ul dir="auto">
<li>
<p dir="auto"><a href="#introduction"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1. 简介</font></font></a></p>
</li>
<li>
<p dir="auto"><a href="#environment"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2. 运行 AnomalyGPT 演示</font></font></a></p>
<ul dir="auto">
<li><a href="#install_environment"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.1 环境安装</font></font></a></li>
<li><a href="#download_imagebind_model"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.2 准备 ImageBind 检查点</font></font></a></li>
<li><a href="#download_vicuna_model"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.3 准备 Vicuna 检查点</font></font></a></li>
<li><a href="#download_anomalygpt"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.4 准备 AnomalyGPT 的 Delta 权重</font></font></a></li>
<li><a href="#running_demo"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.5 部署演示</font></font></a></li>
</ul>
</li>
<li>
<p dir="auto"><a href="#train_anomalygpt"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3. 训练你自己的异常GPT</font></font></a></p>
<ul dir="auto">
<li><a href="#data_preparation"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.1 数据准备</font></font></a></li>
<li><a href="#training_configurations"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.2 训练配置</font></font></a></li>
<li><a href="#model_training"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.3 训练AnoamlyGPT</font></font></a></li>
</ul>
</li>
<li>
<p dir="auto"><a href="#examples"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4.示例</font></font></a></p>
</li>
</ul>

<ul dir="auto">
<li><a href="#license"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执照</font></font></a></li>
<li><a href="#citation"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">引用</font></font></a></li>
<li><a href="#acknowledgments"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">致谢</font></font></a></li>
</ul>
<hr>
<span id="user-content-introduction">
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1. 简介：</font></font><a href="#all_catelogue"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[回到顶部]</font></font></a></h3><a id="user-content-1-introduction-back-to-top" class="anchor" aria-label="永久链接：1. 简介：[返回顶部]" href="#1-introduction-back-to-top"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p align="center" width="100%" dir="auto">
<a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/compare.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/compare.png" alt="AnomalyGPT_logo" style="width: 80%; max-width: 100%;"></a>
</p>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AnomalyGPT</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">是第一个基于大型视觉语言模型 (LVLM) 的工业异常检测 (IAD) 方法，无需手动指定阈值即可检测工业图像中的异常。现有的 IAD 方法只能提供异常分数，需要手动设置阈值，而现有的 LVLM 无法检测图像中的异常。AnomalyGPT 不仅可以指示异常的存在和位置，还可以提供有关图像的信息。</font></font></p>
<a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/AnomalyGPT.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/AnomalyGPT.png" alt="异常GPT" style="max-width: 100%;"></a>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们利用预先训练的图像编码器和大型语言模型 (LLM) 通过模拟异常数据对齐 IAD 图像及其相应的文本描述。我们使用轻量级的基于视觉文本特征匹配的图像解码器来获取定位结果，并设计提示学习器为 LLM 提供细粒度语义并使用提示嵌入微调 LVLM。我们的方法还可以通过提供少量正常样本来检测以前未见过的项目的异常。</font></font></p>
<hr>
<span id="user-content-environment">
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2. 运行 AnomalyGPT 演示</font></font><a href="#all_catelogue"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[返回顶部]</font></font></a></h3><a id="user-content-2-running-anomalygpt-demo-back-to-top" class="anchor" aria-label="永久链接：2. 运行 AnomalyGPT 演示 [返回顶部]" href="#2-running-anomalygpt-demo-back-to-top"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<span id="user-content-install_environment">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.1 环境安装</font></font></h4><a id="user-content-21-environment-installation" class="anchor" aria-label="永久链接：2.1 环境安装" href="#21-environment-installation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在本地克隆存储库：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>git clone https://github.com/CASIA-IVA-Lab/AnomalyGPT.git
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="git clone https://github.com/CASIA-IVA-Lab/AnomalyGPT.git" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">安装所需的软件包：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>pip install -r requirements.txt
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="pip install -r requirements.txt" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<span id="user-content-download_imagebind_model">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.2 准备 ImageBind 检查点：</font></font></h4><a id="user-content-22-prepare-imagebind-checkpoint" class="anchor" aria-label="永久链接：2.2 准备 ImageBind 检查点：" href="#22-prepare-imagebind-checkpoint"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://dl.fbaipublicfiles.com/imagebind/imagebind_huge.pth" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">你可以通过此链接</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下载预先训练好的ImageBind模型</font><font style="vertical-align: inherit;">。下载后，将下载的文件（imagebind_huge.pth）放在</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/pretrained_ckpt/imagebind_ckpt"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[./pretrained_ckpt/imagebind_ckpt/]</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录中。</font></font></p>
<span id="user-content-download_vicuna_model">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.3 准备 Vicuna 检查点：</font></font></h4><a id="user-content-23-prepare-vicuna-checkpoint" class="anchor" aria-label="永久链接：2.3 准备 Vicuna 检查点：" href="#23-prepare-vicuna-checkpoint"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要准备预先训练的 Vicuna 模型，请按照</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/pretrained_ckpt#1-prepare-vicuna-checkpoint"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[此处]</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">提供的说明进行操作。</font></font></p>
<span id="user-content-download_anomalygpt">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.4 准备 AnomalyGPT 的 Delta 权重：</font></font></h4><a id="user-content-24-prepare-delta-weights-of-anomalygpt" class="anchor" aria-label="永久链接：2.4 准备 AnomalyGPT 的 Delta 权重：" href="#24-prepare-delta-weights-of-anomalygpt"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://github.com/yxuansu/PandaGPT"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们使用PandaGPT</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">预先训练的参数</font><font style="vertical-align: inherit;">来初始化我们的模型。您可以在下表中获得使用不同策略训练的 PandaGPT 的权重。在我们的实验和在线演示中，我们使用 Vicuna-7B，</font></font><code>openllmplayground/pandagpt_7b_max_len_1024</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">由于计算资源的限制。如果切换到 Vicuna-13B，预计效果会更好。</font></font></p>
<table>
<thead>
<tr>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基础语言模型</font></font></strong></th>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最大序列长度</font></font></strong></th>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Huggingface Delta Weights 地址</font></font></strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Vicuna-7B（版本 0）</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">512</font></font></td>
<td align="center"><a href="https://huggingface.co/openllmplayground/pandagpt_7b_max_len_512" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">openllmplayground/pandagpt_7b_max_len_512</font></font></a></td>
</tr>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Vicuna-7B（版本 0）</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1024</font></font></td>
<td align="center"><a href="https://huggingface.co/openllmplayground/pandagpt_7b_max_len_1024" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">openllmplayground/pandagpt_7b_max_len_1024</font></font></a></td>
</tr>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Vicuna-13B（版本 0）</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">256</font></font></td>
<td align="center"><a href="https://huggingface.co/openllmplayground/pandagpt_13b_max_len_256" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">openllmplayground/pandagpt_13b_max_len_256</font></font></a></td>
</tr>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">Vicuna-13B（版本 0）</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">400</font></font></td>
<td align="center"><a href="https://huggingface.co/openllmplayground/pandagpt_13b_max_len_400" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">openllmplayground/pandagpt_13b_max_len_400</font></font></a></td>
</tr>
</tbody>
</table>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请将下载的 7B/13B 增量权重文件（pytorch_model.pt）放在</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/pretrained_ckpt/pandagpt_ckpt/7b"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">./pretrained_ckpt/pandagpt_ckpt/7b/</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">或</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/pretrained_ckpt/pandagpt_ckpt/13b"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">./pretrained_ckpt/pandagpt_ckpt/13b/</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录中。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">之后，您可以从下表中下载 AnomalyGPT 权重。</font></font></p>
<table>
<thead>
<tr>
<th align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">设置和数据集</font></font></th>
<th align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">权重地址</font></font></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">MVTec-AD 上的无监督</font></font></td>
<td align="center"><a href="https://huggingface.co/FantasticGNU/AnomalyGPT/blob/main/train_mvtec/pytorch_model.pt" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AnomalyGPT/train_mvtec</font></font></a></td>
</tr>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">不受监管的 VisaA</font></font></td>
<td align="center"><a href="https://huggingface.co/FantasticGNU/AnomalyGPT/blob/main/train_visa/pytorch_model.pt" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AnomalyGPT/train_visa</font></font></a></td>
</tr>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">受 MVTec-AD、VisA、MVTec-LOCO-AD 和 CrackForest 的监督</font></font></td>
<td align="center"><a href="https://huggingface.co/FantasticGNU/AnomalyGPT/blob/main/train_supervised/pytorch_model.pt" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AnomalyGPT/train_supervised</font></font></a></td>
</tr>
</tbody>
</table>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下载后，将 AnomalyGPT 权重放在</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/code/ckpt"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">./code/ckpt/</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录中。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在我们的</font></font><a href="https://huggingface.co/spaces/FantasticGNU/AnomalyGPT" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在线演示</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">中，我们使用监督设置作为默认模型，以获得增强的用户体验。您也可以在本地尝试其他权重。</font></font></p>
<span id="user-content-running_demo">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">2.5. 部署演示</font></font></h4><a id="user-content-25-deploying-demo" class="anchor" aria-label="永久链接：2.5. 部署演示" href="#25-deploying-demo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">完成上述步骤后，您可以在本地运行演示</font></font></p>
<div class="highlight highlight-source-shell notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-c1">cd</span> ./code/
python web_demo.py</pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd ./code/
python web_demo.py" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<hr>
<span id="user-content-train_anomalygpt">
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3. 训练你自己的 AnomalyGPT   </font></font><a href="#all_catelogue"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[回到顶部]</font></font></a></h3><a id="user-content-3-train-your-own-anomalygpt--back-to-top" class="anchor" aria-label="永久链接：3. 训练你自己的 AnomalyGPT [返回顶部]" href="#3-train-your-own-anomalygpt--back-to-top"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">先决条件：</font></font></strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">在训练模型之前，请确保环境已正确安装，并且已下载 ImageBind、Vicuna 和 PandaGPT 的检查点。</font></font></p>
<span id="user-content-data_preparation">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.1数据准备：</font></font></h4><a id="user-content-31-data-preparation" class="anchor" aria-label="永久链接：3.1 数据准备：" href="#31-data-preparation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://www.mvtec.com/company/research/datasets/mvtec-ad/downloads" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">你可以从[此链接]</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下载 MVTec-AD 数据集，从</font></font><a href="https://github.com/amazon-science/spot-diff"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[此链接]</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下载VisA数据集。你也可以从</font></font><a href="https://huggingface.co/datasets/openllmplayground/pandagpt_visual_instruction_dataset/tree/main" rel="nofollow"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[此处]</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下载 PandaGPT 的预训练数据</font><font style="vertical-align: inherit;">。下载后，将数据放在</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/data"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[./data]</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录中。</font></font></p>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/data"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">[./data]</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">目录</font><font style="vertical-align: inherit;">应如下所示：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>data
|---pandagpt4_visual_instruction_data.json
|---images
|-----|-- ...
|---mvtec_anomaly_detection
|-----|-- bottle
|-----|-----|----- ground_truth
|-----|-----|----- test
|-----|-----|----- train
|-----|-- capsule
|-----|-- ...
|----VisA
|-----|-- split_csv
|-----|-----|--- 1cls.csv
|-----|-----|--- ...
|-----|-- candle
|-----|-----|--- Data
|-----|-----|-----|----- Images
|-----|-----|-----|--------|------ Anomaly 
|-----|-----|-----|--------|------ Normal 
|-----|-----|-----|----- Masks
|-----|-----|-----|--------|------ Anomaly 
|-----|-----|--- image_anno.csv
|-----|-- capsules
|-----|-----|----- ...
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="data
|---pandagpt4_visual_instruction_data.json
|---images
|-----|-- ...
|---mvtec_anomaly_detection
|-----|-- bottle
|-----|-----|----- ground_truth
|-----|-----|----- test
|-----|-----|----- train
|-----|-- capsule
|-----|-- ...
|----VisA
|-----|-- split_csv
|-----|-----|--- 1cls.csv
|-----|-----|--- ...
|-----|-- candle
|-----|-----|--- Data
|-----|-----|-----|----- Images
|-----|-----|-----|--------|------ Anomaly 
|-----|-----|-----|--------|------ Normal 
|-----|-----|-----|----- Masks
|-----|-----|-----|--------|------ Anomaly 
|-----|-----|--- image_anno.csv
|-----|-- capsules
|-----|-----|----- ..." tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<span id="user-content-training_configurations">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.2 训练配置</font></font></h4><a id="user-content-32-training-configurations" class="anchor" aria-label="永久链接：3.2 训练配置" href="#32-training-configurations"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">下表显示了我们在实验中使用的训练超参数。超参数的选择基于我们的计算资源限制，即 2 x RTX3090 GPU。</font></font></p>
<table>
<thead>
<tr>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">基础语言模型</font></font></strong></th>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">纪元数</font></font></strong></th>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">批次大小</font></font></strong></th>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">学习率</font></font></strong></th>
<th align="center"><strong><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">最大长度</font></font></strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">小羊驼-7B</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">50</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">16</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1e-3</font></font></td>
<td align="center"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">1024</font></font></td>
</tr>
</tbody>
</table>
<span id="user-content-model_training">
<div class="markdown-heading" dir="auto"><h4 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">3.3 训练异常GPT</font></font></h4><a id="user-content-33-training-anomalygpt" class="anchor" aria-label="永久链接：3.3 训练异常GPT" href="#33-training-anomalygpt"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">要在 MVTec-AD 数据集上训练 AnomalyGPT，请运行以下命令：</font></font></p>
<div class="highlight highlight-source-yaml notranslate position-relative overflow-auto" dir="auto"><pre><span class="pl-s">cd ./code</span>
<span class="pl-s">bash ./scripts/train_mvtec.sh</span></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="cd ./code
bash ./scripts/train_mvtec.sh" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">训练脚本的关键参数如下：</font></font></p>
<ul dir="auto">
<li><code>--data_path</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：json文件的数据路径</font></font><code>pandagpt4_visual_instruction_data.json</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></li>
<li><code>--image_root_path</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：PandaGPT 训练图像的根路径。</font></font></li>
<li><code>--imagebind_ckpt_path</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：ImageBind 检查点的路径。</font></font></li>
<li><code>--vicuna_ckpt_path</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：保存预先训练的 Vicuna 检查点的目录。</font></font></li>
<li><code>--max_tgt_len</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：训练实例的最大序列长度。</font></font></li>
<li><code>--save_path</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：保存训练好的delta权重的目录，该目录会自动创建。</font></font></li>
<li><code>--log_path</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">：保存日志的目录，该目录会自动创建。</font></font></li>
</ul>
<p dir="auto"><font style="vertical-align: inherit;"></font><code>epochs</code><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">请注意，可以在</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/code/config/openllama_peft.yaml"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">./code/config/openllama_peft.yaml</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">文件的参数中设置 epoch 数，可以在</font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/code/dsconfig/openllama_peft_stage_1.json"><font style="vertical-align: inherit;">./code/dsconfig/openllama_peft_stage_1.json</font></a><font style="vertical-align: inherit;">中设置学习率  </font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/code/dsconfig/openllama_peft_stage_1.json"><font style="vertical-align: inherit;"></font></a></p>
<hr>
<span id="user-content-examples">
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">4.示例</font></font></h3><a id="user-content-4-examples" class="anchor" aria-label="永久链接：4. 示例" href="#4-examples"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/demo_1.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/demo_1.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h4 align="center" tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">带有裂缝的混凝土的图像。</font></font></h4><a id="user-content-an-image-of-concrete-with-crack-" class="anchor" aria-label="永久链接：带有裂缝的混凝土图像。" href="#an-image-of-concrete-with-crack-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<hr>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/demo_5.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/demo_5.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h4 align="center" tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">一粒快克胶囊。</font></font></h4><a id="user-content-a-crack-capsule-" class="anchor" aria-label="永久链接：一粒破解胶囊。" href="#a-crack-capsule-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<hr>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/demo_8.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/demo_8.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h4 align="center" tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">切开的榛子的图像。</font></font></h4><a id="user-content-an-image-of-a-cut-hazelnut-" class="anchor" aria-label="永久链接：切开的榛子的图像。" href="#an-image-of-a-cut-hazelnut-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<hr>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/demo_7.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/demo_7.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h4 align="center" tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">破损的瓶子。</font></font></h4><a id="user-content-a-damaged-bottle-" class="anchor" aria-label="永久链接：一个破损的瓶子。" href="#a-damaged-bottle-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<hr>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/demo_2.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/demo_2.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h4 align="center" tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">普通地毯的照片。</font></font></h4><a id="user-content-a-photo-of-normal-carpet-" class="anchor" aria-label="永久链接：普通地毯的照片。" href="#a-photo-of-normal-carpet-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<hr>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/demo_4.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/demo_4.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h4 align="center" tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">有缺陷的木头的照片。</font></font></h4><a id="user-content-a-photo-of-a-piece-of-wood-with-defect-" class="anchor" aria-label="永久链接：一块有缺陷的木头的照片。" href="#a-photo-of-a-piece-of-wood-with-defect-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<hr>
<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/CASIA-IVA-Lab/AnomalyGPT/blob/main/images/demo_3.png"><img src="https://github.com/CASIA-IVA-Lab/AnomalyGPT/raw/main/images/demo_3.png" alt="" style="max-width: 100%;"></a></p>
<div class="markdown-heading" dir="auto"><h4 align="center" tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">一块普通的布料。</font></font></h4><a id="user-content-a-piece-of-normal-fabric-" class="anchor" aria-label="永久链接：一块普通的布料。" href="#a-piece-of-normal-fabric-"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<hr>
<span id="user-content-license">
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">执照</font></font></h3><a id="user-content-license" class="anchor" aria-label="永久链接：许可证" href="#license"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">AnomalyGPT 获得了</font></font><a href="/CASIA-IVA-Lab/AnomalyGPT/blob/main/LICENSE"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">CC BY-NC-SA 4.0 许可</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">。</font></font></p>
<hr>
<span id="user-content-citation">
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">引用：</font></font></h3><a id="user-content-citation" class="anchor" aria-label="永久链接：引用：" href="#citation"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">如果您发现 AnomalyGPT 对您的研究或应用有用，请使用以下 BibTeX 引用：</font></font></p>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto"><pre class="notranslate"><code>@article{gu2023anomalyagpt,
  title={AnomalyGPT: Detecting Industrial Anomalies using Large Vision-Language Models},
  author={Gu, Zhaopeng and Zhu, Bingke and Zhu, Guibo and Chen, Yingying and Tang, Ming and Wang, Jinqiao},
  journal={arXiv preprint arXiv:2308.15366},
  year={2023}
}
</code></pre><div class="zeroclipboard-container">
    <clipboard-copy aria-label="Copy" class="ClipboardButton btn btn-invisible js-clipboard-copy m-2 p-0 tooltipped-no-delay d-flex flex-justify-center flex-items-center" data-copy-feedback="Copied!" data-tooltip-direction="w" value="@article{gu2023anomalyagpt,
  title={AnomalyGPT: Detecting Industrial Anomalies using Large Vision-Language Models},
  author={Gu, Zhaopeng and Zhu, Bingke and Zhu, Guibo and Chen, Yingying and Tang, Ming and Wang, Jinqiao},
  journal={arXiv preprint arXiv:2308.15366},
  year={2023}
}" tabindex="0" role="button">
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-copy js-clipboard-copy-icon">
    <path d="M0 6.75C0 5.784.784 5 1.75 5h1.5a.75.75 0 0 1 0 1.5h-1.5a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-1.5a.75.75 0 0 1 1.5 0v1.5A1.75 1.75 0 0 1 9.25 16h-7.5A1.75 1.75 0 0 1 0 14.25Z"></path><path d="M5 1.75C5 .784 5.784 0 6.75 0h7.5C15.216 0 16 .784 16 1.75v7.5A1.75 1.75 0 0 1 14.25 11h-7.5A1.75 1.75 0 0 1 5 9.25Zm1.75-.25a.25.25 0 0 0-.25.25v7.5c0 .138.112.25.25.25h7.5a.25.25 0 0 0 .25-.25v-7.5a.25.25 0 0 0-.25-.25Z"></path>
</svg>
      <svg aria-hidden="true" height="16" viewBox="0 0 16 16" version="1.1" width="16" data-view-component="true" class="octicon octicon-check js-clipboard-check-icon color-fg-success d-none">
    <path d="M13.78 4.22a.75.75 0 0 1 0 1.06l-7.25 7.25a.75.75 0 0 1-1.06 0L2.22 9.28a.751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018L6 10.94l6.72-6.72a.75.75 0 0 1 1.06 0Z"></path>
</svg>
    </clipboard-copy>
  </div></div>
<hr>
<span id="user-content-acknowledgments">
<div class="markdown-heading" dir="auto"><h3 tabindex="-1" class="heading-element" dir="auto"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">致谢：</font></font></h3><a id="user-content-acknowledgments" class="anchor" aria-label="永久链接：致谢：" href="#acknowledgments"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path d="m7.775 3.275 1.25-1.25a3.5 3.5 0 1 1 4.95 4.95l-2.5 2.5a3.5 3.5 0 0 1-4.95 0 .751.751 0 0 1 .018-1.042.751.751 0 0 1 1.042-.018 1.998 1.998 0 0 0 2.83 0l2.5-2.5a2.002 2.002 0 0 0-2.83-2.83l-1.25 1.25a.751.751 0 0 1-1.042-.018.751.751 0 0 1-.018-1.042Zm-4.69 9.64a1.998 1.998 0 0 0 2.83 0l1.25-1.25a.751.751 0 0 1 1.042.018.751.751 0 0 1 .018 1.042l-1.25 1.25a3.5 3.5 0 1 1-4.95-4.95l2.5-2.5a3.5 3.5 0 0 1 4.95 0 .751.751 0 0 1-.018 1.042.751.751 0 0 1-1.042.018 1.998 1.998 0 0 0-2.83 0l-2.5 2.5a1.998 1.998 0 0 0 0 2.83Z"></path></svg></a></div>
<p dir="auto"><font style="vertical-align: inherit;"></font><a href="https://github.com/yxuansu/PandaGPT"><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">我们从PandaGPT</font></font></a><font style="vertical-align: inherit;"><font style="vertical-align: inherit;">借用了一些代码和预训练权重</font><font style="vertical-align: inherit;">。感谢他们的出色工作！</font></font></p>
<p dir="auto"><a href="https://star-history.com/#CASIA-IVA-Lab/AnomalyGPT&amp;Date" rel="nofollow"><img src="https://camo.githubusercontent.com/07494eac823b5cb71b54a8e963f3a64d8b322281a5ebbb63ba7d14c339f8a947/68747470733a2f2f6170692e737461722d686973746f72792e636f6d2f7376673f7265706f733d43415349412d4956412d4c61622f416e6f6d616c7947505426747970653d44617465" alt="星历史图" data-canonical-src="https://api.star-history.com/svg?repos=CASIA-IVA-Lab/AnomalyGPT&amp;type=Date" style="max-width: 100%;"></a></p>
</span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></span></article></div>
