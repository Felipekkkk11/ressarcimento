Plataforma de Ressarcimento é uma plataforma tecnológica capaz de recepcionar e processar as informações de consumo de transações entre os Participantes do Open Banking Brasil.

## Objetivo

Através de uma Plataforam, o ressarcimento de custos de chamadas de interface entre os Participantes será feito de forma centralizada, a partir do início do compartilhamento de Dados Cadastrais e Transacionais, com a implantação da Plataforma e de um processo unificado de cobrança, observadas as suas atividades e parâmetros a serem estabelecidos.

Dessa forma, o ressarcimento de despesas busca seguir, entre outros, os seguintes objetivos e fundamentos:

 - Assegurar o melhor desenvolvimento e uso eficiente do Ecossistema pelos Participantes, regular o volume de Chamadas de Interface e atribuir maior previsibilidade às obrigações delas decorrentes, coibir abusos nas Chamadas de Interface, danosos ao Ecossistema e aos Participantes e proporcionar melhor experiência do usuário ao utilizar o Ecossistema.
 - Assegurar o tratamento equitativo e aplicação de parâmetros do Ressarcimento justificados, aplicáveis igualmente a todos os Participantes, e evitar que custos de ineficiência tecnológica e operacional componham os custos, respeitados os Limites Mínimos de Gratuidade e os padrões previstos no Regulamento, e na Resolução e legislação vigente.

## Visão geral

A plataforma dispões de alguns módulos, conforme a seguir:

- Módulo de Reporte de Consumo
- Módulo de Processamento e Cobrança
- Módulo de Relatórios de Consumo
- Módulo de Contestanção de Consumo
- Portal do Participante

### Reporte de Consumo

É através deste módulo que os participantes enviarão suas informações de consumos entre participantes para que a plataforma tenha ciência e possa conciliar e contabilizar essas transações.

Cada participante deverá enviar cada transação que fora consumida por sua plataforma ou que tenha consumido de uma plataforma de terceiro.

A plataforma dispões de alguns canais de reporte, como:

- Envio de transações via APIs (REST)
- Envio de Arquivos via SFTP

#### Envio de transações via APIs
O Participante deverá enviar todas as transações que envolveram a sua plataforma, sendo, consumindo informação de plataformas terceiras ou sendo consumido por estas.

Para o envio de informações via APIs o Participante poderá escolher se deseja enviar o reporte de transações de maneira unitária, ou seja, conforme o consumo ocorre, ou enviar de em grupos pelo envio em massa.

##### Reporte unitário
Através deste modelo de notificação é possível enviar de maneira unitária cada uma das transações realizadas junto à sua plataforma.

##### Reporte em massa
Utilize o reporte em massa para enviar grupos de transações, podendo agrupá-las em pacotes maiores para evitar perdas e controle mais rígidos de reenvio.

Este modelo deve ser utilizado para Instituições Participantes que possuem um grande volume de tráfego entre transmissão e recepção de informações, podendo este ser utilizado para envios diários ou por grandes períodos em um dia útil.

Para saber mais sobre as APIs acesse [Portal de APIs - Plataforma de Ressarcimento do Open Banking Brasil](https://ressarcimento.opbkdev.smartfylabs.com/api-docs/)

### Processamento e Cobrança
Este módulo é responsável por conciliar e contabilizar as transações solicitadas e processadas entre os Participantes do Open Banking Brasil.

Esta conciliação ocorrerá de maneira agendada em D+2 após o fechamento do dia.

Deste modo cada Participante deverá enviar o reporte ocorridas para um dia útil em até no máximo 24 horas após o fechamento do dia (00:00 GMT-3).

O Participante que perder o prazo de envio das informações deverá aguardar o relatório oficial de fechamento diário para iniciar o processo de contestação, conforme descrito no item [Módulo de Contestanção de Consumo](#módulo-de-contestação-de-consumo)

### Relatórios de Consumo
[EM DESENVOLVIMENTO]
Este módulo visa disponibilizar os relatórios gerenciais, analíticos e financeiros em relação ao consumo das plataformas entre transmissoras e receptoras.

Uma vez realizada a concialiação e contabilização das transações entre transmissoras e receptoras, de acordo com todos os reportes de transações enviados, as empresas receberão seus relatórios de fechamento diário. Caso haja algum desencontro de informações a Instituição Participante deverá notificar esta diferença para a equipe de suporte do Ressarcimento do Open Banking Brasil através da Plataforma de Ressarcimento. A plataforma irá mediar a comunicação entre os envolvidos e dará início ao processo de análise.

### Módulo de Contestanção de Consumo
[EM DESENVOLVIMENTO]

Para saber mais sobre as APIs acesse [Portal de APIs - Plataforma de Ressarcimento do Open Banking Brasil](https://ressarcimento.opbkdev.smartfylabs.com/api-docs/)

### Portal do Participante
[EM DESENVOLVIMENTO]
