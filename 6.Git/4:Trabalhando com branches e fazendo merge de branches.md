
## 🌿 Trabalhando com Branches e Fazendo Merge

### 🧠 O que são *branches*?

Um **branch** (ramo) é uma linha paralela de desenvolvimento. Ele permite que você trabalhe em **novas funcionalidades**, **correções de bugs** ou **testes**, sem afetar diretamente o código principal (`main` ou `master`).

---

### 📌 Por que usar branches?

- Evita bagunça no código principal.
- Permite testar ideias sem risco.
- Facilita o trabalho em equipe.
- Ajuda a organizar melhor o projeto (ex: `login-feature`, `hotfix-erro404`).

---

## 🛠 Comandos Básicos para Trabalhar com Branches

### ➕ Criar um novo branch

```bash
git branch nome-da-branch
```

### 🔄 Mudar para a branch criada

```bash
git checkout nome-da-branch
```

Ou crie e vá direto:

```bash
git checkout -b nome-da-branch
```

---

### 👀 Ver todas as branches existentes

```bash
git branch
```

A branch atual será marcada com `*`.

---

## 🔃 Fazendo Merge (Unindo alterações)

### 🧩 Exemplo de fluxo completo:

```bash
# Estando na branch 'main'
git checkout -b nova-funcionalidade      # 1. Criar e mudar para nova branch
# (Faça mudanças no código...)
git add .
git commit -m "Adiciona nova funcionalidade"   # 2. Salvar mudanças na nova branch

git checkout main                         # 3. Volta para a branch principal
git pull                                  # 4. Garante que está atualizada
git merge nova-funcionalidade             # 5. Une a branch com as mudanças
```

---

### 💥 Possíveis conflitos

Se você modificou as **mesmas linhas** em `main` e na branch, o Git vai avisar sobre um **conflito**.

**Como resolver:**

1. O Git marca o conflito no arquivo com `<<<<<<<`, `=======`, `>>>>>>>`.
2. Edite o arquivo manualmente para corrigir.
3. Depois:

```bash
git add arquivo-com-conflito
git commit -m "Resolve conflito"
```

---

### 🧹 Apagar uma branch (depois do merge)

```bash
git branch -d nome-da-branch
```

Se quiser forçar a exclusão:

```bash
git branch -D nome-da-branch
```

---

### 💡 Dica de organização com branches

| Tipo de branch       | Nome sugerido         | Uso                         |
|----------------------|------------------------|------------------------------|
| Funcionalidade nova  | `feature/nome`         | Novas funções                |
| Correção de bug      | `hotfix/nome`          | Bugs urgentes                |
| Versão de testes     | `test/nome`            | Testes temporários           |

