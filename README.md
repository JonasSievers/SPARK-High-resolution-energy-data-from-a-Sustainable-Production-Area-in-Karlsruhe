# SPARK: High-resolution energy data from a Sustainable Production Area in Karlsruhe

## Abstract: 
Understanding and optimizing industrial energy systems requires datasets that capture detailed electrical behavior at high temporal resolution over long time periods. Such data are essential for analyzing power quality, identifying operational patterns, and developing data-driven models for forecasting, control, and predictive maintenance.
Yet, most existing open datasets lack the temporal granularity, measurement diversity, and machine-level detail needed to reflect the complexity of industrial environments.
To address this gap, we present a large-scale, high-resolution dataset of industrial electricity measurements comprising more than 74 billion data points collected at 5-second resolution over up to seven years. The dataset includes 22 industrial machines and one photovoltaic system, with up to 190 measured quantities per device, including three-phase voltages and currents, active, reactive, and apparent power, harmonic spectra, total harmonic distortion, and fundamental waveform characteristics.
This unique combination of long-term coverage, high sampling rate, and rich feature space enables unprecedented insight into industrial energy dynamics and provides a robust foundation for advancing machine learning, digital twins, and intelligent energy management in industrial environments.

## Repository Structure
```text
├── dataset/                         # NOT ON GITHUB (must be downloaded before)
├── dataset_clean/                   # NOT ON GITHUB (must be downloaded before)
├── dataset_clean_validation/        # NOT ON GITHUB (must be downloaded before)
├── 01Figures/                       # plots and figures
├── scripts/                         # Source code for preprocessing and analysis
│   ├── 01_Formatting_Naming.ipynb   # Uniform naming conventions for all machines, measurements and paths
│   ├── 02_Formatting_Columns_5secAlignment.ipynb      # Bring all measurments to uniform 5 second steps. 
│   └── 04_Config_Files.ipynb        # Create 00metadata files (Data availability, gap composition, machine details, measurement details, exogenous data details)
│   └── 05_External_Features.ipynb   # Collect external data (Holidays, electricity prices, electricity mix / emissions, weather data)
│   └── 10_Validate_CheckCleanData.ipynb               # Checks & corrects if files can be opened and are named correctly + creats _missing nd _stats files
│   └── 11_Validate_RenameEmpyFiles.ipynb              # Replace empty files with placeholders _EMPTY
│   └── 12_Validate_Physical_limits.ipynb              # Define physical limits and check for outliers + check if basic formulars holf
│   └── 13_AnalyzeTimeSeries.ipynb  # Delete redundant measurements, check for consistent naming (e.g., S_total_vec vs S_total) + check if basic formulars hold
│   └── 13_Outlier_Detection.ipynb  #  Further outlier detection
│   └── 13_Rescaling.ipynb          # Some measruments have misleading units (e.g., 0.1%) we rescale them.
│   └── 14_Final_Validation.ipynb   # Some final validations
│   └── 15_Visualize_for_paper.ipynb                   # Code to create the plots in the paper
│   └── 15_Visualize.ipynb          # Some dummy code to plot

├── requirements.txt        # Python dependencies
└── README.md               # This file
```

## Installation
1️⃣ Clone the repository
```bash
git clone [https://github.com/username/SPARK.git](https://github.com/JonasSievers/SPARK-High-resolution-energy-data-from-a-Sustainable-Production-Area-in-Karlsruhe.git)
cd SPARK-High-resolution-energy-data-from-a-Sustainable-Production-Area-in-Karlsruhe
```

2️⃣ Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate     # On Linux or macOS
venv\Scripts\activate        # On Windows
```

3️⃣ Install dependencies
```bash
pip install -r requirements.txt
```

4️⃣ Download the dataset
```bash
The dataset will be made publicly available upon publication.
Once released, download it from [link to be added] and extract it into the repository root
```

