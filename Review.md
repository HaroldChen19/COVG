## ___***Literature Review***___

### Video Editing


#### 📌Condition (Depth, Canny, Hed Maps) Guided:

***Motions are controlled via additional condition inputs, due to the massive loss of original video information, style editing is preferred even when full semantics are provided***

[Control-A-Video](https://arxiv.org/pdf/2305.13840) and [VideoControlNet](https://arxiv.org/pdf/2307.14073): motion-aware editing; style editing

***Based on diffusion atlases, editing the foreground and background separately is limited in applicable scenarios and prone to unnatural foreground-background splicing and temporal consistency.***

[StableVideo (ICCV'23)](https://arxiv.org/pdf/2308.09592) and [DiffusionAtlas](https://arxiv.org/pdf/2312.03772): can only control foreground and background




📌**Attention (DDIM Inversion) Control:**

***Shapes are controlled via DDIM inversion, so full semantic information is still required for editing.***

[FateZero (ICCV'23 Oral)](https://arxiv.org/pdf/2303.09535), [TokenFlow (ICLR'24)](https://arxiv.org/pdf/2307.10373), and [Video-P2P (CVPR'24)](https://openaccess.thecvf.com/content/CVPR2024/papers/Liu_Video-P2P_Video_Editing_with_Cross-attention_Control_CVPR_2024_paper.pdf): shape-aware editing




