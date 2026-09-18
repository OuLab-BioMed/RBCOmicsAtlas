# RBCOmicsAtlas

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub repo](https://img.shields.io/badge/GitHub-OuLab--BioMed%2FRBCOmicsAtlas-green.svg)](https://github.com/OuLab-BioMed/RBCOmicsAtlas)
[![Web Server](https://img.shields.io/badge/Online-Analysis%20Platform-blue.svg)]()

> Source code for the **RBC Integrative Omics Atlas** — an online web server for multi-omics integration and analysis of red blood cells (erythrocytes) across human diseases.

## Overview

The **RBC Integrative Omics Atlas** is an online platform developed by **OuLab** for the integrative multi-omics analysis of red blood cells (RBCs / erythrocytes) across a wide range of human diseases. It consolidates transcriptomic, proteomic, metabolomic, and lipidomic data from RBCs to enable researchers to explore how RBC biology is altered in disease states.

### Why RBCs?

Red blood cells are the most abundant cell type in human blood and play roles far beyond oxygen transport — including immune modulation, nitric oxide metabolism, and systemic metabolic buffering. Dysregulation of RBC omics profiles has been implicated in numerous diseases.

## Features

- **Multi-omics integration** — combine transcriptome, proteome, metabolome, and lipidome of RBCs
- **Disease comparison** — compare RBC omics profiles across multiple disease conditions
- **Differential analysis** — identify dysregulated genes, proteins, and metabolites
- **Pathway & network** — enriched pathways, protein-protein interaction networks, and metabolite–gene networks
- **Cell-type deconvolution** — estimate RBC subtype composition from bulk profiles
- **Survival & clinical correlation** — link RBC omics signatures with patient outcomes
- **Interactive visualization** — heatmaps, volcano plots, UMAP/t-SNE, circos plots, and networks
- **Download & export** — export results and publication-quality figures

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vue 3 / React, ECharts, D3.js, Plotly |
| Backend | Python (FastAPI / Flask) or R (Plumber) |
| Database | PostgreSQL + Redis cache |
| Analysis | R (limma, WGCNA, clusterProfiler), Python (scanpy, scikit-learn) |
| Deployment | Docker, Nginx |

## Installation & Local Deployment

### Prerequisites

- Node.js >= 16
- Python >= 3.9 or R >= 4.1
- Docker & Docker Compose (recommended)

### Quick Start with Docker

```bash
# Clone the repository
git clone https://github.com/OuLab-BioMed/RBCOmicsAtlas.git
cd RBCOmicsAtlas

# Start all services
docker-compose up -d

# Access the platform
# Open http://localhost:8080 in your browser
```

### Manual Setup

```bash
# Backend
cd backend
pip install -r requirements.txt
python app.py          # starts API server on :5000

# Frontend (new terminal)
cd frontend
npm install
npm run dev            # starts dev server on :3000
```

## Project Structure

```
RBCOmicsAtlas/
├── frontend/              # Frontend source code
│   ├── src/
│   │   ├── views/         # Page components
│   │   ├── components/    # Reusable components
│   │   ├── api/           # API calls
│   │   └── utils/         # Utilities
│   ├── public/
│   └── package.json
├── backend/               # Backend API server
│   ├── app.py
│   ├── routes/            # API endpoints
│   ├── analysis/          # Analysis scripts (R + Python)
│   ├── models/            # Data models
│   └── requirements.txt
├── database/              # Database schemas & seed data
│   ├── schema.sql
│   └── seed/
├── docker/                # Docker configuration
│   ├── Dockerfile
│   └── docker-compose.yml
├── docs/                  # Documentation
├── tests/                 # Test suite
└── README.md
```

## Data Sources

The RBC Integrative Omics Atlas integrates data from:

- Public RBC transcriptomic datasets (GEO, ArrayExpress)
- RBC proteomic studies (ProteomeXchange, PRIDE)
- RBC metabolomic and lipidomic datasets (MetaboLights)
- Published single-cell RBC atlases
- Clinical metadata with patient outcomes

> All data is de-identified and used in compliance with data use agreements. See our [data policy](docs/DATA_POLICY.md) for details.

## Citation

If you use the RBC Integrative Omics Atlas in your research, please cite:

> Shen K-C, Ou [PI Name]. *RBCOmicsAtlas: An online web server for multi-omics analysis of red blood cells across human diseases.* [Journal], 2026. DOI: [pending]

```bibtex
@article{shen2026rbcomicsatlas,
  title   = {RBCOmicsAtlas: An online web server for multi-omics analysis of red blood cells across human diseases},
  author  = {Shen, Kai-Cheng and Ou, [PI Name]},
  journal = {[Journal Name]},
  year    = {2026},
  doi     = {[DOI pending]}
}
```

You can also click the **"Cite this repository"** button on the GitHub repo page.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## Contact

- **Doc.KCshen** (Kai-Cheng Shen) — [kaichengshen2@qq.com](mailto:kaichengshen2@qq.com)
- **OuLab** — BioMedical Institute
- **Issues**: [GitHub Issues](https://github.com/OuLab-BioMed/RBCOmicsAtlas/issues)

---

<p align="center">
  <sub>Built with ❤️ by <a href="https://github.com/OuLab-BioMed">OuLab-BioMed</a></sub>
</p>
