# Notebooks
Flyflow jupyter notebook experiments

## Installing Jupyter Notebook Locally
This guide will walk you through the process of installing Jupyter Notebook on your local machine.

### Prerequisites
Python 3.x installed on your system. You can download it from the official Python website: https://www.python.org/downloads/
Installation Steps
- Open a terminal or command prompt.
- Install Jupyter Notebook using pip, the Python package installer, by running the following command:
```bash
pip install jupyter
```

Wait for the installation process to complete. Pip will download and install Jupyter Notebook along with its dependencies.
Once the installation is finished, you can launch Jupyter Notebook by running the following command in your terminal:
```bash
jupyter notebook
```

Jupyter Notebook will start running and open a web browser window or tab. If it doesn't open automatically, you can copy the URL displayed in the terminal and paste it into your browser's address bar.
You will see the Jupyter Notebook interface in your browser, which shows the contents of the directory where you ran the command.
To create a new notebook, click on the "New" button in the top right corner and select "Python 3" from the dropdown menu.
A new notebook will open in a new tab, and you can start writing and executing Python code in the notebook cells.

## Setting Up Private Environment Variables

To set up your database URL. 

Install the python-dotenv package using pip:
```bash
pip install python-dotenv
```

Create a file named .env in the same directory as your notebook. This file will store your private environment variables.
Open the .env file in a text editor and add your environment variables in the following format:

```
DATABASE_URL=mysql://user:password@localhost/database
```

In your Jupyter Notebook, you can load the environment variables using the load_dotenv function from the dotenv module. Add the following code at the beginning of your notebook:

```python
from dotenv import load_dotenv

load_dotenv()
```

Now you can access your environment variables using the os.getenv function. For example:
```python
import os

database_url = os.getenv('DATABASE_URL')
```

Make sure to add the .env file to your .gitignore file to prevent sensitive information from being pushed to version control repositories.

