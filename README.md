# Wander AI Studio

Wander AI Studio é um projeto pessoal e independente criado por Wander para apoiar seus alunos particulares.

O produto está sendo concebido como uma plataforma de aprendizagem com memória pedagógica: um ambiente no qual Wander poderá organizar alunos, materiais, atividades, mídia, avaliações, feedback e progresso sem depender de várias ferramentas desconectadas.

O produto possui dois modelos principais de atendimento: `English Course` e `School Support`. History e Language Arts são matérias válidas quando fazem parte de um atendimento particular em `School Support`.

Adoção institucional, administração escolar, fluxos institucionais, processos ligados ao emprego de Wander e funções escolares sem relação com seus atendimentos particulares permanecem fora do escopo. O produto não precisa registrar escola, instituição de origem, empregador ou associação institucional dos alunos.

## Estado atual

O código presente em `index.html`, `style.css` e `script.js` ainda é o protótipo legado do conceito anterior de "AI dashboard". Ele permanece somente como referência histórica e não representa a arquitetura nem a experiência aprovadas para o V1.

Neste momento, o repositório contém a documentação do Sprint 0. Nenhuma funcionalidade do V1 foi implementada, e ainda não houve migração para React nem configuração de Supabase, Vercel, Gmail API, Drive API ou OpenAI.

## Direção do V1

O V1 terá:

- dashboards personalizados e ativos para Wander e seus alunos;
- dois perfis de acompanhamento: `English Course` e `School Support`;
- suporte a materiais e conteúdos multimídia;
- memória pedagógica estruturada por aluno;
- experiências interativas orientadas por IA no dashboard do aluno;
- importação revisável das atas Gemini disponíveis no Gmail/Drive;
- `Weekly Challenge`;
- geração contextual de atividades;
- `Assessment Generator` com revisão e aprovação do professor.

## Alunos atuais

| Aluno | Grupo | Modelo | Nível/matérias | Material |
| --- | --- | --- | --- | --- |
| Regina | Adulta | `English Course` | C1 | *American English File 4* |
| Margarete | Adulta | `English Course` | B2 | *American English File 3* |
| Fernando | Adulto | `English Course` | B1 | *American English File 2* |
| Theo | Criança | `School Support` | History + Language Arts | Conforme a necessidade |
| Julia | Criança | `School Support` | Matérias escolares variáveis | Conforme a necessidade |

O Google Drive existente é uma fonte relevante dos materiais utilizados nos cursos *American English File 2, 3 e 4*, incluindo Student's Book, Workbook, áudio e vídeo. Esses materiais poderão ser catalogados e referenciados sem pressupor sua cópia para outro armazenamento e sempre respeitando direitos autorais e permissões.

## Idiomas

- Interface do professor: português.
- Interface padrão dos alunos: inglês.
- Interface padrão de Julia: português.
- Conteúdo pedagógico de inglês para Julia pode ser apresentado em inglês.

A preferência da interface pertence ao aluno, enquanto cada conteúdo ou atividade pode ter seu próprio idioma.

## Direção técnica

Supabase permanece como direção prevista para autenticação, autorização e dados operacionais e pedagógicos. O Google Drive continua sendo a biblioteca relevante dos materiais existentes. Uma eventual utilização do Supabase Storage será decidida no Sprint 1 para conteúdo próprio, uploads e recursos gerados.

O repositório Git canônico é `teacherwanderstayner-svg/wander.ai.studio-`. O repositório `wandermartins-prog/wander.ai.studio-` permanece somente como upstream histórico.

## Documentação

- `WANDER_AI_STUDIO_HANDOFF.md` — fonte autoritativa do projeto.
- `WANDER_AI_STUDIO_V1_BLUEPRINT.md` — escopo e definição aprovados para o V1.
- `WANDER_AI_STUDIO_V1_BACKLOG.md` — sequência de trabalho planejada após o Sprint 0.

## Regra de desenvolvimento

O desenvolvimento deve avançar em incrementos pequenos, completos e verificáveis. Novas ideias devem entrar no backlog sem alterar silenciosamente o escopo do sprint atual.
