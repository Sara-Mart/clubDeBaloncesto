

# 🏀 Actividad 2: Equipo de Baloncesto con HTML y CSS Grid

Este proyecto consiste en la creación de una página web para un equipo de baloncesto ficticio utilizando **HTML**, **CSS** y, específicamente, **CSS Grid**. La actividad incluía realizar un *mockup* previo y desarrollar la web basándose en él. Aproveché la ocasión para ampliar el diseño y convertirlo en un proyecto más completo para mi portafolio.

---

## 🎨 Diseño y planificación

Antes del desarrollo, realicé el mockup en **Figma**, organizando todo el contenido en una **única página** y creando un **menú de navegación** que permite desplazarse entre las distintas secciones mediante anclas.

* Creé un **logo original** para el equipo "Buffalos" utilizando Canva.
* Las imágenes de los jugadores también fueron generadas mediante las herramientas de IA de Canva.
* Además de las secciones requeridas (Inicio y Jugadores), añadí una nueva sección llamada **Partidos**, que no formaba parte de la actividad original, pero complementa el diseño y mejora la experiencia del usuario.

---

## 🧱 Estructura del proyecto

El diseño está dividido en tres secciones principales, cada una ocupando el **alto completo de la pantalla**.

```css
.section {
  width: 100%;
  height: 100vh;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
```

---

## 🏠 Sección Inicio

La portada muestra el logo del equipo, centrado mediante Flexbox.

```css
#contenedor {
  width: 100%;
  height: calc(100vh - 10vh); /* se descuenta la altura del nav */
  display: flex;
  justify-content: center;
  align-items: center;
}
```

---

## 🧑‍🤝‍🧑 Sección Jugadores

Para esta sección utilicé **CSS Grid** con un diseño totalmente responsivo. El mayor reto fue conseguir que las tarjetas se centraran sin necesidad de fijar un tamaño específico, lo cual resolví con `auto-fit` y `minmax()`.

```css
#team {
  margin-top: 20px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, auto));
  /* Esta configuración permite centrar las tarjetas sin fijar un ancho */
  column-gap: 50px;
  row-gap: 50px;
  justify-content: center;
  align-items: center;
}
```

---

## 🏆 Sección Partidos

También utiliza **CSS Grid**, pero en este caso fijé un tamaño concreto para cada tarjeta, lo que facilitó el centrado del contenido.

```css
#partidos {
  margin-top: 20px;
  display: grid;
  grid-template-columns: repeat(3, auto);
  column-gap: 50px;
  row-gap: 50px;
  justify-content: center;
}

.partido {
  width: 250px;
  background-color: #ffffff8c;
  padding: 10px;
  border-radius: 5%;
  text-align: center;
}
```

---

## 📌 Conclusiones

Esta actividad me permitió practicar:

* Diseño con **Figma**
* Generación de elementos visuales personalizados
* Maquetación con **HTML y CSS**
* Uso avanzado de **CSS Grid** y **Flexbox**
* Estructuración de una página de estilo *one-page*

--- Ver web: https://sara-mart.github.io/clubDeBaloncesto/
