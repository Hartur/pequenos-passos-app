# Pequenos Passos — roadmap e escopo

Este documento organiza a sequência de trabalho e distingue a visão futura do escopo a implementar. A visão completa e as hipóteses do produto estão em [product-spec.md](product-spec.md). Critérios específicos do incremento de notificações ficam em [MVP de notificações e registro rápido](planejamento/mvp-notificacoes-e-registro-rapido.md).

## Princípio de priorização

Construir o MVP incrementalmente, priorizando simplicidade, confiabilidade, privacidade, funcionamento local/offline e validação com usuários reais. A presença de uma ideia na visão do produto não a autoriza para implementação. Antes de cada tarefa, confirme o estágio e os critérios aplicáveis neste roadmap e nos documentos vinculados.

## Sequência de etapas

1. **Refinamento da ideia:** definir público, problema, proposta de valor e diferencial. Resultado: visão e hipóteses prioritárias.
2. **Pesquisa científica aplicada:** organizar estudos, limitações e regras que possam orientar o produto. Resultado: biblioteca inicial fundamentada.
3. **Validação com usuários:** entrevistar potenciais usuários e testar entendimento. Resultado: evidências qualitativas de utilidade e necessidades.
4. **Definição do MVP:** selecionar cadastro, registros, calendário, histórico, progresso e sugestões básicas. Resultado: especificação funcional e critérios de aceitação.
5. **Protótipo visual:** desenhar telas e testar fluxos. Resultado: protótipo navegável.
6. **Preparação técnica:** configurar Kotlin, Compose, Room, navegação e testes. Resultado: projeto executável com persistência local.
7. **Implementação do MVP:** desenvolver cadastro, registro, histórico e recomendações. Resultado: aplicativo funcional offline.
8. **Testes com usuários:** observar frequência, dificuldades e utilidade das sugestões. Resultado: melhorias priorizadas.
9. **Validação comercial:** testar limite gratuito, benefícios premium e disposição para pagar. Resultado: evidências iniciais de monetização.
10. **Sincronização e assinatura:** contas, backend, sincronização e pagamentos somente após validar necessidade e modelo comercial e autorizar essa etapa. Resultado: possível versão premium entre dispositivos.
11. **Publicação e evolução:** publicar, acompanhar retenção e avaliações e evoluir com base em evidências.

## Incremento documentado: notificações e registro rápido (versão 0.4)

O incremento de notificações e registro rápido tem especificação de produto, restrições técnicas e critérios de aceitação próprios. Consulte os três documentos listados no [índice de instruções](../AGENTS.md). O escopo inclui configuração e desativação de lembretes por hábito, ações na notificação, persistência local de cumprimento/não cumprimento, abertura opcional para complementação, adiamento sem registro e proteção contra duplicidade. A aceitação deve seguir a lista completa do documento de planejamento.

O documento de planejamento identifica a funcionalidade como candidata importante para o MVP e prioriza primeiro o fluxo básico de notificação, registro e persistência local. Personalizações avançadas de horários, múltiplas notificações, estatísticas detalhadas e sincronização em nuvem ficam para evolução posterior. Isso não autoriza, por si só, as etapas futuras deste roadmap.

## Fora do escopo inicial sem nova autorização

- Backend, contas, autenticação, nuvem, sincronização e pagamentos.
- Funcionalidades premium, mesmo que constem como hipóteses na visão.
- IA em tempo de execução.
- Personalizações avançadas de lembretes, múltiplas notificações e estatísticas detalhadas.

Esses itens exigem etapa autorizada e critérios próprios antes da implementação. Decisões importantes de produto ou arquitetura ainda indefinidas e difíceis de reverter devem ser apresentadas com alternativas para orientação.
