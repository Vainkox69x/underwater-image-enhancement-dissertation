# Underwater Image Enhancement with Rectified Flow

MSc Data Science and Environmental Intelligence dissertation, University of Plymouth.

Deep learning based enhancement of degraded underwater images using rectified flow matching in PyTorch, comparing Swin Transformer and DINOv2 backbones.

## Overview

Underwater images suffer from colour cast, low contrast, haze and loss of detail caused by light absorption and scattering. This project investigated whether flow matching, specifically rectified flow, can restore these images. Two transformer backbones were compared: a Swin Transformer paired with a denoising diffusion model (DDPM), and DINOv2 paired with rectified flow and exponential moving average (EMA) weights. Performance was assessed through quantitative metrics and qualitative visual comparison.

Future work will focus on a faster, lightweight model that can be integrated into real world underwater imaging systems.

## Repository structure

```
.
├── UIEB_rectifiedflow.ipynb     Main notebook: rectified flow with DINOv2 and EMA
├── rf+dinov2+ema/
│   ├── Results_test/            Enhanced outputs for the test set
│   ├── Results_valid/           Validation visualisations (every 10 epochs) and loss curve
│   └── metrics/results.txt      Quantitative evaluation results
├── RF+DINOv2+EMA(VSD-Net-main...)   [describe this file or folder]
└── README.md
```

## Methods

| Component | Description |
|---|---|
| Framework | PyTorch |
| Generative model | Rectified flow (flow matching) |
| Backbone | DINOv2 |
| Comparison model | Swin Transformer with DDPM |
| Training stabilisation | Exponential moving average of weights |
| Dataset | Underwater Image Enhancement Benchmark (UIEB) |

## Results

Quantitative results are stored in `rf+dinov2+ema/metrics/results.txt`. The training loss curve is at `rf+dinov2+ema/Results_valid/loss_per_epoch.png`.

| Method | PSNR | SSIM | [UIQM] | [UCIQE] |
|---|---|---|---|---|
| [DDPM + Swin] | [ ] | [ ] | [ ] | [ ] |
| [Rectified flow + DINOv2 + EMA] | [ ] | [ ] | [ ] | [ ] |

Qualitative examples are in `rf+dinov2+ema/Results_test/`.

`UIEB_rectifiedflow.ipynb`.

