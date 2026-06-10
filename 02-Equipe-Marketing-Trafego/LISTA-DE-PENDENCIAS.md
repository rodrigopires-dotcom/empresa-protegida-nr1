# Lista de Pendências — Empresa Protegida™

> O que falta para cada sistema estar 100% operacional.
> Atualizado: 09/06/2026

---

## 🔴 Bloqueios críticos (travam o lançamento)

| # | Pendência | Responsável | Impacto |
|---|---|---|---|
| 1 | **Criar Grupo WhatsApp** e pegar link oficial de convite | Guilherme | eBook aponta para `wa.me` direto — sem grupo real ainda |
| 2 | **Atualizar eBook** com link do grupo → re-gerar PDF → re-upload no Hotmart | Claude + Guilherme | Compradores caem em link sem destino |
| 3 | **Produzir criativos** (vídeo/imagem) para os anúncios | Guilherme / equipe | Campanhas Meta Ads não podem ser ativadas sem criativos |

---

## 🟡 Infraestrutura de automação (n8n + Telegram)

| # | Pendência | Onde fazer | Tempo estimado |
|---|---|---|---|
| 4 | Criar conta n8n (cloud) | n8n.io | 15 min |
| 5 | Criar bot Telegram via @BotFather | Telegram | 10 min |
| 6 | Configurar variáveis no n8n (META_TOKEN, AD_ACCOUNT, BOT_TOKEN, CHAT_ID) | n8n Settings | 10 min |
| 7 | Importar e ativar `01-relatorio-diario-campanhas.json` | n8n | 20 min |
| 8 | Importar e ativar `03-lembrete-semanal-conteudo.json` | n8n | 15 min |
| 9 | Importar e ativar `04-lembrete-diario-postagem.json` | n8n | 15 min |
| 10 | Pegar **Ad Account ID** no Ads Manager (URL: `act_XXXXXX`) | Meta Ads Manager | 5 min |

---

## 🟠 Meta Ads — para ativar as campanhas

| # | Pendência | Detalhe |
|---|---|---|
| 11 | **Criar criativos** — 4 variações por campanha (vídeo ou imagem) | Ver `CAMPANHAS-META-ADS.md` para briefing de hooks |
| 12 | **Criar as 3 campanhas** no Ads Manager | Estrutura pronta em `CAMPANHAS-META-ADS.md` |
| 13 | **Configurar API de Conversão (CAPI)** no Hotmart | Gerar token em Meta Events Manager → Settings → "Gerar token de acesso" |
| 14 | Confirmar que o Pixel está disparando | Instalar Meta Pixel Helper no Chrome e testar |

---

## 🔵 Conteúdo orgânico (Instagram)

| # | Pendência | Detalhe |
|---|---|---|
| 15 | **Produzir 1ª semana de conteúdo** antes de ligar os anúncios | Ver `CRONOGRAMA-CONTEUDO.md` — Semana 1 |
| 16 | Criar templates no Canva (carrossel + stories + feed) | Paleta: navy #0B1F3A · dourado #C9A96E · fontes Playfair + Inter |
| 17 | Configurar Meta Business Suite para agendamento | Agendar posts da semana toda de uma vez |
| 18 | **Ensaio fotográfico do Guilherme** (autoridade visual) | Fotos profissionais para feed e criativos de anúncio |

---

## ⚪ Fase futura (Degrau 2)

| # | Pendência | Detalhe |
|---|---|---|
| 19 | Definir preço e formato do treinamento (R$297 ou R$497?) | Aguarda validação com leads do grupo WhatsApp |
| 20 | Gravar o treinamento em vídeo | Estrutura: RAIO-X → BLINDAGEM → ESCUDO |
| 21 | Criar produto no Hotmart (Degrau 2) | Configurar checkout, preço, entrega |
| 22 | Criar página de vendas do treinamento | Copy orientada a quem já leu o eBook |
| 23 | Criar sequência de e-mails pós-compra do eBook | Nutrição → pitch do treinamento |

---

## 📊 Resumo executivo

| Fase | Status | O que falta |
|---|---|---|
| Produto eBook | ✅ 90% pronto | Grupo WA + PDF atualizado no Hotmart |
| Meta Pixel | ✅ Configurado | CAPI (token) opcional |
| Campanhas Meta Ads | 🔄 Estrutura pronta | Criativos + ativação |
| Conteúdo orgânico | 🔄 Planejado | Produção + templates Canva |
| n8n + Telegram | ⏳ A fazer | Setup + import de workflows |
| Degrau 2 (treinamento) | ⏳ Fase futura | Tudo |

---

## Ordem de execução recomendada

```
1. Criar Grupo WhatsApp → link oficial
2. Atualizar eBook → re-gerar PDF → re-upload Hotmart
3. Setup n8n + Telegram (seguir AUTOMACAO-N8N-TELEGRAM.md)
4. Produzir templates Canva + 1ª semana de conteúdo
5. Produzir 4 criativos para anúncios
6. Ativar campanhas Meta Ads
7. Ensaio fotográfico do Guilherme
8. [Degrau 2] — quando tiver 50+ compradores no grupo
```
