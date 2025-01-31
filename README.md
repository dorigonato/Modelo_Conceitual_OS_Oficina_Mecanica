# **Modelo de Banco de Dados para Oficina Mecânica**

## **📌 Descrição do Projeto**
Este projeto contém um modelo de banco de dados relacional para o gerenciamento de **ordens de serviço (OS)** em uma oficina mecânica. O objetivo é otimizar o controle de clientes, veículos, mecânicos, serviços e peças, garantindo um sistema eficiente e escalável.

## **📌 Entidades Principais**

### **1️⃣ Cliente**
Armazena informações de clientes, podendo ser **Pessoa Física** ou **Pessoa Jurídica**.

### **2️⃣ Pessoa Física & Pessoa Jurídica**
- **Pessoa Física:** Nome, CPF, Data de Nascimento.
- **Pessoa Jurídica:** Razão Social, CNPJ, Nome Fantasia, Inscrição Estadual.

### **3️⃣ Veículo**
Registra os veículos dos clientes, contendo informações como **placa, marca, modelo e ano**.

### **4️⃣ Ordem de Serviço (OS)**
Controla os serviços realizados nos veículos, armazenando **status, valor total e data de conclusão**.

### **5️⃣ Equipe de Mecânicos & Mecânicos**
- Cada mecânico pertence a uma equipe.
- A equipe é responsável por executar as OS designadas.

### **6️⃣ Serviço & Peça**
- **Serviço:** Contém a descrição e o valor padrão.
- **Peça:** Contém a descrição e o valor unitário.

### **7️⃣ Tabela de Mão de Obra**
Define os valores padronizados da mão de obra para cada tipo de serviço.

## **📌 Relacionamentos Principais**
1. **Cliente (1:N) Veículo** - Um cliente pode ter vários veículos.
2. **Veículo (1:N) OS** - Um veículo pode ter várias ordens de serviço.
3. **Equipe (1:N) Mecânico** - Uma equipe pode ter vários mecânicos.
4. **Equipe (1:N) OS** - Uma equipe pode gerenciar várias OS.
5. **OS (N:M) Serviço** - Uma OS pode conter vários serviços.
6. **OS (N:M) Peça** - Uma OS pode conter várias peças.
