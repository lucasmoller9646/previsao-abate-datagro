# Previsão de Abate Bovino

App de previsão mensal do abate bovino brasileiro (IBGE/SIF), convertido do modelo em Excel: ciclo pecuário (cosseno sobre a média móvel de 12 meses), sazonalidade por categoria, efeito climático (ONI com defasagem distribuída) e cota China.

- `index.html` — aplicação completa, sem dependências de servidor (os dados ficam embutidos e as edições são guardadas no navegador; o Excel é gerado no cliente com SheetJS via CDN).
- Publicado via GitHub Pages a partir da branch `main`.

Fórmula central: `Abate = MM12(ciclo) × (1+saz) × (1+clima) × (1+cota)`.
