
## 🔁 Workflow Básico com Git & GitHub

Esse **workflow** (fluxo de trabalho) mostra os **passos mais comuns** usados por desenvolvedores no dia a dia ao usar Git com GitHub.

---

### 🧩 1. Clonar ou iniciar um repositório

#### 👉 Clonar um repositório existente (do GitHub):
```bash
git clone https://github.com/seu-usuario/seu-projeto.git
cd seu-projeto
```

#### 👉 Criar um repositório novo (do zero):
```bash
mkdir meu-projeto
cd meu-projeto
git init
```

---

### ✍️ 2. Fazer alterações no projeto

Edite arquivos, adicione funcionalidades ou corrija bugs. Após isso, salve os arquivos.

---

### ✅ 3. Verificar status dos arquivos

```bash
git status
```

Você verá quais arquivos foram modificados ou adicionados.

---

### 📥 4. Adicionar arquivos para staging

```bash
git add nome-do-arquivo

# ou adicionar todos:
git add .
```

---

### 💾 5. Fazer um commit

```bash
git commit -m "Descrição breve da mudança"
```

Um **commit** registra suas alterações no histórico do projeto.

---

### 🚀 6. Enviar (push) para o GitHub

```bash
git push origin main
```

**`origin`** é o nome do repositório remoto (normalmente GitHub),  
**`main`** é o nome do branch principal (às vezes pode ser `master`).

---

### 🔄 7. Puxar (pull) alterações de outras pessoas

Antes de começar a trabalhar, é bom garantir que está com a versão mais recente:

```bash
git pull origin main
```

---

### 🔃 Fluxo resumido

```bash
git clone <url>      # 1. Clonar projeto
git pull             # 2. Pegar últimas alterações
...                  # 3. Fazer mudanças nos arquivos
git status           # 4. Verificar alterações
git add .            # 5. Preparar arquivos para commit
git commit -m "..."  # 6. Salvar alterações localmente
git push             # 7. Enviar para o GitHub
```

---

### 💡 Extras (bons hábitos)

- Faça commits com mensagens claras e objetivas.
- Sempre dê `git pull` antes de `git push` para evitar conflitos.
- Trabalhe com **branches** para testar novas funcionalidades.

