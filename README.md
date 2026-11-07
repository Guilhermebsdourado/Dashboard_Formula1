<h1 align="center">Formula 1 Analytics Dashboard</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" />
  <img src="https://img.shields.io/badge/Power%20Query%20(M)-0078D4?style=for-the-badge&logo=microsoft&logoColor=white" />
  <img src="https://img.shields.io/badge/DAX-4B8BBE?style=for-the-badge&logo=microsoft&logoColor=white" />
  <img src="https://img.shields.io/badge/REST%20API-E8571F?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Blender-F5792A?style=for-the-badge&logo=blender&logoColor=white" />
</p>

<p align="center">
  <a href="#português">🇧🇷 Português</a> •
  <a href="#english">🇺🇸 English</a>
</p>

<p align="center">
    <img src="Carro%203d/redbull_girando%20(4).gif" alt="Carro de F1 girando" width="400">
</p>
<p align="center">
  <a href="https://app.powerbi.com/view?r=eyJrIjoiNzUzYjlkMDktZjQzMy00ZmU0LTljZWUtNjBlNTQ4NzZjOGU2IiwidCI6IjgzZTljYmEzLThmZmMtNDYyZi1iYTJlLTBjZWNlYzIxOWRjZSJ9">
    <img src="https://img.shields.io/badge/▶%20Acessar%20o%20dashboard%20interativo-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Acessar o dashboard interativo">
  </a>
</p>

### Português

# Sobre esse projeto
Dashboard interativo em **Power BI** sobre a **Fórmula 1 de 1980 até a temporada atual**: pilotos, equipes, campeonatos, circuitos e pit stops.

O histórico vem de **arquivos CSV** hospedados no repositório [f1-powerbi-dados](https://github.com/Guilhermebsdourado/f1-powerbi-dados) e a temporada atual vem da **API pública Jolpica F1**. A cada atualização agendada, as corridas novas entram sozinhas no relatório.

> 📅 **Projeto em série:** estou apresentando uma página do dashboard por vez, aqui e no LinkedIn. Este README cresce a cada nova página.

### Páginas do dashboard
| # | Página | Status |
|---|---|---|
| 1 | [Visão Geral](#1-visão-geral) | ✅ Publicada |
| 2 | Pilotos | 🔜 Em breve |
| 3 | Equipes | 🔜 Em breve |
| 4 | Temporada | 🔜 Em breve |
| 5 | Circuitos | 🔜 Em breve |
| 6 | Pit Stops | 🔜 Em breve |
| 7 | Bastidores: dados, DAX e animações | 🔜 Em breve |

---

### 1. Visão Geral

<p align="center">
 <img width="1429" height="806" alt="{09E2D106-CAAC-4EA2-AE07-800B2CBA878E}" src="https://github.com/user-attachments/assets/aba88c93-6a3d-4488-a8e3-077a71772458" />
</p>

**Pergunta que a página responde:** *como a Fórmula 1 evoluiu desde 1980, e quem dominou cada época?*

**O que tem na página:**
- **Cards de resumo:** total de corridas, circuitos, equipes, pilotos e vencedores diferentes no período escolhido.
- **Filtro de anos:** todos os visuais respondem ao intervalo de temporadas selecionado.
- **Vencedores diferentes por temporada:** mostra os anos de domínio de uma equipe (poucos vencedores) e os anos equilibrados (muitos vencedores). A temporada em andamento aparece em cinza.
- **Títulos de construtores e de pilotos:** rankings de campeões no período. O título conta quando a temporada termina **ou quando já está matematicamente garantido**.
- **Mapa dos circuitos:** cada bolha mostra quantas corridas aconteceram naquele lugar. Ao clicar num circuito, o traçado da pista aparece ao lado.

**Destaques técnicos:**
- Medida de **temporada em andamento**, que muda a cor da série sem precisar mexer no gráfico quando o ano vira.
- Medida de **título garantido**, que compara a vantagem do líder com o máximo de pontos ainda em disputa (25 por corrida + 8 por sprint restante, com a informação de sprint vinda do calendário da API).
- Tratamento de **casos históricos**, como a desclassificação de Michael Schumacher do campeonato de 1997.

**Insights:**
- **1982** teve **11 vencedores diferentes**, o ano mais equilibrado do período.
- Em **1988**, **2014**, **2015** e **2023**, só **3 pilotos** venceram corridas: anos de domínio de McLaren, Mercedes e Red Bull.
- **Lewis Hamilton** e **Michael Schumacher** lideram com **7 títulos** cada.
- **Andrea Kimi Antonelli** garantiu o título de **2026** no GP do México, com corridas ainda por disputar.

---

### Fontes de dados
| Fonte | Conteúdo | Período |
|---|---|---|
| **Arquivos CSV** (repositório [f1-powerbi-dados](https://github.com/Guilhermebsdourado/f1-powerbi-dados)) | resultados, classificação, campeonatos, pit stops, pilotos, equipes, circuitos | 1980 – 2024 |
| **[API Jolpica F1](https://github.com/jolpica/jolpica-f1)** (sucessora da API Ergast) | as mesmas informações, atualizadas, em JSON | 2024 – hoje |

### Tecnologias
- **Power BI Desktop / Service:** modelagem, DAX, relatório e atualização agendada
- **Power Query (M):** ingestão, paginação da API e tratamento dos dados
- **API Jolpica F1:** API REST pública
- **Blender:** modelos 3D e animações usados no relatório

### Como executar
1. Baixe o arquivo `Dashboard_F1.pbix` deste repositório.
2. Abra em um **Power BI Desktop atualizado**.
3. Os dados já estão salvos no arquivo. Para atualizar, clique em **Atualizar** e, se pedir credenciais, escolha **Anônimo**.

<p align="center">
  <a href="https://app.powerbi.com/view?r=eyJrIjoiNzUzYjlkMDktZjQzMy00ZmU0LTljZWUtNjBlNTQ4NzZjOGU2IiwidCI6IjgzZTljYmEzLThmZmMtNDYyZi1iYTJlLTBjZWNlYzIxOWRjZSJ9">
    <img src="https://img.shields.io/badge/▶%20Acessar%20o%20dashboard%20interativo-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Acessar o dashboard interativo">
  </a>
</p>

### English

# Project Overview
An interactive **Power BI** dashboard covering **Formula 1 from 1980 to the current season**: drivers, teams, championships, circuits and pit stops.

Historical data comes from **CSV files** hosted in the [f1-powerbi-dados](https://github.com/Guilhermebsdourado/f1-powerbi-dados) repository, and the current season comes from the **public Jolpica F1 API**. On every scheduled refresh, new races show up automatically.

> 📅 **Series project:** I'm presenting one page of the dashboard at a time, here and on LinkedIn. This README grows with each new page.

### Dashboard pages
| # | Page | Status |
|---|---|---|
| 1 | [Overview](#1-overview) | ✅ Published |
| 2 | Drivers | 🔜 Coming soon |
| 3 | Teams | 🔜 Coming soon |
| 4 | Season | 🔜 Coming soon |
| 5 | Circuits | 🔜 Coming soon |
| 6 | Pit Stops | 🔜 Coming soon |
| 7 | Behind the scenes: data, DAX and animations | 🔜 Coming soon |

---

### 1. Overview
<p align="center">
 <img width="1429" height="806" alt="{09E2D106-CAAC-4EA2-AE07-800B2CBA878E}" src="https://github.com/user-attachments/assets/aba88c93-6a3d-4488-a8e3-077a71772458" />
</p>
**Question this page answers:** *how has Formula 1 changed since 1980, and who dominated each era?*

**What's on the page:**
- **Summary cards:** races, circuits, teams, drivers and different winners in the selected period.
- **Year slider:** every visual responds to the selected range of seasons.
- **Different winners per season:** shows the years of dominance (few winners) and the balanced years (many winners). The season in progress is shown in grey.
- **Constructors' and drivers' titles:** champions ranking for the period. A title counts when the season ends **or when it is already mathematically clinched**.
- **Circuits map:** each bubble shows how many races took place there. Clicking a circuit shows its track layout.

**Technical highlights:**
- **Season in progress** measure that changes the series color with no manual change when the year turns.
- **Clinched title** measure that compares the leader's margin with the maximum points still available (25 per race + 8 per remaining sprint, with sprint information taken from the API calendar).
- Handling of **historical edge cases**, such as Michael Schumacher's disqualification from the 1997 championship.

**Insights:**
- **1982** had **11 different winners**, the most balanced year in the period.
- In **1988**, **2014**, **2015** and **2023**, only **3 drivers** won races: years of McLaren, Mercedes and Red Bull dominance.
- **Lewis Hamilton** and **Michael Schumacher** lead with **7 titles** each.
- **Andrea Kimi Antonelli** clinched the **2026** title at the Mexico City GP, with races still to go.

---

### Data Sources
| Source | Content | Period |
|---|---|---|
| **CSV files** ([f1-powerbi-dados](https://github.com/Guilhermebsdourado/f1-powerbi-dados) repository) | results, qualifying, standings, pit stops, drivers, teams, circuits | 1980 – 2024 |
| **[Jolpica F1 API](https://github.com/jolpica/jolpica-f1)** (successor of the Ergast API) | same entities, current data in JSON | 2024 – today |

### Technologies
- **Power BI Desktop / Service:** modeling, DAX, report and scheduled refresh
- **Power Query (M):** ingestion, API pagination and data cleaning
- **Jolpica F1 API:** public REST API
- **Blender:** 3D models and animations used in the report

### How to Run
1. Download `Dashboard_F1.pbix` from this repository.
2. Open it in an **up-to-date Power BI Desktop**.
3. The data is already stored in the file. To update it, click **Refresh** and choose **Anonymous** if asked for credentials.

<p align="center">
  <a href="https://app.powerbi.com/view?r=eyJrIjoiNzUzYjlkMDktZjQzMy00ZmU0LTljZWUtNjBlNTQ4NzZjOGU2IiwidCI6IjgzZTljYmEzLThmZmMtNDYyZi1iYTJlLTBjZWNlYzIxOWRjZSJ9">
    <img src="https://img.shields.io/badge/▶%20Acessar%20o%20dashboard%20interativo-F2C811?style=for-the-badge&logo=powerbi&logoColor=black" alt="Acessar o dashboard interativo">
  </a>
</p>
