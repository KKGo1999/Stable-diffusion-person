# 高清人像生成 Stable Diffusion on Colab

[![](https://shields.io/twitter/follow/:kkgo1999?label=Follow)](https://twitter.com/kkgo1999)
[![](https://shields.io/youtube/channel/subscribers/UCx7EyuAEFfga6cTYABxlaCQ)](https://youtube.com/@KKGo1999)
[![](https://shields.io/github/stars/kkgo1999/Stable-diffusion-person?style=social)](https://github.com/KKGo1999)

本文介绍由基于Stable-diffusion的Chilloutmix模型（以及最新的ControlNet）生成高清真实人像的方法及Demo。

* 利用免费的Google Colab的在线环境创建Stable Diffusion WebUI，可以免去配置环境的麻烦。

* 身处内地的朋友：由于Colab是Google的服务，如果你在内地，需要一点上网的技巧（个人用的[Renzhe.Cloud](https://renzhe.cloud/auth/register?code=a7JU)，还比较稳）


## 可以一键运行的Google Colab环境

* Chilloutmix模型（通用的人物生成）：[Colab运行环境](https://colab.research.google.com/drive/1vhsF89FWUww-XhLa1MYXnLeqvmEiO1Yr?usp=sharing)

* Korean Doll Likeness LoRA模型（主要为韩国女生风）：[Colab运行环境](https://colab.research.google.com/drive/1icpYYgxi5dd7Iw2Vo3Fsht0PUVJfc-qH?usp=sharing)、[Civitai效果图](https://civitai.com/models/6424/chilloutmix)

* 图生图ControlNet模型（主要为以图生图）： [Colab运行环境](https://colab.research.google.com/drive/13IGGkt-kqEiqLH6KGWr19Bjqfd-48_9p?usp=sharing)

## YouTube小白教程
* 如果遇到困难，可以参考YouTube教程：[https://www.youtube.com/embed/9upNoWo3WB8](https://www.youtube.com/embed/9upNoWo3WB8)
* 实在搞不定时，可以考虑[加微信](https://www.kkgo1999.top/)入群交流

## 一些Prompts的示例

```text
best quality, ultra high res, photoshoot, (photorealistic:1.4), 1girl, singlet, sleeveless, (light brown hair:1), looking at viewer, smiling, cute, full body

Negative prompt: paintings, sketches, (worst quality:2), (low quality:2), (normal quality:2), lowres, normal quality, ((monochrome)), ((grayscale)), skin spots, acnes, skin blemishes, age spot, glans

Size: 512x768, 
Seed: 4243885665, 
Steps: 24, 
Sampler: DPM++ SDE, 
CFG scale: 8, 
Model hash: 7234b76e42, 
Hires steps: 20, H
Hires upscale: 1.75, 
Hires upscaler: Latent (bicubic antialiased), 
Denoising strength: 0.45


best quality, ultra high res, (photorealistic:1.4), 1girl, loose and oversized black jacket, white sports bra, (yoga pants:1), (light brown hair:1.2), looking at viewer, smiling, full body, streets, urban, makeup, wide angle
Negative prompt: paintings, sketches, (worst quality:2), (low quality:2), (normal quality:2), lowres, normal quality, ((monochrome)), ((grayscale)), skin spots, acnes, skin blemishes, age spot, glans
Size: 512x768, 
Seed: [3, 537380690]
Steps: [28, 32, 50, 60]
Sampler: DPM++ SDE Karras, 
CFG scale: [7,8]
Model hash: 7234b76e42, 
Hires steps: 20, 
Hires upscale: 1.75, 
Hires upscaler: Latent (bicubic antialiased), 
Denoising strength: 0.5


best quality, ultra high res, (photorealistic:1.4), 1woman, sleeveless white button shirt, black skirt, black choker, cute, (Kpop idol), (aegyo sal:1), (platinum blonde hair:1), ((puffy eyes)), looking at viewer, full body, facing front
Negative prompt: paintings, sketches, (worst quality:2), (low quality:2), (normal quality:2), lowres, normal quality, ((monochrome)), ((grayscale)), skin spots, acnes, skin blemishes, age spot, glans, nsfw, nipples
Size: 512x768, 
Seed: 1315543661, 
Steps: 28, 
Sampler: DPM++ SDE Karras, 
CFG scale: 8, 
Model hash: a757fe8b3d, 
Hires steps: 20, 
Hires upscale: 1.75, 
Hires upscaler: Latent (bicubic antialiased), 
Denoising strength: 0.45
```

<!--
https://medium.com/@croath/%E4%BD%8E%E6%88%90%E6%9C%AC%E4%BD%93%E9%AA%8C%E7%94%9F%E6%88%90-ai-%E5%B0%8F%E5%A7%90%E5%A7%90%E7%85%A7%E7%89%87-85ffa7c13cd7
https://www.bilibili.com/video/BV12x4y1V71Q/
-->
