# DSPy-Notebooks
The task was to use DSPy in our backend of the Slide Evaluation Support System to ensure reproducibility and optimize the way we call the LLMs. This repository explores several Working Examples and tries out optimizers initially intended for other use cases on our own use case. The most valuable results are the pipelines and BootstrapFewShot. 

The easiest way to run them is via Anaconda > Jupyter Notebooks or via your G-Mail Account by opening it as a Google Colab Notebook.

If you would like to run the Notebooks locally, please follow the following description in a local terminal e.g. inside of Visual Studio Code.

1. **Install Miniconda or Anaconda:**
   - If you haven't already installed Conda, you can download and install Miniconda or Anaconda from the official website. Miniconda is a lightweight version of Anaconda, and Anaconda comes with a lot of pre-installed packages. Choose the one that best fits your needs.

2. **Open a Terminal or Command Prompt:**
   - Once Conda is installed, open a terminal (on Linux/macOS) or command prompt (on Windows).

3. **Create a New Environment:**
   - To create a new environment, you can use the following command:
     ```bash
     conda create --name myenv python=3.8
     ```
     Replace myenv with the name you want to give to your environment. You can also specify the Python version you want to use by replacing 3.8 with your desired version.

4. **Initialize Conda:**
   - Run the following command to set up Conda's shell initialization scripts:
     ```bash
     conda init
     ```
     This command will set up Conda's shell initialization scripts. It may prompt you to restart your terminal or command prompt session for the changes to take effect. Follow any instructions provided after running this command.

5. **Restart Terminal/Command Prompt:**
   - After running conda init, close and reopen your terminal or command prompt. This step is necessary to ensure that the changes made by conda init are applied.

6. **Activate the Environment:**
   - After creating the environment, you need to activate it using the following command:
     ```bash
     conda activate myenv
     ```
     If you experience issues, double-check that you've followed all the steps correctly and that your Conda installation is up-to-date.

7. **Install Packages:**
   - Once the environment is activated, you can install the required packages using Conda or pip:
     ```bash
     %pip install gradio requests openai dspy-ai pytesseract pillow tesseract dspy
     ```
8. **Set an OpenAI API-Key as an environmental variable:**
   - Set an OPENAI_API_KEY
     ```bash
     export OPENAI_API_KEY='your-api-key-here'
     ```
## Troubleshooting

- **Permission Error:**
  - If you encounter an error message such as `'ModuleNotFoundError'` or similar, even though you have installed the required package, it may be due to a permission issue. In such cases, try using `sudo` (on Unix-based systems) to install the package with elevated privileges. For example:
    ```bash
    sudo pip install package_name
    ```
    Replace `package_name` with the name of the package you're trying to install. Note that using `sudo` grants elevated privileges, so exercise caution when using this command.

8. **Deactivate the Environment:**
   - Once you're done working in your environment, you can deactivate it using the following command:
     ```bash
     conda deactivate
     ```

