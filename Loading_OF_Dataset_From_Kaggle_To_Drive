# Step 1: Install Kaggle API
!pip install kaggle

# Step 2: Upload Kaggle API Key
from google.colab import files
files.upload()  # Manually upload kaggle.json when prompted

# Step 3: Move kaggle.json to the correct directory
!mkdir -p ~/.kaggle
!mv kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json

# Step 4: Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')

# Step 5: Ensure Kaggle_Datasets folder exists in Google Drive
!mkdir -p /content/drive/MyDrive/Kaggle_Datasets

# Step 6: Create a temporary directory for downloading
!mkdir -p /content/temp_sign_language

# Step 7: Download & extract dataset in Colab's temporary storage
!kaggle datasets download -d ahmedkhanak1995/sign-language-gesture-images-dataset -p /content/temp_sign_language --unzip

# Step 8: Move only the extracted files to Google Drive (without the ZIP)
!mv /content/temp_sign_language/* /content/drive/MyDrive/Kaggle_Datasets/

# Step 9: Clean up the temporary folder to save space
!rm -rf /content/temp_sign_language
