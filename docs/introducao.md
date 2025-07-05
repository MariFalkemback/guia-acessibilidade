# Introdução à Acessibilidade Digital
---
## Definição de Acessibilidade Digital

A acessibilidade digital compreende a prática de projetar e desenvolver produtos digitais (websites, aplicativos, sistemas) de maneira que possam ser utilizados de forma eficiente e autônoma por todas as pessoas, independentemente de suas habilidades ou deficiências, incluindo idosos, pessoas autistas, com deficiência visual, auditiva, motora, cognitiva, ou seja, qualquer pessoa que enfrente barreira no uso de tecnologia. Assegurando que o acesso e a interação com o conteúdo digital sejam equitativos.

---
## Por que a acessibilidade ainda não é prioridade?

Estudos mostram que mais de 95% das páginas da internet apresentam problemas de acessibilidade.

Apesar dos avanços legislativos e técnicos, ainda há muitos desafios na efetiva implementação da acessibilidade digital, tanto no setor público quanto no privado. Muitos desenvolvedores e designers ainda não possuem o conhecimento necessário sobre as diretrizes de acessibilidade ou não consideram esse aspecto como prioridade durante o planejamento e construção de interfaces. Além disso, a falta de testes com usuários reais que apresentam algum tipo de limitação compromete a eficácia das soluções adotadas.

Outro fator crítico é a percepção equivocada de que tornar um sistema acessível exige altos investimentos ou representa um esforço técnico desproporcional. No entanto, quando a acessibilidade é considerada desde o início do projeto, ela pode ser integrada de forma mais eficiente e com menor custo, beneficiando não apenas pessoas com deficiência, mas todos os usuários, inclusive aqueles que acessam conteúdos em situações de limitação temporária, como ambientes com muito barulho, pouca iluminação ou uso de dispositivos móveis com conexão instável.

---
## Por que testar acessibilidade é essencial?

No desenvolvimento de sistemas, acessibilidade não é apenas uma boa prática — é uma exigência legal e ética. A acessibilidade digital é reconhecida como um direito por instituições como a ONU, e está prevista em leis brasileiras, como a **[Lei Brasileira de Inclusão](#lbi)** (nº 13.146/2015), nas diretrizes internacionais **[WCAG](#wcag)** (Web Content Accessibility Guidelines), mantidas pelo W3C, e no **[e-MAG](#e-MAG)** (Modelo de Acessibilidade em Governo Eletrônico), mantido pelo governo brasileiro.
O não cumprimento pode acarretar sanções legais, além de comprometer a imagem institucional perante a sociedade.

Em um mundo cada vez mais conectado e dependente da tecnologia para atividades essenciais — como educação, trabalho, saúde e serviços públicos, excluir pessoas por barreiras digitais significa limitar sua cidadania e participação social.

Por isso, é fundamental que instituições de ensino, empresas, desenvolvedores e gestores públicos compreendam a importância da acessibilidade como parte da qualidade e da responsabilidade social de seus produtos e serviços digitais. Iniciativas de capacitação, auditorias de acessibilidade e políticas institucionais voltadas à inclusão são caminhos importantes para transformar o ambiente digital em um espaço verdadeiramente acessível e democrático.

A acessibilidade digital é especialmente importante em contextos educacionais e governamentais, onde o acesso à informação deve ser garantido como um direito fundamental. Quando os recursos pedagógicos não são projetados com acessibilidade, eles podem excluir completamente alunos com deficiência da experiência de aprendizagem.

Além de promover o acesso equitativo, a acessibilidade também oferece benefícios amplos para instituições e empresas. Sites acessíveis tendem a apresentar melhor usabilidade para todos os usuários, independentemente de suas habilidades, pois oferecem navegação mais clara, organização lógica do conteúdo e interfaces intuitivas. Isso pode resultar em maior engajamento, menor taxa de rejeição e melhor posicionamento em mecanismos de busca, visto que a acessibilidade também contribui para o SEO (Search Engine Optimization).

Além disso, quando se considera a acessibilidade desde as etapas iniciais do desenvolvimento de um sistema, os custos de implementação são significativamente menores do que se for necessário realizar correções posteriores. Essa abordagem preventiva também demonstra compromisso social e respeito à diversidade, valores cada vez mais valorizados por consumidores, alunos e cidadãos em geral.

---
## Glossário de Acessibilidade Digital: WCAG, eMAG, LBI, Tecnologia Assistiva

### <h2 id="lbi">Lei Brasileira de Inclusão da Pessoa com Deficiência (LBI)</h2>

A LBI (Lei nº 13.146/2015) define que a acessibilidade no digital é um direito fundamental da pessoa com deficiência e estabelece que:

•	Websites e aplicativos de órgãos públicos e empresas privadas devem ser acessíveis.

•	Os websites e aplicativos devem seguir as diretrizes de acessibilidade internacionalmente reconhecidas.

•	As empresas devem oferecer treinamento sobre acessibilidade para seus funcionários.

### <h2 id="wcag">WCAG (Web Content Accessibility Guidelines)</h2>

As WCAG (Diretrizes de Acessibilidade para Conteúdo Web) constituem um conjunto de recomendações internacionais, publicadas pelo World Wide Web Consortium (W3C), com o propósito de tornar o conteúdo da web mais acessível. A WCAG 2.1 (2018) possui 78 critérios estruturados em quatro princípios fundamentais:

•	**Perceptível**: A informação e os componentes da interface do usuário devem ser apresentados aos usuários de formas que eles possam perceber (e.g., texto alternativo para imagens, legendas para vídeos).

•	**Operável**: Os componentes da interface do usuário e a navegação devem ser operáveis (e.g., acesso por teclado, tempo suficiente para interação).

•	**Compreensível**: A informação e a operação da interface do usuário devem ser compreensíveis (e.g., linguagem clara, comportamento previsível).

•	**Robusto**: O conteúdo deve ser robusto o suficiente para que possa ser interpretado por uma ampla variedade de agentes de usuário, incluindo tecnologias assistivas.

Esses quatro princípios servem como base para a criação de experiências digitais inclusivas, oferecendo diretrizes claras para que desenvolvedores e designers construam conteúdos acessíveis a todas as pessoas, independentemente de suas limitações.

As WCAG estão divididas em três níveis de conformidade: **A (mínimo)**, **AA (médio)** e **AAA (avançado)**. O nível AA é o mais amplamente recomendado, sendo considerado o padrão ideal para a maioria dos sites e sistemas, pois equilibra rigor técnico e viabilidade prática. Cada nível estabelece critérios de sucesso que devem ser seguidos para garantir que os conteúdos atendam às necessidades de acessibilidade de diferentes perfis de usuários.

A WCAG não é o único documento de acessibilidade mantido pelo W3C. Existem outras normas importantes que complementam esse ecossistema:

- **UAAG**: trata da acessibilidade nos agentes de usuário (como navegadores e leitores de tela).
- **ATAG**: orienta sobre ferramentas de autoria e edição de conteúdo acessível.
- **WAI-ARIA**: define padrões para tornar componentes dinâmicos (como menus, modais, carrosséis) acessíveis via HTML.

Não nos aprofundaremos nessas diretrizes aqui, mas é importante saber que elas existem — e que navegadores, editores e frameworks também devem segui-las para garantir uma web verdadeiramente acessível.

<h4>Links Oficiais</h4>
<ul>
  <li><a href="https://www.w3.org/WAI/standards-guidelines/wcag/" target="_blank" rel="noopener noreferrer">Visão Geral das WCAG (em inglês)</a></li>
  <li><a href="https://www.w3c.br/traducoes/wcag/wcag21-pt-BR/" target="_blank" rel="noopener noreferrer">Tradução Oficial da WCAG 2.1 (pt-BR - W3C Brasil)</a></li>
  <li><a href="https://www.w3.org/WAI/standards-guidelines/" target="_blank" rel="noopener noreferrer">Outras Normas: UAAG, ATAG, WAI-ARIA, etc (em inglês)</a></li>
  <li><a href="https://guia-wcag.com/" target="_blank" rel="noopener noreferrer">Guia Rápido da WCAG 2.2 em português</a></li>
</ul>

---

### <h2 id="e-MAG">e-MAG (Modelo de Acessibilidade em Governo Eletrônico)</h2>

o Modelo de Acessibilidade em Governo Eletrônico (e-MAG) adota os padrões do WCAG, oferecendo orientações específicas para a criação e adaptação de conteúdos digitais no setor público, assegurando sua acessibilidade a toda a população.

As recomendações do eMAG permitem que a implementação da acessibilidade digital seja conduzida de forma padronizada, de fácil implementação, coerente com as necessidades brasileiras e em conformidade com os padrões internacionais.

### <h2 id="Tec_assistivas">Tecnologias Assistivas</h2>

Conforme a Lei Brasileira de Inclusão, 13.146 de julho de 2015, tecnologia assistiva é definida como produtos, equipamentos, dispositivos, recursos, metodologias, estratégias, práticas e serviços que tenham como objetivo promover a funcionalidade, relacionada à atividade e à participação da pessoa com deficiência ou com mobilidade reduzida, visando à sua autonomia, independência, qualidade de vida e inclusão social.

Exemplos de Tecnologias Assistivas Digitais:

• <span id="leitores-tela">Leitores de tela:</span> Programas que convertem texto em fala, permitindo que pessoas com deficiência visual acessem conteúdo digital. Exemplos incluem NVDA (Windows), Orca (Linux), VoiceOver (iOS),TalkBack (Android).
    
• Aplicativos e softwares para tradução de Libras:Facilitam a comunicação entre pessoas surdas e ouvintes, como softwares de tradução de Libras e legendas automáticas em vídeos. 

• Dispositivos de controle por voz: Permitem controlar dispositivos eletrônicos, como luzes e eletrodomésticos, por meio de comandos de voz. 