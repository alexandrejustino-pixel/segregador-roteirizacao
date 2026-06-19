# Segregador · Roteirização V2

Ferramenta web para segregar a **Base Roteirizável** e a **Query de Volumosos** em arquivos de IDs, pronta para uso no dia a dia.

## Como usar

1. Abra o site (ou o arquivo `index.html`).
2. Importe a **Base Roteirizável** (CSV principal).
3. Importe a **Query de Volumosos** (CSV com a coluna `SHP_SHIPMENT_ID`).
4. Os arquivos são contados automaticamente. Baixe um a um ou clique em **Baixar todos os arquivos**.

## Arquivos gerados

| # | Arquivo | Conteúdo |
|---|---------|----------|
| 1 | FAKE-UTR | `Id_Unidad` onde CICLO FINAL = FAKE-UTR |
| 2 | FAKE-OTR | `Id_Unidad` onde CICLO FINAL = FAKE-OTR |
| 3 | CHP | `Id_Unidad` onde CICLO FINAL = CHP |
| 4 | Volumosos | `SHP_SHIPMENT_ID` da base de volumosos, sem repetir os IDs dos arquivos 1, 2 e 3 |
| 5 | AM | `Id_Unidad` onde CICLO FINAL = AM |

Cada arquivo baixado contém **apenas os números**, um por linha, sem cabeçalho.

## Observações

- Todo o processamento acontece no navegador. Nenhum dado é enviado para servidores.
- Funciona offline (não depende de internet depois de aberto).
- Os downloads vão para a pasta padrão do navegador (normalmente **Downloads**).
