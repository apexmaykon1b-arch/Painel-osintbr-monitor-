# Painel-osintbr-monitor-
Essa ferramenta compatível com termux e kali/Debian coleta informações de perfils/sites a cada um horário e salva antes e depois, o perfil investigado mudou a bio? A ferramenta percebe e coleta a alteração 

---

### 🔍 Painel OSINTBR Monitor

CLI para **Termux** e **Kali**: coleta de perfis públicos, comparação de mudanças e checagem de username.  
Interface **verde e amarela**, fácil de usar.

**Repositório:**  
https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-

---

### O que faz
- **GitHub (estável):** nome, bio, foto, seguidores, repos, empresa, local, data de atualização do perfil  
- **Página / URL:** título, description, imagem, e-mails, métricas se a página expuser  
- **Username:** testa @ em várias redes  
- **Monitor:** salva alvos, recheca e mostra o que mudou  

> Instagram / TikTok / X podem bloquear leitura automática. Para monitoramento estável, prefira GitHub ou sites públicos.

---

### Instalação — Termux

```bash
pkg update -y
pkg install python git -y
termux-setup-storage

cd ~
git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-.git
cd Painel-osintbr-monitor-

pip install -r requirements.txt
python main.py
```

Se a pasta vier com subpasta:

```bash
cd ~/Painel-osintbr-monitor-
ls
# se aparecer painel-osintbr-monitor:
cd painel-osintbr-monitor
pip install -r requirements.txt
python main.py
```

---

### Instalação — Kali / Debian

```bash
sudo apt update
sudo apt install -y python3 python3-pip python3-venv git

git clone https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-.git
cd Painel-osintbr-monitor-

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
4  →  Listar alvos salvos
5  →  Rechecagem (compara mudanças)
0  →  Sair
```

Dados salvos em: `data/targets.json`

---

### Atualizar depois

```bash
cd ~/Painel-osintbr-monitor-
git pull
pip install -r requirements.txt
python main.py
```

---

### Aviso
Uso apenas em **fontes abertas** e alvos com **autorização**. Não contorna login, CAPTCHA nem contas privadas.

---

**Link:** https://github.com/apexmaykon1b-arch/Painel-osintbr-monitor-
