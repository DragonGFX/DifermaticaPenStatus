# DifermaticaPenStatus

## pens.json — pens autorizadas
Cada pen regista-se sozinha ao configurares (pedem o nome do técnico).

```json
{
  "whitelist": true,
  "pens": [
    { "penId": "abc...", "nome": "Daniel", "atualizadoEmUtc": "..." }
  ]
}
```

- **Perdeu uma pen:** remove essa entrada de `pens` **ou** mete o `penId` em `revoked.json`
- Com `whitelist: true`, só pens listadas funcionam (com internet)

## revoked.json — bloqueio explícito
Lista de PenIds bloqueados de imediato.
