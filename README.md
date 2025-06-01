# Robot-Locomotion-Using-Reinforcement-Learning-SAC-TD3-A2C-
This project explores the application of reinforcement learning (RL) algorithms to train a robotic agent to perform locomotion tasks using continuous control. The implementation is based on the Gymnasium environment suite and Stable-Baselines3 library.


https://github.com/user-attachments/assets/15ed3729-2d21-456d-b8c2-260319346d03


🎯 OBJECTIVE

The goal of the project is to train a humanoid robot to walk effectively by interacting with a simulated environment and improving its performance through trial and error. Three different reinforcement learning algorithms—Soft Actor-Critic (SAC), Twin Delayed Deep Deterministic Policy Gradient (TD3), and Advantage Actor-Critic (A2C)—are used and compared in terms of learning efficiency, stability, and control quality.

🧪 APPROACH

The training and evaluation process is implemented in Python using Stable-Baselines3.

The agent is trained in Gymnasium’s Humanoid-v4 environment.

All three algorithms (SAC, TD3, and A2C) were tested.

SAC was selected as the final algorithm due to its superior performance in terms of training stability and sample efficiency in continuous action environments.

The codebase allows modular switching between algorithms and supports both training and testing modes.

🛠️ TECHNOLOGIES USED

Python

Stable-Baselines3

Gymnasium

PyTorch (via Stable-Baselines3)

TensorBoard (for visualization of training progress)

argparse (for command-line interface)

🚀 FEATURES

Training and testing support for:

SAC (Soft Actor-Critic)

TD3 (Twin Delayed DDPG)

A2C (Advantage Actor-Critic)

Automatic model saving at regular intervals

Real-time environment rendering during test mode

TensorBoard logging for training visualization

Flexible CLI interface for choosing environment and algorithm

📁 PROJECT STRUCTURE

bash
Copy
Edit
.
├── models/            # Saved model checkpoints
├── logs/              # TensorBoard logs
├── main.py            # Main script for training and testing

💻 USAGE

1. Install Dependencies

bash
Copy
Edit
pip install stable-baselines3[extra] gymnasium[all]

2. Train an Agent
bash
Copy
Edit
python main.py Humanoid-v4 SAC --train

3. Test a Trained Agent
bash
Copy
Edit
python main.py Humanoid-v4 SAC --test models/SAC_25000.zip

📌 RESULTS
Using SAC, the robot learned to perform stable and effective locomotion in the Humanoid-v4 environment. Compared to TD3 and A2C, SAC provided faster convergence and more consistent performance during evaluation.
