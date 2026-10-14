# Otimização do fluxo de potência em uma rede de 15 barras

Este repositório reúne os arquivos de um trabalho da disciplina Análise de Sistemas de Potência (EEE581), realizado no primeiro semestre de 2026 com a professora Carmen Lúcia. O estudo usa ANAREDE e FLUPOT para ajustar o ponto de operação da rede, reduzindo o número de ações de controle e respeitando os limites definidos para geração e carregamento dos circuitos.

## Arquivos

- `casobase.PWF`: arquivo do caso-base.
- `asp_ieee14.pwf`: arquivo de rede indicado como entrada no relatório do FLUPOT.
- `codigo_flupot.fpo`: configuração do estudo, com a função objetivo MCNT, os controles considerados e a restrição de carregamento FMVA.
- `fpo.stp`: configurações auxiliares de geração e limites de potência reativa.
- `asp_completo.out`: relatório da execução. Ele registra convergência, mas também avisa que alguns comandos do arquivo de rede foram desconsiderados; confira esses avisos antes de usar os resultados.
- `CORRIGIDO.PWF`: caso salvo com os ajustes do fluxo de potência ótimo.
- `asp_cart_base.pch`: exportação do caso-base em formato PWF, conforme indicado no cabeçalho.
- `casobase.lst`: configuração gráfica do diagrama, incluindo cores e posições dos elementos.

## Observações sobre os arquivos

Os cabeçalhos dos arquivos PWF identificam o sistema como uma rede de 15 barras, embora o nome do repositório e alguns nomes de arquivo mencionem IEEE 14 barras. O relatório disponível também descreve uma execução do caso-base; não encontrei nele a identificação de casos de contingência.

Há ainda uma diferença de nomes: `asp_completo.out` registra a leitura de `asp_ieee14.fpo`, mas esse arquivo não está no repositório. A configuração FPO incluída aqui se chama `codigo_flupot.fpo`. O relatório também informa que comandos como DOPC, DCTE e DGER foram desconsiderados. Esses pontos merecem conferência antes de tentar reproduzir a execução ou atribuir os resultados a esta configuração.
