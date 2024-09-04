# Groqqle-Collab Steps :-

# Step 1: Clone the repository
!git clone https://github.com/jgravelle/Groqqle.git
%cd Groqqle

# Step 2: Install mamba (a faster Conda alternative) in Colab
!pip install -q condacolab
import condacolab
condacolab.install()

# Step 3: Create and activate the environment (optional if specific packages are required)
!mamba create --name groqqle python=3.11 -y
!source activate groqqle

# Step 4: Install the required packages
!pip install -r requirements.txt

# Step 5: Set the API key and run the Streamlit app
import os
os.environ["GROQ_API_KEY"] = "your_api_key_here"  # Replace with your actual API key

# Streamlit requires special handling in Colab, so we'll use the following command:
!streamlit run Groqqle.py & npx localtunnel --port 8501



Notes:
source activate groqqle: Normally, you'd activate the conda environment, but in Colab, activating a conda environment isn't straightforward. Installing packages directly in the Colab environment should work without needing to activate the environment explicitly.
Localtunnel: Since Streamlit runs on a local server, you'll need to expose it to the web using localtunnel. The URL provided by localtunnel will be accessible to view your Streamlit app.
This setup should allow you to run the Groqqle app in a Colab environment.v
