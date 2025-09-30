# msc_project_emotion_sensitivity

**MSc Project: Uncovering Emotional Cues in Online Interactions**

This repository contains all code, data, and outputs for the MSc Data Science dissertation:

**Uncovering Emotional Cues in Online Interactions: A Comparative Study of Human and AI Sensitivity Using Multimodal Data**

## Repository Structure

msc_project_emotion_sensitivity/
│
├── data/                     # Core dataset (CSV)
│   └── final_with_polarity_sbert.csv
│
├── annotation_forms/         # Human annotation survey inputs & responses
│
├── embeddings/               # Saved SBERT embeddings (.npy)
│
├── chapter4_results/         # Outputs (cluster exemplars, metrics, profiles, visuals)
│
├── chapter4_outputs/         # Intermediate model outputs
│
├── notebooks/                # All Jupyter notebooks
│   ├── 00_bootstrap_paths.ipynb      # MUST run first to set repo-aware paths
│   ├── reddit_data_scraper.ipynb
│   ├── dataset_twitter_communities.ipynb
│   ├── data_cleaning_1.ipynb
│   ├── data_cleaning_2.ipynb
│   ├── human_annotation_forms.ipynb
│   ├── analysis_clustering_annotation.ipynb
│   ├── 04_results_analysis.ipynb
│   └── 04_results_analysis_2.ipynb   # Main file to run
│
├── bertopic_outputs/         # Optional outputs for topic modeling
│
├── README.md                 # This file
└── requirements.txt          # List of dependencies


---

## Requirements

Install dependencies (Python 3.8+ recommended):

```bash
pip install -U sentence-transformers umap-learn scikit-learn pandas numpy matplotlib seaborn tqdm openpyxl

---

	How to Run

	1.	Clone the repo:

	git clone https://github.com/lbouz16/msc_project_emotion_sensitivity.git
  	cd msc_project_emotion_sensitivity

  2. Open Jupyter / Colab and run notebooks in this order:

  Preparation
	  •	notebooks/00_bootstrap_paths.ipynb
    → Sets up repo-aware paths (data/, embeddings/, chapter4_results/) so all notebooks run without manual path edits.
    Run this once at the start of your session.

  Data Collection & Cleaning
	  •	reddit_data_scraper.ipynb – Scrapes Reddit data.
	  •	dataset_twitter_communities.ipynb – Processes Twitter data.
	  •	data_cleaning_1.ipynb & data_cleaning_2.ipynb – Cleans and merges multimodal datasets.

  Human Annotation
	  •	human_annotation_forms.ipynb – Prepares annotation forms for survey participants.

  Clustering & Analysis
	  •	analysis_clustering_annotation.ipynb – Generates embeddings, clustering, and comparisons.
	  •	04_results_analysis.ipynb – Core results (k-sweep, cluster assignments, metrics, plots).
	  •	04_results_analysis_2.ipynb – Cluster profiling, exemplars, human vs AI comparison.

    Outputs:
		•	chapter4_results/:
	      •	k_sweep_metrics.csv (clustering performance metrics)
	      •	cluster_profiles.csv & cluster_profiles_readable.csv
	      •	cluster_exemplars_k8.csv
	      •	Figures (.png) for cluster sizes, platform/modality breakdowns
	    •	annotation_forms/:
	      •	annotation_items_form_A.csv / annotation_items_form_B.csv
	      •	annotation_key.csv
	    •	embeddings/:
	      •	sbert_embeddings.npy (cached SBERT embeddings for reproducibility)

  Reproducibility Notes
	•	All notebooks now use repo-relative paths via 00_bootstrap_paths.ipynb.
	•	No Google Drive mounting is required.
	•	Running end-to-end will regenerate embeddings, clusterings, and results.
	•	Cached embeddings in /embeddings/ ensure reproducibility without recomputation.

⸻

Contact

Author: Lina Bouziani
For questions, please reach out via GitHub issues or email (linabouziani@gmail.com)
    
