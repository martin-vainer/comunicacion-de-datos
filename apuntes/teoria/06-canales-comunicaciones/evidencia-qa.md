# Evidencia QA del candidato U6 — 2026-10-11

Estado: autocontrol de autor, **no** revisión independiente. No hubo builds, instalaciones, commits ni modificación de originales/caches. Fuentes y páginas efectivamente observadas se registran en [APUNTE, revisión](APUNTE.md#revision).

## Inspección visual

- U6: PNG inmutables del anexo, pp.2–38, observados en diez hojas de contacto (4 páginas por hoja y último de una). Portada p1 no usada técnicamente. Fórmulas/tablas p4/6/14, paridad p24–26, CRC p27–28, checksum p29 y Hamming p35–38 se cotejaron contra texto. Imágenes selectivas enlazadas en contexto: p7/14/17/18/25/28/38; las demás permanecen en anexo sin copia rutinaria.
- U2: PDF pp.3–11 renderizado con Poppler y visto; avisos Symbol/ArialUnicode no impidieron leer figuras/cifras inspeccionadas. Tabla F6TSVM y esquema de balance comprobados.
- TP6: PDF primera parte p2 y segunda parte pp2–3, observados a 1700 píxeles; mensajes CRC y enlace Hamming verificados visualmente.
- Castro/Fusario2013 PDF199–200 / impresas173–174: ecuación3-40 respalda relación de ganancia; figura y ciertas otras ecuaciones presentan erratas anotadas.
- Gráfico TP6-I E2 dibujado como figura científica con PIL desde despeje de Shannon (Matplotlib no disponible; no se instaló); representa requisito de S/N a capacidad fija, no S/N medido de un receptor. Inspección visual individual del PNG registrada tras su generación.

## Recálculos ejecutados

Python bundled, `tmp/autor-u06/verificar.py`: cálculos en doble precisión, división polinomial XOR, paridad por filas/columnas y enumeración Hamming. No es un build del repo.

| Control | Resultado reproducido | Estado |
|---|---|---|
| TP6-I E1 C [bit/s] | 29901.67877650798 | OK |
| TP6-I E2 B=3000: SNR [dB] | 9.580556381355587 | OK |
| TP6-I E2 B=10000: SNR [dB] | 0.0 | OK |
| TP6-I E2 B=1000: SNR [dB] | 30.0987563371216 | OK |
| TP6-I E4 potencia final/inicial | 102.0 | OK |
| TP6-I E4 SNR final [dB] | 40.08600171761918 | OK |
| TP6-I E5 caída [%] | 14.805569683900767 | OK |
| TP6-I E5 SNR final [dB] | 16.989700043360187 | OK |
| TP6-I E6 C [bit/s] | 67987.86368299345 | OK |
| TP6-II E4 BER | 0.0001 | OK |
| 43 dB→veces potencia | 19952.62314968879 | OK |
| 42,9 dBmV→mV | 139.63683610559377 | OK |
| 2,3 dBmV→mV | 1.3031667784522993 | OK |
| Balance registrado recibido [dBm] | 13.6 | OK |
| Balance registrado sensibilidad límite [dBm] | 10.6 | OK |
| Ruido térmico T300/B3000 [W] | 1.242e-17 | OK |
| Stop and Wait U [%] | 4.761904761904762 | OK |
| Ventana3 U [%] | 14.285714285714286 | OK |
| CRC mensaje 110101 | R=1101; T=1101011101; receptor=0 | OK |
| CRC mensaje 10110101101 | R=0110; T=101101011010110; receptor=0 | OK |
| Paridad p25 | 8 filas y 6 columnas pares | OK |
| Hamming (7,4) | 16 palabras; dmin3; 112 inversiones simples corregidas | OK |

## Enlaces y estructura

- 112 enlaces locales en APUNTE, INDICE, TP6 y repaso comprobados; errores presentes: 0.
- Referencias a candidato U5 aún en escritura: 2 (archivo futuro, si no está al ejecutar este control; el coordinador debe revalidarlas al integrar).
- Delimitadores de matemática en bloque equilibrados; anclas explícitas únicas se comprueban abajo.
- El canon conserva `unidad/estado/fuentes/actualizado`, sin `tema`; cierre Resumen mental y checklist; no hay nuevo simulacro de U6.

## Integridad de fuentes usadas

47 originales comparados con baseline, **0 discrepancias**. Se incluye toda la evidencia gráfica U6 (38 PNG), aunque p1 no se usa para un concepto. SHA-256 completo permite comprobar que las figuras enlazadas son las mismas; las imágenes siguen dentro de capturas.

| Original | SHA-256 |
|---|---|
| `capturas/teoria/06-Canales de comunicaciones/08_10_2026.md` | `2a608b45e43f13e877330cd82a27575d3ef92dd030ce8e896340ea4cdb0800cc` |
| `capturas/teoria/02-senales-telecomunicaciones/apuntes-clase 2.md` | `b9c779ffd83a9b0d4724ceb07aad43ab9ec9b767acc8bc474b94c21d9283bded` |
| `capturas/practica/clase 04.md` | `8da26fe9323dbba1ff9cf7c517a5b4fadb123add85ce467636b8dfba44748f4d` |
| `capturas/practica/Clase 05.md` | `0d32ad51d2f1fa735fd9b05ac9cac63e380776a17d798e675a037449746bb964` |
| `material/teoria/U6/U 6 Canales de Comunicaciones y control de errores.pdf` | `3e4dc09b027b9d9c43df662a29cba26e3f605133a24e1973e4ffaffcaf30c233` |
| `material/teoria/U2/U 2 Características de las señales de telecom.pdf` | `2df3d853f92b76da06a4a3e01bf3d701ad5e7ed2a4537d56d64c9ae5554037f2` |
| `material/practica/U6/TP  6 (1ra parte)    2026.pdf` | `73e17af44a6f697a79a10765e4cbd16abad0d0acfb52fcbe1d4c6c272e5d2cc5` |
| `material/practica/U6/TP   6   (2da parte)  2026.pdf` | `48f1530df7beb9745ad9bce1bc36a2a7d3e80b5186ff12fc51b5e02e584b233c` |
| `material/teoria/DOC-20230425-WA0040.pdf` | `56f7b6926abb5bea6e15e3c926d2344ad49004e4fbad6ad2e10e4060182e90ae` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-01.png` | `00e2c7bb9f1cf8dc64bf1df4250813256ef231538675e19e249815ce6ed62011` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-02.png` | `ec7ee973a711ad58fb231cd016882be3af1b36b9847cf40be910f1e5f63e0311` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-03.png` | `2a027bd735f2b193ae81e9594fa21310c4040d0b8dfa726dc3a341bae12ca94e` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-04.png` | `60feb2201d161fd10be207c78fcbbdc8d2e7cd51354f2b6c45878ffa53fd30b9` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-05.png` | `d6c5085d3456f9b6fa9681b2f1446e2ea533e948ecf273e8c0c60b6113be9d0e` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-06.png` | `13690e24ddd7854c2a6c4d1eeb2787e4fd0e241d0ec22fa1f7d604d654edee09` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-07.png` | `e0ee70faa5793354fc7ab71d4ed2be7493ea180365942ef35e2b232e2673483f` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-08.png` | `13db7588bab309e80412501fc606906ba8657c37c9fd9451567d3240c51b9b70` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-09.png` | `a31d00685819378d46bd6cfe68fee16b6f39d56cdf0f3e8c9dd59b5116af242b` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-10.png` | `dac9b93b83783e013fbca5ef98d945b239dcea6bc8fae78e6de4da77ca08f38e` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-11.png` | `17c1e88a4be2d4bb76b6e26514c40bb2f4eed85edc6e1355c6f3ae02989f67db` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-12.png` | `79a860fab09f4b69fa87f4bed37e02f9fda9185b7a9dfaf040a3a40cbf25117c` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-13.png` | `49b4b4c6d477d49f8c1c9f8cacd592c785b5195b9b0bebdf63b25ba3576a5cb4` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-14.png` | `2c2199a3dacb00b19ff1ad22c7ec9f689670e3ad44369f8df62acb38527a57dd` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-15.png` | `fb89e0e45eba6b604b7a8b229fbcab6801ab279a71d85d00071ef251cbb97e59` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-16.png` | `50b86194135602784c6a56cde524e3f2e4faf5811eeea5e3a319f0ca4ade2506` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-17.png` | `058e2e648e5a3c5b97f75b360a01c88ee45ac6b142db0bd922f11b41a7869bec` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-18.png` | `b763d808aeae7e7d609b8853822a90e7f329a970a2270be4b6af8fddee969185` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-19.png` | `6fe366ea6740e11bc631a96a0ed3716efc72caae4b9f193959170cd79d716ee7` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-20.png` | `4a3a9408aba6196b664649c39c2607fc5741ab4cef7f7858b5688513d8b869ca` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-21.png` | `986c7017c3eb7104164c52f6c5d4aa1723b3fbea28d0ea3a4c02a75b49b1bc4e` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-22.png` | `06968db3a561ab885bafdfd58f103e8639871fdff4055531e4a35b22d4a89c29` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-23.png` | `ad2c5bd3b546ea54d8dd81d6d2c8ee1972e29eb65a7f9ddf251da9db0f2129f0` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-24.png` | `8da277391d31c827772c9910632398e6c266d9cd799c644b02b216fe46a89dad` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-25.png` | `a42eaa33d32f37238f3782d2192c750750192dc03c49c25d81c369e6265b7e0e` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-26.png` | `adec874637755c8d2c19766f50b84b1db9eb24890ee887bd872a3cbb97070aa2` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-27.png` | `b8a65717788c734655df4583d0369c4288eb8d54106597b711cb0214a2302151` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-28.png` | `17d6faac09cb5f04140c7702d06944bf71b0883b3a6901fbf454eff3c5d38753` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-29.png` | `9e91cdfafde94a02d28e790a2e5e083bb297788a12163f26f6f322bee4304651` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-30.png` | `e233497329235a04b641bddd6488c465bb7e0a1afc768b344c739d3724e5e0ab` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-31.png` | `b3b5f7b8f9c9ce6304c9c44bedb2c9ed217659f8f9eabbb9ce37502854c0bcbb` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-32.png` | `ed46dd1320e0d71a5cc0fc692594f6af4570993b7db15ddd2af397c909266148` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-33.png` | `7384548f7a8377adca13bf1fe5af5ff9b59662ecf5cc5df89022a4a80d40646b` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-34.png` | `6fd9c19eeb345ce045a9a37804b76852d2bfa5ac31e2b4d5d6e277cf722932a6` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-35.png` | `dc82b510be1f628b2f58bad30ead3c513cd952a84dcde933873b014dab23f70c` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-36.png` | `4d62446cfb710357895df33f1b42e59d691ef03da8b3a11dab51ef5ecb371894` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-37.png` | `d6690340eb223ea935ec1a9f16a1f1630b1a40ab844b5bd20eb8929dd0a39b7f` |
| `capturas/teoria/06-Canales de comunicaciones/recursos-08-10-2026/pagina-38.png` | `e26b19083369da7b03f1ad5c2e14600e1079716df196e10d72682294db56e3f2` |

## Limitaciones de aceptación

Las cuentas y enlaces no certifican toda la pedagogía ni sustituyen el doble review y control transversal acordados. Eco/efecto pelicular fuera del alcance registrado, consignas ambiguas visibles, soluciones TP6 sin clave oficial. No promocionar estado a revisado antes de la puerta integral.
