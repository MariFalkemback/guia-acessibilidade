# Boas Práticas

Com base nas análises e práticas abordadas neste trabalho, recomenda-se que equipes de design, desenvolvimento e qualidade incorporem as seguintes ações de forma sistemática:

---

## Priorização desde o Início

Elementos acessíveis devem ser considerados desde as fases iniciais do projeto, principalmente na construção do design system. Componentes como botões, formulários e mensagens devem ser planejados com base em padrões acessíveis, evitando retrabalho posterior e promovendo consistência ao longo da aplicação.

A acessibilidade deve realmente ser pensada desde a concepção do projeto, para que alternativas inclusivas sejam implementadas desde as regras de negócio, evitando surpresas no final do ciclo de desenvolvimento.

### Cenário de Exemplo: Sistema bancário com autenticação por biometria facial

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

## Registro adequado de defeitos: 
Barreiras de acessibilidade identificadas em testes devem ser tratadas com a mesma seriedade que outros bugs funcionais. Para isso, é fundamental criar issues específicas nos sistemas de gestão de tarefas, descrevendo claramente a falha, o impacto para o usuário e os critérios de aceitação da correção.

## Participação de pessoas com deficiência (PcD): 
Sempre que possível, é recomendável incluir usuários com deficiência nos ciclos de testes de usabilidade e acessibilidade. A experiência prática desses usuários fornece insights valiosos que muitas vezes não são identificados por ferramentas automáticas ou testadores sem vivência direta com tecnologias assistivas.

## Documentação viva e colaborativa: 
Manter uma base de conhecimento atualizada com exemplos de boas práticas, padrões adotados e lições aprendidas é essencial para o amadurecimento organizacional em acessibilidade. Essa documentação deve ser de fácil acesso e continuamente aprimorada à medida que novos aprendizados e requisitos surgem. 