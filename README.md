# Reinforcement Learning Agent Snake Game
### Universidade Nova de Lisboa - Deep Learning Course (2024-2025)

This project explores the implementation and optimization of a **Deep Q-Network (DQN)** agent to master the classic Snake Game. We systematically investigate the impact of fundamental DQN components—such as **Experience Replay** and **Target Networks**—and compare different **exploration strategies** to achieve an optimal autonomous agent.

## 1. Overview

The goal of this project was to train an intelligent agent to play the Snake Game using Reinforcement Learning.

* **Model:** A **Deep Q-Network (DQN)** model was implemented, utilizing a **Convolutional Neural Network (CNN)** architecture (3 convolutional layers, 2 fully-connected layers) to process the game's visual frames.
* **Methodology:** The project followed a staged approach:
    1. **Task 1 (Basic DQN):** Implementation of a basic DQN **without Experience Replay and Target Network**, including a **Heuristic Policy** for comparison.
    2. **Task 2 (Enhanced DQN):** Integration and analysis of **Experience Replay** and **Target Networks** to improve learning stability.
    3. **Task 3 (Exploration):** Comparison of **Epsilon-Greedy** and **Boltzmann** exploration strategies.
* **Key Finding:** Although **Experience Replay** significantly improved stability (especially with a large buffer, e.g., 10,000), the **Target Network** actually reduced performance stability in our specific setup, leading us to conclude that a DQN with **Replay Buffer but without a Target Network** was the most effective configuration.


## 2. Installation and Setup

This project requires Python and common scientific libraries, primarily PyTorch for the DQN implementation.

1.  **Clone the repository:**
    ```bash
    git clone [URL_TO_YOUR_REPO]
    cd reinforcement_learning_agent_snake_game
    ```

2.  **Create and activate a virtual environment (Recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Linux/macOS
    # .\venv\Scripts\activate  # On Windows
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install torch torchvision torchaudio numpy matplotlib jupyter
    # Note: PyTorch is used for device selection (CPU/CUDA/MPS)
    ```

## 3. How to Run the Code

The core experiments can be reproduced using the provided Jupyter Notebook.

1.  **Start Jupyter:**
    ```bash
    jupyter notebook
    ```
2.  **Open the selected notebook**.
3.  **Run the cells:** The notebook is structured to walk through Task 1, Task 2, and Task 3, allowing you to run the training loops and visualize the learning curves for:
    * Basic DQN vs. Heuristic Policy
    * Impact of Replay Buffer Size (e.g., 10 vs. 10,000)
    * Hard vs. Soft Target Network update strategies
    * Epsilon-Greedy vs. Boltzmann exploration strategies


## 4. Authors

This project was completed by **Team LLMH** for the Nova FCT - 2024-2025 assignment.

* GALLO Lorenzo
* LEKBOURI Lina
* LICHTNER Marc
* WERCK Hugo