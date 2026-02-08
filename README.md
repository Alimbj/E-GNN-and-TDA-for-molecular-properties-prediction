# QM9 Dataset Analysis and Molecular Property Prediction

## 📊 Dataset: QM9
The **QM9 dataset** (Quantum Machine 9) contains 130,831 small organic molecules with up to 9 heavy atoms (C, N, O, F). Each molecule includes:
- **3D atomic coordinates** (`pos`): Cartesian coordinates
- **Atomic numbers** (`z`): Element types (1=H, 6=C, 7=N, 8=O, 9=F)
- **Molecular graph** (`edge_index`): Chemical bond connectivity
- **19 quantum mechanical properties** (`y`): Including HOMO-LUMO gap

**Target Property**: HOMO-LUMO gap (property index 4)

## 📊 Data Processing
- **Dataset split**: 80% train, 10% validation, 10% test
- **Data normalization**: Centered 3D coordinates
- **Target selection**: HOMO-LUMO gap extraction

## 🔍 Exploratory Data Analysis
### Chemical Composition Analysis
- Atomic composition distribution (H, C, N, O, F counts)
- Molecular size analysis
- Chemical class classification (hydrocarbons, heteroatom-containing)
- C/H ratio correlation with target property

### Statistical Analysis
- HOMO-LUMO gap distribution statistics
- Normality testing (Shapiro-Wilk)
- Multi-modality detection
- Correlation analysis between features

### Dimensionality Reduction
- UMAP projection of molecular features
- 2D visualization colored by:
  - HOMO-LUMO gap values
  - Chemical composition
  - Molecular size categories

### Feature Importance
- Random Forest feature ranking

## 🧠 Model Training
Three geometric deep learning architectures implemented:

### 1. SchNet
- Continuous-filter convolutional layers
- Translation and rotation invariant

### 2. DimeNet++
- Directional message passing
- Angular information incorporation

### 3. EGNN (Equivariant Graph Neural Network)
- SE(3)-equivariant architecture
- Coordinate updates during message passing

## 📄 License
MIT License


