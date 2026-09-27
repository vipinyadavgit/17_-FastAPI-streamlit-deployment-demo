# 17_-FastAPI-streamlit-deployment-demo
# Build a Simple Full-Stack Python Application



Build a simple full-stack Python application using **Streamlit** for the frontend and **FastAPI** for the backend.

========================================
## RUN command 
Backend:- uv run uvicorn 17_fastapi_streamlit_deployment_demo.backend.main:app --reload --port 8000

Frontend:- uv run streamlit run src/17_fastapi_streamlit_deployment_demo/frontend/app.py


## Architecture

```text
                 USER
                   |
                   v
            Streamlit UI
                   |
             HTTP Request
                   |
                   v
            FastAPI Backend
                   |
             Business Logic
                   |
             JSON Response
                   |
                   v
            Streamlit UI
                   |
                   v
                 USER
```

## Objective

The purpose of this exercise is to demonstrate how a **frontend and backend communicate with each other** in a full-stack Python application.

The application should have two separate components:

### 1. Frontend — Streamlit

* Build a simple user interface using Streamlit.
* Accept user input.
* Send an HTTP request to the FastAPI backend.
* Receive the JSON response.
* Display the response to the user.

### 2. Backend — FastAPI

* Create REST API endpoints using FastAPI.
* Accept requests from the Streamlit frontend.
* Implement the required business logic.
* Return the result as a JSON response.

## Expected Flow

```text
User Input
    ↓
Streamlit UI
    ↓
HTTP Request
    ↓
FastAPI API
    ↓
Business Logic
    ↓
JSON Response
    ↓
Streamlit UI
    ↓
Display Result
```

## Requirements

The implementation should demonstrate:

* A **separate frontend and backend**
* Communication between frontend and backend using **HTTP**
* REST API development using **FastAPI**
* UI development using **Streamlit**
* JSON request/response handling
* Basic separation of business logic from the UI

## Demo Requirement

The application should be designed so that the **frontend and backend can be demonstrated and tested separately**.

For example:

* The FastAPI backend should be runnable independently and testable through its API documentation or an API client.
* The Streamlit frontend should be runnable independently and configured to communicate with the FastAPI backend through HTTP.

## Run the backend

From the project root, run:

```powershell
uv run uvicorn 17_fastapi_streamlit_deployment_demo.backend.main:app --reload --port 8000
```

Open `http://127.0.0.1:8000/docs` to test the API.

## Suggested Project Structure

```text
project/
│
├── backend/
│   ├── main.py
│   └── ...
│
├── frontend/
│   ├── app.py
│   └── ...
│
├── requirements.txt
└── README.md
```