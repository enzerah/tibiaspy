# Exemplos Fictícios (Sem Dados Reais)

## Exemplo: configuração por servidor

```json
{
  "discord_guild_id": "123456789012345678",
  "ot_key": "example_ot",
  "channels": {
    "online": "#painel-online",
    "guilds": "#painel-guilds",
    "deaths": "#painel-deaths"
  }
}
```

## Exemplo: retorno normalizado de players online

```json
[
  {"name": "KnightAlpha", "level": 250, "vocation": "EK"},
  {"name": "DruidBeta", "level": 220, "vocation": "ED"}
]
```

## Exemplo: evento de morte deduplicável

```json
{
  "event_id": "example_ot:KnightAlpha:2026-03-03T17:10:00Z",
  "player": "KnightAlpha",
  "level": 250,
  "killer": "Dragon Lord",
  "timestamp": "2026-03-03T17:10:00Z"
}
```

## Exemplo: render de painel (texto)

```txt
🟢 ONLINE (2)
- KnightAlpha (250 EK)
- DruidBeta (220 ED)

Última atualização: 17:12:10 UTC
```
