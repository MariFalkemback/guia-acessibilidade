# Verificações Comuns Por Tipo de Deficiência

As barreiras de acessibilidade podem se manifestar de diferentes maneiras, afetando diversos grupos de usuários de forma distinta. Por exemplo, pessoas com deficiência visual podem encontrar dificuldades em sites que não fornecem descrições alternativas para imagens ou que usam combinações de cores que dificultam a leitura. Já usuários com deficiência auditiva podem ser prejudicados pela ausência de legendas em vídeos ou pela falta de transcrições de áudios. Além disso, conteúdos desorganizados ou excessivamente complexos podem representar obstáculos cognitivos relevantes para pessoas com dificuldades de atenção ou aprendizagem.

Para garantir uma acessibilidade digital efetiva, é fundamental considerar as necessidades específicas de diferentes perfis de usuários com deficiência. A aplicação de testes direcionados permite identificar barreiras que afetam diretamente a usabilidade e o acesso à informação. A seguir, são descritas verificações essenciais para cada tipo de deficiência:

•	**Deficiência Visual**: Os testes devem incluir o uso de leitores de tela como NVDA, JAWS (Windows), TalkBack (Android) e VoiceOver (iOS), com o objetivo de verificar se todos os elementos da interface são corretamente identificados e lidos. Também é importante garantir a existência de alternativas textuais para imagens, a presença de foco visível durante a navegação com teclado e a ordem lógica de leitura dos elementos.

•	**Deficiência Auditiva**: A acessibilidade para pessoas com deficiência auditiva depende da disponibilização de recursos visuais equivalentes. Deve-se verificar se vídeos possuem legendas sincronizadas, se há transcrições textuais de áudios e se o sistema evita depender exclusivamente de alertas sonoros, fornecendo sempre uma indicação visual complementar.

•	**Deficiência Motora**: Usuários com limitações motoras frequentemente utilizam teclado, dispositivos adaptados ou navegação por voz. É essencial garantir a navegação completa por teclado, a ausência de tempo limite restritivo para interações, e que os elementos clicáveis ou tocáveis tenham tamanho mínimo adequado (recomenda-se ao menos 44px por 44px, conforme a WCAG 2.1).

•	**Deficiência Cognitiva**: A acessibilidade cognitiva envolve aspectos como clareza, previsibilidade e simplicidade da interface. Deve-se assegurar o uso de linguagem direta e simples, padrões visuais consistentes, e a eliminação de distrações excessivas, como animações rápidas ou sons inesperados, que possam comprometer a concentração do usuário.

A aplicação dessas verificações permite identificar falhas específicas e propor melhorias alinhadas às necessidades reais dos usuários. 


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