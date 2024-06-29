<!-- LOGOTIPO DO PROJETO -->
<div style="display: flex; justify-content: center;">
   <a href="https://github.com/edendenis/git">
     <img src="figures/gold_edf_technology_logo_transparent_background_and_gold_name.png" alt="Logo" width="160" height="160">
   </a>
</div>

<h3 align="center">Configurar/Instalar/Usar o `Token de Acesso Pessoal (PAT)` no `Linux Ubuntu`</h3>

<!-- <div style="display: flex; justify-content: center;">
  <a href="https://zenodo.org/doi/10.5281/zenodo.10668919">
    <img src="https://zenodo.org/badge/758237447.svg" alt="DOI">
  </a>
</div> -->

<p align="center">
 Neste documento estão contidos os principais comandos para configurar/instalar/usar o `Git`.
 <br />
 <a href="https://github.com/edendenis/git"><strong>Explore os documentos »</strong></a>
 <br />
 <br />
 <a href="https://github.com/edendenis/git">Ver demonstração</a>
 ·
 <a href="https://github.com/edendenis/git">Relatar bug</a>
 ·
 <a href="https://github.com/edendenis/git">Solicitar recurso</a>
</p>


# Configurar/Instalar/Usar o `Token de Acesso Pessoal (PAT)` e descrição dos seus principais comandos

## Resumo

Neste documento estão contidos os principais comandos para configurar/instalar/usar o `Token de Acesso Pessoal (PAT)`.

## _Abstract_

_This document contains the main commands for configuring/installing/using the `Personal Access Token (PAT)`._


## Descrição [2]

### `Token de Acesso Pessoal (Personal Access Token, PAT)`

Um `Token de Acesso Pessoal (PAT)` é uma forma de autenticação utilizada em sistemas e serviços online para conceder acesso seguro a recursos específicos. Ele geralmente é composto por uma sequência única de caracteres ou números, que pode ser gerada automaticamente ou definida pelo usuário. Esses tokens são usados em conjunto com o nome de usuário e senha para verificar a identidade do usuário e autorizar o acesso a informações ou funcionalidades restritas. Eles são especialmente úteis em ambientes onde a segurança é uma prioridade, oferecendo uma camada adicional de proteção além das credenciais tradicionais.

Para resolver o problema de autenticação ao usar o git push no `GitHub`, você precisa usar um `Token de Acesso Pessoal (PAT)` em vez de sua senha. A autenticação por senha foi desativada em agosto de 2021. Aqui estão os passos para gerar um `Token de Acesso Pessoal (PAT)` e configurá-lo no `Git`:

### Gerar um `Token de Acesso Pessoal (PAT)` (opção 1)

### Passo 1: Gerar um `Token de Acesso Pessoal (PAT)`

1. **Acesse o `GitHub`**: Vá para `GitHub` e faça login na sua conta.

2. **Navegue até Configurações**: Clique no ícone do seu perfil no canto superior direito e selecione `"Settings"`.

3. **Acesse os Tokens**:

    3.1 No menu à esquerda, clique em `"Developer settings"`.

    3.2 Em seguida, clique em `"Personal access tokens"` e depois em `"Tokens (classic)"`.

4. **Gerar Novo Token**:

    4.1 Clique em `"Generate new token"`.

    4.2 Adicione uma nota para o token, selecione as permissões necessárias (pelo menos "repo" para acesso aos repositórios) e defina a validade do token.

    4.3 Clique em `"Generate token"` no final da página.

5. **Copiar o Token**: Copie o token gerado e guarde-o em um local seguro. Você não poderá vê-lo novamente.

### Passo 2: Configurar o Git para Usar o Token

1. **Atualizar o URL do Repositório**:

    1.1 No terminal, navegue até o diretório do seu repositório local.

    1.2 Atualize o URL remoto para incluir seu token de acesso pessoal: `git remote set-url origin https://<TOKEN>@github.com/edendenis/<nome_do_repositorio_git>.git`

    Substitua `<TOKEN>` pelo token que você gerou.

2. **Executar o `Git Push`**: Agora, você deve conseguir executar o git push sem problemas: `git push`


### Alternativa: Usar Git Credential Manager (opção 2)

Outra alternativa é usar o Git Credential Manager, que gerencia as credenciais de forma segura:

1. **Baixar a Versão Correta do `Git Credential Manager`**: Vamos encontrar o link correto para baixar a versão mais recente do `Git Credential Manager` para `Linux`. Baixar o `Git Credential Manager` `wget https://github.com/git-ecosystem/git-credential-manager/releases/download/v2.0.935/gcm-linux_amd64.2.0.935.deb -O gcm.deb`

2. **Instalar o `Git Credential Manager`**: Instalar o Pacote: `sudo dpkg -i gcm.deb`

3. **Configurar o Git Credential Manager**: Execute o comando: `git config --global credential.helper manager-core`


#### Usar `GitHub CLI` (opção 3)

Outra abordagem é usar a `GitHub CLI (gh)`, que facilita a autenticação e a interação com o `GitHub`. Aqui estão os passos:

1. **Instalar `GitHub CLI`**: `sudo apt install gh`

2. **Autenticar com `GitHub CLI`**: `gh auth login`

<!-- LICENÇA -->
## Licença

Distribuído sob a licença MIT. Consulte `LICENSE.txt` para obter mais informações.

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>

<!-- ROTEIRO -->
## Roteiro

- [x] Adicionar registro de alterações
- [x] Adicionar links de volta ao topo
- [x] Adicionar modelos adicionais com exemplos
- [x] Suporte multilíngue
     - [ ] Espanhol
     - [ ] Inglês
     - [ ] Português
     - [x] Português brasileiro 

Consulte os [problemas abertos](https://github.com/edendenis/google_chrome/issues) para obter uma lista completa dos recursos propostos (e problemas conhecidos).

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>


<!-- CONTRIBUIÇÔES -->
## Contribuições

As contribuições são o que tornam a comunidade de código aberto um lugar incrível para aprender, inspirar e criar. Qualquer contribuição que você fizer será **muito apreciada**.

Se você tiver uma sugestão que possa melhorar isso, bifurque o repositório e crie uma solicitação `pull`. Você também pode simplesmente abrir um problema com a tag “aprimoramento”.
Não se esqueça de dar uma estrela ao projeto! Obrigado novamente!

1. Bifurque o projeto
2. Crie sua ramificação de recursos (`git checkout -b feature/AmazingFeature`)
3. Confirme suas alterações (`git commit -m 'Add some AmazingFeature'`)
4. Envie para a filial (`git push origin feature/AmazingFeature`)
5. Abra uma solicitação pull

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>


<!-- ACKNOWLEDGMENTS -->
## Agradecimentos

* [Best README Template](https://github.com/othneildrew/Best-README-Template?tab=readme-ov-file)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">voltar ao topo</a>)</p>


## Referências

[1] OPEN AI. ***Authenticate git with pat.*** Disponível em: <hhttps://chatgpt.com/c/4a850364-d648-4f2b-b135-76adfac65ba3> (texto adaptado). ChatGPT. Acessado em: 03/08/2023 09:09.

[2] OPENAI. ***Vs code: editor popular.*** Disponível em: <https://chat.openai.com/c/b640a25d-f8e3-4922-8a3b-ed74a2657e42> (texto adaptado). ChatGPT. Acessado em: 22/12/2023 11:36.

