# Bairros e localidades de Pacajus (CE)

Mapa dos bairros da sede e das localidades da zona rural do município de Pacajus, no Ceará.

**Este mapa não é oficial.** Pacajus não tem bairros cadastrados na Malha de Bairros do IBGE (Censo 2022). Os nomes vêm do cadastro de endereços do Censo, e os limites foram estimados a partir desses endereços e das ruas.

## Origem dos dados

| Camada | Fonte |
|---|---|
| Limite municipal e distritos (Pacajus, Itaipaba, Pascoal) | IBGE – Malha de Distritos, Censo 2022 |
| Zona urbana e rural | IBGE – Malha de Setores Censitários, Censo 2022 (situação do setor) |
| Nomes dos bairros e localidades, domicílios e endereços | IBGE – CNEFE 2022 (Cadastro Nacional de Endereços para Fins Estatísticos) |
| Ruas usadas para traçar as divisas | OpenStreetMap |
| Mapa de fundo | OpenStreetMap e Esri (satélite) |

O CNEFE lista os endereços visitados no Censo 2022, cada um com coordenada e com o campo **Localidade**. Na maior parte do país, esse campo corresponde ao bairro. O nome é anotado pelos recenseadores do IBGE durante a coleta, e não informado pelos moradores.

## Como os limites foram feitos

1. Usei os endereços do CNEFE de Pacajus com coordenadas de melhor qualidade (níveis 1 e 2).
2. Cada ponto do município recebeu o nome do endereço mais próximo (diagrama de Voronoi), e as áreas foram juntadas por localidade.
3. Na zona urbana, as ruas do OpenStreetMap dividem a cidade em quarteirões. O quarteirão vai para o bairro que tem pelo menos 80% dos endereços dentro dele. Nos quarteirões mistos, vale o passo 2.
4. Pedaços soltos de bairro com menos de 0,2 km² foram juntados ao bairro vizinho.
5. A divisão entre zona urbana e rural segue a situação dos setores censitários do IBGE.

## Ajustes nos nomes

- Grafias diferentes do mesmo lugar foram unificadas: Cuacu → Coaçu, Cohab → Conjunto Cohab, Croatá 2 → Croatá II, Quilombo Base → Comunidade Quilombola da Base, Aldeia Park 05 → Aldeia Park.
- Vicunha e Rigesa são nomes de empresas e foram incluídas no Tucum.
- Banguê / Banguê I / Banguê II e Croatá / Croatá I / Croatá II ficaram separados, porque aparecem em lugares diferentes.
- Cerca de 3.100 endereços estão registrados só como "Pacajus", sem bairro. Eles não definem limites, mas entram na contagem de domicílios.

## Arquivos

- `index.html` – mapa interativo (Leaflet)
- `dados/bairros_localidades_pacajus.geojson` – polígonos com localidade, distrito, zona, área, endereços e domicílios
- `dados/limite_pacajus.geojson` – limite municipal
- `dados/distritos_pacajus.geojson` – distritos

## Licença

Os polígonos usam ruas do OpenStreetMap, então os arquivos em `dados/` seguem a licença [ODbL](https://opendatacommons.org/licenses/odbl/). Dados do OpenStreetMap © [colaboradores do OpenStreetMap](https://www.openstreetmap.org/copyright). Dados do IBGE são públicos.
