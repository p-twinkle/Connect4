# Connect 4 AI: Image Classification and Game Bot

##  Project Overview
This project involves building a **full-stack AI-driven Connect 4 bot** using deep learning and cloud deployment. The goal is to **train a machine learning model** to play Connect 4, dockerize it, host it on AWS, and develop an interactive **web-based interface** using Anvil.

The key components of this project include:
- **Data Generation**: Using **Monte Carlo Tree Search (MCTS)** to generate a dataset of board positions and optimal moves.
- **Neural Network Training**: Implementing both a **Convolutional Neural Network (CNN)** and a **Transformer model** for move prediction.
- **Web Application**: Deploying an interactive Anvil-based UI where users can play against the trained bot.
- **Cloud Hosting**: Deploying the trained model on AWS using **Docker** for backend hosting.

## Features
- Generates a **large dataset** of Connect 4 board positions and corresponding best moves.
- Implements **MCTS-based AI** for self-play and move generation.
- Trains and compares **CNN and Transformer models** for move prediction.
- Provides an **interactive web interface** to play against the AI bot.
- Deploys **model inference on AWS**, making it accessible via Anvil.

##  Installation & Setup

### ** Prerequisites**
Ensure you have the following installed:
- **Python 3.7+**
- **TensorFlow / PyTorch**
- **Docker**
- **AWS account** (for cloud hosting)
- **Anvil account** (for web UI)

### ** Clone the Repository**
```bash
git clone https://github.com/your-username/connect4-ai.git
cd connect4-ai
```

### ** Install Required Dependencies**
```bash
pip install -r requirements.txt
```

### ** Generate Training Data using MCTS**
```bash
python generate_dataset.py --num_games 100000 --output data/connect4_dataset.csv
```

### ** Train the AI Models**
#### Train CNN Model:
```bash
python train_cnn.py --data data/connect4_dataset.csv --epochs 50
```
#### Train Transformer Model:
```bash
python train_transformer.py --data data/connect4_dataset.csv --epochs 50
```

### ** Dockerize the Model for Cloud Deployment**
```bash
docker build -t connect4-bot .
docker run -p 8080:8080 connect4-bot
```

### ** Deploy on AWS**
1. Set up an **AWS EC2 / Lightsail instance**.
2. Transfer model files using **SFTP**.
3. Run the backend server.


## 📂 Project Structure
```
📦 connect4-ai
│── 📂 data                 # Dataset and preprocessing scripts
│── 📂 models               # Trained models and architecture definitions
│── 📂 web                  # Anvil web application
│── generate_dataset.py     # Monte Carlo Tree Search data generation
│── train_cnn.py            # Training script for CNN
│── train_transformer.py    # Training script for Transformer
│── server.py               # Backend server for model inference
│── Dockerfile              # Docker configuration
│── requirements.txt        # Python dependencies
│── README.md               # Project documentation
```


## Web Application
The web application allows users to:
- **Play against AI** (CNN or Transformer)
- **Start a new game**
- **View AI move predictions**

🔗 **Live Demo**: [MSBA25optim2-YourGroup.anvil.app](#)  
🔗 **Clone Anvil App**: [Anvil Project Link](#)

## Model Performance
- The AI models are evaluated based on:
  - **Win rate against MCTS bots**
  - **Move accuracy on validation datasets**
  - **Performance comparison between CNN & Transformer**

## Hosting & Deployment
- **Backend Model Deployment**: AWS EC2 / Lightsail
- **Web UI Deployment**: Anvil
- **Dockerized API Server**: Flask / FastAPI

## Customization & Enhancements
- Improve AI **move prediction accuracy** by refining CNN/Transformer architectures.
- Optimize AWS deployment for **scalability and cost efficiency**.
- Enhance the Anvil UI with **real-time move visualization**.

## Contact & Contributions


---

