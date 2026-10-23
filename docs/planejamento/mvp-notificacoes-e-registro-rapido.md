# MVP — Notificações e registro rápido

Este documento define os critérios de aceitação e a ordem de implementação da funcionalidade especificada em [notificações e registro rápido](../produto/notificacoes-e-registro-rapido.md).

## Critérios de aceitação

A funcionalidade será considerada pronta quando:

1. O usuário conseguir configurar e desativar lembretes por hábito.
2. A notificação apresentar as ações de cumprimento, não cumprimento e adiamento.
3. Cumprimento e não cumprimento gerarem registros persistentes sem exigir navegação manual pelo aplicativo.
4. O comportamento de abertura para complementação respeitar a preferência configurada.
5. A tela complementar permitir salvar quantidade, duração e observações opcionais.
6. As informações adicionais ficarem vinculadas ao registro original.
7. Adiar não gerar falsos registros de sucesso ou falha.
8. Toques repetidos não criarem registros duplicados.
9. O histórico distinguir dias sem registro de dias explicitamente marcados como não cumpridos.
10. A funcionalidade permanecer utilizável offline.

## Priorização

Esta funcionalidade é candidata importante para o MVP, pois está diretamente ligada à principal proposta de valor do Pequenos Passos: facilitar a consistência sem transformar o acompanhamento em uma tarefa cansativa.

A implementação deve começar com o fluxo básico de notificação, registro e persistência local. Personalizações avançadas de horários, múltiplas notificações, estatísticas detalhadas e sincronização em nuvem poderão ser desenvolvidas posteriormente, conforme a validação com usuários.
