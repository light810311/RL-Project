# CrowdNav Project Setup and Execution Specification

This document specifies the steps required to set up and run the CrowdNav project (Crowd-aware Robot Navigation with Attention-based Deep Reinforcement Learning).

## 1. System Requirements
- Ubuntu 22.04+ (or compatible Linux)
- Node.js v20+ (for OpenSpec)
- Python 3.10+
- CMake (for building RVO2)

## 2. Installation Steps

### 2.1 Node.js and OpenSpec
If Node.js is outdated, upgrade it using NodeSource:
```bash
curl -fsSL https://deb.nodesource.com/setup_20.x | sudo bash -
sudo apt-get install -y nodejs
sudo npm install -g @fission-ai/openspec@latest
```

### 2.2 Python Environment and Dependencies
Install core build tools and dependencies:
```bash
pip install cython
```

### 2.3 Build and Install Python-RVO2
```bash
cd Python-RVO2
python3 setup.py build_ext --inplace
python3 setup.py install --user
cd ..
```

### 2.4 Install CrowdNav
Install the project in editable mode:
```bash
pip install -e .
```

## 3. Execution Guide

### 3.1 Training a Policy
To train the SARL policy (default setting in the paper):
```bash
cd crowd_nav
python3 train.py --policy sarl
```
The logs and weights will be saved in `data/output/`.

### 3.2 Testing a Policy
To test the trained policy:
```bash
cd crowd_nav
python3 test.py --policy sarl --model_dir data/output --phase test
```

### 3.3 Visualizing Results
To run a specific test case with visualization:
```bash
cd crowd_nav
python3 test.py --policy sarl --model_dir data/output --phase test --visualize --test_case 0
```

## 4. Verification
- Verify `rvo2` installation: `python3 -c "import rvo2; print(rvo2.__file__)"`
- Verify `openspec` installation: `openspec --version`
