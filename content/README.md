# 🚀 Guia de Instalação e Uso  

Este projeto utiliza **Node-RED** para simular a produção de peças e armazenar os dados em um banco SQLite.  

---

## 📌 Pré-requisitos  

- [Node.js](https://nodejs.org/) instalado na máquina  
- [Node-RED](https://nodered.org/) instalado  

---

## ⚙️ Como Rodar o Projeto  

1. **Baixe e instale o Node-RED** pelo site [https://nodered.org/](https://nodered.org/).  
2. No terminal (CMD, PowerShell ou Terminal Linux), execute:  
   ```sh
   node-red

3. No navegador, acesse a interface do Node-RED pelo endereço: http://127.0.0.1:1880/
4. Importe o fluxo do projeto:

    No Node-RED, clique no menu superior direito (☰) > Import > Selecionar arquivo.

    Escolha o arquivo flows.json localizado na pasta content.

    Confirme a importação clicando em Importar.


5. Como Visualizar os Dados no Banco de Dados SQLite
    Opção 1: Pelo Node-RED (Debug)
    No Node-RED, localize o nó :memory.

6. Adicione um nó Debug na saída desse nó para visualizar os dados processados.

    Clique no botão Inject "Select table" para buscar os dados no banco de dados.

    Os valores aparecerão na aba Debug, no painel direito da tela do Node-RED.

    Opção 2: Acessando o SQLite Manualmente
    Caso queira acessar os dados diretamente pelo banco SQLite, siga estes passos:

7. Instale o SQLite CLI (caso não tenha):

    No Windows, baixe o SQLite CLI em https://www.sqlite.org/download.html.

    No Linux/Mac, instale via terminal:

    sh
    Copiar
    Editar
    sudo apt install sqlite3  # Debian/Ubuntu  
    brew install sqlite       # macOS  
    No terminal, abra o SQLite e carregue o banco de dados do Node-RED:

    sh
    Copiar
    Editar
    sqlite3 database.db
    Para visualizar os dados da tabela, execute:

    sql
    Copiar
    Editar
    SELECT * FROM nome_da_tabela;
    Para sair do SQLite, use:

    sh
    Copiar
    Editar
    .exit

8. Como Acessar o Dashboard
    O projeto inclui um Dashboard para visualização dos dados em tempo real. Para acessá-lo:

    Certifique-se de que o Node-RED está rodando.

    instale a dependência node-red-dashboard

    No navegador, abra o seguinte endereço:

    arduino
    Copiar
    Editar
    http://127.0.0.1:1880/ui/