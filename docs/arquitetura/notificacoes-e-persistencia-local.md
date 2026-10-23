# Notificações e persistência local

Este documento registra os requisitos e as restrições técnicas da funcionalidade descrita em [notificações e registro rápido](../produto/notificacoes-e-registro-rapido.md).

## Considerações técnicas para o MVP

A funcionalidade será implementada no aplicativo Android nativo, utilizando Kotlin e Jetpack Compose.

Os principais componentes serão:

- **Agendamento de lembretes:** utilizar os mecanismos de agendamento de trabalho do Android adequados à precisão necessária, respeitando restrições de bateria e execução em segundo plano.
- **Notificações com ações:** disponibilizar as ações de cumprimento, não cumprimento e adiamento.
- **Persistência local:** armazenar registros e estados dos lembretes com Room e SQLite.
- **Navegação contextual:** abrir diretamente o hábito e o registro correspondente quando o usuário optar por adicionar detalhes.
- **Idempotência:** impedir que uma ação repetida gere registros duplicados.
- **Permissões:** tratar a autorização para notificações e explicar ao usuário quando elas estiverem desativadas.

A implementação deverá considerar as restrições do Android para notificações, inicialização após reinicialização do aparelho, adiamento e possíveis limitações de precisão do agendamento. Não se deve prometer pontualidade absoluta em todos os dispositivos.
