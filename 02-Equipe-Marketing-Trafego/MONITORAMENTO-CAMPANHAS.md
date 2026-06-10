# Monitoramento de Campanhas — Empresa Protegida™

> Metodologia Pedro Sobral · Budget R$1.000/mês (R$33/dia)
> Atualizado: 09/06/2026

---

## Cadência de revisão (Sobral)

| O que revisar | Frequência | Ação se fora do KPI |
|---|---|---|
| **Criativos** (CTR, CPC) | A cada 2–3 dias | Pausar criativo ruim → ativar variação |
| **Públicos** (CPA, alcance) | A cada 4 dias | Pausar público não entregável → testar novo |
| **Orçamento** (gasto, ROAS) | A cada 2 dias | Ajustar ±20% — nunca mais que isso de uma vez |
| **Estrutura das campanhas** | A cada 7 dias | Reorganizar ad sets se necessário |

---

## KPIs — Semáforo de alerta

| Métrica | ✅ Ótimo | ⚠️ Atenção | 🔴 Pausar |
|---|---|---|---|
| CTR (cliques/impressões) | ≥ 2,0% | 1,0%–1,9% | < 1,0% |
| CPC (custo por clique) | ≤ R$1,00 | R$1,01–R$1,50 | > R$1,50 |
| CPA (custo por compra) | ≤ R$15 | R$15–R$20 | > R$20 |
| ROAS (retorno/gasto) | ≥ 2,0x | 1,35x–1,99x | < 1,35x |
| Frequência | ≤ 2,5x | 2,5x–4x | > 4x (queima de público) |

---

## Relatório diário automático via Telegram (n8n)

**Horário de envio:** 9h00 todos os dias

**Formato da mensagem:**

```
📊 RELATÓRIO DIÁRIO — Empresa Protegida™
📅 [Data de ontem]

💰 Gasto: R$[X] / R$33,00
📱 Impressões: [X]
🖱️ Cliques: [X]
📈 CTR: [X]% [✅/⚠️/🔴]
💲 CPC: R$[X] [✅/⚠️/🔴]
🛒 Compras: [X]
💵 Receita: R$[X]
📉 CPA: R$[X] [✅/⚠️/🔴]
🚀 ROAS: [X]x [✅/⚠️/🔴]

[SE ALGUM KPI VERMELHO:]
⚠️ AÇÃO NECESSÁRIA: [métrica] fora do alvo.
Recomendação: [ação específica]
```

---

## Relatório de criativos (a cada 3 dias)

**Horário de envio:** 9h00 — dias 1, 4, 7, 10, 13... do mês

**Formato da mensagem:**

```
🎨 REVISÃO DE CRIATIVOS — Empresa Protegida™
📅 Últimos 3 dias

CRIATIVO 1: [nome]
  CTR: [X]% | CPC: R$[X] | Gastos: R$[X]
  Status: [✅ Manter / ⚠️ Observar / 🔴 Pausar]

CRIATIVO 2: [nome]
  ...

💡 Recomendação: [top criativo está performando — escalar orçamento nele]
```

---

## Revisão semanal completa (toda segunda-feira)

**Horário de envio:** 8h30 toda segunda

**Inclui:**
1. Resumo da semana (gasto total, compras, receita, ROAS)
2. Top 3 criativos da semana
3. Público com melhor CPA
4. Alerta de frequência (público esgotado?)
5. Recomendação da semana (Sobral: "o que testar esta semana?")

---

## Regras de escala (Sobral)

- **Só escalar** quando CPA ≤ R$15 por 3 dias consecutivos
- **Aumentar budget** em no máximo **+20% a cada 2 dias**
- **Nunca duplicar budget** de um dia para o outro (sinaliza erro ao algoritmo)
- **Criativo vencedor**: replicar em novos ad sets, não aumentar só o gasto

---

## Configuração inicial necessária para o n8n

```
META_AD_ACCOUNT_ID = act_XXXXXXXXXX   (pegar no Ads Manager: URL contém act_...)
META_API_TOKEN     = [seu token de acesso permanente]
TELEGRAM_BOT_TOKEN = [token do @BotFather]
TELEGRAM_CHAT_ID   = [seu chat_id pessoal]
```

> Como pegar o Ad Account ID: no Ads Manager → URL da página → procurar `act_` seguido de números.
