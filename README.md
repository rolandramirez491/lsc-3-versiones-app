# LSC 3 versiones · App Android

App para **aprender y practicar 50 señas de la Lengua de Señas Colombiana (LSC)** y ver cómo las reconocen
**3 versiones** de un reconocedor con inteligencia artificial. Cada versión contiene a la anterior y le agrega algo.

### 🎬 Video de demostración

[![Video de demostración en YouTube](https://img.youtube.com/vi/jHBP7YpeHqU/hqdefault.jpg)](https://youtu.be/jHBP7YpeHqU)

**Ver en YouTube:** https://youtu.be/jHBP7YpeHqU

---

## Descargar e instalar

1. Descarga **`LSC-3-versiones.apk`** desde **[Releases](../../releases/latest)**.
2. Ábrelo en el celular Android y acepta *"instalar apps de origen desconocido"*.
3. Listo: todo funciona **sin internet**, dentro del celular.

## Qué hace

- **Selecciona versión:** V1, V2 o V3, cada una con lo que usa y su acierto.
- **Las 50 señas:** una a una, con un muñeco y el video real de la seña.
- **INTENTAR SEÑA:** abre la cámara. Abre la boca, haz la seña y baja las manos.
  La app dice si acertaste, en qué puesto quedó tu seña en cada versión (V1, V2, V3) y las 4 señas más parecidas.
  Si tocas una, el muñeco te muestra cómo se hace.

## Las 3 versiones

| | Qué usa | Red neuronal | Acierto con personas nuevas |
|---|---|---|---|
| **V1** | las manos (21 puntos de cada mano) | GRU (recurrente) | **66,5 %** |
| **V2** | + muñecas, codos y hombros como referencia | GRU (recurrente) | **72,5 %** |
| **V3** | + lugar de la seña, forma de los 5 dedos, dibujo de la palma y del codo | 5 redes que votan: GRU + 2 MLP + 2 CNN | **82,8 %** |

Medido con el dataset **LSC50** (50 señas, 5 personas), probando siempre con una persona que el modelo nunca vio
(1000 pruebas). Los puntos del cuerpo los saca **MediaPipe** y las redes corren en el celular con **ONNX Runtime**.
