# Modelo de Dados (Alto Nível)

## Entidades centrais

- **ServerOTConfig**
  - Relaciona servidor Discord a um OT habilitado.
  - Pode conter canais de destino por tipo de painel.

- **WatchPlayers**
  - Lista de personagens monitorados por servidor + OT.

- **WatchGuilds**
  - Lista de guilds monitoradas por servidor + OT.

- **PanelState**
  - Armazena referência da mensagem fixa de cada painel por servidor + OT.

- **DeathsSeen**
  - Registro de eventos já publicados para deduplicação.

## Regras de escopo

Toda unicidade relevante considera o par:

- `discord_guild_id`
- `ot_key`

Isso reduz colisões entre comunidades e garante isolamento de configuração.

## Relacionamentos (conceitual)

- Um servidor pode habilitar múltiplos OTs.
- Cada servidor + OT pode ter múltiplos itens em watchlists.
- Cada servidor + OT possui estado de painéis independentes.

## Observações

- Este documento omite esquema completo de colunas, tipos e constraints internas.
- A modelagem foi simplificada para fins de portfólio.
