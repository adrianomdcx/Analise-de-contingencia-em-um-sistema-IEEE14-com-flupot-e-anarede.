# Análise de contingências e correção de violações com ANAREDE e FLUPOT

## Relatório: metodologia por análise de sensibilidade no ANAREDE

**[Abrir o relatório completo em PDF (56 páginas)](https://github.com/adrianomdcx/Analise-de-contingencia-em-um-sistema-IEEE14-com-flupot-e-anarede./blob/metodologia-sensibilidade-anarede/relatorios/Metodologia_ANAREDE_Sensibilidade_e_Correcao_de_Violacoes_em_Contingencias.pdf)**

O relatório apresenta uma metodologia para corrigir violações operativas com o auxílio da análise de sensibilidade do ANAREDE. Os controles de tensão, geração ativa e taps de transformadores são ajustados de forma iterativa, com recálculo do fluxo de potência e avaliação de contingências pelo critério N-1.

**O PDF está na branch [`metodologia-sensibilidade-anarede`](https://github.com/adrianomdcx/Analise-de-contingencia-em-um-sistema-IEEE14-com-flupot-e-anarede./tree/metodologia-sensibilidade-anarede).** Os arquivos de simulação que já estavam neste repositório pertencem ao **estudo realizado com FLUPOT** e agora estão reunidos em [`estudo-flupot/`](estudo-flupot/).

## Onde encontrar cada estudo

| Material | Abordagem | Localização |
| --- | --- | --- |
| Relatório da metodologia com ANAREDE | Análise de sensibilidade, ajustes de controles e correção de violações no caso base e em contingências | [PDF completo](https://github.com/adrianomdcx/Analise-de-contingencia-em-um-sistema-IEEE14-com-flupot-e-anarede./blob/metodologia-sensibilidade-anarede/relatorios/Metodologia_ANAREDE_Sensibilidade_e_Correcao_de_Violacoes_em_Contingencias.pdf) · [Documentação do relatório](https://github.com/adrianomdcx/Analise-de-contingencia-em-um-sistema-IEEE14-com-flupot-e-anarede./tree/metodologia-sensibilidade-anarede/relatorios) |
| Arquivos e resultados do estudo com FLUPOT | Fluxo de potência ótimo, com função objetivo MCNT e restrição de carregamento FMVA | [Pasta `estudo-flupot/`](estudo-flupot/) na branch `main` |

## Metodologia documentada no relatório

1. Identificar as violações no caso base e examinar as sensibilidades no ANAREDE, usando a ferramenta EXSB.
2. Escolher os controles e aplicar ajustes de tensão em barras PV, geração ativa ou taps de transformadores.
3. Recalcular o fluxo de potência e reavaliar as violações após cada ajuste.
4. Analisar desligamentos de circuitos pelo critério N-1 com a ferramenta EXCA e avaliar novas medidas corretivas.

O documento mostra a correção do caso base e a melhora de diversas contingências. Também registra os limites da metodologia e situações que permaneceram críticas; portanto, seus resultados não equivalem à eliminação de todas as violações em N-1. O detalhamento está na conclusão do próprio relatório.

## Arquivos anteriores: estudo com FLUPOT

Os arquivos em [`estudo-flupot/`](estudo-flupot/) são as entradas, configurações e resultados do estudo com **FLUPOT**, utilizando arquivos de rede e representação gráfica do ANAREDE. Eles foram mantidos com seus nomes e conteúdos originais e movidos juntos para a mesma pasta.

O arquivo `asp_completo.out` identifica a execução do FLUPOT V07.13.04 e registra a convergência alcançada. Os comandos `DOBJ MCNT`, `DCON QGEN VGEN TAPC PGEN` e `DRES FMVA` estão em `codigo_flupot.fpo`. Consulte o [guia dos arquivos FLUPOT](estudo-flupot/README.md) para a função de cada arquivo e os nomes de entrada referenciados na configuração.

Os arquivos desse estudo com FLUPOT não são apresentados como os arquivos de entrada da metodologia por sensibilidade descrita no novo PDF. As duas abordagens ficam identificadas separadamente neste repositório.

## Identificação do sistema

O nome do repositório e a introdução do relatório usam a referência IEEE14. Os arquivos de rede do estudo com FLUPOT trazem o título “SISTEMA 15 BARRAS”, e o relatório também inclui a barra 15 nas análises. Para reproduzir os estudos, use a identificação e os dados de cada material, sem assumir que correspondem ao caso IEEE14 padrão sem alterações.

## Contexto acadêmico

Material da disciplina Análise de Sistemas de Potência, UFRJ, 2026. A autoria do relatório e as referências utilizadas estão preservadas no PDF.
