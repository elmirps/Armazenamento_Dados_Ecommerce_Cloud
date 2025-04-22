# 🛒 Armazenando Dados de um E-Commerce na Cloud

Este projeto faz parte do **Laboratório da Digital Innovation One (DIO)**, dentro do bootcamp **Microsoft Azure Cloud Native**. O objetivo é demonstrar como criar uma estrutura básica para armazenar dados de produtos de um e-commerce em uma base de dados na nuvem.

## 🎓 Aprendizados

Durante a execução deste lab, foram abordados:

- Publicação em um Azure SQL Database
- Criação de tabelas SQL com atributos essenciais para um e-commerce
- Uso de scripts SQL para estruturação inicial da base de dados
- Desenvolvimento de scripts Python para inserir dados no banco
- Utilização do **Streamlit** para criação de uma interface visual simples
- Armazenamento de arquivos em nuvem com **Azure Storage Blob**
- Upload de imagens diretamente para o **Azure Blob Storage**
  
## 📂 Estrutura dos Arquivos

- `infos.txt`: Contém credenciais de acesso e script de criação da tabela `Produtos`
- `produtos.json`: Simula um conjunto de produtos com nome, descrição, preço e URL de imagem
- `main.py`: Script Python que consome os dados do JSON e insere na base
- `requirements.txt`: Lista as dependências do projeto, incluindo `streamlit` e `azure-storage-blob`

## 🗃️ Tabela Criada

```sql
CREATE TABLE Produtos (
    id INT IDENTITY(1,1) PRIMARY KEY,
    nome NVARCHAR(255),
    descricao NVARCHAR(MAX),
    preco DECIMAL(18,2),
    imagem_url NVARCHAR(2083)
)
```

## 🚀 Como Executar

1. Clone este repositório:
    ```bash
    git clone https://github.com/digitalinnovationone/Microsoft_Application_Platform.git
    ```
2. Acesse o diretório do Lab01:
    ```bash
    cd Microsoft_Application_Platform/Labs/Lab01
    ```
3. Instale as dependências:
    ```bash
    pip install -r requirements.txt
    ```
4. Execute a interface com Streamlit:
    ```bash
    streamlit run main.py
    ```

## 🌐 Recursos

- Bootcamp completo na [plataforma da DIO](https://web.dio.me/track/microsoft-azure-cloud-native)
- Repositório oficial no [GitHub](https://github.com/digitalinnovationone/Microsoft_Application_Platform)

## ✨ Possíveis Expansões

- Integração com APIs REST para CRUD
- Manipulação de arquivos JSON para simulação de dados
- Interface web para administração dos produtos
- Autenticação e controle de acesso

---

Desenvolvido como parte do programa educacional da DIO ✨



