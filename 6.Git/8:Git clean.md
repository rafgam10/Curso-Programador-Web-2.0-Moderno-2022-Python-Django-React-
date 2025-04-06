
## 🧹 Limpando o Projeto com `git clean`

### ❓ O que é `git clean`?

O comando `git clean` é usado para **remover arquivos e pastas não rastreados** do seu diretório de trabalho, ou seja, arquivos que:

- Não estão sendo versionados pelo Git (untracked);
- Não foram adicionados com `git add`;
- Não estão listados no `.gitignore`.

> 🧠 Ele **NÃO afeta arquivos versionados** nem arquivos staged.

---

### 📦 Exemplo de situação:

Você está testando algo e criou arquivos temporários como:

```
teste.py
arquivo-temp.txt
```

Ao rodar `git status`, eles aparecem como **untracked**. Se quiser limpá-los do diretório, você pode usar:

```bash
git clean -f
```

---

### 🧪 Sempre teste antes com `-n`

Antes de sair apagando arquivos, veja **o que seria removido**:

```bash
git clean -n
```

Ou:

```bash
git clean --dry-run
```

Isso vai listar os arquivos que seriam deletados, mas **sem remover nada ainda**.

---

### 🔥 Remover diretórios não rastreados

Por padrão, o `git clean` **não remove pastas**, apenas arquivos.

Para limpar também diretórios:

```bash
git clean -fd
```

| Flag | Significado                 |
|------|------------------------------|
| `-f` | Força a limpeza              |
| `-d` | Inclui diretórios            |

---

### 💥 Forçar limpeza geral (com cuidado!)

Quer remover **tudo** que é untracked, incluindo arquivos ignorados?

```bash
git clean -xfd
```

| Flag | Efeito extra                |
|------|-----------------------------|
| `-x` | Remove até arquivos no `.gitignore` |

> ⚠️ **Atenção:** Esse comando apaga **tudo** o que não estiver versionado. Use com muita cautela.

---

### 📌 Resumo rápido

| Ação                              | Comando                       |
|-----------------------------------|-------------------------------|
| Ver o que será removido           | `git clean -n`                |
| Remover arquivos untracked        | `git clean -f`                |
| Remover arquivos **e pastas**     | `git clean -fd`               |
| Remover tudo (incl. ignorados)    | `git clean -xfd`              |

---

### 🛟 Dica: use com sabedoria

`git clean` é poderoso, mas **perigoso**: ele **não envia nada para a lixeira**. Se apagar algo sem querer, só recuperando de um backup.

