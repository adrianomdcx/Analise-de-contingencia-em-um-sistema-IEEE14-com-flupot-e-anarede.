# Arquivos do estudo realizado com FLUPOT

Esta pasta reúne os oito arquivos que já estavam no repositório. O estudo usa **FLUPOT** para ajustar o ponto de operação por fluxo de potência ótimo, com arquivos de rede e representação gráfica do ANAREDE.

O relatório sobre análise de sensibilidade no ANAREDE está identificado separadamente no [README principal](../README.md) e na branch `metodologia-sensibilidade-anarede`.

## Conteúdo

| Arquivo | Função no estudo com FLUPOT |
| --- | --- |
| [`casobase.PWF`](casobase.PWF) | Arquivo do caso base em formato ANAREDE. |
| [`asp_ieee14.pwf`](asp_ieee14.pwf) | Arquivo de rede indicado como entrada na configuração e no relatório do FLUPOT. |
| [`codigo_flupot.fpo`](codigo_flupot.fpo) | Comandos do estudo: objetivo MCNT, controles QGEN/VGEN/TAPC/PGEN e restrição FMVA. |
| [`fpo.stp`](fpo.stp) | Associação dos arquivos de entrada, configuração e saída usados pelo FLUPOT. |
| [`asp_completo.out`](asp_completo.out) | Relatório da execução do FLUPOT V07.13.04, incluindo dados, avisos e registro de convergência. |
| [`CORRIGIDO.PWF`](CORRIGIDO.PWF) | Caso corrigido salvo no estudo. |
| [`asp_cart_base.pch`](asp_cart_base.pch) | Exportação do caso em formato PWF, conforme o cabeçalho do arquivo. |
| [`casobase.lst`](casobase.lst) | Configuração gráfica do diagrama no ANAREDE. |

## Referências de arquivos na configuração

Os arquivos originais foram preservados sem alterações. Ao preparar uma nova execução:

- Use esta pasta como diretório de trabalho para manter juntos os arquivos relacionados.
- `fpo.stp` referencia `asp_ieee14.fpo`, enquanto o arquivo de comandos versionado se chama `codigo_flupot.fpo`. Configure a entrada para o nome existente ou prepare uma cópia com o nome esperado.
- A configuração referencia saídas em `saidas/`. Prepare esse diretório no ambiente de execução. O relatório de execução entregue no repositório está salvo diretamente nesta pasta como `asp_completo.out`.
- O relatório registra que os comandos de rede DOPC, DCTE, DGER, DVCO e DMOT foram desconsiderados na leitura pelo FLUPOT; esses avisos fazem parte da execução arquivada.

A convergência registrada em `asp_completo.out` descreve a execução do FLUPOT. Ela não substitui a avaliação de contingências N-1 apresentada no relatório da outra branch.
