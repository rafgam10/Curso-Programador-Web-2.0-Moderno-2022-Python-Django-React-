
## ✏️ Corrigindo Commits com `git commit --amend`

### ❓ O que é `--amend`?

O comando `git commit --amend` permite **editar o último commit feito**, seja para **corrigir a mensagem**, **adicionar arquivos esquecidos**, ou **substituir o commit por um novo**.

É muito útil para **pequenos ajustes**, **antes de enviar o commit ao repositório remoto**.

---

### 📄 1. Corrigir a mensagem do último commit

```bash
git commit --amend
```

Esse comando abre o editor de texto do Git (como o Vim), permitindo **editar a mensagem** do commit anterior.

💡 Para editar a mensagem de forma direta (sem abrir editor):

```bash
git commit --amend -m "Nova mensagem do commit"
```

---

### 🧩 2. Adicionar arquivos esquecidos no commit

Imagine que você cometeu um arquivo, mas esqueceu de incluir outro:

```bash
git add arquivo-esquecido.txt
git commit --amend --no-edit
```

> O `--no-edit` mantém a **mensagem do commit anterior**, apenas atualizando os arquivos.

---

### ⚠️ Importante: cuidado se já fez `git push`

Se você já fez `git push` antes de usar `--amend`, o Git verá isso como um **commit novo** (porque o hash mudou).

Nesse caso, para atualizar o commit no repositório remoto, será necessário forçar o push:

```bash
git push origin nome-da-branch --force
```

> ⚠️ *Use com cuidado! `--force` pode sobrescrever commits de outras pessoas se estiverem no mesmo branch.*

---

### 📌 Resumo prático

| Situação                               | Comando                                       |
|----------------------------------------|-----------------------------------------------|
| Editar a mensagem do último commit     | `git commit --amend -m "Nova mensagem"`       |
| Adicionar arquivo esquecido ao commit | `git add arquivo && git commit --amend`       |
| Alterar arquivos, manter mensagem      | `git commit --amend --no-edit`                |
| Atualizar repositório remoto (com cuidado) | `git push --force`                         |

---

Essa ferramenta ajuda a manter o **histórico limpo e organizado**, evitando vários commits seguidos como:

```
Ex:
        "ajuste"
        "corrigindo erro"
        "agora vai"
```

