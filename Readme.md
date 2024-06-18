# SA-GPT

Clone Repository

```
git clone https://github.com/boxedition/mArcEmp
```

## uiPath

Pasta SaveOutlookAttachments

## Setup

Pull Images:

```
docker compose pull
```

Criar conta para o Paperless:

```
###
# No ambiente de teste foi utilizado:
# utilizador: paperless
# password: paperless
###

docker compose run --rm paperless createsuperuser
```

Inicializar Solução:

```
docker compose up -d
```

Reboot after files changed:

```
###
# Reboot required after paperless generate files
# Due to vecturial database locks
###

docker compose restart privategpt
```
