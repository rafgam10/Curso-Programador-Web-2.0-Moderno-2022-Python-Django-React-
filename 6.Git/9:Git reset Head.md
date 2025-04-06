

## 🔄 Usando `git reset HEAD` para Desfazer Alterações

### ❓ O que é `git reset HEAD`?

O comando `git reset HEAD` é usado para **remover arquivos da área de stage (staging area)** — ou seja, ele **desfaz o `git add`**, mas **não apaga as alterações no arquivo**.

> 🧠 É muito útil quando você adicionou arquivos para commit por engano e quer removê-los do stage sem perder o que escreveu.

---

### 👨‍💻 Exemplo prático

Você adicionou vários arquivos com `git add .`, mas quer tirar um deles do stage:

```bash
git reset HEAD arquivo.txt
```

Esse comando:

- Remove `arquivo.txt` da área de stage
- Mantém as modificações feitas no arquivo

---

### 📄 Como visualizar isso?

```bash
git status
```

Antes do reset:
```
Changes to be committed:
  modified:   arquivo.txt
```

Depois do reset:
```
Changes not staged for commit:
  modified:   arquivo.txt
```

---

### 🧹 Desfazendo todo o stage

Para remover **todos os arquivos** da área de staging:

```bash
git reset HEAD
```

Assim, **nenhum arquivo será incluído no próximo commit**, até você usar `git add` novamente.

---

### 🧠 Dica: HEAD significa "onde você está"

No Git, `HEAD` geralmente aponta para o **último commit atual** (normalmente o topo do branch em que você está).  
Quando você faz `git reset HEAD`, está dizendo:  
> “Volte ao estado do último commit, mas **sem perder as alterações feitas**”.

---

### 📌 Resumo rápido

| Ação                                      | Comando                       |
|-------------------------------------------|-------------------------------|
| Remover um arquivo do stage               | `git reset HEAD nome-do-arquivo` |
| Remover todos os arquivos do stage        | `git reset HEAD`             |
| Ver status do stage antes/depois          | `git status`                 |

---

### ⚠️ Importante

- `git reset HEAD` **não apaga código**
- Ele apenas **desfaz o "git add"**
- Ideal para **reorganizar o que vai no próximo commit**

---
