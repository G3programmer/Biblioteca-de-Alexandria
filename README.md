# 🏛️ Biblioteca de Alexandria

<p align="center">
  <img src="https://img.shields.io/badge/PHP-8.1%2B-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP Version">
  <img src="https://img.shields.io/badge/Environment-CLI-black?style=for-the-badge&logo=gnumetallurgicallaboratory&logoColor=white" alt="CLI">
  <img src="https://img.shields.io/badge/Database-JSON-000000?style=for-the-badge&logo=json&logoColor=white" alt="JSON">
</p>

<p align="center">
  <b>⚡ Um sistema clássico de gerenciamento de acervos feito para o terminal moderno ⚡</b>
</p>

---

O **Biblioteca de Alexandria** é um sistema de gerenciamento de acervos literários desenvolvido inteiramente em **PHP puro (CLI)**. O objetivo principal deste projeto foi consolidar conceitos de lógica estruturada, manipulação de arquivos e, principalmente, explorar o design de código modularizado e a **experiência do usuário (UX) aplicada ao terminal**.

O nome é uma homenagem à famosa biblioteca, trazendo uma estética clássica para um utilitário moderno de linha de comando.

---

## 🎯 Objetivos de Aprendizado e Foco do Projeto

* **Manipulação de CRUD Completo:** Criação, leitura, atualização e deleção de dados persistidos localmente.
* **PHP Puro e Funcional:** Divisão de responsabilidades estruturada através de funções especialistas e isoladas.
* **UX de Terminal (Interface no Console):** Preocupação com a usabilidade, menus limpos, telas que se auto-limpam (`cleaner.php`) e feedbacks claros para o usuário após cada ação.
* **Persistência Híbrida:** Uso de **Arrays Associativos** nativos do PHP para manipulação em memória e conversão para **JSON** (`livros.json`) para salvar os dados no disco.

---

## 🛠️ Ferramentas e Requisitos

### Versões do PHP Aceitáveis
* **Recomendado:** PHP 8.1, 8.2 ou superior.
* **Mínimo Aceitável:** PHP 7.4 (versões anteriores podem não ter suporte total a algumas funções nativas de manipulação de tipos ou JSON CLI de forma idêntica).

### Ferramentas Utilizadas
* **PHP (Ambiente CLI):** Utilizado como linguagem de programação pura para processamento lógico, captura de dados do teclado (`fgets(STDIN)`) e renderização da interface do menu.
* **JSON (JavaScript Object Notation):** Utilizado como nossa tecnologia de banco de dados leve (NoSQL baseado em arquivos). Ele garante a interoperabilidade dos dados brutos em texto estruturado.

---

## 📂 Estrutura Modular

A organização das pastas reflete a separação de responsabilidades do sistema:

```text
├── index.php         # Menu interativo principal (Loop de interface e UX)
├── process.php       # Controlador que gerencia o fluxo de dados e requisições
├── livros.json       # Base de dados em formato JSON
└── functions/        # Funções especialistas que tornam o código modular:
    ├── cleaner.php   # Controle de UX (Limpeza de tela e formatação do terminal)
    ├── create.php    # Lógica de inserção de novos registros no array
    ├── edit.php      # Edição e atualização de livros existentes
    ├── list.php      # Listagem visual estruturada do acervo
    ├── remove.php    # Exclusão de registros do sistema
    ├── save.php      # Conversão do Array Associativo PHP -> JSON e escrita em arquivo
    ├── search.php    # Sistema de busca e filtros dentro do array
    └── stats.php     # Painel de métricas (Contagem de livros, categorias, etc.)

    ⚙️ Como Instalar o PHP (Tutorial Passo a Passo)
Para rodar este projeto, você precisará apenas do interpretador do PHP configurado globalmente no seu sistema operacional.

🪟 No Windows (Prompt de Comando / CMD / PowerShell)
Baixar o PHP:
Acesse o site oficial: https://windows.php.net/download/
Procure pela versão mais recente estável (ex: PHP 8.2 ou 8.3) e baixe a opção VS16 x64 Non Thread Safe (arquivo Zip).

Extrair os Arquivos:
Crie uma pasta chamada php diretamente no seu Disco Local C (Ficará no caminho C:\php).
Extrair todo o conteúdo do arquivo .zip baixado dentro dessa pasta C:\php.

Configurar as Variáveis de Ambiente:
No menu iniciar do Windows, pesquise por "Editar as variáveis de ambiente do sistema" e abra-o.
Clique no botão Variáveis de Ambiente... (na parte inferior da janela).
Na seção Variáveis do Sistema, procure pela variável chamada Path e dê um clique duplo nela.
Clique no botão Novo no canto direito e digite exatamente o caminho da sua pasta: C:\php.
Clique em OK em todas as janelas para fechar e salvar as alterações.

Validar a Instalação:
Abra um novo Prompt de Comando (CMD) e digite:

DOS
php -v
Se aparecer a versão do PHP na tela, a configuração foi feita com sucesso!

🐧 No Linux (Ubuntu / Debian / WSL)
Instalar o PHP no Linux é direto através do gerenciador de pacotes apt:

Abra o seu terminal e atualize os índices de pacotes locais:

Bash
sudo apt update
Instale o interpretador CLI do PHP e o módulo de manipulação de JSON rodando:

Bash
sudo apt install php-cli php-json -y
Valide se a instalação ocorreu com sucesso checando a versão:

Bash
php -v
🚀 Como Baixar e Executar o Projeto
Com o PHP devidamente instalado em sua máquina, siga os passos abaixo:

Abra o terminal na pasta onde deseja salvar o projeto e clone este repositório:

Bash
git clone [https://github.com/G3programmer/code-academy-3C.git](https://github.com/G3programmer/code-academy-3C.git)
Entre na pasta correspondente ao projeto:

Bash
cd "Code Academy"
Inicie a aplicação executando o arquivo principal:

Bash
php index.php