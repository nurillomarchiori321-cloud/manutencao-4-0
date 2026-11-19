# Manutec | Consolidação das Pesquisas Individuais

**Projeto:** P4 - Manutenção 4.0 (Manutec)  
**Equipe:** D  
**Unidade:** 3 - Gestão de Projetos  
**Professor:** Edson Vaz Lopes

Este documento reúne as contribuições individuais sobre riscos, liderança e pessoas, mudanças, métricas, comunicação e qualidade. As recomendações e valores propostos nas pesquisas são identificados como propostas; não representam aprovação formal nem resultados de testes que ainda não foram apresentados.

## 1. Contexto do projeto e contribuições

O Manutec propõe digitalizar o processo de manutenção de uma planta-piloto: identificar equipamentos, abrir e priorizar ordens de serviço, registrar tempo, peças, fotos e evidências em campo, consultar histórico e painel gerencial e integrar os dados ao ERP.

O planejamento da Unidade 2 considera 16 semanas operacionais, com limite de pacote de 24 semanas. A estimativa de custo é de R$ 253.320, a contingência original é de R$ 12.000, a linha de base é de R$ 265.320, a reserva gerencial é de R$ 9.680 e o teto é de R$ 275.000. A integração com o ERP está prevista para depois da validação do piloto em M1 e da autorização correspondente.

| Integrante | Contribuição consolidada |
|---|---|
| Murillo Marchiori | Identificação, análise e resposta aos riscos, com foco em conectividade |
| Paulo Vitor Hobold | Liderança, resistência de técnicos experientes e gestão de conflitos |
| Vitor Devegili | Controle de mudanças e qualidade |
| João Fabijak | Métricas, indicadores e relação com prazo e custo |
| Milena Kostiw Vier | Comunicação e engajamento dos stakeholders |

## 2. Riscos

O gerenciamento de riscos deve ser contínuo: identificar, analisar, planejar respostas, executá-las e monitorar os gatilhos. A matriz abaixo reúne os riscos registrados por Murillo. Probabilidades e impactos são estimativas da equipe; os riscos R5 a R8 precisam de validação.

| ID | Risco | Probabilidade e impacto | Nível | Resposta e responsável |
|---|---|---|---:|---|
| R1 | Perda frequente de conectividade em áreas críticas | Alta, 70%; impacto alto no caminho crítico; VME proposto de R$ 7.000 | 9 - prioritário | Mitigar e transferir parte da obrigação ao fornecedor. Responsável: GP |
| R2 | Retrabalho na integração com o ERP | Média, 40%; impacto estimado de R$ 15.000 | 6 - prioritário | Validar interfaces cedo e reservar esforço para retrabalho. Responsável: EI |
| R5 | Atraso de pré-requisitos externos P1/P2 ou do contrato do ERP P3 | Média; impacto alto por atingir o caminho crítico | 6 - prioritário | Definir marcos contratuais e cobrar semanalmente os fornecedores. Responsável: GP |
| R8 | Funcionamento offline falha em campo, como risco secundário de R1 | Média; impacto alto | 6 - prioritário | Testar offline e sincronização em áreas de baixa cobertura. Responsáveis: D1 e AT |
| R3 | Treinamento adicional necessário para adoção | 25%; impacto médio estimado de R$ 8.000 | 4 - moderado | Validar material com o EM e observar a execução dos cenários de aceite. Responsável: AN |
| R6 | Backlog excede as horas disponíveis | Média; impacto médio | 4 - moderado | Rever o backlog no M0 e acompanhar a velocidade nas semanas S1-S4. Responsáveis: GP e AN |
| R7 | EM ou TS indisponível para aceite e validação | Média; impacto médio | 4 - moderado | Agendar validações com antecedência e confirmar quórum. Responsável: GP |
| R4 | Atraso ou reposição de materiais e dispositivos | 20%; impacto baixo, estimado em R$ 5.000 | 1 - baixo | Confirmar entregas e acionar o fornecedor diante de atraso. Responsável: GP |

Na matriz adotada, impacto baixo corresponde a menos de R$ 6.000; médio, de R$ 6.000 a R$ 11.999; e alto, a partir de R$ 12.000 ou a qualquer efeito no caminho crítico. Nível 6 ou superior é prioritário. R1, R2, R5 e R8 são os riscos prioritários.

### R1 - Conectividade

Os testes preliminares indicam perda frequente de sinal em áreas críticas, mas a rede do piloto ainda não foi instalada. Por isso, a pesquisa trata o evento como risco com probabilidade revisada, e não como falha definitiva já confirmada. A estimativa sobe de 30% para 70%, sobre impacto financeiro de R$ 10.000: o VME passa de R$ 3.000 para R$ 7.000. O gatilho é uma área crítica sem sinal no levantamento ou no teste de aceite.

Resposta proposta:

1. Antes da S1, mapear as áreas críticas com o engenheiro de manutenção (EM) e combinar um nível mínimo de cobertura.
2. Incluir no contrato da rede teste de cobertura e correção de pontos sem sinal dentro do escopo contratado. Mudança de preço depende de aprovação.
3. Implementar fila offline e reenvio automático, com trabalho previsto entre S5 e S7.
4. Testar em campo sem conexão e em áreas de baixa cobertura entre S5 e S9; o técnico de segurança (TS) valida as condições de campo.
5. Concluir o aceite da rede e dos dispositivos até o fim da S9.
6. Se o gatilho persistir, reposicionar ou ampliar pontos de acesso usando contingência. Se isso não resolver, restringir o piloto às áreas cobertas; essa redução de escopo exige aprovação de Paulo Vitor Hobold e decisão antes da atividade F.

O offline reduz o efeito das quedas, mas cria risco secundário de falha na sincronização. O piloto também não pode interromper a produção. Conectividade e sincronização devem, portanto, ser monitoradas em conjunto, sem presumir que tenham a mesma causa.

### Efeito financeiro proposto para R1

Se a revisão de R1 for aprovada, a contingência total passa de R$ 12.000 para R$ 16.000. A linha de base passaria de R$ 265.320 para R$ 269.320 e a reserva gerencial dentro do teto cairia de R$ 9.680 para R$ 5.680. Esta é uma proposta de Murillo, não uma linha de base aprovada.

No cenário de corte orçamentário de 10% analisado por Vitor, o teto seria R$ 247.500. Com custo estimado de R$ 233.320 e contingência revisada de R$ 16.000, a linha de base seria R$ 249.320, excedendo o teto em R$ 1.820. Para manter também uma reserva gerencial de R$ 2.180, seriam necessários R$ 4.000 adicionais. Esse cenário depende da validação das estimativas e exige renegociação ou faseamento de escopo; reduzir a contingência sem reavaliar os riscos ocultaria a exposição.

## 3. Liderança e pessoas

O registro de tempo, peças, fotos e evidências pode ser interpretado por técnicos experientes como fiscalização individual. A resistência deve ser tratada como uma preocupação a compreender e negociar, não como falta de vontade. Se os usuários não registrarem as informações, o histórico e o painel perdem valor, e o aceite do piloto e a decisão sobre a integração ficam sem base.

Práticas propostas por Paulo:

- Explicar que os dados servem ao histórico dos equipamentos, à priorização e ao planejamento, e não à avaliação punitiva individual. Formalizar esse entendimento com a organização cliente.
- Demonstrar benefícios diretos para os técnicos: consulta ao histórico, redução de retrabalho e evidências que também dão respaldo ao profissional.
- Convidar técnicos experientes a validações semanais desde a R1 e ao teste offline em campo, reconhecendo seu conhecimento e usando suas sugestões no desenho do sistema.
- Manter o fluxo essencial e o registro simples, inclusive em modo offline, para que a ferramenta não aumente desnecessariamente o esforço de campo.
- Distribuir responsabilidades conforme competência, disponibilidade e autoridade. O EM e o TS atuam como consultores e validadores; o aceite operacional e a validação de segurança devem respeitar os papéis definidos na RACI.
- Treinar mecânicos e operadores antes do piloto e verificar se conseguem executar os cenários acordados sem defeitos bloqueadores.

A resistência à adoção se relaciona ao risco de treinamento R3 e pode afetar prazo, qualidade dos dados e aceite do piloto. A atividade de comunicação e gestão da mudança (H) e a de treinamento e material de apoio (G), previstas originalmente na semana 10, devem explicar o propósito do sistema, os registros exigidos e o uso dos dados.

## 4. Mudanças

### Solicitação SM-01

| Campo | Registro consolidado |
|---|---|
| Origem | Solicitação da direção, conforme evento da seção 6 do edital |
| Mudança | Aprovação eletrônica de peças e fotos obrigatórias nas ordens de manutenção |
| Benefício pretendido | Aumentar a rastreabilidade das decisões sobre peças e a qualidade das evidências |
| Situação nas pesquisas | Em análise; não há aprovação formal registrada |
| Regras que precisam de decisão | Aprovador e substituto; peças sujeitas à aprovação; prazo de resposta; momento em que a foto é exigida; requisitos da imagem; urgências e operação sem rede |

Para detalhar a proposta, Vitor sugere aprovar a solicitação de peças antes da liberação ou uso e exigir foto válida antes de concluir a ordem. O edital não fixa essas etapas; elas precisam ser confirmadas com direção, manutenção e segurança.

### Impactos e estimativa

A mudança acrescenta fluxo de solicitação, decisão, permissões e histórico de aprovação; torna obrigatória a validação das fotos e afeta ordens, execução em campo, histórico, treinamento, comunicação, piloto e integração com o ERP. Como anexar fotos e registrar peças já pertenciam ao escopo, deve-se estimar o trabalho adicional sem orçar novamente a funcionalidade que já existia.

As atividades B, C, D, G/H, F e E são apontadas como críticas no plano de 16 semanas. Não há evidência de capacidade livre que permita absorver o esforço sem efeito no prazo. As oito semanas até o limite de 24 semanas não são folga automática nem trabalho contratado.

Como método de estimativa proposto, o custo incremental líquido seria:

**ΔC = 80hGP + 45hDev + 40hAN + 40hAT + 70hEI + Cexterno - Ceconomia**

As horas representam esforço adicional por papel e as taxas são em reais por hora. Cexterno inclui apenas custos novos; Ceconomia, trabalho opcional realmente retirado. As horas da mudança, a carga disponível e o custo final ainda não foram informados, então não há estimativa aprovada de prazo ou custo.

### Backlog proposto após aprovação

| Item | Entrega | Critério de aceite proposto |
|---|---|---|
| M-01 - Solicitação de peças | Vincular peças, quantidades, motivo e solicitante à ordem; exibir estados pendente, aprovada e rejeitada | Solicitação válida fica pendente; só a decisão autorizada libera o fluxo definido |
| M-02 - Decisão eletrônica | Perfil de aprovador, decisão, data, responsável e justificativa de rejeição | Usuário sem permissão não aprova; alteração relevante em peça ou quantidade exige nova decisão e preserva o histórico |
| M-03 - Foto obrigatória | Vincular evidência válida à ordem e verificar a exigência antes da conclusão | Conclusão sem foto válida é impedida, inclusive por chamada direta ao servidor |
| M-04 - Operação offline | Guardar rascunho, fotos e fila de envio; mostrar o estado da sincronização | Queda de rede não perde evidência nem aprova a solicitação; reenvio não duplica registros nem confirma pendências |
| M-05 - Histórico e ERP | Registrar trilha de decisões e definir estados e dados conciliados com o ERP | Autor e decisão são rastreáveis; integração ponta a ponta ocorre somente após M1 e autorização |
| M-06 - Adoção e apoio | Atualizar manual, treinamento, mensagens e orientação a aprovadores e técnicos | Participantes executam solicitação, aprovação/rejeição, foto e recuperação de falha de rede nos cenários acordados |

### Governança da mudança

O fluxo recomendado é registrar a solicitação, avaliar impactos, decidir aprovar/rejeitar/adiar, atualizar os artefatos e só então implementar e verificar. Paulo Vitor Hobold aprova mudanças de escopo conforme a RACI da Unidade 2. A Ciser autoriza o uso da reserva gerencial e o aumento do teto. A aprovação do projeto para implantar a mudança é diferente da aprovação operacional de cada pedido de peças.

Depois da decisão, atualizar escopo/EAP, backlog, releases, cronograma, orçamento, RACI, riscos, testes, comunicação e treinamento. O contrato de treinamento de R$ 18.000 cobre o treinamento original; o fornecedor deve confirmar se o conteúdo adicional está incluído.

## 5. Métricas

João propõe um painel semanal com indicador, fórmula, responsável, origem do dado, período e ação associada. Toda comparação deve usar a mesma data de corte. Percentuais acumulados devem ser calculados pela soma dos numeradores dividida pela soma dos denominadores, não pela média simples de amostras de tamanhos diferentes.

| Indicador | Situação e definição proposta | Leitura e ação |
|---|---|---|
| Falha de sincronização | 7% foi mencionado nos materiais, mas faltam janela, numerador, denominador e amostra. Proposta: operações únicas com erro ou sem confirmação até 5 minutos após o retorno da conexão / operações válidas elegíveis × 100 | Recuperar logs, definir se a falha representa perda ou apenas atraso e segmentar por área, dispositivo, versão e condição da rede |
| Sucesso no prazo | Proposta inicial: operações confirmadas no servidor em até 5 minutos / operações elegíveis × 100; meta de pelo menos 98% em janela de 7 dias, ainda a validar com o EM | Se a definição dos 7% for comparável, o sucesso seria 93%, cinco pontos percentuais abaixo da meta proposta |
| Integridade dos registros | Comparar origem e destino por identificador único | Critério de aceite proposto: zero perda e zero duplicação não resolvida; investigar qualquer ocorrência |
| Fila offline | Quantidade e idade do registro pendente mais antigo, distinguindo dispositivo ainda sem rede de conexão já restabelecida | AT coleta; D1 investiga atrasos; GP acompanha impacto no aceite |
| Adesão ao piloto | 48% foi reportado, sem definição de período, população ou denominador | Validar como a adesão foi calculada antes de comparar ou definir ação |
| Ordens incompletas | 22% foi reportado, sem lista de campos obrigatórios, período ou denominador | Definir quais campos caracterizam incompletude e calcular sobre ordens válidas do mesmo período |
| Prazo | IDP = VA / VP, comparando valor agregado e valor planejado na mesma data | Abaixo de 1 indica menos trabalho agregado que o planejado; não converter diretamente em semanas de atraso |
| Custo | IDC = VA / CR, onde CR é custo real acumulado | Abaixo de 1 indica desempenho de custo desfavorável; registrar custos reais, sem usar o orçamento total como custo realizado |
| Previsão de custo final | Custo real acumulado + estimativa do custo restante | Comparar com a linha de base vigente e o teto; separar custos realizados, compromissos e reservas para evitar dupla contagem |
| Marcos | Previsão comparada com M1 ao fim da S12 e M2 ao fim da S16 | Reavaliar sucessores se C, D ou F atrasarem; P1 e P2 têm uma semana de folga no plano citado |

Os valores 48%, 7% e 22% são sinais que exigem diagnóstico, não uma descrição completa da qualidade do piloto. O complemento de 7% só equivale a 93% de sucesso se todas as operações tiverem classificação binária comparável. Uma operação pendente ou tentativas repetidas podem mudar essa interpretação. Sem operações elegíveis, registrar “sem dados”, nunca 0% de falhas.

O plano da Unidade 2 não fornece VP, VA e CR acumulados da execução; portanto, as pesquisas não calculam IDP ou IDC reais. Também não há base para afirmar que a meta de 98% foi aprovada. João consolida o painel acadêmico; no projeto, GP coordena as respostas e o EM valida o aceite operacional.

## 6. Comunicação e engajamento

O evento de comunicação é a reclamação da segunda planta, que afirma que as decisões estão sendo tomadas apenas pela equipe da primeira unidade. A segunda planta deve ser ouvida porque pode ser afetada pelas decisões, embora o escopo inicial continue sendo um piloto em uma planta.

| Público | Ação de comunicação e participação |
|---|---|
| Representantes das duas plantas | Reunir representantes para apresentar andamento e ouvir necessidades; a frequência deve ser acordada |
| Profissionais da segunda planta | Disponibilizar canal para dúvidas, dificuldades e sugestões; registrar e encaminhar necessidades para análise e priorização da gerência de manutenção |
| Mecânicos e operadores da planta-piloto | Realizar validações semanais; explicar finalidade e uso dos dados; registrar sugestões e dificuldades |
| Aprovadores e direção | Comunicar as regras da SM-01, os impactos e as decisões de aprovação; registrar decisões e responsáveis |
| Todos os stakeholders envolvidos | Compartilhar atas, decisões e atualizações do projeto com as duas unidades |

Incluir a segunda planta em consultas e validações não autoriza expandir o sistema para essa unidade. Necessidades identificadas devem ser registradas e priorizadas; qualquer expansão continua sujeita ao controle formal de escopo. A participação também ajuda a antecipar requisitos sem comprometer o piloto.

A comunicação sobre registros, fotos e histórico deve reduzir receio de fiscalização punitiva e explicar os benefícios práticos para os técnicos. O retorno dos usuários deve alimentar backlog, treinamento, riscos e critérios de aceite.

## 7. Qualidade

A qualidade depende de requisitos claros e critérios de aceite verificáveis. A garantia da qualidade atua nos processos que dão confiança de que os requisitos serão atendidos; o controle da qualidade verifica os resultados produzidos. O PDCA pode orientar o ciclo: planejar regras e critérios, executar a versão autorizada, verificar testes e métricas e agir sobre os desvios.

### Testes propostos para SM-01

| Cenário | Resultado esperado e evidência |
|---|---|
| Aprovar e rejeitar peças | Só aprovador autorizado decide; rejeição mantém o bloqueio previsto; registrar responsável, data, decisão e justificativa |
| Usuário sem permissão | Tentativa de aprovação não autorizada é recusada |
| Alterar após aprovação | Mudança relevante em peça ou quantidade exige nova decisão e conserva o histórico anterior |
| Concluir sem foto | Ordem não é concluída sem evidência válida, inclusive por chamada direta ao servidor; a imagem fica vinculada à ordem correta |
| Perder e recuperar a rede | Foto e registro ficam preservados offline; reenvio não duplica; estado pendente não aparece como aprovado ou concluído no servidor |
| Regressão | Revalidar abertura de ordens, peças, tempo, histórico e painel |
| Integração com ERP | Executar teste ponta a ponta somente após M1 e autorização formal; verificar conciliação de falhas e reenvios |

Cada evidência de teste deve registrar versão, entrada, resultado esperado, resultado obtido e defeitos. A liberação proposta exige aprovação dos cenários críticos acordados, nenhum defeito bloqueador aberto e evidências de integridade e uso em campo aceitas. O EM valida aderência operacional; o TS valida segurança em campo; o GP coordena o aceite.

Treinamento também deve ser avaliado pela execução dos cenários, não apenas pela presença. Mecânicos e operadores praticam pedido de peças, consulta de estado, fotos úteis e pendências de sincronização. Aprovadores praticam fila, autorização, rejeição, justificativa e substituição em ausências. O procedimento para urgências deve ser acordado com manutenção e segurança.

## 8. Integração e decisões pendentes

As contribuições convergem em uma sequência de trabalho:

1. Confirmar período, numerador, denominador e origem dos indicadores de 48%, 7% e 22%; separar falha, atraso e perda de dados.
2. Mapear cobertura das áreas críticas e confirmar o critério mínimo de rede com EM, TI e fornecedor.
3. Encaminhar SM-01 para decisão e definir regras de aprovação, fotos, urgências e operação sem rede.
4. Estimar capacidade, prazo e custo da mudança; decidir se contingência, orçamento e escopo precisam ser atualizados.
5. Atualizar os artefatos afetados e preparar testes, comunicação e treinamento para o escopo autorizado.
6. Validar a solução com técnicos e operadores, envolver representantes da segunda planta e manter explícito o limite do piloto.
7. Decidir o aceite em M1 com base em testes e indicadores; iniciar a integração com o ERP apenas após validação e autorização.

Antes de tratar as propostas como linha de base, a equipe ainda precisa confirmar o critério mínimo de cobertura, as definições dos indicadores, a memória da contingência revisada, o custo e a capacidade da SM-01, as regras operacionais de aprovação e fotos, e a frequência de comunicação com a segunda planta.

## 9. Documentos de origem

- [Pesquisa individual de riscos - Murillo Marchiori](Pesquisa_Individual_Riscos_Murillo_Marchiori.pdf)
- [Pesquisa de liderança - Paulo Vitor Hobold](Pesquisa_liderança_paulo_v_hobold.pdf)
- [Pesquisa de métricas e cronograma - João Fabijak](Pesquisa_Metricas_Joao_Fabijak_e_Cronograma_U3.pdf)
- [Pesquisa de comunicação - Milena Kostiw Vier](Pesquisa_individual_Comunicação_MilenaVier.pdf)
- [Pesquisa de mudanças e qualidade - Vitor Devegili](Pesquisa_Mudancas_Qualidade_Manutec_Vitor_Devegili.pdf)
- [Relatório da Unidade 2 - planejamento, cronograma e orçamento](../n2-planejamento/Relatorio_Unidade_2_Manutencao_4_0.pdf)
- [README do repositório Manutec](../README.md)
