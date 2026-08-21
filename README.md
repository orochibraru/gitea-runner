# Gitea Runner, my setup

## The runner

```bash
git clone https://github.com/orochibraru/gitea-runner.git
cd gitea-runner
curl -fsSL https://get.docker.com | sh
apt install -y micro
cp .example.env .env
micro .env
```

## Dockcheck

### Install

```bash
curl -fsSL https://raw.githubusercontent.com/mag37/dockcheck/main/dockcheck.sh -o dockcheck.sh
chmod +x dockcheck.sh
./dockcheck.sh
```

### Cron

```bash
0 3 * * 0 /home/user/dockcheck.sh -a -n >> /var/log/dockcheck.log 2>&1
```
