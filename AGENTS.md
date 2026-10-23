# Pequenos Passos — instruções para agentes

## Documentação e escopo

- Consulte [a visão e especificação do produto](docs/product-spec.md) para princípios, funcionalidades planejadas, evidências e hipóteses comerciais.
- Consulte [o roadmap](docs/roadmap.md) antes de iniciar uma etapa; implemente somente o escopo autorizado e priorizado para ela.
- Para notificações e registro rápido, siga os documentos específicos: [regras de produto](docs/produto/notificacoes-e-registro-rapido.md), [restrições técnicas](docs/arquitetura/notificacoes-e-persistencia-local.md) e [critérios e priorização do MVP](docs/planejamento/mvp-notificacoes-e-registro-rapido.md).
- As regras de produto definem o comportamento esperado; os documentos de arquitetura definem restrições técnicas; os documentos de planejamento definem escopo e validação. Evite repetir especificações: atualize o documento responsável e mantenha os demais como referências.

## Contexto e objetivo

Pequenos Passos é um aplicativo Android para ajudar pessoas a desenvolver hábitos e habilidades por meio de pequenas ações, acompanhamento consistente e recomendações baseadas em evidências científicas. O MVP deve evoluir incrementalmente, priorizando simplicidade, confiabilidade, privacidade e validação com usuários reais. Não implemente funcionalidades futuras só por estarem previstas na visão.

## Tecnologias e limites

- Kotlin, Jetpack Compose, Room com SQLite, ViewModel, StateFlow e Kotlin Coroutines.
- Android Studio é o ambiente de desenvolvimento previsto.
- Priorize funcionamento offline no MVP e separe interface, regras de negócio e persistência. Mantenha recomendações independentes da interface.
- Prefira soluções simples, testáveis e sem abstrações ou dependências desnecessárias; justifique novas bibliotecas.
- Não introduza backend, autenticação, sincronização em nuvem ou pagamentos sem autorização explícita para a etapa.

## Princípios de produto

- O usuário controla hábitos, metas, lembretes e registros; recomendações são transparentes, compreensíveis e ignoráveis.
- Ausência de registro não significa falha. Interrupções não apagam o progresso anterior.
- Não culpe ou envergonhe o usuário, não trate estimativas científicas como garantias universais e não invente evidências ou referências.

## Processo de implementação

1. Identifique o objetivo, os critérios de aceitação e o escopo autorizado no roadmap.
2. Inspecione a estrutura, os padrões existentes e a documentação relevante antes de alterar código.
3. Para tarefas com várias alterações, proponha um plano curto; implemente apenas o escopo acordado.
4. Ao alterar regras de negócio, escreva ou atualize testes. Execute os testes e verificações pertinentes antes de concluir e nunca afirme que passaram sem executá-los.
5. Atualize a documentação responsável quando o comportamento esperado mudar, sem duplicar especificações.
6. Resuma alterações, validações e limitações. Nunca inclua segredos, tokens ou credenciais no repositório.

Se uma decisão importante de produto ou arquitetura estiver indefinida e for difícil de reverter, apresente alternativas e solicite orientação antes de assumir o compromisso.
