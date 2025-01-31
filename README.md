# BaliMask3D Dataset & Framework

## 📌 Overview
*BaliMask3D* is a dataset and framework designed to advance 3D object completion and reconstruction, specifically for *traditional Balinese masks. These masks, which hold deep cultural and artistic significance, have been digitized to support research in **3D reconstruction, deep learning, and cultural preservation*.

This project employs *360-degree photogrammetry, Signed Distance Fields (SDFs), and transformer-based architectures* (e.g., *VQ-VAE, SDFusion*) to reconstruct incomplete 3D data with high accuracy.

## 🔥 Features
- 📊 *High-Fidelity 3D Dataset: Traditional Balinese masks scanned using **structured light scanning & photogrammetry*.
- 🤖 *Transformer-Based 3D Completion: Implements **VQ-VAE* and *SDFusion* models for reconstructing missing 3D data.
- 🎭 *Cultural Heritage Digitalization: Contributes to preserving **Balinese artistic heritage* through digitization.
- 📏 *Evaluation Metrics: Assesses reconstructed masks using **Uniform Hausdorff Distance (UHD)* and *Topological Morphology Distance (TMD)*.
- 🏗 *Flexible Framework*: Includes data preprocessing, training pipelines, and evaluation scripts.

## 📂 Dataset Structure
```bash
BaliMask3D/
│── data/
│   ├── raw/                  # Raw 3D scans of Balinese masks
│   ├── processed/            # Preprocessed & normalized 3D models
│   ├── sdf/                  # Signed Distance Fields representations
│   ├── annotations/          # Metadata and labels
│
│── models/
│   ├── vqvae/                # VQ-VAE model implementation
│   ├── sdfusion/             # SDFusion architecture for 3D completion
│   ├── checkpoints/          # Pretrained model weights
│
│── scripts/
│   ├── preprocess.py         # Mesh normalization & SDF generation
│   ├── train.py              # Model training pipeline
│   ├── evaluate.py           # Performance evaluation (UHD, TMD)
│
│── notebooks/                # Jupyter notebooks for visualization & analysis
│── README.md                 # Project documentation
```

## 🚀 Installation
bash
# Clone repository
git clone https://github.com/TrianCode/Bali3DMask.git
cd Bali3DMask

# Create virtual environment
python -m venv balimask3d_env
source balimask3d_env/bin/activate  # For Linux/macOS
balimask3d_env\Scripts\activate    # For Windows

# Install dependencies
pip install -r requirements.txt


## 🔧 Usage
### 1️⃣ *Preprocess Data*
Convert raw 3D scans into normalized meshes and SDF representations.
bash
python scripts/preprocess.py --input data/raw --output data/processed


### 2️⃣ *Train Model*
Train *VQ-VAE* or *SDFusion* for 3D reconstruction.
bash
python scripts/train.py --model vqvae --epochs 100 --batch_size 16


### 3️⃣ *Evaluate Performance*
Assess reconstruction accuracy using UHD & TMD metrics.
bash
python scripts/evaluate.py --model vqvae --dataset data/processed


### 4️⃣ *Visualize 3D Models*
Use Jupyter Notebooks for visualization.
bash
jupyter notebook notebooks/visualize_results.ipynb


## 📊 Evaluation Metrics
- *Uniform Hausdorff Distance (UHD)*: Measures the geometric similarity between ground truth and reconstructed 3D models.
- *Topological Morphology Distance (TMD)*: Evaluates the structural consistency of completed models.


## 🤝 Contributing
We welcome contributions! Feel free to open an issue or submit a pull request:
1. *Fork the repo* and *clone it locally*.
2. Create a new *feature branch* (git checkout -b feature-branch).
3. Commit changes (git commit -m "Add new feature").
4. Push to the branch (git push origin feature-branch).
5. Open a *Pull Request*.

## 📜 License
This project is licensed under the *MIT License*. See the [LICENSE](LICENSE) file for details.

## 💡 Acknowledgments
This project is supported by *Institut Teknologi Sepuluh Nopember (ITS)* and contributors dedicated to cultural preservation and 3D research.

📧 *Contact:* [7025231008@student.its.ac.id]
(mailto:7025231008@student.its.ac.id) | [anny@its.ac.id](mailto:anny@its.ac.id) | [hadziq@its.ac.id](mailto:hadziq@its.ac.id)
