# Previsão de Abate Bovino — DATAGRO

App de previsão mensal do abate bovino brasileiro (IBGE/SIF), convertido do modelo em Excel: ciclo pecuário (cosseno sobre a média móvel de 12 meses), sazonalidade por categoria, efeito climático (ONI com defasagem distribuída) e cota China.

**Acesso:** https://lucasmoller9646.github.io/previsao-abate-datagro/

- `index.html` — aplicação completa, sem servidor: os dados ficam embutidos e as edições são guardadas no navegador de quem usa (exporte/importe o estado em JSON para levar a outro computador). O Excel é gerado no cliente com SheetJS via CDN.
- A versão colaborativa, com estado compartilhado, cenários e safras de previsão, é o artifact no claude.ai.

Fórmula central: `Abate = MM12(ciclo) × (1+saz) × (1+clima) × (1+cota)`.
