# Fast VVC-SCC: Efficient Intra Coding for Screen Content

A collection of learning-based fast intra coding methods for **Versatile Video Coding Screen Content Coding (VVC-SCC)**, targeting two core bottlenecks of the VTM encoder:

| Task | Method | Venue |
|------|--------|-------|
| Fast CU Partition | **MSP-CNN** (Multi-Stage Prediction CNN) | IEEE TMM 2026 |
| Fast Intra Mode Decision | **HFF-CNN** (Hierarchical Feature Fusion CNN) | IEEE SPL 2025 |

Both methods are proposed by the Huaqiao University team (Zeng Huanqiang, Chen Jing, Zeng Jiaxin et al.) and focus on reducing VTM intra encoding complexity for screen content (graphics, UI, text-overlay) with negligible RD degradation.

## Key Features

- **MSP-CNN** — Multi-stage CNN (one subnet per CU depth 64→32→16→8→4) taking luma CU + normalized QP as input, predicting QTMT partition-mode probabilities (NS/QT/BTH/BTV/TTH/TTV) to early-terminate RDO recursion. **~46.9% intra encoding time reduction.**
- **HFF-CNN** — Hierarchical feature fusion CNN with multi-scale convolution + SE channel attention, directly predicting the best intra prediction mode (from 67 angular + IBC + PLT candidates) to skip unnecessary RMD/RDO searches. **~36.6% intra encoding time reduction.**

## Dataset

We provide the screen content video sequences used for CU partition label mining, intra-mode decision training, and BD-BR / ΔT evaluation. Please download from the following Baidu Pan links:

| Dataset | Description | Link | Extraction Code |
|---------|-------------|------|-----------------|
| **SCVEandCTC444** | Screen Content Video sequences + JVET CTC 444 test set (CU partition label mining & evaluation) | [Baidu Pan](https://pan.baidu.com/s/1FsvtasOoAEkTXZwpzHFvRw?pwd=a6tw) | `a6tw` |
| **VVC-SCC CU split Set** | Additional screen content sequences for CU partition training & BD-BR / ΔT testing | [Baidu Pan](https://pan.baidu.com/s/1SjE3yn_WtBRCTkFzhvfRjA?pwd=3zir) | `3zir` |
| **VVC-SCC Intra Mode Set** | Additional screen content sequences for intra-mode decision training & BD-BR / ΔT testing | [Baidu Pan](https://pan.baidu.com/s/1Db42L2WFqTgoaQOl3jK2eQ?pwd=gj2t) | `gj2t` |

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

