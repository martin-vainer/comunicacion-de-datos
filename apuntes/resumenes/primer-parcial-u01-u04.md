# Comunicación de Datos — Primer parcial · U1–U4

Cuadros y fórmulas para repasar antes de rendir. No reemplaza los apuntes ni los ejercicios.

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
