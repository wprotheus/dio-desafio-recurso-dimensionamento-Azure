# DIO - Trilha Java Básico

## Autor

🔸[wprotheus](https://github.com/wprotheus)

---

## Desafio - Recursos e Dimensionamentos na Azure

Atividade executada conforme orientações abaixo, retiradas do [Descrição do Desafio](https://web.dio.me/lab/computacao-e-rede-laboratorio/learning/9322371b-97ee-4148-8f27-70b7b6f38a47)  
<small><sup>Obs.: O link acima somente é acessado através de uma conta na plataforma DIO.</sup></small>

### Descrição do Desafio

> Este laboratório tem como objetivo **explorar os recursos da plataforma Microsoft Azure.**
  
### Orientações para a entrega:

> - Entregue o link do repositório como parte da conclusão do desafio. Esse link será o acesso direto ao seu resumo documentado no GitHub.

---  

# ⚙️ Configurando Recursos e Dimensionamentos em Máquinas Virtuais na Azure

## 🎯 Objetivo

Criar uma **Máquina Virtual (VM)** no Azure com recursos dimensionados corretamente (CPU, RAM, disco, rede) conforme a necessidade do cenário.

---

## ✅ Pré-requisitos

- Conta ativa na Azure
- Grupo de Recursos já criado
- Permissão para provisionar VMs

---

## 📘 Passo a Passo

### 1. Acessar o Portal Azure

- [https://portal.azure.com](https://portal.azure.com)

---

### 2. Criar uma Nova Máquina Virtual

1. Pesquise por **"Máquinas Virtuais"** > clique em **“+ Criar”**
2. Configure a aba **Básico**:
    - **Grupo de Recursos:** selecione o existente
    - **Nome da VM:** `vm-demo`
    - **Região:** selecione a mais próxima
    - **Imagem:** `Ubuntu 22.04` ou `Windows Server 2022`
    - **Tipo de autenticação:** senha ou chave SSH
    - **Nome de usuário:** `azureuser`
    - **Senha/chave:** defina conforme política

---

### 3. Escolher Tamanho (Dimensionamento)

- Clique em **“Alterar tamanho”**
- Selecione uma opção com base no uso:

| Tipo de Carga    | Tamanho sugerido    | Descrição                     |
|------------------|---------------------|-------------------------------|
| Testes/Dev       | `B1s`, `B2s`        | Baixo custo, uso básico       |
| Web/App Server   | `D2s_v3`, `D4s_v3`  | Balanceado                   |
| Alta performance | `F4s_v2`, `E4s_v3`  | CPU ou memória intensivo     |

> ⚠️ O custo varia conforme o tipo de VM.

---

### 4. Configurar Disco e Rede

- **Disco do SO:** SSD padrão ou premium
- **Disco de dados:** opcional, conforme necessidade
- **Rede virtual/Sub-rede:** use existente ou crie nova
- **IP público:** necessário se desejar acesso remoto

---

### 5. Revisar + Criar

- Verifique todas as configurações
- Clique em **Criar**
- Aguarde o provisionamento

---

## 📈 Dicas de Dimensionamento

- **CPU e RAM sob demanda:** pode ser redimensionado depois
- **Monitoramento:** use o Azure Monitor para avaliar consumo
- **Tags:** use para organização e controle de custos

---

## ✅ Resultado Esperado

Máquina Virtual configurada corretamente, com recursos compatíveis com a carga de trabalho pretendida, pronta para uso via SSH ou RDP.

---  

## 📷 Capturas de telas

### Tela #1:
<img src="./img_vm/tela (3).png" alt="Tela criando VM" width="350px"/>  

### Tela #2:
<img src="./img_vm/tela (2).png" alt="Tela conexão VM via SSH/CLI" width="350px"/> 

### Tela #3:
<img src="./img_vm/tela (1).png" alt="Tela terminal Ubuntu" width="350px"/>  

### Tela #4:
<img src="./img_vm/tela (4).png" alt="Tela recursos criados" width="350px"/>

---  

> **Nota:** Este guia aborda configurações básicas. Para recursos avançados e personalizações, consulte a documentação oficial da [Microsoft](https://learn.microsoft.com/pt-br/azure/virtual-machines/).
