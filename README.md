# 📌 Machine Learning no Azure ML

## 🔹 Visão Geral
Este repositório contém um modelo de previsão treinado e implantado no **Azure Machine Learning**. Para além disso, inclui um passo a passo detalhado do processo de criação e configuração dos **pontos de extremidade**.

## 🛠️ Tecnologias Utilizadas
- **Azure Machine Learning**
- **Python & Jupyter Notebook**
- **Azure ML Studio**
- **APIs REST para consumo do modelo**

## 🚀 Passo a Passo

### 1️⃣ Criar um Workspace no Azure ML
1. Entre no **Azure Portal**.
2. Vá até **Azure Machine Learning** e clique em **Criar workspace**.
3. Configure as opções do workspace (nome, região, assinatura, grupo de recursos, etc.).

### 2️⃣ Criar e Treinar o Modelo
1. No **Azure ML Studio**, crie um **Experimento**.
2. Carregue os dados para treino.
3. Escolha o algoritmo adequado e ajuste os parâmetros.
4. Treine o modelo e avalie seu desempenho.

### 3️⃣ Implantação do Modelo
1. Registre o modelo treinado no **Azure ML Registry**.
2. Configure o **Compute Target** para a implantação.
3. Implante o modelo como um **Web Service**.
4. Gere o **ponto de extremidade REST** para consumo da API.

### 4️⃣ Testar e Consumir a API
1. Copie a URL do **ponto de extremidade**.
2. Utilize **Postman** ou **Python (requests)** para fazer chamadas à API.
3. Passe os dados corretos no formato JSON e analise as previsões.

## 📂 Arquivos no Repositório
- **README.md** → Passo a passo da implementação.
- **endpoints.json** → Arquivo JSON contendo os detalhes dos pontos de extremidade.

## 📌 Como Consumir o Modelo (Exemplo de Requisição)
```python
import requests
import json

url = "https://seu-endpoint.azurewebsites.net/score"
headers = {"Content-Type": "application/json", "Authorization": "Bearer SUA_CHAVE"}

data = {"input_data": [[5.1, 3.5, 1.4, 0.2]]}

response = requests.post(url, headers=headers, data=json.dumps(data))
print(response.json())
```
