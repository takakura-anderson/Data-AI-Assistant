# 🧠 Corporate Data AI Assistant

> Assistente Inteligente de Dados Corporativos executado 100% localmente utilizando Large Language Models (LLMs) através do Ollama.

## 📖 Sobre o projeto

O **Corporate Data AI Assistant** é um assistente virtual especializado em análise de dados, engenharia de dados e documentação técnica, desenvolvido para executar modelos de Inteligência Artificial localmente, preservando a privacidade das informações corporativas.

O projeto permite que o usuário converse com diferentes especialistas, envie documentos para análise e obtenha respostas contextualizadas sem depender de serviços em nuvem.

Este projeto foi desenvolvido como evolução do laboratório **"Construa Seu Assistente Virtual com Inteligência Artificial"**, demonstrando a aplicação prática de IA Local, Engenharia de Prompt e processamento inteligente de documentos.

---

# 🎯 Objetivos

* Executar IA completamente offline
* Preservar a privacidade dos dados
* Auxiliar profissionais de dados
* Responder utilizando conhecimento proveniente de documentos enviados pelo usuário
* Evitar respostas inventadas quando não houver informação suficiente
* Demonstrar boas práticas de Engenharia de IA

---

# ✨ Funcionalidades

## 💬 Chat Inteligente

* Conversação em linguagem natural
* Histórico de conversa
* Janela dinâmica de contexto
* Gerenciamento automático de tokens

---

## 🧠 Especialistas disponíveis

O usuário pode selecionar diferentes perfis especializados:

* SQL & Bancos de Dados
* Python & Engenharia de Dados
* Power BI
* Assistente Técnico

Cada especialista utiliza instruções (System Prompt) específicas para melhorar a qualidade das respostas.

---

## 📂 Base de Conhecimento

O assistente pode extrair conhecimento automaticamente de diversos formatos de arquivos.

### Arquivos suportados

* CSV
* Excel (.xlsx/.xls)
* Parquet
* PDF
* DOCX
* TXT
* Markdown
* Python
* SQL
* JSON
* XML
* YAML

Após o upload, o sistema produz um resumo estrutural do documento e utiliza essas informações como contexto para responder às perguntas do usuário.

---

## 📊 Telemetria

O sistema acompanha em tempo real:

* consumo de tokens
* janela de contexto
* velocidade da inferência
* tempo de resposta
* modelo utilizado
* utilização da memória de contexto

---

# 🏗 Arquitetura

```
Usuário
      │
      ▼
 Interface Streamlit
      │
      ▼
 Seleção do Especialista
      │
      ▼
 System Prompt
      │
      ▼
 Base de Conhecimento
(upload de arquivos)
      │
      ▼
 Janela Dinâmica de Contexto
      │
      ▼
 Ollama
(Modelo Local)
      │
      ▼
Resposta da IA
```

---

# 🛠 Tecnologias utilizadas

* Python
* Streamlit
* Ollama
* Pandas
* Transformers
* PyPDF
* python-docx
* PyYAML
* dotenv

---

# 🤖 Modelos suportados

O projeto foi desenvolvido para trabalhar com modelos executados pelo Ollama, como por exemplo:

* Qwen 2.5 Coder
* Gemma 4
* Phi-4 Mini Reasoning

O modelo pode ser alterado dinamicamente pela interface.

---

# 🔒 Privacidade

Um dos principais objetivos do projeto é manter os dados dentro da infraestrutura do usuário.

Todas as consultas são realizadas localmente através do Ollama, evitando o envio de documentos corporativos para serviços externos.

---

# 📈 Métricas monitoradas

Durante a execução o sistema apresenta:

* Tokens de entrada
* Tokens de saída
* Utilização da janela de contexto
* Tempo de inferência
* Velocidade (tokens/segundo)
* Modelo em execução

---

# 🚀 Como executar

## 1. Clone o repositório

```bash
git clone https://github.com/SEU_USUARIO/corporate-data-ai-assistant.git
```

## 2. Entre na pasta

```bash
cd corporate-data-ai-assistant
```

## 3. Crie um ambiente virtual

```bash
python -m venv .venv
```

Windows

```bash
.venv\Scripts\activate
```

Linux

```bash
source .venv/bin/activate
```

## 4. Instale as dependências

```bash
pip install -r requirements.txt
```

## 5. Instale os modelos no Ollama

Exemplo:

```bash
ollama pull qwen2.5-coder:3b
ollama pull gemma4:e4b
ollama pull phi4-mini-reasoning
```

## 6. Execute

```bash
streamlit run src/app.py
```

---

# 📂 Estrutura do projeto

```
corporate-data-ai-assistant/

├── src/
├── docs/
├── data/
├── README.md
├── LICENSE
├── requirements.txt
├── .gitignore
└── .env.example
```

---

# 🎓 Aprendizados

Este projeto reúne diversos conceitos de Engenharia de IA, incluindo:

* Prompt Engineering
* IA Local
* Retrieval baseado em documentos
* Gerenciamento de contexto
* Engenharia de Dados
* Processamento de documentos
* Streamlit
* Observabilidade
* Arquitetura modular

---

# 🔮 Próximos passos

* RAG utilizando banco vetorial
* Embeddings locais
* Memória persistente entre sessões
* Suporte a múltiplos documentos simultaneamente
* Citação das fontes utilizadas nas respostas
* Integração com bancos de dados
* Interface para gerenciamento de conhecimento
* Arquitetura multiagente

---

# 📄 Licença

Este projeto está licenciado sob a **MIT License**.

---

# 👨‍💻 Autor

**Anderson Takakura**

Projeto desenvolvido para fins de estudo, experimentação e evolução em Inteligência Artificial aplicada, Engenharia de Dados e IA Local.
