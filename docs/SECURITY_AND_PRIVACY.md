# Segurança e Privacidade (Versão Pública)

## Objetivo

Definir o que pode ser compartilhado em portfólio técnico sem expor ativos sensíveis do sistema real.

## O que pode ser público

- Arquitetura em alto nível
- Decisões técnicas e trade-offs
- Fluxos operacionais genéricos
- Diagramas e exemplos fictícios

## O que deve permanecer privado

- Tokens, segredos e chaves
- IDs reais de guild, canais e usuários
- Selectors/regras completas de scraping
- Estratégias anti-bot/anti-bloqueio
- Logs brutos contendo dados identificáveis

## Checklist de redaction

- [ ] Remover valores reais de `.env`
- [ ] Sanitizar prints/logs
- [ ] Trocar nomes reais por placeholders
- [ ] Validar links para não expor ambientes internos
- [ ] Revisar histórico git antes de publicar

## Responsabilidade

Este material não substitui revisão jurídica/compliance quando aplicável. O foco aqui é compartilhamento técnico seguro para fins de portfólio.
