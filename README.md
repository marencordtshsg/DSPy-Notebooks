# DSPy-Notebooks
The task was to use DSPy in our backend of the Slide Evaluation Support System to ensure reproducibility and optimize the way we call the LLMs. This repository explores:

(1) Working Examples on other tasks, e.g., HotPotQA, GSM8K, and 
(2) defines and technically assessed a self-defined metric "completeness_check" for the procession of checkpoints in the Single Slide Feedback and 
(3) tries out optimizers initially intended for other use cases on the output of our Single Slide Feedback.

To our surprise, the GSM8K Examples, applied on Examples containing slide input and expected output of our Single Slide Feedback, leads to an output which is exactly how we would like the Single Slide Feedback to be. The DSPy module ChainOfThought inside of the optimizer BootstrapFewShot that is trained on an Example from the Single Slide Feedback and optimized along the pre-defined metric gsm8k_metric, leads to an output for the Single Slide Feedback, which meets our expectations. However, as we are training and developing on the same example, this is clearly an overfit. **[TO-DO: Generate more examples of the form: Example({'question': "[slide.markdown]", 'gold_reasoning': "[prompt including checkpoints]", 'answer': "[example of a great example for Single Slide Feedback Output]})] and add it to "Min Work Ex GSM8K applied on Single Slide Feedback.ipynb" so that trainset does not equal devset anymore**.

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

### Table of Contents
***NO SETUP NEEDED*** 
HotPotQA.ipynb is a working example based on a powerful database of English Wikipedia and executes a small question-answering-game that tests the LM's capability to retrieve information from a question and sections in the context to generate a correct response.//
***OPENAI_API_KEY SETUP NEEDED***
Min Work Ex GSM8K applied on Single Slide Feedback.ipynb applies the GSM8K optimizer on our use case by training the LLM program on positive examples.
Minimum Working Example GSM8K illustrates the main functionality of the 'teleprompter', a program which saves how we call an LLM and that can be optimized and used further in other parts of our code. 




