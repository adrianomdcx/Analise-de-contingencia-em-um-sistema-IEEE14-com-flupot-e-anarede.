# Estudo de fluxo de potência ótimo com FLUPOT

Esta pasta reúne os arquivos usados no estudo com **FLUPOT**. O objetivo é ajustar o ponto de operação da rede por fluxo de potência ótimo, usando os dados de rede e o diagrama do ANAREDE.

O estudo por análise de sensibilidade no ANAREDE está no relatório indicado no [README principal](../README.md), na branch `metodologia-sensibilidade-anarede`.

## O que é cada arquivo

| Arquivo | Para que serve |
| --- | --- |
| [`casobase.PWF`](casobase.PWF) | Dados do caso base em formato ANAREDE. |
| [`asp_ieee14.pwf`](asp_ieee14.pwf) | Dados da rede indicados como entrada na configuração do FLUPOT. |
| [`codigo_flupot.fpo`](codigo_flupot.fpo) | Comandos da otimização: objetivo MCNT, controles QGEN/VGEN/TAPC/PGEN e restrição FMVA. |
| [`fpo.stp`](fpo.stp) | Define os nomes dos arquivos de entrada e saída usados pelo FLUPOT. |
| [`asp_completo.out`](asp_completo.out) | Relatório da execução do FLUPOT V07.13.04, com os resultados, os avisos e o registro de convergência. |
| [`CORRIGIDO.PWF`](CORRIGIDO.PWF) | Caso corrigido salvo no estudo. |
| [`asp_cart_base.pch`](asp_cart_base.pch) | Exportação do caso em formato de dados de rede ANAREDE. |
| [`casobase.lst`](casobase.lst) | Configuração gráfica do diagrama no ANAREDE. |

## Para preparar uma nova execução

Use esta pasta como diretório de trabalho, mantendo juntos os arquivos relacionados. Em `fpo.stp`, a entrada de comandos aparece como `asp_ieee14.fpo`, mas o arquivo disponível aqui se chama `codigo_flupot.fpo`. Ajuste essa referência ao abrir o estudo ou use uma cópia com o nome esperado pela configuração.

As saídas estão configuradas para a pasta `saidas/`, que precisa existir no ambiente de execução. O relatório já disponível neste repositório está salvo diretamente nesta pasta, como `asp_completo.out`.

## Sobre o resultado salvo

O relatório registra que o FLUPOT alcançou convergência. Também informa que os comandos de rede DOPC, DCTE, DGER, DVCO e DMOT foram desconsiderados na leitura. Esses avisos ajudam a entender como a execução foi realizada.

Esse resultado corresponde ao estudo de otimização com FLUPOT. A avaliação de contingências N-1 por análise de sensibilidade está descrita no relatório do ANAREDE.
