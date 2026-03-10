# TibiaSpy — Portfolio (Public Documentation)

Este repositório é uma **versão pública e documental** do projeto TibiaSpy.

> Objetivo: apresentar arquitetura, decisões técnicas, fluxos operacionais e boas práticas sem expor código-fonte proprietário, segredos ou dados sensíveis.

## O que você vai encontrar

- Visão geral do sistema e componentes
- Fluxo de dados fim a fim
- Modelagem de dados (alto nível)
- Estratégia operacional e monitoramento
- Segurança, privacidade e limites do escopo público
- Roadmap e lições aprendidas

## Stack técnico (resumo)

- **Linguagem e runtime:** Python 3.10+
- **Bot e comandos Discord:** Nextcord (slash commands e loops assíncronos)
- **Persistência:** SQLAlchemy ORM com SQLite em desenvolvimento e PostgreSQL em produção
- **Dashboard e APIs internas:** Flask
- **Coleta de dados:** providers de scraping por OT, com contrato padronizado para facilitar expansão
- **Operação e deploy:** Docker Compose, systemd e automações de manutenção
- **Qualidade e segurança:** Pytest, validações de configuração e hardening documentado

### Impacto prático da stack

- **Escalabilidade por contexto:** isolamento por servidor Discord e OT para suportar múltiplos ambientes sem conflito.
- **Evolução incremental:** arquitetura por providers permite adicionar novos OTs sem refatorar o núcleo.
- **Confiabilidade operacional:** painéis fixos e atualização idempotente reduzem ruído e inconsistência de estado.
- **Manutenção simplificada:** SQLAlchemy e documentação operacional diminuem risco em mudanças e deploys.

## O que não está incluído

- Código-fonte do bot/dashboard
- Credenciais, tokens, IDs reais
- Endpoints privados, regras anti-abuso internas
- Dados de clientes, servidores ou jogadores reais

## Estrutura

- `docs/ARCHITECTURE.md` — arquitetura e fluxo principal
- `docs/DECISIONS.md` — decisões técnicas e trade-offs
- `docs/DATA_MODEL.md` — entidades e relacionamentos
- `docs/OPERATION.md` — operação, deploy e troubleshooting
- `docs/ROADMAP.md` — evolução planejada
- `docs/FAQ.md` — perguntas comuns
- `docs/EXAMPLES.md` — exemplos fictícios de entrada/saída
- `docs/DIAGRAMS.md` — diagramas Mermaid

## Como usar este material

1. Comece por `docs/ARCHITECTURE.md`.
2. Consulte `docs/DECISIONS.md` para contexto de design.
3. Use `docs/DIAGRAMS.md` para leitura rápida em apresentações.

## Licença do conteúdo

Este repositório documenta um sistema real de forma resumida e sanitizada.
Você pode adaptar o formato para estudos e portfólio, respeitando propriedade intelectual e confidencialidade.

---

Se você é recrutador(a) ou tech lead e quiser uma walkthrough técnica, use esta documentação como base para discussão de arquitetura e operação em produção.
