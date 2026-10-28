<!-- ============================================================
     MAINTAINER NOTES (delete this block before publishing)

     1. Every token wrapped in full-width brackets, e.g. 【paper-link】,
        is a placeholder — replace ALL of them before making the repo public:
        - 【repo-url】                 → this repository's URL (used in badges)
        - 【paper-link】               → the paper page (arXiv / DOI / venue)
        - 【code-link】                → the official code / weights release
                                          (replace with "—" if none exists)
        - 【survey-link】              → link for each related survey
        - 【affiliation】              → the organization behind a model
        - 【project-link】              → project homepage of the survey
        - 【venue】 / 【license】 / 【contact-email】 → self-explanatory
     2. LVGM status markers follow Table 2 of the survey:
        ✅ confirmed LVGM · 🔶 believed to be an LVGM · ❌ not an LVGM
     3. Benchmarks marked with † are not publicly released
        (per Table 5 of the survey).
     4. The 55 models / 27 benchmarks below are exactly those curated in
        the survey. When extending the list, mark entries that are new
        relative to the survey with a 🆕 badge and keep rows consistent.
     ============================================================ -->

# Awesome-LVGM

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: 【license】](https://img.shields.io/badge/License-【license】-blue.svg)](【repo-url】/blob/main/LICENSE)
[![Last Updated](https://img.shields.io/badge/Last_Updated-Oct_2026-green)](【repo-url】/commits)

A curated list of research on **Large Video Generative Models (LVGMs)**: surveys, representative models, and evaluation benchmarks.

> This repository accompanies the survey **"Large Video Generative Models: A Systematic Survey"** by Rui Zhang, Min Wang, Jiazhe Miao, Rongxuan Zhang, Zhirui Yang, Yulin Gong, and Yixin Su ([Huazhong University of Science and Technology](https://www.hust.edu.cn)). It will be continuously updated to track new LVGMs, benchmarks, and resources.
>
> - 📄 Paper: 【paper-link】
> - 🏠 Project page: 【project-link】

**What is an LVGM?** The survey formally defines a *Large Video Generative Model* as a video generative model that is:

1. pretrained on at least **10<sup>7</sup> image/video–text pairs**;
2. equipped with at least **10<sup>9</sup> (billion-level) parameters**;
3. capable of **zero-shot generation** on open-domain tasks such as text-to-video, image-to-video, and video editing; and
4. natively generating videos of **≥ 5 seconds at ≥ 720p**, with flexible duration, resolution, and aspect ratio.

Models such as Sora, Veo, Kling, Seedance, HunyuanVideo, and Wan fall within this scope, while most pre-2023 video generators do not.

## Contents

- [Surveys](#surveys)
- [Models](#models) — 55 representative models (2016–2026)
- [Benchmarks](#benchmarks) — 27 evaluation benchmarks
- [Contributing](#contributing)
- [Citation](#citation)
- [License](#license)

## Surveys

| Survey | Focus | Venue / Year | Link |
| --- | --- | --- | --- |
| ⭐ **Large Video Generative Models: A Systematic Survey** (this work) | LVGM definition, architectures, data construction, training, evaluation, and applications | 【venue】 · 2026 | 【paper-link】 |
| Video Generative Adversarial Networks: A Review | Video GANs | ACM Computing Surveys · 2022 | 【survey-link】 |
| A Survey on Video Diffusion Models | Video diffusion models | ACM Computing Surveys · 2024 | 【survey-link】 |
| A Comprehensive Survey on Text-to-Video Generation | Text-to-video generation | Chinese Journal of Electronics · 2025 | 【survey-link】 |
| Controllable Video Generation: A Survey | Controllable video generation | arXiv · 2025 | 【survey-link】 |
| Diffusion Model-Based Video Editing: A Survey | Diffusion-based video editing | International Journal of Computer Vision · 2026 | 【survey-link】 |
| A Comprehensive Survey on Human Video Generation | Human video generation | arXiv · 2024 | 【survey-link】 |
| Human Motion Video Generation: A Survey | Human motion video generation | IEEE TPAMI · 2025 | 【survey-link】 |
| Video Generation Models: A Survey of Post-Training and Alignment | Post-training and alignment | Transactions on Machine Learning Research · 2026 | 【survey-link】 |
| Evolution of Video Generative Foundations | Evolution of video generative foundations | arXiv · 2026 | 【survey-link】 |

## Models

55 representative video generation models and systems curated in the survey (2016–2026), ordered chronologically. Scale and output figures follow Table 2 of the survey (f = frames; † = with frame interpolation and/or super-resolution; NR = not reported).

**LVGM status:** ✅ confirmed LVGM · 🔶 believed to be an LVGM · ❌ not an LVGM

| Model | Affiliation | Year | Paper | Code | Notes |
| --- | --- | --- | --- | --- | --- |
| VideoGAN | MIT | 2016 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 32 f @ 64×64 |
| TGAN | U. Tokyo / Preferred Networks | 2016 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f @ 64×64 |
| MoCoGAN | USC / NVIDIA | 2017 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f (variable via recurrence) @ 64×64 |
| Vid2Vid | NVIDIA | 2018 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · duration matches input · ≤2048×1024 |
| VideoVAE | 【affiliation】 | 2018 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · NR |
| TGANv2 | U. Tokyo / Preferred Networks | 2018 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f · multiple aspect ratios |
| SVG | 【affiliation】 | 2018 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · short clips @ 64×64 |
| DVD-GAN | Google DeepMind | 2019 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · ≤48 f @ 256×256 |
| TGANv2-ODE | U. Tokyo / Preferred Networks | 2020 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · NR |
| NÜWA | Microsoft | 2021 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · ~4 s @ 336×336 · 2.9M IT / 241K VT |
| StyleGAN-V | Samsung AI | 2021 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · arbitrary length & fps @ 256–1024² |
| VideoGPT | UCSD | 2021 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f @ 64–128² |
| GODIVA | 【affiliation】 | 2021 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · short clips · ≥136M VT |
| CogVideo | Tsinghua / Zhipu AI | 2022 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 9.4B · short clips @ 480×480 · 5.4M VT |
| TATS | 【affiliation】 | 2022 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f (1024 f sliding) @ 128–256² |
| VDM | Google | 2022 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f @ 64×64 |
| MCVD | 【affiliation】 | 2022 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16/30 f, longer via AR |
| Make-A-Video | Meta | 2022 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 76 f† @ 768² · 2.3B IT + ~20M V |
| Imagen Video | Google | 2022 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · ~5.3 s† @ 1280×768 · 14M VT + 460M IT |
| MagicVideo | ByteDance | 2022 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f @ 256×256 |
| Gen-2 | Runway | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · ~4 s |
| NUWA-XL | Microsoft | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · ≤3376 f (hierarchical) |
| Video LDM | LMU Munich / Runway | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 113 f† @ 1280×2048 · 10.7M VT |
| Pika 1.0 | Pika Labs | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · ~3 s · multiple aspect ratios |
| AnimateDiff | 【affiliation】 | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 417M/453M · resolution bound to base T2I model |
| DragNUWA | Peking University / Microsoft Research | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · short clips · controllable motion generation |
| VideoCrafter1 | Tencent | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f @ 320×512–576×1024 · 10M VT + 600M IT |
| SVD | Stability AI | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · ~1.5B · 14/25 f @ 1024×576 |
| VideoPoet | Google | 2023 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 8B · 17/41 f, longer via AR† @ 896×512 |
| VideoCrafter2 | Tencent | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 16 f @ 320×512 |
| Sora | OpenAI | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · ≤60 s · up to 1080p · multiple aspect ratios |
| Open-Sora 1.0 | HPC-AI Tech | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 724M · 16 f (2 s) @ 512×512 |
| Veo 1 | Google DeepMind | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · >60 s @ 1080p |
| Kling 1.0 | Kuaishou | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 5/10 s (120 s extended) |
| CogVideoX | Zhipu AI / Tsinghua | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | ✅ (5B) · 2B/5B · 6–10 s @ 480–768p |
| Movie Gen | Meta | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | ✅ · 30B · 16 s @ 1080p† |
| HunyuanVideo | Tencent | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | ✅ · 13B · ~5 s @ 720p |
| Veo 2 | Google DeepMind | 2024 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · minute-scale · ≤4K |
| Wan 2.1 | Alibaba | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | ✅ (14B) · 1.3B/14B · ~5 s @ 480/720p |
| Open-Sora 2.0 | HPC-AI Tech | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | ✅ · 11B · ≤129 f @ 256/768 px · trained for ~$200K |
| Veo 3 | Google DeepMind | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 8 s @ 720/1080p |
| Seedance 1.0 | ByteDance | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 5/10 s · ≤1080p |
| Lumos-1 | 【affiliation】 | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | ❌ · 1B/3B · 60M IT + 10M VT @ 256–384p |
| Veo 3.1 | Google DeepMind | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 4/6/8 s @ 720p–4K† |
| Hailuo 2.3 | MiniMax | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 6/10 s · 1080p (6 s) / 768p (10 s) |
| Gen-4.5 | Runway | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 2–10 s @ 720p |
| Kling 2.6 | Kuaishou | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 5/10 s |
| Seedance 1.5 Pro | ByteDance | 2025 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · NR |
| Kling 3.0 | Kuaishou | 2026 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · ≤15 s |
| Vidu Q3 | Shengshu Technology | 2026 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 1–16 s @ 540–1080p |
| Seedance 2.0 | ByteDance | 2026 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · ≤15 s · world-model capability |
| Happy Horse | 【affiliation】 | 2026 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · NR |
| Gemini Omni 1.1 Flash | Google | 2026 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 3–10 s @ 360p–4K† |
| Wan 3.0 | Alibaba | 2026 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · 2–30 s @ 480–1080p |
| Seedance 2.5 | ByteDance | 2026 | [Paper](【paper-link】) | [Code](【code-link】) | 🔶 · ≤30 s |

## Benchmarks

27 evaluation benchmarks curated in the survey (Table 5), grouped by their primary evaluation measures. Benchmarks marked with **†** have not been publicly released at the time of the survey.

| Benchmark | Evaluation Focus | Venue / Year | Paper | Code |
| --- | --- | --- | --- | --- |
| FETV | Visual Quality · Prompt Adherence | NeurIPS · 2023 | [Paper](【paper-link】) | [Code](【code-link】) |
| EvalCrafter | Visual Quality · Prompt Adherence · Composition · Motion | CVPR · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| VBench | Visual Quality · Prompt Adherence · Composition · Motion | CVPR · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| MiraBench | Visual Quality · Motion · Physical Plausibility | NeurIPS · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| Video-Bench | Visual Quality · Prompt Adherence | CVPR · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| Wan-Bench † | Visual Quality · Prompt Adherence · Composition · Motion · Physical Plausibility | Tech Report · 2025 | [Paper](【paper-link】) | — |
| GenAI-Bench | Prompt Adherence · Composition | ECCV · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| T2V-CompBench | Composition | CVPR · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| WorldModelBench | Prompt Adherence · Physical Plausibility | NeurIPS · 2026 | [Paper](【paper-link】) | [Code](【code-link】) |
| DEVIL | Motion | NeurIPS · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| VBench++ | Motion · Reference · Safety | IEEE TPAMI · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| WorldScore | Motion · Physical Plausibility | ICCV · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| SeedVideoBench-1.0 † | Motion · Reference | Tech Report · 2025 | [Paper](【paper-link】) | — |
| OpenS2V-Eval | Reference Consistency | NeurIPS · 2026 | [Paper](【paper-link】) | [Code](【code-link】) |
| MSVBench | Reference · Narrative | arXiv · 2026 | [Paper](【paper-link】) | [Code](【code-link】) |
| SeedVideoBench-2.0 † | Reference · Narrative · Multimodal Coherence | Tech Report · 2026 | [Paper](【paper-link】) | — |
| OmniVideo-1.0 † | Reference · Physical Plausibility | Tech Report · 2025 | [Paper](【paper-link】) | — |
| StoryEval | Narrative | CVPR · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| T2VBench | Narrative | CVPR · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| VBench-2.0 | Narrative · Physical Plausibility | arXiv · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| VIDEOPHY | Physical Plausibility | ICLR · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| VIDEOPHY-2 | Physical Plausibility | arXiv · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| ChronoMagic-Bench | Physical Plausibility (state changes) | NeurIPS · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| TAVGBench | Multimodal Coherence | ACM MM · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |
| VABench | Multimodal Coherence | CVPR · 2026 | [Paper](【paper-link】) | [Code](【code-link】) |
| T2AV-Compass | Multimodal Coherence | arXiv · 2025 | [Paper](【paper-link】) | [Code](【code-link】) |
| T2VSafetyBench | Safety | NeurIPS · 2024 | [Paper](【paper-link】) | [Code](【code-link】) |

## Contributing

This repository is still a work in progress and will be updated regularly. Contributions are welcome!

- **Adding new papers/models**: please open a pull request or an issue with the paper title, affiliation, year, and a brief summary highlighting the key techniques.
- **Entry format**: follow the existing tables — one row per entry, with `Paper` and `Code` links wherever available.
- **Corrections**: if you spot a mistake (venue, year, affiliation, or scale figure), please open an issue or submit a PR; feedback is greatly appreciated.
- **Contact**: you can also reach the maintainers at 【contact-email】.

## Citation

If you find this survey or repository useful, please consider citing:

```bibtex
@article{zhang2026lvgm,
  author  = {Zhang, Rui and Wang, Min and Miao, Jiazhe and Zhang, Rongxuan and
             Yang, Zhirui and Gong, Yulin and Su, Yixin},
  title   = {Large Video Generative Models: A Systematic Survey},
  journal = {【venue, e.g., ACM Computing Surveys】},
  year    = {2026}
}
```

## License

This repository is released under the 【license, e.g., MIT / CC BY 4.0】 license. All model and benchmark resources listed here remain the property of their respective authors and organizations.

---

Maintained by 【team name】 · Last updated: October 2026


---
*AI生成*
# Awesome-LVGMs
