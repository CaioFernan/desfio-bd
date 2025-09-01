# 🧪 Prática: Configuração de uma Instância de Banco de Dados no Microsoft Azure

## 🎯 Objetivo
Criar, configurar e testar a conexão a uma instância de banco de dados na plataforma Azure.

---

## 1️⃣ Acessar o Portal
1. Entre em [https://portal.azure.com](https://portal.azure.com).
2. Faça login com sua conta Microsoft.

---

## 2️⃣ Criar Recurso de Banco de Dados
1. No menu lateral, clique em **Criar um recurso**.
2. Pesquise por **SQL Database** (ou escolha MySQL/PostgreSQL se preferir).
3. Clique em **Criar**.

---

## 3️⃣ Configurações Básicas
- **Assinatura**: selecione sua assinatura ativa.  
- **Grupo de recursos**: crie um novo (ex.: `rg-lab-db`).  
- **Nome do Banco**: `sqldb-lab`.  
- **Servidor**: clique em **Criar novo** e defina:
  - Nome do servidor (único globalmente).
  - Região: *Brazil South*.
  - Autenticação: **Login e senha** (ex.: usuário `dbadmin`).  

---

## 4️⃣ Computação + Armazenamento
- Selecione o nível de serviço:
  - **Basic** ou **S0** (baixo custo, ideal para prática).
- Ajuste armazenamento padrão (não precisa aumentar para testes).

---

## 5️⃣ Rede
- Configure acesso:  
  - **Acesso público** → **Adicionar meu IP**.  
  - (Para prática, não há necessidade de Private Endpoint).

---

## 6️⃣ Revisar e Criar
- Clique em **Revisar + Criar**.  
- Verifique os dados.  
- Clique em **Criar**.  
⏳ Aguarde a implantação.

---

## 7️⃣ Testar Conexão
- Após criada, abra o recurso da base.  
- Copie o **nome do servidor** (ex.: `sqlsrv-lab.database.windows.net`).  
- No seu computador (Ubuntu), instale cliente SQL:
  ```bash
  sudo apt update && sudo apt install -y mssql-tools
