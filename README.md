# 📋 Lista de Presença e Gestão de Eventos

Uma aplicação web desenvolvida para facilitar o controle de entrada e confirmação de convidados em eventos da igreja. O sistema permite validação em tempo real, pesquisa por grupos (G.A.) e geração de relatórios.

## ✨ Funcionalidades

* **Sincronização em Tempo Real:** Utiliza o Google Firebase. Vários recepcionistas podem usar ao mesmo tempo em celulares diferentes e a lista atualiza instantaneamente para todos.
* **Sistema de Abas:**
    * **Convidados:** Lista de quem ainda não chegou.
    * **Presentes Confirmados:** Lista de quem já foi validado.
* **Pesquisa Poderosa:** Permite filtrar convidados pelo **Nome**, pelo **Membro Responsável** ou pelo **G.A. (Grupo de Assistência)**.
* **Cadastro Rápido:** Possibilidade de adicionar novas pessoas na hora do evento (estas já entram automaticamente na lista de confirmados).
* **Exportação Profissional:** Gera um relatório final em **Excel (.xlsx)** com as colunas organizadas, sem erros de formatação.
* **Interface Responsiva:** Funciona perfeitamente em computadores e celulares.

## 🛠️ Tecnologias Utilizadas

* **Frontend:** HTML5, CSS3, JavaScript.
* **Backend (Banco de Dados):** Firebase Realtime Database (Google).
* **Bibliotecas:**
    * `SheetJS` (xlsx): Para geração do arquivo Excel.
    * `Firebase SDK`: Para conexão com o banco de dados.

## 🚀 Como Configurar o Projeto

### 1. Configuração do Banco de Dados (Firebase)
1.  Crie um projeto no [Firebase Console](https://console.firebase.google.com/).
2.  No menu lateral, escolha **Build** > **Realtime Database** e crie um banco.
3.  Na aba **Regras (Rules)**, defina a leitura e escrita como `true` para permitir o funcionamento do app.
4.  Vá nas configurações do projeto (⚙️) e copie as chaves de acesso (`firebaseConfig`).

### 2. Configuração do Código
1.  Abra o arquivo `index.html`.
2.  Localize a variável `const firebaseConfig`.
3.  Substitua os valores existentes pelas chaves do seu próprio projeto Firebase.

### 3. Importando uma Lista de Convidados (Planilha)
Para começar o evento com a lista cheia:
1.  Tenha sua planilha com as colunas: `nome`, `responsavel`, `telefone`, `ga`.
2.  Use um conversor online de **CSV para JSON**.
3.  No Firebase, crie um nó (pasta) chamado `convidados`.
4.  Clique nos três pontos ao lado de `convidados` > **Importar JSON**.

## 📱 Como Usar

1.  Acesse o link do projeto (hospedado no GitHub Pages).
2.  **Para confirmar alguém:** Vá na aba "Convidados", pesquise o nome e clique no botão verde **(✔)**.
3.  **Para desfazer:** Se marcou errado, vá na aba "Presentes Confirmados" e clique no botão vermelho **(↩️)**.
4.  **Para ver totais:** Observe os contadores no topo das abas (ex: `Convidados (45)`).
5.  **Ao final do evento:** Clique no botão verde **"Baixar Excel"** na aba de confirmados para ter o relatório completo.

---
*Desenvolvido para auxiliar na organização e excelência dos eventos.*
