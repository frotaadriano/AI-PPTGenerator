
 # AIPPTGenerator

## Description (English)

A FastAPI application that transforms text files into PowerPoint presentations (.pptx) using Azure OpenAI for text summarization and image generation.

### Features

- Upload .txt files
- Text summarization using Azure OpenAI
- Image generation using Azure OpenAI
- PowerPoint creation with summarized text and images

### Technologies Used

- Python
- FastAPI
- Azure OpenAI - (openailib version 1.35.3) 
- python-pptx
- Requests

### Prerequisites

- Python 3.8+
- Azure account with access to Azure OpenAI
- Install dependencies listed in `requirements.txt`
- Migrate to the newest OpenAI API version: [OpenAI Python Migration Guide](https://github.com/openai/openai-python/discussions/742)

### Easy way to install openai version 1x
- If neeed help with openai lib: https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/migration?tabs=python-new%2Cdalle-fix 


### WSL Setup (Optional for Linux Environment on Windows)

1. Install WSL:
    ```bash
    wsl --install -d Ubuntu
    ```

2. Update packages and install dependencies:
    ```bash
    sudo apt-get update
    sudo apt-get install curl
    sudo apt-get install bash
    ```

3. Navigate to your project folder and install Grit:
    ```bash
    cd /mnt/.../AI-PPTGenerator
    curl -fsSL https://docs.grit.io/install | bash
    grit install
    grit apply openai
    ```

4. For help with OpenAI lib: [OpenAI Migration Guide](https://learn.microsoft.com/en-us/azure/ai-services/openai/how-to/migration?tabs=python-new%2Cdalle-fix)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/AIPPTGenerator.git
    cd AIPPTGenerator
    ```

2. Create and activate a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # Linux/Mac
    venv\Scripts\activate  # Windows
    ```

3. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Configure your Azure OpenAI credentials in the `.env` file:
    ```
    AZURE_OPENAI_API_KEY=your-openai-api-key
    ```

### Usage

1. Start the FastAPI server:
    ```bash
    uvicorn app:app --reload
    ```

2. Access the API documentation at [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs) to test the upload endpoint.

3. Use the `/generate-ppt` endpoint to upload a .txt file and get the generated PPT.

### Project Structure

```plaintext
AIPPTGenerator/
├── app.py               # Main FastAPI application file
├── requirements.txt     # Project dependencies
├── README.md            # Project documentation
└── .env                 # Environment configurations (not included in the repository)
```

### Example Usage
Upload a .txt file to the /generate-ppt endpoint.
The API will return a generated .pptx file with summarized content and relevant images.

### Contribution

Fork the project.
Create a feature branch (git checkout -b feature/new-feature).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature/new-feature).
Create a new Pull Request.

### License
This project is licensed under the MIT License - see the LICENSE file for details.



