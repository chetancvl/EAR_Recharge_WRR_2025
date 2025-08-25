# EAR_Recharge_WRR_2025
This repository contains the code, input data, and outputs used for the recharge modeling study of the Bexar and Nueces basins in the Edwards Aquifer Region, Texas, USA.
The workflow uses machine learning and deep learning models (ERT, RF, XGBoost, HGB, CNN) to predict recharge and validate against hydrological models and GRACE data.  

## 📂 Repository Structure
├── Bexar_TWBD/ # Code and outputs for Bexar basin
│ └── Results_Bexar/ # Model outputs
│ ├── Data_English_Units_Data/
│ ├── Data_SI_Units/
│ ├── Figures_English_Units/
│ └── Figures_SI_Units/
├── Nueces_TWBD/ # Code and outputs for Nueces basin
│ └── Results_Nueces/ # Model outputs
│ ├── Data_English_Units_Data/
│ ├── Data_SI_Units/
│ ├── Figures_English_Units/
│ └── Figures_SI_Units/
├── Data/ # Input datasets (Daymet, CMIP, GRACE, Observed, etc.)
├── Manuscript_Figures/ # Final figures used in the manuscript
├── Post_processor_Figures_for_WRR_ms.ipynb # Post-processing notebook
├── EAR_Recharge_Manuscript_code.py # Script to run all notebooks in order
└── README.md

## ▶️ Running the Workflow
1. **Download and unzip** the repository into any folder on your system.
2.  **Set up the environment**
3. **Run the pipeline**:
    ```bash
    python EAR_Recharge_Manuscript_code.py
  
  This will:
    1. Execute Bexar_TWBD/Aquifer_Recharge_Bexar.ipynb
    2. Execute Nueces_TWBD/Aquifer_Recharge_Nueces.ipynb
    3. Execute Post_processor_Figures_for_WRR_ms.ipynb
    
  Outputs will be saved under each basin’s Results_* folders and manuscript figures under Manuscript_Figures/.
  
##  ⚙️ Environment
This project was developed and tested with the following software versions:
JupyterLab: 4.2.5
Python: 3.10.13
pandas: 2.2.2
numpy: 1.24.3
scikit-learn: 1.5.1
xgboost: 2.1.1
shap: 0.45.1
joblib: 1.4.2
tensorflow: 2.17.0
h5py: 3.11.0
matplotlib: 3.9.2
seaborn: 0.13.2
plotly: 5.24.0
scipy: 1.14.1
statsmodels: 0.14.2
Other standard libraries: tqdm, dateutil, IPython, PIL, prettytable, tabulate.

# Notes for Readers
The repository uses relative paths (Path(__file__)), so after unzipping, no path edits are required.
Large outputs are stored in the Results_* folders; manuscript-ready figures are in Manuscript_Figures/.
The individual .ipynb files and output can be accessed with JupyterLab.
