Step 1: Install Ollama (Ubuntu)
```
curl https://ollama.ai/install.sh | sh
```
Step 2: Identify the Model you would like to use in the local:

| Model | Parameters | Size | Download |
|-------|------------|------|----------|
| Llama 2 | 7B | 3.8GB | ollama run llama2 |
| Mistral | 7B | 4.1GB | ollama run mistral |
| Dolphin Phi | 2.7B | 1.6GB | ollama run dolphin-phi |
| Phi-2 | 2.7B | 1.7GB | ollama run phi |
| Neural Chat | 7B | 4.1GB | ollama run neural-chat |
| Starling | 7B | 4.1GB | ollama run starling-lm |
| Code Llama | 7B | 3.8GB | ollama run codellama |
| Llama 2 Uncensored | 7B | 3.8GB | ollama run llama2-uncensored |
| Llama 2 13B | 13B | 7.3GB | ollama run llama2:13b |
| Llama 2 70B | 70B | 39GB | ollama run llama2:70b |
| Orca Mini | 3B | 1.9GB | ollama run orca-mini |
| Vicuna | 7B | 3.8GB | ollama run vicuna |
| LLaVA | 7B | 4.5GB | ollama run llava |

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


## Modify the existing Model:

Pull the Model in local:
```
ollama pull llama2
```

Create a Modelfile:

```
FROM llama2

# set the temperature to 1 [higher is more creative, lower is more coherent]
PARAMETER temperature 1

# set the system message
SYSTEM """
You are Mario from Super Mario Bros. Answer as Mario, the assistant, only.
"""
```
Next, create and run the model:

```
ollama create mario -f ./Modelfile
ollama run mario
>>> hi
Hello! It's your friend Mario.
```
