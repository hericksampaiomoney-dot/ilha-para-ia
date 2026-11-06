# 🏝️ IlhaIA - Aplicação Desktop

**IlhaIA** é uma aplicação desktop desenvolvida para oferecer uma experiência interativa e integrada com inteligência artificial, contando com uma interface de usuário moderna e um sistema de configuração centralizado.

---

## 🛠️ Requisitos e Dependências

Para que a aplicação funcione corretamente, certifique-se de atender aos seguintes requisitos:

1. **Ollama (Obrigatório):**
   * O **IlhaIA** depende do [Ollama](https://ollama.com/) rodando localmente para gerenciar e executar os modelos de linguagem.
   * Certifique-se de ter o Ollama instalado e o serviço ativo na sua máquina (geralmente rodando em segundo plano na porta padrão `http://localhost:11434`).

2. **Modelo Utilizado:**
   * O projeto está configurado para utilizar o modelo **`llama3`** (ou o modelo especificado no arquivo de configuração).
   * Certifique-se de baixar o modelo previamente no seu Ollama executando o comando no terminal:
     ```bash
     ollama pull llama3
     ```

---

## 📁 Estrutura do Projeto

A estrutura de arquivos do projeto é organizada da seguinte forma:

```text
IlhaIA-v1.0/
├── IlhaIA.exe       # Executável principal da aplicação
├── config.json      # Arquivo de configurações do sistema (inclui parâmetros do modelo)
└── ux/              # Recursos e componentes da interface do usuário (UI/UX)
```

---

## 🚀 Como Executar

1. **Verifique o Ollama:** Inicie o aplicativo Ollama no seu sistema para garantir que a API esteja acessível.
2. **Download / Extração:** Certifique-se de que todos os arquivos (`IlhaIA.exe`, `config.json` e a pasta `ux/`) estejam no mesmo diretório.
3. **Iniciando o Programa:** Dê um duplo clique no arquivo `IlhaIA.exe` para iniciar a aplicação.

---

## ⚙️ Configuração (`config.json`)

O arquivo `config.json` permite personalizar parâmetros do aplicativo, como o modelo de IA utilizado e o endereço do servidor Ollama. 

Exemplo de estrutura de configuração:

```json
{
  "app_name": "IlhaIA",
  "version": "1.0",
  "theme": "dark",
  "ai_settings": {
    "model": "llama3",
    "ollama_url": "http://localhost:11434"
  },
  "settings": {
    "auto_update": true,
    "log_level": "info"
  }
}
```

> **Nota:** Certifique-se de manter a sintaxe JSON válida ao editar este arquivo.

---

## 🎨 Interface e Recursos (`ux/`)

A pasta `ux/` contém os arquivos essenciais para a renderização da interface do usuário, incluindo:
* Arquivos de estilo e temas.
* Elementos gráficos e ícones.
* Scripts de componentes de interface.

---

## 💻 Requisitos de Sistema

* **Sistema Operacional:** Windows 10/11 (64-bit)
* **Hardware:** Processador compatível e memória RAM adequada para rodar o modelo localmente (recomendado 8GB+ RAM).
* **Permissões:** Permissão de leitura/escrita no diretório onde o arquivo `config.json` está localizado.

---

## 📄 Licença

Este projeto é disponibilizado sob os termos da licença padrão do projeto. Consulte os detalhes no repositório oficial ou entre em contato com os desenvolvedores.

## 🔒 Privacidade

**Onde ficam seus dados:** o IlhaIA roda localmente no seu computador.
As conversas são processadas pelo Ollama em `localhost:11434` e não são
enviadas a servidores do desenvolvedor nem de terceiros.

**O que é gravado em disco:** com `"log_level": "info"` no `config.json`,
o aplicativo pode registrar eventos de uso em arquivos locais. Para não
guardar nada, ajuste o nível de log para o mínimo.

**Atualizações:** com `"auto_update": true`, o app consulta a rede para
buscar novas versões. Para desativar, mude para `false`.

**Seus direitos:** como os dados ficam só na sua máquina, você tem
controle total e pode apagar os arquivos de log quando quiser.
