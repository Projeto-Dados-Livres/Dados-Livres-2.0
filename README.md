<div align="center">

<img src="dadoslivres-logo.png" alt="Logo do Dados Livres" width="180" />

# Dados Livres

### Dados abertos só têm valor quando as pessoas conseguem encontrá-los e usá-los.

**Uma plataforma livre e colaborativa para catalogar fontes de dados abertos e aplicações cívicas.**

[![Licença: GPL v3](https://img.shields.io/badge/Licen%C3%A7a-GPLv3-blue.svg)](https://gitlab.com/dados-livres/dados-livres/-/blob/master/LICENSE)
[![Python](https://img.shields.io/badge/Python-3-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-Microframework-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?logo=docker&logoColor=white)](https://docs.docker.com/compose/)
[![Telegram](https://img.shields.io/badge/Telegram-Comunidade-26A5E4?logo=telegram&logoColor=white)](https://t.me/dadoslivres)
[![PRs bem-vindos](https://img.shields.io/badge/PRs-bem--vindos-brightgreen.svg)](#-como-contribuir)

[🌐 **Acessar a plataforma**](https://dadoslivres.org/) ·
[📖 Sobre o projeto](https://dadoslivres.org/about) ·
[🤝 Como contribuir](https://dadoslivres.org/how_to_contribute) ·
[💬 Entrar na comunidade](https://t.me/dadoslivres)

</div>

---

## 💡 Por que o Dados Livres existe?

Governos e organizações publicam cada vez mais dados abertos. O problema é que eles ficam **espalhados**, **difíceis de achar** e **desconectados** de quem realmente os usa na prática.

O **Dados Livres** resolve isso reunindo tudo em um só lugar:

- 🗂️ **Fontes de dados abertos**: de onde os dados vêm.
- 🧩 **Aplicações cívicas**: o que as pessoas já constroem com esses dados.
- 🔗 **A ligação entre os dois**: cada fonte mostra as aplicações que a utilizam, e cada aplicação mostra as fontes que ela consome.

Tudo isso feito **de forma colaborativa**, por qualquer pessoa, **sem precisar escrever uma linha de código**.

> 🌍 O projeto está alinhado às diretrizes da ONU, com foco nos **ODS 10** (Redução das Desigualdades) e **ODS 16** (Paz, Justiça e Instituições Eficazes), facilitando o **controle social** e a difusão dos dados abertos para os mais diversos fins.

---

## ✨ O que torna o Dados Livres diferente

| | |
|---|---|
| 🖱️ **Cadastro sem código** | Qualquer pessoa registra fontes e aplicações por formulário, sem conhecimento técnico. |
| 🔄 **Fontes ↔ Aplicações conectadas** | Navegue de uma fonte para os projetos que a usam, e vice-versa, direto no perfil. |
| 🤝 **Curadoria coletiva** | O catálogo cresce com a contribuição da comunidade. |
| 🆓 **Software livre de verdade** | Código aberto sob GPLv3, sem fins lucrativos. |
| 🐳 **Fácil de rodar** | Suba o projeto local com `docker compose up` ou com um ambiente Python simples. |

### 🔭 No horizonte

- [ ] Cadastro de **artigos científicos** que utilizam dados abertos
- [ ] Cadastro de **notícias** baseadas em dados abertos

Quer ajudar a tirar algum desses itens do papel? Veja o [quadro de issues](https://gitlab.com/dados-livres/dados-livres/-/boards).

---

## 🚀 Comece em 2 minutos

### Opção 1: Docker Compose (mais rápido)

Pré-requisito: [Docker e o plugin docker compose](https://docs.docker.com/engine/install/).

```sh
git clone https://github.com/Projeto-Dados-Livres/Dados-Livres.git
cd Dados-Livres
docker compose up -d
```

Pronto! Acesse **http://localhost:5000** 🎉

Para acompanhar os logs (encerre com `CTRL+C`):

```sh
docker compose logs --follow
```

### Opção 2: Ambiente Python local

Pré-requisitos: [Git](https://git-scm.com/downloads), [Python 3](https://www.python.org/downloads/) e [Pip](https://pip.pypa.io/en/stable/installation/).

```sh
# 1. Clone o repositório (idealmente, o seu fork)
git clone https://github.com/Projeto-Dados-Livres/Dados-Livres.git
cd Dados-Livres

# 2. Crie e ative o ambiente virtual (veja o seu sistema abaixo)
python3 -m venv venv

# 3. Instale as dependências
pip install -r requirements.txt

# 4. Configure o banco de dados local
flask db upgrade

# 5. Rode a aplicação
flask run
```

Acesse **http://localhost:5000** no navegador.

<details>
<summary><b>🐧 Linux</b></summary>

```sh
python3 -m venv venv
source venv/bin/activate
```

> Em distribuições derivadas de Debian/Ubuntu, se o sistema pedir o pacote **python3-venv**, rode `sudo apt-get install python3-venv` e repita o comando `python3 -m venv venv`.

</details>

<details>
<summary><b>🍎 macOS</b></summary>

```sh
pip install virtualenv
python3 -m venv venv
source venv/bin/activate
```

</details>

<details>
<summary><b>🪟 Windows</b></summary>

```sh
pip install virtualenv
python3 -m venv venv
venv\Scripts\activate
```

</details>

---

## 🤝 Como contribuir

Toda ajuda é bem-vinda, e **você não precisa programar para contribuir**.

### 📌 Sem código: ajude a construir o catálogo

1. [Crie sua conta](https://dadoslivres.org/auth/register_request) (ou faça [login](https://dadoslivres.org/auth/login)).
2. Cadastre uma [**fonte de dados abertos**](https://dadoslivres.org/register_source) ou uma [**aplicação cívica**](https://dadoslivres.org/register_software).
3. Conhece alguém que faz projetos com dados abertos? Divulgue!

### 💻 Com código: melhore a plataforma

Novas funcionalidades, correções e ideias são feitas aqui, no [repositório do Dados Livres](https://gitlab.com/dados-livres/dados-livres). Para começar:

1. **Faça um fork** do projeto e clone o seu fork (veja [Comece em 2 minutos](#-comece-em-2-minutos)).
2. **Crie uma branch** para a sua alteração:
   ```sh
   git checkout -b nome_da_branch
   ```
3. **Adicione e salve** suas mudanças:
   ```sh
   git add nome_do_arquivo
   git commit -m "descreva o que você editou ou criou"
   ```
4. **Envie** para o GitLab:
   ```sh
   git push --set-upstream origin nome_da_branch
   ```
   Ou, se estiver trabalhando pelo GitHub:
   ```sh
   git push origin nome_da_branch
   ```
5. **Abra um Merge Request** (GitLab) ou **Pull Request** (GitHub) descrevendo sua contribuição.

### 🧭 Por onde começar?

- 📋 [Quadro de issues](https://gitlab.com/dados-livres/dados-livres/-/boards): ideias e tarefas abertas
- 📖 [Guia de contribuição na plataforma](https://dadoslivres.org/how_to_contribute)
- 💬 [Comunidade no Telegram](https://t.me/dadoslivres): tire dúvidas e conheça outras pessoas contribuindo

---

## 🛠️ Tecnologias

| Camada | Tecnologias |
|---|---|
| **Back-end** | Python + Flask |
| **Front-end** | HTML, CSS, JavaScript e Bootstrap |
| **Infra** | Docker Compose |

---

## 🌱 História

O Dados Livres nasceu em **2018**, como um projeto de pesquisa no **Instituto Federal de Educação, Ciência e Tecnologia do Rio Grande do Norte (IFRN)**. Hoje é mantido e foi fundado por:

<table>
  <tr>
    <td align="center">
      <a href="https://gitlab.com/mariacarolinass">
        <b>Carolina Soares</b>
      </a><br />
      <a href="https://mariacarolinass.github.io/carolinasoares/">Site</a> ·
      <a href="https://t.me/carolsoaresm">Telegram</a>
    </td>
    <td align="center">
      <a href="https://gitlab.com/pbaesse">
        <b>Pedro Baesse</b>
      </a><br />
      <a href="https://pbaesse.me/">Site</a> ·
      <a href="https://t.me/pbaesse">Telegram</a>
    </td>
  </tr>
</table>

---

## 📣 Fale com a gente

- 💬 **Comunidade:** [t.me/dadoslivres](https://t.me/dadoslivres)
- ✉️ **Mantenedores:** [mcarolinasoares0@gmail.com](mailto:mcarolinasoares0@gmail.com) · [pbaesse@gmail.com](mailto:pbaesse@gmail.com)

**Redes sociais:**
[LinkedIn](https://www.linkedin.com/company/dados-livres/) ·
[YouTube](https://www.youtube.com/channel/UCo1LRnYUpCXejZAckGvWmGA) ·
[Instagram](https://www.instagram.com/dadoslivres/) ·
[Twitter](https://twitter.com/dadoslivres) ·
[Facebook](https://www.facebook.com/dadoslivres)

---

## 📄 Licença

Distribuído sob a [Licença GPL-3.0](https://gitlab.com/dados-livres/dados-livres/-/blob/master/LICENSE). Isso significa que você pode usar, estudar, modificar e compartilhar o código, desde que mantenha a mesma liberdade para quem vier depois.

<div align="center">

**Se o Dados Livres é útil para você, deixe uma ⭐ no repositório e compartilhe com quem trabalha com dados abertos!**

</div>
