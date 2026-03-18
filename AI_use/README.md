# How to Use (and Not Use) AI in 2026

**SSBM Geneva — AI Seminar Series**

A 90-minute interactive seminar on using AI intelligently: where it helps, how it actually works under the hood, and where it falls apart.

## View the Slides

**Live:** [https://chrispedder.github.io/SSBM-Lectures/AI_use/slides/](https://chrispedder.github.io/SSBM-Lectures/AI_use/slides/)

**Locally:**
```bash
cd slides
python -m http.server 8000
# Open http://localhost:8000
```

## What the Lecture Covers

### Part A: How to Use AI

- **The AI Landscape in 2026** — current tools, the hype cycle, where we actually are
- **AI as a Career Multiplier** — how AI serves you differently at junior, mid, and senior career stages
- **Personal Branding with AI** — using AI to amplify your thinking, not replace it

### Part B: How Models Work — and Where They Break

- **How Models Learn and Fail** — live MNIST demo showing models that are confident and spectacularly wrong
- **How LLMs Are Built** — training data scale (30% of all text ever written), recency bias, RLHF and the sycophancy problem, the synthetic data ouroboros
- **Where AI Works and Doesn't** — a three-tier honest framework:
  - *Okay:* when you're expert enough to check it, repetitive work, the blank sheet of paper problem
  - *Not okay:* when you're learning, when ambiguity creates unchecked problems, when it creates more work than it saves
  - *Never okay:* frontier knowledge, unwritten assumed expertise, physical/vocational work requiring principles not rules
- **Using AI with Integrity** — transparency, data privacy, cognitive wellbeing
- **Your AI Action Plan** — concrete commitments to take away

## Repository Structure

```
AI_use/
├── README.md                           # This file
├── pyproject.toml                      # Python dependencies (uv)
│
├── slides/
│   ├── index.html                      # Reveal.js presentation
│   ├── part_a.md                       # Part A: How to use AI
│   ├── part_b.md                       # Part B: How models work & where they fail
│   ├── images/                         # Slide images (MNIST outputs, diagrams)
│   └── README.md                       # Slides editing guide
│
└── notebooks/
    ├── mnist_confidence_demo.ipynb      # Live demo: confident wrong predictions
    ├── visualizations.ipynb             # Neural network architecture visualizations
    ├── bayesian_nn_mnist_demo.ipynb     # Bayesian vs Standard DNN comparison
    ├── bacterium_visualization.ipynb    # Free Energy Principle bacterium model
    └── outputs/                         # Generated figures and animations
```

## Running the MNIST Demo

The `mnist_confidence_demo.ipynb` notebook is designed to be run live in front of an audience. It trains a CNN on MNIST in about a minute and then reveals the model's most confident mistakes.

```bash
# Install dependencies
uv venv --python 3.12
source .venv/bin/activate
uv pip install -e .

# Launch the notebook
jupyter notebook notebooks/mnist_confidence_demo.ipynb
```

The demo produces:
- A sample grid of handwritten digits
- The 8 most confident wrong predictions with confidence bar charts
- Confidence distributions comparing right vs wrong predictions
- A noise robustness test showing accuracy collapsing while confidence stays high

## Setup

### Prerequisites

- Python 3.12+
- [uv](https://github.com/astral-sh/uv) package manager (recommended)

### Installation

```bash
git clone https://github.com/ChrisPedder/SSBM-Lectures.git
cd SSBM-Lectures/AI_use
uv venv --python 3.12
source .venv/bin/activate
uv pip install -e .
```

## Contact

- **Chris Pedder** — chrisjbpedder@hey.com
- LinkedIn: [linkedin.com/in/chris-pedder](https://www.linkedin.com/in/chris-pedder/)
- GitHub: [github.com/ChrisPedder/SSBM-Lectures](https://github.com/ChrisPedder/SSBM-Lectures)

## License

Educational material provided for teaching purposes. See LICENSE file for details.
