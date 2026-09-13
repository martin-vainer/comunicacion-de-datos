# Cuestionario – Comunicación de Datos

## Pregunta 1 – Circuito Teleinformático Básico

**El circuito de datos de un Circuito Teleinformático Básico comprende:**

1. El ECD y el ETD  
2. Ninguna de las opciones son elegibles  
3. El ECD, el medio de comunicaciones y el ETD  
4. Sólo el medio de comunicaciones  
5. **El ECD y el medio de comunicaciones ✅**

### ¿Por qué?
El **circuito de datos** está formado por los **ECD (Equipos de Comunicación de Datos)** y el **medio de comunicación**.

Los **ETD (Equipos Terminales de Datos)** generan o reciben la información, pero no forman parte del circuito de datos propiamente dicho.

---

## Pregunta 2 – Modelo OSI

**¿Qué afirmación es correcta respecto del modelo OSI?**

a. Es un estándar del IEEE  
b. **La norma V.24 es de la capa 1 ✅**  
c. Ninguna de las anteriores  
d. Entre capas iguales se usan interfaces  
e. La compresión de datos es de la capa 5  

### ¿Por qué?
La norma **V.24** corresponde a características de la interfaz física entre equipos, por lo que pertenece a la:

**Capa 1 → Física**

Recordar:

- Entre **capas iguales** → se utilizan **protocolos**
- Entre **capas adyacentes** → existen **interfaces**
- Compresión y cifrado → **Capa 6 (Presentación)**
- OSI fue desarrollado por **ISO**, no IEEE.

---

## Pregunta 3 – Modelo OSI

**¿Qué afirmación es incorrecta respecto del modelo OSI?**

a. **Es un estándar del IEEE ✅**
b. Entre capas iguales se usan protocolos  
c. La norma V.24 es de la capa 1  
d. La criptografía es de la capa 6  
e. Ninguna de las anteriores  

### ¿Por qué?
El modelo OSI fue desarrollado por la **ISO (International Organization for Standardization)**, no por el IEEE.

Las demás son correctas:

- Capas iguales → protocolos
- V.24 → Capa 1
- Criptografía → Capa 6

---

## Pregunta 4 – Analizador de espectro

**Las variaciones en el tiempo de una señal de comunicaciones pueden ser apreciadas en forma directa mediante un analizador de espectro.**

- Verdadero
- **Falso ✅**

### ¿Por qué?
El **analizador de espectro** muestra la señal en función de la frecuencia:

**Amplitud vs. Frecuencia**

Para observar directamente cómo cambia con el tiempo se utiliza un **osciloscopio**:

**Amplitud vs. Tiempo**

---

## Pregunta 5 – Códigos de línea

**¿Qué código de línea ocupa más ancho de banda y es autosincronizante?**

a. Unipolar NRZ  
b. Ninguno de los anteriores  
c. Bipolar RZ  
d. Polar NRZ  
e. **Polar RZ ✅**

### ¿Por qué?
En **RZ (Return to Zero)** la señal vuelve a cero dentro de cada bit.

Esto provoca:

**Más transiciones → mejor sincronización → mayor ancho de banda**

Polar RZ garantiza transiciones dentro de cada intervalo de bit, por lo que es autosincronizante.

---

## Pregunta 6 – Código de línea y componente continua

**¿Qué código es más adecuado para un medio con etapas inductivas, sin continuidad óhmica, requiriendo mínima componente continua y menor ancho de banda?**

a. Polar RZ  
b. Ninguno de los anteriores  
c. Unipolar NRZ  
d. Bipolar RZ  
e. **HDB3 ✅**

### ¿Por qué?
Las etapas inductivas, como los **transformadores**, no permiten transmitir correctamente componente continua.

**HDB3**:

- Tiene componente continua prácticamente nula.
- Evita largas secuencias sin transiciones.
- Mantiene el sincronismo.
- Ocupa menos ancho de banda que alternativas RZ.

Por eso es adecuado para este tipo de medios.

---

## Pregunta 7 – Respuesta en frecuencia de un canal

**¿Qué filtro se adapta mejor a la respuesta en frecuencia de un canal de comunicaciones?**

1. Pasa bajo  
2. Pasa alto  
3. **Pasa banda ✅**  
4. Rechazo de banda  

### ¿Por qué?
Un canal de comunicaciones normalmente permite transmitir solamente un **rango determinado de frecuencias**:

**f_min < f < f_max**

Las frecuencias inferiores y superiores a ese rango son atenuadas.

Por eso su comportamiento se aproxima al de un **filtro pasa banda**.

---

# Recordatorios rápidos

- **ECD + medio de comunicación → circuito de datos**
- **OSI → ISO, no IEEE**
- **Misma capa → protocolo**
- **Capas adyacentes → interfaz**
- **Capa 1 → Física → V.24**
- **Capa 6 → Presentación → compresión y criptografía**
- **Osciloscopio → tiempo**
- **Analizador de espectro → frecuencia**
- **RZ → más transiciones → más sincronismo pero más ancho de banda**
- **HDB3 → baja componente continua + sincronismo + AB reducido**
- **Canal de comunicaciones → comportamiento pasa banda**