# SegMambaFuse

This is the official Pytorch implementation of the paper SegMambaFuse:  Multi-Level Attention and Adaptive Mamba Fusion for Medical Image Segmentation


## Usage:
### Recommended environment:
**Please run the following commands.**
```
conda create -n emcadenv python=3.8
conda activate emcadenv

pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113

pip install mmcv-full -f https://download.openmmlab.com/mmcv/dist/cu113/torch1.11.0/index.html

pip install -r requirements.txt

```

### Data preparation:
- **Synapse Multi-organ dataset:**
Download the processed Synapse dataset from the following  [drive link](https://drive.google.com/file/d/1tGqMx-E4QZpSg2HQbVq5W3KSTHSG0hjK/view?usp=share_link) or download the Synapse data following the Data preparation section of [EMCAD paper](https://github.com/SLDGroup/EMCAD/tree/main). Then move the Synapse dataset into the root path: ./data/Synapse

- **BTCV dataset:**
The dataset is publicly available on the Synapse website:  [https://www.synapse.org/Synapse:syn3193805/files/](https://www.synapse.org/Synapse:syn3193805/files/) and the preprocessing was conducted following the **Data preparation** procedure described in the [EMCAD repository](https://github.com/SLDGroup/EMCAD/tree/main). Move train and test images into the root path: data_sets/Synapse/dataset13classes and naming train and test: `train_npz_new`,`test_vol_h5_new` respectively

- **ACDC dataset:**
Download the preprocessed ACDC dataset from [Google Drive](https://drive.google.com/file/d/1CruCQ-jjvA97BX-LIYwXaRMLmp3DN9zc/view) and move it into './data/ACDC/' folder.

- **ISIC2017 datasets:**
Download the ISIC17 data at https://challenge.isic-archive.com/data/#2017. Move them (data_train.npy, mask_train.npy, data_val.npy, mask_val.npy, data_test.npy, test_mask.npy) into the root path: data_sets/ISIC2017/processe


- **ISIC2017 datasets:**
Download the ISIC17 data at https://challenge.isic-archive.com/data/#2017. Move them (data_train.npy, mask_train.npy, data_val.npy, mask_val.npy, data_test.npy, test_mask.npy) into the root path: data_sets/ISIC2017/processe

### Training:
```
cd into SegMambaFuse
python -W ignore train_synapse.py --root_path /path/to/train/data --volume_path path/to/test/data --encoder pvt_v2_b2         # replace --root_path and --volume_path with your actual path to data.

```

### Trained Weights on Synapse Dataset:
You can download the trained weights on Synapse dataset from [Google Drive](https://drive.google.com/drive/folders/1S-hxcgMlTFEX9GJGTUF7XWdZBGx7MiZl?usp=sharing).   

### Testing:
```
cd into SegMambaFuse 
```

## Acknowledgement
We are very grateful for these excellent works [timm](https://github.com/huggingface/pytorch-image-models), [CASCADE](https://github.com/SLDGroup/CASCADE), [MERIT](https://github.com/SLDGroup/MERIT), [G-CASCADE](https://github.com/SLDGroup/G-CASCADE), [PP-SAM](https://github.com/SLDGroup/PP-SAM), [PraNet](https://github.com/DengPingFan/PraNet), [Polyp-PVT](https://github.com/DengPingFan/Polyp-PVT) and [TransUNet](https://github.com/Beckschen/TransUNet), which have provided the basis for our framework.

## Citations

``` 
@inproceedings{bui2026SegMambaFuse,
  title={SegMambaFuse:  Multi-Level Attention and Adaptive Mamba Fusion for Medical Image Segmentation},

}
```
