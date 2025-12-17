# CRISP-Real2Sim

```bash
git clone --recursive https://github.com/Z1hanW/CRISP-Real2Sim.git
cd CRISP-Real2Sim
```

---

## 1) Setup
### Create conda environment
```bash
conda create -n cps python=3.10 -y
conda activate cps
```

### Install PyTorch (CUDA 12.4)

```bash
pip install torch==2.4.1 torchvision==0.19.1 torchaudio==2.4.1 "xformers>=0.0.27" \
  --index-url https://download.pytorch.org/whl/cu124
  
pip install torch-scatter -f https://data.pyg.org/whl/torch-2.4.1+cu124.html
```

### (if failed to install) Install compiler toolchain

```bash
conda install -c conda-forge gxx_linux-64=11
```

### Install remaining dependencies

```bash
pip install -r requirements.txt
```

### Run extra install scripts (prep/)

```bash
cd prep
sh install*
cd ..
```

---

## 2) Download Data

Download the raw data into `./data`:

```bash
gdown --folder "https://drive.google.com/drive/folders/1k712Oj9StmWXRzSeSMiHZc3LtvsVk2Rw" -O data
```

---

---

## 4) Run Full Pipeline (Example)

If `all_gv.sh` is your main entry script:

```bash
sh all_gv.sh $PATH$

e.g. sh all_gv.sh 
```

---

## 5) Visualization Human-Scene Reconstruction

```bash
sh vis.sh <PATH_TO_RESULT>
```

> If your script supports flags (e.g., `--scene_name`, `--data_root`, `--out_dir`), document them here.

---

## 6) Train Your Agent

Code Testing ... 


---

## 7) Visualize Your Agent Directly

Code Testing ... 


---
