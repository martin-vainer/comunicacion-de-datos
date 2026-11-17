# Comunicación de Datos — Primer parcial · U1–U4

Cuadros y fórmulas para repasar antes de rendir. No reemplaza los apuntes ni los ejercicios. [Fuentes y mapa de estudio](../../docs/flujo-agentico.md#mapa-estudio-parciales).

## Conversiones rápidas

| Magnitud | Equivalencia | Ejemplo de parcial |
|---|---|---|
| Frecuencia | 1 kHz = 1 000 Hz; 1 MHz = 1 000 kHz | 3,4 kHz = 3 400 Hz |
| Tiempo | 1 ms = 1 000 μs = 0,001 s | 125 μs = 0,125 ms = 0,000125 s |
| Cantidad de datos | 1 byte = 8 bits | 250 000 bytes = 2 000 000 bits |
| Tasa binaria | 1 kbit/s = 1 000 bit/s; 1 Mbit/s = 1 000 kbit/s | 1,544 Mbit/s = 1 544 kbit/s |
| Distancia | 1 km = 1 000 m | 30 000 m = 30 km |
| Velocidad de desplazamiento | 1 m/s = 3,6 km/h | 18 km/h = 5 m/s |
| Potencia | 1 W = 1 000 mW | 100 mW = 0,1 W |

**No mezcles magnitudes:** Hz cuenta ciclos por segundo; baudios, símbolos por segundo; bit/s, bits por segundo. Pasar de mW a dBm tampoco es cambiar un prefijo: dBm expresa un nivel logarítmico referido a 1 mW.

## U1 · Introducción a las comunicaciones

- **Teleinformática:** integra procesamiento y transmisión. Centralizado/distribuido indica **dónde** se procesa; lote/interactivo, **si hay diálogo**; en línea no significa necesariamente en tiempo real.
- **Circuito teleinformático:** ETD A → ECD A → medio → ECD B → ETD B. El **ETD** origina o recibe datos; el **ECD** comunica el terminal con el medio. En el esquema de cátedra, **circuito de datos** abarca los ECD y el medio; **enlace de datos**, la relación entre los ETD.
- **Internet:** red de redes autónomas. **IXP**: infraestructura para intercambiar tráfico entre redes. **IETF**: especificaciones técnicas; **IANA**: coordinación de identificadores. Un RFC no es necesariamente un estándar.
- **OSI:** protocolo = reglas entre pares; interfaz = frontera local entre capas vecinas; servicio = lo que una capa le ofrece a la superior.

| Capa OSI | Función mínima |
|---|---|
| 7. Aplicación | Ofrece servicios de red a aplicaciones. |
| 6. Presentación | Adapta representación: formatos, compresión, cifrado. |
| 5. Sesión | Gestiona el diálogo y la sincronización de sesiones. |
| 4. Transporte | Transfiere datos extremo a extremo; según protocolo, regula flujo y ofrece confiabilidad. |
| 3. Red | Encaminamiento y reenvío entre redes. |
| 2. Enlace | Tramas y control entre nodos directamente conectados. |
| 1. Física | Transmite bits como señales por el medio. |

| Electricidad básica · TP1 | Variables y condición | Ejemplo |
|---|---|---|
| **Ohm y potencia:** $V=RI$; $P=VI$ | $V$ tensión [V], $I$ corriente [A], $R$ resistencia [Ω], $P$ potencia [W]; continua y carga resistiva. | 12 V y 2 A → 6 Ω y 24 W. |

[Apunte U1](../teoria/01-introduccion-comunicaciones/APUNTE.md)

## U2 · Señales de telecomunicaciones

- **Analógica/digital:** valores continuos / símbolos discretos. Amplificar aumenta también el ruido presente; regenerar decide y reconstruye el símbolo.
- **Fourier:** una periódica se representa con continua (media firmada), fundamental y armónicos. Media cero no implica RMS cero. **Banda base:** sin trasladar a una portadora.
- **Ancho de banda:** es un intervalo de frecuencias medido en hertz. Sus extremos dependen del criterio: para una línea pueden ser los puntos de $3\ \text{dB}$ y, para el tren rectangular del TP, se toma el primer cero de la envolvente en $1/\tau$. Por eso nunca hay que dar un ancho de banda sin decir de qué objeto se habla y cómo se delimitó.
- **Filtros:** pasa bajos, pasa altos, pasa banda y rechazo de banda. Canal telefónico vocal del ejemplo: **pasa banda, aproximadamente 300–3400 Hz**, no rechazo de banda.
- **Códigos de línea:** primero mirá **qué niveles** se usan; después, **si vuelve a cero dentro del bit** (RZ) o no tiene retorno obligatorio (NRZ).

| Código | Forma y reloj | Continua |
|---|---|---|
| Unipolar NRZ | Una polaridad y cero; rachas iguales sin transiciones. | Generalmente no nula. |
| Polar NRZ | Signos opuestos para 0 y 1; rachas iguales sin transiciones. | Cero si se compensan las áreas de ambos signos. |
| AMI (bipolar NRZ) | Los 1 alternan signo; los 0 quedan a cero. Ceros largos sin reloj. | Marcas alternadas: sin continua sostenida en el modelo ideal. |
| Bipolar RZ | Como AMI, pero las marcas vuelven a cero dentro del bit. Los ceros largos siguen sin reloj. | Balance por alternancia de marcas. |
| Polar RZ | Signos opuestos para 0 y 1; retorna a cero y da referencia en cada bit. | Depende del balance de áreas, como en polar NRZ. |
| Manchester | Dos mitades opuestas por bit; transición central obligatoria. | Cero por bit con mitades simétricas. |
| HDB3 | Sustituye cuatro ceros con una violación controlada de AMI para recuperar reloj. | Mantiene el balance de marcas. |

**Al leer un gráfico:** la media del recorte puede no ser cero aunque el código balancee a largo plazo (por ejemplo, AMI con una cantidad impar de marcas). A igual tasa y con pulsos rectangulares, acortar el pulso de NRZ a RZ exige más banda bajo el criterio del primer cero.

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| **Frecuencia:** $f=1/T$ | $f$ [Hz]; $T$ período [s], señal periódica. | 2 ms → 500 Hz. |
| **Eficaz:** $V_{\mathrm{rms}}=A/\sqrt 2$ | $V_{\mathrm{rms}}$ valor eficaz y $A$ pico [V], sinusoide sin continua. | 300 V de pico → 212,1 V eficaces. |
| **Banda:** $B=f_{\mathrm{sup}}-f_{\mathrm{inf}}$ | $B$ ancho; $f_{\mathrm{sup}},f_{\mathrm{inf}}$ límites [Hz], mismo criterio. | 300–3400 Hz → 3100 Hz. |
| **Tren rectangular:** $\Delta f=1/T$, $B_0=1/\tau$, $C_0=A\tau/T$ | $T$ período y $\tau$ ancho de pulso [s]; $\Delta f$ separación y $B_0$ primer cero [Hz]; $A$ amplitud y $C_0$ continua [V], tren rectangular unipolar. | $T=10$ ms, $\tau=0,5$ ms, $A=1$ V → 100 Hz, 2 kHz y 0,05 V. |
| **Longitud de onda:** $\lambda=v/f$ | $\lambda$ [m]; $v$ propagación [m/s]; $f$ frecuencia [Hz] en ese medio. | En aire, $v\approx 3\cdot10^8$ m/s; 100 MHz → 3 m. |
| **Ganancia relativa:** $G=10\log_{10}(P_s/P_e)$; $P_s=P_e10^{G/10}$ | $G$ ganancia con signo [dB]; $P_s,P_e$ potencias positivas de salida/entrada en la misma unidad. | 1 W → 0,5 W: −3,01 dB. |
| **Nivel de potencia:** $L=10\log_{10}(P/1\,\mathrm{mW})$; $P=1\,\mathrm{mW}\,10^{L/10}$ | $L$ nivel [dBm]; $P$ potencia positiva [mW]; referencia fija de 1 mW. | 100 mW → 20 dBm; 0 dBm → 1 mW. |

**Armónicas del tren:** en el ejemplo, 2000 Hz ÷ 100 Hz = **orden 20**; ese coeficiente es cero. Antes hay **19 armónicas positivas no nulas**; no contés la continua. El espectro no termina en ese cero.

[Apunte U2](../teoria/02-senales-telecomunicaciones/APUNTE.md)

## U3 · Redes de telecomunicaciones

| Distinción | Qué recordar |
|---|---|
| Simplex / half duplex / full duplex | Un sentido / ambos alternados / ambos simultáneos. |
| Serie / paralelo | Bits sucesivos / varias posiciones simultáneas. Es otro criterio. |
| Asincrónica / sincrónica | Delimita caracteres con arranque/parada **y** sincroniza bits / mantiene referencia temporal y delimita bloques. |
| Orientado al carácter / al bit | Control mediante caracteres reservados / patrones de bits. |
| Circuitos / paquetes | Asigna recursos a una sesión / comparte recursos entre unidades; puede haber espera. |
| Topología | Estrella: nodo central; bus: medio común; anillo: circuito cerrado; malla: enlaces entre pares. |

- **Tasas:** modulación = símbolos/s (baudios); transmisión = bits totales/s; transferencia = bits útiles/s; transferencia real = bits útiles correctos/s.
- **RTPC:** lazo local conecta abonado y central; troncal conecta centrales; PBX es central privada. Conmutación espacial separa por camino, temporal por turno.

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| **Modulación:** $V_m=1/\tau$ | $V_m$ [baudios]; $\tau$ intervalo constante [s/símbolo]. | 1 ms/símbolo → 1000 baudios. |
| **Multinivel:** $V_t=V_m\log_2 n$ | $V_t$ transmisión [bit/s], $V_m$ modulación [baudios], $n$ niveles (potencia de 2); mapeo fijo sin redundancia. | 1200 baudios, 4 niveles → 2400 bit/s. |
| **Rendimiento:** $\eta=b_u/b_t$ | $\eta$ fracción útil; $b_u,b_t$ bits útiles y tiempos totales de bit por carácter; sin pausas. Contá paridad si existe. | 1 arranque + 7 datos + 2 de parada, sin paridad → 7/10 = 70 %. |
| **Tiempo de transmisión:** $t=N_{\rm tot}/V_t$ | $t$ [s], $N_{\rm tot}$ bits enviados incluidos los de control, $V_t$ tasa bruta [bit/s]. | 100 caracteres de 10 tiempos de bit a 1000 bit/s → 1 s. |
| **Malla completa:** $N_e=n(n-1)/2$ | $N_e$ enlaces; $n$ nodos; un enlace por par. | 4 nodos → 6 enlaces. |
| **Tráfico:** $A=\lambda T_R$ | $A$ [Erlang], ocupación media; $\lambda$ [llamadas/h], $T_R$ retención media [h/llamada]. | 60 llamadas/h, 3 min/llamada → 3 Erlangs. |

| Balance de potencia · TP3 | Variables y condición | Ejemplo |
|---|---|---|
| **Pérdida de cable:** $L_c=\alpha d$ | $L_c$ [dB], $\alpha$ atenuación por distancia a la frecuencia de trabajo [dB/km], $d$ longitud [km]. | 5 dB/km × 30 km = 150 dB. |
| **Nivel recibido:** $P_R=P_T+\sum G-\sum L$ | $P_R,P_T$ niveles [dBm]; $G$ ganancias y $L$ pérdidas de cada elemento en cascada [dB]. Compará con la sensibilidad y el margen requerido. | 2 mW → +3,01 dBm; con 150 dB de pérdida llegan −146,99 dBm. Para llegar a −60 dBm sin margen faltan 86,99 dB de ganancia. |

**Splitter:** calculá cada boca por separado; una boca de −3,5 dB entrega unos 0,447 W si entran 1 W. Si te piden pérdida global, sumá las **potencias** de salida antes de convertir a dB; no sumes las pérdidas de las bocas.

[Apunte U3](../teoria/03-redes-telecomunicaciones/APUNTE.md) · [TP3: balance](../practica/tp-03-redes.md#e17)

## U4 · Modulación, digitalización y multiplexación

- **Modular** adapta una señal al medio: AM/FM/PM varían amplitud/frecuencia/fase; ASK/FSK/PSK eligen estados discretos de esos parámetros; QAM combina amplitud y fase. **Moduladora** = mensaje; **portadora** = soporte; **modulada** = salida. Datos digitales no obligan a una portadora cuadrada.
- **Constelación:** contá puntos, no anillos. PSK pura tiene un solo radio; varias amplitudes y fases son compatibles con QAM. **16-PSK y 16-QAM** tienen la misma tasa bruta a iguales baudios; la 16-QAM cuadrada del curso da menos error a igual energía por bit respecto del ruido y con canal/receptor comparables.
- **Por pulsos:** PAM cambia altura; PWM/PDM, duración; PPM, posición. PCM/MIC: elegir instantes → redondear amplitudes → asignar bits. Delta codifica subida/bajada; ADM adapta el paso; DPCM codifica el error de predicción.

| Multiplexación | Cómo separa señales |
|---|---|
| FDM | Bandas de frecuencia distintas; guardas entre canales. |
| OFDM | Espectros superpuestos: en el modelo ideal, el pico de cada subportadora coincide con ceros de las otras. Exige sincronismo. |
| TDM síncrono | Turnos fijos, aun con entradas inactivas. |
| STDM | Turnos según demanda; requiere identificación y puede generar colas. |
| WDM | Longitudes de onda distintas en una misma fibra. |
| CDM | Códigos de correlación controlada, en el mismo tiempo y banda. |

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| AM: $B_{\rm DBL}=2B_m$; $B_{\rm BLU}=B_m$ | $B_m$: banda del mensaje; $B_{\rm DBL}$, $B_{\rm BLU}$: bandas ocupadas [Hz], sin márgenes. | 3 kHz → 6 kHz y 3 kHz. |
| FM (Carson): $B_{\rm FM}\approx 2(\Delta f+f_a)$ | $B_{\rm FM}$ banda significativa, $\Delta f$ desviación máxima y $f_a$ frecuencia del tono [Hz]. Aproximación, no borde exacto. | 10 kHz de desviación y tono de 2 kHz → 24 kHz. |
| PSK regular: $\Delta\theta=360^\circ/M$ | $\Delta\theta$ separación angular; $M$ cantidad de fases equiespaciadas. No se aplica a QAM. | 16-PSK → 22,5° entre vecinos. |
| Muestreo: $f_s=1/T_s$; $f_s\ge 2f_{\max}$ | $f_s$: tasa [muestras/s]; $T_s$: intervalo [s]; $f_{\max}$: máxima frecuencia de entrada [Hz]. Para señal limitada en banda, el doble es el límite ideal; en práctica, margen y filtro. | 125 μs → 8000 muestras/s; 4 kHz de tope → 8000 muestras/s como límite. |
| PCM: $b=\log_2 L$, $V_{\rm PCM}=f_sb$ | $L$: niveles (potencia de 2); $b$: bits/muestra; $f_s$: muestras/s; $V_{\rm PCM}$: tasa binaria [bit/s] sin entramado. | A 8000 muestras/s: 128 niveles → 7 bit/muestra → 56 kbit/s; 256 niveles → 8 → 64 kbit/s. |
| TDM: $V_{\rm línea}=N_b f_{\rm trama}$ | $V_{\rm línea}$: tasa de línea [bit/s]; $N_b$: bits/trama (incluido control); $f_{\rm trama}$: tramas/s. | E1: 256 × 8000 = 2,048 Mbit/s; T1: 193 × 8000 = 1,544 Mbit/s. |

- **Conteo de trama:** E1/PCM30: 32 ranuras × 8 bits = **256 bits**; 30 de voz, TS0 de alineación/control y TS16 de señalización. T1/PCM24: 24 octetos + 1 bit de trama = **193 bits**. Muestras cuantificadas en un gráfico no prueban que se estén multiplexando fuentes.
- **Jerarquías, no técnicas de multiplexación:** PDH agrega tributarios casi síncronos; SDH/SONET organizan tramas síncronas con acceso más directo a tributarios.

**Gray:** estados vecinos difieren en un bit; limita el daño al confundir vecinos, no corrige errores.

[Apunte U4](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md)
