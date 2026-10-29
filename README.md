
---

# Painel-osintbr-monitor-

Ferramenta para **Termux** e **Kali/Debian**: coleta perfis/sites, salva versões e compara mudanças (ex.: bio alterada).

**Repositório:**  
https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-

---

### O que faz
- **GitHub (estável):** nome, bio, foto, seguidores, repos, empresa, local, atualização do perfil  
- **Página / URL:** título, description, imagem, e-mails, métricas se expuser  
- **Username:** testa @ em várias redes  
- **Monitor:** salva alvos, recheca e mostra o que mudou  

> Instagram / TikTok / X podem bloquear leitura automática. Prefira GitHub ou sites públicos.

---

### Instalação — Termux

```bash
pkg update -y

pkg install python git unzip -y

cd ~

git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-.git

cd Painel-osintbr-monitor-

# extrair o ZIP do projeto

unzip -o painel-osintbr-monitor.zip -d .
cd painel-osintbr-monitor

pip install -r requirements.txt

python main.py
```

Se o nome do ZIP for outro:

```bash
cd ~/Painel-osintbr-monitor-
ls *.zip
unzip -o NOME_DO_ZIP.zip -d .
find . -name "main.py"
cd pasta/que/aparecer
pip install -r requirements.txt
python main.py
```

---

### Instalação — Kali / Debian

```bash
sudo apt update
sudo apt install -y python3 python3-pip python3-venv git unzip

cd ~
git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-.git
cd Painel-osintbr-monitor-

unzip -o painel-osintbr-monitor.zip -d .
cd painel-osintbr-monitor

python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python main.py
```

---

### Uso rápido
```text
1  →  Coletar GitHub (@usuario)
2  →  Coletar URL pública
3  →  Checar username
4  →  Listar alvos
5  →  Rechecagem (compara mudanças)
0  →  Sair
```

Dados em: `data/targets.json`

---

### Atualizar

```bash
cd ~/Painel-osintbr-monitor-
git pull
# se o ZIP foi atualizado no repo:
unzip -o painel-osintbr-monitor.zip -d .
cd painel-osintbr-monitor
pip install -r requirements.txt
python main.py
```

---

### Aviso
Uso em **fontes abertas** e alvos **autorizados**. Não contorna login, CAPTCHA nem contas privadas.

**Link:** https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-