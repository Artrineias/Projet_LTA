
# Projeto de Sistema para o Campeonato LTA: Uma Proposta Abrangente

Com a recente unificação dos cenários de League of Legends das Américas, o **LTA (League of Legends Championship of The Americas)** surge como um supercampeonato, consolidando as antigas LCS, CBLOL e LLA. Para gerenciar a complexidade e a grandiosidade deste novo formato, apresentamos uma proposta de sistema, detalhando suas etapas de desenvolvimento, com exceção da criação de interfaces. Este documento servirá como base para a construção de uma plataforma robusta e funcional para o LTA.

-----

## Etapa 1 – Requisitos – Diagrama de Casos de Uso

A primeira etapa foca na compreensão e documentação das necessidades do sistema, identificando quem irá interagir com ele e o que cada um poderá fazer.

### Atores Identificados:

  * **Espectador:** O fã do campeonato que consome as informações e transmissões.
  * **Administrador da Liga:** Responsável pela gestão geral do campeonato, configuração de partidas, equipes e conteúdo do sistema.
  * **Gerente de Equipe:** Responsável por gerenciar as informações de sua equipe, incluindo jogadores e comissão técnica.
  * **Jogador/Membro da Comissão Técnica:** Acessa informações restritas da equipe e do campeonato.

### Requisitos Funcionais:

  * **RF01:** O sistema deve permitir que o Espectador visualize o calendário de jogos.
  * **RF02:** O sistema deve exibir a classificação atualizada das equipes nas conferências Norte e Sul.
  * **RF03:** O sistema deve permitir assistir às partidas ao vivo e aos VODs (vídeos sob demanda) dos jogos passados.
  * **RF04:** O sistema deve apresentar estatísticas detalhadas das partidas, jogadores e equipes.
  * **RF05:** O sistema deve permitir que o Espectador configure notificações para o início dos jogos de suas equipes favoritas.
  * **RF06:** O Administrador da Liga deve poder cadastrar, editar e remover equipes e jogadores.
  * **RF07:** O Administrador da Liga deve poder agendar as partidas do campeonato.
  * **RF08:** O Administrador da Liga deve poder atualizar os resultados das partidas e as estatísticas.
  * **RF09:** O Administrador da Liga deve poder publicar notícias e comunicados oficiais.
  * **RF10:** O Gerente de Equipe deve poder submeter a escalação de sua equipe para as partidas.
  * **RF11:** O Gerente de Equipe deve poder atualizar as informações de perfil dos seus jogadores e comissão técnica.
  * **RF12:** Jogadores e Membros da Comissão Técnica devem poder visualizar informações internas e comunicados da liga.

### Requisitos Não Funcionais:

  * **RNF01 (Desempenho):** O sistema deve suportar um alto volume de acessos simultâneos durante as transmissões ao vivo, com tempo de carregamento de página inferior a 2 segundos.
  * **RNF02 (Usabilidade):** A interface do sistema deve ser intuitiva e de fácil navegação para todos os tipos de usuários.
  * **RNF03 (Disponibilidade):** O sistema deve ter uma disponibilidade de 99.8% durante o período do campeonato.
  * **RNF04 (Segurança):** O sistema deve garantir a segurança dos dados dos usuários e a integridade das informações da liga, utilizando autenticação de dois fatores para administradores e gerentes de equipe.
  * **RNF05 (Compatibilidade):** O sistema deve ser compatível com os principais navegadores web (Chrome, Firefox, Safari, Edge) e dispositivos móveis (iOS e Android).

### Diagrama de Casos de Uso:

*(Espaço para os Diagramas)*

### Narrativas dos Casos de Uso:

**Caso de Uso: Visualizar Calendário de Jogos**

  * **Ator:** Espectador
  * **Descrição:** O Espectador acessa a seção de calendário para ver as datas, horários e confrontos das próximas partidas do LTA.
  * **Fluxo Principal:**
    1.  O Espectador clica na opção "Calendário" no menu principal.
    2.  O sistema exibe o calendário com os jogos da semana atual.
    3.  O Espectador pode filtrar os jogos por conferência (Norte/Sul) e por semana/etapa do campeonato.

**Caso de Uso: Gerenciar Equipes**

  * **Ator:** Administrador da Liga
  * **Descrição:** O Administrador da Liga gerencia as informações das equipes participantes.
  * **Fluxo Principal:**
    1.  O Administrador da Liga faz login no sistema.
    2.  Acessa o painel de administração e seleciona a opção "Gerenciar Equipes".
    3.  O sistema exibe a lista de equipes cadastradas.
    4.  O Administrador pode adicionar uma nova equipe, editar as informações de uma equipe existente ou removê-la do campeonato.

-----

## Etapa 3 – Gestão de Configuração de Software

Para garantir a organização e o controle do desenvolvimento do projeto, propõe-se o uso do GitHub.

### Proposta de Organização da Configuração:

  * **Repositório Central:** Um único repositório no GitHub chamado `sistema-lta` será criado.
  * **Estrutura de Pastas:**
      * `/docs`: Para toda a documentação do projeto (requisitos, diagramas, atas de reunião).
      * `/src`: Contendo o código-fonte da aplicação.
      * `/tests`: Para os códigos de teste automatizados.
      * `/design`: Onde os arquivos de design da interface (Figma, Adobe XD) seriam armazenados.
  * **Estratégia de Branches:**
      * `main`: Branch principal, contendo apenas versões estáveis e testadas do sistema (releases).
      * `develop`: Branch de desenvolvimento principal, onde as novas funcionalidades são integradas.
      * `feature/<nome-da-feature>`: Branches criadas a partir de `develop` para desenvolver novas funcionalidades específicas (ex: `feature/calendario-de-jogos`).
      * `bugfix/<nome-do-bug>`: Branches para correção de bugs.
  * **Acesso ao Professor:** O usuário `AndersonLuizBarbosa` será adicionado como "Collaborator" ao repositório, com permissões de leitura (`Read`) ou escrita (`Write`), conforme a necessidade de avaliação e contribuição.

-----

## Etapa 4 – Métricas

A medição é fundamental para acompanhar o progresso e a qualidade do projeto.

### Cálculo de Pontos de Função (Estimado):

A Análise de Pontos de Função (APF) é uma técnica para medir o tamanho funcional de um software. Uma estimativa simplificada, considerando os requisitos funcionais, poderia ser:

| Tipo de Função                | Complexidade Baixa | Complexidade Média | Complexidade Alta |
| :---------------------------- | :----------------- | :----------------- | :---------------- |
| Entradas Externas             | 3                  | 4                  | 6                 |
| Saídas Externas               | 4                  | 5                  | 7                 |
| Consultas Externas            | 3                  | 4                  | 6                 |
| Arquivos Lógicos Internos     | 7                  | 10                 | 15                |
| Arquivos de Interface Externa | 5                  | 7                  | 10                |

Considerando os requisitos, uma contagem inicial simplificada poderia ser:

  * **Entradas Externas:** 6 (Login, Cadastro de Equipe, Agendamento de Partida, etc.) - Média Complexidade: 6 \* 4 = 24
  * **Saídas Externas:** 4 (Relatório de Classificação, Notificações, etc.) - Média Complexidade: 4 \* 5 = 20
  * **Consultas Externas:** 5 (Visualizar Calendário, Ver Estatísticas, etc.) - Baixa Complexidade: 5 \* 3 = 15
  * **Arquivos Lógicos Internos:** 3 (Equipes, Jogadores, Partidas) - Média Complexidade: 3 \* 10 = 30
  * **Arquivos de Interface Externa:** 1 (Integração com API da Riot Games para dados em tempo real) - Média Complexidade: 1 \* 7 = 7

**Total de Pontos de Função Não Ajustados (UFP):** 24 + 20 + 15 + 30 + 7 = **96**

Este valor seria refinado com uma análise mais aprofundada.

### Métricas para Acompanhamento:

  * **Velocity (Velocidade):** Mede a quantidade de "trabalho" (em Story Points) que a equipe consegue entregar por Sprint. Ajuda a prever o tempo necessário para completar o backlog.
  * **Lead Time:** O tempo total desde a concepção de uma funcionalidade até a sua entrega em produção.
  * **Cycle Time:** O tempo que a equipe leva para desenvolver e testar uma funcionalidade após o início do trabalho nela.
  * **Burndown Chart:** Gráfico que mostra o progresso do trabalho em uma Sprint, comparando o trabalho restante com o tempo disponível.
  * **Densidade de Defeitos:** Número de defeitos encontrados por Pontos de Função ou por release, indicando a qualidade do software.

-----

## Etapa 5 – SCRUM

A metodologia ágil SCRUM será utilizada para gerenciar o desenvolvimento do projeto de forma iterativa e incremental.

### Backlog do Sistema (Product Backlog):

Uma lista priorizada das funcionalidades desejadas para o sistema:

  * **Épico: Visualização do Campeonato**
      * Como Espectador, quero ver o calendário de jogos para saber quando meu time joga.
      * Como Espectador, quero ver a tabela de classificação para acompanhar o desempenho das equipes.
      * Como Espectador, quero assistir às transmissões ao vivo.
  * **Épico: Gerenciamento da Liga**
      * Como Administrador, quero cadastrar e gerenciar as equipes participantes.
      * Como Administrador, quero agendar as partidas das etapas do campeonato.
      * Como Administrador, quero inserir os resultados e estatísticas das partidas.
  * **Épico: Gerenciamento de Equipes**
      * Como Gerente de Equipe, quero submeter a escalação para a próxima partida.
      * Como Gerente de Equipe, quero atualizar o perfil dos meus jogadores.
  * **Épico: Notificações e Conteúdo**
      * Como Espectador, quero ser notificado sobre o início dos jogos.
      * Como Administrador, quero publicar notícias sobre o campeonato.

### Primeira Sprint:

  * **Duração:** 2 semanas.
  * **Objetivo da Sprint:** Entregar uma versão inicial do sistema com as funcionalidades essenciais de visualização do campeonato para os espectadores.
  * **Itens do Backlog da Sprint:**
      * Desenvolver a funcionalidade de visualização do calendário de jogos.
      * Implementar a exibição da tabela de classificação.
      * Criar a estrutura para o cadastro de equipes e jogadores (backend).

### Simulação da Execução da Sprint:

  * **Sprint Planning:** A equipe se reúne para selecionar os itens do backlog e detalhar as tarefas.
  * **Daily Scrum:** Reuniões diárias de 15 minutos para sincronizar o trabalho e identificar impedimentos.
  * **Desenvolvimento:** A equipe trabalha nas tarefas definidas.
  * **Sprint Review:** Ao final da Sprint, a equipe apresenta as funcionalidades desenvolvidas para as partes interessadas.
  * **Sprint Retrospective:** A equipe reflete sobre o que deu certo e o que pode ser melhorado para a próxima Sprint.

### Burndown Chart:

*(Espaço para o Grafico).*

-----

## Etapa 6 – Teste

Garantir a qualidade do sistema é crucial, e um plano de testes bem definido é o caminho para isso.

### Plano de Teste:

  * **Objetivo:** Validar que o sistema atende a todos os requisitos funcionais e não funcionais, garantindo uma experiência de usuário de alta qualidade.
  * **Escopo:** Todas as funcionalidades descritas no backlog do produto.
  * **Tipos de Teste:**
      * **Teste de Unidade:** Testar os menores componentes do código de forma isolada.
      * **Teste de Integração:** Garantir que os diferentes módulos do sistema funcionam corretamente quando combinados.
      * **Teste de Sistema:** Testar o sistema como um todo, em um ambiente similar ao de produção.
        .
      * **Teste de Usabilidade:** Avaliar a facilidade de uso do sistema com usuários reais.
      * **Teste de Carga e Estresse:** Simular um grande número de usuários acessando o sistema simultaneamente para verificar o desempenho e a estabilidade.
      * **Teste de Segurança:** Identificar e corrigir vulnerabilidades de segurança.
  * **Ferramentas:** Planilhas (Google Sheets, Excel) para documentar os casos de teste, Jira para gestão de bugs, e ferramentas automatizadas como Selenium (para testes de UI) e JMeter (para testes de carga).
-----

### **Casos de Teste para o Sistema LTA**

### **Testes Relacionados ao Espectador (RF01 - RF05)**

  * **RF01: O sistema deve permitir que o Espectador visualize o calendário de jogos.**

      * **CT01:** Verificar a visualização do calendário da semana atual.
          * **Passos:** 1. Acessar a página principal. 2. Clicar no menu "Calendário".
          * **Resultado Esperado:** O sistema exibe os confrontos agendados para a semana corrente, com data, horário e equipes.
      * **CT02:** Verificar o filtro de calendário por Conferência (Norte).
          * **Passos:** 1. Ir para a página "Calendário". 2. Selecionar o filtro "Conferência Norte".
          * **Resultado Esperado:** A lista de jogos é atualizada, mostrando apenas os confrontos da Conferência Norte.
      * **CT03:** Verificar a navegação para semanas anteriores no calendário.
          * **Passos:** 1. Ir para a página "Calendário". 2. Clicar no controle para visualizar a semana anterior.
          * **Resultado Esperado:** O sistema exibe os jogos que ocorreram na semana anterior, com seus respectivos resultados.

  * **RF02: O sistema deve exibir a classificação atualizada das equipes nas conferências Norte e Sul.**

      * **CT04:** Verificar a visualização da tabela de classificação da Conferência Sul.
          * **Passos:** 1. Acessar a página "Classificação". 2. Selecionar a aba "Conferência Sul".
          * **Resultado Esperado:** O sistema exibe a tabela de classificação apenas com as equipes da Conferência Sul, ordenadas por número de vitórias.
      * **CT05:** Verificar se a classificação é atualizada após o registro de um resultado.
          * **Passos:** 1. Anotar a classificação atual. 2. Aguardar o admin registrar o resultado de uma partida. 3. Atualizar a página de classificação.
          * **Resultado Esperado:** A equipe vencedora tem sua contagem de vitórias incrementada, e a perdedora, sua contagem de derrotas. A ordem da tabela é ajustada se necessário.

  * **RF03: O sistema deve permitir assistir às partidas ao vivo e aos VODs.**

      * **CT06:** Verificar o acesso a uma transmissão ao vivo.
          * **Passos:** 1. Acessar a página principal durante um jogo ao vivo. 2. Clicar no banner "Assista Ao Vivo".
          * **Resultado Esperado:** O player de vídeo é carregado e inicia a transmissão ao vivo da partida.
      * **CT07:** Verificar a visualização de um VOD (vídeo de jogo passado).
          * **Passos:** 1. Ir para a página "Calendário". 2. Selecionar uma partida que já ocorreu. 3. Clicar no ícone de "Assistir VOD".
          * **Resultado Esperado:** O player de vídeo é carregado com a gravação completa da partida selecionada.

  * **RF04: O sistema deve apresentar estatísticas detalhadas das partidas, jogadores e equipes.**

      * **CT08:** Verificar a visualização de estatísticas de um jogador específico.
          * **Passos:** 1. Acessar a página "Estatísticas". 2. Clicar na aba "Jogadores". 3. Selecionar um jogador da lista.
          * **Resultado Esperado:** O sistema exibe a página de perfil do jogador com estatísticas como KDA, campeões mais jogados e taxa de vitórias.
      * **CT09:** Verificar as estatísticas de uma partida finalizada.
          * **Passos:** 1. Ir para a página "Calendário". 2. Clicar em uma partida concluída. 3. Acessar a aba "Estatísticas da Partida".
          * **Resultado Esperado:** O sistema exibe os dados detalhados da partida, como ouro total, dragões, barões e estatísticas de cada jogador no confronto.

  * **RF05: O sistema deve permitir que o Espectador configure notificações.**

      * **CT10:** Verificar a ativação de notificação para uma equipe favorita.
          * **Passos:** 1. Acessar a página de uma equipe. 2. Clicar no ícone de "sino" ou "seguir".
          * **Resultado Esperado:** O sistema exibe uma mensagem de confirmação "Você será notificado sobre os jogos desta equipe". O ícone muda para indicar que a notificação está ativa.
      * **CT11:** Verificar o recebimento da notificação de início de partida.
          * **Passos:** 1. Ativar a notificação para uma equipe (CT10). 2. Aguardar o horário de início da partida dessa equipe.
          * **Resultado Esperado:** O usuário (se logado e com permissões ativas) recebe uma notificação push ou um alerta no site informando que a partida começou.

### **Testes Relacionados ao Administrador da Liga (RF06 - RF09)**

  * **RF06: O Administrador da Liga deve poder cadastrar, editar e remover equipes e jogadores.**

      * **CT12:** Verificar o cadastro de uma nova equipe com sucesso.
          * **Passos:** 1. Fazer login como Admin. 2. Acessar o painel "Gerenciar Equipes". 3. Clicar em "Adicionar Nova Equipe". 4. Preencher todos os dados (nome, logo, conferência) e salvar.
          * **Resultado Esperado:** A equipe é criada com sucesso e aparece na lista de equipes do sistema.
      * **CT13:** Verificar a tentativa de cadastro de equipe com dados faltando.
          * **Passos:** 1. Fazer login como Admin. 2. Ir para o cadastro de equipe. 3. Preencher o nome, mas deixar o campo "conferência" em branco e salvar.
          * **Resultado Esperado:** O sistema exibe uma mensagem de erro indicando que o campo "conferência" é obrigatório e não salva o registro.
      * **CT14:** Verificar a edição das informações de um jogador.
          * **Passos:** 1. Fazer login como Admin. 2. Acessar o perfil de uma equipe e selecionar um jogador. 3. Clicar em "Editar". 4. Alterar a função (role) do jogador e salvar.
          * **Resultado Esperado:** A informação do jogador é atualizada no sistema.

  * **RF07: O Administrador da Liga deve poder agendar as partidas do campeonato.**

      * **CT15:** Verificar o agendamento de uma nova partida.
          * **Passos:** 1. Fazer login como Admin. 2. Acessar o painel "Agendar Partidas". 3. Selecionar as duas equipes, data, hora e etapa do campeonato. 4. Salvar.
          * **Resultado Esperado:** A partida é criada e aparece corretamente no calendário público.
      * **CT16:** Verificar a tentativa de agendar uma partida com uma equipe já alocada no mesmo horário.
          * **Passos:** 1. Fazer login como Admin. 2. Tentar agendar uma nova partida para a "Equipe A" em um horário que ela já tem um jogo.
          * **Resultado Esperado:** O sistema exibe um alerta de conflito de agendamento e impede a criação da partida.

  * **RF08: O Administrador da Liga deve poder atualizar os resultados das partidas e as estatísticas.**

      * **CT17:** Verificar a atualização do resultado de uma partida.
          * **Passos:** 1. Fazer login como Admin. 2. Localizar uma partida em andamento ou recém-finalizada no painel. 3. Clicar em "Atualizar Resultado". 4. Definir a "Equipe A" como vencedora e salvar.
          * **Resultado Esperado:** O status da partida muda para "Finalizada" e o resultado é exibido no calendário público.
      * **CT18:** Verificar o input das estatísticas pós-jogo.
          * **Passos:** 1. Fazer login como Admin. 2. Acessar uma partida finalizada. 3. Inserir os dados de KDA para um jogador e salvar.
          * **Resultado Esperado:** As estatísticas inseridas são salvas e exibidas na página de detalhes da partida.

  * **RF09: O Administrador da Liga deve poder publicar notícias e comunicados oficiais.**

      * **CT19:** Verificar a publicação de uma nova notícia.
          * **Passos:** 1. Fazer login como Admin. 2. Acessar o painel "Gerenciar Notícias". 3. Clicar em "Nova Notícia". 4. Inserir título, corpo do texto, imagem e clicar em "Publicar".
          * **Resultado Esperado:** A notícia aparece na seção de notícias do site.
      * **CT20:** Verificar a edição de uma notícia já publicada.
          * **Passos:** 1. Fazer login como Admin. 2. Localizar uma notícia existente. 3. Clicar em "Editar". 4. Alterar o título e salvar.
          * **Resultado Esperado:** O título da notícia é atualizado na página principal.

### **Testes Relacionados ao Gerente de Equipe e Jogadores (RF10 - RF12)**

  * **RF10: O Gerente de Equipe deve poder submeter a escalação de sua equipe para as partidas.**

      * **CT21:** Verificar a submissão de escalação dentro do prazo.
          * **Passos:** 1. Fazer login como Gerente de Equipe. 2. Acessar o painel "Próxima Partida". 3. Selecionar os 5 jogadores titulares e salvar a escalação.
          * **Resultado Esperado:** O sistema confirma o envio da escalação e bloqueia novas edições (ou exibe como "final").
      * **CT22:** Verificar a tentativa de submeter escalação após o prazo.
          * **Passos:** 1. Fazer login como Gerente de Equipe. 2. Tentar acessar a funcionalidade de submissão de escalação após o horário limite definido pelo admin.
          * **Resultado Esperado:** O sistema exibe uma mensagem "O prazo para envio da escalação foi encerrado" e não permite a submissão.

  * **RF11: O Gerente de Equipe deve poder atualizar as informações de perfil dos seus jogadores.**

      * **CT23:** Verificar a atualização da foto de perfil de um jogador.
          * **Passos:** 1. Fazer login como Gerente de Equipe. 2. Acessar a página de gerenciamento da sua equipe. 3. Selecionar um jogador. 4. Fazer o upload de uma nova foto de perfil e salvar.
          * **Resultado Esperado:** A nova foto do jogador é exibida em seu perfil público.
      * **CT24:** Verificar que um Gerente não pode editar jogadores de outra equipe.
          * **Passos:** 1. Fazer login como Gerente da "Equipe A". 2. Tentar navegar pela URL para a página de gerenciamento da "Equipe B".
          * **Resultado Esperado:** O sistema exibe uma mensagem de "Acesso Negado" ou redireciona para a página inicial.

  * **RF12: Jogadores e Membros da Comissão Técnica devem poder visualizar informações internas.**

      * **CT25:** Verificar o acesso de um jogador à área de comunicados da liga.
          * **Passos:** 1. Fazer login com uma conta de jogador. 2. Acessar a seção "Comunicados Internos".
          * **Resultado Esperado:** O jogador consegue visualizar os comunicados que foram publicados pelo Admin para jogadores e equipes.
      * **CT26:** Verificar que um Espectador não consegue acessar a área de comunicados internos.
          * **Passos:** 1. Fazer login com uma conta de Espectador (ou estar deslogado). 2. Tentar acessar a URL da área "Comunicados Internos".
          * **Resultado Esperado:** O sistema redireciona para a página de login ou exibe uma mensagem de erro de permissão.

### **Testes de Regressão e Cenários Adicionais**

  * **CT27 (RF02):** Verificar se a tabela de classificação lida corretamente com empates (ex: duas equipes com 5 vitórias e 2 derrotas), aplicando o critério de desempate correto (ex: confronto direto).
  * **CT28 (RF06):** Verificar a remoção de uma equipe do campeonato, garantindo que ela não apareça mais no calendário e classificação.
  * **CT29 (RF01/RF07):** Verificar se uma partida remarcada pelo Admin reflete a nova data/hora imediatamente no calendário público.
  * **CT30 (RF04):** Verificar se a página de estatísticas gerais do campeonato (ex: jogador com maior KDA, campeão com maior taxa de vitória) é calculada e exibida corretamente.

-----

### **Tabela de Casos de Teste**

| ID do Teste | RF Associado | Título do Teste                                                  | Passos                                                                                                                                                                                                                                                                                                                                                                                                    | Resultado Esperado                                                                                                                                                                                | Status                       |
| :---------- | :----------- | :--------------------------------------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :--------------------------- |
| **CT01** | RF01         | Verificar a visualização do calendário da semana atual.            | 1. Acessar a página principal. \<br\> 2. Clicar no menu "Calendário".                                                                                                                                                                                                                                                                                                                                     | O sistema exibe os confrontos agendados para a semana corrente, com data, horário e equipes.                                                                                                     | (A ser preenchido)           |
| **CT02** | RF01         | Verificar o filtro de calendário por Conferência (Norte).         | 1. Ir para a página "Calendário". \<br\> 2. Selecionar o filtro "Conferência Norte".                                                                                                                                                                                                                                                                                                                      | A lista de jogos é atualizada, mostrando apenas os confrontos da Conferência Norte.                                                                                                               | (A ser preenchido)           |
| **CT03** | RF01         | Verificar a navegação para semanas anteriores no calendário.       | 1. Ir para a página "Calendário". \<br\> 2. Clicar no controle para visualizar a semana anterior.                                                                                                                                                                                                                                                                                                          | O sistema exibe os jogos que ocorreram na semana anterior, com seus respectivos resultados.                                                                                                      | (A ser preenchido)           |
| **CT04** | RF02         | Verificar a visualização da tabela de classificação da Conferência Sul. | 1. Acessar a página "Classificação". \<br\> 2. Selecionar a aba "Conferência Sul".                                                                                                                                                                                                                                                                                                                         | O sistema exibe a tabela de classificação apenas com as equipes da Conferência Sul, ordenadas por número de vitórias.                                                                               | (A ser preenchido)           |
| **CT05** | RF02         | Verificar se a classificação é atualizada após o registro de um resultado. | 1. Anotar a classificação atual. \<br\> 2. Aguardar o admin registrar o resultado de uma partida. \<br\> 3. Atualizar a página de classificação.                                                                                                                                                                                                                                                                     | A equipe vencedora tem sua contagem de vitórias incrementada, e a perdedora, sua contagem de derrotas. A ordem da tabela é ajustada se necessário.                                                     | (A ser preenchido)           |
| **CT06** | RF03         | Verificar o acesso a uma transmissão ao vivo.                       | 1. Acessar a página principal durante um jogo ao vivo. \<br\> 2. Clicar no banner "Assista Ao Vivo".                                                                                                                                                                                                                                                                                                        | O player de vídeo é carregado e inicia a transmissão ao vivo da partida.                                                                                                                          | (A ser preenchido)           |
| **CT07** | RF03         | Verificar a visualização de um VOD (vídeo de jogo passado).         | 1. Ir para a página "Calendário". \<br\> 2. Selecionar uma partida que já ocorreu. \<br\> 3. Clicar no ícone de "Assistir VOD".                                                                                                                                                                                                                                                                                     | O player de vídeo é carregado com a gravação completa da partida selecionada.                                                                                                                     | (A ser preenchido)           |
| **CT08** | RF04         | Verificar a visualização de estatísticas de um jogador específico. | 1. Acessar a página "Estatísticas". \<br\> 2. Clicar na aba "Jogadores". \<br\> 3. Selecionar um jogador da lista.                                                                                                                                                                                                                                                                                           | O sistema exibe a página de perfil do jogador com estatísticas como KDA, campeões mais jogados e taxa de vitórias.                                                                                  | (A ser preenchido)           |
| **CT09** | RF04         | Verificar as estatísticas de uma partida finalizada.             | 1. Ir para a página "Calendário". \<br\> 2. Clicar em uma partida concluída. \<br\> 3. Acessar a aba "Estatísticas da Partida".                                                                                                                                                                                                                                                                                     | O sistema exibe os dados detalhados da partida, como ouro total, dragões, barões e estatísticas de cada jogador no confronto.                                                                       | (A ser preenchido)           |
| **CT10** | RF05         | Verificar a ativação de notificação para uma equipe favorita.    | 1. Acessar a página de uma equipe. \<br\> 2. Clicar no ícone de "sino" ou "seguir".                                                                                                                                                                                                                                                                                                                       | O sistema exibe uma mensagem de confirmação "Você será notificado sobre os jogos desta equipe". O ícone muda para indicar que a notificação está ativa.                                            | (A ser preenchido)           |
| **CT11** | RF05         | Verificar o recebimento da notificação de início de partida.     | 1. Ativar a notificação para uma equipe (CT10). \<br\> 2. Aguardar o horário de início da partida dessa equipe.                                                                                                                                                                                                                                                                                                | O usuário (se logado e com permissões ativas) recebe uma notificação push ou um alerta no site informando que a partida começou.                                                                       | (A ser preenchido)           |
| **CT12** | RF06         | Verificar o cadastro de uma nova equipe com sucesso.             | 1. Fazer login como Admin. \<br\> 2. Acessar o painel "Gerenciar Equipes". \<br\> 3. Clicar em "Adicionar Nova Equipe". \<br\> 4. Preencher todos os dados (nome, logo, conferência) e salvar.                                                                                                                                                                                                                          | A equipe é criada com sucesso e aparece na lista de equipes do sistema.                                                                                                                           | (A ser preenchido)           |
| **CT13** | RF06         | Verificar a tentativa de cadastro de equipe com dados faltando.  | 1. Fazer login como Admin. \<br\> 2. Ir para o cadastro de equipe. \<br\> 3. Preencher o nome, mas deixar o campo "conferência" em branco e salvar.                                                                                                                                                                                                                                                             | O sistema exibe uma mensagem de erro indicando que o campo "conferência" é obrigatório e não salva o registro.                                                                                    | (A ser preenchido)           |
| **CT14** | RF06         | Verificar a edição das informações de um jogador.                | 1. Fazer login como Admin. \<br\> 2. Acessar o perfil de uma equipe e selecionar um jogador. \<br\> 3. Clicar em "Editar". \<br\> 4. Alterar a função (role) do jogador e salvar.                                                                                                                                                                                                                                     | A informação do jogador é atualizada no sistema.                                                                                                                                                  | (A ser preenchido)           |
| **CT15** | RF07         | Verificar o agendamento de uma nova partida.                     | 1. Fazer login como Admin. \<br\> 2. Acessar o painel "Agendar Partidas". \<br\> 3. Selecionar as duas equipes, data, hora e etapa do campeonato. \<br\> 4. Salvar.                                                                                                                                                                                                                                                     | A partida é criada e aparece corretamente no calendário público.                                                                                                                                  | (A ser preenchido)           |
| **CT16** | RF07         | Verificar a tentativa de agendar uma partida com uma equipe já alocada no mesmo horário. | 1. Fazer login como Admin. \<br\> 2. Tentar agendar uma nova partida para a "Equipe A" em um horário que ela já tem um jogo.                                                                                                                                                                                                                                                                         | O sistema exibe um alerta de conflito de agendamento e impede a criação da partida.                                                                                                               | (A ser preenchido)           |
| **CT17** | RF08         | Verificar a atualização do resultado de uma partida.             | 1. Fazer login como Admin. \<br\> 2. Localizar uma partida em andamento ou recém-finalizada no painel. \<br\> 3. Clicar em "Atualizar Resultado". \<br\> 4. Definir a "Equipe A" como vencedora e salvar.                                                                                                                                                                                                                    | O status da partida muda para "Finalizada" e o resultado é exibido no calendário público.                                                                                                         | (A ser preenchido)           |
| **CT18** | RF08         | Verificar o input das estatísticas pós-jogo.                     | 1. Fazer login como Admin. \<br\> 2. Acessar uma partida finalizada. \<br\> 3. Inserir os dados de KDA para um jogador e salvar.                                                                                                                                                                                                                                                                                  | As estatísticas inseridas são salvas e exibidas na página de detalhes da partida.                                                                                                                 | (A ser preenchido)           |
| **CT19** | RF09         | Verificar a publicação de uma nova notícia.                      | 1. Fazer login como Admin. \<br\> 2. Acessar o painel "Gerenciar Notícias". \<br\> 3. Clicar em "Nova Notícia". \<br\> 4. Inserir título, corpo do texto, imagem e clicar em "Publicar".                                                                                                                                                                                                                                   | A notícia aparece na seção de notícias do site.                                                                                                                                                   | (A ser preenchido)           |
| **CT20** | RF09         | Verificar a edição de uma notícia já publicada.                  | 1. Fazer login como Admin. \<br\> 2. Localizar uma notícia existente. \<br\> 3. Clicar em "Editar". \<br\> 4. Alterar o título e salvar.                                                                                                                                                                                                                                                                            | O título da notícia é atualizado na página principal.                                                                                                                                             | (A ser preenchido)           |
| **CT21** | RF10         | Verificar a submissão de escalação dentro do prazo.              | 1. Fazer login como Gerente de Equipe. \<br\> 2. Acessar o painel "Próxima Partida". \<br\> 3. Selecionar os 5 jogadores titulares e salvar a escalação.                                                                                                                                                                                                                                                             | O sistema confirma o envio da escalação e bloqueia novas edições (ou exibe como "final").                                                                                                         | (A ser preenchido)           |
| **CT22** | RF10         | Verificar a tentativa de submeter escalação após o prazo.        | 1. Fazer login como Gerente de Equipe. \<br\> 2. Tentar acessar a funcionalidade de submissão de escalação após o horário limite definido pelo admin.                                                                                                                                                                                                                                                              | O sistema exibe uma mensagem "O prazo para envio da escalação foi encerrado" e não permite a submissão.                                                                                            | (A ser preenchido)           |
| **CT23** | RF11         | Verificar a atualização da foto de perfil de um jogador.         | 1. Fazer login como Gerente de Equipe. \<br\> 2. Acessar a página de gerenciamento da sua equipe. \<br\> 3. Selecionar um jogador. \<br\> 4. Fazer o upload de uma nova foto de perfil e salvar.                                                                                                                                                                                                                            | A nova foto do jogador é exibida em seu perfil público.                                                                                                                                           | (A ser pre-preenchido)       |
| **CT24** | RF11         | Verificar que um Gerente não pode editar jogadores de outra equipe. | 1. Fazer login como Gerente da "Equipe A". \<br\> 2. Tentar navegar pela URL para a página de gerenciamento da "Equipe B".                                                                                                                                                                                                                                                                                     | O sistema exibe uma mensagem de "Acesso Negado" ou redireciona para a página inicial.                                                                                                             | (A ser preenchido)           |
| **CT25** | RF12         | Verificar o acesso de um jogador à área de comunicados da liga.    | 1. Fazer login com uma conta de jogador. \<br\> 2. Acessar a seção "Comunicados Internos".                                                                                                                                                                                                                                                                                                                  | O jogador consegue visualizar os comunicados que foram publicados pelo Admin para jogadores e equipes.                                                                                          | (A ser preenchido)           |
| **CT26** | RF12         | Verificar que um Espectador não consegue acessar a área de comunicados internos. | 1. Fazer login com uma conta de Espectador (ou estar deslogado). \<br\> 2. Tentar acessar a URL da área "Comunicados Internos".                                                                                                                                                                                                                                                                         | O sistema redireciona para a página de login ou exibe uma mensagem de erro de permissão.                                                                                                          | (A ser preenchido)           |
| **CT27** | RF02         | Verificar se a tabela de classificação lida corretamente com empates. | 1. Criar um cenário onde duas equipes têm o mesmo número de vitórias/derrotas. \<br\> 2. Verificar a ordem na tabela de classificação.                                                                                                                                                                                                                                                                              | As equipes são ordenadas de acordo com o critério de desempate pré-definido (ex: confronto direto).                                                                                             | (A ser preenchido)           |
| **CT28** | RF06         | Verificar a remoção de uma equipe do campeonato.                   | 1. Fazer login como Admin. \<br\> 2. Acessar "Gerenciar Equipes". \<br\> 3. Selecionar uma equipe e clicar em "Remover". \<br\> 4. Confirmar a remoção.                                                                                                                                                                                                                                                                     | A equipe removida não deve mais aparecer nas páginas de classificação, calendário ou lista de equipes.                                                                                            | (A ser preenchido)           |
| **CT29** | RF01/RF07    | Verificar se uma partida remarcada reflete no calendário público. | 1. Fazer login como Admin. \<br\> 2. Acessar o calendário e selecionar uma partida futura para editar. \<br\> 3. Alterar a data e/ou hora da partida e salvar. \<br\> 4. Deslogar e acessar o calendário público.                                                                                                                                                                                                               | A partida é exibida no calendário público com a nova data e hora corretas.                                                                                                                        | (A ser preenchido)           |
| **CT30** | RF04         | Verificar a atualização das estatísticas gerais do campeonato.   | 1. Fazer login como Admin e atualizar o resultado de uma partida com estatísticas detalhadas. \<br\> 2. Acessar a página pública de "Estatísticas".                                                                                                                                                                                                                                                               | A página de estatísticas gerais (ex: jogador com maior KDA, campeão com maior taxa de vitória) é atualizada para refletir os novos dados inseridos.                                                 | (A ser preenchido)           |                                                                                    |

-----

### **Casos de Teste para os Requisitos Não Funcionais (RNF)**

Os testes a seguir focam em medir e validar os atributos de qualidade do sistema, como desempenho, usabilidade, segurança, entre outros.

### **Testes Relacionados a Desempenho (RNF01)**

  * **RNF01 (Desempenho):** O sistema deve suportar um alto volume de acessos simultâneos durante as transmissões ao vivo, com tempo de carregamento de página inferior a 2 segundos.
      * **CT-RNF01: Teste de Carga em Páginas Chave.**
          * **Método:** Utilizar ferramentas como Apache JMeter ou LoadRunner para simular 10.000 usuários simultâneos acessando a página da transmissão ao vivo.
          * **Métrica de Sucesso:** O tempo médio de resposta do servidor deve permanecer abaixo de 1.500ms e a taxa de erros deve ser inferior a 1%.
      * **CT-RNF02: Medição do Tempo de Carregamento da Homepage.**
          * **Método:** Utilizar a ferramenta Google Lighthouse ou WebPageTest para analisar a página inicial (`index.html`).
          * **Métrica de Sucesso:** A métrica "Largest Contentful Paint" (LCP) deve ser inferior a 2 segundos em uma conexão 4G padrão.
      * **CT-RNF03: Teste de Estresse (Stress Test).**
          * **Método:** Aumentar progressivamente o número de usuários virtuais no JMeter até que o sistema apresente degradação significativa (aumento do tempo de resposta ou taxa de erros).
          * **Métrica de Sucesso:** O sistema deve se manter funcional até 150% da carga esperada e deve se recuperar automaticamente (voltar aos tempos de resposta normais) após o pico de estresse ser removido.

### **Testes Relacionados a Usabilidade (RNF02)**

  * **RNF02 (Usabilidade):** A interface do sistema deve ser intuitiva e de fácil navegação para todos os tipos de usuários.
      * **CT-RNF04: Teste de Tarefa do Usuário.**
          * **Método:** Recrutar 5 usuários representativos (espectadores) e pedir que executem a tarefa: "Encontre contra quem a equipe 'LOUD' jogou na semana passada e qual foi o placar".
          * **Métrica de Sucesso:** Pelo menos 4 de 5 usuários devem conseguir completar a tarefa em menos de 60 segundos sem ajuda.
      * **CT-RNF05: Avaliação Heurística.**
          * **Método:** Um ou mais especialistas em UX/UI avaliam a interface com base nas 10 Heurísticas de Usabilidade de Nielsen.
          * **Métrica de Sucesso:** O relatório deve identificar os problemas de usabilidade e classificá-los por severidade. O sucesso é a criação do relatório para guiar melhorias.

### **Testes Relacionados a Disponibilidade (RNF03)**

  * **RNF03 (Disponibilidade):** O sistema deve ter uma disponibilidade de 99.8% durante o período do campeonato.
      * **CT-RNF06: Monitoramento de Uptime Contínuo.**
          * **Método:** Configurar um serviço externo (como UptimeRobot ou Pingdom) para verificar a página inicial do sistema a cada 5 minutos, 24/7.
          * **Métrica de Sucesso:** Ao longo de um mês, o tempo total de inatividade registrado não deve exceder o equivalente a 0.2% do período (aprox. 1 hora e 26 minutos).
      * **CT-RNF07: Teste de Recuperação (Failover).**
          * **Método:** Desligar manualmente o servidor web principal em um ambiente de teste que possua um servidor secundário (backup).
          * **Métrica de Sucesso:** O sistema de backup deve assumir o tráfego automaticamente em menos de 1 minuto, sem perda de dados e com mínima ou nenhuma percepção pelo usuário.

### **Testes Relacionados a Segurança (RNF04)**

  * **RNF04 (Segurança):** O sistema deve garantir a segurança dos dados e a integridade das informações, utilizando 2FA para administradores.
      * **CT-RNF08: Teste de Injeção de SQL (SQL Injection).**
          * **Método:** Utilizar uma ferramenta como o SQLMap ou inserir manualmente strings maliciosas (ex: `' OR 1=1 --`) nos campos do formulário de login.
          * **Métrica de Sucesso:** O sistema deve rejeitar a entrada, retornar uma mensagem de erro genérica e não permitir o login ou expor informações do banco de dados.
      * **CT-RNF09: Verificação da Autenticação de Dois Fatores (2FA).**
          * **Método:** Tentar fazer login com uma conta de Administrador.
          * **Métrica de Sucesso:** Após inserir usuário e senha corretos, o sistema deve solicitar um código de 2FA. O login só deve ser bem-sucedido com um código válido. Acesso deve ser negado com um código inválido.
      * **CT-RNF10: Teste de Quebra de Autorização.**
          * **Método:** Fazer login como "Gerente de Equipe" e tentar acessar diretamente a URL do painel de administração (ex: `/admin-agendar.html`).
          * **Métrica de Sucesso:** O sistema deve exibir uma mensagem de "Acesso Negado" ou redirecionar o usuário para uma página de erro autorizada, impedindo o acesso à funcionalidade.

### **Testes Relacionados a Compatibilidade (RNF05)**

  * **RNF05 (Compatibilidade):** O sistema deve ser compatível com os principais navegadores e dispositivos móveis.
      * **CT-RNF11: Teste Cross-Browser.**
          * **Método:** Abrir e navegar pelas 5 páginas principais do site (Início, Calendário, Classificação, Equipes, Notícias) nas versões mais recentes do Google Chrome, Mozilla Firefox e Microsoft Edge em um Desktop.
          * **Métrica de Sucesso:** A aparência e a funcionalidade devem ser consistentes em todos os navegadores, sem quebras de layout ou erros de script.
      * **CT-RNF12: Teste de Responsividade.**
          * **Método:** Utilizar as ferramentas de desenvolvedor do navegador para emular a visualização do site em diferentes tamanhos de tela (ex: iPhone 12, Samsung Galaxy S20, iPad).
          * **Métrica de Sucesso:** O layout deve se adaptar corretamente a cada tela, o texto deve ser legível, e todos os elementos clicáveis devem ser facilmente acessíveis sem a necessidade de zoom ou rolagem horizontal.

-----

### **Tabela de Casos de Teste para RNF**

| ID do Teste  | RNF Associado | Título do Teste                                     | Ferramentas / Método                                                                | Passos / Métrica de Sucesso                                                                                                                                                                   | Status                       |
| :----------- | :------------ | :-------------------------------------------------- | :---------------------------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :--------------------------- |
| **CT-RNF01** | RNF01         | Teste de Carga em Páginas Chave                     | Apache JMeter / LoadRunner                                                          | **Métrica:** Simular 10.000 usuários na página de transmissão. O tempo médio de resposta deve ser \< 1.500ms e a taxa de erros \< 1%.                                                                 | (A ser preenchido)           |
| **CT-RNF02** | RNF01         | Medição do Tempo de Carregamento da Homepage        | Google Lighthouse / WebPageTest                                                     | **Métrica:** A métrica "Largest Contentful Paint" (LCP) da página inicial deve ser \< 2 segundos.                                                                                                | (A ser preenchido)           |
| **CT-RNF03** | RNF01         | Teste de Estresse do Servidor                       | Apache JMeter                                                                       | **Métrica:** O sistema deve operar até 150% da carga esperada e se recuperar automaticamente após o pico.                                                                                       | (A ser preenchido)           |
| **CT-RNF04** | RNF02         | Teste de Tarefa do Usuário                          | Observação de usuários reais                                                        | **Passos:** Pedir para um usuário encontrar o placar do último jogo da "LOUD". \<br\> **Métrica:** 80% dos usuários devem completar a tarefa em \< 60 segundos.                                        | (A ser preenchido)           |
| **CT-RNF05** | RNF02         | Avaliação Heurística da Interface                   | Especialistas em UX/UI, Heurísticas de Nielsen                                      | **Métrica:** Produção de um relatório com problemas de usabilidade classificados por severidade, a ser usado pela equipe de desenvolvimento.                                                        | (A ser preenchido)           |
| **CT-RNF06** | RNF03         | Monitoramento de Uptime Contínuo                    | UptimeRobot / Pingdom                                                               | **Métrica:** O tempo de inatividade registrado em 30 dias não deve exceder 0.2% do período total.                                                                                               | (A ser preenchido)           |
| **CT-RNF07** | RNF03         | Teste de Recuperação (Failover)                     | Simulação de falha em ambiente de teste                                             | **Métrica:** O servidor de backup deve assumir o tráfego em menos de 1 minuto após a falha do servidor principal.                                                                                 | (A ser preenchido)           |
| **CT-RNF08** | RNF04         | Teste de Injeção de SQL (SQL Injection)             | SQLMap / Teste manual                                                               | **Passos:** Inserir strings maliciosas no formulário de login. \<br\> **Métrica:** O sistema deve barrar a tentativa sem expor dados.                                                              | (A ser preenchido)           |
| **CT-RNF09** | RNF04         | Verificação da Autenticação de Dois Fatores (2FA)   | Teste funcional manual                                                              | **Passos:** Fazer login como Admin. \<br\> **Métrica:** O sistema DEVE exigir um código de 2FA e SÓ DEVE permitir acesso com um código válido.                                                       | (A ser preenchido)           |
| **CT-RNF10** | RNF04         | Teste de Quebra de Autorização                      | Teste funcional manual                                                              | **Passos:** Fazer login como "Gerente" e tentar acessar a URL `/admin-agendar.html`. \<br\> **Métrica:** O sistema deve impedir o acesso e exibir uma página de erro de permissão.                    | (A ser preenchido)           |
| **CT-RNF11** | RNF05         | Teste Cross-Browser                                 | Navegadores: Chrome, Firefox, Edge                                                  | **Passos:** Navegar pelas 5 páginas principais em cada navegador. \<br\> **Métrica:** Layout e funcionalidades devem ser idênticos e sem erros.                                                      | (A ser preenchido)           |
| **CT-RNF12** | RNF05         | Teste de Responsividade                             | Ferramentas de desenvolvedor do navegador (emulação)                                | **Passos:** Visualizar o site em viewports de celular, tablet e desktop. \<br\> **Métrica:** O layout deve se adaptar sem quebras ou rolagem horizontal.                                               | (A ser preenchido)           |