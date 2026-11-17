# Comunicación de Datos — Segundo parcial · U5–U8

Cuadros y fórmulas para repasar antes de rendir. No reemplaza los apuntes ni los ejercicios.

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
