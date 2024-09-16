## ___***Composite Video Generation***___

### Training Dataset
[OpenVid-1M: A Large-Scale High-Quality Dataset for Text-to-video Generation](https://github.com/NJU-PCALab/OpenVid-1M)

### Compatitors
[Consistent Video-to-Video Transfer Using Synthetic Dataset (ICLR'24)](https://arxiv.org/pdf/2311.00213): Using a synthetic datasets (like CoVR dataset) for training with human instruction-like prompt (*e.g.*, "make ...", "turn ...", "change ...").

**Per-video tuning:**

[Tune-a-video: One-shot tuning of image diffusion models for text-to-video generation (ICCV'23)](https://arxiv.org/pdf/2212.11565)

[Vid2Vid-Zero: Zero-shot Video Editing Using Off-the-shelf Image Diffusion Models](https://arxiv.org/pdf/2303.17599)

[ControlVideo: Conditional Control for One-shot Text-driven Video Editing and Beyond](https://arxiv.org/pdf/2305.17098)

[Video-P2P: Video Editing with Cross-attention Control (CVPR'24)](https://openaccess.thecvf.com/content/CVPR2024/papers/Liu_Video-P2P_Video_Editing_with_Cross-attention_Control_CVPR_2024_paper.pdf)

[MotionDirector: Motion Customization of Text-to-Video Diffusion Models (ECCV'24 Oral)](https://arxiv.org/pdf/2310.08465)

[MotionClone: Training-Free Motion Cloning for Controllable Video Generation](https://arxiv.org/pdf/2406.05338)




**Tuning-free:**


[Pix2Video: Video Editing using Image Diffusion (ICCV'23)](https://arxiv.org/pdf/2303.12688)

[Rerender A Video: Zero-Shot Text-Guided Video-to-Video Translation (SIGGRAPH Asia'23)](https://arxiv.org/pdf/2306.07954)

[TokenFlow: Consistent Diffusion Features for Consistent Video Editing (ICLR'24)](https://arxiv.org/pdf/2307.10373)

[Control-A-Video: Controllable Text-to-Video Diffusion Models with Motion Prior and Reward Feedback Learning](https://arxiv.org/pdf/2305.13840) (Add. input)

[Make-Your-Video: Customized Video Generation Using Textual and Structural Guidance (TVCG'24)](https://arxiv.org/pdf/2306.00943) (Add. Depth input)

[VideoComposer: Compositional Video Synthesis with Motion Controllability (NeurIPS'23)](https://arxiv.org/pdf/2306.02018) (Add. input)



**Image-to-Video:**

[DynamiCrafter: Animating Open-domain Images with Video Diffusion Priors (ECCV'24 Oral)](https://arxiv.org/pdf/2310.12190)

[Stable Video Diffusion: Scaling Latent Video Diffusion Models to Large Datasets](https://arxiv.org/pdf/2311.15127)



### Metrics
To be updated

## Version-2 (Sept. 16)
### 2.1. Overview
![](./assets/pipeline/v2_pipe.png)
#### Compare to Version-1, we add spatial LoRA and temporal LoRA to U-Net, and only fine-tuned LoRA, not the entire U-Net.
We found that comparing to Version-1, only fine-tuning LoRA can show better editing ability， *e.g.*, the backgroud editing.


### 2.2. Showcases (320x512)--12,800 samples/steps

<table class="center">
  <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"erupting volcano"</td>
    <td colspan="1">"black clouds"</td>
    <td colspan="1">"black sky"</td>
    <td colspan="1">"an airplane in the sky"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_2/set_1/set_1.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_1/set_1_ed1.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_1/set_1_ed2.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_1/set_1_ed4.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_1/set_1_ed3.gif width="140">
  </td>
  </tr>

  <tr>
    <td colspan="1">Refrence Video</td>
   <td colspan="1">"black hair"</td>
    <td colspan="1">"red hair"</td>
    <td colspan="1">"a woman is crying"</td>
   <td colspan="1">"a woman is laughing"</td>
   <td colspan="1">"with green background"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_2/set_2/set_2.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_2/ed1.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_2/ed2.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_2/ed3.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_2/ed4.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_2/ed5.gif width="140">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"a man is eating"</td>
    <td colspan="1">"eating a cake"</td>
    <td colspan="1">"short hair"</td>
   <td colspan="1">"an Asian"</td>
    <td colspan="1">"on the beach"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_2/set_3/set_3.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_3/ed1.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_3/ed2.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_3/ed3.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_3/ed4.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_3/ed5.gif width="140">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"red shirt"</td>
    <td colspan="1">"long hair"</td>
   <td colspan="1">"a girl"</td>
    <td colspan="1">"on the playground"</td>
    <td colspan="1">"on the beach"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_2/set_6/set_6.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_6/ed1.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_6/ed2.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_6/ed3.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_6/ed4.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_6/ed5.gif width="140">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"black phone"</td>
    <td colspan="1">"green wall"</td>
    <td colspan="1">"a woman"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_2/set_4/set_4.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_4/ed1.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_4/ed2.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_4/ed3.gif width="140">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"it's running"</td>
    <td colspan="1">"red water"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_2/set_5/set_5.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_5/ed1.gif width="140">
  </td>
  <td>
    <img src=assets/V_2/set_5/ed2.gif width="140">
  </td>
  </tr>
  
</table >
 
## Version-1 (Sept. 11)
### 1.1. Overview
![](./assets/pipeline/v1_pipe.png)
#### Training:
**General pipeline:** Given a video, we first encode it into a latent representation frame-by-frame via the VAE encoder. Then, both the forward diffusion process and backward denoising process are performed in the latent space, where denoising conditions should be involved. Accordingly, the generated videos are obtained through the VAE decoder.

**Condition Encoding:** Different from previous T2V or I2V works that use text or single frame (image) as conditions, we adopt both text and video as conditions for U-Net simultaneously. Specifically, the text embedding is constructed with pre-trained CLIP text encoder, we employ the image encoder counterpart to extract features of frames across the given input video. We use the full visual tokens from the last layer of the CLIP image ViT to extract more complete information. Then, to obtain a context representation that can be interpreted by the denoising U-Net, a query transformer is introduced, which comprises N stacked layers of cross-attention and FFN.

Subsequently, the text embedding and context (video) embedding are emplyed to interact with the U-Net intermediate features through the dual cross-attention layers, where the *tanh* gating and adaptively learnable for each layers are employed to control the coefficient that fuses text-conditioned and video-conditioned features.

#### Inference:
During inference, given a reference video and a delta (editing) caption as conditions, our model can generate edited video from noise. Specifically, similar to video editing, two guidance scales are introduced to trade off the impact of the two control signals, *i.e.*, video condition and text condition. 



### 1.2. Showcases (320x512)--12,800 samples/steps

<table class="center">
  <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"erupting volcano"</td>
    <td colspan="1">"black clouds"</td>
    <td colspan="1">"an airplane in the sky"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_1/set_1/set_1.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_1/set_1_ed1.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_1/set_1_ed2.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_1/set_1_ed3.gif width="180">
  </td>
  </tr>

  <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"red hair"</td>
    <td colspan="1">"a woman is crying"</td>
   <td colspan="1">"a woman is laughing"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_1/set_2/set_2.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_2/ed2.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_2/ed3.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_2/ed4.gif width="180">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"a man is eating"</td>
    <td colspan="1">"eating a cake"</td>
   <td colspan="1">"an Asian"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_1/set_3/set_3.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_3/ed1.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_3/ed2.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_3/ed4.gif width="180">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"red shirt"</td>
    <td colspan="1">"long hair"</td>
   <td colspan="1">"a girl"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_1/set_6/set_6.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_6/ed1.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_6/ed2.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_6/ed3.gif width="180">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"black phone"</td>
    <td colspan="1">"green wall"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_1/set_4/set_4.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_4/ed1.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_4/ed2.gif width="180">
  </td>
  </tr>

   <tr>
    <td colspan="1">Refrence Video</td>
    <td colspan="1">"it's running"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/V_1/set_5/set_5.gif width="180">
  </td>
  <td>
    <img src=assets/V_1/set_5/ed1.gif width="180">
  </td>
  </tr>
  <!-- <tr>
    <td colspan="2">"two people dancing"</td>
    <td colspan="2">"girl talking and blinking"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/showcase/dance1.jpeg_00.png width="170">
  </td>
  <td>
    <img src=assets/showcase/dance1.gif width="170">
  </td>
  <td>
    <img src=assets/V_1/showcase/girl3.jpeg_00.png width="170">
  </td>
  <td>
    <img src=assets/V_1/showcase/girl3.gif width="170">
  </td>
  </tr> -->


  <!-- <tr>
    <td colspan="2">"zoom-in, a landscape, springtime"</td>
    <td colspan="2">"A blonde woman rides on top of a moving <br>washing machine into the sunset."</td>
  </tr>
  <tr>
  <td>
    <img src=assets/showcase/Upscaled_Aime_Tribolet_springtime_landscape_golden_hour_morning_pale_yel_e6946f8d-37c1-4ce8-bf62-6ba90d23bd93.mp4_00.png width="170">
  </td>
  <td>
    <img src=assets/showcase/Upscaled_Aime_Tribolet_springtime_landscape_golden_hour_morning_pale_yel_e6946f8d-37c1-4ce8-bf62-6ba90d23bd93.gif width="170">
  </td>

  <td>
    <img src=assets/showcase/Upscaled_Alex__State_Blonde_woman_riding_on_top_of_a_moving_washing_mach_c31acaa3-dd30-459f-a109-2d2eb4c00fe2.mp4_00.png width="170">
  </td>
  <td>
    <img src=assets/showcase/Upscaled_Alex__State_Blonde_woman_riding_on_top_of_a_moving_washing_mach_c31acaa3-dd30-459f-a109-2d2eb4c00fe2.gif width="170">
  </td>
  </tr>

  <tr>
    <td colspan="2">"explode colorful smoke coming out"</td>
    <td colspan="2">"a bird on the tree branch"</td>
  </tr>
  <tr>
  <td>
    <img src=assets/showcase/explode0.jpeg_00.png width="170">
  </td>
  <td>
    <img src=assets/showcase/explode0.gif width="170">
  </td>

  <td>
    <img src=assets/showcase/bird000.jpeg width="170">
  </td>
  <td>
    <img src=assets/showcase/bird000.gif width="170">
  </td>
  </tr> -->
</table >


## Acknowledgements

Our work is built on top of [DynamiCrafter](https://github.com/Doubiiu/DynamiCrafter) and [VideoCrafter](https://github.com/AILab-CVC/VideoCrafter). Thanks for their awesome work!

