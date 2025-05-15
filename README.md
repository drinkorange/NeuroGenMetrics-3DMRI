# NeuroGenMetrics‑3DMRI

> *Pre‑trained feature extractors and reference pipelines for computing FID and LPIPS on 3D MRI volumes — **code coming soon***.

---

## 🌟 Motivation

Quantitatively evaluating generative models on volumetric medical images is still tricky.
While 2D natural‑image models such as **Inception‑V3** (FID) and **AlexNet/VGG** (LPIPS) work great for photographs, they ignore domain‑specific texture and physiology in 3D MRI scans.

**NeuroGenMetrics‑3DMRI** will provide:

| Component                                                                | Status        |
| ------------------------------------------------------------------------ | ------------- |
| 🧠 3D ResNet trained on large multi‑site T1/T2 datasets                  | `coming soon` |
| 📈 Drop‑in FID‑3D & LPIPS‑3D scripts (PyTorch)                           | `coming soon` |
| 🔬 Benchmark configs                                                     | `coming soon` |

---

## 🚀 Quick Start

Code will be released as a standard Git repository. Once the first public commit lands you can try it out like this:

```bash
# clone the repo
git clone https://github.com/drinkorange/NeuroGenMetrics-3DMRI.git
cd NeuroGenMetrics-3DMRI

# create and activate an isolated environment
conda create -n neurogenmetrics3d python=3.11 -y
conda activate neurogenmetrics3d

# install Python dependencies
pip install -r requirements.txt

# (optional) fetch pretrained checkpoints
./scripts/download_checkpoints.sh
```

> **Note:** Checkpoints  will be uploaded in the v0.1.0 tag. Stay tuned!

---

## 🔑 Key Features

* **Domain‑aware backbone** — 3D ResNet pre‑trained on >5 k multi‑site brain MRIs.
* **Drop‑in API** — one‑liner wrappers to compute *FID‑3D* and *LPIPS‑3D* for any PyTorch tensor `(B, C, D, H, W)`.
* **Batch & patch mode** — memory‑efficient evaluation of large volumes with optional sliding‑window.

---

## 📂 Dataset Compatibility

This repo is *modality‑agnostic* as long as inputs are single‑channel 3D volumes scaled to `[0, 1]`.

| Modality | Tested? | Notes                                                  |
| -------- | ------- | ------------------------------------------------------ |
| T1‑w     | ✅       | default training domain                                |
| T2‑w     | ✅       | minor contrast shift handled by adaptive normalization |
| FLAIR    | 🚧      | support planned in v0.2                                |
| DWI/ADC  | 🚧      | experimental branch ongoing                            |

---

---

## 📅 Roadmap

* [x] **Internal pre‑training completed**
* [ ] **Open‑source cleanup & refactor** — tidy code, add tests & docs
* [ ] **v0.1.0 Release** — inference‑only checkpoints + FID/LPIPS scripts
* [ ] **Multi‑modal support** — integrate FLAIR & DWI modalities
* [ ] **Paper / tech report submission**

---

## 🤝 Contributing

Contributions and constructive feedback are welcome after the first public release. Please open an issue to discuss major changes before submitting a PR.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for the complete license text.

---

<p align="center">
  <em>Code is on the way – watch ★ and stay tuned!</em>
</p>

