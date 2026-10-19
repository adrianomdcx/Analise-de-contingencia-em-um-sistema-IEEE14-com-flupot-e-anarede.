# Metodologia ANAREDE: sensibilidade e correção de violações em contingências

**[Abrir o relatório completo em PDF (56 páginas)](Metodologia_ANAREDE_Sensibilidade_e_Correcao_de_Violacoes_em_Contingencias.pdf)**

Este relatório apresenta uma metodologia para corrigir violações operativas com a análise de sensibilidade do **ANAREDE**. O estudo parte da correção do caso base e avalia os ajustes necessários após contingências N-1, considerando seus efeitos sobre o restante da rede.



## Como o estudo foi conduzido

As sensibilidades ajudam a identificar quais controles têm maior influência sobre as violações de tensão, carregamento e geração de potência reativa. A partir delas, o estudo orienta ajustes de tensão em barras PV, geração ativa e taps de transformadores.

Após cada alteração, o fluxo de potência é recalculado para verificar o efeito sobre toda a rede. Esse processo é repetido até corrigir o caso base e, depois, avaliar os desligamentos de circuitos pelo critério N-1. As ferramentas EXSB e EXCA do ANAREDE apoiam, respectivamente, a análise de sensibilidade e a avaliação das contingências.

## Guia de leitura

| Conteúdo | Páginas do PDF |
| --- | --- |
| EXSB e interpretação das sensibilidades | 6 a 9 |
| Estratégia de correção e fluxograma | 10 e 11 |
| EXCA e análise de contingências N-1 | 22 |
| Exemplos das contingências 6-11 e 6-12 | 29 a 32 |
| Resultados finais e limitações | 55 |

As páginas acima seguem a contagem do leitor de PDF, incluindo a capa como página 1; elas diferem da numeração impressa.

## Resultados e limitações

O estudo obteve um caso base sem violações e melhorou a condição de operação em diversas contingências. Também mostrou que o controle com maior sensibilidade nem sempre pode ser usado: seu ajuste pode atingir um limite ou provocar novas violações em outros pontos da rede.

Algumas contingências permaneceram críticas. Os casos **9-14, 13-14 e 4-15** não foram contidos com os controles disponíveis. Já **5-6 e 5-15** permaneceram acima dos limites normais, embora os autores os tenham considerado contidos ao avaliar os limites emergenciais.

## Estudo com FLUPOT

O estudo de fluxo de potência ótimo realizado com **FLUPOT**, que já estava neste repositório, está documentado em [`estudo-flupot/`](../estudo-flupot/README.md). A descrição dos arquivos dessa pasta se refere ao estudo de otimização com FLUPOT; a metodologia discutida neste PDF usa a análise de sensibilidade no ANAREDE.

[Voltar à apresentação do repositório](../README.md).
