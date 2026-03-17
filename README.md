# Modeling and Optimization of Epidemiological Control Policies through Reinforcement Learning

**Author:** Ishir Rao 
**Publication:** *Journal of Emerging Investigators* **Full Paper:** [Read the full article here](https://emerginginvestigators.org/articles/22-157)

---

## 📄 Abstract
Pandemics involve high transmission of a disease that impact global and local health and economical patterns. The impact of a pandemic can be minimized by enforcing certain restrictions on a community. However, these restrictions, while minimizing infection and death rates, can also lead to economic crisis. Epidemiological models help to propose pandemic control strategies based on non-pharmaceutical interventions such as social distancing, curfews, and lockdowns which reduce the economic impact of these restrictions.

In this research, we utilize an epidemiological **SEIRD (Susceptible, Exposed, Infected, Recovered, Deceased)** model—a compartmental model for virtually simulating a pandemic day-by-day. This is combined with a **Deep Double Recurrent Q-Network (DDRQN)** to train an agent to enforce the optimal restriction on the SEIRD simulation based on a reward function. We tested two agents with unique reward functions and pandemic goals to obtain two strategies. 

* **Agent 1:** Implemented long lockdowns to reduce the initial spread, followed by cyclical and shorter lockdowns to mitigate resurgence.
* **Agent 2:** Provided similar infection rates but an improved economy by implementing a 10-day lockdown and 20-day no-restriction cycle.

By implementing these automated strategies, humanity can efficiently develop novel pandemic control policies that minimize disease spread and the economic impacts of pandemics.

---

## 🛠️ Project Structure
To keep the implementation accessible and reproducible, the entire simulation and model architecture are contained within a single file.

* `project_code.py`: Contains the SEIRD environment class, the DDRQN neural network architecture, and the training/evaluation logic.

---

## 🔬 Methodology

### The SEIRD Model
The simulation tracks the population through five distinct states:
1.  **Susceptible (S):** Healthy individuals at risk.
2.  **Exposed (E):** Individuals who have contracted the virus but are not yet infectious.
3.  **Infected (I):** Individuals capable of spreading the virus.
4.  **Recovered (R):** Individuals who have survived and gained immunity.
5.  **Deceased (D):** Individuals who have succumbed to the disease.

### Reinforcement Learning (MORL)
We utilized Multi-Objective Reinforcement Learning to navigate the trade-off between public health safety and economic stability. The agent learns through a reward function that penalizes both high infection rates and the economic cost of strict lockdowns.

---

## 🚀 Getting Started

### Prerequisites
Ensure you have Python installed along with the following dependencies:
* `numpy`
* `torch` (PyTorch)
* `matplotlib`
* `pandas`

### Installation & Execution

1. Clone the Repository
2. Run the simulation: python project_code.py
3. Adjust the simulation parameters and reward function!

### Citation
If you use this research or code in your work, please cite the original article:

Rao et al. (2023). Modeling and Optimization of Epidemiological Control Policies through Reinforcement Learning. Journal of Emerging Investigators.
