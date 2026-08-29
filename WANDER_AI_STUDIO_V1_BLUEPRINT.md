# Wander AI Studio — V1 Product Blueprint

## 1. Status e autoridade

Este documento registra o V1 aprovado do Wander AI Studio.

Quando houver conflito de informação, vale a seguinte ordem:

1. instrução explícita mais recente de Wander;
2. este V1 Product Blueprint aprovado;
3. estado atual do repositório, da aplicação e dos dados;
4. `WANDER_AI_STUDIO_HANDOFF.md`;
5. brainstorming anterior.

O arquivo `WANDER_AI_STUDIO_HANDOFF.md` permanece como handoff autoritativo e fonte da visão, dos princípios e do contexto do projeto. Este Blueprint congela o recorte do V1 sem substituir esse documento.

## 2. Identidade do produto

Wander AI Studio é um projeto pessoal e independente para os alunos particulares de Wander. Seus dois modelos principais são `English Course` e `School Support`; por isso, o produto não se restringe conceitualmente ao ensino de inglês.

History e Language Arts são matérias válidas quando fazem parte do atendimento particular em `School Support`. Permanecem fora do escopo a adoção institucional, a administração escolar, fluxos institucionais, processos ligados ao emprego de Wander, IPC institucional e funções escolares sem relação com os atendimentos particulares.

O produto não deve registrar nome de escola, instituição de origem, empregador ou associação institucional dos alunos de `School Support`, pois esses dados não são necessários. Ele será uma plataforma pessoal de ensino e aprendizagem com recursos multimídia e assistência de IA. Seu valor central é reunir, em um sistema persistente, o contexto de cada aluno, as atividades realizadas, o feedback e as próximas ações pedagógicas.

## 3. Objetivo do V1

O V1 deve provar um ciclo completo e útil:

```text
Wander acompanha um aluno
        ↓
organiza ou cria uma atividade contextual
        ↓
atribui conteúdo no dashboard do aluno
        ↓
o aluno aprende, pratica e envia
        ↓
o resultado e o feedback ficam registrados
        ↓
Wander revisa o desempenho e planeja o próximo passo
```

O V1 não será apenas uma coleção de links. Seus dashboards devem ser personalizados e ativos: precisam apresentar dados, conteúdo e ações correspondentes ao usuário e ao contexto pedagógico atual.

## 4. Pessoas e papéis de acesso

### Professor/administrador

Wander é o professor e administrador. Ele deve poder gerenciar alunos, consultar o histórico, organizar e atribuir conteúdo, revisar submissões, auditar avaliações geradas e registrar feedback.

### Aluno

Cada aluno deve acessar somente seu próprio ambiente, atividades, feedback e progresso. Nenhum aluno pode visualizar dados de outro aluno.

### Alunos atuais de referência

| Aluno | Grupo | Modelo | Nível ou matérias | Material confirmado |
| --- | --- | --- | --- | --- |
| Regina | Adulta | `English Course` | C1 | *American English File 4* |
| Margarete | Adulta | `English Course` | B2 | *American English File 3* |
| Fernando | Adulto | `English Course` | B1 | *American English File 2* |
| Theo | Criança | `School Support` | History + Language Arts | Conforme a necessidade |
| Julia | Criança | `School Support` | Matérias escolares variáveis conforme a necessidade | Conforme a necessidade |

Livros, unidades e outros materiais serão cadastrados quando confirmados; este Blueprint não presume informações adicionais nem registra a instituição de origem das matérias escolares.

## 5. Perfis de acompanhamento

Os dois perfis principais descrevem o tipo de acompanhamento pedagógico e não substituem os papéis de acesso professor/aluno.

### `English Course`

Percurso estruturado de aprendizagem de inglês, normalmente associado a nível, livro ou curso, unidade atual, objetivos linguísticos e progressão.

### `School Support`

Apoio individual relacionado às necessidades escolares do aluno particular, como revisão de conteúdo, preparação para uma atividade ou avaliação e acompanhamento de dificuldades específicas.

Um aluno deve ter um perfil principal configurado. A modelagem futura não deve impedir que necessidades dos dois perfis coexistam quando Wander considerar apropriado.

## 6. Experiência principal

### Dashboard de Wander

O dashboard do professor deve oferecer, no recorte do V1:

- visão dos alunos e de seus perfis;
- situação atual, próximos itens e submissões recentes;
- acesso ao histórico e à memória pedagógica;
- criação, organização e atribuição de atividades;
- revisão de respostas e registro de feedback;
- acesso ao `Weekly Challenge`;
- geração contextual de atividades;
- geração e auditoria de assessments;
- entrada para importar e revisar atas Gemini.

### Dashboard do aluno

O dashboard de cada aluno deve ser privado, personalizado, ativo e acionável. Ele não será apenas uma lista personalizada de atividades e materiais. Deve oferecer experiências interativas orientadas por IA usando, conforme disponível:

- perfil;
- idade ou faixa etária;
- nível;
- curso ou matéria;
- livro e unidade;
- materiais;
- últimas aulas;
- memória pedagógica;
- dificuldades e pontos fortes;
- atividades anteriores, tentativas e feedback;
- progresso.

Exemplos conceituais de ações:

- `Continue Learning`;
- `Practice from Your Last Class`;
- `Quick Quiz`;
- `Explain It Another Way`;
- `Visual Review`;
- `Watch & Respond`;
- `Weekly Challenge`.

O dashboard também deve mostrar:

- curso ou apoio atual;
- materiais e conteúdo recente;
- atividades pendentes e concluídas;
- `Weekly Challenge` vigente;
- envios, correções e feedback;
- visão apropriada de progresso.

A linguagem e o grau de detalhe devem ser adequados à idade e ao contexto do aluno. Prática formativa de baixo risco pode ser gerada interativamente, desde que contexto, conteúdo, proveniência, respostas e resultados possam ser inspecionados por Wander. Assignments formais e assessments sempre exigem aprovação explícita de Wander antes da publicação.

## 7. Escopo funcional do V1

### 7.1 Gestão de alunos

- criar, editar e desativar alunos;
- classificar o acompanhamento como `English Course` ou `School Support`;
- registrar idade ou faixa etária quando necessário;
- associar nível, livro, unidade, materiais e objetivos;
- manter notas pedagógicas do professor.

### 7.2 Conteúdo multimídia

O V1 deve aceitar atividades e materiais com combinações de:

- texto e leitura;
- áudio autorizado;
- vídeos autorizados do material;
- vídeos incorporados do YouTube;
- imagens da web, com origem quando aplicável;
- imagens geradas por IA;
- diagramas gerados por IA;
- visual reviews;
- vocabulary visuals;
- grammar support visual;
- arquivos e links;
- perguntas e exercícios interativos e verificáveis.

O Google Drive existente é uma fonte relevante de materiais pedagógicos. Para *American English File 2, 3 e 4*, Wander possui no Drive os materiais usados nas aulas, incluindo Student's Book, Workbook e arquivos de áudio e vídeo. A arquitetura deve permitir catalogar e referenciar esses materiais sem presumir que todos serão copiados para o banco ou para outro armazenamento.

O armazenamento e a distribuição devem respeitar privacidade, permissões e direitos autorais. Livros e materiais comerciais podem fornecer contexto pedagógico, mas não devem ser reproduzidos ou distribuídos sem autorização.

### 7.3 Atividades, submissões e feedback

- Wander cria ou seleciona uma atividade e a atribui a um aluno;
- o aluno abre, realiza e envia a atividade;
- tentativas, respostas e estado ficam persistidos;
- correção automática pode ser usada apenas em formatos adequados e definidos;
- Wander pode revisar e complementar o resultado;
- o aluno recebe feedback claro e tem histórico acessível.

### 7.4 Memória pedagógica estruturada

A memória deve existir nos dados do produto, não somente em conversas com IA. Deve poder reunir:

- perfil e tipo de acompanhamento;
- nível, curso, livro e unidade;
- tópicos e objetivos estudados;
- materiais e atividades atribuídos;
- respostas, tentativas, resultados e feedback;
- dificuldades recorrentes e pontos fortes;
- progresso e notas do professor;
- recomendações e próximos passos, com origem identificável.

Informações inferidas por IA não devem ser tratadas automaticamente como fatos. Wander deve poder revisar ou corrigir registros pedagógicos relevantes.

### 7.5 Importação de atas Gemini de Gmail/Drive

O V1 deve prever um fluxo de importação das atas Gemini relacionadas às aulas e disponíveis no Gmail ou Google Drive.

Fluxo esperado:

1. localizar uma ata elegível;
2. exibir origem, data e conteúdo para conferência;
3. associá-la ao aluno correto;
4. extrair uma proposta de tópicos, dificuldades, decisões e próximos passos;
5. permitir revisão e edição por Wander;
6. somente após confirmação, incorporar os itens aprovados à memória pedagógica;
7. manter referência à origem para rastreabilidade e evitar duplicação.

A importação não deve varrer, copiar ou enviar indiscriminadamente o conteúdo da conta. O acesso deverá ser mínimo e deliberado.

### 7.6 Weekly Challenge

Wander deve poder criar, gerar, revisar, publicar e encerrar um desafio semanal. O desafio pode ser individual ou reutilizado com adaptações, deve aceitar conteúdo multimídia e precisa registrar participação, envio, feedback e resultado quando aplicável.

O dashboard do aluno deve destacar o desafio vigente e seu prazo ou estado.

### 7.7 Geração contextual de atividades

Wander deve poder solicitar uma atividade usando contexto selecionado e verificável, incluindo quando disponível:

- aluno e perfil de acompanhamento;
- idade ou faixa etária;
- nível;
- livro, unidade e materiais autorizados;
- tópicos estudados;
- dificuldades, pontos fortes e histórico relevante;
- objetivo, formato e duração definidos pelo professor.

Para Wander, o resultado deve ser um rascunho editável e nenhuma atividade formal deve ser publicada ou atribuída automaticamente sem sua ação explícita. No dashboard do aluno, somente práticas formativas de baixo risco podem ser geradas interativamente, mantendo inspeção de contexto, proveniência, respostas e resultados pelo professor.

### 7.8 Assessment Generator

O gerador deve permitir definir aluno ou grupo-alvo, objetivos, conteúdos, formatos de questão, extensão e critérios. Deve produzir um rascunho de assessment e, quando aplicável, gabarito ou critérios de avaliação.

O processo deve ser auditável pelo professor:

- contexto utilizado visível;
- proveniência por questão quando possível, indicando evidências como aula/data, tópico, livro/unidade, material, atividade anterior, dificuldade ou erro registrado e `Weekly Challenge`;
- itens e respostas esperadas editáveis;
- indicação clara de conteúdo gerado;
- validação de pontuação e total;
- aprovação explícita de Wander antes da publicação;
- registro da versão aprovada e de alterações relevantes.

Wander deve conseguir inspecionar a origem pedagógica de cada questão antes de aprovar o assessment.

### 7.9 Progresso e visão pedagógica

O V1 deve apresentar ao aluno uma visão simples e encorajadora. Wander deve ter uma visão mais detalhada de conclusão, desempenho, tentativas, dificuldades recorrentes e próximos passos.

## 8. Requisitos de segurança e privacidade

- autenticação individual e separação entre professor e aluno;
- autorização por registro, impedindo acesso entre alunos;
- segredos somente em ambiente servidor;
- coleta mínima de dados pessoais;
- arquivos privados por padrão;
- registro de origem para dados importados ou gerados;
- revisão humana antes de incorporar inferências relevantes;
- possibilidade futura de exportação e exclusão de dados;
- envio para provedores de IA limitado ao contexto necessário e selecionado;
- nenhum material protegido deve ser transformado em repositório não autorizado.

## 9. Direção técnica e fontes de dados

Supabase permanece como direção técnica prevista para autenticação, autorização, banco de dados, memória pedagógica, atividades, submissões, tentativas, feedback, progresso, `Weekly Challenges`, assessments e proveniência.

O Google Drive não será substituído pelo Supabase como biblioteca dos materiais existentes. Supabase Storage poderá ser usado futuramente para conteúdo próprio do Studio, uploads e recursos gerados, conforme decisão técnica do Sprint 1.

O repositório Git canônico é `teacherwanderstayner-svg/wander.ai.studio-`. O repositório `wandermartins-prog/wander.ai.studio-` permanece somente como upstream e referência histórica.

Esta direção não configura nem conecta qualquer serviço no Sprint 0.

## 10. Idiomas

- interface do professor: português;
- interface padrão do aluno: inglês;
- interface padrão de Julia: português;
- quando Julia estiver estudando inglês, o conteúdo pedagógico dessa matéria pode ser apresentado em inglês.

A arquitetura deve representar separadamente a preferência de idioma de cada aluno e o idioma próprio de cada conteúdo ou atividade. Não deve existir a suposição de um único idioma global para todos os estudantes.

## 11. Princípios de experiência

- interface clara para usuários com idades e níveis diferentes;
- ações principais visíveis, sem aparência de simples diretório de links;
- feedback adequado ao aluno e detalhes pedagógicos reservados a Wander;
- estados explícitos para rascunho, atribuído, em andamento, enviado, revisado e concluído;
- acessibilidade e uso responsivo como critérios desde a fundação;
- preferência de idioma por aluno e idioma do conteúdo tratados separadamente.

## 12. Fora do escopo do V1

- adoção institucional, administração escolar e fluxos institucionais;
- processos ligados ao emprego de Wander;
- IPC institucional e funções escolares não relacionadas aos atendimentos particulares;
- registro da escola, instituição de origem, empregador ou associação institucional dos alunos;
- contas específicas para pais ou responsáveis, salvo decisão posterior explícita;
- reprodução integral de livros comerciais;
- orquestração entre vários provedores de IA;
- criação autônoma e publicação sem revisão do professor;
- relatórios preditivos avançados;
- biblioteca visual sofisticada;
- substituição do julgamento pedagógico de Wander.

History e Language Arts não estão fora do escopo quando são matérias do atendimento particular em `School Support`.

## 13. Critérios de sucesso do V1

O V1 estará comprovado quando:

1. Wander conseguir manter alunos dos dois perfis em dashboards ativos;
2. cada aluno acessar somente seu ambiente personalizado;
3. Wander atribuir uma atividade multimídia e o aluno conseguir enviá-la;
4. resultado, tentativa e feedback permanecerem registrados;
5. a memória pedagógica puder ser consultada e atualizada com rastreabilidade;
6. uma ata Gemini puder ser importada, revisada e associada sem duplicação;
7. um `Weekly Challenge` puder completar seu ciclo de publicação e resposta;
8. uma atividade contextual puder ser gerada, editada e atribuída;
9. um assessment puder ser gerado, auditado, aprovado e aplicado;
10. a proveniência pedagógica das questões geradas puder ser inspecionada quando disponível;
11. o Drive puder ser usado como fonte catalogada sem cópia obrigatória de seus materiais;
12. preferências de interface e idiomas de conteúdo funcionarem separadamente;
13. nenhum aluno puder acessar dados de outro aluno.

## 14. Restrições do Sprint 0

Este Sprint 0 é exclusivamente documental. Ele não autoriza implementação, migração para React ou configuração de Supabase, Vercel, Gmail API, Drive API ou OpenAI. Decisões técnicas detalhadas serão tomadas e validadas em etapas próprias do backlog.
