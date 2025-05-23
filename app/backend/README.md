# Backend for RAG Chat App

This directory contains the backend code for the RAG (Retrieval Augmented Generation) chat application. The backend is built using [Quart](https://quart.palletsprojects.com/), an asynchronous Python web framework, and integrates with Azure services like Azure OpenAI and Azure Cognitive Search.

## Features

- **Chat and Q&A APIs**: Provides endpoints for chat and question-answering functionality.
- **Authentication**: Supports user authentication and access control.
- **File Upload and Management**: Allows users to upload, list, and delete files.
- **Integration with Azure Services**: Uses Azure OpenAI for GPT models and Azure Cognitive Search for data retrieval.
- **Customizable Approaches**: Supports different RAG approaches for chat and Q&A.

## Directory Structure

- `app.py`: Main entry point for the backend application, defining routes and API endpoints.
- `prepdocs.py`: Handles document preprocessing and setup for ingestion into Azure Cognitive Search.
- `approaches/`: Contains classes implementing different RAG approaches for chat and Q&A.
- `auth/`: Handles authentication and access control logic.
- `utils/`: Utility functions and helpers used across the backend.

## Key Endpoints

- `/ask`: Handles user questions and returns answers using the RAG approach.
- `/chat`: Provides a conversational chat interface.
- `/upload`: Allows users to upload files for processing.
- `/list_uploaded`: Lists files uploaded by the user.
- `/delete_uploaded`: Deletes user-uploaded files.
- `/config`: Returns configuration settings for the frontend.
- `/auth_setup`: Provides MSAL.js settings for authentication.

## Development

### Prerequisites

- Python 3.9, 3.10, or 3.11
- Azure services configured via `azd` (Azure Developer CLI)

### Running Locally

1. Ensure you have deployed the app using `azd up`.
2. Start the backend server:

   ```shell
   python app.py