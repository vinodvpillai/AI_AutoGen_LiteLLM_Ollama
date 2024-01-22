# Ollama
Ollama is a tool that allows you to run open-source large language models (LLMs) locally on your machine. It supports a variety of models, including Llama 2, Code Llama, and others.

Step 1: Install Ollama (Ubuntu)
```
curl https://ollama.ai/install.sh | sh
```
Step 2: Identify the Model you would like to use in the local:

Reference: https://github.com/jmorganca/ollama

Step 3: Pull & Run the Model in local
```
ollama run mistral
```
Step 4: Pull the Model in local:
```
ollama pull llama2
```
Step 5: Remove the Model from local:
```
ollama rm llama2
```

---

# Python (Ubuntu)

```
sudo add-apt-repository ppa:deadsnakes/ppa

sudo apt install python3.11

sudo apt install python3.11-full

python3.11 -V
```

---

# Create Python VM

Step 1: Get into the folder
```
python3.11 -m venv .venv
```
Step 2: Activate the Virtual Machine
```
source .venv/bin/activate
```
Step 3: Verify we are using the correct Python Version & PIP
```
python -V
pip -V
```

---
# Autogen

Inside the Python VM and install the Autogen using pip

```
pip install pyautogen
```
---

# Litellm

Inside the Python VM and install the litellm using pip

```
pip install litellm
pip install 'litellm[proxy]'
```
---

# Now we ask litellm to access the alreading running Ollama Model - mistral

```
litellm --model ollam/mistral
```
