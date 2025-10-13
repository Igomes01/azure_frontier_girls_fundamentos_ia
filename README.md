# 🤖 Fundamentos de IA com Azure - Frontier Girls

Bem-vinda ao repositório de fundamentos de Inteligência Artificial usando Azure! Este projeto foi criado para te ajudar a dar os primeiros passos no mundo da IA, usando ferramentas da Microsoft Azure.

## 📚 Sobre este Projeto

Este repositório contém materiais práticos e didáticos para aprender:
- Como se conectar com modelos de IA da Azure OpenAI
- Como criar agentes inteligentes que realizam tarefas específicas
- Como criar ferramentas (tools) para os agentes usarem
- Como orquestrar múltiplos agentes para trabalharem juntos

## 🎯 Para Quem é Este Projeto?

Este projeto é perfeito para você que:
- **Já tem experiência com código**
- ✨ Está começando a aprender sobre Inteligência Artificial
- 🌱 Quer entender como usar IA na prática
- 🔧 Deseja criar suas próprias aplicações de IA
- 🚀 Quer explorar as ferramentas de IA da Microsoft Azure


## 📋 Pré-requisitos

Antes de começar, você vai precisar:

### 1. Python instalado
- Versão: Python 3.10 ou superior
- [Download Python](https://www.python.org/downloads/)

### 2. Conta na Azure
- Crie uma conta gratuita: [Portal Azure](https://azure.microsoft.com/free/)
- Você ganha créditos grátis para testar!

### 3. Git instalado
- Git: Sistema de controle de versão necessário para clonar o repositório
- [Download Git](https://git-scm.com/downloads)
- **Windows**: Durante a instalação, aceite as opções padrão
- **Mac**: Git já vem instalado ou use `brew install git`
- **Linux**: Use `sudo apt install git` (Ubuntu) ou equivalente

### 4. Azure CLI instalado
- Azure CLI (Command-Line Interface): Ferramenta essencial para autenticação com Azure
- [Download Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli)
- Após instalar, você precisará fazer login com `az login`

### 5. Editor de Código
- Visual Studio Code (recomendado): [Download VS Code](https://code.visualstudio.com/)
- Extensão Jupyter para VS Code

### 6. Conhecimentos Básicos
- Python básico (variáveis, funções, imports)
- Vontade de aprender! 🎓

## 🚀 Como Começar

**Clique em ctrl+' no VsCode para abrir o prompt de comando e rodar os seguintes codigos:**

### Passo 1: Obtenha os Arquivos do Projeto

**Opção A: Usando Git (Recomendado)**
```bash
git clone https://github.com/Igomes01/azure_frontier_girls_fundamentos_ia.git
cd azure_frontier_girls_fundamentos_ia
```

**Opção B: Download direto (se não tiver Git instalado)**
1. Vá para: https://github.com/Igomes01/azure_frontier_girls_fundamentos_ia
2. Clique no botão verde "**Code**" → "**Download ZIP**"
3. Extraia o arquivo ZIP em uma pasta de sua escolha
4. Abra o terminal na pasta extraída

### Passo 2: Crie um Ambiente Virtual

**Windows (PowerShell ou CMD):**
```bash
python -m venv .venv
.venv\Scripts\activate
```

**Linux/Mac:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### Passo 3: Faça Login no Azure CLI

**Importante:** Este passo é essencial para autenticação!

```bash
az login
```

Este comando vai:
- Abrir uma janela no navegador
- Solicitar que você faça login com sua conta Azure
- Autenticar sua máquina para usar os recursos do Azure

**Nota:** Se você estiver usando o notebook `criacao_agentes.ipynb` que trabalha com agentes, o `az login` é **obrigatório** para que a autenticação funcione corretamente.

### Passo 4: Instale as Dependências Python

```bash
pip install openai azure-ai-projects azure-identity agent-framework python-dotenv
```

Ou, alternativamente, use o arquivo `requirements.txt`:

```bash
pip install -r requirements.txt
```

### Passo 5: Configure suas Credenciais do Azure

1. Crie um arquivo `.env` na raiz do projeto (já existe um modelo)
2. Preencha com suas credenciais do Azure:

```env
AZURE_AI_PROJECT_ENDPOINT=seu-endpoint-aqui
AZURE_AI_MODEL_DEPLOYMENT_NAME=nome-do-seu-modelo
AZURE_MODEL_ENDPOINT=endpoint-do-modelo
AZURE_AI_MODEL_API_KEY=sua-chave-api-aqui
```

### Passo 6: Abra os Notebooks

Abra o VS Code na pasta do projeto e comece pelos notebooks na ordem:

1. **`chat.ipynb`** - Introdução: seu primeiro chat com IA
2. **`criacao_agentes.ipynb`** - Avançado: criando agentes inteligentes

## 📖 Estrutura do Projeto

```
azure_frontier_girls_fundamentos_ia/
│
├── 📓 chat.ipynb                  # Notebook 1: Introdução ao Azure OpenAI
├── 📓 criacao_agentes.ipynb       # Notebook 2: Criando Agentes Inteligentes
├── 📄 .env                        # Suas credenciais Azure (não compartilhar!)
├── 📁 .venv/                      # Ambiente virtual Python
└── 📄 README.md                   # Este arquivo
```

## 📓 Notebooks

### 1️⃣ chat.ipynb - Seu Primeiro Chat com IA

**O que você vai aprender:**
- Como se conectar ao Azure OpenAI
- Como fazer sua primeira chamada para um modelo de IA
- Como personalizar as respostas da IA
- Entender os parâmetros básicos (temperature, tokens, etc.)

**Tempo estimado:** 15-20 minutos

**Conceitos-chave:**
- API e Endpoints
- Modelos de linguagem (GPT)
- Roles (system, user, assistant)
- Parâmetros de geração de texto

---

### 2️⃣ criacao_agentes.ipynb - Criando Agentes Inteligentes

**O que você vai aprender:**
- O que são agentes de IA
- Como criar agentes especializados (matemática, viagens, receitas)
- Como dar ferramentas aos agentes (Tools)
- Como criar um orquestrador que gerencia múltiplos agentes

**Tempo estimado:** 40-50 minutos

**Conceitos-chave:**
- Agentes especializados
- Instructions (instruções personalizadas)
- Tools (ferramentas que os agentes podem usar)
- Orquestração de agentes
- Programação assíncrona (async/await)

**Exemplos práticos:**
- ✅ Agente de matemática que explica cálculos
- ✅ Agente de viagens que fala como pirata
- ✅ Agente de receitas que salva arquivos
- ✅ Orquestrador que escolhe o agente certo automaticamente

## 🔑 Como Obter suas Credenciais do Azure

### Passo a Passo Detalhado:

1. **Acesse o Portal Azure**
   - Vá para [portal.azure.com](https://portal.azure.com)
   - Faça login com sua conta

2. **Crie um Recurso Azure OpenAI**
   - Clique em "Create a resource"
   - Busque por "Azure OpenAI"
   - Clique em "Create"
   - Escolha sua assinatura e crie um resource group

3. **Deploy um Modelo**
   - Após criar o recurso, vá em "Model deployments"
   - Clique em "Create new deployment"
   - Escolha um modelo (ex: gpt-4, gpt-35-turbo)
   - Dê um nome ao deployment (ex: "gpt-4.1")

4. **Obtenha suas Credenciais**
   - No recurso Azure OpenAI, vá em "Keys and Endpoint"
   - Copie:
     - `Endpoint` → vai para `AZURE_MODEL_ENDPOINT`
     - `Key` → vai para `AZURE_AI_MODEL_API_KEY`
   - O nome do deployment que você criou → vai para `AZURE_AI_MODEL_DEPLOYMENT_NAME`

5. **Para Azure AI Foundry (opcional para agentes)**
   - Acesse [ai.azure.com](https://ai.azure.com)
   - Crie um projeto
   - Copie o endpoint do projeto → vai para `AZURE_AI_PROJECT_ENDPOINT`

## 🛠️ Troubleshooting (Solucionando Problemas)

### Erro: "git command not found" ou "'git' is not recognized"
**Solução:** 
- Certifique-se de que instalou o Git: [Download Git](https://git-scm.com/downloads)
- Após instalar, **reinicie completamente o VS Code e o terminal**
- Teste executando: `git --version`
- **Alternativa**: Use a Opção B (Download ZIP) se não conseguir instalar o Git

### Erro: "Azure CLI not found" ou "az command not found"
**Solução:** 
- Certifique-se de que instalou o Azure CLI: [Download Azure CLI](https://learn.microsoft.com/cli/azure/install-azure-cli)
- Após instalar, **reinicie o terminal/prompt de comando**
- Teste executando: `az --version`

### Erro: "Please run 'az login' to setup account" ou problemas de autenticação nos notebooks
**Solução:** 
- Execute `az login` no terminal
- Uma janela do navegador vai abrir para você fazer login
- Após fazer login, volte ao terminal e tente novamente
- Isso é **obrigatório** para usar o notebook `criacao_agentes.ipynb`

### Erro: "Module not found"
**Solução:** Certifique-se de que o ambiente virtual está ativado e instale novamente:
```bash
pip install openai azure-ai-projects azure-identity agent-framework python-dotenv
```

### Erro: "Authentication failed"
**Solução:** 
- Verifique se suas credenciais no arquivo `.env` estão corretas
- Certifique-se de não ter espaços extras
- Verifique se a chave API não expirou
- Se estiver usando agentes, certifique-se de ter executado `az login`

### Erro: "Rate limit exceeded"
**Solução:** 
- Você atingiu o limite de chamadas da API
- Aguarde alguns minutos ou verifique sua quota no Portal Azure

### Erro: "Deployment not found"
**Solução:**
- Verifique se o nome do deployment no `.env` está correto
- Verifique se o deployment está ativo no Portal Azure

## 💡 Dicas para Aprender

1. **Execute cada célula em ordem** - Os notebooks são sequenciais
2. **Experimente modificar o código** - Mude as perguntas, as instruções dos agentes
3. **Leia os comentários** - Eles explicam cada linha de código
4. **Teste com suas próprias ideias** - Crie agentes personalizados!
5. **Não tenha medo de errar** - Erros fazem parte do aprendizado

## 📚 Recursos Adicionais

### Documentação Oficial
- [Azure OpenAI Service](https://learn.microsoft.com/azure/ai-services/openai/)
- [Microsoft Agent Framework](https://github.com/microsoft/agent-framework)
- [Azure AI Foundry](https://learn.microsoft.com/azure/ai-studio/)

### Tutoriais e Guias
- [Quickstart Azure OpenAI](https://learn.microsoft.com/azure/ai-services/openai/quickstart)
- [Python para Iniciantes](https://learn.microsoft.com/training/paths/beginner-python/)

### Comunidade
- [Microsoft Learn](https://learn.microsoft.com/)
- [Azure Community](https://techcommunity.microsoft.com/azure)

## 🤝 Como Contribuir

Quer ajudar a melhorar este projeto? Toda contribuição é bem-vinda!

1. Faça um Fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona MinhaFeature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

## ⚠️ Importante - Segurança

- **NUNCA** compartilhe seu arquivo `.env` ou suas chaves API
- **NUNCA** faça commit do `.env` no GitHub
- Use sempre variáveis de ambiente para credenciais
- Se você expôs uma chave acidentalmente, revogue-a imediatamente no Portal Azure

## 🎉 Vamos Começar!

Pronta para começar sua jornada em IA? Abra o notebook `chat.ipynb` e vamos lá! 🚀

Se tiver dúvidas, não hesite em abrir uma issue no GitHub!

**Bom aprendizado! 📚✨**
