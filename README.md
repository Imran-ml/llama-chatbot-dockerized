<p align="left">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker"/>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/>
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript"/>
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx"/>
  <img src="https://img.shields.io/badge/Ollama-grey?style=for-the-badge" alt="Ollama"/>
  <img src="https://img.shields.io/badge/Llama%203-blueviolet?style=for-the-badge" alt="Llama 3"/>
</p> 


# Llama 3 Chatbot with Docker

Run LLM model Locally using Docker right inside your codebase. In this project, I did not used the suporting GUI like Open WebUI or LM Studio or any other, so the purpose to use stand alone LLM models with ollama to give you the idea that how you can use it in your project/code instead of running through third party. Everything is containerized with Docker, so setup is clean and repeatable. Its just a fun side project so my connections can learn more about running models locally in their own projects. 

## Features

* **Simple Chat Interface:** Easy-to-use web interface for interacting with the chatbot.
* **Llama 3 Powered:** Utilizes the **Llama 3** model for generating responses.
* **Dockerized:** The entire application (backend, Ollama, and frontend) is containerized for easy setup and deployment using Docker Compose.
* **FastAPI Backend:** A Python backend built with FastAPI serves the chat functionality.
* **Ollama Integration:** Uses Ollama to serve the Llama 3 model locally.

## Technical Details & Versions

* **Language Model:** **Llama 3**
* **Python Version:** The Python version 3.11-slim. 
* **Backend Framework:** FastAPI 
* **ASGI Server:** Uvicorn 
* **HTTP Client (Python):** HTTPX 
* **LLM Serving:** `ollama/ollama` Docker image
* **Frontend Web Server:** `nginx:alpine` Docker image
* **Containerization:** Docker & Docker Compose

## Directory Structure

llama-chatbot-dockerized/

├── backend/

│   ├── main.py   

│   └── requirements.txt 

├── frontend/

│   └── index.html   

├── docker-compose.yml  

└── Dockerfile         

## Prerequisites

* **Docker:** Ensure Docker is installed and running. Download from [https://www.docker.com/get-started](https://www.docker.com/get-started).
* **Docker Compose:** This is usually included with Docker Desktop. If not, follow the installation guide for your OS.

## How to Run with Docker

1.  **Clone the repository**
    ```bash
    git clone https://github.com/Imran-ml/llama-chatbot-dockerized
    cd llama-chatbot-dockerized
    ```

2.  **Navigate to the project directory:**
    Make sure you are in the `llama-chatbot-dockerized`.

3.  **Build and run the application using Docker Compose:**
    * Build the backend Docker image based on `Dockerfile`.
    * Pull the `ollama/ollama` image and the `nginx:alpine` image.
    * Start all defined services (Ollama, backend, frontend).
    * The `ollama` service is configured to automatically pull the **Llama 3** model upon starting. This might take some time during the first run as the model is downloaded.

    ```bash
    docker-compose up --build
    ```

    You will see logs from all the containers in your terminal.

4.  **Access the Chatbot:**
    Once the services are up and running:
    * Open your web browser and go to: `http://localhost:8080` to interact with the chatbot.
    * The backend API is accessible at `http://localhost:8000`.
    * The Ollama API is at `http://localhost:11434`.

## Usage

1.  Open `http://localhost:8080` in your browser.
2.  The chat interface should load.
3.  Type your message in the input field and press Enter or click the send button to chat with the **Llama 3** model.

## About Author
  **Name**: Muhammad Imran Zaman

  **Company**: [DOCUFY GmbH](https://docufy.de/en/home/)

  **Role**: Lead Machine Learning Engineer

  **Professional Links**:
    - HuggingFace: [Profile](https://huggingface.co/ImranzamanML)
    - Kaggle: [Profile](https://www.kaggle.com/muhammadimran112233)
    - LinkedIn: [Profile](linkedin.com/in/muhammad-imran-zaman)
    - Google Scholar: [Profile](https://scholar.google.com/citations?user=ulVFpy8AAAAJ&hl=en)
    - Medium: [Profile](https://medium.com/@imranzaman-5202)
    
- **Project Repository**: [GitHub Repo](https://github.com/Imran-ml/llama-chatbot-dockerized)
