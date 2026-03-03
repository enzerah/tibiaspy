# Arquitetura (Visão Geral)

## Propósito

O sistema monitora eventos de servidores OT e publica painéis automatizados em servidores Discord, com atualização contínua e persistência de estado.

## Componentes principais

- **Bot Discord**: recebe comandos administrativos, mantém loops de atualização e publica painéis.
- **Providers de dados**: adaptadores que coletam dados externos e retornam um formato padronizado.
- **Camada de persistência**: guarda configurações por servidor, watchlists e estado de painéis.
- **Módulo de painéis**: garante mensagem fixa por painel e atualizações seguras (incluindo truncamento).
- **Dashboard/automação operacional** (quando habilitado): apoio para manutenção, deploy e observabilidade.

## Fluxo fim a fim

1. Administrador habilita um OT para o servidor Discord.
2. Administrador configura canais por tipo de painel (ex.: online, guilds, deaths).
3. Loops periódicos consultam providers.
4. Dados são normalizados e comparados com o estado anterior.
5. Painéis são editados em mensagens fixas no Discord.
6. Estado e deduplicação são salvos para evitar repetição de eventos.

## Princípios de design

- **Escopo por servidor + OT** para isolamento multi-tenant.
- **Atualizações idempotentes** para reduzir ruído.
- **Resiliência operacional** com fallback e logs úteis.
- **Extensibilidade** via interface de provider.

## Limites desta documentação pública

Esta visão é intencionalmente de alto nível e omite detalhes de implementação, seletores de scraping, credenciais e código de produção.
