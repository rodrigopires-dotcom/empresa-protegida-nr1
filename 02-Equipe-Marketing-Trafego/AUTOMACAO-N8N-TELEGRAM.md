# Automação n8n + Telegram — Empresa Protegida™

> Setup completo: do zero à automação rodando.
> Atualizado: 09/06/2026

---

## Parte 1 — Criar a infraestrutura

### 1.1 · Criar conta no n8n (15 min)

1. Acesse **[n8n.io](https://n8n.io)** → clique em "Get started free"
2. Escolha **n8n Cloud** (Starter ~$24/mês — mais fácil que self-host)
   - Alternativa gratuita: usar [Railway](https://railway.app) com Docker (requer conhecimento técnico)
3. Crie sua conta → acesse o painel
4. Anote a URL do seu workspace: `https://[seu-nome].n8n.cloud`

---

### 1.2 · Criar o Bot do Telegram (10 min)

1. Abra o Telegram → pesquise **@BotFather**
2. Envie: `/newbot`
3. Escolha um nome: `Empresa Protegida NR1`
4. Escolha um username: `empresa_protegida_nr1_bot` (deve terminar em `bot`)
5. **Copie o token** (formato: `1234567890:ABCdefGHIjklMNOpqrsTUVwxyz`)
6. Salve em local seguro → você vai usar no n8n

**Como obter seu Chat ID:**
1. Pesquise **@userinfobot** no Telegram → envie qualquer mensagem
2. Ele retorna seu `id` numérico → esse é seu `TELEGRAM_CHAT_ID`

---

### 1.3 · Obter o Ad Account ID do Meta (5 min)

1. Acesse [Ads Manager](https://business.facebook.com/adsmanager)
2. Olhe a URL: `?act=XXXXXXXXXX`
3. O número após `act=` é seu **Ad Account ID**
4. No n8n, usar no formato: `act_XXXXXXXXXX`

---

### 1.4 · Configurar variáveis no n8n

No n8n: Settings → Variables → criar as seguintes:

| Variável | Valor |
|---|---|
| `META_TOKEN` | Seu token de API do Meta |
| `META_AD_ACCOUNT` | `act_XXXXXXXXXX` |
| `TELEGRAM_TOKEN` | Token do @BotFather |
| `TELEGRAM_CHAT_ID` | Seu chat_id numérico |

---

## Parte 2 — Workflows a importar

### Workflow 1 · Relatório Diário de Campanhas

**Arquivo:** `workflows/01-relatorio-diario-campanhas.json`

**O que faz:**
- Roda todo dia às 9h00
- Chama a API do Meta e puxa os dados de ontem
- Calcula CTR, CPC, CPA, ROAS
- Compara com os KPIs definidos
- Envia mensagem formatada no Telegram com semáforo (✅ ⚠️ 🔴)

**Trigger:** Schedule — `0 9 * * *`

---

### Workflow 2 · Revisão de Criativos (a cada 3 dias)

**Arquivo:** `workflows/02-revisao-criativos.json`

**O que faz:**
- Roda a cada 3 dias às 9h00
- Puxa performance por criativo (últimos 3 dias)
- Identifica o melhor e o pior criativo
- Envia recomendação de pausa ou escala

**Trigger:** Schedule — `0 9 */3 * *`

---

### Workflow 3 · Lembrete Semanal de Conteúdo

**Arquivo:** `workflows/03-lembrete-semanal-conteudo.json`

**O que faz:**
- Roda toda domingo às 10h00
- Envia checklist da semana de conteúdo
- Lista o que precisa ser produzido
- Pergunta se está pronto (resposta no Telegram)

**Trigger:** Schedule — `0 10 * * 0`

---

### Workflow 4 · Lembrete Diário de Postagem

**Arquivo:** `workflows/04-lembrete-diario-postagem.json`

**O que faz:**
- Roda todo dia às 20h00 (D-1)
- Verifica o que precisa postar amanhã (baseado no cronograma)
- Envia lembrete com tema, formato e horário
- Se segunda-feira ou dia especial, adiciona detalhes do criativo

**Trigger:** Schedule — `0 20 * * *`

---

### Workflow 5 · Alerta de KPI Crítico (tempo real)

**Arquivo:** `workflows/05-alerta-kpi-critico.json`

**O que faz:**
- Roda a cada 4 horas (durante horário comercial)
- Verifica se alguma campanha está com gasto alto + CPA ruim
- Envia alerta imediato se ROAS < 1,0 com gasto > R$10 no dia

**Trigger:** Schedule — `0 9,13,17,21 * * *`

---

## Parte 3 — Como importar os workflows

1. No n8n: clique em **"+"** → "Import workflow"
2. Selecione o arquivo JSON da pasta `workflows/`
3. Após importar: configure as credenciais
   - Para o Telegram: Add Credential → Telegram API → cole o bot token
   - Para o Meta: Add Credential → HTTP Header Auth → `Authorization: Bearer [META_TOKEN]`
4. Ative o workflow (toggle verde no canto superior)
5. Teste clicando em "Test workflow" antes de ativar

---

## Parte 4 — Estrutura de mensagem no Telegram

### Emojis padrão do projeto

| Emoji | Significado |
|---|---|
| ✅ | Métrica dentro do alvo |
| ⚠️ | Atenção — próximo do limite |
| 🔴 | Fora do alvo — ação necessária |
| 📊 | Relatório de dados |
| 🎨 | Criativo / conteúdo |
| 💰 | Financeiro / orçamento |
| 📅 | Data / agenda |
| ⏰ | Lembrete urgente |

---

## Parte 5 — Checklist de ativação

- [ ] Conta n8n criada e acessível
- [ ] Bot Telegram criado (@BotFather)
- [ ] Token do bot salvo no n8n (variável)
- [ ] Chat ID pessoal configurado
- [ ] Token Meta API configurado
- [ ] Ad Account ID configurado
- [ ] Workflow 1 importado e testado
- [ ] Workflow 2 importado e testado
- [ ] Workflow 3 importado e testado
- [ ] Workflow 4 importado e testado
- [ ] Workflow 5 importado e testado
- [ ] Todos os workflows ativados (toggle verde)
- [ ] Primeiro relatório recebido no Telegram ✅

---

## Tempo estimado de setup completo

| Etapa | Tempo |
|---|---|
| Conta n8n + bot Telegram | 30 min |
| Importar e configurar workflows | 45 min |
| Testes e ajustes | 30 min |
| **Total** | **~2 horas** |
