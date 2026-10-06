# CrowdVision AI

**Chess-Inspired AI for Crowd Risk Prediction and Escalation Analysis**

CrowdVision AI is a computer vision and decision-intelligence system designed to analyze crowd scenes, identify anomalous behavior, and estimate potential risk escalation.

Inspired by strategic decision-making in chess engines, the system combines visual feature extraction, crowd representation, probabilistic reasoning, and Monte Carlo Tree Search (MCTS) to explore how observed crowd conditions may evolve.

The final output is translated into a simple three-level risk assessment to support proactive analysis for surveillance and public-safety research.

---

## Overview

Crowd monitoring systems commonly focus on identifying abnormalities in the current scene. CrowdVision AI explores a different approach by combining **computer vision with predictive decision-making** to analyze the current crowd state and estimate potential future risk.

The system follows a multi-stage pipeline:

1. Detect individuals in the crowd
2. Build a structured representation of crowd interactions
3. Extract visual and spatial features
4. Detect anomalous crowd behavior
5. Simulate possible future states
6. Estimate escalation probability
7. Fuse prediction signals
8. Generate a final crowd-risk level

---

## Key Capabilities

- Crowd analysis from a single image
- Person detection using YOLOv11
- Graph-based crowd representation
- Deep visual feature extraction
- Crowd anomaly detection
- Monte Carlo Tree Search for state simulation
- Bayesian reasoning for escalation analysis
- Confidence-based prediction fusion
- Three-level crowd-risk assessment

---

## System Architecture

```text
                         Crowd Image
                              |
                              v
                    Person Detection
                         YOLOv11
                              |
                              v
              Crowd Representation & Graph
                         Modeling
                              |
                              v
                  Visual Feature Extraction
                    ResNet-18 / ViT-MAE
                              |
                              v
                   Crowd Anomaly Detection
                              |
                              v
                Monte Carlo Tree Search
                         (MCTS)
                              |
                              v
                  Bayesian Network
                       Reasoning
                              |
                              v
              Confidence-Based Prediction
                         Fusion
                              |
                              v
                    Crowd Risk Prediction
                              |
                              v
               +--------------+--------------+
               |              |              |
               v              v              v
             GREEN          YELLOW           RED
          Normal State    Increased Risk    High Risk
```

---

## Core Components

### 1. Person Detection

The system uses **YOLOv11** to identify individuals within a crowd image.

The detected individuals form the basis for subsequent crowd representation and spatial analysis.

---

### 2. Crowd Representation

Detected individuals are represented using a structured interaction graph.

Gaussian-weighted relationships are used to model spatial interactions between people and capture characteristics such as:

- Crowd density
- Local neighborhoods
- Spatial relationships
- Interaction patterns

This representation provides a structured view of the crowd beyond individual object detection.

---

### 3. Visual Feature Extraction

Deep learning models are used to extract visual information from crowd scenes.

The project incorporates:

- **ResNet-18**
- **ViT-MAE**

The extracted representations provide visual and contextual information for downstream anomaly and risk analysis.

---

### 4. Crowd Anomaly Detection

The system analyzes visual and spatial characteristics to identify unusual crowd behavior.

Relevant information includes:

- Crowd density
- Spatial irregularity
- Local interaction patterns
- Appearance features
- Anomaly descriptors

---

### 5. Monte Carlo Tree Search

CrowdVision AI uses **Monte Carlo Tree Search (MCTS)** as a chess-inspired planning component.

Rather than analyzing only the observed crowd state, the system explores possible future crowd conditions through simulation.

This provides a decision-making layer for examining potential risk escalation.

---

### 6. Bayesian Risk Reasoning

Bayesian Networks are used to reason about escalation probability based on the available prediction signals.

This probabilistic component complements the visual analysis and simulated future states.

---

### 7. Confidence-Based Prediction Fusion

The system combines prediction signals using confidence information to generate the final crowd-risk assessment.

The output is represented using three alert levels:

| Alert | Interpretation |
|---|---|
| 🟢 Green | Normal crowd conditions |
| 🟡 Yellow | Increased risk; continue monitoring |
| 🔴 Red | High-risk situation requiring immediate attention |

---

## AI Pipeline

CrowdVision AI combines several AI techniques within a single workflow:

```text
Computer Vision
      |
      v
Person Detection
      |
      v
Crowd Representation
      |
      v
Feature Extraction
      |
      v
Anomaly Detection
      |
      v
Decision Intelligence
      |
      +---- MCTS Simulation
      |
      +---- Bayesian Reasoning
      |
      v
Confidence-Based Fusion
      |
      v
Risk Assessment
```

---

## Dataset

The project uses the **ShanghaiTech Crowd Dataset** for crowd-anomaly analysis.

| Attribute | Details |
|---|---|
| Dataset | ShanghaiTech Crowd Dataset |
| Images | 1,198 |
| Scene Types | Dense and Sparse Crowds |
| Purpose | Crowd anomaly detection and risk analysis |

---

## Technology Stack

| Category | Technology |
|---|---|
| Programming Language | Python |
| Deep Learning | PyTorch |
| Object Detection | YOLOv11 |
| Visual Feature Extraction | ResNet-18 |
| Vision Transformer | ViT-MAE |
| Search / Planning | Monte Carlo Tree Search |
| Probabilistic Reasoning | Bayesian Networks |
| Data Storage | HDF5 |
| Development Environment | Jupyter Notebook |

---

## Project Structure

```text
crowdvision-ai/
│
├── crowdvision_ai.ipynb     # Main project notebook
├── project_report.pdf       # Project documentation
├── README.md
├── LICENSE
└── .gitignore
```

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/thrishikav9-del/crowdvision-ai.git
cd crowdvision-ai
```

### 2. Install Dependencies

Install the required Python libraries:

```bash
pip install torch torchvision opencv-python numpy scipy matplotlib networkx
```

### 3. Launch the Notebook

```bash
jupyter notebook crowdvision_ai.ipynb
```

The project can then be explored through the notebook workflow.

---

## Workflow

The complete analysis pipeline follows these steps:

```text
1. Input crowd image
        ↓
2. Detect individuals
        ↓
3. Construct crowd interaction graph
        ↓
4. Extract visual and spatial features
        ↓
5. Detect anomalous crowd behavior
        ↓
6. Simulate possible future states using MCTS
        ↓
7. Estimate escalation probability using Bayesian reasoning
        ↓
8. Fuse prediction signals
        ↓
9. Generate crowd-risk level
```

---

## Applications

CrowdVision AI can support research and experimentation in areas such as:

- Smart surveillance
- Public-event monitoring
- Smart-city safety systems
- Transportation safety
- Stadium security
- Emergency-response analysis
- Disaster-management research

---

## Future Enhancements

Potential extensions include:

- Video-based crowd analysis
- Graph Neural Networks for crowd interaction modeling
- Reinforcement learning for adaptive planning
- Multi-camera crowd monitoring
- Edge AI deployment
- Real-time surveillance dashboards

---

## Research Direction

CrowdVision AI explores the combination of **computer vision, probabilistic reasoning, and search-based decision-making** for proactive crowd-risk analysis.

The chess-inspired MCTS component provides a planning perspective, while Bayesian reasoning and visual models contribute complementary information for risk assessment.

---

## Scope and Disclaimer

This project was developed for academic and research purposes to explore computer vision, probabilistic AI, and intelligent planning techniques for crowd-risk analysis.

The system is intended as a research prototype and should not be treated as a standalone system for real-world security or emergency decisions.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Author

**Vullasa Thrishika**

B.Tech Artificial Intelligence  
Amrita Vishwa Vidyapeetham
