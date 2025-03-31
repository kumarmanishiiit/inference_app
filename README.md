# FastAPI Inference App

This repository contains a FastAPI-based inference application for serving machine learning models via REST API endpoints. The app can accept input data, perform model inference, and return the results in a structured format.

## Features
- Lightweight and fast API using FastAPI
- Easy model deployment
- Scalable and customizable
- Supports various input and output formats

## Prerequisites
Ensure you have the following installed on your machine:

- Python 3.8+
- pip (Python package manager)
- Git

## Installation

1. **Clone the Repository:**
```bash
git clone https://github.com/your-username/fastapi-inference-app.git
cd fastapi-inference-app
```

2. **Create a Virtual Environment (Optional but Recommended)**
```bash
python3 -m venv venv
source venv/bin/activate # For Linux/macOS
# On Windows: venv\Scripts\activate
```

3. **Install Dependencies**
```bash
pip install -r requirements.txt
```

## Configuration

- Place your model file in the `models/` directory.
- Update the model loading logic in `app/main.py` if necessary.
- Configure environment variables using a `.env` file (optional).

## Usage

1. **Run the FastAPI App**
```bash
uvicorn app.main:app --host 0.0.0.0 --port 8000
```

2. **Access the API Documentation**
- Swagger UI: [http://localhost:8000/docs](http://localhost:8000/docs)
- ReDoc: [http://localhost:8000/redoc](http://localhost:8000/redoc)

## Example Request
You can use `curl` or any HTTP client to send requests:
```bash
curl -X POST http://localhost:8000/predict \
  -H "Content-Type: application/json" \
  -d '{"input_data": [1.0, 2.0, 3.0, 4.0]}'
```

## Deployment
You can deploy the app using Docker.

1. **Build the Docker Image:**
```bash
docker build -t fastapi-inference-app .
```

2. **Run the Docker Container:**
```bash
docker run -p 8000:8000 fastapi-inference-app
```

## Contributing
Contributions are welcome! Please submit a pull request or open an issue for suggestions and improvements.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.