# Pequenos Passos — Especificação do Produto

## Nova funcionalidade: notificações interativas e registro rápido de hábitos

### 1. Objetivo

Permitir que o usuário registre o cumprimento de um hábito diretamente pela notificação do celular, sem precisar navegar pelo aplicativo para realizar a ação mais comum.

O princípio central é reduzir o atrito do registro diário: **um toque para registrar o resultado; detalhes adicionais somente quando desejado.**

### 2. Configuração dos lembretes

Cada hábito poderá ter um lembrete configurável pelo usuário, com opções como:

- Horário do lembrete.
- Dias da semana em que ele será exibido.
- Ativar ou desativar o lembrete individualmente.
- Escolher se o registro rápido deverá abrir o aplicativo para adicionar informações complementares.

A opção de abrir o aplicativo para adicionar detalhes virá **ativada por padrão**, mas poderá ser desativada nas configurações do aplicativo.

### 3. Interação com a notificação

No horário configurado, o sistema exibirá uma notificação relacionada ao hábito, com três ações:

- **Cumpri:** registra que o hábito foi realizado.
- **Não cumpri:** registra explicitamente que o hábito não foi realizado.
- **Adiar:** posterga o lembrete sem registrar sucesso ou falha.

O comportamento deverá priorizar a rapidez, permitindo que o usuário registre o resultado sem precisar abrir o aplicativo.

#### Ao selecionar “Cumpri”

1. Registrar o resultado como concluído.
2. Salvar a data e o horário do registro.
3. Salvar a referência ao hábito correspondente.
4. Se a abertura para detalhes estiver ativada, abrir o aplicativo na tela de complementação do registro.
5. Permitir que o usuário adicione informações opcionais, como quantidade realizada, duração e observações.

#### Ao selecionar “Não cumpri”

1. Registrar explicitamente que o hábito não foi realizado.
2. Salvar a data e o horário do registro.
3. Se a abertura para detalhes estiver ativada, permitir que o usuário informe o contexto, o motivo ou outras observações, sem obrigatoriedade.
4. Se a configuração estiver desativada, concluir o registro sem abrir o aplicativo.

O registro negativo não deve apagar o progresso anterior nem gerar mensagens de culpa.

#### Ao selecionar “Adiar”

1. Não registrar o hábito como cumprido ou não cumprido.
2. Agendar um novo lembrete conforme a opção de adiamento escolhida ou uma duração padrão configurável.
3. Evitar notificações duplicadas para o mesmo lembrete.
4. Manter o hábito sem resultado registrado até que o usuário tome uma decisão ou registre a execução por outro caminho.

Adiar não deve ser interpretado como falha.

### 4. Complementação opcional do registro

A tela de complementação deverá ser simples, rápida e adaptável ao tipo de hábito.

O usuário poderá informar:

- Quantidade realizada.
- Duração da atividade.
- Observações livres.
- Informações específicas relevantes para o hábito, quando aplicável.

Exemplos:

| Hábito | Registro básico | Informações complementares |
|---|---|---|
| Leitura | Cumpri | 5 páginas, 15 minutos, observação sobre o livro |
| Exercício | Cumpri | 30 minutos, tipo de atividade, intensidade opcional |
| Estudo | Cumpri | 45 minutos, assunto estudado |
| Alimentação | Cumpri parcialmente, se essa opção estiver disponível no fluxo do hábito | Seguiu o planejamento até o almoço; saiu da dieta à tarde |
| Meditação | Cumpri | 10 minutos, observação sobre a experiência |

Os exemplos não devem impor campos rígidos a todos os hábitos. O modelo deve permitir diferentes unidades e quantidades, pois cada usuário poderá acompanhar atividades muito distintas.

### 5. Registro parcial e hábitos com diferentes critérios

O produto deverá distinguir três conceitos:

- **Resultado do hábito:** cumprido, não cumprido ou parcialmente cumprido, quando o hábito admitir essa classificação.
- **Quantidade ou duração:** quanto foi realizado, independentemente do resultado geral.
- **Observações:** informações adicionais fornecidas voluntariamente pelo usuário.

Por exemplo, uma pessoa pode ter lido cinco páginas, embora sua meta fosse dez. O registro pode ser parcial, com a quantidade efetivamente realizada preservada.

Da mesma forma, alguém pode ter seguido o planejamento alimentar durante parte do dia, mas não durante todo o período. O aplicativo deverá permitir descrever esse resultado sem reduzir toda a experiência a uma classificação binária.

A classificação parcial poderá ser opcional ou oferecida de acordo com a configuração do hábito. Ela não deve tornar o registro rápido mais complexo.

### 6. Configuração de abertura após o registro

A preferência de abertura do aplicativo deverá existir nas configurações, com o seguinte comportamento inicial:

- **Ativada:** depois de selecionar “Cumpri” ou “Não cumpri”, o aplicativo abre a tela para complementar o registro.
- **Desativada:** o resultado é salvo diretamente pela notificação, sem exigir que o usuário abra o aplicativo.
- **Adiar:** somente reagenda o lembrete, sem abrir obrigatoriamente a tela de detalhes.

Quando o usuário adicionar informações complementares, elas deverão ser associadas ao mesmo registro, sem criar duas execuções distintas para o mesmo evento.

A implementação também deverá tratar com segurança toques repetidos, notificações antigas e alterações realizadas simultaneamente no aplicativo.

### 7. Histórico e uso dos dados

Cada registro deverá preservar, no mínimo:

- Hábito associado.
- Data e horário da execução ou da declaração do resultado.
- Status do registro.
- Quantidade realizada, quando aplicável.
- Duração, quando aplicável.
- Observações opcionais.
- Origem do registro, como notificação ou aplicativo, quando útil para auditoria e análise.

É importante distinguir o horário em que a atividade ocorreu do horário em que o usuário informou o resultado. Quando esses horários não forem iguais, o aplicativo não deverá apresentar o horário do toque como se fosse necessariamente o horário exato da execução.

O histórico deverá permitir consultar as informações complementares e, futuramente, utilizá-las para gráficos, acompanhamento de metas e recomendações personalizadas.

### 8. Regras de experiência do usuário

- Registrar um resultado deve exigir o menor número possível de interações.
- Informações complementares nunca devem ser obrigatórias para concluir o registro.
- A ausência de registro não equivale a uma falha confirmada.
- Adiar um lembrete não equivale a cumprir ou não cumprir o hábito.
- O usuário deve poder corrigir registros incorretos.
- O aplicativo deve preservar o histórico de maneira consistente.
- A experiência deve evitar culpa, pressão excessiva e punições por interrupções.
- O aplicativo deve funcionar offline, utilizando os recursos locais do Android para notificações e persistência no MVP.
