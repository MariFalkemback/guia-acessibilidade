# Boas Práticas e Considerações Finais

A acessibilidade digital não deve ser tratada como uma etapa final ou complementar no desenvolvimento de software, mas sim como um compromisso contínuo com a inclusão e a equidade no acesso à informação. Garantir que produtos digitais sejam utilizáveis por todas as pessoas, independentemente de suas habilidades, é não apenas uma exigência legal e ética, mas uma condição essencial para a qualidade e a sustentabilidade das soluções tecnológicas.

Com base nas análises e práticas abordadas neste trabalho, recomenda-se que equipes de design, desenvolvimento e qualidade incorporem as seguintes ações de forma sistemática:

---

## Priorização desde o Início

Elementos acessíveis devem ser considerados desde as fases iniciais do projeto, principalmente na construção do design system. Componentes como botões, formulários e mensagens devem ser planejados com base em padrões acessíveis, evitando retrabalho posterior e promovendo consistência ao longo da aplicação.

A acessibilidade deve realmente ser pensada desde a concepção do projeto, para que alternativas inclusivas sejam implementadas desde as regras de negócio, evitando surpresas no final do ciclo de desenvolvimento.

### Cenário de Exemplo 

- Sistema bancário com autenticação por biometria facial

**Decisão de negócio:**  
O Product Owner propõe que os usuários façam login e validem operações usando reconhecimento facial como medida de segurança.

**Visão com acessibilidade desde o início:**

- Usuários com deficiência visual não conseguem posicionar o rosto corretamente sem auxílio.
- Pessoas com deformidades faciais, paralisias ou mudanças na aparência podem não ser reconhecidas.
- Usuários com deficiência motora podem ter dificuldade para alinhar a câmera.

**Decisão tomada ainda nas regras de negócio: O projeto já prevê alternativas viáveis, como:**

- Autenticação por token (SMS, e-mail ou app autenticador).
- Login por senha + segundo fator.
- Atendimento humano como fallback (ex: telefone com perguntas de segurança).

**Impacto prático na implementação: Quando o time for implementar, já sabe que:**

- O recurso facial será opcional, não obrigatório.
- O fluxo permitirá troca de método sem barreiras visuais ou motoras.

---

## Definição clara da cobertura padrão dos testes de acessibilidade
  
Para garantir a qualidade e a consistência dos testes, recomenda-se definir um cenário padrão para avaliação da acessibilidade. Esse cenário deve incluir os seguintes parâmetros:

dispositivo utilizado, sistema operacional e sua versão, navegador e versão, tecnologia assistiva empregada e versão, além do leitor de pdf e sua versão quando aplicável. 

Também é essencial listar quais critérios da WCAG são considerados  nos testes, especificando quais critérios estão integralmente cobertos, quais estão parcialmente cobertos (com justificativa) e quais estão fora do escopo, com a devida justificativa. 

Essa padronização assegura que os testes sejam replicáveis e facilita a compreensão do alcance dos testes realizados, deixando claro quais critérios não são aplicáveis ao contexto do projeto.

---

## Registro adequado de defeitos 
Barreiras de acessibilidade identificadas em testes devem ser tratadas com a mesma seriedade que outros bugs funcionais. Para isso, é fundamental criar issues específicas nos sistemas de gestão de tarefas, descrevendo claramente a falha, o impacto para o usuário e os critérios de aceitação da correção.

## Participação de pessoas com deficiência (PcD) 
Sempre que possível, é recomendável incluir usuários com deficiência nos ciclos de testes de usabilidade e acessibilidade. A experiência prática desses usuários fornece insights valiosos que muitas vezes não são identificados por ferramentas automáticas ou testadores sem vivência direta com tecnologias assistivas.

## Documentação viva e colaborativa 
Manter uma base de conhecimento atualizada com exemplos de boas práticas, padrões adotados e lições aprendidas é essencial para o amadurecimento organizacional em acessibilidade. Essa documentação deve ser de fácil acesso e continuamente aprimorada à medida que novos aprendizados e requisitos surgem. 

A adoção dessas práticas promove uma cultura de desenvolvimento mais inclusiva, fortalece a conformidade com diretrizes como as WCAG e contribui para a construção de produtos digitais mais justos, eficazes e centrados no usuário. A acessibilidade, portanto, não é apenas uma meta técnica, mas um valor essencial a ser cultivado em todas as etapas do ciclo de vida do software.

A realização de testes de acessibilidade digital requer um conjunto de procedimentos objetivos que permitam identificar falhas, registrar evidências e propor melhorias de forma sistemática. Para isso, é fundamental adotar um roteiro estruturado com base nas diretrizes da WCAG (Web Content Accessibility Guidelines), contemplando diferentes aspectos da interação entre o usuário e a interface.

Este guia prático foi desenvolvido para apoiar equipes de design, desenvolvimento e qualidade na condução de testes manuais e semiautomatizados em páginas web e sistemas digitais. Cada item listado contempla o que deve ser verificado, como executar o teste, qual critério da WCAG está relacionado e um modelo padronizado de descrição do erro, facilitando o registro e o encaminhamento de correções.

Os testes cobrem pontos críticos como componentes dinâmicos, validação de formulários, feedback visual e auditivo, navegação por regiões (landmarks), uso correto de modais, estrutura semântica, acessibilidade de vídeos, dimensionamento responsivo e tamanho de áreas clicáveis. Essas práticas não apenas garantem conformidade técnica, mas também promovem uma experiência mais inclusiva para usuários com diferentes perfis de deficiência.