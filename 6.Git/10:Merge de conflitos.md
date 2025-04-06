

## ⚔️ Merge de Conflitos no Git

### ❓ O que é um conflito de merge?

Um **conflito de merge** acontece quando **duas branches modificam a mesma parte de um arquivo**, e o Git **não sabe qual versão manter**.

Isso exige que **você resolva o conflito manualmente**, escolhendo o que vai permanecer no código final.

---

### 👇 Exemplo de situação

Você está na branch `main` e quer mesclar a branch `feature`:

```bash
git merge feature
```

Se ambos modificaram o mesmo trecho do arquivo, o Git retorna:

```
Auto-merging arquivo.txt
CONFLICT (content): Merge conflict in arquivo.txt
Automatic merge failed; fix conflicts and then commit the result.
```

---

### 🧾 O que aparece no arquivo com conflito?

```txt
<<<<<<< HEAD
Conteúdo da branch atual (ex: main)
=======
Conteúdo da outra branch (ex: feature)
>>>>>>> feature
```

Você deve **editar esse bloco**, decidindo qual conteúdo manter (ou unir os dois de forma lógica).

---

### 🛠️ Como resolver o conflito

1. Abra o arquivo com conflito.
2. Apague as marcas `<<<<<<<`, `=======` e `>>>>>>>`.
3. Mantenha o conteúdo correto.
4. Salve o arquivo.
5. Marque como resolvido:

```bash
git add arquivo.txt
```

6. Finalize o merge com:

```bash
git commit
```

> 💡 Dica: se o conflito veio de um `merge`, o Git já prepara a mensagem de commit automaticamente.

---

### ✅ Exemplo final resolvido

Antes:
```txt
<<<<<<< HEAD
console.log("Olá mundo");
=======
console.log("Hello world");
>>>>>>> feature
```

Depois de resolver:
```js
console.log("Olá, mundo! Hello world!");
```

---

### 🧠 Ferramentas úteis para resolver conflitos

- **VS Code**: destaca visualmente os conflitos e permite resolver com cliques.
- **GitKraken, Meld, Sourcetree**: ferramentas gráficas para merge.
- **`git mergetool`**: abre uma ferramenta de merge se você tiver uma configurada.

---

### 📌 Resumo rápido

| Etapa                        | Comando ou Ação                  |
|-----------------------------|----------------------------------|
| Fazer o merge               | `git merge nome-da-branch`       |
| Ver conflitos               | `git status`                     |
| Editar os arquivos          | Remover as marcações do conflito |
| Marcar como resolvido       | `git add arquivo`                |
| Finalizar o merge           | `git commit`                     |

