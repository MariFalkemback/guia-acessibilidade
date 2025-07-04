# Classificaçao de Defeitos em Testes de Acessibilidade

Para facilitar a análise e priorização de correções, os defeitos podem ser classificados conforme sua natureza e impacto sobre a interação do usuário com a aplicação. 

Esses defeitos podem ser agrupados em categorias, considerando tanto sua origem quanto o impacto que causam. 
Além da classificação por tipo, os defeitos de acessibilidade também devem ser analisados quanto ao seu nível de risco, ou seja, o grau de impacto que cada falha representa na experiência de uso, especialmente para pessoas com deficiência. Essa categorização é essencial para priorizar correções e orientar equipes de desenvolvimento sobre quais barreiras comprometem de forma mais severa a inclusão digital.

Segundo Lopes e Souza (2020), a avaliação de acessibilidade deve considerar não apenas a existência de falhas, mas sua gravidade na interação com o sistema. Da mesma forma, Ferreira et al. (2018) destacam que a priorização de correções deve partir de uma análise combinada entre frequência da ocorrência, impacto funcional e ausência de alternativas para o usuário.

Com base nisso, os níveis de risco podem ser definidos da seguinte forma:

## Baixo 

Refere-se a falhas com impacto limitado na experiência geral. Embora possam dificultar levemente a navegação, não comprometem a funcionalidade principal e geralmente possuem soluções alternativas simples. Exemplo: ausência de título em uma imagem decorativa.

## Médio

 Representa barreiras que causam desconforto ou dificultam a interação, mas que ainda permitem o acesso por meios alternativos. Exemplo: formulários com campos sem rótulo visível, mas com instruções textuais ao redor.

## Alto

: Envolve falhas críticas que impedem o acesso completo a conteúdo ou funcionalidades essenciais. Esse tipo de barreira compromete diretamente o direito de acesso à informação e pode excluir totalmente determinados perfis de usuários. Exemplo: botão de envio de formulário que não pode ser acionado por teclado ou não é identificado por [leitores de tela](introducao.md#leitores-tela).

A definição do nível de risco, portanto, é um elemento estratégico dentro do processo de auditoria de acessibilidade. Ela permite alinhar esforços de correção com os princípios das WCAG e com os objetivos de inclusão, usabilidade e conformidade legal.