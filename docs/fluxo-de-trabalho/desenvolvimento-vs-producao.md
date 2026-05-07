# Desenvolvimento vs Produção

## O que é desenvolvimento e o que é produção?

**Desenvolvimento** é tudo que usamos enquanto estamos construindo o sistema — testes, rascunhos, documentação interna, configurações da máquina de cada um.

**Produção** é o sistema pronto, funcionando para o usuário final, rodando no servidor.

---

## Como vamos separar os dois ambientes

A equipe vai usar o **GitHub Flow**, que funciona assim:

- A branch **`main`** representa a produção. Só entra código testado e funcionando.
- A branch **`develop`** representa o desenvolvimento. É onde o código novo é criado e testado antes de ir para produção.

Quando uma funcionalidade estiver pronta e testada na branch `develop`, ela é mesclada (merge) na branch `main`.

---

## Arquivos que ficam só no desenvolvimento

Estes arquivos existem no computador da equipe mas **não vão para o servidor de produção:**

| Arquivo / Pasta | Motivo |
|---|---|
| `docs/` | Documentação interna do projeto |
| `.env` | Contém senhas e configurações sensíveis |
| Arquivos de teste | Usados só durante o desenvolvimento |
| Configurações de IDE | Específicas de cada máquina |

---

## Arquivos que vão para produção

Estes são os arquivos que o servidor precisa para o sistema funcionar:

| Arquivo / Pasta | Motivo |
|---|---|
| `src/` | Código principal do sistema (PHP) |
| `.htaccess` | Configuração do servidor Apache |
| `config/` | Configurações do banco de dados (sem senhas) |

---

## Como evitar que arquivos sensíveis sejam publicados

Vamos usar um arquivo chamado **`.gitignore`** na raiz do projeto. Ele diz ao Git quais arquivos devem ser ignorados e nunca enviados ao GitHub.

O `.gitignore` vai conter:

```
.env
/vendor
*.log
.DS_Store
.vscode/
```

---

## Por que escolhemos o GitHub Flow?

O GitHub Flow é simples e funciona bem para equipes pequenas como a nossa (duas pessoas). Ele evita que código quebrado vá para produção porque exige que o código passe pela branch `develop` antes de chegar na `main`.

Essa abordagem foi discutida em aula como uma das formas mais comuns de separar ambiente de desenvolvimento e produção em projetos reais.
