# Regras de Negocio e Dados

## 1. Objetivo

Consolidar uma primeira versao das regras de negocio e do entendimento do modelo de dados com base no comportamento sugerido pela interface.

## 2. Entidades principais inferidas

### 2.1 Usuario

- id_usuario
- nome
- email ou login
- perfil
- status
- data_ultimo_acesso

### 2.2 Cidadao

- id_cidadao
- nome_completo
- cpf
- data_nascimento
- telefone
- endereco
- bairro

### 2.3 Protocolo

- id_protocolo
- numero_protocolo
- data_criacao
- status_atual
- canal
- subcanal ou programa
- id_cidadao
- descricao
- codigo_cid
- percentual_elegibilidade
- usuario_responsavel
- situacao_ativa

### 2.4 Movimentacao

- id_movimentacao
- id_protocolo
- status_origem
- status_destino
- usuario_executor
- data_hora
- observacao

### 2.5 Feedback

- id_feedback
- tipo_feedback
- id_cidadao
- id_protocolo_relacionado
- descricao
- data_registro
- status

## 3. Regras de negocio inferidas

### RN-001. Todo registro deve possuir protocolo unico

Cada linha da grade deve corresponder a um identificador unico e rastreavel.

### RN-002. Todo protocolo deve estar vinculado a um cidadao

Como a tela exibe Nome/CPF, o caso aparentemente depende de identificacao da pessoa atendida.

### RN-003. Todo protocolo deve possuir status atual

O status e essencial para acompanhamento operacional.

### RN-004. O protocolo deve possuir data de criacao

A data e usada para ordenacao, auditoria e filtro.

### RN-005. O protocolo pode ser classificado por canal e subcanal

A tela sugere uma camada principal e outra complementar, como "Cadastro" e "Remedio em Casa".

### RN-006. A elegibilidade deve ser calculada ou atribuida

Todo registro exibido na grade possui percentual. Isso indica um motor de calculo, uma avaliacao humana parametrizada ou ambos.

### RN-007. Aprovacao e reprovacao dependem de criterios formais

Os status "Aprovados" e "Reprovados" sugerem decisao baseada em regras predefinidas.

### RN-008. Casos podem exigir recadastro

Quando dados estao incompletos, desatualizados ou inconsistentes, o fluxo pode direcionar o caso para recadastro.

### RN-009. Casos podem exigir segunda via

O sistema aparenta contemplar emissao, reemissao ou reprocessamento de documento, autorizacao ou item similar.

### RN-010. Registros podem ficar inativos

Deve haver regra para distinguir ativos de inativos.

### RN-011. Toda alteracao relevante deve gerar historico

Mudancas de status, elegibilidade, vinculo de cidadao ou classificacao devem ser rastreadas.

## 4. Regras de elegibilidade

Como a formula nao esta visivel, recomenda-se documentar a regra em separado. Ate a confirmacao oficial, pode-se considerar esta estrutura:

- documentacao apresentada;
- consistencia cadastral;
- enquadramento no programa;
- validacao clinica ou tecnica;
- prioridade assistencial;
- conformidade com regras vigentes.

Resultado esperado:

- percentual de elegibilidade;
- classificacao visual;
- possibilidade de aprovacao, reprovacao ou necessidade de complemento.

## 5. Dicionario inicial de campos da tela principal

| Campo | Descricao funcional | Tipo sugerido |
|---|---|---|
| status_icone | Indicador visual da situacao | Enum/Icone |
| protocolo | Identificador do caso | Texto/Numero |
| criado_em | Data e hora de criacao | DataHora |
| canal_principal | Categoria principal do fluxo | Texto |
| canal_secundario | Programa ou subcategoria | Texto |
| nome_cidadao | Nome completo | Texto |
| cpf | Documento de identificacao | Texto |
| mensagem | Descricao do item ou demanda | Texto longo |
| cid_codigo | Codigo complementar ou tecnico | Texto |
| elegibilidade_percentual | Score do caso | Decimal/Inteiro |
| ativo | Indicador de atividade do registro | Booleano |

## 6. Incertezas que devem ser fechadas

- O sistema e de saude, assistencia, ouvidoria ou um modelo hibrido?
- O "CID" e de fato codigo clinico?
- "Remedio em Casa" e canal, programa ou unidade administrativa?
- A elegibilidade e automatica, manual ou mista?
- Existe SLA por status ou tipo de caso?
