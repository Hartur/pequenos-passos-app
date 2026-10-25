# Pequenos Passos — telas e interações do protótipo

Este documento registra as decisões de produto feitas para o protótipo visual. Ele define o conteúdo e os estados das telas. A especificação de notificações continua sendo a fonte de verdade para lembretes e registro rápido.

## Escopo e estados futuros

Os estados de conta, assinatura e sincronização fazem parte do protótipo para validar entendimento e proposta de valor. Eles não autorizam a implementação de autenticação, pagamentos ou nuvem antes da etapa correspondente do roadmap.

No estado sem conta, o aplicativo apresenta um hábito ativo. A tela explica de forma breve que criar uma conta permite acompanhar mais hábitos e preservar a continuidade entre dispositivos quando esse recurso estiver disponível. A mensagem não deve sugerir que os dados locais estejam protegidos por sincronização enquanto ela não estiver ativa.

## Navegação principal

A navegação inferior reúne quatro destinos: **Hoje**, **Hábitos**, **Registros** e **Mais**. Ela destaca o destino atual e preserva o contexto ao trocar de tela.

## Hoje

A tela Hoje mostra somente os hábitos agendados para o dia em foco, com nome, meta ou duração, horário quando existir e o estado do registro. A tela não interpreta ausência de registro como falha.

### Com conta

- Exibe foto ou avatar, cumprimento e nome da pessoa.
- Mostra a data, o seletor de dia e o resumo dos hábitos concluídos entre os hábitos planejados.
- Lista vários hábitos programados para o dia.
- Cada item permite reconhecer a categoria por cor e ícone e informa se está concluído, parcial ou ainda sem registro.

### Sem conta

- Não exibe foto, cumprimento ou nome de perfil.
- Exibe somente o hábito ativo permitido nesse estado.
- Mostra um convite curto para criar uma conta e acompanhar mais hábitos. O convite não interrompe o registro do hábito já existente.

## Hábitos

A tela Hábitos lista os hábitos cadastrados e oferece adicionar, editar e iniciar a remoção de vários itens.

### Edição rápida no card

Cada card mostra e permite ajustar rapidamente:

- dias da semana em que o hábito deve ser realizado;
- duração ou meta de tempo;
- ação de editar os detalhes;
- ação de remover o hábito.

### Remoção de vários hábitos

Ao selecionar **Remover vários**, os cards passam para o modo compacto e escondem os controles de edição rápida. A seleção ocorre ao tocar no próprio card, sem checkbox ou radio button.

- Um item selecionado recebe fundo cinza claro e o seu nome fica riscado.
- A tela informa a quantidade de itens selecionados e mantém uma ação para cancelar o modo.
- Enquanto não houver seleção, não há ação de exclusão disponível.
- Ao selecionar pelo menos um item, aparece uma ação flutuante **Excluir _n_ hábitos**. A exclusão efetiva deve pedir confirmação antes de remover dados.

## Registros

A tela Registros oferece um gráfico em períodos semanais, mensais ou anuais. A visão semanal é o estado inicial do protótipo.

Os gráficos mostram a frequência de registros por hábito e mantêm uma legenda distinguindo registrado, parcialmente realizado e sem registro. Dias sem registro não podem ser incluídos em contagens de falha nem receber linguagem punitiva.

## Mais

A tela Mais agrupa preferências de perfil e informações do plano:

- perfil: alterar nome, senha e foto;
- assinatura: informar se está ativa ou se a pessoa está no plano gratuito;
- sincronização: informar o estado atual da nuvem, como conectada, pendente, indisponível ou não conectada.

Quando a sincronização não estiver disponível ou não tiver sido ativada, a tela deve explicar que os dados permanecem no aparelho. Estados de assinatura e nuvem precisam representar o estado real do serviço quando forem implementados.
