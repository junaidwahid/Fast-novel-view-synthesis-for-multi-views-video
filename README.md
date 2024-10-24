# 🎥 Fast Novel View Synthesis for Multi-View Video

![HLCV1online-video-cutter com-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/070a5a5f-df6c-4f54-8327-79513b119006)

A lightning-fast approach for 3D video synthesis that transforms multi-view video recordings into novel viewpoint videos. Our method achieves an **850x speedup** compared to the previous state-of-the-art while maintaining good visual quality.

A deatil report can be found in the repository as Report.pdf file

## 🚀 Key Features

- **Ultra-Fast Processing**: Process a 10-second 30 FPS multi-view video (1K resolution) in just 1.5 hours
- **State-of-the-Art Performance**: Achieves 25.6 PSNR and 7.25 JOD score
- **Memory Efficient**: Uses optimized neural radiance fields for each frame
- **Smooth Output**: Implements continual training and video denoising for consistent results

## 📊 Performance Comparison

| Method | PSNR | JOD | Processing Time (GPU-Hours) |
|--------|------|-----|---------------------------|
| Ours (Setting 2 + Denoised) | 25.62 | 7.25 | 1.51 |
| DyNeRF | 29.59 | 8.07 | 1300 |

## 🏗️ Pipeline
![Capture](https://github.com/user-attachments/assets/747fb100-ffea-49bd-ba2e-48b49b58e8c9)

Our method consists of three main stages:
1. Frame-by-frame scene reconstruction using fast NeRF models
2. Novel view rendering for each frame
3. Video denoising for temporal consistency

## 📈 Results

Our method achieves significant speedup while maintaining good visual quality:

- **Setting 1**: Independent frame optimization (6.5 GPU hours)
  - PSNR: 26.2
  - JOD: 6.88

- **Setting 2**: Continual training (1.5 GPU hours)
  - PSNR: 25.37
  - JOD: 6.35

- **Setting 2 + Denoiser**: Best quality-speed trade-off
  - PSNR: 25.62
  - JOD: 7.25
  - Processing Time: 1.51 GPU hours

## 📝 Citation

If you find this work useful in your research, please consider citing:

```bibtex
@article{tran2024fast,
  title={Fast Novel View Synthesis for Multi-Views Video},
  author={Tran, Tuan Anh and Junaid},
  year={2024}
}
```

## 🙏 Acknowledgments

- Neural 3D Video Synthesis dataset from Li et al.
- FastDVDNet for video denoising
- Instant-NGP for fast neural rendering
