# Comunicación de Datos — Resumen rápido U1–U8

**Primer parcial:** U1–U4 · **Segundo parcial:** U5–U8. Cuadros para recordar diferencias y fórmulas para repasar unidades y supuestos. No reemplaza los apuntes ni los ejercicios.

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

[Apunte U1](../teoria/01-introduccion-comunicaciones/APUNTE.md)

## U2 · Señales de telecomunicaciones

- **Analógica/digital:** valores continuos / símbolos discretos. Amplificar aumenta también el ruido presente; regenerar decide y reconstruye el símbolo.
- **Fourier:** una periódica se representa con continua (media firmada), fundamental y armónicos. Media cero no implica RMS cero. **Banda base:** sin trasladar a una portadora.
- **Ancho de banda:** señal = extensión espectral según criterio; canal = intervalo que deja pasar con una tolerancia. Filtros: pasa bajos, pasa altos, pasa banda y rechazo de banda.

| Código / rasgo | Qué recordar |
|---|---|
| Unipolar / polar | Una polaridad y cero / dos polaridades. |
| NRZ / RZ | Sin retorno interior obligatorio / vuelve a cero dentro del bit. |
| AMI | Unos alternan signo; ceros al nivel cero. Rachas de ceros dificultan recuperar reloj. |
| HDB3 | Sustituye cuatro ceros con un patrón que introduce una violación controlada de AMI. |
| Manchester | Transición central por bit: da reloj y balance de continua. |

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| **Frecuencia:** $f=1/T$ | $f$ [Hz]; $T$ período [s], señal periódica. | 2 ms → 500 Hz. |
| **Eficaz:** $V_{\mathrm{rms}}=A/\sqrt 2$ | $V_{\mathrm{rms}}$ valor eficaz y $A$ pico [V], sinusoide sin continua. | 300 V de pico → 212,1 V eficaces. |
| **Banda:** $B=f_{\mathrm{sup}}-f_{\mathrm{inf}}$ | $B$ ancho; $f_{\mathrm{sup}},f_{\mathrm{inf}}$ límites [Hz], mismo criterio. | 300–3400 Hz → 3100 Hz. |
| **Primer cero:** $B_0=1/\tau$ | $B_0$ [Hz] desde continua; $\tau$ duración [s] del pulso rectangular ideal. | 0,5 ms → 2 kHz; el espectro no termina allí. |
| **Longitud de onda:** $\lambda=v/f$ | $\lambda$ [m]; $v$ propagación [m/s]; $f$ frecuencia [Hz] en ese medio. | En aire, $v\approx 3\cdot10^8$ m/s; 100 MHz → 3 m. |

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
| **Rendimiento:** $\eta=b_u/b_t$ | $\eta$ fracción útil; $b_u,b_t$ bits útiles y tiempos totales de bit por carácter; sin pausas. | 1 arranque + 7 datos + 1 parada → 7/9 ≈ 77,8 %. |
| **Malla completa:** $N_e=n(n-1)/2$ | $N_e$ enlaces; $n$ nodos; un enlace por par. | 4 nodos → 6 enlaces. |
| **Tráfico:** $A=\lambda T_R$ | $A$ [Erlang], ocupación media; $\lambda$ [llamadas/h], $T_R$ retención media [h/llamada]. | 60 llamadas/h, 3 min/llamada → 3 Erlangs. |

[Apunte U3](../teoria/03-redes-telecomunicaciones/APUNTE.md)

## U4 · Modulación, digitalización y multiplexación

- **Modular** adapta una señal al medio: AM/FM/PM varían amplitud/frecuencia/fase; ASK/FSK/PSK eligen estados discretos de esos parámetros; QAM combina amplitud y fase. Más estados permiten más bits/símbolo, pero exigen distinguir estados más próximos a igual potencia y geometría comparable.
- **Por pulsos:** PAM cambia altura; PWM/PDM, duración; PPM, posición. PCM/MIC: elegir instantes → redondear amplitudes → asignar bits. Delta codifica subida/bajada; ADM adapta el paso; DPCM codifica el error de predicción.

| Multiplexación | Cómo separa señales |
|---|---|
| FDM | Bandas de frecuencia distintas; guardas entre canales. |
| OFDM | Subportadoras ortogonales de espectros superpuestos; exige sincronismo. |
| TDM síncrono | Turnos fijos, aun con entradas inactivas. |
| STDM | Turnos según demanda; requiere identificación y puede generar colas. |
| WDM | Longitudes de onda distintas en una misma fibra. |
| CDM | Códigos de correlación controlada, en el mismo tiempo y banda. |

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| AM: $B_{\rm DBL}=2B_m$; $B_{\rm BLU}=B_m$ | $B_m$: banda del mensaje; $B_{\rm DBL}$, $B_{\rm BLU}$: bandas ocupadas [Hz], sin márgenes. | 3 kHz → 6 kHz y 3 kHz. |
| FM (Carson): $B_{\rm FM}\approx 2(\Delta f+f_a)$ | $B_{\rm FM}$ banda significativa, $\Delta f$ desviación máxima y $f_a$ frecuencia del tono [Hz]. Aproximación, no borde exacto. | 10 kHz de desviación y tono de 2 kHz → 24 kHz. |
| Muestreo: $f_s\ge 2f_{\max}$ | $f_s$: tasa [muestras/s]; $f_{\max}$: máxima frecuencia de entrada [Hz], señal limitada en banda. Límite ideal; en práctica, margen y filtro antialias. | 3,4 kHz → 6,8 kmuestras/s como límite. |
| PCM: $V_{\rm PCM}=f_sb$ | $V_{\rm PCM}$: tasa binaria [bit/s]; $f_s$: muestras/s; $b$: bits/muestra; sin entramado. | 8000 muestras/s × 8 bit/muestra = 64 kbit/s. |
| TDM: $V_{\rm línea}=N_b f_{\rm trama}$ | $V_{\rm línea}$: tasa de línea [bit/s]; $N_b$: tamaño fijo [bit/trama]; $f_{\rm trama}$: tramas/s. | E1: 256 × 8000 = 2,048 Mbit/s; T1: 193 × 8000 = 1,544 Mbit/s. |

- **Jerarquías, no técnicas de multiplexación:** PDH agrega tributarios casi síncronos; SDH/SONET organizan tramas síncronas con acceso más directo a tributarios. E1/PCM30: 30 canales de voz; T1/PCM24: 24.

**Gray:** estados vecinos difieren en un bit; limita el daño al confundir vecinos, no corrige errores.

[Apunte U4](../teoria/04-modulacion-digitalizacion-multiplexacion/APUNTE.md)

## U5 · Teoría de la información y codificación

- **Información:** lo improbable informa más. Entropía = incertidumbre media por símbolo, no significado; máxima si todos los resultados son equiprobables. **Memoria nula:** el historial no cambia las probabilidades; no implica equiprobabilidad.
- **Fuente:** compacta la representación, con o sin pérdida; Huffman es prefijo sin pérdida y une primero las menores probabilidades. **Canal:** agrega redundancia para detectar/corregir; bloque trata grupos de entrada, convolucional usa también estado previo.

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| Información: $I_i=-\log_2 p_i$ | $I_i$: información del resultado [Shannon]; $p_i$: probabilidad positiva del resultado $i$ [sin unidad]. | Probabilidad ¼ → 2 Shannon. |
| Entropía: $H=-\sum_i p_i\log_2p_i$ | $H$ [bit informativo/símbolo]; $p_i$: probabilidades de los símbolos; se omiten términos nulos. | Dos símbolos equiprobables → 1 bit/símbolo. |
| Tasa: $\Gamma=Hr_s$ | $\Gamma$ [bit informativo/s]; $r_s$: ritmo de la fuente [símbolos/s]. Fuente sin memoria. | 1 bit/símbolo × 100 símbolos/s = 100 bit/s informativos. |
| Eficiencia: $\eta_{\rm inf}=H/\overline L$ | $\eta_{\rm inf}$: relación sin unidad; $\overline L$: longitud media [bit/símbolo]; código de fuente binario sin pérdida. | $H=1$ y longitud media 2 → 50 %. |
| Redundancia: $R_{\rm abs}=n-k$ | $R_{\rm abs}$ [bit/palabra]; $k$: bits de entrada/bloque; $n$: bits/palabra; código binario de bloque fijo. | Repetición triple: 3 − 1 = 2 bit/palabra. |

- **Representaciones:** ITA N.º 2: 5 bit y cambio letras/cifras; BCD 8421: 4 bit por dígito decimal; ASCII básico: 7 bit por posición; EBCDIC: 8 bit por posición, identificar la página.
- **Propiedades:** no singular = palabras distintas para símbolos distintos; unívoco = el flujo tiene una sola decodificación; prefijo = ninguna palabra inicia otra.
- **No confundas:** tasa informativa (demanda), tasa binaria transmitida y capacidad del canal (límite, U6).

[Apunte U5](../teoria/05-teoria-informacion-codificacion/APUNTE.md)

## U6 · Canales de comunicaciones

**Capacidad** es el techo de tasa confiable, no la velocidad usada. **Atenuación** reduce nivel; **distorsión** altera forma; **ruido** agrega perturbaciones (térmico, diafonía, impulsivo, intermodulación). La **ISI** mezcla símbolos vecinos; la ecualización compensa la respuesta del canal, no elimina todo ruido.

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| **Nyquist–Hartley:** $C=2B\log_2 n$ | $C$ capacidad [bit/s], $B$ banda [Hz], $n$ niveles distinguibles (potencia de 2); canal paso bajo ideal sin ruido ni ISI. | 3000 Hz y 4 niveles → 12 kbit/s. |
| **Shannon–Hartley:** $C=B\log_2(1+S/N)$ | $S,N$ potencias medias de señal y ruido [W]; canal limitado en banda con ruido blanco gaussiano aditivo. Usá $S/N$ en veces, no en dB (0 dB equivale a 1 vez). | 3000 Hz, $S/N=1$ → 3 kbit/s. |
| **Ganancia y nivel:** $G=10\log_{10}(P_{\rm sal}/P_{\rm ent})$; $L=10\log_{10}(P/1\,\mathrm{mW})$ | $G$ [dB], $L$ [dBm]; potencias positivas y misma unidad en cada cociente. Para tensión, $20\log_{10}$ del cociente si las impedancias resistivas son iguales; dBmV usa 1 mV de referencia. | Duplicar potencia → +3,01 dB; 100 mW → 20 dBm. |
| **Factor de ruido:** $F_r=(S/N)_{\rm ent}/(S/N)_{\rm sal}$ | Cocientes lineales medidos en la misma banda; $F_r$ adimensional. | De 100 a 50 → $F_r=2$. |
| **Distancia mínima:** $e_d=d_{\min}-1$; $e_c=\lfloor(d_{\min}-1)/2\rfloor$ | $d_{\min}$ menor número de posiciones distintas entre palabras válidas; $e_d,e_c$ bits erróneos garantizados en modos separados de detección/corrección. | Distancia 7 → detecta 6 o corrige 3. |

- **Paridad:** detecta un número impar de inversiones; puede omitir uno par. **CRC:** residuo de división polinómica módulo 2; residuo nulo no garantiza ausencia de error.
- **ARQ:** detecta y pide retransmisión; Stop & Wait espera confirmación, ventana permite varias tramas pendientes. **FEC:** agrega redundancia para corregir en destino sin pedir repetición. **BER:** fracción de bits recibidos erróneos.

[Apunte U6](../teoria/06-canales-comunicaciones/APUNTE.md) · [Decibeles y balance](../teoria/06-canales-comunicaciones/APUNTE.md#decibeles)

## U7 · Medios de comunicaciones

| Medio | Qué recordar |
|---|---|
| **Par trenzado / multipar** | El trenzado y la recepción diferencial reducen interferencia; NEXT es diafonía medida en el extremo cercano. Categoría, blindaje y terminación A/B son criterios distintos. |
| **Coaxil / guía de onda** | El blindaje del coaxil confina el campo; la guía conduce microondas. Adaptar impedancias reduce reflexiones. |
| **Fibra óptica** | Núcleo de índice mayor que el revestimiento; guía por reflexión total interna bajo la condición angular adecuada. La atenuación resta potencia; la dispersión ensancha pulsos. |
| **Radio / microondas** | La antena acopla el circuito al espacio. La onda directa exige despeje; el retorno ionosférico depende de la frecuencia y las condiciones de propagación. |
| **Satélite** | Uplink: tierra → satélite. Downlink: satélite → tierra. El transpondedor retransmite; GEO suele dar mayor cobertura por satélite y retardo que LEO. |

- **Fibra multimodo:** varios caminos; el perfil gradual reduce dispersión modal respecto del escalón. **Monomodo:** evita la dispersión entre modos, no toda dispersión. LED/láser emiten; fotodiodo recibe. Un modo no significa un único canal WDM.

| Fórmula | Variables y condición | Ejemplo |
|---|---|---|
| **Antena de cuarto de onda:** $L=c/(4f)$ | $L$ longitud ideal [m], $f$ frecuencia [Hz], $c$ propagación en aire, aprox. $3\times10^8$ m/s. | 150 MHz → 0,50 m. |
| **Balance:** $P_{\rm Rx}=P_{\rm Tx}+\sum G-\sum L_p$; $M=P_{\rm Rx}-S_{\rm Rx}$ | $P_{\rm Tx},P_{\rm Rx}$ niveles y $S_{\rm Rx}$ sensibilidad [dBm]; $G$ ganancias, $L_p$ pérdidas, $M$ margen [dB]; referencias compatibles. | 20 dBm + 10 dB − 80 dB → −50 dBm; umbral −60 dBm → 10 dB de margen. |

[Apunte U7](../teoria/07-medios-comunicaciones/apuntes-comunicacion-de-datos-u7.md)

## U8 · Hardware de comunicaciones

| Interfaz o señal | Qué recordar |
|---|---|
| **ETD/DTE ↔ ETCD/DCE** | Terminal que origina/consume datos ↔ equipo que lo adapta al medio. Interfaz: conector **mecánico**, niveles **eléctricos**, señales **funcionales**. |
| **RS-232 / V.24** | Serie; para datos, 1 negativo y 0 positivo. V.24 define circuitos; V.28, características eléctricas asimétricas. El conector solo no identifica una interfaz. |
| **TD/RD · RTS/CTS · DTR/DSR** | Datos transmitidos/recibidos · pedido y habilitación de emisión · terminal y módem listos. DCD detecta portadora; RI avisa llamada. |
| **Null-módem** | Une dos DTE cruzando TD con RD y conservando tierra de señal; los puentes locales no informan el estado del receptor remoto. |
| **RS-449 · X.21 · V.35** | RS-449 se asocia con RS-422/423; X.21 digital síncrona; V.35 síncrona con señales balanceadas y desbalanceadas. No siempre alcanza recablear. |

| Módem | Idea clave |
|---|---|
| **Vocal** | Adapta al canal telefónico vocal. V.34 usa QAM/TCM; V.90: máximos nominales 56 kbit/s bajada y 33,6 kbit/s subida, no caudal útil garantizado. |
| **Banda base / xDSL** | Banda base: sin traslado a portadora vocal. xDSL aprovecha más banda del par; ADSL es asimétrico y HDSL, simétrico. |
| **Cable módem** | CATV/HFC: acceso con planta híbrida óptico-coaxial y terminación CMTS, no fibra hasta cada usuario. |

- **Funciones de cátedra:** principales, modulación y codificación; complementarias, ecualización, señalización y control de flujo; especiales, compresión, detección/corrección y diagnóstico. **Flujo** evita saturar al receptor; no corrige bits dañados.

[Apunte U8](../teoria/08-hardware-comunicaciones/APUNTE.md)
