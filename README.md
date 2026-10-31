# Relatório de Prática Profissional – IFRN (Técnico Integrado)

Formulário web que ajuda estudantes dos **Cursos Técnicos de Nível Médio na forma Integrada do IFRN** a elaborar o **Relatório Final de Prática Profissional** e gera o documento em **Word (.docx)**, já formatado conforme as normas da ABNT, para revisão.

> [!IMPORTANT]
> **Ferramenta não oficial.** Este projeto é uma iniciativa independente de apoio e não substitui os modelos, orientações e procedimentos oficiais do IFRN. Ele foi feito para ajudar na elaboração do relatório de acordo com as regulamentações vigentes. Em caso de divergência, valem a regulamentação institucional, o Projeto Pedagógico do Curso (PPC) e as orientações da Coordenação do Curso e do(a) orientador(a).

---

## Por que usar

- **Você digita os dados uma vez só.** Nome, matrícula, curso, orientador(a) e período preenchem automaticamente a capa, a folha de rosto, o termo de validação e os quadros de identificação.
- **O formulário mostra só os campos da sua modalidade.** Você escolhe a modalidade, e o formulário pede apenas os dados e as seções que se aplicam a ela.
- **A formatação ABNT já vem pronta.** Fonte, margens, espaçamento, numeração progressiva das seções, quadros numerados com título e fonte, paginação e sumário automático.
- **Há orientações em cada campo.** Cada seção explica o que escrever, sem precisar apagar quadros de instrução depois.
- **Você confere antes de gerar.** A última etapa aponta campos vazios, o tamanho do resumo e a soma das cargas horárias, e mostra a estrutura (sumário) que será gerada.
- **Os seus dados ficam no seu computador.** Nada é enviado a servidores.

## Modalidades contempladas

Estas são as modalidades do art. 3º da Regulamentação da Prática Profissional Discente (Resolução nº 25/2019-CONSUP) que se aplicam aos cursos técnicos integrados:

| Bloco | Modalidade | Dados pedidos no formulário |
|---|---|---|
| A | Estágio (obrigatório ou não obrigatório) | Unidade concedente, supervisor(a), Termo de Compromisso |
| B | Programa de aprendizagem | Empresa contratante, entidade formadora, empregado(a) monitor(a), contrato |
| C | Atividade profissional efetiva | Tipo de vínculo, organização, cargo ou função, chefia |
| D | Atividades relacionadas ao empreendedorismo | Tipo (MEI, empresa júnior, miniempresa, incubada, hotel de projeto), nome, CNPJ/CCMEI |
| E | Prática como componente curricular – projetos | Tipo (integrador, ensino, pesquisa, extensão), título, nº no SUAP, edital, coordenador(a), participação e demais integrantes da equipe |
| F | TAL ou Programa de Apoio à Formação Estudantil | Programa e edital, disciplina ou laboratório, docente responsável |
| G | Serviço voluntário (Lei nº 9.608/1998) | Entidade, responsável, Termo de Adesão |

**Prática combinada.** É possível marcar mais de uma modalidade. Nesse caso, o relatório ganha:
- uma subseção de caracterização para cada modalidade;
- um quadro com a carga horária de cada atividade, que é a base da média ponderada do art. 6º, § 1º;
- um título temático sugerido;
- se for o caso, um(a) orientador(a) por atividade, cada um com a sua assinatura no termo de validação.

**Projetos em equipe.** O relatório continua **individual**. A equipe é identificada no Quadro 1, e o estudante descreve a sua própria participação.

## Estrutura do relatório gerado

**Elementos pré-textuais**
- Capa
- Folha de rosto
- Termo de validação pelo(a) orientador(a)
- Agradecimentos (opcional)
- Resumo e palavras-chave
- Lista de abreviaturas e siglas (opcional)
- Sumário

**Elementos textuais**
1. Introdução
2. Identificação da prática profissional (Quadro 1 e, se combinada, Quadro 2)
3. Caracterização do contexto da prática profissional (subseções conforme a modalidade)
4. Atividades desenvolvidas: plano de atividades × execução, descrição das atividades, resultados e produtos
5. Relação entre teoria e prática
6. Análise crítica da experiência
7. Considerações finais

**Elementos pós-textuais**
- Referências (em ordem alfabética automática)
- Anexo A – Plano de Atividades deferido
- Anexo B – Documentos comprobatórios, com a lista dos documentos usuais da modalidade

Campos não preenchidos saem **destacados em amarelo** no Word, para facilitar a revisão.

## Como usar (estudantes)

1. Abra o formulário no navegador. Se quiser ver como funciona primeiro, use **Carregar exemplo fictício**.
2. Preencha as etapas na ordem que preferir. O progresso de cada etapa aparece no menu lateral.
3. O rascunho é salvo automaticamente **neste navegador**. Para continuar em outro computador ou enviar ao orientador(a), use **Salvar rascunho**, que baixa um arquivo `.json`. Depois, abra esse arquivo com **Abrir rascunho**.
4. Na etapa **Revisar e gerar**, confira os pontos indicados e clique em **Gerar relatório (.docx)**.
5. No Word:
   - atualize o sumário: botão direito sobre ele > *Atualizar campo* > *Atualizar o índice inteiro*;
   - insira fotos, organogramas e gráficos, com título e fonte;
   - cole o Plano de Atividades e os comprovantes nos anexos;
   - revise o texto.
6. Entregue ao seu orientador(a), que preenche e assina o termo de validação.

> [!TIP]
> Fotos, organogramas e gráficos são inseridos **depois, no Word**. O formulário cuida do texto, dos quadros e da formatação.

### Dependências externas

O arquivo carrega dois recursos por CDN:

| Recurso | Origem | Uso |
|---|---|---|
| [docx](https://github.com/dolanmiu/docx) **9.5.1** | `cdn.jsdelivr.net` | Geração do arquivo `.docx` no navegador |
| Atkinson Hyperlegible, Literata e IBM Plex Mono | Google Fonts | Tipografia da interface |

Se a rede bloquear esses endereços, as fontes caem para as do sistema sem prejuízo. A biblioteca **docx** é necessária para gerar o arquivo. Para uso totalmente offline, baixe `dist/index.iife.js` da versão 9.5.1 e referencie o arquivo localmente.

## Privacidade

- Todo o processamento acontece **no navegador** do estudante.
- O formulário não usa banco de dados, não exige login e não envia dados a terceiros.
- O rascunho automático usa o armazenamento local do navegador (`localStorage`). Ele pode ser apagado a qualquer momento pelo botão **Limpar relatório**. Em computadores compartilhados, recomenda-se limpar o formulário ao terminar.

## Base normativa e técnica

- IFRN. **Resolução nº 25/2019-CONSUP**: Regulamentação da Prática Profissional Discente.
- **Projeto Pedagógico do Curso (PPC)** de cada curso: carga horária e modalidades admitidas.
- ABNT **NBR 10719** (relatório técnico e/ou científico), **NBR 6023** (referências), **NBR 10520** (citações), **NBR 6024** (numeração progressiva) e **NBR 6027** (sumário).
- Lei nº 11.788/2008 (estágio), Lei nº 9.608/1998 (serviço voluntário) e Lei Complementar nº 128/2008 (MEI).

> [!NOTE]
> A Organização Didática do IFRN está em revisão. Quando a nova versão e a Instrução Normativa sobre a prática profissional forem aprovadas, a ferramenta deverá ser atualizada (nomenclatura das modalidades, requisitos e referências normativas).

## Limitações conhecidas

- Não insere imagens. Figuras são incluídas no Word, após a geração.
- O sumário é um campo do Word e precisa ser atualizado ao abrir o documento.
- Não há edição simultânea: cada estudante preenche o próprio relatório.
- Modalidades exclusivas de licenciaturas e de cursos superiores (art. 3º, V-b a V-d, VII, VIII e IX) não são contempladas.

## Materiais complementares

Junto com o formulário, este repositório pode disponibilizar:

- **Template em Word** (`Template_Relatorio_Pratica_Profissional_Tecnico_Integrado.docx`), para quem preferir preencher direto no editor de texto.
- **Ficha de avaliação para orientadores** (`Ficha_Avaliacao_Orientador_Pratica_Profissional.docx`), uma sugestão de critérios e cálculo da nota ponderada. Não faz parte do material dos estudantes.

## Contribuições

Sugestões e correções são bem-vindas, principalmente de docentes, coordenações de curso e estudantes. Abra uma *issue* descrevendo:
- o problema ou a sugestão;
- a modalidade envolvida;
- se possível, o trecho da norma ou do PPC que fundamenta o ajuste.

## Licença

Defina a licença do repositório (sugestão: [MIT](https://opensource.org/license/mit)).
A marca do IFRN pertence à instituição, e o seu uso segue as normas institucionais de identidade visual.
