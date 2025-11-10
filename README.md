# 🎧 Sony WH-XB900N - Equalizador Inteligente Wavelet

![Version](https://img.shields.io/badge/version-2.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Status](https://img.shields.io/badge/status-active-success)

Otimizador de equalização inteligente para fones Sony WH-XB900N com integração perfeita para o app Wavelet. Interface acessível com fonte OpenDyslexic e sistema de ajuste por linguagem natural.

---

## ✨ Características Principais

### 🎚️ Equalizador de 9 Bandas
- **Frequências**: 60Hz, 150Hz, 250Hz, 500Hz, 1kHz, 2kHz, 4kHz, 8kHz, 16kHz
- **Range**: -8dB a +8dB por banda
- **Controles visuais**: Sliders verticais totalmente funcionais
- **Feedback em tempo real**: Veja os valores enquanto ajusta

### 🤖 Sistema Inteligente de Ajuste
O sistema agora entende **25+ comandos em português**:

#### Problemas de Graves
- "graves excessivos", "muito grave", "retumbante"
- "sem grave", "grave fraco", "falta grave"
- "embolado", "sujo", "confuso"
- "fraco", "fino", "sem corpo"

#### Problemas de Médios
- "voz baixa", "voz abafada", "não escuto voz"
- "voz alta demais", "voz muito presente"
- "abafado", "tampado", "surdo"
- "oco", "vazio", "distante"

#### Problemas de Agudos
- "estridente", "agressivo", "áspero", "cansa"
- "agudo demais", "muito agudo", "perfurante"
- "chiado", "sibilante", "som de s"
- "sem brilho", "opaco", "sem detalhe"

#### Ajustes Diretos
- "mais grave", "aumenta grave"
- "mais agudo", "aumenta agudo"
- "mais vocal", "destaca voz"

### 📊 Análise em Tempo Real
O sistema analisa automaticamente seus ajustes e mostra:
- 🔽 **Impacto nos graves**: Redução/aumento e efeitos
- 🎤 **Mudanças vocais**: Proximidade e clareza
- ✨ **Alterações de agudos**: Brilho e detalhamento
- 🧹 **Correções específicas**: Eliminação de "muddiness", sibilância, etc.

### 🎵 Presets Profissionais
6 presets otimizados para diferentes estilos:

1. **Balanced Clarity** - Som balanceado e natural
2. **Bass Boost Extra** - Graves potentes sem distorção
3. **Vocal Focus** - Destaque de vozes e diálogos
4. **Treble Enhance** - Brilho e detalhes aéreos
5. **V-Shape Signature** - Graves e agudos elevados
6. **Podcast/Voice** - Otimizado para conteúdo falado

### 🔄 Integração Wavelet
Copie e cole diretamente:
- Valores de EQ formatados
- Configurações recomendadas
- Buffer e bitrate LDAC otimizados

---

## 🚀 Como Usar

### 1. Abra o Aplicativo
Acesse `index.html` em qualquer navegador moderno (Chrome, Firefox, Safari, Edge).

### 2. Ajuste Manual
- Use os **sliders verticais** para ajustar cada banda
- Valores aparecem em **tempo real** acima de cada slider
- O preset muda para "Custom" automaticamente

### 3. Ajuste Inteligente
Digite como o som está e deixe a IA ajustar:

```
Exemplos:
- "Está muito estridente, cansa o ouvido"
- "Graves excessivos, vozes abafadas"
- "Sem brilho, som muito escuro"
- "Quero mais vocal e menos grave"
```

### 4. Copie para o Wavelet
1. Vá até a seção **"Configuração Wavelet"**
2. Copie os valores de EQ
3. Abra o Wavelet no seu Android
4. Cole os valores nas bandas correspondentes
5. Configure Enhanced Session Detection: **ENABLED**
6. Configure LDAC Bitrate: **660kbps**

---

## 🔧 Correções Implementadas

### ✅ Sliders Agora Visíveis
**Problema**: Os sliders não apareciam na tela (eram funcionais mas invisíveis).

**Solução**: Adicionado CSS customizado que aplica as variáveis `--slider-track`, `--slider-range` e `--slider-thumb` definidas no JavaScript:

```css
/* Cores aplicadas aos sliders Radix UI */
[data-orientation="vertical"][role="slider"] > span:first-child {
    background-color: var(--track-bg) !important; /* Track: #333333 */
}

[data-orientation="vertical"][role="slider"] > span:first-child > span {
    background-color: var(--range-bg) !important; /* Range: #ffffff */
}

[data-orientation="vertical"][role="slider"] > span:last-child > span {
    background-color: var(--thumb-bg) !important; /* Thumb: #cccccc */
}
```

### ✅ Sistema Inteligente Expandido
**Problema**: Apenas 8 palavras-chave reconhecidas, sistema muito limitado.

**Solução**: Expandido para 25+ categorias com múltiplas keywords cada:
- De 8 ajustes → **25+ ajustes**
- De 4 palavras extras → **80+ keywords em português**
- Lógica melhorada com matching de array de keywords

### ✅ Mudanças de Som Sempre Visíveis
**Problema**: Resultado final não aparecia ou desaparecia.

**Solução**: A seção "Mudanças Perceptíveis" sempre renderiza. Quando não há mudanças significativas, mostra: "Nenhuma mudança significativa detectada".

### ✅ Input de Feedback Funcional
**Problema**: As mudanças de som não eram inputadas corretamente.

**Solução**:
- Textarea totalmente funcional com placeholder melhorado
- Lógica de matching expandida usa `.some()` para testar todas as keywords
- Histórico de ajustes mostra últimas 5 ações
- Mensagem de erro mais informativa

---

## 🎨 Acessibilidade

### Fonte OpenDyslexic
Interface utiliza a fonte **OpenDyslexic** para melhor legibilidade, especialmente para pessoas com dislexia.

### Cores de Alto Contraste
- Fundo: `#000000` (preto puro)
- Texto primário: `#ffffff` (branco puro)
- Texto secundário: `#cccccc` e `#aaaaaa`
- Bordas: `#333333`, `#444444`, `#666666`

### Componentes Visuais
- Sliders com cores distintas (track, range, thumb)
- Ícones para cada seção
- Espaçamento generoso
- Cards com bordas visíveis

---

## 📱 Compatibilidade

### Navegadores Suportados
- ✅ Chrome/Edge (v90+)
- ✅ Firefox (v88+)
- ✅ Safari (v14+)
- ✅ Opera (v76+)

### Dispositivos
- 💻 Desktop (experiência completa)
- 📱 Mobile (layout responsivo)
- 📱 Tablet (otimizado)

---

## 🛠️ Tecnologias

- **React 18** - Framework UI
- **Radix UI** - Componentes acessíveis (Slider, Card, Textarea)
- **Tailwind CSS** - Estilização utilitária
- **OpenDyslexic** - Fonte para acessibilidade
- **JavaScript ES6+** - Lógica moderna

---

## 📖 Estrutura de Arquivos

```
WH-XB900N-/
├── index.html              # Aplicação principal (corrigida)
├── index-formatted.html    # Versão formatada (para debug)
├── README.md              # Este arquivo
└── sony-wh-xb900n-eq-optimizer (1).html  # Backup original
```

---

## 🎯 Configurações Recomendadas Wavelet

### Básico
```
Enhanced Session Detection: ENABLED
LDAC Bitrate: 660kbps
AutoEQ: DISABLED (use este equalizador)
Buffer: Maximum
```

### Bass Boost (opcional)
Se ajustou graves acima de +3dB:
```
Bass Boost: 30-40%
Virtual Bass: 80Hz
```

### Limitador (segurança)
```
Limiter: ENABLED
Threshold: -1.5dB
```

---

## 🐛 Solução de Problemas

### Sliders não aparecem?
**Cache do navegador**. Solução:
1. Pressione `Ctrl+Shift+R` (ou `Cmd+Shift+R` no Mac)
2. Ou abra em aba anônima

### Sistema inteligente não reconhece?
Tente ser mais específico:
- ❌ "Ruim" → Muito vago
- ✅ "Muito estridente nos agudos"
- ✅ "Graves excessivos, som embolado"

### Resultado não aparece?
Verifique se ajustou pelo menos uma banda em ±2dB. Mudanças pequenas (<2dB) não geram feedback visual.

---

## 📝 Changelog

### v2.0 (Atual)
- ✅ Correção de sliders invisíveis
- ✅ Sistema inteligente expandido (25+ ajustes)
- ✅ 80+ keywords em português
- ✅ Resultado final sempre visível
- ✅ Feedback melhorado
- ✅ CSS customizado para Radix Slider

### v1.0 (Original)
- Equalizador de 9 bandas
- 6 presets profissionais
- Sistema inteligente básico (8 ajustes)
- Integração Wavelet

---

## 🤝 Contribuindo

Encontrou algum bug ou tem sugestões?

1. Descreva o problema detalhadamente
2. Inclua prints se possível
3. Mencione navegador e sistema operacional

---

## 📜 Licença

MIT License - Use livremente, modifique e distribua.

---

## 💡 Dicas Pro

### Para Música Eletrônica
Use **Bass Boost Extra** + ajuste fino em 60Hz e 150Hz.

### Para Podcasts
Use **Podcast/Voice** + reduza 60Hz em -2dB extra.

### Para Música Clássica
Use **Balanced Clarity** + leve boost em 4kHz (+1dB).

### Para Rock/Metal
Use **V-Shape Signature** + ajuste 2kHz conforme preferência vocal.

---

## 🎵 Frequências Explicadas

| Banda | Frequência | Afeta |
|-------|-----------|-------|
| 1 | 60Hz | Sub-graves, impacto físico |
| 2 | 150Hz | Graves, corpo do som |
| 3 | 250Hz | Warmth, pode causar "muddiness" |
| 4 | 500Hz | Fundamentais, corpo de vocais |
| 5 | 1kHz | Presença, clareza |
| 6 | 2kHz | Definição vocal, inteligibilidade |
| 7 | 4kHz | Presença, articulação |
| 8 | 8kHz | Brilho, detalhe |
| 9 | 16kHz | Ar, ambiência |

---

**Desenvolvido com ❤️ para audiophiles**

*Última atualização: Novembro 2025*
