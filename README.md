Visual encoding constitutes the basis of large multimodal models (LMMs) in understanding the visual world. Conventional LMMs process images in fixed sizes
and limited resolutions, while recent explorations in this direction are limited in
adaptivity, efficiency, and even correctness. In this work, we first take GPT-4V and
LLaVA-1.5 as representative examples and expose systematic flaws rooted in their
visual encoding strategy. To address the challenges, we present LLaVA-UHD, a
large multimodal model that can efficiently perceive images in any aspect ratio and
high resolution. LLaVA-UHD includes three key components: (1) An image modularization strategy that divides native-resolution images into smaller variable-sized
slices for efficient and extensible encoding, (2) a compression module that further
condenses image tokens from visual encoders, and (3) a spatial schema to organize
slice tokens for LLMs. Comprehensive experiments show that LLaVA-UHD outperforms established LMMs trained with 2-3 orders of magnitude more data on
9 benchmarks. Notably, our model built on LLaVA-1.5 336×336 supports 6 times
larger (i.e., 672×1088) resolution images using only 94% inference computation,
and achieves 6.4 accuracy improvement on TextVQA. Moreover, the model can be
efficiently trained in academic settings, within 23 hours on 8 A100 GPUs (vs. 26
hours of LLaVA-1.5)
