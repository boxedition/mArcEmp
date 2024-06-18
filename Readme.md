# SA-GPT

Clone Repository

```
git clone https://github.com/boxedition/mArcEmp
```

## uiPath

Pasta SaveOutlookAttachments

Regra Outlook: https://i.imgur.com/WxQIExz.png

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

> Note:
>
> PaperLess não consegue fazer ocr de pdf encriptados. Existe possíbilidade da causa estar relacionada com assinaturas
>
> https://imgur.com/36VO9Rf

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
