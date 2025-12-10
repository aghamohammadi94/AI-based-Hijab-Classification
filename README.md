
# Hijab Detection model

This is a hijab Detection project

---

## 🛠️ Technologies Used

- Python  
- TensorFlow / Keras  
- VGG16 (pretrained on ImageNet)  
- NumPy 
- Matplotlib  
- Pillow
- OpenCV
- Mediapipe

---

## Main 8 steps of this project :

1. Collecting datasets from Google (Data Crawling).
2. Using mediapipe and opencv, images downloaded from Google were worked on and images containing faces were identified and cropped and saved in a new folder to be given to the model.
3. Using the VGG16 pre-trained network, feature extraction was performed on the images.
4. Making a simple model and combining it with the VGG16 model.
5. Since the number of images to train the model is small, data augmentation was used to augment the training data.
6. The model was trained using the dataset obtained from the faces and the model was saved.
7. The accuracy and loss diagram of the model was saved.
8. The trained and stored model was tested on new images and on the webcam.

---

## Steps to run this on your system

**Step 1**. To use the VGG16 pre-trained model, you need to download the vgg16_weights_tf_dim_ordering_tf_kernels_notop.h5 file.
If you don't have this file or you encounter an error while downloading, this file is located in the vgg16_notop folder.

**Step 2**. To test the model:
You can use the testing-the-model-with-webcam.py file to test the model on your webcam or the testing-the-model-with-new-images.ipynb file to test the model on new images.

---

## Model Architecture
Combined Architecture

Image → conv_base(VGG16 pre-trained model) → Flatten → Dense(256) → Sigmoid

Tip: conv_base contains the VGG16 model, but with the new input size and the output with one class.

---

## ⚙️ Installation

```bash
# Clone repository
git clone https://github.com/aghamohammadi94/Hijab-Detection-assignment.git

# Enter the project folder
cd Hijab-Detection-assignment


# Step 1 — Make sure Chocolatey is installed
## In PowerShell (with Run as Administrator) enter this command:
choco --version
## If it shows version → it is installed
## If it gives error → it needs to be installed


# Step 2 — Installing Chocolatey (if not installed)
## Open PowerShell as Administrator and run this command:
Set-ExecutionPolicy Bypass -Scope Process -Force; `
[System.Net.ServicePointManager]::SecurityProtocol = `
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; `
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

## Once done, close and reopen the terminal and test the following command:
## To enable new paths (PATH)
choco


# Step 3 — Install Python with Chocolatey
choco install python -y
## It is better to install a specific version, for example 3.10.7, in this project
## Installing the required version of Python with Chocolatey
choco install python --version=3.10.7 -y
## To install Unlisted versions with Chocolatey:
choco install python --version=3.10.7 -y --force
## Or if you already have a newer version and want to install the old version:
choco install python --version=3.10.7 --allow-downgrade -y
## Tips:
## ✔ If you have multiple versions, Chocolatey will install them side by side.
## ✔ If Chocolatey doesn't find the version, in rare cases Chocolatey will delete the version and it will no longer exist, but Python itself will keep the versions.
## ✔ In this case: Go to the Python downloads site and download and install the Installer version 3.10.7.
## ✔ Installing Python with Chocolatey includes pip. So there is no need to install pip after installation.


# Step 4 — Verify Python is installed
python --version
## On some systems you should use this
py --version
## View installed Python versions
## This command will list all installed versions
py -0


# Step 5 — Create a virtual environment with a custom name

## Windows:
python -m venv new-venv
# or
## If you have multiple versions of Python installed, you can specify which version to use when building venv
## This venv uses exactly version 3.10
## It is very important that you use python 3.10
py -3.10 -m venv new-venv

## macOS / Linux:
python3 -m venv new-venv
# or
python3.10 -m venv new-venv


# Step 6 — Activate the virtual environment

## Windows:
new-venv\Scripts\activate

## macOS / Linux:
source new-venv/bin/activate


# Step 7 — Update the main package management tools in Python
python -m pip install --upgrade pip setuptools wheel


# Step 8 — Install required libraries
pip install -r requirements.txt


# Step 9 — Quick test:
python 05_testing-the-model-with-webcam.py
```


```
project/
├─ data-crawling
├─ datasets/
|  ├─ train/
|  |  ├─ hijab
|  |  └─ without_hijab
|  └─ validation/
|     ├─ hijab
|     └─ without_hijab
├─ downloads
├─ images/
|  ├─ hijab
|  └─ without_hijab
├─ new-test-images
├─ test-images
├─ vgg16_notop
├─ Hijab_Detection.h5
└─ README.md
```

---

## URL ---> The addresses of the images downloaded and used in this project in order of folder name inside Google Drive

To access the ".env" so you can use Project Paths and Training Hyperparameters, simply download the ".env" file from this address.

Tip: There was no need to put the ".env" file inside the project.

.env : https://drive.google.com/file/d/1za4TwNo9A3Gg9Vh-M-8fgwsWrup02eUp/view?usp=sharing

datasets : https://drive.google.com/drive/folders/1vsRnE8Ute0bUUOYMmjGLW7EnSaqnqqC5?usp=sharing

downloads : https://drive.google.com/drive/folders/1fdsutBQASgw8wYjIgMUdq5gwilgh5It3?usp=sharing

images : https://drive.google.com/drive/folders/1-5N8KiY_PSa7Ivxr-vhfWHHVuxQ80xO2?usp=sharing

test-images : https://drive.google.com/drive/folders/1AVCfaKNStqOznGI9uVNoXCx3vjUKej8s?usp=sharing

new-test-images : https://drive.google.com/drive/folders/1DYPsWVTR76R60au1Ku9kGclG5WvLWwgH?usp=sharing

---

<div align="center">
  <table>
    <tr>
      <td align="center">
        <img src="Training and validation accuracy.png" width="400"><br>
        <strong>Training and validation accuracy</strong>
      </td>
      <td align="center">
        <img src="Training and validation loss.png" width="400"><br>
        <strong>Training and validation loss</strong>
      </td>
    </tr>
  </table>
</div>



