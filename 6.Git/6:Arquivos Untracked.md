
## 🗂️ Arquivos *Untracked* no Git

### ❓ O que são arquivos "untracked"?

No Git, um arquivo **untracked** é um **arquivo novo**, que está no seu diretório de trabalho mas **ainda não foi adicionado ao controle de versão**.

> Em outras palavras: o Git **vê** o arquivo, mas **ainda não está rastreando** ele.

---

### 🔍 Como identificar arquivos untracked?

Execute:

```bash
git status
```

Você verá algo assim:

```
Untracked files:
  (use "git add <file>..." to include in what will be committed)
    novo-arquivo.txt
```

Isso significa que `novo-arquivo.txt` **não está sendo versionado** ainda.

---

### ✅ Como começar a rastrear (trackear) um arquivo?

Use o comando:

```bash
git add novo-arquivo.txt
```

Depois disso, o arquivo sai da categoria de "untracked" e passa a ser **"staged"** (pronto para commit).

Você pode também adicionar todos os arquivos novos de uma vez:

```bash
git add .
```

---

### 🧽 Ignorar arquivos *untracked* com `.gitignore`

Se você **não quiser rastrear certos arquivos**, como:

- Arquivos temporários
- Logs
- Pastas `node_modules` ou `venv`

Adicione esses nomes ao arquivo `.gitignore`.

Exemplo:

```
*.log
node_modules/
.env
```

Assim, o Git nem vai listar esses arquivos como *untracked*.

---

### 🧨 Cuidado ao limpar arquivos *untracked*

Se quiser **remover todos os arquivos untracked** do seu projeto (⚠️ isso é irreversível!), use:

```bash
git clean -f
```

Ou para ver o que seria apagado antes:

```bash
git clean -n
```

---

### 📌 Resumo rápido

| Situação                      | Significado                                | Ação recomendada           |
|------------------------------|---------------------------------------------|-----------------------------|
| `Untracked file`             | O Git viu o arquivo, mas não o versiona     | Use `git add arquivo`       |
| Quer ignorar um arquivo      | Git não deve rastrear nunca                 | Use `.gitignore`            |
| Quer apagar arquivos untracked | Limpar o diretório de arquivos soltos       | Use `git clean -f` (com cuidado) |

---
