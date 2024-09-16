# PASSO-A-PASSO

Sim, você pode usar o GitHub para compartilhar suas configurações e extensões do Visual Studio Code (VSCode). Aqui está um guia passo a passo sobre como fazer isso:

## 1. Criar um Repositório no GitHub
• Acesse o GitHub e faça login na sua conta.
• Crie um novo repositório:
• Clique no botão "New" ou "Novo" na sua página inicial do GitHub.
• Dê um nome ao repositório (por exemplo, vscode-config).
• Escolha se deseja que o repositório seja público ou privado.
• Clique em "Create repository".
## 2. Exportar Configurações e Extensões
### Localize suas Configurações:

As configurações do VSCode estão geralmente localizadas em:
• Windows: %APPDATA%\Code\User\

• *macOS: ~/Library/Application Support/Code/User/*

• Linux: ~/.config/Code/User/

Copie os Arquivos:
Copie os arquivos settings.json, keybindings.json e qualquer outro arquivo relevante (como snippets) para uma pasta local que você usará para o repositório.

### Listar Extensões Instaladas:
Execute o seguinte comando no terminal para gerar uma lista de extensões:
bash

code --list-extensions > extensions.txt
Adicione os Arquivos ao Repositório:
Coloque os arquivos copiados e o extensions.txt na pasta do repositório que você criou.

## 3. Fazer o Commit e Push para o GitHub
Abra o terminal na pasta do repositório.
Inicialize o repositório Git (se ainda não estiver inicializado):

git init
Adicione os arquivos:

git add .
Faça o commit:

git commit -m "Adicionando configurações do VSCode"
Adicione o repositório remoto:

git remote add origin https://github.com/SEU_USUARIO/vscode-config.git
Envie os arquivos para o GitHub:

git push -u origin master - 

## 4. Importar Configurações em Outro Computador

### Clone o Repositório:
No outro computador, clone o repositório que você criou:

git clone https://github.com/SEU_USUARIO/vscode-config.git

Copie os Arquivos para a Pasta de Configurações do VSCode:
Copie os arquivos do repositório clonado para a pasta de configurações do VSCode, conforme mencionado anteriormente.

Instalar Extensões:
No terminal, navegue até a pasta do repositório clonado e execute:

*cat extensions.txt | xargs -L 1 code --install-extension*

### Conclusão
Usando o GitHub, você pode facilmente compartilhar e versionar suas configurações e extensões do VSCode. Isso permite que você mantenha um histórico de alterações e facilite a colaboração com outras pessoas, se necessário.