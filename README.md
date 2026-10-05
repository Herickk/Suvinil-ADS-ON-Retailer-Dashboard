# Suvinil ADS ON – Dashboard de Lojistas

🇧🇷 Português | [🇺🇸 English](README.en.md)

Dashboard em **Power BI** para acompanhar os lojistas cadastrados no programa **Suvinil ADS ON**: situação de cada loja no fluxo de ativação, perfil dos contatos, planos contratados, distribuição geográfica e acesso ao dashboard individual de cada lojista.

> **Última atualização dos dados:** 05/10/2026 (indicada no cabeçalho do relatório)

---

## 📌 Visão geral

O relatório responde a perguntas como:

- Quantas lojas estão cadastradas e em que etapa cada uma está?
- Quais planos (antigos e novos) estão sendo contratados?
- Em quais regiões e estados estão os lojistas?
- Quem são os contatos (cargos) cadastrados?
- Onde está o dashboard individual de cada loja?

---

## 🧭 Componentes do dashboard

### 1. Filtros (topo da página)

| Filtro | Descrição |
|---|---|
| **Região** | Filtra por região do Brasil (Sudeste, Sul, Norte etc.) |
| **Estado** | Filtra por UF |
| **Razão Social** | Filtra por loja específica |
| **Plano Escolhido** | Filtra pelo plano contratado |

Todos começam em **"Todos"** e afetam todos os visuais da página.

### 2. Lojistas cadastrados (gráfico de rosca)

Mostra o **total de lojas (17)** e a distribuição por status:

| Status | Lojas | % | Significado |
|---|---|---|---|
| **Em Veiculação** | 12 | 71% | Campanha ativa e rodando |
| **Setup Inicial** | 3 | 18% | Loja em configuração/onboarding |
| **Aguardando Pagamento** | 2 | 12% | Cadastro feito, pagamento pendente |

### 3. Cargo

Gráfico de barras com o **cargo do contato** cadastrado em cada loja (ex.: Gerente 17,65%, Sócio administrador 11,76%, Diretor, Diretora de marketing, Dono, Gerente de marketing – 5,88% cada). Possui barra de rolagem com mais cargos.

### 4. Planos Antigos

Matriz de **plano × periodicidade** (Mensal, Trimestral, Semestral), com a quantidade de lojas em cada combinação:

| Plano | Mensal | Trimestral | Semestral |
|---|---|---|---|
| Basic | – | 1 | 2 |
| Premium | – | 1 | – |
| Business | – | – | 3 |

### 5. Planos Novos

Quantidade de lojas por plano da nova estrutura de planos:

| Plano | Lojas |
|---|---|
| Start | 2 |
| Basic | 4 |
| Premium | 2 |

### 6. Localização (mapa)

Mapa com os **estados onde há lojistas** destacados em laranja. Útil para ver a cobertura geográfica rapidamente.

### 7. Região e Estado

Gráficos de barras com o **percentual de lojas** por região e por estado:

- **Região:** Sudeste (52,94%), Sul (29,41%), Norte (11,76%) e outras (rolagem)
- **Estado:** São Paulo (29,41%), Rio Grande do Sul (23,53%), Minas Gerais (17,65%) e outros (rolagem)

### 8. Botões de status

Segmentação rápida por etapa do fluxo. Ao clicar, todo o relatório é filtrado:

- **Selecionar tudo**
- **Aguardando pagamento**
- **Em veiculação**
- **Setup inicial**

### 9. Tabela de lojistas

Lista detalhada, uma linha por loja:

| Coluna | Descrição |
|---|---|
| **CNPJ** | CNPJ da loja |
| **Estado** | UF da loja |
| **Razão Social** | Nome empresarial |
| **Dashboard** | Link do dashboard individual (Looker Studio) ou o texto **"Setup inicial"** quando ainda não foi liberado |

---

## 🔄 Fluxo de status das lojas

```
Aguardando Pagamento  →  Setup Inicial  →  Em Veiculação
```

> A ordem acima é ilustrativa; confirme com o time responsável o fluxo oficial.

---

## 💡 Como usar

1. Use os **filtros do topo** ou os **botões de status** para segmentar os dados.
2. Clique em uma **barra, fatia ou estado** em qualquer gráfico para filtrar os demais visuais (filtro cruzado).
3. Na **tabela**, clique no link da coluna *Dashboard* para abrir o painel individual da loja.
4. Para limpar a seleção, clique novamente no elemento selecionado ou em **Selecionar tudo**.

---

## ⚠️ Observações

- Alguns **CNPJs aparecem em notação científica** (ex.: `1,53753E+13`). Isso indica que a coluna está como **número** na fonte. Recomenda-se converter para **texto** na origem para preservar o CNPJ completo.
- Os **Planos Antigos** e **Novos** coexistem; lojas migradas ou contratadas após a mudança aparecem na estrutura nova.
- Os dados de lojistas (CNPJ, razão social, links) são **sensíveis**: não os versione neste repositório.

---

## 🛠️ Tecnologias

- Power BI (Service)
- Google Looker Studio (dashboards individuais por loja)
- Mapa: Microsoft Bing Maps (visual nativo do Power BI)

---

## 📄 Licença / Responsável

Preencha aqui o responsável pelo relatório e a política de uso interno.
