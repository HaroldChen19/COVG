# ___***Literature Review***___

## Video Editing


### 📌 Condition (Depth, Canny, Hed Maps) Guided:

***"Motions are controlled via additional condition inputs, due to the massive loss of original video information, style editing is preferred even when full semantics are provided."***

[Text2Video-Zero (ICCV'23 Oral)](https://arxiv.org/pdf/2303.13439), [Rerender A Video (SIGGRAPH Asia'23)](https://arxiv.org/pdf/2306.07954), [Pix2Video (ICCV'23)](https://arxiv.org/pdf/2303.12688), [ControlVideo](https://arxiv.org/pdf/2305.17098), [Gen-1 (ICCV'23)](https://arxiv.org/pdf/2302.03011), [VideoComposer (NeurIPS'23)](https://arxiv.org/pdf/2306.02018), [Control-A-Video](https://arxiv.org/pdf/2305.13840), [VideoControlNet](https://arxiv.org/pdf/2307.14073), [Make-Your-Video (TVCG'24)](https://arxiv.org/pdf/2306.00943), [MotionClone](https://arxiv.org/pdf/2406.05338): motion-aware editing; style editing

***"Domain specific"***

[Text2Video-Zero (ICCV'23 Oral)](https://arxiv.org/pdf/2303.13439), [MotionEditor (CVPR'24)](https://openaccess.thecvf.com/content/CVPR2024/papers/Tu_MotionEditor_Editing_Video_Motion_via_Content-Aware_Diffusion_CVPR_2024_paper.pdf), [Follow-Your-Pose (AAAI'24)](https://github.com/mayuelala/FollowYourPose), [Follow-Your-Pose v2](https://arxiv.org/pdf/2406.03035): skeleton/motion-aware editing, only for specific domain (i.e., human)

***"Based on diffusion atlases, editing the foreground and background separately is limited in applicable scenarios and prone to unnatural foreground-background splicing and temporal consistency."***

[Text2LIVE (ECCV'22 Oral)](https://arxiv.org/pdf/2204.02491), [StableVideo (ICCV'23)](https://arxiv.org/pdf/2308.09592) and [DiffusionAtlas](https://arxiv.org/pdf/2312.03772): can only control foreground and background




### 📌 Attention (DDIM Inversion) Control:

***"Shapes are controlled via DDIM inversion, so full semantic information is still required for editing."***

[Text2Video-Zero (ICCV'23 Oral)](https://arxiv.org/pdf/2303.13439), [Pix2Video (ICCV'23)](https://arxiv.org/pdf/2303.12688), [Tune-A-Video(ICCV'23)](https://arxiv.org/pdf/2212.11565), [Vid2Vid-Zero](https://arxiv.org/pdf/2303.17599), [ControlVideo](https://arxiv.org/pdf/2305.17098), [VMC (CVPR'24)](https://arxiv.org/pdf/2312.00845), [FateZero (ICCV'23 Oral)](https://arxiv.org/pdf/2303.09535), [TokenFlow (ICLR'24)](https://arxiv.org/pdf/2307.10373), and [Video-P2P (CVPR'24)](https://openaccess.thecvf.com/content/CVPR2024/papers/Liu_Video-P2P_Video_Editing_with_Cross-attention_Control_CVPR_2024_paper.pdf): shape-aware editing


### 📌 Additional Tuning Control

***"Additional tuning for specific video(s), makes it cannot be general"***

[Rerender A Video (SIGGRAPH Asia'23)](https://arxiv.org/pdf/2306.07954), [Tune-A-Video(ICCV'23)](https://arxiv.org/pdf/2212.11565), [Vid2Vid-Zero](https://arxiv.org/pdf/2303.17599), [ControlVideo](https://arxiv.org/pdf/2305.17098), [Video-P2P (CVPR'24)](https://openaccess.thecvf.com/content/CVPR2024/papers/Liu_Video-P2P_Video_Editing_with_Cross-attention_Control_CVPR_2024_paper.pdf), [Customize-A-Video (ECCV'24)](https://arxiv.org/pdf/2402.14780), [MotionDirector (ECCV'24 Oral)](https://arxiv.org/pdf/2310.08465): Additional tuning on specific videos is needed to learn the motion paradigm


### 📌 Text-based Video-to-Video

[InsV2V (ICLR'24)](https://arxiv.org/pdf/2311.00213): additional pair data for training
