# GUIA DE ORIENTAÇÃO & FONTE DE CONHECIMENTO — NOTEBOOKLM
## Disciplina: Saneamento Ambiental II (TH510) — Tratamento de Águas Residuárias (P2)
## Foco de Escopo: Do Nível Preliminar até Reatores Anaeróbios de Fluxo Ascendente (UASB / RAFA)

---

> ### 📌 DIRETRIZES GERAIS PARA O NOTEBOOKLM / ASSISTENTE DE IA
> 1. **Objetivo Central:** Atuar como um tutor acadêmico rigoroso e focado na resolução de questões conceituais, comparativas, diagnósticos operacionais e exercícios numéricos de dimensionamento para a prova P2.
> 2. **Perfil de Cobrança da Professora:**
>    - A prova **não cobra decoreba nem mera transcrição de normas**.
>    - Cobra **raciocínio aplicado, justificativa técnica de parâmetros adotados, coerência das unidades e diagnóstico de problemas de engenharia**.
>    - Toda escolha de parâmetro (ex: TAS, TDH, profundidade, velocidade) deve vir acompanhada da sua respectiva justificativa física, biológica ou hidráulica.
> 3. **Corte Temático Rígido da P2:**
>    - **ENTRA NA P2:** Visão Geral de Níveis de Tratamento, Caracterização Qualitativa/Quantitativa, Diluição/Mistura em Corpos Receptores, Tratamento Preliminar (Grades, Parshall, Desarenador), Tratamento Primário (Decantador Primário), Lagoas de Estabilização (Anaeróbias, Facultativas, Maturação) e Reatores UASB/RAFA.
>    - **NÃO ENTRA NA P2:** Lodos Ativados, Tanques Sépticos / Filtros Anaeróbios descentralizados da NBR 7229/13969, Wetlands Construídos, Gerenciamento de Lodo e Reúso da Água.

---

# MÓDULO 1: INTRODUÇÃO, NÍVEIS DE TRATAMENTO & CARACTERIZAÇÃO DO ESGOTO

### 1.1 Níveis de Tratamento de Esgoto Sanitário
* **Tratamento Preliminar:**
  * *Objetivo:* Remoção de sólidos grosseiros flutuantes/em suspensão grosseira e areia/inertes abrasivos.
  * *Unidades:* Grades de barras e desarenadores (caixas de areia).
  * *Eficiência em DBO:* Praticamente nula ($0\%$). Função é estritamente proteção mecânica de bombas, tubulações e unidades a jusante.
* **Tratamento Primário:**
  * *Objetivo:* Remoção de sólidos em suspensão sedimentáveis e matéria orgânica particulada decantável.
  * *Unidades:* Decantadores primários convencionais.
  * *Eficiências típicas:* Remoção de SST entre $50\%\text{ a }70\%$; Remoção de DBO entre $25\%\text{ a }35\%$.
* **Tratamento Secundário:**
  * *Objetivo:* Remoção de matéria orgânica dissolvida e coloidal não decantável por processos biológicos (anaeróbios ou aeróbios).
  * *Unidades do escopo da prova:* Lagoas de Estabilização e Reatores UASB (RAFA).
  * *Eficiências típicas:* Remoção de DBO entre $65\%\text{ a }85\%$ (UASB) e até $80\%\text{ a }90\%$ (Sistemas de Lagoas).
* **Tratamento Terciário / Avançado:** Remoção de nutrientes (N e P) e patógenos (desinfecção por UV, cloração ou lagoas de maturação).

---

### 1.2 Parâmetros Qualitativos do Esgoto Sanitário
* **DBO₅,₂₀ (Demanda Bioquímica de Oxigênio):** Quantidade de oxigênio consumida por microrganismos aeróbios para estabilizar a matéria orgânica biodegradável a $20^\circ\text{C}$ durante 5 dias. Esgoto doméstico típico: $250 \text{ a } 400\text{ mg/L}$.
* **DQO (Demanda Química de Oxigênio):** Quantidade de oxigênio necessária para oxidar quimicamente toda a matéria orgânica (biodegradável + inerte) via dicromato de potássio. Esgoto doméstico típico: $450 \text{ a } 800\text{ mg/L}$.
* **Relação DQO / DBO:**
  * Se $\text{DQO} / \text{DBO} < 2{,}5$: Esgoto predominantemente doméstico, altamente biodegradável, ideal para tratamento biológico.
  * Se $\text{DQO} / \text{DBO} > 3{,}0 \text{ a } 4{,}0$: Presença marcante de efluentes industriais com fração recalcitrante ou compostos tóxicos.
* **SST (Sólidos Suspensos Totais):** Composto por Sólidos Suspensos Voláteis (SSV - fração orgânica) e Sólidos Suspensos Fixos (SSF - fração mineral/inerte). Esgoto típico: $200 \text{ a } 350\text{ mg/L}$.
* **Contribuição Per Capita Padrão no Brasil:**
  * Cota de água ($q$): $150 \text{ a } 250\text{ L/(hab}\cdot\text{d)}$ (adotar $200\text{ L/(hab}\cdot\text{d)}$ se não especificado).
  * Carga de DBO per capita: $54\text{ g DBO/(hab}\cdot\text{d)} = 0{,}054\text{ kg DBO/(hab}\cdot\text{d)}$.
  * Carga de SST per capita: $60\text{ g SST/(hab}\cdot\text{d)} = 0{,}060\text{ kg SST/(hab}\cdot\text{d)}$.

---

### 1.3 Fórmulas Fundamentais de Quantificação e Mistura no Rio

1. **Crescimento Populacional Geométrico:**
   $$P_f = P_i \cdot (1 + r)^n$$
   * $P_f$: População futura projetada [hab].
   * $P_i$: População inicial [hab]; $r$: taxa anual decimal; $n$: alcance do projeto [anos].

2. **Vazão Média de Esgoto:**
   $$\bar{Q} = \frac{P \cdot q \cdot R}{86.400} + Q_{\text{inf}}$$
   * $R$: Coeficiente de retorno esgoto/água ($R = 0{,}80$).
   * $86.400$: Conversão de dias para segundos ($24 \times 3.600$).
   * $Q_{\text{inf}}$: Vazão de infiltração na rede [L/s].

3. **Vazões Extremas:**
   * $Q_{\text{máx,d}} = k_1 \cdot \bar{Q}$ (dia de maior consumo, $k_1 = 1{,}20$).
   * $Q_{\text{máx,h}} = k_1 \cdot k_2 \cdot \bar{Q} + Q_{\text{inf}}$ (hora de maior consumo, $k_2 = 1{,}50$). Fator de ponta global $K = k_1 \cdot k_2 = 1{,}80$.
   * $Q_{\text{mín}} = k_3 \cdot \bar{Q}$ ($k_3 = 0{,}50$).

4. **Carga Poluidora ($W$) e Concentração ($C$):**
   $$W = \frac{Q \cdot C}{1.000} \quad [\text{kg/d}] \qquad \text{com } Q \text{ em } [\text{m}^3/\text{d}] \text{ e } C \text{ em } [\text{mg/L ou g/m}^3]$$

5. **População Equivalente (PE):**
   $$PE = \frac{W_{\text{industrial}}}{0{,}054\text{ kg DBO/(hab}\cdot\text{d)}}$$

6. **Balanço de Massa na Zona de Mistura Fluvial:**
   $$C_0 = C_m = \frac{Q_r \cdot C_r + Q_e \cdot C_e}{Q_r + Q_e}$$
   * $Q_r, C_r$: Vazão e concentração a montante no corpo d'água receptor.
   * $Q_e, C_e$: Vazão e concentração do efluente da ETE.

7. **Cinética de Desoxigenação / Decaimento de DBO (Streeter-Phelps simplificado):**
   $$C(t) = C_0 \cdot e^{-k_1 \cdot t} \qquad t = \frac{x}{U}$$
   * $k_1$: Coeficiente de desoxigenação [d⁻¹]; $k_{1,T} = k_{1,20} \cdot 1{,}047^{(T - 20)}$.
   * $x$: Distância fluvial a jusante [km]; $U$: velocidade média do rio [km/d].

---

# MÓDULO 2: TRATAMENTO PRELIMINAR (PARSHALL & DESARENADOR)

### 2.1 Calha Parshall (Medição & Controle Hidráulico)
* **Função:** Medir com precisão a vazão afluente em regime crítico/livre e servir como controle de nível a montante para manter a velocidade no desarenador constante.
* **Equação de Vazão:**
   $$Q = K \cdot H_p^n \quad \iff \quad H_p = \left(\frac{Q}{K}\right)^{1/n}$$
   * $H_p$: Carga hidráulica medida a 2/3 da entrada convergente [m].
   * $K, n$: Coeficientes tabelados em função da largura da garganta ($W$). Ex: Garganta $W = 6'' \implies K = 0{,}381, n = 1{,}58$.
* **Cálculo do Degrau a Jusante ($z$):**
   $$z = \frac{Q_{\text{máx},f} \cdot H_{p,\text{mín}} - Q_{\text{mín},i} \cdot H_{p,\text{máx}}}{Q_{\text{máx},f} - Q_{\text{mín},i}}$$
   * *Justificativa de engenharia:* O degrau no fundo evita que o nível de água do canal a jusante afogue a garganta da Parshall na vazão máxima, garantindo escoamento livre com ressalto hidráulico.

---

### 2.2 Desarenador de Fluxo Horizontal (Caixa de Areia Retangular)
* **Objetivo:** Remover partículas minerais discretas (areia, pedriscos, cascalho com diâmetro $\ge 0{,}20\text{ mm}$ e densidade $\approx 2{,}65\text{ g/cm}^3$) para evitar abrasão em rotores de bombas e assoreamento de tubulações e digestores.
* **Regra de Ouro da Velocidade Horizontal ($v_h$):**
   $$v_h \approx 0{,}30\text{ m/s} \quad (\text{faixa aceitável: } 0{,}25 \text{ a } 0{,}40\text{ m/s})$$
   * *Por que exatamente $0{,}30\text{ m/s}$?* Se $v_h < 0{,}25\text{ m/s}$, a matéria orgânica putrescível decanta junto com a areia, gerando mau cheiro e contaminando o material removido. Se $v_h > 0{,}40\text{ m/s}$, as partículas de areia sofrem arraste/ressuspensão e não sedimentam.
* **Velocidade de Sedimentação Crítica da Areia ($v_{s,c}$):** Adota-se $v_{s,c} \approx 0{,}020 \text{ a } 0{,}025\text{ m/s}$ ($2{,}0 \text{ a } 2{,}5\text{ cm/s}$) para grãos de $0{,}20\text{ mm}$.
* **Roteiro de Dimensionamento:**
   1. Área molhada transversal: $A_{\text{transv}} = B \cdot H = \frac{Q_{\text{máx}}}{v_h}$
   2. Fixar lâmina útil $H$ ($0{,}30 \text{ a } 0{,}60\text{ m}$) e determinar a largura $B = \frac{A_{\text{transv}}}{H}$.
   3. Comprimento teórico: $L_{\text{teórico}} = \frac{H \cdot v_h}{v_{s,c}}$.
   4. Comprimento de projeto: $L_{\text{proj}} = 1{,}50 \cdot L_{\text{teórico}}$ (adiciona-se $50\%$ para absorver turbulências de entrada e saída).
   5. Taxa de Aplicação Superficial: $\text{TAS} = \frac{Q_{\text{máx}}}{B \cdot L} \le 1.000 \text{ a } 1.300\text{ m}^3/(\text{m}^2\cdot\text{d})$.
   6. Volume do poço de areia: Prever remoção periódica baseada em taxa de $30 \text{ a } 40\text{ L de areia / } 1.000\text{ m}^3\text{ de esgoto}$.

---

# MÓDULO 3: TRATAMENTO PRIMÁRIO (DECANTADORES CONVENCIONAIS)

### 3.1 Mecanismo de Funcionamento
* Sedimentação de sólidos em suspensão do Tipo II (floculenta).
* O esgoto entra em baixa velocidade, escoa radialmente (circulares) ou longitudinalmente (retangulares) e os sólidos decantam para a tremonha de lodo de fundo.

### 3.2 Critérios Normativos NBR 12209/2011 & Dimensionamento
1. **Taxa de Aplicação Superficial (TAS):**
   * Para vazão média $\bar{Q}$: $\text{TAS} = 30 \text{ a } 40\text{ m}^3/(\text{m}^2\cdot\text{d})$.
   * Para vazão máxima horária $Q_{\text{máx}}$: $\text{TAS}_{\text{máx}} \le 60\text{ m}^3/(\text{m}^2\cdot\text{d})$.
   * *Área superficial requerida:* $A_{\text{sup}} = \frac{Q}{\text{TAS}}$.
2. **Tempo de Detenção Hidráulica ($\theta_H$ ou TDH):**
   * $\theta_H = \frac{V}{Q} = 1{,}5 \text{ a } 2{,}5\text{ horas}$ na vazão de projeto.
3. **Profundidade Útil ($H$):**
   * Geralmente entre $2{,}5 \text{ a } 4{,}0\text{ m}$ (média típica: $3{,}0\text{ m}$).
4. **Taxa de Escoamento sobre o Vertedor ($q_L$):**
   * $q_L = \frac{Q}{L_{\text{vert}}} \le 250\text{ m}^3/(\text{m}\cdot\text{d})$ (em $Q_{\text{máx}}$).
   * Para decantador circular de parede simples: $L_{\text{vert}} = \pi \cdot D$.
   * *Justificativa de engenharia:* Evita velocidades ascendentes pontuais elevadas junto à borda que possam ressuspender os flocos decantados.

---

# MÓDULO 4: LAGOAS DE ESTABILIZAÇÃO

### 4.1 Tipos de Lagoas e Suas Funções
* **Lagoa Anaeróbia (LA):**
  * *Profundidade elevada ($H = 3{,}5 \text{ a } 5{,}0\text{ m}$):* Minimiza a área exposta ao ar, retém o calor biológico e previne a dissolução de oxigênio superficial, mantendo ambiente rigorosamente anóxico.
  * *Carga Orgânica Volumétrica ($\lambda_v$):* $\lambda_v = \frac{W_{\text{in}}}{V_{\text{LA}}} = 100 \text{ a } 300\text{ g DBO}/(\text{m}^3\cdot\text{d})$.
  * *TDH:* Curto, de $3 \text{ a } 6\text{ dias}$. Remoção de DBO: $50\%\text{ a }65\%$.
  * *Acúmulo de lodo:* $V_{\text{lodo}} = n_{\text{anos}} \cdot K \cdot \text{Pop}$ (taxa $K \approx 0{,}03 \text{ a } 0{,}04\text{ m}^3/\text{hab}\cdot\text{ano}$).
* **Lagoa Facultativa (LF):**
  * *Simbiose Algas-Bactérias:*
    * Na camada superior iluminada, as microalgas realizam **fotossíntese**, liberando oxigênio dissolvido ($O_2$) e consumindo $CO_2$.
    * As bactérias aeróbias e facultativas utilizam esse $O_2$ para oxidar a matéria orgânica, liberando $CO_2$, água e nutrientes para as algas.
    * No fundo anóxico, bactérias anaeróbias digerem o lodo acumulado.
  * *Profundidade rasa ($H = 1{,}5 \text{ a } 2{,}0\text{ m}$):* Garante penetração de luz solar na zona fótica.
  * *Critério de Mara para Carga Superficial Máxima ($\lambda_{s,\text{máx}}$):*
    $$\lambda_{s,\text{máx}} = 350 \cdot (1{,}085)^{(T - 20)} \quad [\text{kg DBO}/(\text{ha}\cdot\text{d})]$$
    * $T$: Temperatura média do ar no mês mais frio [$^\circ\text{C}$].
    * *Área superficial:* $A_{\text{sup}} = \frac{W_{\text{in,LF}}}{\lambda_{s,\text{proj}}}$ (onde $1\text{ ha} = 10.000\text{ m}^2$).
    * *Atenção ao afluente:* Se houver Lagoa Anaeróbia a montante com $60\%$ de remoção, a carga que entra na facultativa é apenas $40\%$ da carga bruta ($W_{\text{in,LF}} = 0{,}40 \cdot W_{\text{bruta}}$).
* **Lagoas de Maturação:**
  * *Objetivo principal:* Remoção de patógenos (coliformes termotolerantes, vírus, cistos de protozoários e ovos de helmintos).
  * *Condições:* Pouca profundidade ($H = 0{,}8 \text{ a } 1{,}2\text{ m}$), alta penetração de radiação UV do sol, pH elevado pela fotossíntese ($> 8{,}5 \text{ a } 9{,}0$), altas concentrações de $O_2$ e escassez de alimento provocam a lise e decaimento das bactérias entéricas.
  * *Modelo de Dispersão Não Ideal (Wehner-Wilhelm):*
    $$N_e = N_i \cdot \frac{4 \cdot a \cdot e^{1 / (2 \cdot d)}}{(1 + a)^2 \cdot e^{a / (2 \cdot d)} - (1 - a)^2 \cdot e^{-a / (2 \cdot d)}} \qquad a = \sqrt{1 + 4 \cdot k_{b,T} \cdot T_d \cdot d}$$

---

# MÓDULO 5: REATORES ANAERÓBIOS DE FLUXO ASCENDENTE (UASB / RAFA)

### 5.1 Princípio de Funcionamento & Estrutura
* O esgoto bruto entra pelo fundo do reator e ascende através de um manto denso de lodo anaeróbio granulado ou floculento.
* As bactérias fermentativas e metanogênicas degradam a matéria orgânica, produzindo biogás ($CH_4$ e $CO_2$).
* **Separador Trifásico (GLS - Gás / Líquido / Sólido):**
  * Localizado na parte superior do reator.
  * *Defletores de gás:* Capturam as bolhas de biogás e impedem que elas subam para o compartimento de decantação. Sem o defletor, a turbulência do gás impediria a sedimentação do lodo.
  * *Zona de decantação:* Permite que os flocos de lodo que sobem se separem da água clarificada e escorreguem de volta para o compartimento de digestão pelas frestas inclinadas ($\ge 45^\circ \text{ a } 60^\circ$).
  * *Câmaras de biogás:* Conduzem o metano para queima ou aproveitamento energético.

### 5.2 Roteiro Completo de Dimensionamento de UASB (NBR 12209)

1. **Volume Útil do Reator ($\text{Vol}_{\text{UASB}}$):**
   * Fixa-se o Tempo de Detenção Hidráulica ($\theta_H$): $\theta_H = 6 \text{ a } 10\text{ h}$ (média típica de $8{,}0\text{ h}$ para esgoto doméstico brasileiro com $T \ge 20^\circ\text{C}$).
   $$\text{Vol}_{\text{UASB}} = \bar{Q} \cdot \theta_H$$
   * *Verificação de Carga Orgânica Volumétrica (COV):*
     $$\text{COV} = \frac{W_{\text{DQO}}}{\text{Vol}_{\text{UASB}}} \le 2{,}5 \text{ a } 5{,}0\text{ kg DQO}/(\text{m}^3\cdot\text{d})$$

2. **Altura Útil ($H$) e Área Superficial ($A$):**
   * Altura líquida típica: $H = 4{,}0 \text{ a } 5{,}0\text{ m}$ (adotar $4{,}5\text{ m}$).
   $$A_{\text{reator}} = \frac{\text{Vol}_{\text{UASB}}}{H}$$

3. **Velocidade Ascensional ($v_{\text{asc}}$) — CRITÉRIO CRÍTICO DE PROVA:**
   $$v_{\text{asc}} = \frac{Q}{A_{\text{reator}}}$$
   * Na vazão média ($\bar{Q}$): $v_{\text{asc}} \le 0{,}60 \text{ a } 0{,}80\text{ m/h}$.
   * No pico horário ($Q_{\text{máx}}$): $v_{\text{asc,máx}} \le 1{,}0 \text{ a } 1{,}20\text{ m/h}$.
   * *Justificativa de engenharia:* Se a velocidade ascensional no pico for maior que $1{,}2\text{ m/h}$, as forças hidrodinâmicas de arraste superam a velocidade de sedimentação do lodo anaeróbio, lavando a biomassa para fora do reator (colapso operacional).

4. **Malha de Distribuição de Fundo (Tubos Injetores):**
   * Adota-se 1 tubo para cada $2{,}0 \text{ a } 3{,}0\text{ m}^2$ de fundo de reator.
   $$n_{\text{tubos}} = \frac{A_{\text{reator}}}{A_{\text{tubo}}}$$
   * *Justificativa de engenharia:* Distribuição homogênea que evita curtos-circuitos hidráulicos e canalizações preferenciais de esgoto cru pelo manto de lodo.

5. **Decantador Superior e Frestas de Passagem:**
   * Taxa de aplicação superficial no topo do decantador: $\text{TAS}_{\text{dec}} = \frac{Q_{\text{máx}}}{A_{\text{dec}}} \le 1{,}0 \text{ a } 1{,}2\text{ m/h}$.
   * Velocidade de passagem nas aberturas inferiores (frestas): $v_p = \frac{Q_{\text{máx}}}{A_{\text{frestas}}} \le 2{,}0 \text{ a } 2{,}5\text{ m/h}$.
   * Inclinação das paredes do decantador: Mínimo $45^\circ \text{ a } 50^\circ$ (preferível $60^\circ$) para permitir que o lodo retorne por gravidade sem raspadores mecânicos.

6. **Estimativa de Produção de Biogás / Metano:**
   $$M = Y_{\text{CH}_4} \cdot \Delta W_{\text{DQO}} \approx 0{,}35 \cdot (W_{\text{DQO,rem}} - W_{\text{lodo}})$$
   * $0{,}35\text{ m}^3\text{ CH}_4/\text{kg DQO}$ removida nas CNTP ($0{,}38$ a $20^\circ\text{C}$).
   * Composição típica do biogás: $65\%\text{ a }75\% \text{ CH}_4$, $25\%\text{ a }35\% \text{ CO}_2$, traços de $H_2S$ (responsável pelo odor de ovo podre e corrosão ácida).

---

# GUIA RÁPIDO DE DIAGNÓSTICO OPERACIONAL (QUESTÕES DISCURSIVAS)

1. **Problema: Mau cheiro característico ($H_2S$) e corrosão em unidades de concreto.**
   * *Causa:* Redução anaeróbia de sulfatos a sulfetos em condições anóxicas com baixo potencial redox; pH ácido favorece liberação do gás $H_2S$.
   * *Solução:* Confinamento com lajes/coberturas estanques, lavadores biológicos ou químicos de gases, adição de álcalis para manter pH $\ge 7{,}0$ e evitar turbulência em vertedores.
2. **Problema: Perda excessiva de biomassa / lodo saindo no efluente do UASB.**
   * *Causas prováveis:* Pico de vazão ultrapassando $v_{\text{asc}} > 1{,}2\text{ m/h}$; entupimento do coletor de biogás fazendo bolhas subirem pelo decantador; ou choque orgânico/acidificação do manto de lodo (queda da relação alcalinidade a bicarbonato / ácidos voláteis).
3. **Problema: Presença de areia no lodo de fundo do UASB ou do Decantador Primário.**
   * *Causa:* Desarenador subdimensionado, canal com velocidade horizontal $v_h > 0{,}40\text{ m/s}$ ou falta de limpeza do poço de areia preliminar.
4. **Problema: Matéria orgânica decantando e apodrecendo no canal do Desarenador.**
   * *Causa:* Velocidade horizontal $v_h < 0{,}25\text{ m/s}$ decorrente de Parshall mal calibrada ou degrau $z$ inadequado provocando remanso.

---

### Dicionário Rápido de Unidades e Fatores de Conversão Críticos
* $1\text{ L/s} = 3{,}6\text{ m}^3/\text{h} = 86{,}4\text{ m}^3/\text{d}$
* $1\text{ m}^3/\text{s} = 86.400\text{ m}^3/\text{d}$
* $1\text{ ha} = 10.000\text{ m}^2$
* $\text{mg/L} \equiv \text{g/m}^3$
* $\text{Carga (kg/d)} = \frac{Q(\text{m}^3/\text{d}) \cdot C(\text{mg/L})}{1.000}$
* $\text{Concentração (mg/L)} = \frac{W(\text{kg/d}) \cdot 1.000}{Q(\text{m}^3/\text{d})}$
* $1\text{ m}^3 \text{ CH}_4 \approx 35{,}8\text{ MJ} \approx 9{,}9\text{ kWh}$ de energia teórica.
