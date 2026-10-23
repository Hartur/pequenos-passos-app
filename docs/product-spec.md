# Pequenos Passos — visão e especificação do produto

**Versão de referência:** 0.3, planejamento consolidado  
**Plataforma inicial:** Android  
**Tecnologias previstas:** Kotlin, Jetpack Compose e Room  
**Modelo comercial proposto:** freemium, com plano gratuito local e possível assinatura premium com sincronização em nuvem.

Este documento descreve a visão, princípios, funcionalidades planejadas, fundamentação e hipóteses do produto. O escopo autorizado para cada etapa está em [roadmap.md](roadmap.md). A especificação detalhada de notificações da versão 0.4 está em [notificações e registro rápido](produto/notificacoes-e-registro-rapido.md), com requisitos técnicos em [notificações e persistência local](arquitetura/notificacoes-e-persistencia-local.md) e critérios em [MVP de notificações](planejamento/mvp-notificacoes-e-registro-rapido.md).

## 1. Visão e proposta de valor

Pequenos Passos ajuda pessoas a começar pequeno, visualizar seu progresso e continuar evoluindo, mesmo quando a rotina não é perfeita. O usuário escolhe livremente o comportamento ou habilidade, define uma meta e acompanha sua evolução. O aplicativo ajuda a transformar objetivos abstratos em ações concretas, acompanhar a execução e sugerir próximos passos com base no histórico.

Os pilares são autonomia (o usuário escolhe hábitos e objetivos), simplicidade (registro com pouco esforço), orientação (sugestões informadas por pesquisas) e progresso visível (histórico, gráficos e marcos). O aplicativo não determina quais hábitos a pessoa deve ter. Exemplos incluem leitura, exercício, estudo, concentração, meditação, sono, idiomas, instrumentos, atividades pessoais e outros comportamentos escolhidos pelo usuário.

## 2. Princípios do produto

- O usuário pode cadastrar qualquer hábito; exemplos ajudam, mas não formam uma lista restritiva.
- Incentivar metas iniciais realistas e progressão gradual, sem impor aumentos.
- Distinguir realizado, parcialmente realizado, não realizado e sem registro. A falta de registro não equivale a falha confirmada.
- Interrupções não apagam o progresso. O produto pode apoiar a retomada, por exemplo sugerindo uma meta temporariamente menor ou mudança de contexto.
- Marcos e gamificação mostram acompanhamento, sem alegar que certa quantidade de dias forma um hábito ou certa quantidade de horas comprova expertise.
- Privacidade e autonomia: o usuário controla dados, lembretes e metas. Não usar mensagens culpabilizadoras nem penalizar pausas.

## 3. Fundamentação científica e implicações

Repetição, automaticidade e desenvolvimento de habilidade são conceitos relacionados, mas distintos. O produto deve comunicar essa distinção e apresentar evidências como referências, não como garantias individuais.

### Formação de hábitos

A revisão sistemática e meta-análise *Time to Form a Habit: A Systematic Review and Meta-Analysis of Health Behaviour Habit Formation and Its Determinants* (2024) reuniu 20 estudos e 2.601 participantes. Em quatro estudos, as medianas variaram de 59 a 66 dias, as médias de 106 a 154 dias e houve grande variabilidade individual. Implicações: não prometer prazo universal e permitir acompanhamento prolongado. Fontes: [PubMed](https://pubmed.ncbi.nlm.nih.gov/39685110/) e [texto completo no PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC11641623/).

Lally et al. (2010), em *How are habits formed: Modelling habit formation in the real world*, estimaram entre 18 e 254 dias para atingir 95% do nível assintótico de automaticidade entre participantes cujo modelo pôde ser ajustado. Uma oportunidade perdida não prejudicou materialmente a formação naquele contexto experimental. Implicações: apoiar contextos estáveis, evitar penalidades por falhas isoladas e facilitar retomadas. [DOI](https://doi.org/10.1002/ejsp.674).

### Habilidades e prática

Ericsson, Krampe e Tesch-Römer (1993), em *The Role of Deliberate Practice in the Acquisition of Expert Performance*, investigaram prática estruturada e direcionada à melhoria. A regra popular das 10.000 horas não é um prazo universal para expertise: domínio, qualidade da prática, feedback e diferenças individuais importam. Macnamara, Hambrick e Oswald (2014) encontraram diferenças relevantes entre domínios na proporção da variação de desempenho explicada pela prática deliberada. Implicações: registrar tempo de prática e metas pessoais, distinguindo prática acumulada de competência demonstrada. Fontes: [Ericsson et al.](https://doi.org/10.1037/0033-295X.100.3.363) e [Macnamara et al.](https://doi.org/10.1177/0956797614535810).

Não há prazo universal bem estabelecido após o qual um hábito necessariamente desapareça. O produto pode registrar interrupções e apoiar retomadas, mas não deve usar contagem regressiva para prever perda de hábito ou habilidade.

Revisões de intervenções digitais identificam automonitoramento, definição de metas, lembretes, feedback e personalização entre técnicas de mudança de comportamento. Isso orienta o produto, sem garantir resultados de uma implementação específica. Fontes: [JMIR (2024)](https://www.jmir.org/2024/1/e54375) e [Annals of Behavioral Medicine](https://academic.oup.com/abm/article/57/10/817/7251346).

## 4. Funcionalidades previstas

### Hábitos e registros

O cadastro poderá incluir nome, descrição, categoria opcional, frequência, meta inicial, unidade, contexto ou horário preferencial, data de início e lembretes opcionais. O registro poderá indicar realizado, realizado parcialmente ou não realizado, com possibilidade de corrigir registros anteriores. Ausência de registro permanece distinta de falha.

### Histórico e progresso

Calendário e histórico permitem consultar registros, padrões, interrupções e mudanças de metas. O painel poderá apresentar frequência, percentual nos dias elegíveis e registrados (com critérios transparentes), tempo de prática, evolução de metas, marcos e retomadas.

### Próximos passos e orientações

Um motor determinístico poderá sugerir manter a meta, aumentá-la gradualmente, reduzi-la temporariamente, rever horário/contexto, retomar por uma ação menor ou aguardar mais registros. Recomendações devem ser opcionais, justificadas e independentes da interface.

A biblioteca poderá abordar metas realistas, repetição em contextos estáveis, prática deliberada, planejamento de obstáculos, retomada e progressão gradual. Incluir fontes quando aplicável e explicitar limitações.

### Lembretes e gamificação

Lembretes locais ficam sob controle do usuário. Os fluxos e critérios da funcionalidade nova estão especificados exclusivamente no [documento de notificações](produto/notificacoes-e-registro-rapido.md).

Gamificação poderá incluir marcos de consistência, calendário, gráficos, tempo de prática, progresso até metas, reconhecimento de retomadas e histórico de evolução. Marcos como 30 ou 60 dias são objetivos de acompanhamento, não prazos científicos universais. Metas de prática como 10, 50, 100 ou 500 horas não representam níveis comprovados de expertise.

## 5. Monetização proposta e hipóteses

O modelo proposto é freemium: versão gratuita útil e local; premium para valor adicional concreto, especialmente continuidade entre dispositivos.

### Gratuito

Possíveis recursos: um hábito ativo, armazenamento local, registros diários, calendário e histórico, progresso básico, sugestões iniciais baseadas em regras, biblioteca básica, lembretes locais e uso offline. O limite de um hábito é hipótese a validar e pode ser restritivo. Sem conta ou nuvem, os dados não terão sincronização nem backup remoto automático; a interface deverá explicar isso e orientar sobre troca de aparelho e reinstalação.

### Premium futuro

Possíveis recursos: múltiplos hábitos, sincronização em nuvem, conta, uso em vários dispositivos, backup/restauração e histórico sincronizado. Relatórios avançados e jornadas guiadas são possibilidades posteriores. O diferencial deve ser a continuidade, sem retirar do gratuito o essencial para ser útil.

A sincronização pode justificar assinatura por resolver continuidade e exigir operação recorrente, mas demanda autenticação, controle de acesso, resolução de conflitos, segurança e tratamento de falhas. A primeira versão é local; nuvem depende da validação da proposta.

Assinaturas mensal e anual são opções a avaliar; preços não estão definidos. R$ 7,90–12,90 por mês e anual equivalente a aproximadamente 8–10 mensalidades são apenas hipóteses de pesquisa, não preços definidos ou aceitos. Validar disposição para pagar, taxas de lojas e pagamentos, impostos, infraestrutura, armazenamento, suporte, aquisição, cancelamento e margem sustentável. Desconto anual deve preservar margem.

## 6. Direção técnica e dados conceituais

A implementação Android prevista usa Kotlin e Jetpack Compose; Room/SQLite para dados locais; ViewModel, StateFlow e corrotinas para estado e trabalho assíncrono. Backend Java/Spring Boot, contas, pagamentos e sincronização são possibilidades futuras, condicionadas à necessidade comercial e autorização do roadmap. Não é necessária IA em tempo de execução no MVP. IA poderá apoiar pesquisa/síntese, sempre com revisão das fontes originais.

Estruturas conceituais previstas (a refinar durante desenvolvimento):

- **Habit:** id, nome, descrição, categoria, unidade, meta, frequência, contexto, início e arquivamento.
- **HabitLog:** id, hábito, data, status, quantidade realizada, duração e observação.
- **HabitGoalHistory:** histórico de metas e vigências.
- **Strategy:** orientações e referências.
- **RecommendationRule:** regras de recomendação.
- **Milestone:** marcos pessoais e conquistas.
- **PracticeSession:** sessões e duração.
- **UserAccount** e **SyncMetadata:** conceitos futuros para conta e sincronização.

Uma futura sincronização deve prever autenticação segura, identidade de registros, sincronização incremental, concorrência e conflitos, modo offline, exclusão de conta e dados, proteção em trânsito e repouso e recuperação de falhas, preservando histórico e evitando duplicações.

## 7. Métricas e responsabilidade

Métricas a acompanhar: ativação (cadastro e primeiro registro), retenção, frequência de registro, utilidade percebida das recomendações, retomada após interrupções, marcos, conversão para premium, cancelamentos, receita recorrente, custo de infraestrutura por pagante e margem após taxas, impostos e custos. Métricas devem distinguir falta de registro de abandono confirmado.

Coletar somente o necessário; permitir consultar e excluir registros; não compartilhar sem consentimento; proteger dados sincronizados; explicar limitações das recomendações; não transformar estimativas em garantias; e deixar metas e notificações sob controle do usuário. A nuvem futura exige política clara, segurança e procedimentos aplicáveis de exclusão e exportação. O plano local reduz transmissão de dados.

## 8. Diretrizes estabelecidas e hipóteses

Diretrizes estabelecidas: Android inicial; Kotlin e Compose; hábitos escolhidos pelo usuário; registro e histórico simples; progresso visual; recomendações transparentes baseadas em regras; conteúdo informado por pesquisa; primeira versão local.

Hipóteses ainda a validar: limite de um hábito no gratuito; múltiplos hábitos e sincronização premium; periodicidade e preços; relatórios avançados ou jornadas guiadas; necessidade de backend/autenticação; política final de backup e migração. Não tratar essas hipóteses como autorização de implementação.
