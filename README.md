# DifermaticaPenStatus

Lista pública de pens **revogadas**. A app consulta este ficheiro com internet (sem token).

## Bloquear uma pen perdida

1. Abre `revoked.json`
2. Acrescenta o `PenId` (está em `Config\pen-id.txt` na pen, ou no ecrã ao arrancar)
3. Commit + push para `main`

Exemplo:

```json
{
  "revoked": [
    "a1b2c3d4e5f6789012345678abcdef01"
  ],
  "message": "Esta pen foi bloqueada remotamente. Contacta a Difermatica."
}
```

Quando a pen tiver internet, a app fecha e deixa de funcionar.
Para reativar: remove o id da lista e apaga `Config\pen-blocked.json` na pen (ou a app limpa sozinha se já não estiver na lista).
