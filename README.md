# **Next Word Prediction API**

This repository provides an API built with FastAPI to predict the next word in a text sequence, leveraging a pre-trained GPT-2 model.

---

## **Directory Layout**

```
project-root/
├── src/
│   ├── utils.py        # Utility functions for text preprocessing and tokenization
│   ├── model.py        # Loading the GPT-2 model and tokenizer
│   ├── api.py          # FastAPI app and endpoints
│   └── predict.py      # Script for interacting with the API
├── venv/           # Virtual environment for dependencies
├── main.py         # Entry point for starting the API
├── README.md       # Documentation for the project
└── requirements.txt # List of dependencies
```

### **File Descriptions**

- **`src/api.py`:** Sets up the FastAPI application and defines the `/predict` endpoint.
- **`src/model.py`:** Handles loading the GPT-2 model and tokenizer.
- **`src/utils.py`:** Includes functions for text preprocessing, tokenization, and generating predictions.
- **`src/predict.py`:** A demonstration script to test the API.
- **`venv`:** Contains the virtual environment with installed packages.
- **`main.py`:** Starts the FastAPI server using uvicorn.
- **`README.md`:** Provides setup and usage instructions for the project.
- **`requirements.txt`:** Lists all the necessary dependencies.

---

## **Setup Instructions**

### **1. Clone the Repository**
```bash
git clone <repository_url>
```

### **2. Navigate to the Project Directory**
```bash
cd next-word-prediction-api
```

### **3. Create a Virtual Environment**
(Optional but recommended)
```bash
python3 -m venv .venv
source .venv/bin/activate  # For macOS/Linux
.venv\Scripts\activate   # For Windows
```

### **4. Install Dependencies**
```bash
pip install -r requirements.txt
```

---

## **Running the API**

### **1. Start the API Server**
```bash
python main.py
```
The server will start at `http://127.0.0.1:8000`.

### **2. Test the API**
- Use the `src/predict.py` script to send requests.
- Alternatively, send a POST request using cURL or Postman to the `/predict` endpoint with a JSON payload.

#### **Example Request with cURL**
```bash
curl -X POST -H "Content-Type: application/json" -d '{"text": "This is a test"}' http://127.0.0.1:8000/predict
```

---

## **API Details**

### **Endpoint: `/predict` (POST)**

#### **Request Format**
```json
{
  "text": "This is an example"
}
```

#### **Response Format**
```json
{
  "next_word": "sentence"
}
```

---

## **Additional Notes**

- The API leverages a pre-trained GPT-2 model from the Hugging Face Transformers library.
- The `utils.py` module provides basic text preprocessing, with room for further customization.
- The `predict.py` script demonstrates how to send requests using the `requests` library.

This documentation serves as an introduction. Feel free to expand it with details about model performance, use cases, or enhancements for production deployment.

---

