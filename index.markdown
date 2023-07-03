---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

# Incorporating Ultrasound Tongue Images for Audio-Visual Speech Enhancement

### Author: [Rui-Chen Zheng](https://zhengrachel.github.io/), [Yang Ai](http://staff.ustc.edu.cn/~yangai/), [Zhen-Hua Ling](http://staff.ustc.edu.cn/~zhling/#!index.md).

Audio-visual speech enhancement (AV-SE) aims to enhance degraded speech along with extra visual information such as lip videos, and has been shown to be more effective than audio-only speech enhancement. This paper proposes the incorporating of ultrasound tongue images to improve the performance of lip-based AV-SE systems further. To address the challenge of acquiring ultrasound tongue images during inference, we first propose to employ knowledge distillation during training to investigate the feasibility of leveraging tongue-related information without directly inputting ultrasound tongue images. Specifically, we guide an audio-lip speech enhancement student model to learn from a pre-trained audio-lip-tongue speech enhancement teacher model, thus transferring tongue-related knowledge. To better model the alignment between the lip and tongue modalities, we further propose the introduction of a lip-tongue key-value memory network into the AV-SE model. This network enables the retrieval of tongue features based on readily available lip features, thereby assisting and improving the subsequent speech enhancement task. Experimental results demonstrate that both methods significantly improve the quality and intelligibility of the enhanced speech compared to traditional lip-based AV-SE baselines. Moreover, both proposed methods exhibit strong generalization performance on unseen speakers and in the presence of unseen noises. Furthermore, phone error rate (PER) analysis of automatic speech recognition (ASR) reveals that while all phonemes benefit from introducing ultrasound tongue images, palatal and velar consonants benefit most.

* * *

| Method           | LivingRoom Noise at 2.5dB | Cafe Noise at -2.5dB |
|:-----------------|:-----------------------|:------------------------|
| Noisy            |<audio  src="audio/01fi-015_xaud-noisy_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-noisy_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-noisy_2.5_living.png)|![spec](spec/05ms-015_xaud-noisy_-2.5_cafe.png)|
| Groundtruth      |<audio  src="audio/01fi-015_xaud-gt_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-gt_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-gt_2.5_living.png)|![spec](spec/05ms-015_xaud-gt_-2.5_cafe.png)|
| VSE              |<audio  src="audio/01fi-015_xaud-vse_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-vse_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-vse_2.5_living.png)|![spec](spec/05ms-015_xaud-vse_-2.5_cafe.png)|
| PVSE             |<audio  src="audio/01fi-015_xaud-pvse_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-pvse_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-pvse_2.5_living.png)|![spec](spec/05ms-015_xaud-pvse_-2.5_cafe.png)|
| IOAVSE           |<audio  src="audio/01fi-015_xaud-ioavse_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-ioavse_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-ioavse_2.5_living.png)|![spec](spec/05ms-015_xaud-ioavse_-2.5_cafe.png)|
| KD-based         |<audio  src="audio/01fi-015_xaud-kd_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-kd_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-kd_2.5_living.png)|![spec](spec/05ms-015_xaud-kd_-2.5_cafe.png)|
| Memory-based     |<audio  src="audio/01fi-015_xaud-memory_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-memory_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-memory_2.5_living.png)|![spec](spec/05ms-015_xaud-memory_-2.5_cafe.png)|
| Audio-Lip        |<audio  src="audio/01fi-015_xaud-lip_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-lip_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-lip_2.5_living.png)|![spec](spec/05ms-015_xaud-lip_-2.5_cafe.png)|
| Audio-Lip-Tongue |<audio  src="audio/01fi-015_xaud-lip_tongue_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-lip_tongue_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-lip_tongue_2.5_living.png)|![spec](spec/05ms-015_xaud-lip_tongue_-2.5_cafe.png)|
| Audio-Tongue     |<audio  src="audio/01fi-015_xaud-tongue_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-tongue_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-tongue_2.5_living.png)|![spec](spec/05ms-015_xaud-tongue_-2.5_cafe.png)|
| Audio-Only       |<audio  src="audio/01fi-015_xaud-ao_2.5_living.wav" controls="controls"></audio >|<audio  src="audio/05ms-015_xaud-ao_-2.5_cafe.wav" controls="controls"></audio >|
|                  |![spec](spec/01fi-015_xaud-ao_2.5_living.png)|![spec](spec/05ms-015_xaud-ao_-2.5_cafe.png)|

* * *

| Method           | LivingRoom Noise at -7.5dB | Cafeteria Noise at -7.5dB |
|:-----------------|:-----------------------|:------------------------|
| Noisy            |<audio  src="audio/10me-016_xaud-noisy_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-noisy_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-noisy_-7.5_living.png)|![spec](spec/50ms-184_aud-noisy_-7.5_cafeteria.png)|
| Groundtruth      |<audio  src="audio/10me-016_xaud-gt_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-gt_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-gt_-7.5_living.png)|![spec](spec/50ms-184_aud-gt_-7.5_cafeteria.png)|
| VSE              |<audio  src="audio/10me-016_xaud-vse_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-vse_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-vse_-7.5_living.png)|![spec](spec/50ms-184_aud-vse_-7.5_cafeteria.png)|
| PVSE             |<audio  src="audio/10me-016_xaud-pvse_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-pvse_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-pvse_-7.5_living.png)|![spec](spec/50ms-184_aud-pvse_-7.5_cafeteria.png)|
| IOAVSE           |<audio  src="audio/10me-016_xaud-ioavse_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-ioavse_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-ioavse_-7.5_living.png)|![spec](spec/50ms-184_aud-ioavse_-7.5_cafeteria.png)|
| KD-based         |<audio  src="audio/10me-016_xaud-kd_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-kd_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-kd_-7.5_living.png)|![spec](spec/50ms-184_aud-kd_-7.5_cafeteria.png)|
| Memory-based     |<audio  src="audio/10me-016_xaud-memory_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-memory_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-memory_-7.5_living.png)|![spec](spec/50ms-184_aud-memory_-7.5_cafeteria.png)|
| Audio-Lip        |<audio  src="audio/10me-016_xaud-lip_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-lip_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-lip_-7.5_living.png)|![spec](spec/50ms-184_aud-lip_-7.5_cafeteria.png)|
| Audio-Lip-Tongue |<audio  src="audio/10me-016_xaud-lip_tongue_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-lip_tongue_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-lip_tongue_-7.5_living.png)|![spec](spec/50ms-184_aud-lip_tongue_-7.5_cafeteria.png)|
| Audio-Tongue     |<audio  src="audio/10me-016_xaud-tongue_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-tongue_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-tongue_-7.5_living.png)|![spec](spec/50ms-184_aud-tongue_-7.5_cafeteria.png)|
| Audio-Only       |<audio  src="audio/10me-016_xaud-ao_-7.5_living.wav" controls="controls"></audio >|<audio  src="audio/50ms-184_aud-ao_-7.5_cafeteria.wav" controls="controls"></audio >|
|                  |![spec](spec/10me-016_xaud-ao_-7.5_living.png)|![spec](spec/50ms-184_aud-ao_-7.5_cafeteria.png)|


