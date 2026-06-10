# Funil de Vendas — Empresa Protegida™

> Mapa completo: da impressão do anúncio até a compra.
> Atualizado: 09/06/2026

---

## Diagrama do Funil

```
┌─────────────────────────────────────────────────────────┐
│                    TOPO DO FUNIL (ToFu)                 │
│                                                         │
│  📱 META ADS (Facebook + Instagram)                     │
│  ├── Campanha: Criação de Audiência                     │
│  │   Objetivo: Alcance / Brand Awareness                │
│  │   Público: Frio (interesses: CLT, RH, gestão PME)   │
│  │   Budget: ~R$10/dia                                  │
│  │                                                      │
│  └── Campanha: Geração de Leads                         │
│      Objetivo: Lead Gen / Traffic                       │
│      Público: Frio + Lookalike                          │
│      Budget: ~R$13/dia                                  │
└────────────────────┬────────────────────────────────────┘
                     │ clique no anúncio
                     ▼
┌─────────────────────────────────────────────────────────┐
│                   MEIO DO FUNIL (MoFu)                  │
│                                                         │
│  🛒 PÁGINA DE VENDAS HOTMART                            │
│  URL: hotmart.com/product/empresa-protegida-nr1         │
│                                                         │
│  Pixel dispara: ViewContent                             │
│  Evento: Visita na Página de Produto Hotmart            │
│                                                         │
│  Elemento crítico: headline + prova social + CTA claro  │
│  Meta conversão: ≥2% de visitantes → checkout          │
└────────────────────┬────────────────────────────────────┘
                     │ clica em "Comprar"
                     ▼
┌─────────────────────────────────────────────────────────┐
│                FUNDO DO FUNIL (BoFu)                    │
│                                                         │
│  💳 CHECKOUT HOTMART                                    │
│  Pixel dispara: InitiateCheckout                        │
│  Evento: Visita na Página de Pagamento                  │
│                                                         │
│  Métodos: cartão / Pix / boleto                         │
│  Preço: R$27                                            │
└────────────────────┬────────────────────────────────────┘
                     │ pagamento aprovado
                     ▼
┌─────────────────────────────────────────────────────────┐
│                    CONVERSÃO ✅                          │
│                                                         │
│  🎉 COMPRA CONFIRMADA                                   │
│  Pixel dispara: Purchase (valor da transação)           │
│                                                         │
│  Hotmart entrega: PDF do eBook por e-mail               │
│  Próximo passo: entrar no Grupo WhatsApp                │
│  (CTA no eBook → wa.me/5531997194731)                   │
└────────────────────┬────────────────────────────────────┘
                     │ entra no grupo
                     ▼
┌─────────────────────────────────────────────────────────┐
│                    RETENÇÃO + UPSELL                    │
│                                                         │
│  💬 GRUPO WHATSAPP — Empresa Protegida™                 │
│  • Conteúdo gratuito (NR-1, portarias, checklists)      │
│  • Aquecimento para Degrau 2                            │
│  • Lançamento do Treinamento (R$297–497) — fase futura  │
└─────────────────────────────────────────────────────────┘
```

---

## KPIs por etapa

| Etapa | Métrica | Meta |
|---|---|---|
| Anúncio | CTR | ≥ 1,5% |
| Anúncio | CPC | ≤ R$1,50 |
| Página de vendas | Taxa de clique no CTA | ≥ 3% |
| Checkout | Taxa de abandono | ≤ 70% |
| Compra | CPA (Custo por Aquisição) | ≤ R$20 |
| Compra | ROAS | ≥ 1,35 |

---

## Pontos de otimização prioritários

1. **Criativo → CTR** — se CTR < 1,5%, trocar creative (Sobral: testar a cada 2–3 dias)
2. **LP → Checkout** — se < 2% chegam ao checkout, revisar headline e prova social da página Hotmart
3. **Checkout → Compra** — se abandono > 70%, verificar clareza do preço e trust signals
4. **Compra → Grupo** — CTA no eBook precisa ser claro (✅ já atualizado)

---

## Remarketing (ativar quando tiver volume)

| Audiência | Evento base | Campanha |
|---|---|---|
| Visitou a página de produto | ViewContent | Anúncio de remarketing (urgência) |
| Iniciou checkout mas não comprou | InitiateCheckout | Anúncio de abandono (desconto ou escassez) |
| Comprou | Purchase | Lookalike 1% → Campanha de escala |
