# Metodologia ANAREDE: sensibilidade e correção de violações em contingências

**[Abrir o relatório completo em PDF (56 páginas)](Metodologia_ANAREDE_Sensibilidade_e_Correcao_de_Violacoes_em_Contingencias.pdf)**

O relatório está nesta branch, `metodologia-sensibilidade-anarede`, e foi publicado com um nome de arquivo que descreve seu conteúdo. O PDF original foi preservado integralmente: a alteração se limita ao nome do arquivo.

## Identificação do documento

- **Título na capa:** Relatório-Análise de sistemas de potência.
- **Instituição:** Universidade Federal do Rio de Janeiro (UFRJ), Grupo 6.
- **Ano:** 2026.
- **Autores:** Adriano Macena da Costa, Vitor dos Santos Barcelos, João Pedro Diniz da Rocha e Leonardo de Lima Rodrigues.

## O que a metodologia faz

O estudo usa análises de sensibilidade no **ANAREDE** para orientar ajustes de tensão em barras PV, geração ativa e taps de transformadores. Após cada ajuste, recalcula o fluxo de potência e verifica as violações. A metodologia é aplicada inicialmente ao caso base e depois à avaliação de contingências N-1 de circuitos.

| Etapa | Onde consultar no PDF |
| --- | --- |
| Ferramenta EXSB e interpretação das sensibilidades | Páginas 6 a 9 |
| Estratégia iterativa e fluxograma de correção | Páginas 10 e 11 |
| Ferramenta EXCA e análise de contingências N-1 | Página 22 |
| Exemplos de correção das contingências 6-11 e 6-12 | Páginas 29 a 32 |
| Resultados finais e limitações | Página 55 |

A tabela usa a contagem física de páginas do PDF, começando pela capa como página 1. A numeração impressa no documento é diferente.

## Alcance dos resultados

A conclusão apresenta a correção do caso base e a melhora de diversas contingências, mas também identifica casos que permaneceram críticos. As contingências 9-14, 13-14 e 4-15 não foram contidas pelos controles disponíveis. Os casos 5-6 e 5-15 permaneceram acima dos limites normais, sendo considerados contidos pelos autores sob limites emergenciais.

O relatório descreve os resultados obtidos e os limites dos controles considerados; não afirma que todas as violações de contingências foram eliminadas.

## Relação com os arquivos FLUPOT

Os arquivos anteriormente publicados no repositório pertencem ao **estudo realizado com FLUPOT**. Eles estão identificados e descritos em [`estudo-flupot/`](../estudo-flupot/README.md), também acessível pela branch `main`.

Este PDF documenta a metodologia de análise de sensibilidade no ANAREDE. Os arquivos do estudo FLUPOT ficam mantidos como outro material do repositório, sem serem apresentados como uma reprodução automática dos casos descritos no relatório.

[Voltar à apresentação do repositório](../README.md).
