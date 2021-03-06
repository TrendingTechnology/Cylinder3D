
# Cylindrical and Asymmetrical 3D Convolution Networks for LiDAR Segmentation

 The source code of our work **"Cylindrical and Asymmetrical 3D Convolution Networks for LiDAR Segmentation**
![img|center](./img/pipeline.png)

## News
- **2020-11** We preliminarily release the Cylinder3D--v0.1, supporting the LiDAR semantic segmentation on SemanticKITTI and nuScenes.
- **2020-11** Our work achieves the **1st place** in the leaderboard of SemanticKITTI semantic segmentation (until CVPR2021 DDL, still rank 1st in term of Accuracy now), and based on the proposed method, we also achieve the **1st place** in the leaderboard of SemanticKITTI panoptic segmentation.
<p align="center">
        <img src="./img/leaderboard.png" width="40%"> 
</p>

## Installation

### Requirements
- PyTorch >= 1.2 
- yaml
- Cython
- [torch-scatter](https://github.com/rusty1s/pytorch_scatter)
- [nuScenes-devkit](https://github.com/nutonomy/nuscenes-devkit) (optional for nuScenes)
- [spconv](https://github.com/traveller59/spconv)

## Data Preparation

### SemanticKITTI
```
./
├── 
├── ...
└── path_to_data_shown_in_config/
    ├──sequences
        ├── 00/           
        │   ├── velodyne/	
        |   |	├── 000000.bin
        |   |	├── 000001.bin
        |   |	└── ...
        │   └── labels/ 
        |       ├── 000000.label
        |       ├── 000001.label
        |       └── ...
        ├── 08/ # for validation
        ├── 11/ # 11-21 for testing
        └── 21/
	    └── ...
```

### nuScenes
```
./
├── 
├── ...
└── path_to_data_shown_in_config/
		├──v1.0-trainval
		├──v1.0-test
		├──samples
		├──sweeps
		├──maps

```

## Training
1. modify the config/semantickitti.yaml with your custom settings. We provide a sample yaml for SemanticKITTI.
2. train the network by running "sh train.sh".


### Pretrained Models
-- We provide a pretrained model for SemanticKITTI [LINK1](https://drive.google.com/file/d/1q4u3LlQXz89LqYW3orXL5oTs_4R2eS8P/view?usp=sharing) or [LINK2](https://pan.baidu.com/s/1c0oIL2QTTcjCo9ZEtvOIvA) (access code: xqmi)

## TODO List
- [ ] Release pretrained model for nuScenes.
- [ ] Support more models, including PolarNet, RandLA, SequeezeV3 and etc.
- [ ] Support more datasets, including A2D2 and etc.  
- [ ] Integrate LiDAR Panoptic Segmentation into the codebase.

## Acknowledgments
We thanks for the opensource codebases, [PolarSeg](https://github.com/edwardzhou130/PolarSeg)  and [SPVNAS](https://github.com/mit-han-lab/e3d)
