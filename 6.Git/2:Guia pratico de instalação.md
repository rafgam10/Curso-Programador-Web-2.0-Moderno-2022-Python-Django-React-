

## 🛠 Guia Prático de Instalação – Git & GitHub

### 📦 1. Instalando o Git

#### 🔵 No **Windows**:

1. Acesse: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. O download inicia automaticamente.
3. Execute o instalador.
4. **Dê "Next" em tudo**, mantendo as opções padrão.
5. Ao finalizar, você pode usar o **Git Bash** para digitar comandos Git.

#### 🟢 No **Linux (Ubuntu/Debian)**:

Abra o terminal e digite:

```bash
sudo apt update
sudo apt install git
```

#### 🟣 No **macOS**:

Use o Homebrew (se não tiver, instale o Homebrew antes):

```bash
brew install git
```

---

### ⚙️ 2. Verificar se o Git foi instalado

Execute no terminal ou Git Bash:

```bash
git --version
```

Se tudo estiver certo, ele mostrará a versão instalada, como:

```
git version 2.42.0
```

---

### 🧑‍💻 3. Configurar o Git pela primeira vez

Digite no terminal:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

Isso define quem é você nos commits.

---

### 🔐 4. Criar e conectar-se ao GitHub

1. Acesse: [https://github.com](https://github.com)
2. Crie sua conta (se ainda não tiver).
3. No canto superior direito, clique em seu avatar > **Settings**.
4. Vá em **Developer Settings > Personal Access Tokens**.
5. Crie um token com permissões de `repo`, `workflow`, etc. (GitHub agora usa token no lugar da senha para comandos `git push`).

---

### 🔁 5. Clonar, adicionar, e enviar um projeto para o GitHub

```bash
# Clonar repositório
git clone https://github.com/seu-usuario/seu-repositorio.git

# Entrar na pasta do projeto
cd seu-repositorio

# Fazer alterações, depois:
git add .
git commit -m "Minha primeira alteração"
git push origin main
```

---

### 🚨 Dica extra: Configurar chave SSH (opcional, mas útil)

```bash
ssh-keygen -t ed25519 -C "seuemail@exemplo.com"
```

Depois, copie a chave gerada e adicione no GitHub (Settings > SSH and GPG Keys).

