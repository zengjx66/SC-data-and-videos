# Fast VVC-SCC





## Key Features

VVC-SCC, Fast Intra Prediction Mode, Fast CU Partition

## Dataset

We provide the screen content video sequences and JVET CTC 444 test set used for CU partition label mining and evaluation. Please download from the following Baidu Pan links:

| Dataset | Description | Link | Extraction Code |
|---------|-------------|------|-----------------|
| **SCVEandCTC444** | Screen Content Video sequences + JVET CTC 444 test set (used for CU partition label mining & evaluation) | [Baidu Pan](https://pan.baidu.com/s/1FsvtasOoAEkTXZwpzHFvRw?pwd=a6tw) | `a6tw` |
| **VVC-SCC CU split Set** | Additional screen content sequences for training & BD-BR / ΔT testing | [Baidu Pan](https://pan.baidu.com/s/1SjE3yn_WtBRCTkFzhvfRjA?pwd=3zir) | `3zir` |
| **VVC-SCC intra mode  Set** | Additional screen content sequences for training & BD-BR / ΔT testing | [Baidu Pan](link:https://pan.baidu.com/s/1Db42L2WFqTgoaQOl3jK2eQ?pwd=gj2t ) | `gj2t` |
After downloading, organize the sequences according to your VTM encoding pipeline and update the sequence list file before running CU trace extraction.

## Citation
@article{zeng2025hffcnn,
  author  = {Zeng, Jiaxin and Chen, Jing and Zeng, Huanqiang and Zhang, Xudong and Lin, Qi},
  title   = {Hierarchical Feature Fusion CNN: Fast Intra Prediction Mode Decision for VVC Screen Content Coding},
  journal = {IEEE Signal Processing Letters},
  volume  = {32},
  pages   = {2229--2233},
  year    = {2025},
  publisher = {IEEE}
}


@article{chen2026mspcnn,
  author  = {Chen, Jing and Zeng, Jiaxin and Zeng, Huanqiang and Zhang, Xudong and Lin, Qi},
  title   = {Multi-Stage Prediction CNN: Fast CU Partition for VVC Screen Content Coding},
  journal = {IEEE Transactions on Multimedia},
  year    = {2026},
  doi     = {10.1109/TMM.2026.3680425}
}

