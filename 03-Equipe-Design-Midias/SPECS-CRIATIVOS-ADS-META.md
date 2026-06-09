# Specs de Produção — Criativos de Anúncio Meta
## Empresa Protegida™ · Handoff para Designer

> Gerado por **Design Squad (UI Engineer + Dan Mall)** · 05/06/2026
> Ferramenta recomendada: **Canva Pro** ou Adobe Express
> Todos os valores são exatos — não estimar, não aproximar.

---

## TOKENS DE IDENTIDADE VISUAL

### Paleta de Cores

| Token | Hex | Uso |
|---|---|---|
| `--navy` | `#111111` | Fundo escuro, fundo de capa e slide 5 |
| `--red` | `#C41010` | Acento, CTA, bordas de destaque, numeração ERRO |
| `--red-soft` | `#E02020` | Hover de botão, destaque secundário |
| `--gold` | `#C9A96E` | Escudo dourado, detalhes premium |
| `--white` | `#FFFFFF` | Texto sobre fundo escuro |
| `--cream` | `#FAFAF8` | Fundo slides 2–4 (erros) |
| `--muted` | `#666666` | Texto secundário, copy de suporte |
| `--ink` | `#1A1A1A` | Texto principal sobre fundo claro |
| `--overlay-30` | `rgba(17,17,17,0.30)` | Overlay leve sobre foto |
| `--overlay-70` | `rgba(17,17,17,0.70)` | Overlay sobre legenda queimada |

### Tipografia

| Token | Família | Peso | Tamanho base | Uso |
|---|---|---|---|---|
| `--font-display` | Playfair Display | 800 | variável | Headlines principais |
| `--font-title` | Playfair Display | 700 | variável | Títulos de seção |
| `--font-body` | Inter | 400 | variável | Corpo de texto |
| `--font-body-light` | Inter | 300 | variável | Subtítulos, copy leve |
| `--font-label` | Inter | 700 | variável | Labels, CTAs, badges |
| `--font-micro` | Inter | 600 | variável | Rodapés, @handles |

### Escudo SVG (Visual Hammer)

```svg
<!-- Escudo padrão — usar em todos os criativos -->
<svg viewBox="0 0 60 72" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M30 2L4 13V33C4 52 15 65 30 70C45 65 56 52 56 33V13L30 2Z"
        fill="#C9A96E"/>
</svg>

<!-- Escudo outline (versão wireframe para fundo claro) -->
<svg viewBox="0 0 60 72" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path d="M30 2L4 13V33C4 52 15 65 30 70C45 65 56 52 56 33V13L30 2Z"
        fill="none" stroke="#C41010" stroke-width="2"/>
</svg>
```

---

## CRIATIVO 1 — REEL · 1080 × 1920px · 9:16

**Arquivo de saída:** `AD1-Reel-Alerta-1080x1920.mp4`
**Duração:** 20 segundos · 30fps
**Ferramenta:** CapCut, Canva (apresentação → exportar vídeo) ou DaVinci Resolve

### Grid e Zonas Seguras

```
┌─────────────────────────────┐  ← 1080px
│  ZONA MORTA TOPO (150px)    │  ← UI do Instagram cobre
├─────────────────────────────┤
│                             │
│   ZONA SEGURA DE CONTEÚDO   │  ← 1620px úteis
│        (1080 × 1620)        │
│                             │
├─────────────────────────────┤
│  ZONA MORTA BASE (150px)    │  ← Botões de ação cobrem
└─────────────────────────────┘
```

### Spec por Cena

#### CENA 1 — Gancho (0–3s)

| Elemento | Spec |
|---|---|
| Fundo | Vídeo do Guilherme (câmera direta, blazer navy) · fundo ambiente escuro |
| Overlay | `rgba(17,17,17,0.20)` sobre o vídeo inteiro |
| **Escudo** | SVG dourado · `160 × 192px` · posição: `x=60px, y=1650px` (canto inf. esq.) · **aparece com fade-in 0.5s** |
| **Texto gancho** | Não aparece na cena 1 — a fala carrega o gancho |
| Animação escudo | opacity 0→1 em 500ms, easing ease-out |

#### CENA 2 — Corpo (3–15s)

| Elemento | Spec |
|---|---|
| Fundo | Continuação do vídeo do Guilherme |
| **Legenda queimada** | Fundo pill `--overlay-70` · border-radius 8px · padding 12px 20px |
| Fonte legenda | Inter 700 · `52px` · cor `#FFFFFF` · line-height 1.3 |
| Posição legenda | Centro horizontal · `y=1480px` (acima da zona morta base) |
| Largura máx. legenda | `860px` (margem de 110px em cada lado) |
| Escudo | Permanece no canto inf. esq. · `opacity: 0.85` |
| **Linha vermelha** | `1080 × 4px` · cor `#C41010` · `y=1616px` (acima zona morta) |

**Texto queimado por bloco (sincronizar com a fala):**
```
Bloco 1: "Desde 26 de maio de 2026..."
Bloco 2: "...sua empresa já pode ser autuada"
Bloco 3: "por um risco psicossocial."
Bloco 4: "Pressão. Sobrecarga. Conflito."
Bloco 5: "A NR-1 exige documentação."
Bloco 6: "E o fiscal já chegou pra PME."
```

#### CENA 3 — CTA (15–20s)

| Elemento | Spec |
|---|---|
| Fundo | Fade para `#111111` sólido (transição 0.5s do vídeo) |
| **Escudo** | Centralizado · `240 × 288px` · `opacity: 0.15` (watermark) |
| **Texto CTA linha 1** | "Guia Empresa Protegida™" · Playfair Display 700 · `64px` · `#FFFFFF` · centro |
| **Texto CTA linha 2** | "NR-1 sem complicação" · Inter 300 · `36px` · `rgba(255,255,255,0.65)` · centro |
| **Preço** | "R$ 27" · Inter 800 · `80px` · `#C41010` · centro |
| **Botão** | `600 × 96px` · bg `#C41010` · border-radius `12px` · texto "Link na bio 🛡️" · Inter 700 · `36px` · `#FFFFFF` |
| Posição botão | Centro horizontal · `y=1520px` |
| **@handle** | "@guiavelaroficial" · Inter 600 · `28px` · `rgba(255,255,255,0.35)` · centro · `y=1650px` |

### Exportação

- Formato: MP4 · H.264 · bitrate mínimo 4Mbps
- Resolução: 1080 × 1920px
- Fps: 30
- Áudio: manter áudio original do Guilherme · normalizar em -14 LUFS
- Thumbnail: frame do escudo aparecendo (aprox. 0.8s)

---

## CRIATIVO 2 — ESTÁTICA · Feed 1080×1080px + Story 1080×1920px

**Arquivos de saída:**
- `AD2-Estatica-Feed-1080x1080.png`
- `AD2-Estatica-Story-1080x1920.png`

### VERSÃO FEED — 1080 × 1080px

#### Grid

```
┌──────────────────────────────┐ ← 1080px
│     Margin top: 80px         │
│  ┌────────────────────────┐  │
│  │   Área útil: 920×920   │  │ ← margin 80px em cada lado
│  │                        │  │
│  │    [ESCUDO central]    │  │
│  │                        │  │
│  │  [HEADLINE]            │  │
│  │  [SUBTÍTULO]           │  │
│  │                        │  │
│  │  [FOTO miniatura]  ●   │  │
│  └────────────────────────┘  │
│  [BARRA VERMELHA 6px base]   │
└──────────────────────────────┘
```

#### Especificações de Cada Elemento

| Elemento | Posição (x, y) | Dimensão | Estilo |
|---|---|---|---|
| **Fundo** | 0, 0 | 1080×1080 | cor `#111111` sólido |
| **Escudo SVG** | centro, y=280px | 220×264px | fill `#C9A96E` · opacity 1 |
| **Badge texto** | centro, y=130px | auto | "🛡️ EMPRESA PROTEGIDA™" · Inter 700 · 22px · `#C41010` · letter-spacing 0.2em |
| **Headline** | centro, y=580px | max-w 860px | "Sua empresa está protegida contra a nova NR-1?" · Playfair Display 800 · 64px · `#FFFFFF` · line-height 1.1 · alinhamento centro |
| **Subtítulo** | centro, y=760px | max-w 760px | "Entenda os riscos psicossociais e comece a se adequar — sem juridiquês." · Inter 300 · 32px · `rgba(255,255,255,0.65)` · linha-height 1.4 |
| **Foto Guilherme** | x=900px, y=900px | 120×120px circular | object-fit cover · object-position center top · border 3px `rgba(255,255,255,0.3)` |
| **Nome autor** | x=700px, y=900px | auto | "Guilherme Avelar" · Inter 600 · 24px · `#FFFFFF` |
| **Handle** | x=700px, y=930px | auto | "@guiavelaroficial ✓" · Inter 400 · 20px · `rgba(255,255,255,0.4)` |
| **Linha decorativa** | centro, y=548px | 60×3px | cor `#C41010` |
| **Barra base** | 0, 1074px | 1080×6px | cor `#C41010` |

### VERSÃO STORY — 1080 × 1920px

Reaproveitamento da versão feed com adaptações:

| Ajuste | Spec |
|---|---|
| Escudo | Aumentar para 300×360px · y=420px |
| Headline | Fonte 72px · y=900px |
| Subtítulo | Fonte 36px · y=1100px · max-w 860px |
| Foto autor | Aumentar para 150×150px · posicionar x=860px, y=1620px |
| Área segura topo | Não colocar elementos acima de y=200px (UI do app cobre) |
| Área segura base | Não colocar elementos abaixo de y=1720px (botões cobrem) |
| Barra base | y=1914px |

### Exportação Estática

- Formato: PNG · 72dpi (Meta não requer mais)
- Tamanho máx. arquivo: 30MB (PNG com fundo sólido fica ~2MB)
- Perfil de cor: sRGB
- Texto em imagem: Meta penaliza imagens com >20% de área coberta por texto — manter headline + subtítulo dentro do limite

---

## CRIATIVO 3 — CARROSSEL · 5 slides · 1080 × 1080px cada

**Arquivos de saída:**
- `AD3-Carrossel-Slide1-Capa.png`
- `AD3-Carrossel-Slide2-Erro1.png`
- `AD3-Carrossel-Slide3-Erro2.png`
- `AD3-Carrossel-Slide4-Erro3.png`
- `AD3-Carrossel-Slide5-Oferta.png`

### SISTEMA DE GRID DOS SLIDES

```
Margem horizontal: 80px em cada lado → área útil: 920px
Margem vertical: 80px topo, 100px base → área útil: 900px
Rodapé fixo (todos os slides): altura 60px · y=980px
```

### SLIDE 1 — CAPA (fundo navy)

| Elemento | Posição | Dimensão | Estilo |
|---|---|---|---|
| Fundo | 0, 0 | 1080×1080 | `#111111` |
| Escudo SVG | centro, y=220px | 160×192px | fill `#C9A96E` |
| **Número "3"** | centro, y=440px | auto | Inter 800 · 200px · `#C41010` · opacity 0.15 (watermark atrás do escudo) |
| **Título linha 1** | centro, y=500px | max-w 860px | "3 erros que deixam" · Playfair Display 700 · 56px · `#FFFFFF` |
| **Título linha 2** | centro, y=580px | max-w 860px | "sua empresa exposta" · Playfair Display 700 · 56px · `#FFFFFF` |
| **Título linha 3** | centro, y=660px | max-w 860px | "à nova NR-1 🛡️" · Playfair Display 700 · 56px · `#C41010` |
| Subtítulo | centro, y=760px | max-w 760px | "Se você tem CLT, deslize →" · Inter 400 · 28px · `rgba(255,255,255,0.5)` |
| **Seta deslize** | x=960px, y=500px | 40px | "→" · Inter 700 · 48px · `rgba(255,255,255,0.3)` |
| Rodapé | 0, 980px | 1080×100px | fundo `rgba(196,16,16,0.15)` · texto "Empresa Protegida™" · Inter 700 · 22px · `#C41010` · centro |

### SLIDES 2, 3, 4 — ERROS (fundo claro)

**Template base igual para os 3 — só muda número, título e copy.**

| Elemento | Posição | Dimensão | Estilo |
|---|---|---|---|
| Fundo | 0, 0 | 1080×1080 | `#FAFAF8` |
| **Borda esquerda** | 0, 0 | 6×1080px | `#C41010` sólido |
| **Badge ERRO X** | x=80px, y=80px | auto | "ERRO 1" (ou 2, 3) · Inter 800 · 28px · `#C41010` · letter-spacing 0.15em |
| **Linha decorativa** | x=80px, y=130px | 60×3px | `#C41010` |
| **Título** | x=80px, y=180px | max-w 860px | texto do erro · Playfair Display 700 · 60px · `#1A1A1A` · line-height 1.15 |
| **Copy suporte** | x=80px, y=420px | max-w 860px | texto de suporte · Inter 400 · 34px · `#444444` · line-height 1.5 |
| Escudo outline | x=880px, y=80px | 80×96px | stroke `rgba(196,16,16,0.2)` · fill none |
| Rodapé | 0, 980px | 1080×100px | fundo `#111111` · texto "Empresa Protegida™" · Inter 700 · 22px · `#C41010` · centro |

**Variações por slide:**

| Slide | Badge | Título | Copy |
|---|---|---|---|
| 2 | ERRO 1 | Achar que NR-1 é só para empresa grande | A lei não tem limite mínimo. Se tem um CLT, a obrigação é sua — e o fiscal não pergunta o tamanho antes de autuar. |
| 3 | ERRO 2 | Confundir risco psicossocial com "problema de RH" | Pressão por metas, conflitos, sobrecarga agora são fiscalizáveis. Não basta bom ambiente — precisa documentar. |
| 4 | ERRO 3 | Esperar a visita do fiscal para se organizar | A fiscalização punitiva começou em 26/05/2026. Quem ainda "vai se organizar" já está em risco. |

### SLIDE 5 — OFERTA (fundo navy)

| Elemento | Posição | Dimensão | Estilo |
|---|---|---|---|
| Fundo | 0, 0 | 1080×1080 | `#111111` |
| Escudo SVG | centro, y=180px | 200×240px | fill `#C9A96E` |
| **Título** | centro, y=460px | max-w 860px | "Proteja sua empresa" · Playfair Display 800 · 64px · `#FFFFFF` |
| **Título linha 2** | centro, y=548px | max-w 860px | "ainda hoje." · Playfair Display 800 · 64px · `#FFFFFF` |
| **Preço** | centro, y=650px | auto | "R$ 27" · Inter 800 · 96px · `#C41010` |
| Copy | centro, y=780px | max-w 760px | "Garantia incondicional de 7 dias" · Inter 300 · 28px · `rgba(255,255,255,0.6)` |
| **Botão CTA** | centro, y=880px | 640×80px | bg `#C41010` · border-radius 12px · "Garantir meu guia agora →" · Inter 700 · 30px · `#FFFFFF` |
| Rodapé | 0, 980px | 1080×100px | fundo `rgba(196,16,16,0.15)` · "Empresa Protegida™" · Inter 700 · 22px · `#C41010` · centro |

---

## CHECKLIST DE EXPORTAÇÃO — META ADS

### Formatos obrigatórios

| Criativo | Formato | Resolução | Limite de tamanho |
|---|---|---|---|
| Reel (vídeo) | MP4 · H.264 | 1080×1920px | 4GB (na prática: < 100MB) |
| Estática feed | PNG ou JPG | 1080×1080px | 30MB |
| Estática story | PNG ou JPG | 1080×1920px | 30MB |
| Carrossel (cada slide) | PNG ou JPG | 1080×1080px | 30MB por slide |

### Nomes de arquivo para entrega

```
AD1-Reel-Alerta-vA-1080x1920.mp4
AD1-Reel-Alerta-vB-1080x1920.mp4
AD2-Estatica-Feed-HeadlineA-1080x1080.png
AD2-Estatica-Feed-HeadlineC-1080x1080.png
AD2-Estatica-Story-1080x1920.png
AD3-Carrossel-S1-Capa.png
AD3-Carrossel-S2-Erro1.png
AD3-Carrossel-S3-Erro2.png
AD3-Carrossel-S4-Erro3.png
AD3-Carrossel-S5-Oferta.png
```

### Regra dos 20% de texto (Meta)

Meta penaliza imagens com muita área de texto — checar com a ferramenta:
https://www.facebook.com/ads/tools/text_overlay

Peças com risco: AD2 (estática) — manter headline curta, dar espaço ao escudo e à foto.

---

## NOTAS DE QA — verificar antes de entregar

- [ ] Escudo dourado (`#C9A96E`) presente em todos os criativos
- [ ] Barra vermelha `#C41010` de 6px na base dos slides 1 e 5 do carrossel e na estática feed
- [ ] Foto do Guilherme com `object-position: center top` (mostra o rosto, não o corpo)
- [ ] Texto da legenda do Reel legível em fundo escuro e fundo claro
- [ ] Nenhuma promessa de "zero multa" em nenhuma peça visual
- [ ] "@guiavelaroficial" presente em todos os criativos (autoridade)
- [ ] Rodapé "Empresa Protegida™" em todos os slides do carrossel
- [ ] Testar visualização no celular antes de subir (zoom 100% em tela de 6")
