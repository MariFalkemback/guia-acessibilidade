# <h1 id="roteiros">Roteiros de Testes</h1>

A realização de testes de acessibilidade é uma etapa essencial para garantir que aplicações digitais possam ser utilizadas por todos, independentemente de limitações físicas, sensoriais ou cognitivas. 

Esses testes devem seguir roteiros bem definidos que cubram os principais aspectos de interação, navegação, percepção e compreensão da interface, conforme orientado pelas Diretrizes de Acessibilidade para Conteúdo Web (WCAG).

Para facilitar esse processo, os roteiros de teste são organizados por ambiente, abrangendo plataformas web (desktop e mobile), aplicativos móveis e documentos em formato PDF, com instruções claras sobre como executar cada verificação, os critérios das WCAG aplicáveis e como registrar falhas de acessibilidade com base em observações padronizadas.

Essa sistematização permite maior consistência nos testes manuais e automatizados, além de orientar as equipes de desenvolvimento na identificação e resolução de problemas. 
A seguir, são apresentados os roteiros organizados por tipo de ambiente:

•	**Testes para Web (Desktop)**: Focados na navegação por teclado, uso de leitores de tela, contraste de cores, estrutura semântica e interatividade.

•	**Testes para Mobile  e Mobile Web / WebView**: Adaptação dos critérios de desktop para ambientes móveis, com ênfase em navegação por gestos e compatibilidade com leitores de tela nativos.

•	**Testes para PDF**: Testes de estrutura semântica, leitura por tecnologias assistivas, ordem de leitura, idioma e interatividade via teclado.

Esses roteiros não substituem testes com usuários reais, mas servem como base técnica estruturada para validação contínua da acessibilidade durante o ciclo de desenvolvimento.

## Testes para Web (Desktop)

A tabela a seguir apresenta os roteiros de testes de acessibilidade aplicáveis ao ambiente Web (Desktop):

| ITEM DO TESTE | COMO TESTAR | WCAG Aplicável | OBSERVAÇÕES (Texto Padrão para Registro de Erro) |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------|:-----------------|:------------------------------------------------------------------------------------------|
| O idioma da página está definido corretamente? | Verificar se o atributo lang está presente no HTML (ex: <html lang="pt-BR">) | 3.1.1  | Informar páginas sem definição de idioma, dificultando a leitura por leitores de tela. |
| Idioma de partes diferentes está indicado? | Verificar se palavras/frases em outros idiomas têm lang específico (ex: lang="en") | 3.1.2 | Indicar trechos com outro idioma sem marcação adequada. |
| É possível parar, pausar ou ocultar conteúdo em movimento? | Verificar sliders/carrosséis automáticos, banners animados, vídeos em loop | 2.2.2 | Informar se não há controles visíveis para pausar conteúdo em movimento. |
| Há controle de volume para áudio reproduzido automaticamente? | Verificar se áudios têm controles ou podem ser pausados | 1.4.2 | Indicar áudios que iniciam sozinhos e não podem ser pausados ou silenciados. |
| O conteúdo responde corretamente ao uso apenas do teclado (sem mouse)? | Tentar realizar todas as interações usando apenas o teclado | 2.1.2, 2.1.4 | Listar funções inacessíveis ou ativadas indevidamente por teclas únicas. |
| Há feedback visual para ações que afetam o conteúdo (ex: envio de formulário)? | Submeter formulários, interagir com botões e aguardar resposta visual ou sonora | 3.2.1, 4.1.3 | Listar interações sem retorno visual ou auditivo. |
| Os campos possuem instruções e sugestões de correção em caso de erro? | Testar formulários com dados incorretos | 3.3.2, 3.3.3 | Informar campos que não oferecem ajuda ou sugestões de correção. |
| A navegação não depende exclusivamente de cores? | Verificar botões, gráficos, indicadores | 1.4.1 | Indicar elementos cuja única diferenciação é cor (ex: "botão verde para continuar"). |
| Há informações sensoriais dependentes apenas de visão ou audição? | Observar orientações como "clique no botão vermelho" ou "ouça o alerta" | 1.3.3 | Apontar instruções que não tenham alternativas acessíveis para todos os sentidos. |
| Elementos com foco ou ponteiro revelam conteúdo visível e acessível? | Navegar com teclado/mouse e verificar tooltips, menus suspensos, popups | 1.4.13 | Indicar conteúdos ocultos que não aparecem ou não são acessíveis via teclado. |
| Há título claro na aba ou topo da página? | Verificar se o title do HTML representa bem o conteúdo | 2.4.2 | Indicar páginas com título genérico ou ausente. |
| Elementos interativos têm o mesmo rótulo visual e programático? | Verificar se botão visível como "Enviar" também é lido como "Enviar" pelo leitor | 2.5.3 | Listar botões cuja label visual e label semântico não correspondem. |
| O sistema previne erros críticos antes da submissão (financeiro, dados sensíveis)? | Simular envio de formulário com dados relevantes (ex: pagamento, matrícula) | 3.3.4 | Indicar falta de revisão/confirmação antes de ações críticas. |
| Existem elementos piscando mais de 3x por segundo? | Observar banners, gifs, sliders, animações | 2.3.1 | Indicar elementos com flash perigoso (risco de convulsão). |
| Há instruções claras sem depender exclusivamente de localização visual? | Verificar se há instruções do tipo "veja no canto direito" sem apoio de ícone/texto | 1.3.3 | Indicar instruções que dependem apenas de localização visual. |
| Informações são agrupadas de forma lógica? | Observar se formulários e seções têm agrupamentos coerentes com headings ou fieldsets | 1.3.1 | Informar se campos ou conteúdos relacionados não estão agrupados semanticamente. |
| A ordem de leitura dos elementos está lógica? | Navegar com setas direcionais, Tab, H, U, V (leitor de tela). | 1.3.2, 2.4.3 | Descrever elementos que são lidos em uma ordem ilógica ou inesperada. |
| Campos de formulário possuem rótulos acessíveis? | Navegar com leitor de tela por formulários. | 1.1.1, 1.3.1 | Listar campos sem rótulo visível ou programático (rótulo associado via código). |
| Imagens têm texto alternativo (alt) adequado? | Passar o cursor com leitor de tela sobre as imagens. | 1.1.1 | Listar imagens sem descrição textual alternativa ou com descrições inadequadas. |
| O contraste de cores é adequado? | Testar com Colour Contrast Analyser. | 1.4.3 | Listar textos com contraste insuficiente em relação à cor de fundo. |
| A navegação por teclado funciona? | Navegar utilizando as teclas Tab e Shift+Tab. | 2.1.1 | Identificar elementos da interface que não são acessíveis ou navegáveis via teclado. |
| O foco é visível na navegação por teclado? | Observar o indicador de foco ao navegar com o teclado. | 2.4.7 | Listar elementos interativos que não apresentam um indicador de foco visível. |
| Há mudança inesperada de contexto? | Interagir com menus, botões e formulários. | 3.2.2 | Listar mudanças inesperadas de contexto ao interagir com elementos da interface. |
| Links são descritivos? | Navegar com atalho de links (atalho 'U' no NVDA, rotor no VoiceOver). | 2.4.4 | Listar links com texto genérico como “clique aqui”, que não fornecem contexto. |
| Títulos são informativos e bem estruturados? | Verificar a estrutura de títulos com atalho 'H' (headings) no leitor de tela. | 2.4.2 | Listar páginas ou seções sem títulos claros e descritivos. |
| Campos obrigatórios são indicados corretamente? | Tentar submeter formulários sem preencher campos obrigatórios. | 3.3.1 | Listar campos obrigatórios sem indicação clara ou com mensagens de erro inacessíveis. |
| Componentes dinâmicos são acessíveis? | Inspecionar com leitor de tela se carrosséis, abas e menus possuem rótulo programático. | 4.1.2, 1.3.1 | Indicar componentes dinâmicos sem nome ou com nome genérico que não descreve sua função. |
| A validação de campos de entrada é acessível? | Inserir dados incorretos e verificar se as mensagens de erro são anunciadas por leitores de tela. | 3.3.1, 3.3.3 | Informar se as mensagens de erro não são acessíveis ou não são anunciadas por leitores de tela. |
| Mudanças visuais são anunciadas por leitores de tela? | Verificar se atualizações em tempo real (e.g., status de carregamento) são lidas por leitores de tela. | 4.1.3 | Indicar mudanças na interface que não são percebidas por tecnologias assistivas. |
| A navegação por região (landmarks) funciona? | Usar atalhos de navegação por regiões (e.g., rotor do VoiceOver ou tecla 'R' no NVDA). | 1.3.1, 2.4.1 | Informar páginas sem landmarks ou com uso inadequado que dificulta a navegação. |
| O foco em modais (popups) é automático e fechável? | Abrir um modal e verificar se o foco é automaticamente transferido para ele e se pode ser fechado com a tecla Esc. | 2.4.3, 2.4.7, 3.2.1 | Informar modais que não recebem o foco na abertura ou que não podem ser fechados via teclado. |
| Elementos têm nome e função programáticos? | Inspecionar elementos interativos com ferramentas como o Accessibility Tree. | 4.1.2 | Listar elementos sem acessibilidade semântica (sem nome, papel ou valor programático). |
| Existe bypass para blocos repetitivos? | Verificar a existência de um link "Pular para o Conteúdo Principal" ou similar. | 2.4.1 | Indicar ausência de um atalho para pular blocos de conteúdo repetitivos. |
| Conteúdo audiovisual é acessível? | Verificar vídeos incorporados e seus recursos de acessibilidade. | 1.2.2, 1.2.1 | Listar vídeos sem legendas, transcrições ou outras alternativas de acessibilidade. |
| O layout é resiliente a zoom e fontes grandes? | Aumentar o zoom (até 200%) ou usar fontes grandes no navegador. | 1.4.4 | Informar se elementos se sobrepõem, desaparecem ou quebram o layout. |
| O tamanho das áreas clicáveis é suficiente? | Clicar com o botão direito no elemento e selecionar "Inspecionar". Deve têr pelo menos 44x44 px | 2.5.5 | Indicar alvos de toque ou clique que são muito pequenos. |

## Testes para Aplicativos Mobile e Mobile Web / WebView

Os testes realizados para Web (Desktop) também podem ser aplicados ao ambiente mobile, desde que sejam feitas adaptações específicas para suas particularidades. No contexto móvel, a atenção deve se concentrar em aspectos como:

•	**A navegação por gestos, como deslizar o dedo ou realizar toques múltiplos na tela;**

•	**O uso de leitores de tela nativos, como o TalkBack no sistema Android e o VoiceOver no iOS;**

•	**A verificação do comportamento do foco em elementos interativos, como campos de formulário, botões, links e imagens;**

•	**A confirmação de que todos os componentes da interface respondem corretamente ao toque e fornecem retorno auditivo apropriado por meio das tecnologias assistivas.**


Esses ajustes garantem que a experiência do usuário em dispositivos móveis seja tão acessível quanto em ambientes de desktop.

A tabela a seguir apresenta os roteiros de testes de acessiblidade para ambiente mobile:

| ITEM DO TESTE                                     | COMO TESTAR                                                                                               | WCAG Aplicável | OBSERVAÇÕES (Texto Padrão para Registro de Erro)                                            |
| :------------------------------------------------ | :---------------------------------------------------------------------------------------------------------- | :------------- | :------------------------------------------------------------------------------------------ |
| A navegação por gestos funciona corretamente?| Deslizar o dedo, realizar toques múltiplos e outros gestos nativos do sistema.                              | 2.1.1          | Relatar elementos que não respondem aos gestos ou causam navegação confusa.                 |
| O uso de leitores de tela nativos é compatível? | Ativar TalkBack (Android) ou VoiceOver (iOS) e interagir com a interface.                                   | 2.1.1, 4.1.2   | Indicar problemas de leitura ou reconhecimento de elementos pelos leitores de tela.         |
| O comportamento do foco em elementos interativos é adequado? | Verificar a ordem do foco ao interagir com campos, botões, links e imagens.                               | 2.4.3, 2.4.7   | Informar quando o foco pula, desaparece ou não segue uma ordem lógica.                     |
| Componentes da interface respondem corretamente ao toque? | Tocar em botões, links, campos e verificar feedback visual e auditivo.                                    | 2.5.2          | Listar elementos que não respondem ao toque ou não fornecem feedback apropriado.           |
| Áreas clicáveis são grandes o suficiente para toque? | Inspecionar o elemento nas ferramentas de desenvolvedor do navegador/emulador para verificar dimensões, garantindo pelo menos 44x44 pixels. | 2.5.5          | Indicar alvos de toque muito pequenos que dificultam a interação.                           |
| O layout se adapta bem a diferentes orientações de tela? | Girar o dispositivo entre modo retrato e paisagem para verificar a adaptação do conteúdo.                  | 1.3.4          | Informar quando o layout se quebra ou o conteúdo se torna inacessível na mudança de orientação. |
| O uso da meta viewport é adequado? | Inspecionar o código para verificar a meta tag `viewport` e se `user-scalable=no` não está presente.         | 1.4.4          | Relatar quando o zoom do usuário é desabilitado ou a escala inicial é muito pequena.        |
| Há descrição para conteúdo não textual em Mobile Web? | Navegar com leitor de tela para verificar se imagens, ícones e gráficos têm texto alternativo descritivo. | 1.1.1          | Listar elementos não textuais sem descrição acessível ou com descrições inadequadas.        |
| Conteúdos apenas áudio/vídeo pré-gravados possuem alternativas? | Verificar se vídeos e áudios pré-gravados têm legendas, transcrições ou audiodescrição.          | 1.2.1, 1.2.2, 1.2.3, 1.2.5 | Indicar ausência de legendas, transcrições ou audiodescrições para mídias pré-gravadas.    |
| A utilização de cores é o único meio de transmitir informação? | Observar se a cor é o único recurso para indicar status, ações ou diferenciar elementos importantes. | 1.4.1          | Relatar quando a informação crucial depende exclusivamente da cor, sem alternativa textual ou de ícone. |
| O contraste de cores do conteúdo é suficiente? | Usar ferramentas de análise de contraste (ex: Colour Contrast Analyser) no navegador do dispositivo/emulador. | 1.4.3, 1.4.11  | Listar textos ou elementos gráficos importantes com contraste insuficiente em relação ao fundo. |
| O conteúdo pode ser pausado, parado ou ocultado? | Verificar se carrosséis, animações ou conteúdos com limite de tempo podem ser controlados pelo usuário. | 2.2.2          | Informar elementos que se movem, piscam ou rolam automaticamente sem opção de pausa/parada. |
| Há atalho para pular blocos repetitivos (Mobile)? | Verificar a existência e funcionalidade de links "Pular para o Conteúdo Principal" ou similar. | 2.4.1          | Indicar ausência de um atalho para pular blocos de conteúdo repetitivos, especialmente em interfaces com muitos elementos fixos. |
| Links e botões têm finalidade clara no contexto? | Navegar com leitor de tela e verificar se o texto de links e botões é descritivo, sem termos genéricos como "clique aqui". | 2.4.4, 2.4.6   | Listar links ou botões com texto genérico, que não indicam sua função sem o contexto visual. |
| Elementos com movimento respondem a gestos de ponteiro? | Interagir com elementos que controlam movimentos (ex: sliders, carrosséis) usando gestos de toque únicos. | 2.5.1          | Informar quando gestos mais complexos são exigidos onde um único toque seria suficiente.    |
| Há opção de cancelar ou reverter ações de ponteiro? | Realizar ações de arrastar e soltar ou toques longos e verificar se há opção de cancelar antes da conclusão. | 2.5.2          | Relatar ações que são ativadas na *pressão inicial* do toque e não na liberação.           |
| Rótulos visíveis correspondem ao nome programático? | Usar leitor de tela para verificar se o texto visível de um componente é lido de forma consistente com seu nome acessível. | 2.5.3          | Indicar inconsistência entre o rótulo visível e o nome programático lido pelo leitor de tela. |
| Funcionalidades por movimento têm alternativa? | Se o aplicativo usa movimentos (ex: agitar para desfazer), verificar se há uma alternativa via interface. | 2.5.4          | Relatar quando funcionalidades ativadas por movimento não têm uma alternativa UI.           |
| O idioma da página é declarado? | Inspecionar o código HTML para verificar o atributo `lang` na tag `<html>`.                  | 3.1.1        | Informar se o idioma principal da página não está declarado, prejudicando a pronúncia do leitor de tela. |
| Idiomas de partes do conteúdo são declarados? | Verificar se trechos de texto em idiomas diferentes do principal têm seu `lang` declarado.    | 3.1.2          | Relatar quando trechos em outro idioma não são marcados corretamente.                      |
| Mudanças de contexto inesperadas são evitadas? | Interagir com formulários e controles para verificar se não há mudanças inesperadas de tela ou foco. | 3.2.1, 3.2.2   | Listar mudanças de contexto súbitas ou inesperadas ao preencher campos ou interagir com controles. |
| Validação de entrada de dados é clara e acessível? | Inserir dados incorretos e verificar se as mensagens de erro são claras e acessíveis via leitor de tela. | 3.3.1, 3.3.3   | Informar quando mensagens de erro não são lidas, claras ou não sugerem correção.           |
| Prevenção de erros está implementada para dados críticos? | Testar submissão de formulários críticos (financeiros, legais) e verificar mecanismos de prevenção de erros. | 3.3.4          | Relatar ausência de revisão, confirmação ou opção de reverter para formulários com dados sensíveis. |
| Mensagens de status são anunciadas por leitores de tela? | Observar interações que geram mensagens de status (ex: "carregando", "sucesso") e verificar se são anunciadas. | 4.1.3          | Indicar mensagens de status que não são percebidas por leitores de tela.                  |

## Testes para PDF

A tabela a seguir apresenta o roteiro de verificação da acessibilidade em arquivos PDF, com instruções práticas de teste e os respectivos critérios da WCAG, visando apoiar a conformidade normativa e a construção de documentos digitais mais inclusivos:

| ITEM DO TESTE | COMO TESTAR | WCAG Aplicável | OBSERVAÇÕES (Texto Padrão para Registro de Erro) |
|:---------------------------------------|:----------------------------------------------------------------------------------------------------------|:-----------------|:------------------------------------------------------------------------------------------|
| O conteúdo não textual possui descrição alternativa adequada? | Verificar se todas as imagens, gráficos e outros elementos não textuais possuem texto alternativo (alt text) ou estão marcados como artefato se forem decorativos. | 1.1.1 | Apontar imagens ou elementos gráficos sem descrição textual alternativa adequada. |
| As informações e relações estão semanticamente estruturadas? | Validar se a estrutura lógica do documento (títulos, listas, tabelas, etc.) está corretamente marcada com tags. | 1.3.1 | Informar se a estrutura semântica do PDF não está corretamente taggeada (e.g., títulos não são títulos). |
| A ordem de leitura do conteúdo está lógica e previsível? | Verificar a ordem de leitura do conteúdo (tags) para garantir que seja lógica e não confusa. | 1.3.2 | Descrever trechos do PDF onde a ordem de leitura das tags é ilógica ou inesperada. |
| As informações dependem apenas de características sensoriais? | Assegurar que as informações não são transmitidas apenas por características sensoriais (como forma, tamanho, localização, orientação ou som). | 1.3.3 | Indicar informações que dependem exclusivamente de atributos sensoriais sem alternativas textuais. |
| A cor é o único meio de transmitir informações importantes? | Confirmar que a cor não é o único meio visual de transmitir informação, indicar uma ação ou solicitar uma resposta. | 1.4.1 | Apontar elementos onde a cor é o único diferenciador para transmitir significado ou ação. |
| O contraste entre texto e fundo é suficiente? | Utilizar um analisador de contraste para verificar o contraste mínimo entre o texto e seu plano de fundo. | 1.4.3 | Listar textos no PDF com contraste insuficiente em relação à cor de fundo. |
| Há uso de texto embutido em imagens? | Evitar o uso de texto incorporado em imagens sempre que possível; o texto deve ser selecionável e pesquisável. | 1.4.5 | Informar se há texto em formato de imagem que deveria ser texto real (selecionável). |
| Contraste sem texto | Verificar o contraste de elementos gráficos essenciais e componentes de interface de usuário. | 1.4.11 | Indicar elementos gráficos que não possuem contraste suficiente em relação ao fundo. |
| O conteúdo interativo pode ser operado apenas com teclado?| Testar a navegabilidade e interatividade de formulários ou elementos clicáveis usando apenas o teclado. | 2.1.1 | Apontar componentes interativos do PDF (como campos de formulário) que não são operáveis via teclado. |
| Há atalhos de teclado que prejudicam a navegação?| Garantir que, se houver um atalho de teclado com uma única tecla, ele possa ser desativado ou remapeado. | 2.1.2 | Listar atalhos de teclado de uma única tecla que bloqueiam o usuário ou não podem ser desativados. |
| É possível ignorar blocos repetitivos? | Verificar a existência de links ou marcadores que permitam pular blocos de conteúdo repetitivos (como cabeçalhos e rodapés fixos). | 2.4.1 | Indicar a ausência de um mecanismo para pular blocos de conteúdo repetitivos. |
| O título do documento está presente e é descritivo? | Confirmar se o documento possui um título descritivo nas suas propriedades (Metadados do PDF). | 2.4.2 | Informar se o título do documento PDF está ausente ou é genérico. |
| A ordem de foco dos elementos interativos é lógica? | Assegurar que a ordem de foco dos elementos interativos (como campos de formulário) segue uma sequência lógica. | 2.4.3 | Descrever campos interativos onde a ordem de tabulação/foco não é lógica ou previsível. |
| Os links informam sua finalidade no contexto? | Verificar se os links são descritivos em seu contexto, permitindo que o usuário entenda sua finalidade. | 2.4.4 | Listar links com texto genérico (ex: "clique aqui") que não fornecem contexto sobre seu destino. |
| O conteúdo pode ser acessado por múltiplos caminhos? | Garantir que há múltiplas formas de encontrar as informações no documento (ex: índice, marcadores, pesquisa). | 2.4.5 | Informar se o PDF oferece apenas uma forma de acessar as informações importantes. |
| Os cabeçalhos e rótulos são descritivos? | Assegurar que cabeçalhos (headings) e rótulos de formulário são informativos e descrevem o tópico ou a finalidade do componente. | 2.4.6 | Apontar cabeçalhos ou rótulos de formulário que não são descritivos ou estão ausentes. |
| O idioma principal do documento está definido? | Verificar se o idioma principal do documento está definido nas propriedades do PDF. | 3.1.1  | Informar se o idioma principal do PDF não está especificado. |
| Mudanças de idioma em trechos estão corretamente marcadas? | Confirmar se as mudanças de idioma em partes do texto estão marcadas corretamente. | 3.1.2 | Indicar trechos do PDF em outro idioma que não estão corretamente marcados. |
| O preenchimento de formulários altera o contexto inesperadamente? | Assegurar que qualquer mudança de contexto ao preencher um formulário é iniciada pelo usuário ou ele é alertado sobre ela. | 3.2.2 | Listar casos onde a conclusão de um campo de formulário causa uma mudança de contexto inesperada. |
| A navegação e os elementos se mantêm consistentes? | Verificar se a navegação (links, botões) e os elementos de identificação (cabeçalhos, rodapés) são consistentes. | 3.2.3 | Apontar elementos de navegação ou identificação que não são consistentes em todo o PDF. |
| Os erros em formulários são identificados corretamente? | Se ocorrerem erros na entrada de dados (em formulários), verificar se o erro é identificado claramente e descrito em texto. | 3.3.1 | Informar se os erros em campos de formulário não são claramente identificados para o usuário. |
| Há rótulos ou instruções claras nos campos? | Confirmar que os campos de formulário possuem rótulos ou instruções claras sobre o formato da entrada necessária. | 3.3.2 | Listar campos de formulário que não fornecem rótulos ou instruções claras. |
| O sistema fornece sugestões para correção de erros? | Se um erro de entrada for detectado, verificar se o sistema fornece sugestões de como corrigi-lo. | 3.3.3 | Apontar campos de formulário onde o sistema não oferece sugestões para correção de erros. |
| Os componentes interativos têm nome, função e valor definidos? | Assegurar que todos os componentes da interface (especialmente em formulários interativos) têm nome, função e valor programáticos definidos. | 4.1.2 | Listar componentes interativos do PDF que não têm nome, função ou valor programáticos definidos (ex: botões sem rótulo). |