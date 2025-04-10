# Stable Diffusion WebUI Setup with Automatic1111

## Prerequisites
- Python 3.8 or higher
- Git
- Virtual Environment (optional but recommended)

## Step 1: Clone the Repository
```bash
git clone https://github.com/AUTOMATIC1111/stable-diffusion-webui.git
cd stable-diffusion-webui
```

## Step 2: Set Up a Virtual Environment (Optional)
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

## Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

## Step 4: Download Stable Diffusion Model
- Download the model from [Hugging Face](https://huggingface.co/CompVis/stable-diffusion-v-1-4-original)
- Place the model in the `models/Stable-diffusion` directory.

## Step 5: Run the WebUI
```bash
python app.py
```

## Step 6: Access the WebUI
- Open your browser and go to `http://127.0.0.1:5000`

## Explanation
This optimized code provides a streamlined setup process for the Stable Diffusion WebUI using Automatic1111. It includes clear steps for cloning the repository, setting up a virtual environment, installing dependencies, downloading the model, and running the application. Each command is concise and easy to follow, ensuring a smooth installation experience.
