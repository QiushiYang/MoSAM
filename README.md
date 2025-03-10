<<<<<<< HEAD
<div align="center">

# MoSAM: Motion-Guided Segment Anything for Videos with Spatial-Temporal Memory Selection

[Qiushi Yang](https://qiushiyang.github.io/), [Yuan Yao](https://scholar.google.com/citations?user=mpwXqNoAAAAJ&hl=zh-CN), [Miaomiao Cui](https://scholar.google.com/citations?user=C-7UhS9dBroC&hl=zh-CN), [Liefeng Bo](https://scholar.google.com/citations?user=FJwtMf0AAAAJ&hl=en)

[Tongyi Lab, Alibaba](https://tongyi.aliyun.com/welcome) 
</div>

[[Arxiv]](https://github.com/QiushiYang/MoSAM) [[Project Page]](https://github.com/QiushiYang/MoSAM)

This repository is the official implementation of MoSAM: Motion-Guided Segment Anything for Videos with Spatial-Temporal Memory Selection

## Getting Started

#### MoSAM Installation 

SAM 2 needs to be installed first before use. The code requires `python>=3.10`, as well as `torch>=2.3.1` and `torchvision>=0.18.1`. Please follow the instructions [here](https://github.com/facebookresearch/sam2?tab=readme-ov-file) to install both PyTorch and TorchVision dependencies. You can install **the MoSAM version** of SAM 2 on a GPU machine using:
```
cd sam2
pip install -e .
pip install -e ".[notebooks]"
```

Please see [INSTALL.md](https://github.com/facebookresearch/sam2/blob/main/INSTALL.md) from the original SAM 2 repository for FAQs on potential issues and solutions.

Install other requirements:
```
pip install matplotlib==3.7 tikzplotlib jpeg4py opencv-python lmdb pandas scipy loguru
```

#### SAM 2.1 Checkpoint Download

```
cd checkpoints && \
./download_ckpts.sh && \
cd ..
```

#### Main Inference
```
python scripts/main_inference.py 
```

### Input is Video File

```
python scripts/demo.py --video_path <your_video.mp4> --txt_path <path_to_first_frame_bbox.txt>
```

### Input is Frame Folder
```
# Only JPG images are supported
python scripts/demo.py --video_path <your_frame_directory> --txt_path <path_to_first_frame_bbox.txt>
```

## Acknowledgment

MoSAM is built on top of [SAM 2](https://github.com/facebookresearch/sam2?tab=readme-ov-file) by Meta FAIR. 

The comparisons and this website are also inspired by the concurrent works, [SAMURAI](https://yangchris11.github.io/samurai/) and [SAM2Long](https://github.com/Mark12Ding/SAM2Long)

The VOT evaluation code is modifed from [VOT Toolkit](https://github.com/votchallenge/toolkit) by Luka Čehovin Zajc.

## Citation

Please consider citing our paper and the wonderful `SAM 2` if you found our work interesting and useful.
```
@article{ravi2024sam2,
  title={SAM 2: Segment Anything in Images and Videos},
  author={Ravi, Nikhila and Gabeur, Valentin and Hu, Yuan-Ting and Hu, Ronghang and Ryali, Chaitanya and Ma, Tengyu and Khedr, Haitham and R{\"a}dle, Roman and Rolland, Chloe and Gustafson, Laura and Mintun, Eric and Pan, Junting and Alwala, Kalyan Vasudev and Carion, Nicolas and Wu, Chao-Yuan and Girshick, Ross and Doll{\'a}r, Piotr and Feichtenhofer, Christoph},
  journal={arXiv preprint arXiv:2408.00714},
  url={https://arxiv.org/abs/2408.00714},
  year={2024}
}
@article{yao2025towards,
  title={Towards Fine-grained Interactive Segmentation in Images and Videos},
  author={Yao, Yuan and Yang, Qiushi and Cui, Miaomiao and Bo, Liefeng},
  journal={arXiv preprint arXiv:2502.09660},
  year={2025}
}
```
=======
# Nerfies

This is the repository that contains source code for the [Nerfies website](nerfies.github.io).

If you find Nerfies useful for your work please cite:
```
@article{park2020nerfies
  author    = {Park, Keunhong and Sinha, Utkarsh and Barron, Jonathan T. and Bouaziz, Sofien and Goldman, Dan B and Seitz, Steven M. and Martin-Brualla, Ricardo},
  title     = {Deformable Neural Radiance Fields},
  journal   = {arXiv preprint arXiv:2011.12948},
  year      = {2020},
}
```

# Website License
<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This website is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.
>>>>>>> 49c0730 (Add README.)
