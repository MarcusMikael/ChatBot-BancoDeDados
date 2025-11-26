# Chatbot com Banco de Dados Vetorial – N8N + Supabase

##  Descrição do Projeto
Este projeto implementa um chatbot baseado em busca semântica, capaz de responder perguntas sobre conteúdos de Banco de Dados utilizando um banco vetorial.

O sistema usa embeddings para comparar a pergunta do usuário com documentos armazenados e retornar a resposta mais adequada.

---

##  Tecnologias Utilizadas

- **N8N** – Orquestração dos fluxos e criação do chatbot
- **Supabase + pgvector** – Banco vetorial para armazenamento e consulta de embeddings
- **OpenAI** – Geração dos embeddings e resposta final
- **Google Drive** – Fonte do conhecimento do chatbot pelos arquivo que contém.

---

## Funcionamento da Busca Semântica

1. O usuário envia uma pergunta pelo chat do n8n  
2. A pergunta é convertida em um vetor (embedding)  
3. Esse vetor é comparado com os vetores dos documentos armazenados  
4. Os trechos mais semelhantes são retornados  
5. A IA monta a resposta usando esses trechos  
6. O usuário recebe a resposta final

Esse processo permite que o chatbot encontre respostas mesmo que as palavras exatas não apareçam nos documentos.

---

## Estrutura do Repositório

/
├── workflow/ # Workflow exportado do n8n
│ └── ChatBot - Banco De Dados.json
│
├── src/ # Códigos da criação do  banco
│ └── Scripts SQL
│
├── docs/ # Relatório técnico
│ └── Relatório ChatBot.pdf
│
└── README.md # Este arquivo

---

##  Como importar o workflow

1. Abra o n8n  
2. Clique em **Import**  
3. Selecione o arquivo:

/workflow/ChatBot - Banco De Dados.json

O fluxo será carregado com:

- Trigger de mensagem  
- Criação de embeddings  
- Consulta ao Supabase  
- Resposta usando IA

---

## Prints do funcionamento 

<img width="1354" height="645" alt="image" src="https://github.com/user-attachments/assets/4c1891dd-1cc7-4565-9887-ad20557898de" />

<img width="1362" height="645" alt="image" src="https://github.com/user-attachments/assets/67be384f-3ec5-461b-9325-9bcddc0aae5c" />


## Vídeo de Apresentação    

 [Assista ao vídeo aqui](https://youtu.be/CqsENO5hzRk)

👤 Autores

Marcus Mikael Rodrigues Vieira.
João Pedro Lima Barbosa.
