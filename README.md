# In Silico Multi-Epitope Vaccine Design Against *Cryptococcus neoformans*

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS](https://img.shields.io/badge/CSS-3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Bioinformatics](https://img.shields.io/badge/Field-Bioinformatics-brightgreen)](https://en.wikipedia.org/wiki/Bioinformatics)

> A computational immunoinformatics approach to designing a multi-epitope subunit vaccine for the prevention of cryptococcal meningitis

## 📋 Table of Contents
- [Overview](#overview)
- [Background](#background)
- [Methodology](#methodology)
- [Key Findings](#key-findings)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Results Visualization](#results-visualization)
- [Future Directions](#future-directions)
- [Contributing](#contributing)
- [Citation](#citation)
- [License](#license)
- [Contact](#contact)

## 🔬 Overview

This project presents a comprehensive computational approach to designing a multi-epitope vaccine against *Cryptococcus neoformans*, the causative agent of cryptococcal meningitis. Using reverse vaccinology and immunoinformatics tools, we identified and validated immunogenic epitopes from four conserved proteins to construct a novel vaccine candidate.

**Key Features:**
- Multi-epitope vaccine design targeting both cellular and humoral immunity
- Comprehensive immunoinformatics screening for safety and efficacy
- Structural modeling and molecular dynamics validation
- In silico cloning for heterologous expression
- Interactive web visualization of research findings

## 🦠 Background

Cryptococcal meningitis claims over **180,000 lives annually**, predominantly affecting immunocompromised individuals, particularly HIV/AIDS patients. Despite available antifungal treatments, several challenges persist:

- High treatment toxicity
- Drug resistance
- Limited accessibility in resource-limited settings
- Lack of preventive strategies

Currently, **no licensed vaccine exists** for cryptococcal infections, making this a critical area for vaccine development research.

## 🧬 Methodology

### Computational Pipeline

1. **Protein Selection**
   - Mp88 (Mannoprotein 88)
   - Hsp70 (Heat Shock Protein 70)
   - Cda2 (Chitin Deacetylase 2)
   - GPI-anchored cell wall protein

2. **Epitope Prediction & Screening**
   - CTL epitope prediction using NetCTL 1.2
   - HTL epitope prediction using NetMHCIIpan
   - B-cell epitope prediction using ABCpred
   - Allergenicity, toxicity, and antigenicity assessment

3. **Vaccine Construction**
   - Multi-epitope assembly with appropriate linkers
   - β-defensin adjuvant integration
   - PADRE sequence for broad HLA coverage

4. **Structure Prediction & Validation**
   - 3D modeling using I-TASSER
   - Refinement with GalaxyRefine
   - Quality assessment (Ramachandran plot, ERRAT, Verify3D)

5. **Molecular Docking & Dynamics**
   - Docking with TLR2 and TLR4 immune receptors
   - 100 ns molecular dynamics simulation using GROMACS
   - Stability analysis (RMSD, RMSF, Rg, SASA)

6. **Immune Simulation**
   - C-ImmSim server for immune response prediction

7. **Codon Optimization & Cloning**
   - JCat codon optimization for *E. coli* expression
   - In silico cloning into pET-28a(+) vector

## 🎯 Key Findings

### Vaccine Construct Properties
- **Length:** 458 amino acids
- **Molecular Weight:** 49.6 kDa
- **Theoretical pI:** 9.67
- **Instability Index:** 38.96 (stable)
- **Aliphatic Index:** 74.87 (thermostable)
- **Grand Average Hydropathicity:** -0.274 (hydrophilic)
- **Antigenicity Score:** 0.78 (highly antigenic)

### Validation Results
- ✅ Non-allergenic
- ✅ Non-toxic
- ✅ Soluble upon overexpression
- ✅ Stable binding with TLR2 and TLR4
- ✅ Structurally stable in MD simulation
- ✅ Elicits robust immune response (cellular & humoral)

### Structural Quality
- **Ramachandran Plot:** 92.8% in favored regions
- **ERRAT Score:** 87.43%
- **Verify3D:** 81.25% residues with ≥0.2 3D-1D score

## 📁 Project Structure

```
cryptococcus-vaccine-design/
│
├── index.html                    # Main project webpage
├── README.md                     # Project documentation (this file)
├── LICENSE                       # MIT License
├── CITATION.cff                  # Citation metadata
├── .gitignore                    # Git ignore rules
│
├── docs/
│   ├── Vaccine-Minor-Report.docx # Complete research report
│   └── methodology.md            # Detailed methodology
│
├── data/
│   ├── protein_sequences/        # Input protein FASTA sequences
│   ├── epitopes/                 # Predicted epitope data
│   └── structures/               # PDB files and models
│
├── results/
│   ├── docking/                  # Molecular docking results
│   ├── md_simulation/            # MD trajectory data
│   ├── immune_simulation/        # C-ImmSim outputs
│   └── figures/                  # Publication-quality figures
│
├── scripts/
│   ├── epitope_prediction.py    # Epitope screening scripts
│   ├── structure_validation.py  # Structure quality checks
│   └── analysis.py               # Results analysis
│
└── assets/
    ├── css/                      # Stylesheets
    ├── js/                       # JavaScript files
    └── images/                   # Project images
```

## 🚀 Installation

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Git (for cloning the repository)

### Clone Repository

```bash
git clone https://github.com/yourusername/cryptococcus-vaccine-design.git
cd cryptococcus-vaccine-design
```

### Local Deployment

Simply open `index.html` in your web browser:

```bash
# On macOS
open index.html

# On Linux
xdg-open index.html

# On Windows
start index.html
```

Or use a local server:

```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000

# Node.js
npx http-server
```

Then navigate to `http://localhost:8000` in your browser.

## 💻 Usage

### Web Interface

The interactive HTML page provides:
- Comprehensive research overview
- Methodology details
- Visual results and figures
- Interactive navigation
- Responsive mobile design

### Accessing Data

All raw data, sequences, and analysis scripts are available in the respective directories. See `data/README.md` for data format specifications.

## 🛠️ Technologies Used

### Bioinformatics Tools
- **NetCTL 1.2** - CTL epitope prediction
- **NetMHCIIpan** - HTL epitope prediction
- **ABCpred** - B-cell epitope prediction
- **VaxiJen** - Antigenicity prediction
- **AllerTop** - Allergenicity assessment
- **ToxinPred** - Toxicity prediction
- **I-TASSER** - Protein structure prediction
- **GalaxyRefine** - Structure refinement
- **HADDOCK** - Molecular docking
- **GROMACS** - Molecular dynamics simulation
- **C-ImmSim** - Immune response simulation
- **JCat** - Codon optimization

### Web Technologies
- **HTML5** - Structure and content
- **CSS3** - Styling and layout
- **JavaScript (ES6+)** - Interactivity and animations
- **Responsive Design** - Mobile-friendly interface

## 📊 Results Visualization

The project includes interactive visualizations for:
- Vaccine construct schematic
- 3D structural models
- Molecular docking complexes
- MD simulation trajectories
- Immune response profiles
- Ramachandran plots

Access these through the web interface or in the `results/figures/` directory.

## 🔮 Future Directions

1. **Experimental Validation**
   - Expression and purification in *E. coli*
   - In vitro immunogenicity testing
   - Animal model studies

2. **Optimization**
   - Alternative adjuvant testing
   - Epitope variant analysis
   - Delivery system optimization

3. **Clinical Translation**
   - Toxicity studies
   - Efficacy trials
   - Regulatory pathway assessment

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and development process.

## 📝 Citation

If you use this work in your research, please cite:

```bibtex
@mastersthesis{kaverappa2025vaccine,
  author       = {Kaverappa M, Inchal},
  title        = {In Silico Multi-Epitope Vaccine Design Targeting Key Immunogenic Properties of Cryptococcus neoformans for the Prevention of Cryptococcal Meningitis},
  school       = {Garden City University},
  year         = {2025},
  address      = {Bengaluru, India},
  type         = {MSc Bioinformatics Minor Project},
  supervisor   = {Dr. Chemmugil}
}
```

Or in text format:
> Kaverappa M, I. (2025). In Silico Multi-Epitope Vaccine Design Targeting Key Immunogenic Properties of *Cryptococcus neoformans* for the Prevention of Cryptococcal Meningitis. MSc Bioinformatics Minor Project, Garden City University, Bengaluru.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📧 Contact

**Inchal Kaverappa M**  
MSc Bioinformatics  
Garden City University, Bengaluru

**Supervisor:** Dr. Chemmugil  
Department of Life Sciences

---

## 🙏 Acknowledgments

- Garden City University for providing research facilities
- Dr. Chemmugil for guidance and supervision
- Open-source bioinformatics tool developers
- The computational biology community

---

<div align="center">

**⭐ Star this repository if you found it helpful!**

Made with 💙 for advancing vaccine research against *Cryptococcus neoformans*

</div>