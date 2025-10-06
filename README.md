# Módulo Relé Temporizador Programável


# 🧠 Aula Prática – Módulo de Relé Temporizador Programável DK-C-01

## 🎯 **Título**
Explorando as Funções do Módulo Temporizador Programável DK-C-01

<img src="img/modulo_rele.jpg" alt="Módulo Relé DK-C-01" width="50%">

---

## 🎓 **Objetivo da Aula**
- Compreender o **princípio de funcionamento** de um **relé temporizador eletrônico programável**.  
- Configurar e testar **diferentes modos de operação (P-1 a P-4)** do módulo DK-C-01.  
- Aplicar o módulo em **situações práticas de automação**, como acionamento temporizado e controle cíclico de cargas.  
- Desenvolver habilidades de **interpretação de datasheet** e **configuração de parâmetros de temporização**.

---

## 🧰 **Materiais Necessários**
| Quantidade | Componente | Descrição |
|-------------|-------------|------------|
| 1 | Módulo DK-C-01 | Temporizador programável 12 V |
| 1 | Fonte de alimentação 12 V DC | 1 A mínimo |
| 1 | Lâmpada 127 V | Carga de teste |
| 1 | Multímetro | Para medições e verificação |
| 1 | Botão (push button) | Para simular sinal de disparo (trigger) |

---

## ⚙️ **Fundamentação Teórica**
O **módulo DK-C-01** é um **temporizador multifunção** com **display digital e três botões (S1, S2, S3)**.  
Ele permite configurar tempos de **atraso de ativação, desligamento, ciclos repetitivos e modos de operação automáticos**.

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

### Principais modos:

- **P-1:** Temporizador simples (liga e desliga após o tempo).  
- **P-2:** Temporização dupla (tempo de ligado + tempo de desligado).  
- **P-3:** Ciclo automático (liga/desliga em loop).  
- **P-4:** Atraso de ligação ao energizar.  

### Principais Funções:

- Controle de bombas de água.  
- Sistemas de ventilação com atraso.  
- Iluminação temporizada.  
- Controle de máquinas com pausa cíclica.

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

### 💾 Licença e Créditos

Este documento é uma tradução técnica adaptada para documentação em GitHub.  
Baseado no manual original: *“Multifunction Timer Delay DK-C-01”*.

## 🧩 **Atividades Práticas**

### 🔹 **Atividade 1 – Reconhecimento do Módulo**
1. Identifique no módulo os terminais de **alimentação (VCC e GND)**, **entrada de sinal (TRIG)** e **saída do relé (NO, COM, NC)**.  
2. Ligue o módulo à fonte de 12 V e observe o **display**.  
3. Teste os botões **S1, S2 e S3** e verifique suas funções conforme o manual.

---

### 🔹 **Atividade 2 – Modo P-1 (Temporizador Simples)**
1. Pressione **S1 por 2 segundos** para entrar no menu e selecione **P-1**.  
2. Escolha a variação **A1**, **A2** ou **A3**.  
3. Ajuste um tempo de **5 segundos**.  
4. Aplique o sinal de disparo (toque breve no botão TRIG).  
5. Observe o comportamento do relé — ele deve ligar e desligar conforme o tempo configurado.  
6. Registre o comportamento em cada variação A1, A2 e A3.

---

### 🔹 **Atividade 3 – Modo P-2 (Duplo Tempo ON/OFF)**
1. Selecione **P-2**.  
2. Configure o tempo de ligado (X = 3 s) e desligado (Y = 2 s).  
3. Aplique o sinal de disparo.  
4. Observe o ciclo de funcionamento: **liga → espera → desliga**.  
5. Teste com diferentes tempos e registre as observações.

---

### 🔹 **Atividade 4 – Modo P-3 (Ciclo Contínuo)**
1. Selecione **P-3** e escolha **A1**.  
2. Configure X = 2 s (ligado) e Y = 2 s (desligado).  
3. Observe o ciclo repetitivo (pisca-pisca contínuo).  
4. Alterne para **A2** e analise a diferença no comportamento.  
5. Discuta possíveis aplicações desse modo (ex: sinalização, intermitência de bomba ou motor).

---

### 🔹 **Atividade 5 – Modo P-4 (Atraso de Ligação)**
1. Selecione **P-4**.  
2. Configure o tempo para **5 segundos**.  
3. Desligue e ligue a fonte.  
4. Observe que o relé só é acionado **após** o tempo configurado.  
5. Discuta aplicações práticas (ex: partida retardada de equipamentos).

---

## 📊 **Atividade Complementar**
Monte um pequeno circuito de **automação de iluminação**, comumente denominado **Mituteria Eletrônica**  onde a lâmpada acende automaticamente por alguns segundos após o pressionar de um botão pulsador (modo P-1).

---

## 🧩 **Questões para Reflexão**
1. Qual a principal diferença entre os modos P-2 e P-3?  
2. Por que o módulo utiliza isolamento óptico no sinal de disparo?  
3. Como a memória permanente influencia na confiabilidade do sistema?  
4. Em quais situações o modo P-4 seria mais indicado?

---

## 🧾 **Conclusão**
Ao final da aula, o aluno deverá ser capaz de:
- Identificar e configurar corretamente cada modo de funcionamento.  
- Aplicar o temporizador em cenários de automação real.  
- Entender o uso de parâmetros de tempo e suas aplicações práticas.


