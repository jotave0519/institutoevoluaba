# Brand Guidelines v1.0 — Instituto Evoluaba

> Última atualização: 2026-09-13
> Status: Documentado a partir da identidade visual real já em uso em institutoevoluaba.com.br
> Fonte: CSS e ativos extraídos do site ao vivo da clínica (não inventados), mais decisões de composição tomadas ao construir a landing page de Avaliação Neuropsicológica.

## Referência rápida

| Elemento | Valor |
|---------|-------|
| Primary Color | #D99B1A |
| Secondary Color | #1A1530 |
| Accent Color | #E8B54A |
| Primary Font | Fraunces (títulos) |
| Voice | Acolhedora, direta, específica — sem jargão vago |

---

## 1. Color Palette

### Primary Colors

| Name | Hex | RGB | Uso |
|------|-----|-----|-----|
| Primary Blue | #D99B1A | rgb(217,155,26) | Dourado/mostarda: cor de ação da especialidade Neuropsicologia. CTA principal, ícones de destaque, sublinhados |
| Primary Dark | #A3730E | rgb(163,115,14) | Hover de fundo, elementos que precisam de mais peso visual sobre fundo claro |

*(Os nomes de linha "Blue/Dark" vêm do template padrão da skill `brand` — o valor real é o dourado da marca, não azul.)*

### Secondary Colors

| Name | Hex | RGB | Uso |
|------|-----|-----|-----|
| Secondary Purple | #1A1530 | rgb(26,21,48) | Tinta: cor de texto principal, fundo de seções escuras (CTA final, rodapé) |
| Accent Green | #E8B54A | rgb(232,181,74) | Dourado claro: hover de botão, texto de eyebrow sobre fundo escuro |

### Neutral Palette

| Name | Hex | RGB | Uso |
|------|-----|-----|-----|
| Background | #FBF8F3 | rgb(251,248,243) | Fundo geral das páginas (creme) |
| Surface | #F4EFE6 | rgb(244,239,230) | Fundo de seções alternadas, cards sobre fundo creme |
| Card | #FFFFFF | rgb(255,255,255) | Fundo de cards individuais |
| Text Primary | #1A1530 | rgb(26,21,48) | Títulos e texto de maior ênfase |
| Text Secondary | #4A4560 | rgb(74,69,96) | Corpo de texto |
| Text Muted | #7A7590 | rgb(122,117,144) | Legendas, texto auxiliar |
| Border | #E8E2D4 | rgb(232,226,212) | Divisores, bordas de card |

### Cores por especialidade (uso real observado no site)

O Instituto Evoluaba usa uma cor própria para cada especialidade da clínica multidisciplinar. Use estas cores apenas para identificar a especialidade correspondente (chips, tags, ícones), nunca como substituto da paleta principal:

| Especialidade | Hex |
|---|---|
| Neuropsicologia | #D99B1A (dourado, cor "primary" da marca) |
| Fonoaudiologia | #2BB5E0 |
| Psicologia | #E91E8C |
| Terapia ABA | #F77F00 |
| Psicomotricidade | #06A77D |
| Terapia Ocupacional | #E63946 |
| Musicoterapia | #7B3FA9 |

### Accessibility

Pares validados matematicamente (fórmula de contraste relativo WCAG) na landing page de Avaliação Neuropsicológica:

| Combinação | Contraste | Nível |
|---|---|---|
| Texto tinta (#1A1530) sobre dourado (#D99B1A) — botão principal | 7.25:1 | AAA |
| Texto secundário (#4A4560) sobre fundo creme (#FBF8F3) | 8.58:1 | AAA |
| Eyebrow (#8F6209, variante mais escura do dourado) sobre fundo creme | 5.06:1 | AA |
| Texto claro (#C4BFD4) sobre fundo tinta (#1A1530) — seção CTA final | 9.84:1 | AAA |
| Texto do rodapé (#9089A6) sobre fundo tinta escura (#140F26) | 5.61:1 | AA |

**Regra prática:** nunca usar branco puro como texto sobre o dourado principal (#D99B1A) — o contraste fica em 2.43:1, abaixo do mínimo AA. Use sempre a tinta escura (#1A1530) como texto sobre dourado.

---

## 2. Typography

### Font Stack

```css
--font-heading: 'Fraunces', Georgia, 'Times New Roman', serif;
--font-body: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
```

Fraunces é uma serifada com eixo itálico e de peso variável (opsz); use peso 400 (regular) para títulos grandes — peso 600+ some com o caráter elegante e fino que já é a marca registrada visual do site. Use itálico peso 300–400 para elementos decorativos (numeração i./ii./iii., faixa de palavras-chave rolando).

### Carregamento de fontes

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,300;1,9..144,500&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### Type Scale (usado na landing page de referência)

| Elemento | Tamanho (desktop) | Peso | Font |
|---|---|---|---|
| H1 | clamp(28px, 3.6vw, 42px) | 400 | Fraunces |
| H2 | ~32px | 400 | Fraunces |
| H3 | ~18px | 500 | Fraunces |
| Corpo | 16px | 400 | Inter |
| Eyebrow (rótulo de seção) | 12px, maiúsculas, letter-spacing 0.2em | 600 | Inter |

---

## 3. Logo

### Ativo disponível

Hoje existe apenas **um** arquivo de logo confirmado: um PNG quadrado (270×270, com transparência) com a borboleta de peças de quebra-cabeça saindo do casulo dourado, mais o wordmark "INSTITUTO EVOLUABA" embutido na própria imagem, extraído do favicon do site (`cropped-favicon-evoluaba-270x270.png`).

**Não existem ainda**, até onde foi possível confirmar: uma versão horizontal separada, uma versão só do ícone sem o texto, nem uma versão monocromática. Se a clínica tiver esses arquivos em outro lugar (ex: pasta de identidade visual usada por um designer), vale reunir aqui.

### Uso observado

- Em fundos claros (creme, branco): a logo funciona bem no tamanho original.
- Em fundos escuros (tinta #1A1530): **evitar** usar a logo, porque o texto "INSTITUTO" embutido na imagem é escuro e some por cima do fundo escuro. Nesses contextos (ex: rodapé), usar wordmark de texto simples na cor clara em vez da imagem.
- Tamanho mínimo recomendado: 40px de altura (abaixo disso, o texto embutido na imagem fica ilegível; o ícone da borboleta ainda funciona sozinho).

### Don'ts

- Não usar a logo sobre o fundo escuro da marca (ver acima).
- Não recolorir a borboleta (o efeito de peças coloridas é o elemento mais reconhecível da marca).
- Não esticar fora da proporção quadrada original.

---

## 4. Voice & Tone

### Observação sobre a voz já estabelecida

O site institucional atual (institutoevoluaba.com.br) usa uma voz acolhedora e reflexiva, com frases como "a família precisa de mais clareza, não mais opiniões" e "compreensão mais aprofundada". Isso comunica cuidado, mas tende a ficar abstrato — a página de Avaliação Neuropsicológica antiga, por exemplo, nunca chegava a citar sintomas concretos (TDAH, dificuldade de aprendizagem, memória) pelo nome.

### Recomendação para páginas de conversão (Google Ads, landing pages)

Para páginas com objetivo de conversão direta, recomenda-se manter o acolhimento mas ancorar em **sinais concretos e linguagem específica**, seguindo os princípios da skill `copywriting` (clareza antes de tudo, benefícios antes de recursos, especificidade antes de vago) e `humanizer` (evitar contrastes do tipo "não X mas Y", tríades forçadas, fechamentos de uma linha, travessões em excesso).

### Brand Personality

| Traço | Descrição |
|-------|-----------|
| **Acolhedora** | Entende a ansiedade da família, sem ser piegas |
| **Direta** | Vai ao ponto sobre sintomas e processo, sem rodeios |
| **Específica** | Cita sinais concretos em vez de "dificuldades" genéricas |
| **Multidisciplinar** | Comunica que faz parte de uma clínica maior (fono, psicologia, TO etc.), não uma especialidade isolada |

### Termos a evitar

| Evitar | Motivo |
|-------|--------|
| "compreensão mais aprofundada" / "profundidade" | Vago, repetido em excesso no site atual, não diz nada específico |
| "revolucionário", "estado da arte" | Não se aplica a um serviço de saúde e soa exagerado |
| Travessões (—) em prosa | Tell comum de texto gerado por IA (skill `humanizer`) |
| Promessas categóricas não verificáveis (“garantimos”, “resolve totalmente”) | Risco ético/legal em conteúdo de saúde |

---

## 5. Imagery Guidelines (recomendação — fotos reais ainda pendentes)

Nenhuma foto real da clínica foi fornecida até o momento; as landing pages usam placeholders `[FOTO: ...]` claramente marcados. Quando as fotos reais estiverem disponíveis, recomenda-se:

- **Pessoas reais**, não banco de imagens genérico — a autenticidade é justamente o que falta hoje.
- **Luz natural, ambiente acolhedor**, evitando o clichê de consultório clínico frio.
- **Crianças/adolescentes**: sempre com autorização de uso de imagem por escrito dos responsáveis.
- Tratamento de cor neutro, sem filtro pesado, para não destoar da paleta creme/dourado do site.

---

## 6. Design Components (implementados na landing page de referência)

### Botões

| Tipo | Fundo | Texto | Border Radius |
|------|-------|-------|----------------|
| Primário (CTA) | #D99B1A | #1A1530 | 999px (pílula) |
| Primário (hover) | #E8B54A | #1A1530 | 999px |

### Cards e superfícies

| Elemento | Radius |
|---|---|
| Cards (depoimentos, sinais, passos) | 24px |
| Selos flutuantes (pill/badge sobre foto) | 14px / 999px |
| Placeholders de foto | 24px |

### Spacing

Escala usada: 6px, 10px, 14px, 16px, 18px, 22px, 24px, 32px, 40px, 48px, 56px, 80px (seções). Não segue uma escala numérica redonda (4/8/16/24/32/48) — foi ajustada visualmente durante a construção da página; considerar padronizar em uma escala formal se o design system crescer para mais páginas.

---

## Changelog

| Versão | Data | Mudanças |
|--------|------|----------|
| 1.0 | 2026-09-13 | Documento inicial, criado a partir da identidade real extraída do site ao vivo e das decisões tomadas na landing page de Avaliação Neuropsicológica |
