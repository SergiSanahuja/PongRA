# 🏓 AR Face & Hand Tracking Pong (Effect House)

![Effect House](https://img.shields.io/badge/Platform-Effect_House_(TikTok)-000000?style=for-the-badge&logo=tiktok&logoColor=white)
![Language](https://img.shields.io/badge/Logic-Visual_Scripting-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-In_Development-green?style=for-the-badge)

Un juego interactivo de **Pong en Realidad Aumentada (AR)** desarrollado para TikTok utilizando **Effect House**. El proyecto utiliza avanzados algoritmos de tracking facial y gestual en tiempo real para ofrecer una experiencia de juego "manos libres" e inmersiva.

---

## 🎮 ¿Cómo se juega? (Lógica de Estados)

El juego implementa una **máquina de estados secuencial** para garantizar que los jugadores están listos antes de lanzar la pelota:

1. **Fase 1: Escaneo Facial:** El filtro se activa y escanea la escena buscando un rostro humano (**Face Tracking**). Si no hay nadie frente a la cámara, el juego permanece en pausa.
2. **Fase 2: Calibración de Manos:** Una vez detectada la cara, el sistema espera a detectar **dos manos simultáneamente** (**Hand Tracking**). Cada mano controlará una pala del Pong (Izquierda y Derecha).
3. **Fase 3: ¡A jugar!:** Cuando se cumplen ambas condiciones (Cara + 2 Manos), la pelota se libera y comienza la partida. Si el jugador esconde una mano, el juego se pausa automáticamente por seguridad.

---

## 🛠️ Características Técnicas

* **Visual Scripting Avanzado:** Gestión de lógica compleja mediante nodos sin necesidad de código tradicional.
* **Multi-Hand Tracking:** Configuración del motor de Effect House para detectar y trackear de forma independiente `Hand 0` y `Hand 1`.
* **Control de Coordenadas:** Mapeo del eje vertical ($Y$) de las manos de los usuarios para mover las palas en tiempo real de forma fluida.
* **UX Dinámica:** Textos e indicaciones en pantalla que guían al usuario a través de las fases de calibración.

---

## 📂 Estructura del Proyecto

* `/Assets`: Modelos 3D, texturas 2D para las palas/pelota y fuentes tipográficas.
* `/VisualScripting`: Capturas o descripciones de los *subgraphs* principales (`GameManager`, `PaddleController`).
* `effect.ehproj`: Archivo principal del proyecto de Effect House.

---

## 🚀 Cómo probarlo en tu ordenador

1. Descarga e instala [Effect House](https://effecthouse.tiktok.com/).
2. Clona este repositorio en tu máquina local:
   ```bash
   git clone [https://github.com/](https://github.com/)[SergiSanahuja]/[PongRA].git
