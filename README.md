# CustomizedTextGenerator-GPT2

 Custom GPT-2 Text Generation with Gradio and AWS RDS

This project provides a Gradio interface for generating text using a fine-tuned GPT-2 model. It allows users to input their name, address, and a prompt. The generated text, along with the user details, is stored in an AWS RDS PostgreSQL database.

## Requirements

- Python 3.6+
- Gradio
- Transformers
- safetensors
- torch
- psycopg2
- boto3 (if needed)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-repo/custom-gpt2-text-gen.git
   cd custom-gpt2-text-gen
  Install the required Python packages:

pip install gradio transformers safetensors torch psycopg2
Create a table in your RDS database:

CREATE TABLE user_data (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    address VARCHAR(255),
    prompt TEXT,
    generated_text TEXT,
    timestamp TIMESTAMP
);

# RDS PostgreSQL Configuration
RDS_HOST = 'your_rds_host'
RDS_PORT = 'your_rds_port'
RDS_DB_NAME = 'your_db_name'
RDS_USER = 'your_db_user'
RDS_PASSWORD = 'your_db_password'
Running the Application
python app.py


File Structure
arduino
Copy code
custom-gpt2-text-gen/
├── README.md
├── app.py
├── fine_tuned_model/
│   └── runs/
│       ├── config.json
│       ├── model.safetensor
│       └── vocab.json
└── requirements.txt

app.py: Main application file.
fine_tuned_model/: Directory containing the fine-tuned GPT-2 model files.
README.md: Project documentation file.

### Explanation:

1. **Requirements**: Lists the necessary dependencies.
2. **Installation**: Provides steps to clone the repository and install the required packages.
3. **Configuration**: Instructs the user to set up the RDS PostgreSQL configuration.
4. **Running the Application**: Details how to start the Gradio interface and use the application.
5. **File Structure**: Describes the project's directory structure.
6. **License**: Mentions the project's license.
7. **Acknowledgments**: Credits the tools and libraries used in the project.
