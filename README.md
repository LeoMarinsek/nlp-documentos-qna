# 🤖 NLP - Extração de Respostas em Documentos (Português)

Este projeto demonstra o uso de **NLP (Processamento de Linguagem Natural)** com foco em documentos em **português**, utilizando modelos baseados em Transformers para responder perguntas diretamente a partir do conteúdo de arquivos PDF como **contratos ou relatórios**.

---

## 📌 Objetivo

Construir uma solução prática e simples que:
- Leia e processe documentos PDF em português
- Faça extração de texto e pré-processamento
- Aplique **Reconhecimento de Entidades Nomeadas (NER)**
- Permita realizar **perguntas e respostas (QnA)** sobre o conteúdo
- Exponha a solução como uma **API REST usando Flask**

---

## 📁 Estrutura de Pastas

```
nlp_documentos_qna/
├── data/
│   ├── exemplo_contrato.pdf
│   └── texto_limpo.txt
├── notebooks/
│   ├── 01_exploracao_pdf.ipynb
│   ├── 02_leitura_pdf_preprocessamento.ipynb
│   ├── 03_nlp_extracao_ner.ipynb
│   ├── 04_perguntas_respostas_qna.ipynb
│   └── 05_api_flask_qna.ipynb
├── README.md
├── requirements.txt
```

---

## 🧰 Tecnologias e Ferramentas

- Python
- Jupyter Notebook
- Transformers (Hugging Face)
- Flask + Flask-CORS
- PyMuPDF (fitz)
- SpaCy (pt_core_news_sm)
- pip, requests, pandas, numpy

---

## 📚 Etapas do Projeto

### 📄 01 - Leitura e exploração do PDF
- Utiliza PyMuPDF para extrair texto página por página
- Visualiza a estrutura geral do documento

### 🧼 02 - Pré-processamento de texto
- Remove espaços desnecessários, quebras de linha, símbolos
- Gera um arquivo `.txt` com o conteúdo limpo

### 🧠 03 - Extração de entidades (NER)
- Usa SpaCy com modelo em português
- Identifica entidades como ORG, MONEY, DATE, PERSON

### ❓ 04 - Perguntas e respostas (QnA)
- Utiliza o modelo `pierreguillou/bert-base-cased-squad-v1.1-portuguese`
- Permite perguntar livremente sobre o conteúdo
- Exibe a resposta mais provável e a confiança

### 🌐 05 - API Flask
- Cria uma API REST com Flask
- Permite enviar perguntas via POST e retornar a resposta
- Exemplo de uso com `requests`

---

## 🔧 Como Executar

```bash
git clone https://github.com/seu-usuario/nlp-documentos-qna.git
cd nlp-documentos-qna
pip install -r requirements.txt
```

Execute os notebooks em ordem de 01 até 05.

---

## 🔍 Exemplo de saída da API

```json
{
  "pergunta": "Qual o valor do contrato?",
  "resposta": "R$ 12.000,00",
  "score": 0.75
}
```

---

## 📦 Futuras melhorias

- Interface Web (Streamlit ou React)
- Armazenamento em banco de dados vetorial (VectorDB)
- Uso de Langchain e RAG com documentos múltiplos
- Deploy com Docker ou FastAPI

---

## 👨‍💻 Autor

**Leonardo Thomaz Marinsek**  
