# Módulo Relé Temporizador Programável

# ⏱️ Manual do Temporizador Multifuncional DK-C-01

## 📘 Descrição Geral

**Nome do produto:** Módulo de relé temporizador programável  
**Modelo:** DK-C-01  
**Fabricante:** Shenzhen Deek Technology Co., Ltd.  

### Especificações Técnicas

| Parâmetro | Valor |
|------------|--------|
| Tensão de trabalho | DC 12 V (faixa de operação: 10 V – 16 V) |
| Tipo de entrada | DC 4 V – 20 V (botão, sensor PNP, sinal PLC, etc.) |
| Capacidade de saída | 30 V DC / 5 A ou 220 V AC / 5 A |
| Corrente em repouso | 20 mA |
| Corrente de trabalho | 50 mA |
| Vida útil | > 10 milhões de operações |
| Temperatura de trabalho | −40 °C ~ 85 °C |
| Peso | ~ 26 g |
| Dimensões | 64,2 mm × 34,8 mm × 18,5 mm |

### Recursos

- Circuito de entrada com proteção contra inversão de polaridade.  
- Isolamento óptico no sinal de entrada (alta imunidade a ruído).  
- Memória permanente dos parâmetros configurados.  
- MCU com programação online (pode ser personalizada pelo fabricante).  

---

## ⚙️ Funções dos Botões

| Botão | Função |
|--------|---------|
| **S1** | Pressione por 2 s para entrar no menu de seleção de modo (P-1 a P-4). Pressões curtas alternam os modos. |
| **S2** | Tecla **OK/Shift** — alterna a posição do dígito que pisca; confirma ajustes. |
| **S3** | Ajusta valores (0-9) ou posição do ponto decimal (ajustando a unidade de tempo). |

### Unidades de Tempo
- Ponto decimal na **unidade** → 0–999 minutos  
- Ponto decimal na **dezena** → 0–99,9 segundos  
- Sem ponto decimal → 0–999 segundos  

---

## 🧭 Modos de Operação

### 🔹 Modo P-1 — Temporizador Simples
- Ao receber o sinal de disparo, o relé **liga**, aguarda o tempo configurado e **desliga**.
- Sub-modos:
  - **A1** — novo disparo durante a contagem é ignorado.  
  - **A2** — novo disparo reinicia a contagem.  
  - **A3** — novo disparo cancela a contagem e desliga o relé.  

---

### 🔹 Modo P-2 — Temporização Dupla (Ligar/Desligar)
- Recebe o sinal de disparo:
  - Primeiro tempo (X): relé **liga**.  
  - Segundo tempo (Y): relé **desliga** após contagem.  

---

### 🔹 Modo P-3 — Ciclo Automático (Loop)
- **A1:** relé liga ao energizar, desliga após o tempo definido e repete infinitamente.  
- **A2:** relé inicia desligado, liga após o tempo configurado e repete infinitamente.  

---

### 🔹 Modo P-4 — Atraso de Ligar (Power-On Delay)
- Após energizar, aguarda o tempo definido e **liga o relé** automaticamente.  

---

## 🪛 Configuração Passo a Passo

1. Pressione **S1** por 2 s → entra no menu de modos.  
2. Use **S1** para escolher **P-1 ~ P-4**, confirme com **S2**.  
3. Se aplicável, selecione sub-modo (A1 / A2 / A3) e confirme.  
4. Ajuste o ponto decimal com **S3** (define unidade de tempo).  
5. Use **S2** para escolher o dígito e **S3** para ajustar valores.  
6. Confirme novamente com **S2** até parar o piscar do display.  

---

## 🧩 Ligações

O módulo e o dispositivo podem compartilhar a mesma fonte de alimentação (12 V DC).  
Possui proteção contra polaridade reversa e isolamento óptico no sinal de entrada.

---

## 🏭 Fabricante

**Shenzhen Deek Technology Co., Ltd.**  
China  

---

### 💾 Licença e Créditos

Este documento é uma tradução técnica adaptada para documentação em GitHub.  
Baseado no manual original: *“Multifunction Timer Delay DK-C-01”*.

