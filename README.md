OR_OWRD_OSU_training
=========================

This repository contains two [Jupyter Notebooks](https://jupyter.org/), which facilitate access and aggregation of the field-level ET and consumptive use data from the OWRD-DRI historical water use geodatabase (1985-2024). The first notebook ([et_cu_data_retrieval_gee.ipynb](https://github.com/ba-minor/OR_OWRD_OSU_training/blob/main/notebooks/et_cu_data_retrieval_gee.ipynb)) is intended to be run in Google Colab within a web browser (e.g., Google Chrome) and it leverages Earth Engine & Python to process the geodatabase. The second notebook ([et_cu_data_retrieval_python.ipynb](https://github.com/ba-minor/OR_OWRD_OSU_training/blob/main/notebooks/et_cu_data_retrieval_python.ipynb)) is intended to be run in a local Python environment and it only uses Python to process the geodatabase. 

<span style="color:red">Requirements</span>:
> The first notebook requires the user to have Google Workspace, access to Earth Engine, and to have a registered Google Cloud project, but it does not require you to set up a Python environment or have the database downloaded locally.<br><br>
> The second notebook requires the user to set up a Python environment and download the entire geodatabase, but it does not require the user to have access to Earth Engine.
<br><br>

If you want to use the first notebook, please open the notebook within your browser through [GitHub](https://github.com/ba-minor/OR_OWRD_OSU_training/blob/main/notebooks/et_cu_data_retrieval_gee.ipynb) and use the Colab icon at the top of the notebook to start a Google Colab session.

If you want to use the second notebook, please use the workflow below:

---

# 1. Clone the GitHub repository
> find the "<span style="color:green"><> Code</span>" icon
## <span style="color:yellow">Options</span>:
> GitHub Desktop<br>
> Download zip file<br>

---

# 2. Python Installation
> We recommend installing the **Miniconda** version as opposed to the **Anaconda** version. Miniconda is a miniature installation of Anaconda. The guide below will use Miniconda.<br><br>
> If the installation guide below fails, please refer to these links ([Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main), [Anaconda](https://www.anaconda.com/docs/getting-started/anaconda/main)). They contain more detailed information on how to install Python.<br><br>
> Ensure that you are downloading an installer (below) that is compatible with your operating system!

## Windows installation
> Command Prompt - command line interface<br>

Copy and paste the following line of code into the Command Prompt
```bash
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe --output .\Downloads\Miniconda3-latest-Windows-x86_64.exe
```

Then go to the location of your downloaded file (e.g. Downloads folder) and double-click the installer to launch.<br>

After finishing the installation, open Anaconda Prompt (or Command Prompt if you have added the Miniconda path, Miniconda bin folder path, and Miniconda Scripts folder path to your PATH environment variable) and verify the installation by checking the version
```bash
conda --version
```

## MacOS/Linux installation
> Terminal - command line interface<br>

Copy and paste the following lines of code (sequentially) into the Terminal to download
```bash
curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
```

Now install it
```bash
bash ~/Miniconda3-latest-MacOSX-arm64.sh
```

Finally, initialize conda
```bash
conda init
```

Close and reopen your terminal for changes to take effect.<br>

Verify the installation by checking the version.
```bash
conda --version
```

---

# 3. Prepare your Python environment
> You can use the YML file ("environment.yml") or prepare it yourself

Navigate to the repo within Anaconda Prompt or Terminal
> Navigate to the cloned version (local version) of the GitHub repository using "change directory", "cd" for short:
``` bash
cd PATH/TO/OR_OWRD_OSU_training
```

For example, if you cloned the repo to a GitHub folder on a macbook, you would navigate to the folder like this:
```bash
cd /Users/[YOUR_USERNAME]/Documents/GitHub/OR_OWRD_OSU_training
```
<br>

Create the environment one of two ways from the Anaconda Prompt or Terminal:
1. YML file
```bash
conda env create -f environment.yml

conda activate py311
```

2. Prepare it yourself
```bash
conda create -n py311 python=3.11

conda activate py311

conda install -c conda-forge geopandas pandas jupyterlab folium requests
```

Start Jupyter Lab after activating your environment and installing all packages
> The code below should open jupyter in your browser
```bash
jupyter lab
```

Find the notebook within the Jupyter File Browser panel on the left-hand side




