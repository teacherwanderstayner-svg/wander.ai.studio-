# Wander AI Studio — V1 Backlog

## 1. Como usar este backlog

Este backlog transforma o V1 Product Blueprint em incrementos planejáveis. A ordem abaixo preserva dependências e evita construir toda a plataforma de uma vez.

Cada sprint deve começar com objetivo, resultado esperado e arquivos/componentes afetados. Deve terminar com validação e aprovação antes do próximo sprint. Ideias novas entram no backlog e não alteram silenciosamente o sprint em andamento.

Nenhum item após o Sprint 0 está autorizado para implementação por este documento.

## 2. Estado dos sprints

| Sprint | Objetivo | Estado |
| --- | --- | --- |
| 0 | Documentar e congelar o V1 | Em conclusão nesta tarefa |
| 1 | Definir fundação técnica e modelo de dados | Pendente |
| 2 | Criar autenticação, autorização e perfis | Pendente |
| 3 | Entregar dashboards ativos | Pendente |
| 4 | Entregar conteúdo, atividades e submissões | Pendente |
| 5 | Entregar memória pedagógica e progresso | Pendente |
| 6 | Entregar importação revisável das atas Gemini | Pendente |
| 7 | Entregar Weekly Challenge | Pendente |
| 8 | Entregar geração contextual de atividades | Pendente |
| 9 | Entregar Assessment Generator auditável | Pendente |
| 10 | Endurecer, validar e preparar o V1 | Pendente |

## 3. Sprint 0 — Documentação e congelamento

### Objetivo

Registrar uma definição compartilhada do produto antes de alterar a arquitetura ou iniciar integrações.

### Entregas

- manter `WANDER_AI_STUDIO_HANDOFF.md` como fonte autoritativa;
- criar `WANDER_AI_STUDIO_V1_BLUEPRINT.md`;
- criar `WANDER_AI_STUDIO_V1_BACKLOG.md`;
- atualizar `README.md` para o escopo pessoal e independente;
- identificar explicitamente o HTML/CSS/JavaScript existente como protótipo legado;
- preservar `index.html`, `style.css` e `script.js` sem alterações.

### Critério de aceite

Os documentos refletem os alunos atuais, os dois perfis, o escopo funcional aprovado e os limites do produto, sem implementar funcionalidades.

## 4. Sprint 1 — Fundação técnica e dados

### Objetivo

Decidir e validar a fundação antes da migração do protótipo.

### Backlog

- registrar decisões para frontend, backend, hospedagem e dados;
- registrar `teacherwanderstayner-svg/wander.ai.studio-` como repositório canônico e `wandermartins-prog/wander.ai.studio-` como upstream histórico;
- definir ambientes de desenvolvimento e produção;
- validar Supabase como direção prevista para autenticação, autorização e dados operacionais e pedagógicos;
- modelar professor, aluno, perfil de acompanhamento, curso/material, atividade, atribuição, tentativa, resposta, feedback e progresso;
- modelar memória pedagógica com fonte, estado de revisão e rastreabilidade;
- modelar conteúdo multimídia e permissões de arquivo;
- definir catálogo/referências para materiais do Google Drive sem cópia obrigatória;
- decidir o uso de Supabase Storage para conteúdo próprio, uploads e recursos gerados;
- modelar preferência de idioma por aluno separadamente do idioma do conteúdo/atividade;
- definir estados de atividades e assessments;
- produzir plano de migração do protótipo legado;
- definir estratégia de testes, acessibilidade, backup, exportação e exclusão.

### Critério de aceite

Arquitetura e modelo de dados revisados por Wander, com segurança e privacidade contempladas antes de qualquer dado real ser inserido.

## 5. Sprint 2 — Identidade, acesso e perfis

### Objetivo

Estabelecer acesso privado e separação segura entre professor e alunos.

### Backlog

- implementar autenticação de Wander e dos alunos;
- implementar papel de professor/administrador;
- implementar papel de aluno;
- aplicar autorização por registro e arquivo;
- criar gestão de alunos com ativação e desativação;
- oferecer os perfis `English Course` e `School Support`;
- cadastrar Regina como adulta, `English Course`, C1, *American English File 4*;
- cadastrar Margarete como adulta, `English Course`, B2, *American English File 3*;
- cadastrar Fernando como adulto, `English Course`, B1, *American English File 2*;
- cadastrar Theo como criança, `School Support`, History + Language Arts;
- cadastrar Julia como criança, `School Support`, com matérias variáveis conforme a necessidade;
- não registrar escola, instituição, empregador ou associação institucional;
- testar que um aluno nunca acessa dados de outro.

### Critério de aceite

Wander administra alunos e cada aluno autenticado acessa somente seu próprio registro.

## 6. Sprint 3 — Dashboards personalizados e ativos

### Objetivo

Substituir a experiência de diretório de links por ambientes úteis e orientados a tarefas.

### Backlog

- criar dashboard de Wander com alunos, pendências e atividade recente;
- criar dashboard individual do aluno;
- adaptar conteúdo e linguagem ao perfil e contexto do aluno;
- implementar interface do professor em português e interface padrão dos alunos em inglês;
- configurar Julia com interface padrão em português e permitir conteúdo pedagógico de inglês em inglês;
- separar preferência de idioma do aluno do idioma próprio da atividade;
- apresentar curso/material atual e próximos itens;
- oferecer ações conceituais como `Continue Learning`, `Practice from Your Last Class`, `Quick Quiz`, `Explain It Another Way`, `Visual Review`, `Watch & Respond` e `Weekly Challenge`;
- permitir práticas formativas interativas de baixo risco com conteúdo, contexto, proveniência, respostas e resultados inspecionáveis por Wander;
- definir estados vazios, carregamento, erro e ausência de permissão;
- validar responsividade e acessibilidade básica.

### Critério de aceite

Professor e aluno veem dados reais permitidos e conseguem iniciar suas ações principais a partir do dashboard.

## 7. Sprint 4 — Conteúdo, atividades e submissões

### Objetivo

Entregar o primeiro ciclo completo de atribuição e resposta.

### Backlog

- criar e editar materiais e atividades;
- suportar texto, áudio autorizado, vídeos autorizados do material e vídeos incorporados do YouTube;
- suportar imagens da web com origem, imagens e diagramas gerados por IA, visual reviews, vocabulary visuals e grammar support visual;
- combinar recursos multimídia com atividades verificáveis;
- catalogar e referenciar Student's Book, Workbook, áudio e vídeo de *American English File 2, 3 e 4* existentes no Drive sem presumir cópia;
- atribuir atividade a um aluno;
- registrar prazo e estado;
- permitir abertura, resposta e envio pelo aluno;
- armazenar tentativas e respostas;
- permitir revisão e feedback de Wander;
- implementar correção automática somente para formatos aprovados e determinísticos;
- exigir aprovação explícita de Wander antes da publicação de assignments formais;
- apresentar correção e feedback ao aluno.

### Critério de aceite

Uma atividade multimídia percorre criação, atribuição, envio, revisão e feedback com persistência.

## 8. Sprint 5 — Memória pedagógica e progresso

### Objetivo

Transformar histórico de aprendizagem em contexto estruturado e útil.

### Backlog

- registrar tópicos, objetivos, resultados, tentativas e feedback;
- permitir a Wander registrar forças, dificuldades e notas;
- distinguir fatos registrados, observações do professor e inferências geradas;
- exigir revisão para inferências relevantes;
- mostrar linha do tempo e resumo por aluno;
- mostrar progresso simples e encorajador ao aluno;
- mostrar visão pedagógica detalhada a Wander;
- preparar seleção explícita de contexto para recursos de IA.

### Critério de aceite

Wander consegue entender o histórico e o próximo passo de um aluno, e cada item relevante tem origem reconhecível.

## 9. Sprint 6 — Importação das atas Gemini

### Objetivo

Incorporar informações úteis de aulas registradas no Gmail/Drive sem transformar mensagens ou arquivos em memória automaticamente.

### Backlog

- definir consentimento, escopos mínimos e fontes elegíveis;
- conectar Gmail/Drive somente após aprovação técnica específica;
- localizar atas candidatas sem coleta indiscriminada;
- exibir origem, data e prévia;
- associar a ata ao aluno correto;
- propor extração de tópicos, dificuldades e próximos passos;
- permitir edição, aprovação ou descarte;
- incorporar somente os itens aprovados;
- registrar referência à origem e impedir duplicação;
- testar revogação de acesso e tratamento de erro.

### Critério de aceite

Uma ata elegível é localizada, revisada, associada e incorporada com confirmação de Wander, origem preservada e proteção contra duplicidade.

## 10. Sprint 7 — Weekly Challenge

### Objetivo

Criar uma rotina semanal visível e reutilizável de prática.

### Backlog

- criar e editar um desafio;
- definir período, público e objetivo;
- permitir adaptação individual;
- aceitar conteúdo multimídia;
- revisar antes da publicação;
- destacar o desafio vigente no dashboard do aluno;
- registrar participação, envio, resultado e feedback;
- encerrar e arquivar o desafio.

### Critério de aceite

Wander publica um desafio, o aluno participa e o ciclo permanece registrado no histórico.

## 11. Sprint 8 — Geração contextual de atividades

### Objetivo

Gerar rascunhos úteis a partir de contexto pedagógico deliberadamente selecionado.

### Backlog

- definir formulário de objetivo, formato e duração;
- selecionar aluno e fontes de contexto;
- mostrar claramente o contexto que será enviado;
- minimizar dados pessoais enviados ao provedor;
- gerar rascunho estruturado;
- permitir edição, regeneração e descarte;
- exigir ação explícita para salvar, atribuir ou publicar;
- permitir geração interativa somente para prática formativa de baixo risco no dashboard, sob as regras de inspeção do professor;
- exigir aprovação explícita de Wander antes de publicar assignments formais;
- registrar proveniência e versão aprovada;
- testar adequação a adulto/criança e aos dois perfis.

### Critério de aceite

Wander gera uma atividade coerente com contexto selecionado, consegue auditá-la e editá-la e mantém controle sobre sua publicação.

## 12. Sprint 9 — Assessment Generator auditável

### Objetivo

Gerar avaliações cuja qualidade, resposta esperada e pontuação possam ser verificadas pelo professor.

### Backlog

- selecionar objetivos, tópicos, contexto e formatos;
- configurar extensão, dificuldade e pontuação;
- gerar questões, respostas e critérios quando aplicável;
- mostrar o contexto utilizado;
- registrar proveniência por questão quando possível, vinculando aula/data, tópico, livro/unidade, material, atividade anterior, dificuldade/erro ou `Weekly Challenge`;
- permitir a Wander inspecionar a origem pedagógica de cada questão antes da aprovação;
- permitir editar questões, alternativas, gabarito, rubrica e pontos;
- validar total de pontos e consistência estrutural;
- manter rascunho separado da versão aprovada;
- exigir aprovação explícita antes de atribuir;
- registrar versão, autoria gerada e alterações relevantes;
- executar o assessment e registrar respostas e resultado.

### Critério de aceite

Wander consegue inspecionar, corrigir, aprovar e aplicar uma avaliação sem depender de conteúdo oculto ou publicação automática.

## 13. Sprint 10 — Qualidade e preparação do V1

### Objetivo

Validar o fluxo completo, proteger dados reais e preparar uma liberação controlada.

### Backlog

- testar o ciclo completo com os dois perfis;
- executar testes de autorização entre alunos;
- revisar acessibilidade e responsividade;
- revisar privacidade, retenção, exportação e exclusão;
- validar upload e acesso a mídia;
- validar falhas e indisponibilidade de integrações;
- verificar logs sem exposição de dados ou segredos;
- revisar backup e recuperação;
- atualizar documentação operacional;
- realizar piloto controlado e registrar feedback;
- corrigir bloqueadores antes de declarar o V1 pronto.

### Critério de aceite

Os critérios de sucesso do Blueprint são demonstrados em ambiente controlado, sem falhas críticas de privacidade, autorização ou perda de dados.

## 14. Backlog posterior ao V1

- contas de pais ou responsáveis, se aprovadas;
- notificações por e-mail;
- taxonomia avançada de erros;
- revisão personalizada automática mais sofisticada;
- relatórios avançados;
- geração sintética de listening por IA;
- biblioteca visual sofisticada e reutilizável;
- integração com múltiplos provedores de IA;
- recursos institucionais somente se um projeto separado for explicitamente criado.

Esses itens não são pré-requisitos para validar o V1.
