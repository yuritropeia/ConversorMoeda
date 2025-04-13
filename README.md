# 💱 Conversor de Moedas em Python

Este é um projeto de **conversor de moedas em Python**, que utiliza a biblioteca `customtkinter` para a interface gráfica e realiza integrações com fontes externas (API e XML) para obter cotações atualizadas e listas de moedas disponíveis. O objetivo é fornecer uma maneira prática e visual de consultar a conversão de valores entre diferentes moedas.

---

## 🗂 Estrutura do Projeto

```
📁 conversor_moedas/
  ├── main.py                # Interface principal com CustomTkinter
  ├── pegar_cotacao.py       # Integração com API de câmbio (economia.awesomeapi.com.br)
  ├── pegar_moedas.py        # Leitura de arquivos XML para listar moedas e câmbios
```

---

## 📌 Funcionalidades

- Interface gráfica moderna com `CustomTkinter`
- Seleção de moeda de origem e destino
- Conversão em tempo real com dados atualizados
- Leitura dinâmica de moedas e pares de câmbio via arquivos XML
- Integração com API externa para obtenção da taxa de câmbio atual

---

## 📸 Interface do Usuário

A interface apresenta:

- Um **menu suspenso** para selecionar a moeda de origem
- Um **menu suspenso** para selecionar a moeda de destino
- Um **botão de conversão** que realiza o cálculo da taxa
- Um **campo de resultado** que exibe quanto vale 1 unidade da moeda de origem na moeda de destino
- Uma **lista de moedas** com descrição de cada sigla no câmbio

![image](https://github.com/user-attachments/assets/1fb4c7b2-9f51-4578-bb51-881323b55819)

---

## 🔧 Tecnologias Utilizadas

- Python 3.9+
- [CustomTkinter]
- `requests`
- `xml.etree.ElementTree` (leitura dos XMLs)
- API pública: [economia.awesomeapi.com.br]

---

## 📄 Detalhes dos Arquivos

### `main.py`

- Responsável por construir a interface gráfica do usuário
- Importa os métodos `pegar_cotacao()` e `pegar_moedas()` dos arquivos auxiliares
- Apresenta os campos interativos e faz a chamada à função de conversão ao clicar no botão

### `pegar_cotacao.py`

- Realiza uma requisição HTTP à API da AwesomeAPI
- Retorna o valor atual da cotação no formato JSON
- Exemplo de endpoint utilizado: `https://economia.awesomeapi.com.br/last/USD-BRL`

### `pegar_moedas.py`

- Lê dois arquivos XML:
  - Um com a **lista de moedas disponíveis**
  - Outro com os **pares de câmbio suportados**
- Constrói listas de moedas que são retornadas para preenchimento da interface

---

## 📦 Como Executar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seuusuario/conversor_moedas.git
   cd conversor_moedas
   ```

2. **Instale as dependências:**
   ```bash
   pip install customtkinter requests
   ```

3. **Execute o aplicativo:**
   ```bash
   python main.py
   ```

---

## 🧪 Exemplo de Uso

- Escolha "USD" como moeda de origem e "BRL" como destino
- Clique em **Converter**
- A interface irá exibir algo como:
  ```
  1 USD = 5.08 BRL
  ```
