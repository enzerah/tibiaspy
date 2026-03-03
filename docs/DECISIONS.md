# Decisões Técnicas

## 1) Bot orientado a loops periódicos

**Decisão**: usar tarefas periódicas para atualização contínua de painéis.

**Motivação**:
- estado sempre recente para comunidades ativas;
- modelo simples de entender e operar.

**Trade-off**:
- maior volume de chamadas externas;
- necessidade de controle de frequência e backoff.

## 2) Providers com contrato único

**Decisão**: padronizar providers em uma interface comum.

**Motivação**:
- adicionar novos OTs com menor acoplamento;
- reaproveitar pipeline de renderização e persistência.

**Trade-off**:
- necessidade de normalização entre fontes heterogêneas.

## 3) Mensagem fixa por painel

**Decisão**: editar sempre a mesma mensagem em vez de postar continuamente.

**Motivação**:
- melhor UX no canal;
- menos spam e histórico mais limpo.

**Trade-off**:
- exige controle de estado de mensagem e tratamento de falhas de edição.

## 4) Persistência de deduplicação

**Decisão**: registrar eventos já publicados (ex.: mortes recentes).

**Motivação**:
- evitar notificações duplicadas;
- manter consistência entre reinicializações.

**Trade-off**:
- crescimento de dados operacionais ao longo do tempo.

## 5) Escopo multi-tenant por guild + OT

**Decisão**: toda configuração e watchlist é contextualizada por servidor e OT.

**Motivação**:
- isolamento lógico por comunidade;
- segurança de configuração e previsibilidade.

**Trade-off**:
- queries mais verbosas e necessidade de índices adequados.
