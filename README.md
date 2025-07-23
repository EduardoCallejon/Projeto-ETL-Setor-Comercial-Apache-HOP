# Projeto de ETL local

## Alinhamento com os stakeholders <br>
Em conversa com os representantes da empresa, foi alinhado a necessidade dos seguintes indicadores; <br>
1 - Venda por período <br>
2 - Venda por vendedor <br>
3 - Venda por produto <br>
<br>
## Montagem da arquitetura

Os dados de origem  para está análise, foram gerados através do Python.

O projeto irá abordar um cenário, onde os dados vem de planilhas em excel, após isso os dados são <br>
tratados via apache HOP enviados para um banco staging area, e a partir do mesmo, é feita as trat- <br>  
-ivas de atualização incremental e é enviado para o DW, que será consumido por Power BI.
