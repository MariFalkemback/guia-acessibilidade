# <h1 id="roteiros">Roteiros de Testes</h1>

Para facilitar o processo de testes, os roteiros são organizados por ambiente — web (desktop), web móvel e aplicativos nativos — e apresentam instruções claras sobre como executar cada verificação, quais critérios das WCAG são aplicáveis e orientam sobre o registro padronizado de falhas de acessibilidade.

Essa sistematização permite maior consistência nos testes manuais e automatizados, além de orientar as equipes de desenvolvimento na identificação e resolução de problemas. 

Os testes cobrem pontos críticos como componentes dinâmicos, validação de formulários, feedback visual e auditivo, navegação por regiões (landmarks), uso correto de modais, estrutura semântica, acessibilidade de vídeos, dimensionamento responsivo e tamanho de áreas clicáveis. 

A seguir, são apresentados os roteiros organizados por tipo de ambiente:

•	**Testes para Web (Desktop)**: Focados na navegação por teclado, uso de leitores de tela, contraste de cores, estrutura semântica e interatividade.

•	**Testes para Mobile Web / WebView**: Adaptação dos critérios de desktop para ambientes móveis, com ênfase em navegação por gestos e compatibilidade com leitores de tela nativos.

•	**Testes para Aplicativos Nativos (Android / iOS)**: Avaliação de propriedades específicas de acessibilidade em componentes nativos, como contentDescription e accessibilityLabel, além da navegação por gestos e foco de tela.

Esses roteiros não substituem testes com usuários reais, mas servem como base técnica estruturada para validação contínua da acessibilidade durante o ciclo de desenvolvimento.

## Testes para Web (Desktop)



| ITEM DO TESTE                          | COMO TESTAR                                                                                               | WCAG Aplicável   | OBSERVAÇÕES (Texto Padrão para Registro de Erro)                                            |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------|:-----------------|:------------------------------------------------------------------------------------------|
| A ordem de leitura dos elementos está lógica?         | Navegar com setas direcionais, Tab, H, U, V (leitor de tela).                                             | 1.3.2, 2.4.3     | Descrever elementos que são lidos em uma ordem ilógica ou inesperada.                     |
| Campos de formulário possuem rótulos acessíveis?       | Navegar com leitor de tela por formulários.                                                               | 1.1.1, 1.3.1     | Listar campos sem rótulo visível ou programático (rótulo associado via código).           |
| Imagens têm texto alternativo (alt) adequado?    | Passar o cursor com leitor de tela sobre as imagens.                                                      | 1.1.1            | Listar imagens sem descrição textual alternativa ou com descrições inadequadas.           |
| O contraste de cores é adequado?                     | Testar com Colour Contrast Analyser.                                                                      | 1.4.3            | Listar textos com contraste insuficiente em relação à cor de fundo.                       |
| A navegação por teclado funciona?                 | Navegar utilizando as teclas Tab e Shift+Tab.                                                             | 2.1.1            | Identificar elementos da interface que não são acessíveis ou navegáveis via teclado.      |
| O foco é visível na navegação por teclado?                           | Observar o indicador de foco ao navegar com o teclado.                                                    | 2.4.7            | Listar elementos interativos que não apresentam um indicador de foco visível.             |
| Há mudança inesperada de contexto?                    | Interagir com menus, botões e formulários.                                                                | 3.2.2            | Listar mudanças inesperadas de contexto ao interagir com elementos da interface.          |
| Links são descritivos?                      | Navegar com atalho de links (atalho 'U' no NVDA, rotor no VoiceOver).                                     | 2.4.4            | Listar links com texto genérico como “clique aqui”, que não fornecem contexto.            |
| Títulos são informativos e bem estruturados?                   | Verificar a estrutura de títulos com atalho 'H' (headings) no leitor de tela.                             | 2.4.2            | Listar páginas ou seções sem títulos claros e descritivos.                                |
| Campos obrigatórios são indicados corretamente?                    | Tentar submeter formulários sem preencher campos obrigatórios.                                            | 3.3.1            | Listar campos obrigatórios sem indicação clara ou com mensagens de erro inacessíveis.     |
| Componentes dinâmicos são acessíveis?       | Inspecionar com leitor de tela se carrosséis, abas e menus possuem rótulo programático.                    | 4.1.2, 1.3.1     | Indicar componentes dinâmicos sem nome ou com nome genérico que não descreve sua função.  |
| A validação de campos de entrada é acessível?         | Inserir dados incorretos e verificar se as mensagens de erro são anunciadas por leitores de tela.         | 3.3.1, 3.3.3     | Informar se as mensagens de erro não são acessíveis ou não são anunciadas por leitores de tela. |
| Mudanças visuais são anunciadas por leitores de tela?            | Verificar se atualizações em tempo real (e.g., status de carregamento) são lidas por leitores de tela.    | 4.1.3, ARIA Live | Indicar mudanças na interface que não são percebidas por tecnologias assistivas.           |
| A navegação por região (landmarks) funciona?       | Usar atalhos de navegação por regiões (e.g., rotor do VoiceOver ou tecla 'R' no NVDA).                   | 1.3.1, 2.4.1     | Informar páginas sem landmarks ou com uso inadequado que dificulta a navegação.           |
| O foco em modais (popups) é automático e fechável?                | Abrir um modal e verificar se o foco é automaticamente transferido para ele e se pode ser fechado com a tecla Esc. | 2.4.3, 2.4.7, 3.2.1 | Informar modais que não recebem o foco na abertura ou que não podem ser fechados via teclado. |
| Elementos têm nome e função programáticos?            | Inspecionar elementos interativos com ferramentas como o Accessibility Tree.                              | 4.1.2            | Listar elementos sem acessibilidade semântica (sem nome, papel ou valor programático).    |
| Existe bypass para blocos repetitivos?           | Verificar a existência de um link "Pular para o Conteúdo Principal" ou similar.                           | 2.4.1            | Indicar ausência de um atalho para pular blocos de conteúdo repetitivos.                 |
| Conteúdo audiovisual é acessível?         | Verificar vídeos incorporados e seus recursos de acessibilidade.                                          | 1.2.2, 1.2.1     | Listar vídeos sem legendas, transcrições ou outras alternativas de acessibilidade.        |
| O layout é resiliente a zoom e fontes grandes?    | Aumentar o zoom (até 200%) ou usar fontes grandes no navegador.                                           | 1.4.4            | Informar se elementos se sobrepõem, desaparecem ou quebram o layout.                     |
| O tamanho das áreas clicáveis é suficiente?             | Clicar com o botão direito no elemento e selecionar "Inspecionar". Deve têr pelo menos 44x44 px                                     | 2.5.5  | Indicar alvos de toque ou clique que são muito pequenos.                                  |

## Testes para Mobile Web / WebView

Os testes realizados para Web (Desktop) também podem ser aplicados ao ambiente mobile, desde que sejam feitas adaptações específicas para suas particularidades. No contexto móvel, a atenção deve se concentrar em aspectos como:

•	**A navegação por gestos, como deslizar o dedo ou realizar toques múltiplos na tela;**

•	**O uso de leitores de tela nativos, como o TalkBack no sistema Android e o VoiceOver no iOS;**

•	**A verificação do comportamento do foco em elementos interativos, como campos de formulário, botões, links e imagens;**

•	**A confirmação de que todos os componentes da interface respondem corretamente ao toque e fornecem retorno auditivo apropriado por meio das tecnologias assistivas.**


Esses ajustes garantem que a experiência do usuário em dispositivos móveis seja tão acessível quanto em ambientes de desktop.

| ITEM DO TESTE                                     | COMO TESTAR                                                                                               | WCAG Aplicável | OBSERVAÇÕES (Texto Padrão para Registro de Erro)                                            |
| :------------------------------------------------ | :---------------------------------------------------------------------------------------------------------- | :------------- | :------------------------------------------------------------------------------------------ |
| **A navegação por gestos funciona corretamente?** | Deslizar o dedo, realizar toques múltiplos e outros gestos nativos do sistema.                              | 2.1.1          | Relatar elementos que não respondem aos gestos ou causam navegação confusa.                 |
| **O uso de leitores de tela nativos é compatível?** | Ativar TalkBack (Android) ou VoiceOver (iOS) e interagir com a interface.                                   | 2.1.1, 4.1.2   | Indicar problemas de leitura ou reconhecimento de elementos pelos leitores de tela.         |
| **O comportamento do foco em elementos interativos é adequado?** | Verificar a ordem do foco ao interagir com campos, botões, links e imagens.                               | 2.4.3, 2.4.7   | Informar quando o foco pula, desaparece ou não segue uma ordem lógica.                     |
| **Componentes da interface respondem corretamente ao toque?** | Tocar em botões, links, campos e verificar feedback visual e auditivo.                                    | 2.5.2          | Listar elementos que não respondem ao toque ou não fornecem feedback apropriado.           |
| **Áreas clicáveis são grandes o suficiente para toque?** | Clicar com o botão direito no elemento e selecionar "Inspecionar". Deve têr pelo menos 44x44 px                                  | 2.5.5          | Indicar alvos de toque muito pequenos que dificultam a interação.                           |
| **O layout se adapta bem a diferentes orientações de tela?** | Girar o dispositivo entre modo retrato e paisagem para verificar a adaptação do conteúdo.                  | 1.3.4          | Informar quando o layout se quebra ou o conteúdo se torna inacessível na mudança de orientação. |
| **O uso da meta viewport é adequado?** | Inspecionar o código para verificar a meta tag `viewport` e seu `user-scalable`.                          | 1.4.4          | Relatar quando o zoom do usuário é desabilitado ou a escala inicial é muito pequena.        |

## Testes para Aplicativos Nativos (Android / iOS)

Com o crescimento do uso de dispositivos móveis, os aplicativos nativos tornaram-se uma das principais formas de acesso a serviços digitais. Por esse motivo, garantir a acessibilidade nesses ambientes é tão fundamental quanto na web. 

Diferentemente da web, os aplicativos nativos utilizam componentes e bibliotecas específicas de cada sistema operacional, como Android e iOS. Por isso, os testes de acessibilidade devem considerar aspectos próprios dessas plataformas, incluindo a verificação das propriedades de acessibilidade dos elementos, a correta navegação por gestos com leitores de tela ativados, e o comportamento do foco ao abrir telas e componentes dinâmicos.

De acordo com as Diretrizes de Acessibilidade para Conteúdo Web (WCAG) — aplicáveis também a aplicativos móveis por meio de sua extensão conceitual —, é essencial que elementos interativos tenham rótulos programáticos (labels), que o foco de navegação siga uma ordem lógica e que a experiência com leitores de tela seja fluida e compreensível.

A avaliação de acessibilidade em aplicativos nativos exige atenção a aspectos específicos da interface e do comportamento dos componentes em ambientes móveis. Esses testes devem garantir que os elementos da aplicação estejam devidamente rotulados, que a navegação por gestos seja funcional, que o agrupamento de elementos respeite a lógica visual e semântica da interface, e que o foco seja posicionado de maneira previsível ao iniciar uma nova tela.

Os itens a seguir representam pontos críticos no uso de tecnologias assistivas, como TalkBack (Android) e VoiceOver (iOS). Quando essas práticas não são observadas, usuários com deficiência visual, por exemplo, podem enfrentar dificuldades severas para compreender o conteúdo, identificar botões e navegar entre seções do aplicativo.

| **ITEM DO TESTE**                         | **COMO TESTAR**                                                                                       | **WCAG APLICÁVEL**            | **OBSERVAÇÕES (Texto Padrão para Registro de Erro)**                                                                |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Labels programáticos estão presentes?                      | Verificar se os elementos possuem `contentDescription` (Android) ou `accessibilityLabel` (iOS).       | 1.1.1                         | Indicar botões, imagens ou ícones sem descrição acessível ou com nome genérico.                                     |
| A navegação por gestos funciona?                      | Ativar TalkBack ou VoiceOver e navegar com gestos nativos.                                            | 2.1.1                         | Relatar elementos que não respondem aos gestos ou são ignorados pelo leitor de tela.                                |
| O agrupamento semântico está correto?             | Explorar a tela com leitor de tela e verificar se elementos relacionados são lidos juntos.             | 1.3.1                         | Informar quando elementos visualmente agrupados são lidos fora de contexto ou de forma isolada.                     |
| O foco  é coerente ao abrir uma tela?           | Abrir uma nova tela e verificar se o foco começa em um título ou campo relevante.                     | 2.4.3                         | Informar telas em que o foco começa em áreas neutras ou fora do conteúdo principal.                                 |
| Há feedback em componentes interativos?      | Interagir com botões, campos ou menus e verificar se o feedback é percebido pelo leitor de tela.       | 4.1.2, 4.1.3                  | Indicar ausência de retorno auditivo ao interagir com elementos importantes da interface.                           |
| Elementos clicáveis têm área adequada?      | Clicar com o botão direito no elemento e selecionar "Inspecionar". Deve têr pelo menos 44x44 px.                                               | 2.5.5                         | Listar elementos difíceis de tocar por serem muito pequenos ou com espaçamento insuficiente.                        |
| Elementos não acessíveis são ocultados?    | Verificar se itens puramente visuais são ignorados por leitores de tela.                             | 1.1.1, 1.3.1                  | Relatar quando imagens decorativas são lidas ou elementos não interativos recebem foco indevido.                   |
| CCampos com erro informam o usuário?          | Inserir dados inválidos e verificar se a mensagem de erro é lida pelo leitor de tela.                 | 3.3.1, 3.3.3                  | Informar quando mensagens de erro não são lidas ou visíveis apenas visualmente.                                     |
| A leitura do título da tela funciona?                 | Ao abrir a tela, verificar se o título é anunciado corretamente pelo leitor de tela.                   | 2.4.2                         | Listar telas que não têm título ou cujo título não é anunciado ao abrir.                                            |
| Transições e atualizações são anunciadas?  | Verificar se mudanças de status (ex: carregando, enviado com sucesso) são lidas em tempo real.        | 4.1.3, ARIA Live              | Indicar mudanças visuais não anunciadas, como status ou atualizações de conteúdo.                                  |


A tabela a seguir resume os principais testes recomendados, servindo como checklist funcional para auditorias internas de acessibilidade digital:

| ITEM DO TESTE                               | COMO TESTAR                                                                                                | DIRETRIZ WCAG / Relevância | TEXTO PADRÃO                                            |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------------------|:-------------|:--------------------------------------------------------|
| Componentes dinâmicos têm nome acessível?   | Inspecionar com leitor de tela se carrosséis, abas, menus têm rótulo.                                      | 4.1.2, 1.3.1 | Indicar componentes sem nome ou com nome genérico.      |
| Campos de entrada possuem validação acessível? | Inserir dados errados e verificar se mensagens de erro são lidas.                                          | 3.3.1, 3.3.3 | Informar se as mensagens não são anunciadas por leitores. |
| Mudanças visuais são também anunciadas?     | Verificar se atualizações em tempo real (ex: status de carregamento) são lidas.                            | 4.1.3, ARIA Live | Indicar mudanças não percebidas pelo leitor de tela.    |
| Navegação por região (landmarks) funciona corretamente? | Usar atalhos de navegação por regiões (ex: rotor do VoiceOver ou tecla R no NVDA).                        | 1.3.1, 2.4.1 | Informar páginas sem landmarks ou com uso inadequado.   |
| Modal (popup) é focado automaticamente e fecha com Esc? | Abrir modal e verificar foco, e se o Esc o fecha.                                                          | 2.4.3, 2.4.7, 3.2.1 | Informar modais que não recebem foco ou não são fecháveis. |
| Todos os elementos têm nome e função programáticos? | Inspecionar elementos interativos com ferramenta como o Accessibility Tree.                                | 4.1.2        | Listar elementos sem acessibilidade semântica.          |
| Existe bypass de blocos repetitivos?        | Verificar se existe link de pular para o conteúdo principal.                                               | 2.4.1        | Indicar ausência de atalho para o conteúdo principal.   |
| Conteúdo audiovisual possui legendas ou transcrição? | Verificar vídeos incorporados e seus recursos de acessibilidade.                                           | 1.2.2, 1.2.1 | Listar vídeos sem legendas ou alternativas.             |
| Tamanhos de fonte e zoom não quebram layout? | Aumentar zoom (até 200%) ou usar fontes grandes no navegador.                                              | 1.4.4        | Informar se elementos se sobrepõem ou somem.            |
| Áreas clicáveis têm tamanho suficiente?     | Clicar com o botão direito no elemento e selecionar "Inspecionar". Deve têr pelo menos 44x44 px                                               | 2.5.5  | Indicar alvos de toque muito pequenos.                  |