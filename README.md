# SPARK: High-resolution energy data from a Sustainable Production Area in Karlsruhe

## Abstract: 
Understanding and optimizing industrial energy systems requires datasets that capture detailed electrical behavior at high temporal resolution over long time periods. Such data are essential for analyzing power quality, identifying operational patterns, and developing data-driven models for forecasting, control, and predictive maintenance.
Yet, most existing open datasets lack the temporal granularity, measurement diversity, and machine-level detail needed to reflect the complexity of industrial environments.
To address this gap, we present a large-scale, high-resolution dataset of industrial electricity measurements comprising more than 74 billion data points collected at 5-second resolution over up to seven years. The dataset includes 22 industrial machines and one photovoltaic system, with up to 190 measured quantities per device, including three-phase voltages and currents, active, reactive, and apparent power, harmonic spectra, total harmonic distortion, and fundamental waveform characteristics.
This unique combination of long-term coverage, high sampling rate, and rich feature space enables unprecedented insight into industrial energy dynamics and provides a robust foundation for advancing machine learning, digital twins, and intelligent energy management in industrial environments.

## Repository Structure
```text
├── dataset/                       # Optionally unprocessed data
├── dataset_clean/                 # Local data directory (kept outside Git LFS or ignored if large)
├── dataset_clean_validation/      # Local data directory with validation _stats.csv and _missing.scv files (kept outside Git LFS or ignored if large)
├── 01Figures/                     # plots and figures
├── scripts/                       # Source code for preprocessing and analysis
│   ├── preprocess_data.py
│   ├── plot_thd_radars.py
│   └── utils/
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
The dataset will be made publicly available upon publication.
Once released, download it from [link to be added] and extract it into the repository root, so that the folder structure appears as follows:
