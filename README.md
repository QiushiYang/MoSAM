<div align="center">
<img align="left" width="100" height="100" src="https://github.com/user-attachments/assets/1834fc25-42ef-4237-9feb-53a01c137e83" alt="">

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
