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


After run this you will seee that....

 You can now view your Streamlit app in your browser.

  Local URL: http://localhost:8501
  Network URL: http://172.28.0.12:8501
  External URL: http://34.139.88.62:8501

Need to install the following packages:
  localtunnel@2.0.2
Ok to proceed? (y)

To proceed typy 'y' and hit enter...You will see this link 
 your url is: https://proud-cameras-love.loca.lt.....
 click that link...Please proceed with caution.

To access the website, please enter the tunnel password below.
Tunnel Password: 34.139.88.62 
*******
From  External URL copy ip address and hit enter again..


Notes:
source activate groqqle: Normally, you'd activate the conda environment, but in Colab, activating a conda environment isn't straightforward. Installing packages directly in the Colab environment should work without needing to activate the environment explicitly.
Localtunnel: Since Streamlit runs on a local server, you'll need to expose it to the web using localtunnel. The URL provided by localtunnel will be accessible to view your Streamlit app.
This setup should allow you to run the Groqqle app in a Colab environment.v
