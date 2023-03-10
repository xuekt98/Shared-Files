# 实验内容：
四类任务：Inpainting/Uncropping，Colorization，semantic $\leftrightarrow$ photo, sketch $\to$ photo

<font color=red>个人认为BBDM需要加入pixel space和latent space两部分的实验。一方面原因是要证明我们的方法比传统的conditional diffusion有更好的理论保证，那么不止是需要在latent space可以有更好的效果，在pixel space也能达到。另一方面是Inpainting，Colorization这些实验在Pixel space效果会更好一些。</font>

## 1. Inpainting/Uncropping
数据集：Visual GENOME/Places2  
对比模型：Palette（2021），DeepFillv2（2019），HiFill（2020），LDM（2022）（<font color=green>如果用Places2数据集，这部分实验结果可以直接用Palette文中的结果</font>）  
| Model | FID $\downarrow$ | IS $\uparrow$ | diversity $\uparrow$ | LPIPS $\downarrow$ |
| - | - | - | - | - |
| DeepFillv2（2019） | | | | |
| HiFill（2020） | | | | |
| Palette（2021） | | | | |
| LDM（2022） | | | | |
| Pixel-Space BBDM（ours）| | | | |
| Latent-Space BBDM（ours）| | | | |

## 2. Colorization
数据集：Visual GENOME/Places2  
对比模型：cGAN（Pix2Pix）（2017），PixColor（2017），Coltran（2021），Palette（2021），LDM（2022）（<font color=green>如果用Places2数据集，这部分实验结果可以直接用Palette文中的结果</font>）  

| Model | FID $\downarrow$ | IS $\uparrow$ | diversity $\uparrow$ | LPIPS $\downarrow$ |
| - | - | - | - | - |
| cGAN（Pix2Pix）（2017） | | | | |
| PixColor（2017） | | | | |
| Coltran（2021） | | | | |
| Palette（2021） | | | | |
| LDM（2022） | | | | |
| Pixel-Space BBDM（ours）| | | | |
| Latent-Space BBDM（ours）| | | | |

## 3. semantic $\leftrightarrow$ photo
数据集：CelebAMaskHQ（人脸），ADE20K（街景）  
对比模型：cGAN（Pix2Pix）（2017），OASIS（2021），Spade（2019），CDE（2021），LDM（2022）（<font color=magenta>这个部分有些实验现在已经跑过了可以直接用，不过ADE20K这种街景的效果可能会比较差。</font>）

#### CelebAMaskHQ
| Model | FID $\downarrow$ | IS $\uparrow$ | diversity $\uparrow$ | LPIPS $\downarrow$ |
| - | - | - | - | - |
| cGAN（Pix2Pix）（2017） | 56.997 | | 0 | 0.431 |
| Spade（2019） | 44.171 | | 0 | 0.531 |
| OASIS（2021） | 27.751 | | 39.662 | 0.526 |
| CDE（2021） | | | | |
| LDM（2022） | | | | |
| Pixel-Space BBDM（ours）| | | | |
| Latent-Space BBDM（ours）| | | | |

## 4. sketch $\to$ photo
数据集：edges2shoe/edges2handbags  
对比模型：cGAN（Pix2Pix）（2017），CycleGAN（2017），Spade（2019），DRIT++（2020），OASIS（2021），CDE（2021），LDM（2022）（<font color=magenta>这个部分有些实验现在已经跑过了可以直接用。</font>）

#### edges2shoes
| Model | FID $\downarrow$ | IS $\uparrow$ | diversity $\uparrow$ | LPIPS $\downarrow$ |
| - | - | - | - | - |
| cGAN（Pix2Pix）（2017） | 36.339 | | 0 | 0.183 |
| CycleGAN（2017） | 66.115 | | 0 | 0.276 |
| Spade（2019） | | | | |
| DRIT++（2021） | 53.373 | | 23.552 | 0.498 |
| OASIS（2021） | | | | |
| CDE（2021） | | | | |
| LDM（2022） | | | | |
| Pixel-Space BBDM（ours）| | | | |
| Latent-Space BBDM（ours）| | | | |

#### edges2handbags
| Model | FID $\downarrow$ | IS $\uparrow$ | diversity $\uparrow$ | LPIPS $\downarrow$ |
| - | - | - | - | - |
| cGAN（Pix2Pix）（2017） | 32.994 | | 0 | 0.273 |
| CycleGAN（2017） | 40.175 | | 0 | 0.367 |
| Spade（2019） | | | | |
| DRIT++（2021） | 43.675 | | 30.169 | 0.411 |
| OASIS（2021） | | | | |
| CDE（2021） | | | | |
| LDM（2022） | | | | |
| Pixel-Space BBDM（ours）| | | | |
| Latent-Space BBDM（ours）| | | | |
