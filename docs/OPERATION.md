# Operação e Confiabilidade

## Rotina operacional

- Iniciar serviço do bot com variáveis de ambiente válidas.
- Confirmar sincronização de comandos no Discord.
- Validar se canais de painéis estão configurados por servidor + OT.
- Acompanhar logs dos loops de atualização.

## Sinais de saúde

- Atualização periódica de mensagens fixas.
- Ausência de erros repetitivos de provider.
- Baixa taxa de retriable errors em rede.
- Latência de atualização dentro da janela esperada.

## Troubleshooting (alto nível)

### Painel não atualiza

- Verificar se OT está habilitado para o servidor.
- Confirmar canais configurados para o tipo de painel.
- Checar disponibilidade da fonte externa de dados.

### Duplicidade de eventos

- Validar persistência e consulta de deduplicação.
- Revisar chave de idempotência do evento.

### Falha ao subir serviço

- Checar variáveis obrigatórias no ambiente.
- Revisar permissões do bot no servidor Discord.
- Confirmar conectividade com banco de dados.

## Práticas recomendadas

- Alertas para falhas consecutivas de provider.
- Backup periódico do banco.
- Deploy com rollback planejado.
- Mudanças de scraping testadas em ambiente de validação.
