# SPRINT DE GESTÃO ÁGIL DE PROJETOS E PRODUTOS
## FERRAMENTAS UTILIZADAS NO MVP
Miro: desenvolvimento de uma lean inception para ideação e delimitação do escopo do MVP
Figma: desenvolvimento de protótipos de baixa fidelidade
Jira: gestão do backlog do produto e do projeto

## DOCUMENTOS DO REPOSITÓRIO
MVP Canvas - Miro: https://miro.com/app/board/uXjVM2S9g5o=/  
Figma:  
Jira: https://afsneto.atlassian.net/jira/software/projects/AFSN/boards/1/backlog

## LEAN INCEPTION
### KICKOFF
Esse MVP tem como escopo a ideação e planejamento inicial de um novo produto de software.

A empresa MYLINES é dona de 3 concessões de linhas de transmissão, totalizando 600 km de extensão. Para cada concessão temos um almoxarifado onde os materiais sobressalentes são armazenados. Como exemplo destes materiais temos: 
* Torres metálicas treliçadas;
* Isoladores;
* Bobinas de cabos condutores e para-raios;
* Acessórios e ferragens.

O objetivo deste projeto é o desenvolvimento de uma plataforma Web para gerenciamento e unificação do inventório de materiais sobressalentes localizados nos diferentes almoxarifados.

### EQUIPE
* PO: José
* Scrum Master: Bruna
* Desenvolvedor Backend: Adriano
* Desenvolvedor Frontend: Roberta
### VISION
* PARA responsáveis pela O&M (operação e manutenção)
* QUE estejam tentando consultar os materiais sobressalentes de cada almoxarifado
* O SAVEINLINE 
* É um aplicativo Web
* QUE auxilia na consulta e realiza a gestão automática de materiais sobressalentes disponíveis em cada almoxarifado
* DIFERENTE de tabelas .xlsx independentes e alimentadas isoladamente pelo gestor de cada almoxarifado.
*  NOSSO PRODUTO oferece uma solução integrada e automatizada para o gerenciamento de múltiplos almoxarifados da empresa, buscando assim maior dinamismo no atendimento de ocorrências em campo.

### IS - IS NOT - DOES - DOES NOT DO
#### IS
* Um aplicativo Web que auxilia no consulta e integração de almoxarifados da empresa
* Plataforma que fornece avisos personalizados para a coordenação e gerência de O&M
#### IS NOT
* Um aplicativo para realização de compra e venda de materiais
* Aplicativo para cálculo dos custos de envio (frete, impostos, embalagem) dos materiais entre concessões
#### DOES
* Cadastro e consulta de materiais existentes para cada almoxarifado
* Acompanhamento de frequência de uso dos materiais
* Envio automático de relatórios para a gerência
* Apresentação da lista de materiais necessários conforme instrução de trabalho (IT) solicitada

#### DOES NOT DO
* Realiza compra / reposição de materiais
* Consulta de preços históricos
* Elaboração e envio automático de pedidos de compra ao mercado para os fornecedores homologados

### GOALS
* Redução nas despesas
    * Evitar a compra de materiais disponíveis em outros almoxarifados
    * Integração entre os almoxarifados
    * Compra otimizada de maiores volumes de materiais necessários em diferentes concessões (melhora com negociação junto ao fonrecedor devido ao aumento no volume negociado de materiais)
* Maior agilidade no atendimento de emergências
    * Consulta rápida sem necessidade de comunicação com cada almoxarifado
    * Verificação por geolocalização da disponibilidade do material em almoxarifado mais próximo para atendimento da emergência
    * Lista automatizada de materiais para cada tipo de intervenção
* Melhor controle 
    * Possibilidade de extração de relatórios
    * Melhor planejamento na compra de materiais com maior utilização pela O&M
    * Compatibilização dos dados técnicos dos materiais disponíveis em cada almoxarifado

### PERSONAS
* André, "o gerente"  
    * 51 anos; engenheiro eletricista; averso a novas tecnologias.
    * Responsável pela mobilização de equipes disponíveis em campo para atendimentos emergenciais.
    * Precisa de um sistema com interface simples para consultas aos almoxarifados.
    
* Renato, "chefe da equipe em campo"
    * 37 anos; engenheiro eletricista; é autodisciplinado.
    * Responsável pela orientação e alinhamento da instrução de trabalho junto à equipe, conforme característica da emergência.
    * Possui certa facilidade com tecnologia, não havendo limitações no uso de aplicativos Web.
    * Necessita de um relatório incluindo a instrução de trabalho, relacionado à ocorrência, junto com a relação de materiais e ferramentas necessários à intervenção.
    
* Rodrigo, "chefe do almoxarifado"
    * 32 anos; técnico eletricista; conhecimento adquirido pela prática em campo.
    * Responsável pelo controle de materiais do almoxarifado.
    * Necessita de consultas simples e rápidas aos materiais disponíveis no almoxarifado, e melhor controle dos itens que entram e saem do almoxarifado.


### USER JOURNEYS
* André, "o gerente"  
    * Recebe uma comunicação do centro de operações (COL) sobre a ocorrência de um sinistro.
    * Entra em comunicação com o engenheiro de campo responsável pela linha de transmissão onde foi identificada a ocorrência.
    * Acesso ao sistema SAVEINLINE, seleciona o tipo da ocorrência, nome ou sigla do engenheiro de campo responsável e registra a solicitação.
    * Após a solução da ocorrência, André verifica através do um relatório gerado pelo sistema, um resumo da ocorrência e relação dos materiais / ferramentas utilizadas no serviço.
* Renato, "chefe de equipe em campo" 
    * Após atendimento da ligação do André, e do COL, Renato mobiliza equipe para intervenção.
    * Renato e equipe vai até almoxarifado buscar materiais e ferramentas conforme relação fornecida pelo sistema.
    * Após solução do problema, Renato preenche um formulário do sistema indicando quais materiais foram utilizados em campo, e quais retornaram ao almoxarifado.
* Rodrigo, "chefe do almoxarifado"
    * Mantém o almoxarifado em ordem.
    * Verifica diariamente os materiais e ferramentas, mantendo a relação de materiais cadastrados no sitema sempre atualizada.
    * Após intervenção em campo e submissão do relatório do Renato no sistema, Rodrigo verifica relação de materiais utilizados.
    * Rodrigo confirma as alterações indicadas pelo Renato, atualizando assim a relação dos materiais disponíveis no almoxarifado.
    * Rodrigo indica no sistema quais itens necessitam de reposição, e esta solicitação é recebida pelo André.

### FEATURE BRAINSTORMING
* Interface simples    
* Cadastro de novos materiais
* Busca de material por Estado ou concessão (Transmissora)
* Após localização do material nova página é aberta com as seguintes informações:
    * Código do material
    * Fabricante
    * Descrição
    * Quantidade
    * Cacterísticas Técnicas
    * Opção para anexar desenhos ou documentos técnicos
* Na página do material botão para solicitação de compra de novas unidades
* Na tela de submissão do relatório após retorno de campo, opção para realizar o upload de fotos com o registro do sinistro.
* Desenvolvimento futuro de app Android para utilização em conjunto da plataforma Web, com foco na equipe em campo.
* Definir opção para cadastramento de novos tipos de intervenção em campo (instruções de trabalho), com as informações:
    * Código da intervenção
    * Descrição
    * Relação de material necessário
    * Estimativa de tempo para solução do problema
    * Número de profissionais envolvidos
* Opção para geração de gráficos em barras para acompanhamento da utilização ao longo de um período de tempo de materiais (para determinado código ou por tipo de material empregado)

### TECHNICAL, BUSINESS AND UX REVIEW
![Alt text](imagens\Tech_Bus_Ux.PNG "TECHNICAL, BUSINESS AND UX REVIEW")
### SEQUENCER
![Alt text](imagens\Sequencer.PNG "SEQUENCER")
### MVP CANVAS
![Alt text](imagens\MVP_Canvas.PNG "MVP CANVAS")
## UI/UX Design
Protótipo de baixa fidelidade

## Backlog do produto

## Backlog da sprint

## Video
