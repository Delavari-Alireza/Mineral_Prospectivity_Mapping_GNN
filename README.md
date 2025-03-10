# Mineral Prospectivity Mapping (MPM) Using Graph Neural Networks

This repository contains Python implementations of advanced graph neural network (GAT and GCN) models applied for Mineral Prospectivity Mapping (MPM). The primary goal is to predict and identify potential mineral deposit locations using graph neural network techniques.

## Project Overview

Mineral Prospectivity Mapping (MPM) is a critical step in mineral exploration, aiding exploration teams in efficiently identifying locations likely to contain mineral deposits. This project implements Graph Attention Networks (GAT) and Graph Convolutional Networks (GCN) to leverage spatial and geological data.

## Repository Content

- **deepGAT.ipynb**: Deep Graph Attention Network implementation.
  - **Accuracy:** Validation (~81%), Training (~94%).


- **GAT.ipynb**: Graph Attention Network implementation.


- **GCN.ipynb**: Simple Graph Convolutional Network implementation.
  - **Accuracy:** Validation (~91%), Training (~94%).



## Results

### Deep Graph Attention Network (DeepGAT)

<p align="center">
  <img src="/images/DeepGat-knn2.jpg" width="45%" />
  <img src="/images/DeepGat-knn5.jpg" width="45%" />
</p>

### Graph Attention Network (GAT)

<p align="center">
  <img src="/images/Gat-knn2.jpg" width="45%" />
  <img src="/images/Gat-knn5.jpg" width="45%" />
</p>

### Graph Convolutional Network (GCN)

<p align="center">
  <img src="/images/GCN-knn2.jpg" width="45%" />
</p>


## Data Used

Dataset: `label_deposit_nondeposit.csv` with geospatial fuzzy membership features and coordinates.

### Data Columns:
- **OBJECTID**, **pointid**: Identifiers.
- **Features**: `FuzzyMe_Eu`, `FuzzyMe_de`, `FuzzyMe_se`, `FuzzyMe_ar`, `FuzzyMe__1`, `FuzzyMe__2`
- **Coordinates**: (`x`, `y`)
- **Class label**: `class` (1 for mineral deposit, 0 for non-deposit)

## Key Libraries and Tools
- **PyTorch & PyTorch Geometric**
- **Scikit-learn**
- **StandardScaler**

## Project Workflow
1. **Data Preprocessing**: Normalization.
2. **Graph Construction**: KNN graph creation.
3. **Model Training**: GAT and GCN with dropout and early stopping.
4. **Validation & Prediction**: Model evaluation and prediction.

## Dependencies

Install via:
```bash
pip install torch torch-geometric pandas numpy sklearn
```

## Repository Structure
```
├── images
│   ├── deepGAT_result.png
│   ├── GAT_result.png
│   └── GCN_result.png
├── deepGAT.ipynb
├── GAT.ipynb
├── GCN.ipynb
├── label_deposit_nondeposit.csv
├── predicted_data_deepGAT_KNN2.xlsx
├── README.md
```

## Acknowledgements
Special thanks to **Mirakbar Seyedhamzeh** for invaluable guidance and data contributions.

## Contributions
Contributions and feedback are welcome. Please submit issues or pull requests.

## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
