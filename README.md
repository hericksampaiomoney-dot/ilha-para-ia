# 🏝️ Ilha Virtual de IA

> Um projeto de ilha virtual em 3D onde um agente de Inteligência Artificial explora o ambiente autonomamente, interage com a fauna e objetos, coleta recursos, fabrica itens e conversa em tempo real com o jogador.

## ✨ Recursos

* **🌐 Mundo 3D Interativo:** Ilha com praia, bosque, montanha, animais e ciclo dinâmico de dia e noite.

* **🤖 IA Autônoma:** Tomada de decisão livre para explorar o ambiente e escolher ações.

* **🎒 Sistema de Crafting:** Gerenciamento de mochila, coleta de itens, receitas e criação de objetos.

* **💬 Interação Social:** Conversação em linguagem natural com a IA e atribuição de tarefas.

* **🗺️ Exploração Guiada:** Inventário de recursos da ilha e rotas até pontos de interesse (como o topo da montanha).

* **⏱️ Controle do Ambiente:** Painel para ajustar o tempo/clima e interagir diretamente com o mundo.

## 🛠️ Requisitos Previos

Certifique-se de ter os seguintes softwares instalados antes de iniciar:

* **Python:** `3.10` ou superior.

* **Ollama:** Instalado e rodando em segundo plano ([Download Ollama](https://ollama.com/)).

* **Modelo LLM:** Modelo `llama3.2` baixado no Ollama.

## 🚀 Como Executar

1. **Baixe o modelo de IA padrão:**

   ```
   ollama pull llama3.2
   
   ```

2. **Inicie o servidor:**

   ```
   python servidor.py
   
   ```

3. **Acesse a aplicação:**
   Abra o seu navegador e acesse: <http://127.0.0.1:5000>

## ⚙️ Configuração

As configurações padrão ficam armazenadas no arquivo `config.json`:

```
{
  "provedor": "ollama",
  "modelo_ollama": "llama3.2",
  "porta": 5000
}

```

> 💡 **Variáveis de Ambiente:** É possível sobrescrever as configurações definindo variáveis no sistema. Exemplo: use `PORTA` para alterar a porta HTTP ou `MODELO_OLLAMA` para trocar o modelo de linguagem utilizado.

## 📦 Gerar Executável (.exe para Windows)

Para compilar o projeto em um executável autônomo:

```
build.bat

```

*O script instalará os pacotes necessários e gerará o arquivo em `dist/IlhaIA.exe`.*

## 📁 Estrutura do Projeto

```
├── servidor.py          # Servidor Flask, lógica de decisões da IA e chat
├── static/
│   ├── index.html       # Interface principal, renderização 3D e lógica do jogo
│   └── three.min.js     # Biblioteca Three.js para gráficos 3D
├── config.json          # Configurações de provedor, modelo e porta
├── requirements.txt     # Dependências Python do projeto
└── build.bat            # Script de automação do build no Windows

```

## 🔌 Rotas da API

| Método | Rota | Descrição | 
| ----- | ----- | ----- | 
| `GET` | `/` | Carrega a interface do jogo. | 
| `GET` | `/status` | Retorna o provedor e modelo atualmente configurados. | 
| `POST` | `/decisao` | Envia o estado atual da ilha e recebe a próxima ação da IA. | 
| `POST` | `/conversar` | Processa e responde mensagens enviadas pelo jogador. | 
