# Análise de contingências com ANAREDE e FLUPOT

**[Ler o relatório: análise de sensibilidade no ANAREDE e correção de violações em contingências](https://github.com/adrianomdcx/Analise-de-contingencia-em-um-sistema-IEEE14-com-flupot-e-anarede./blob/metodologia-sensibilidade-anarede/relatorios/Metodologia_ANAREDE_Sensibilidade_e_Correcao_de_Violacoes_em_Contingencias.pdf)**

O relatório mostra como a análise de sensibilidade do ANAREDE pode ajudar a escolher ajustes de tensão, geração ativa e taps de transformadores para corrigir violações na rede. O estudo começa pelo caso base e depois avalia a saída de circuitos pelo critério N-1.

Também estão disponíveis os arquivos de um estudo feito com **FLUPOT**, voltado ao ajuste do ponto de operação por fluxo de potência ótimo. Os dois trabalhos estão identificados abaixo para facilitar a consulta.

## Onde encontrar o material

| Estudo | Material disponível |
| --- | --- |
| **ANAREDE: análise de sensibilidade e contingências** | [Relatório completo, com 56 páginas](https://github.com/adrianomdcx/Analise-de-contingencia-em-um-sistema-IEEE14-com-flupot-e-anarede./blob/metodologia-sensibilidade-anarede/relatorios/Metodologia_ANAREDE_Sensibilidade_e_Correcao_de_Violacoes_em_Contingencias.pdf) e [guia de leitura](https://github.com/adrianomdcx/Analise-de-contingencia-em-um-sistema-IEEE14-com-flupot-e-anarede./tree/metodologia-sensibilidade-anarede/relatorios), na branch `metodologia-sensibilidade-anarede`. |
| **FLUPOT: fluxo de potência ótimo** | Entradas, configurações e resultados na pasta [`estudo-flupot/`](estudo-flupot/), disponível na branch `main`. |

## Como foi feito o estudo com ANAREDE

A análise começa pela identificação das violações no caso base. Com as sensibilidades obtidas pela ferramenta EXSB, são escolhidos os controles que podem ajudar em cada situação. Depois de cada ajuste, o fluxo de potência é calculado novamente para verificar o efeito sobre o restante da rede.

Com o caso base ajustado, a ferramenta EXCA é usada para avaliar as contingências N-1. Quando surgem novas violações, o processo de análise e ajuste é repetido.

Foi possível corrigir o caso base e melhorar o comportamento da rede em diversas contingências. Algumas situações, porém, continuaram críticas com os controles disponíveis. Esses resultados e suas limitações são discutidos na conclusão do relatório.

## O que há nos arquivos do FLUPOT

**Os arquivos de simulação que já estavam neste repositório foram usados no estudo com FLUPOT.** Eles estão reunidos em [`estudo-flupot/`](estudo-flupot/), junto de um [guia com a função de cada arquivo](estudo-flupot/README.md).

Nesse estudo, o arquivo `codigo_flupot.fpo` define a função objetivo MCNT, os controles de geração e tensão, os taps e a restrição de carregamento FMVA. O resultado da execução está em `asp_completo.out`.

O relatório de análise de sensibilidade no ANAREDE e os arquivos de otimização com FLUPOT pertencem a abordagens diferentes. Por isso, cada conjunto tem sua própria descrição e localização.

## Sobre a rede utilizada

Os materiais usam a referência IEEE14, mas também incluem a barra 15. Os arquivos do FLUPOT trazem o título “SISTEMA 15 BARRAS”. Ao consultar ou repetir os estudos, considere os dados dos casos apresentados em cada material.

Trabalhos da disciplina Análise de Sistemas de Potência, UFRJ, 2026. A autoria e as referências do relatório estão no PDF.
