Pequenos Passos

Documento de visão do produto, especificação funcional, fundamentação científica, arquitetura e monetização

Versão: 0.3 — Planejamento consolidado
Plataforma inicial: Android
Tecnologias principais: Kotlin, Jetpack Compose e Room
Modelo comercial proposto: freemium, com plano gratuito local e assinatura premium com sincronização em nuvem
Objetivo: ajudar pessoas a desenvolver hábitos e habilidades de forma progressiva, acompanhar sua evolução e retomar suas atividades após interrupções, utilizando orientações baseadas em evidências científicas.

---

1. Visão geral

O Pequenos Passos será um aplicativo de acompanhamento de hábitos e evolução pessoal. O usuário poderá escolher livremente o comportamento ou a habilidade que deseja desenvolver, definir uma meta inicial e acompanhar sua evolução ao longo do tempo.

O aplicativo não pretende determinar quais hábitos a pessoa deve ter. Sua função será ajudar o usuário a transformar objetivos abstratos em ações concretas, acompanhar sua execução e sugerir próximos passos de acordo com o histórico registrado.

A proposta combina quatro elementos:

1. Autonomia: o usuário escolhe o hábito e define seus objetivos.
2. Simplicidade: o registro diário deve exigir o mínimo de esforço.
3. Orientação: o aplicativo oferece sugestões fundamentadas em pesquisas sobre hábitos e aprendizagem.
4. Progresso visível: calendários, gráficos e marcos tornam a evolução mais fácil de perceber.

A monetização deverá seguir a mesma filosofia de simplicidade: oferecer uma versão gratuita realmente útil e cobrar por recursos adicionais que proporcionem valor concreto, especialmente sincronização e continuidade entre dispositivos.

1.1. Exemplos de objetivos

- Ler regularmente.
- Praticar exercícios físicos.
- Estudar ou desenvolver habilidades profissionais.
- Melhorar a concentração.
- Meditar ou reservar momentos para relaxamento.
- Desenvolver uma rotina de sono.
- Aprender um idioma.
- Praticar um instrumento musical.
- Dedicar mais tempo a atividades pessoais.
- Desenvolver qualquer outro comportamento escolhido pelo usuário.

1.2. Proposta de valor

Ajudar o usuário a começar pequeno, visualizar seu progresso e continuar evoluindo, mesmo quando sua rotina não é perfeita.

O aplicativo deverá priorizar simplicidade, autonomia, consistência e transparência.

---

2. Princípios do produto

2.1. O usuário escolhe o hábito

O usuário poderá cadastrar qualquer hábito ou atividade.

O sistema poderá oferecer exemplos e sugestões de configuração, mas não deverá restringir o uso a uma lista fechada de comportamentos.

2.2. Começar pequeno

O aplicativo incentivará a definição de uma primeira meta realista.

Exemplo:

- Objetivo: ler mais.
- Meta inicial: ler duas páginas por dia.
- Contexto escolhido: depois do café da manhã.
- Evolução possível: aumentar gradualmente a quantidade de leitura quando o usuário considerar apropriado.

2.3. Registro simples

O registro diário deverá ser rápido. O usuário poderá informar se realizou a atividade, se realizou parcialmente ou se não conseguiu realizá-la.

A ausência de registro deverá ser diferente de uma falha confirmada.

2.4. Retomar sem recomeçar do zero

Uma interrupção não deverá apagar o progresso anterior.

O aplicativo poderá sugerir uma meta temporariamente menor, uma mudança de contexto ou uma retomada gradual.

2.5. Gamificação sem falsas promessas

O usuário poderá visualizar níveis, marcos e progresso acumulado.

O aplicativo não deverá afirmar que uma pessoa formou um hábito ou se tornou especialista simplesmente porque completou determinado número de dias ou horas.

2.6. Privacidade e autonomia

O aplicativo deverá permitir que o usuário controle seus dados, seus lembretes e suas metas. A monetização não deverá depender de mensagens culpabilizadoras ou de mecanismos que penalizem pausas.

---

3. Fundamentação científica

O produto deverá utilizar pesquisas sobre formação de hábitos, prática deliberada e mudança de comportamento como fundamento para suas funcionalidades.

É importante distinguir:

- Repetição: quantas vezes a pessoa realizou a atividade.
- Automaticidade: quanto o comportamento passa a ocorrer de forma relativamente automática em determinado contexto.
- Desenvolvimento de habilidade: como o desempenho evolui por meio da prática, do feedback e de outros fatores.

Esses conceitos estão relacionados, mas não são equivalentes.

3.1. Tempo para formação de hábitos

A revisão sistemática e meta-análise Time to Form a Habit: A Systematic Review and Meta-Analysis of Health Behaviour Habit Formation and Its Determinants (2024) reuniu 20 estudos e 2.601 participantes.

As medianas reportadas em quatro estudos variaram de 59 a 66 dias, enquanto as médias variaram de 106 a 154 dias. As estimativas individuais apresentaram grande variabilidade.

Fontes:

- "PubMed" (https://pubmed.ncbi.nlm.nih.gov/39685110/)
- "Texto completo no PMC" (https://pmc.ncbi.nlm.nih.gov/articles/PMC11641623/)

Implicações: não estabelecer um prazo universal, permitir acompanhamento prolongado e tratar estimativas como referências populacionais, não como garantias individuais.

3.2. Repetição em contextos estáveis

Lally et al. (2010), em How are habits formed: Modelling habit formation in the real world, estudaram comportamentos repetidos em contextos cotidianos.

Entre os participantes cujo modelo de automaticidade pôde ser ajustado, o tempo estimado para atingir 95% do nível assintótico variou de 18 a 254 dias.

O estudo também observou que uma oportunidade perdida não prejudicou materialmente a formação do hábito naquele contexto experimental.

Fonte: "DOI — How are habits formed?" (https://doi.org/10.1002/ejsp.674)

Implicações: associar hábitos a contextos estáveis, evitar penalidades por falhas isoladas e facilitar a retomada.

3.3. Prática deliberada e expertise

Ericsson, Krampe e Tesch-Römer (1993), em The Role of Deliberate Practice in the Acquisition of Expert Performance, investigaram a importância da prática estruturada e direcionada à melhoria do desempenho.

A popular regra das 10.000 horas não representa um prazo universal para alcançar expertise. O desenvolvimento de habilidades depende de fatores como domínio, qualidade da prática, feedback e características individuais.

Uma meta-análise de Macnamara, Hambrick e Oswald (2014) identificou diferenças importantes na proporção da variação de desempenho explicada pela prática deliberada em diferentes domínios.

Fontes:

- "Ericsson et al. (1993)" (https://doi.org/10.1037/0033-295X.100.3.363)
- "Macnamara et al. (2014)" (https://doi.org/10.1177/0956797614535810)

Implicações: registrar tempo de prática, permitir metas pessoais de horas e distinguir prática acumulada de competência demonstrada.

3.4. Interrupções e perda de hábitos

Não existe um prazo universal bem estabelecido após o qual um hábito necessariamente desaparece.

O produto poderá registrar períodos de interrupção e sugerir retomadas, mas não deverá utilizar uma contagem regressiva para afirmar quando o usuário perderá um hábito ou uma habilidade.

3.5. Técnicas digitais de mudança de comportamento

Revisões sistemáticas identificaram técnicas como automonitoramento, definição de metas, lembretes, feedback e personalização em intervenções digitais voltadas à formação de hábitos.

Fontes:

- "JMIR — Digital Behavior Change Intervention Designs for Habit Formation" (https://www.jmir.org/2024/1/e54375)
- "Annals of Behavioral Medicine — Effective Behavior Change Techniques" (https://academic.oup.com/abm/article/57/10/817/7251346)

Essas evidências orientarão as funcionalidades, sem pressupor que qualquer implementação específica produzirá resultados garantidos.

---

4. Funcionalidades do aplicativo

4.1. Cadastro de hábitos

O usuário poderá definir:

- Nome e descrição.
- Categoria opcional.
- Frequência.
- Meta inicial.
- Unidade de medida.
- Contexto ou horário preferencial.
- Data de início.
- Lembretes opcionais.

4.2. Registro diário

Cada registro poderá indicar:

- Realizado.
- Realizado parcialmente.
- Não realizado.
- Sem registro.

O usuário poderá corrigir registros anteriores.

4.3. Calendário e histórico

O calendário permitirá consultar registros, identificar padrões, observar interrupções e visualizar mudanças nas metas.

4.4. Painel de progresso

O painel poderá mostrar:

- Frequência de realização.
- Percentual de realização nos dias elegíveis e registrados, com critérios transparentes.
- Tempo acumulado de prática.
- Evolução das metas.
- Marcos alcançados.
- Histórico de retomadas.

4.5. Motor de próximos passos

Um motor de regras determinísticas poderá sugerir:

1. Manter a meta atual.
2. Experimentar um aumento gradual.
3. Reduzir temporariamente a meta.
4. Rever o horário ou contexto.
5. Retomar com uma ação menor.
6. Aguardar mais registros antes de recomendar uma mudança.

As recomendações deverão ser opcionais e apresentar justificativas compreensíveis.

4.6. Biblioteca de orientações

A biblioteca reunirá estratégias sobre metas realistas, repetição em contextos estáveis, prática deliberada, planejamento de obstáculos, retomada e progressão gradual.

As orientações deverão incluir fontes científicas quando aplicável e explicitar suas limitações.

4.7. Lembretes

O usuário poderá configurar notificações locais, com horários e frequência sob seu controle.

4.8. Gamificação

A gamificação poderá incluir:

- Marcos de consistência.
- Calendário visual.
- Gráficos de frequência.
- Tempo acumulado de prática.
- Progresso até metas pessoais.
- Reconhecimento de retomadas.
- Histórico de evolução.

Marcos como 30 ou 60 dias poderão ser apresentados como objetivos de acompanhamento, sem afirmar que representam prazos científicos universais para a formação de hábitos.

Para habilidades, o aplicativo poderá permitir marcos de 10, 50, 100 ou 500 horas, por exemplo, sempre deixando claro que são metas de prática e não níveis comprovados de expertise.

---

5. Modelo de monetização

5.1. Estratégia geral: freemium

O modelo comercial proposto será baseado em duas versões:

- Plano gratuito: permite experimentar o conceito e acompanhar um hábito localmente.
- Plano premium: oferece continuidade entre dispositivos, sincronização em nuvem e outros benefícios que forem validados.

A intenção é que a versão gratuita seja útil por si só, enquanto a versão paga resolva uma necessidade adicional concreta.

5.2. Plano gratuito

O plano gratuito poderá oferecer:

- Cadastro de um hábito ativo.
- Armazenamento local no aparelho.
- Registro diário.
- Calendário e histórico.
- Progresso básico.
- Sugestões iniciais baseadas em regras.
- Biblioteca básica de orientações.
- Lembretes locais.
- Funcionamento offline.

O limite inicial proposto é de um hábito cadastrado. Esse limite ainda deverá ser validado com usuários, pois pode ser restritivo demais para quem deseja acompanhar mais de um comportamento.

Os dados permanecerão armazenados localmente. Não será necessária uma conta para utilizar as funcionalidades básicas.

Ponto de atenção: a ausência de nuvem significa que os dados não estarão automaticamente sincronizados ou protegidos por um backup remoto. A interface deverá comunicar isso claramente e oferecer instruções para evitar perda de dados ao trocar de aparelho ou reinstalar o aplicativo.

5.3. Plano premium

A principal proposta do premium será permitir que o usuário continue sua jornada em diferentes dispositivos, sem depender de um único aparelho.

Funcionalidades candidatas:

- Cadastro de múltiplos hábitos.
- Sincronização em nuvem.
- Conta de usuário.
- Acesso aos mesmos hábitos em diferentes dispositivos.
- Backup remoto.
- Restauração dos dados após troca de aparelho.
- Histórico sincronizado.
- Continuidade dos registros e metas em diferentes dispositivos.

Funcionalidades adicionais, como relatórios avançados e jornadas guiadas, poderão ser avaliadas posteriormente.

O principal diferencial comercial deverá ser a continuidade da experiência, não a retirada de funcionalidades básicas essenciais para tornar o aplicativo útil.

5.4. Assinatura mensal e anual

O premium poderá oferecer duas opções:

Mensal: pagamento recorrente, com menor compromisso inicial.

Anual: pagamento antecipado por doze meses, com desconto em relação ao preço mensal acumulado.

Os preços ainda não foram definidos.

A estratégia de preço deverá considerar:

- Disposição real dos usuários para pagar.
- Custos das lojas de aplicativos.
- Impostos e taxas de pagamento.
- Infraestrutura e armazenamento.
- Custos de suporte.
- Custos de aquisição de usuários.
- Taxa de cancelamento.
- Margem necessária para sustentar o produto.

A assinatura anual poderá melhorar a previsibilidade da receita e reduzir a frequência de cobranças, mas o desconto deverá preservar uma margem sustentável.

5.5. Hipóteses de preço para teste

Como ponto de partida para pesquisa comercial, poderão ser avaliadas faixas como:

- Mensal: R$ 7,90 a R$ 12,90.
- Anual: preço equivalente a aproximadamente 8 a 10 mensalidades.

Esses valores são hipóteses de teste, não preços definidos ou comprovadamente aceitos pelo mercado.

O preço final deverá ser escolhido após entrevistas, testes de oferta e análise de custos.

5.6. Por que cobrar pela sincronização?

A sincronização resolve uma necessidade concreta: permitir que o usuário mantenha o mesmo histórico e continue registrando suas atividades ao trocar de dispositivo ou utilizar mais de um aparelho.

Ela também cria uma justificativa recorrente para a assinatura, pois o serviço de nuvem exige manutenção contínua.

Entretanto, sincronização não deverá ser tratada como uma funcionalidade trivial. Ela exige autenticação, controle de acesso, resolução de conflitos, proteção dos dados e tratamento de falhas de rede.

Por isso, a primeira versão deverá funcionar localmente. A nuvem será implementada quando a proposta principal estiver validada.

---

6. Arquitetura e tecnologias

6.1. Aplicativo Android

Kotlin + Jetpack Compose

Escolhidos para aprender desenvolvimento Android nativo e aproveitar o conhecimento de Java.

6.2. Persistência local

Room + SQLite

Armazenará hábitos, registros, metas, orientações e marcos sem depender de um servidor.

6.3. Estado e arquitetura

ViewModel + StateFlow + corrotinas

Separarão a interface da lógica e permitirão operações assíncronas.

6.4. Backend futuro

Java + Spring Boot

Poderá fornecer APIs para contas, sincronização, backup e compartilhamento.

O backend deverá ser adicionado quando a necessidade comercial justificar o custo e a complexidade.

6.5. Sincronização futura

A implementação deverá considerar:

- Autenticação segura.
- Identificação dos registros.
- Sincronização incremental.
- Tratamento de alterações concorrentes.
- Resolução de conflitos.
- Funcionamento offline.
- Exclusão de conta e dados.
- Proteção de dados em trânsito e armazenados.
- Recuperação após falhas.

A sincronização deverá preservar o histórico e evitar duplicações.

6.6. Inteligência artificial

A IA será utilizada inicialmente para pesquisa, síntese e organização de evidências científicas, com revisão das fontes originais.

Não será necessária IA em tempo de execução no MVP.

---

7. Modelo de dados inicial

Habit

Representa um hábito cadastrado.

Campos conceituais:

- "id"
- "name"
- "description"
- "category"
- "unit"
- "targetValue"
- "frequency"
- "preferredContext"
- "startDate"
- "isArchived"

HabitLog

Representa um registro diário.

Campos:

- "id"
- "habitId"
- "date"
- "status"
- "actualValue"
- "durationMinutes"
- "note"

HabitGoalHistory

Preserva o histórico de metas e suas datas de vigência.

Strategy

Armazena orientações e referências.

RecommendationRule

Representa regras do motor de recomendações.

Milestone

Armazena marcos pessoais e conquistas.

PracticeSession

Armazena sessões de prática e duração.

UserAccount — futuro

Representará a conta do usuário no plano premium.

SyncMetadata — futuro

Poderá armazenar informações técnicas necessárias para sincronização, como versão do registro, data da última alteração e estado de sincronização.

Essas estruturas serão refinadas durante o desenvolvimento.

---

8. Plano de execução

Etapa 1 — Refinamento da ideia

Definir público, problema, proposta de valor e diferencial.

Resultado: documento de visão e hipóteses prioritárias.

Etapa 2 — Pesquisa científica aplicada

Organizar os estudos, suas limitações e as regras que poderão orientar o produto.

Resultado: biblioteca inicial de estratégias fundamentadas.

Etapa 3 — Validação com usuários

Entrevistar potenciais usuários e testar a compreensão da proposta.

Resultado: evidências qualitativas sobre utilidade e necessidades.

Etapa 4 — Definição do MVP

Selecionar cadastro, registros, calendário, histórico, progresso e sugestões básicas.

Resultado: especificação funcional com critérios de aceitação.

Etapa 5 — Protótipo visual

Desenhar as telas e testar os fluxos principais.

Resultado: protótipo navegável.

Etapa 6 — Preparação técnica

Configurar Kotlin, Compose, Room, navegação e testes.

Resultado: projeto executável com persistência local.

Etapa 7 — Implementação do MVP

Desenvolver o fluxo completo de cadastro, registro, histórico e recomendações.

Resultado: aplicativo funcional offline.

Etapa 8 — Testes com usuários

Observar frequência de uso, dificuldades e utilidade das sugestões.

Resultado: lista priorizada de melhorias.

Etapa 9 — Validação comercial

Testar o limite gratuito, os benefícios premium e a disposição para pagar.

Resultado: primeiras evidências sobre monetização.

Etapa 10 — Sincronização e assinatura

Implementar contas, backend, sincronização e pagamentos somente após validar a necessidade e o modelo comercial.

Resultado: versão premium capaz de sustentar a experiência entre dispositivos.

Etapa 11 — Publicação e evolução

Publicar, acompanhar retenção e avaliações e evoluir o produto com base em evidências.

Resultado: produto público em melhoria contínua.

---

9. Métricas de sucesso

O projeto deverá acompanhar:

- Ativação: usuários que cadastram um hábito e fazem o primeiro registro.
- Retenção: usuários que continuam utilizando o aplicativo.
- Frequência de registro.
- Utilidade percebida das recomendações.
- Retomada após interrupções.
- Marcos alcançados.
- Conversão do plano gratuito para o premium.
- Cancelamento das assinaturas.
- Receita recorrente mensal.
- Custo de infraestrutura por usuário pagante.
- Margem após taxas, impostos e custos operacionais.

As métricas deverão distinguir ausência de registro de abandono confirmado.

---

10. Privacidade e responsabilidade

O aplicativo deverá:

- Coletar somente os dados necessários.
- Permitir consultar e excluir registros.
- Evitar compartilhamento sem consentimento.
- Proteger os dados sincronizados.
- Explicar as limitações das recomendações.
- Não apresentar estimativas como garantias científicas.
- Permitir que o usuário controle suas metas e notificações.

A versão gratuita local reduzirá a necessidade de transmissão de dados. O plano premium exigirá uma política de privacidade clara, medidas de segurança e procedimentos para exclusão e exportação dos dados conforme aplicável.

---

11. Decisões e hipóteses ainda abertas

Diretrizes já estabelecidas

- O produto será inicialmente Android.
- Kotlin e Jetpack Compose serão as tecnologias principais.
- O aplicativo permitirá que o usuário escolha seus hábitos.
- O registro e o histórico serão simples.
- O progresso poderá ser acompanhado visualmente.
- As sugestões utilizarão regras transparentes.
- A pesquisa científica orientará o conteúdo.
- A primeira versão funcionará localmente.

Hipóteses a validar

- Limitar o plano gratuito a um hábito.
- Oferecer múltiplos hábitos e sincronização no premium.
- Cobrar mensalmente ou anualmente.
- Definir preços na faixa inicialmente sugerida.
- Acrescentar relatórios avançados ou jornadas guiadas.
- Implementar backend e autenticação.
- Escolher a política definitiva de backup e 
