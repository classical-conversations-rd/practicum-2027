# Investigación UX de compra: Prácticum 2027 (Ciencias)

Fecha: 1 de octubre de 2026.
Alcance: mejores prácticas de experiencia de compra, información y redacción para la página del Prácticum 2027 de Classical Conversations República Dominicana (evento de un día, calculadora de boletas en US$/RD$, Stripe Checkout, códigos promocionales, becas financiadas por patrocinadores y reconocimiento a patrocinadores).

Datos fijos: fecha del Prácticum 2027 = "Fecha por confirmar" (pendiente de Claudia, CC); tema: Ciencias; sede: Iglesia de Convertidos a Cristo (ICC), Santo Domingo; precios iguales a 2026 (US$30 / RD$1,800; niños incluyen almuerzo). Contacto: José Genao Pilarte, ccrep.dom@gmail.com, (849) 201-6825 / (809) 763.7495.

## Método y límites

- Libros NN/g (serie "Ecommerce User Experience", 5.ª edición): se extrajeron los índices de guías y los "Key Findings by Report" del informe 01. Se cita "NN/g Ecom NN, guía N, p. X" (NN = número de informe; N = número de guía; p. = página del índice de la guía). Las páginas son las que imprime el propio índice del PDF.
- NN/g "How People Read Online, 2.ª ed.": se usó el listado de guías (numeración propia del informe) y los "Key Takeaways". Se cita "NN/g Lectura, guía N, p. X".
- NN/g "Writing Compelling Digital Copy" (diapositivas): el PDF está protegido con contraseña y no se pudo leer. Las ideas de ese material se cubren con el informe "How People Read Online". El taller en .docx no se revisó.
- Donna Spencer, "A Practical Guide to Information Architecture": se leyó el capítulo de rotulado (labelling) y el resumen de navegación. Se cita "Spencer, cap. 17".
- nbm.org y stpauls.co.uk: se consultaron la portada y las páginas de boletas, visita y apoyo mediante lectura web (resúmenes automáticos) y se inspeccionó el HTML de las portadas para tipografías y colores. Lo que dependía solo del resumen automático (por ejemplo "fondo blanco con gris sutil") está marcado como "por verificar en navegador". No se imitan marca, logotipos ni fotografías de ninguno de los dos sitios; se toman patrones, no activos.

---

## (a) Checklist priorizada de recomendaciones

Prioridad: P1 = imprescindible antes de abrir ventas; P2 = importante; P3 = deseable.

### Selección de boletas y claridad de precios

1. **P1. Mostrar los precios en la sección de boletas sin acción previa, en una lista plana de tipos de boleta.**
   Qué: Adulto US$30 / RD$1,800; Niño (incluye almuerzo) US$30 / RD$1,800 (confirmar el precio vigente de niño y almuerzo según las variables PRICE_NINO y PRICE_ALMUERZO); cada línea con una frase de "qué incluye".
   Por qué: los usuarios abandonan cuando no ven el precio hasta añadir al carrito. nbm.org lo resuelve con cuatro líneas ("$10 Per Adult", "$7 Youth (ages 3-17)"...) y un solo botón.
   Fuente: NN/g Ecom 07, guías 15 y 16, pp. 86 y 95; Ecom 09, guía 28, p. 102; nbm.org/visit/tickets.

2. **P1. Mostrar siempre moneda con símbolo y abreviatura: "US$30" y "RD$1,800" (nunca "$30" a secas).**
   Por qué: en República Dominicana "$" es ambiguo (el peso dominicano también usa "$"). NN/g recomienda símbolo más abreviatura.
   Fuente: NN/g Ecom 10, guía 25, p. 103; guía 28 (coherencia en toda la página y en gráficos), p. 111.

3. **P1. Presentar ambas monedas lado a lado con la moneda de cobro marcada como oficial y la otra como equivalente.**
   Qué: "US$30 (aprox. RD$1,800)" si el cobro de Stripe es en una sola moneda; si Stripe cobra en las dos, ofrecer un selector claro "Pagar en: US$ / RD$". Indicar la tasa fija usada (US$1 = RD$60) y decir que es la tasa del evento.
   Por qué: si los precios se fijan en una moneda, la otra debe presentarse como estimado; el usuario no debe descubrir una diferencia en el pago.
   Fuente: NN/g Ecom 10, guías 26 y 27, pp. 105 y 109; guía 7 (cambiar de moneda sin sacar al usuario de la página), p. 57.

4. **P1. Calculadora con una sola columna de lectura: cantidad de adultos, cantidad de niños, total en ambas monedas, desglose visible.**
   Qué: líneas "2 adultos x US$30 = US$60", "1 niño (incluye almuerzo) x US$30 = US$30", "Descuento -US$X", "Total US$Y / RD$Z". Cantidades con botones menos/más, cantidad muy visible, sin botón "Actualizar".
   Por qué: el total debe reflejarse al instante y sin sorpresas; las cantidades deben ser obvias.
   Fuente: NN/g Ecom 04, guías 20, 33 y 34, pp. 88, 139 y 143.

5. **P1. Declarar "qué incluye" y "qué no incluye" junto al precio, antes de la compra.**
   Qué: incluye: sesiones de 9:00 a. m. a 4:00 p. m., cuaderno de trabajo impreso (si aplica), café (si aplica, confirmar con patrocinador), almuerzo solo para niños (y adultos si se confirma). No incluye: transporte, parqueo (confirmar).
   Por qué: describir cada elemento del paquete y mostrar cargos adicionales cuanto antes reduce abandonos; St Paul's y nbm.org también aclaran qué cubre la entrada.
   Fuente: NN/g Ecom 03, guía 14, p. 78; Ecom 07, guía 19, p. 106; Ecom 09, guía 28, p. 102; nbm.org (aclara que ciertas áreas no requieren boleta).

6. **P1. Declarar los cargos: "Sin cargos adicionales" si es cierto; si Stripe o impuestos añaden algo, mostrarlo antes de pedir datos personales.**
   Fuente: NN/g Ecom 04, guía 103, p. 321 (total completo antes de pedir pago); Ecom 07, guía 19, p. 106; Ecom 10, guía 29, p. 113.

7. **P2. Política de reembolso y cambios en lenguaje simple, junto al botón de compra.**
   Qué: decidir y escribir una política concreta (por ejemplo: cambio de nombre permitido hasta X días antes; reembolso solo si el evento se cancela). nbm.org lo resume en tres viñetas ("no reembolsable ni intercambiable", fechas, identificación al recoger la pulsera).
   Por qué: las políticas vagas generan desconfianza; deben ser específicas y enlazarse desde el carrito/pago.
   Fuente: NN/g Ecom 04, guía 30, p. 131; Ecom 06, guías 8 y 16, pp. 61 y 88; Ecom 07, guía 25, p. 136.

8. **P2. Advertir antes de pagar los requisitos inusuales: nombre de cada asistente, edad de los niños, un correo para recibir las boletas.**
   Fuente: NN/g Ecom 04, guía 76, p. 251.

### Códigos promocionales y descuentos

9. **P1. Aplicar automáticamente los descuentos que se anuncian; el código solo para los casos que no se pueden inferir.**
   Qué: el enlace `?promo=HOMELIFE` ya aplica el descuento; mostrarlo con una etiqueta fija ("Descuento familias HomeLife Academy aplicado: -20% en boletas de adulto") y no exigir escribir nada. Conservar el campo manual para quien llega sin enlace.
   Por qué: los usuarios quieren que lo anunciado se aplique solo; hacerlos memorizar códigos baja la confianza.
   Fuente: NN/g Ecom 04, guía 22, p. 102; Ecom 01, "Help Users Save Money"; Ecom 07, guías 6 y 8, pp. 49 y 55.

10. **P1. Campo de código visible en la calculadora y en el pago, con mensajes de error útiles.**
    Qué: etiqueta "¿Tienes un código de descuento?" con campo desplegable; confirmación en texto ("Código aplicado: -US$6"); error en texto ("Ese código no es válido. Revisa mayúsculas y que no haya espacios."). Mantener códigos cortos, sin confundir O y 0.
    Fuente: NN/g Ecom 04, guías 113 y 118, pp. 338 y 350; guías 81 y 84 (errores), pp. 266 y 272; guía 104 (reflejar el descuento en el total), p. 322.

11. **P2. Mostrar el ahorro real en dinero, no solo el porcentaje, y a qué boletas aplica.**
    Qué: "Ahorras US$6 por adulto. No aplica a boletas de niño." Evitar plazos artificiales; si hay fecha límite de precio, decirla.
    Fuente: NN/g Ecom 07, guías 17 y 7, pp. 97 y 54; Ecom 04, guía 23, p. 107; guía 56 (restricciones de tiempo lo más flexibles posible), p. 201.

### Confianza

12. **P1. Bloque de confianza junto al botón de pago: pago procesado por Stripe, datos de tarjeta no se guardan en este sitio, contacto humano visible.**
    Qué: texto como "El pago se realiza en la página segura de Stripe. No guardamos tu tarjeta." Teléfono y correo del coordinador (José Genao Pilarte) a un toque en móvil, con horario de respuesta.
    Fuente: NN/g Ecom 09, guías 31 y 37 de privacidad en correo (Ecom 12, guía 37, p. 106); Ecom 06, guías 31, 33, 34 y 36, pp. 138, 144, 144 y 153; Ecom 04, guía 31, p. 134; guía 114, p. 342.

13. **P1. Sección "Quiénes organizamos" enlazada desde el pie: Classical Conversations RD, coordinador, sede, historia del Prácticum.**
    Fuente: NN/g Ecom 09, guías 11, 12 y 14, pp. 52, 52 y 65; St Paul's (pie con misión, contacto y número de registro de la entidad: copiar la práctica, incluyendo la razón social de CC RD si existe).

14. **P2. Prueba social real: testimonios con nombre y apellido de familias que asistieron al Prácticum 2026 (con permiso).**
    Por qué: reseñas y testimonios con nombre son más creíbles que citas anónimas. No inventar ninguno; si no hay permiso, omitir la sección.
    Fuente: NN/g Ecom 09, guías 20-22, pp. 84-87; Ecom 03, guía 33, p. 146.

15. **P2. Cuidar ortografía, consistencia de nombres (ICC, CC RD) y fechas desactualizadas de 2026 en toda la página.**
    Por qué: hasta los errores pequeños bajan la credibilidad. Esto incluye quitar cualquier mención residual de "25 de julio de 2026" y "Gramática" en la versión 2027.
    Fuente: NN/g Ecom 09, guías 2, 3 y 4, pp. 27, 29 y 35.

### Traspaso a Stripe, confirmación y correo

16. **P1. Paso previo al traspaso: resumen del pedido editable y botón con verbo y destino claros.**
    Qué: tarjeta "Tu pedido" (cantidades, descuento, total en US$ y RD$) con enlace "Cambiar"; botón "Continuar al pago seguro (Stripe)". Avisar que se abrirá la página de Stripe. Un solo botón principal, visualmente dominante.
    Fuente: NN/g Ecom 04, guías 48, 50, 51 y 53, pp. 184, 187, 189 y 196; guías 119 y 120, pp. 351 y 355.

17. **P1. Compra sin registro y con el mínimo de datos: nombre completo en un solo campo, correo, y nada más en nuestro lado.**
    Por qué: nunca exigir cuenta; autocompletar del navegador; una sola columna.
    Fuente: NN/g Ecom 04, guías 52, 55, 57, 58, 59, 60 y 75, pp. 192, 199, 205, 209, 213, 214 y 250; Ecom 01, "Avoid Asking for Extra Information".

18. **P1. Página de confirmación (`gracias`) inmediatamente después del pago, con todo el detalle y los siguientes pasos.**
    Qué: arriba, "Pago recibido. Te esperamos en el Prácticum 2027" (con "Fecha por confirmar" mientras no se confirme); número de pedido corto y legible; cantidades, total pagado en la moneda cobrada; qué llevar; cómo cambiar un nombre; teléfono y correo. Sin ofertas ni publicidad extraña. Un único enlace secundario a "Apoyar una beca".
    Fuente: NN/g Ecom 04, guías 121, 122, 123 y 124, pp. 358, 358, 362 y 363; Ecom 06, guía 12, p. 74.

19. **P1. Correo de confirmación inmediato desde un remitente reconocible, con asunto descriptivo y la información clave en el primer párrafo.**
    Qué: remitente "Prácticum CC República Dominicana" (no "no-reply"); asunto "Confirmación de boletas: Prácticum 2027 (Ciencias)" sin número de pedido ni emojis ni mayúsculas; primer párrafo con total, cantidades y fecha (o "fecha por confirmar"); lista corta con viñetas; contacto con teléfono. Cuando se confirme la fecha, enviar un segundo correo cuyo asunto lo diferencie ("Fecha confirmada").
    Fuente: NN/g Ecom 12, guías 1, 4, 7, 10, 12, 15, 16, 21, 28, 29, 31, 32, 39 y 42, pp. 39, 42, 46, 51, 55, 58, 60, 65, 82, 83, 90, 95, 108 y 119.

20. **P2. Aviso de cambios importantes por correo y recordatorio previo al evento (sin marketing).**
    Qué: un recordatorio con horario, dirección de ICC, mapa, qué llevar, y cómo contactar. No usar correos transaccionales para pedir encuestas ni publicidad.
    Fuente: NN/g Ecom 12, guías 34 y 39, pp. 100 y 108; Ecom 08, guía 29, p. 87 (avisar de retrasos o cambios).

### Becas, patrocinio y donaciones

21. **P1. Sección "Apoya una beca" con una pregunta de decisión: "Quiero asistir y no puedo pagar" / "Quiero patrocinar a una familia" / "Quiero patrocinar el evento como empresa o iglesia".**
    Qué: tres tarjetas de igual peso, con una frase de impacto cada una (qué cubre un aporte: por ejemplo "US$30 cubren una boleta de adulto"; usar solo cifras reales), siguiendo el esquema de nbm.org ("Support the Annual Fund / Become a Member / Corporate Support") y de St Paul's ("Ways to donate", "Become a friend").
    Fuente: nbm.org/support; stpauls.co.uk/support-us; NN/g Ecom 08, guías 1, 30 y 33, pp. 24, 88 y 94 (punto de entrada claro y página de aterrizaje para regalos).

22. **P1. Flujo de "patrocinar a una familia" como regalo: cantidad, mensaje opcional, anonimato y recibo, sin crear cuenta.**
    Qué: opciones "Patrocinar 1 boleta de adulto" / "1 familia (2 adultos + niños)" / "Otro monto"; campo opcional "De" y mensaje; casilla "Prefiero ser anónimo"; aviso explícito de cuándo y cómo se informa al donante (sin revelar datos de la familia becada). Aclarar si el aporte es deducible o no (decidir con la coordinación).
    Fuente: NN/g Ecom 08, guías 8, 11, 17, 21, 22 y 28, pp. 51, 58, 71, 74, 77 y 87; guía 15 (costo de cada opción explícito), p. 68.

23. **P1. Solicitud de beca sin fricción y con dignidad: formulario corto, lenguaje respetuoso, respuesta en plazo definido.**
    Qué: pedir solo nombre, correo, teléfono, número de adultos y niños, y una línea opcional de contexto; decir quién revisa, en cuánto tiempo responde (por ejemplo "en 5 días hábiles") y que la información es confidencial. Evitar términos como "caso social" o "necesitados"; usar "beca" y "familias que lo necesitan".
    Fuente: NN/g Ecom 04, guía 58, p. 209; Ecom 09, guías 31 y 32, pp. 121 y 124 (explicar para qué se piden los datos); Ecom 06, guía 36, p. 153 (tiempos de respuesta).

24. **P2. Rendición de cuentas de las becas: contador público "Becas entregadas: N familias" y "Becas disponibles", actualizado manualmente.**
    Por qué: mostrar los esfuerzos por causas sociales genera confianza; el contador debe ser real o no mostrarse.
    Fuente: NN/g Ecom 09, guía 13, p. 56; Ecom 07, guía 9, p. 60 (incluir causas benéficas en promociones).

25. **P2. Reconocimiento de patrocinadores en un bloque propio ("Quienes hacen posible el Prácticum"), con logotipo, nombre y qué aportó, agrupados por tipo de aporte.**
    Qué: sede (ICC), alianza (Home Life Academy), café (Café Santo Domingo - Induban), impresión de cuadernos (Imprenta Amigos del Hogar), y los de 2027 cuando se confirmen. Para UNIREMHOS no declarar aporte alguno hasta confirmarlo. No inventar niveles de patrocinio. Enlazar el nombre del patrocinador solo si lo autorizan.
    Fuente: NN/g Ecom 09, guía 15, p. 68 (enlazar fuentes reputables); nbm.org y St Paul's ("Corporate partnerships") como patrón.

### Preguntas frecuentes, visita y contacto

26. **P1. Preguntas frecuentes cortas, agrupadas por tema y visibles en la misma página (menos de 20 preguntas).**
    Qué: temas "Boletas y pagos", "El día del evento", "Niños", "Becas y patrocinio". Preguntas redactadas como las haría una madre o un padre ("¿Puedo llevar a mis hijos pequeños?", "¿Puedo pagar en pesos?", "¿Hay factura?", "¿Cuándo es la fecha?"). Pregunta visualmente distinta de la respuesta. Colocar un enlace corto a las preguntas dentro del bloque de compra.
    Fuente: NN/g Ecom 06, guías 19, 20, 22 y 24, pp. 94, 99, 108 y 118; guías 8 y 13 (enlaces contextuales), pp. 61 y 75; guía 1 (usar "Preguntas frecuentes"), p. 30.

27. **P1. Bloque "Visita": sede, mapa, cómo llegar, parqueo, horario del día, accesibilidad, qué llevar.**
    Qué: dirección de ICC con enlace a mapa; horario "9:00 a. m. a 4:00 p. m." y hora de acreditación (confirmar); parqueo; accesibilidad; qué traer. Fecha: "Fecha por confirmar" hasta que Claudia la confirme, con indicación de cuándo se publicará.
    Fuente: NN/g Ecom 04, guía 101, p. 314 (dirección, indicaciones, mapa, horario y teléfono); Ecom 11 (localizadores de tienda, para el patrón del mapa); Ecom 10, guías 20-21, p. 94-97 (fechas y horas sin ambigüedad); nbm.org (dirección, horario y metro bajo el hero); stpauls.co.uk ("last entry", estación cercana).

### Estilo de redacción

28. **P1. Escribir para escaneo: el resumen en la parte superior, titulares con la palabra clave al inicio, viñetas, negritas en palabras clave, párrafos cortos.**
    Qué: cada sección empieza con una frase-resumen (qué es, cuándo, cuánto). Titulares como "Boletas: US$30 por persona" en lugar de "Asegura tu lugar en esta gran experiencia". Patrón pirámide invertida.
    Fuente: NN/g Lectura, guías 3-9, 25-30 y 35-37, pp. 166-177 y 295-330; patrón F y "layer cake" (Key Takeaways: Destination Pages, p. 155).

29. **P1. Rotular con palabras obvias y estables; evitar etiquetas ingeniosas.**
    Qué: menú: "Boletas", "Programa", "Conferencista", "Visita", "Apoyo", "Preguntas frecuentes", "Contacto". Botones con verbo: "Comprar boletas", "Solicitar una beca", "Patrocinar una familia". Evitar "Más información" repetido; usar el texto que informa como enlace.
    Fuente: Spencer, cap. 17 ("las mejores etiquetas son aburridas y completamente obvias"); NN/g Lectura, guías 32-34, pp. 319-322; Ecom 06, guía 17, p. 89.

30. **P2. Lenguaje claro para lectores no nativos del tema: explicar "Ciencias en la educación clásica", sin modismos; si el contenido de Home Life Academy está en inglés, traducirlo o resumirlo en español.**
    Fuente: NN/g Lectura, guías 50-54, pp. 379-385; Ecom 10, guías 14-16, pp. 78-87; Ecom 03, guía 16, p. 85.

31. **P2. Tono: cálido, sobrio y concreto, con una pizca de patrimonio clásico; sin presión.**
    Qué: no usar contadores falsos ni "últimos lugares" a menos que sea cierto; sin ventanas emergentes al entrar ni al salir.
    Fuente: NN/g Ecom 07, guías 1, 2, 10 y 12, pp. 27, 34, 62 y 73; Ecom 04, guía 24, p. 112 (escasez, con cuidado); Ecom 09, guía 36, p. 132 ("evitar trucos").

---

## (b) Lo que tomamos de nbm.org y stpauls.co.uk

Nota: la estructura proviene de la lectura de las páginas; las tipografías y los colores de abajo salen del HTML publicado de las portadas. Todo lo marcado "por verificar" debe revisarse en un navegador antes de copiarse.

### Estructura de información (IA)

| Patrón | nbm.org | stpauls.co.uk | Qué tomamos para el Prácticum 2027 |
|---|---|---|---|
| Menú principal corto, en orden de tarea | Visit, Exhibitions, Explore, Programs & Events, Support, About; accesos separados "Tickets" y "Member login" | Worship and music, Visit us, What's on, Safeguarding, Shop; botón "Tickets" destacado | Seis o siete rótulos: Boletas (botón destacado), Programa, Conferencista, Visita, Apoyo, Preguntas. El botón de boletas siempre visible, también en móvil. |
| Datos prácticos justo debajo del hero | Horario ("Thursday - Monday, 10am - 5pm"), dirección y metro, en una franja bajo el título | Bloque "Welcome" con horario, última entrada, precio por adulto y niño, dirección y estación | Franja inmediatamente debajo del hero: tema, "Fecha por confirmar", horario 9:00 a. m. a 4:00 p. m., ICC con dirección, precio US$30 / RD$1,800. |
| Boletas como lista plana con una sola acción | Cuatro líneas de precio, viñetas de políticas, un botón azul "Purchase Tickets Now" | "Book sightseeing tickets" repetido en menú, en el bloque de bienvenida y en el pie; menciona descuentos y gratuidades | Lista plana de boletas, viñetas de política, un botón principal "Comprar boletas". Repetir el botón en menú, hero y pie. |
| Cuadros de apoyo con peso igual | "Support the Annual Fund", "Become a Member", "Corporate Support", "Shop Our Store" como tarjetas iguales; luego "More Ways to Give" en texto | "Ways to donate" y "Become a friend" como secciones separadas con imagen y frase de impacto | Tres tarjetas iguales: "Solicitar una beca", "Patrocinar una familia", "Patrocinar el evento". Más abajo, "Otras formas de apoyar" en texto (ofrendas en especie, voluntariado, difusión). |
| Cada sección termina en una acción | Hero, exposiciones, programas, noticias, apoyo | Hero, qué sucede, planifica tu visita, horarios, donaciones, amigos | Cada bloque cierra con un solo enlace de acción hacia el siguiente paso lógico. |
| Pie de página completo | Nombre, dirección, horario, precios, teléfonos, enlaces institucionales | Cuatro columnas más número de registro de la entidad | Pie con nombre de CC RD, coordinador, teléfonos, correo, dirección de ICC, enlaces a políticas y preguntas, y créditos de patrocinadores. |
| Tono de ayuda y bienvenida | Instrucciones directas ("Tickets include access to all exhibitions") | "We want to ensure that everyone can explore...": inclusivo antes que restrictivo | Frases de apertura y accesibilidad antes que prohibiciones. |

### Tipografía

- nbm.org (del HTML): Public Sans como tipografía de texto y las familias Haboro y Haboro Condensed (Adobe Fonts) para titulares; menú en mayúsculas con peso regular y titular del hero grande y en negrita. Qué tomar: contraste claro entre titular fuerte y texto sobrio, y etiquetas de menú breves.
- stpauls.co.uk (del HTML): Raleway desde Google Fonts; menú en sentido de frase (solo la primera letra en mayúscula) y mayúsculas solo en el logotipo. Qué tomar: menú en minúsculas con inicial mayúscula, que lee más cálido y menos institucional.
- Para el Prácticum: mantener la identidad actual (Cormorant Garamond para titulares y EB Garamond para texto) porque ya transmite herencia clásica. Añadir una sola sans-serif de apoyo (por ejemplo Public Sans, gratuita en Google Fonts) únicamente para precios, botones, etiquetas del calculador y formularios, donde la legibilidad numérica importa más que el carácter. Tamaño mínimo de texto 16 px; precios en peso 600-700 y en cifras de ancho uniforme (`font-variant-numeric: tabular-nums`).

### Color y fondo (paleta clara obligatoria)

- nbm.org (por verificar en navegador): fondo blanco, texto casi negro, azul oscuro en navegación y botón principal, acento rojo (#cd190a aparece en el HTML), fotografías a todo color sin filtros. Aprendizaje: una sola tinta oscura para estructura, un solo acento para acción, y mucho blanco.
- stpauls.co.uk (por verificar en navegador): fondo predominantemente blanco con zonas de gris muy claro para separar secciones, texto #171717 y un azul marino profundo (#141E3C aparece en el HTML), sin bloques de color saturado; el color lo aportan las fotografías. Aprendizaje: separar secciones con fondos casi blancos alternados en lugar de marcos y sombras.
- Aplicación al sitio actual (paleta clara ya definida: marino #0F2142, naranja #E8743A, crema #F6EEE3, papel #FCF9F4, tinta #26272B):
  1. Alternar fondos entre "papel" (#FCF9F4) y "crema" (#F6EEE3) de sección en sección; usar blanco solo para tarjetas de boleta y de formulario, de modo que el bloque de compra "flote" sin usar fondos oscuros.
  2. Reservar el naranja exclusivamente para la acción principal (Comprar boletas) y para el total/ahorro; no usarlo en decoración.
  3. Usar el marino para titulares, menú y el texto de precios.
  4. Una textura sutil de papel (ruido de 2 a 3 % de opacidad) o un filete fino en marino al 10 % entre secciones, en lugar de degradados fuertes.
  5. Verificar contraste mínimo 4.5:1 para texto y para el naranja sobre crema (el naranja #E8743A sobre crema no alcanza 4.5:1 para texto pequeño; usar #CE5C26 o más oscuro para texto, y el naranja claro solo en botones con texto marino o blanco grande).

### Imágenes y recorte

- St Paul's: recortes verticales de fachadas o de momentos humanos, luz cálida natural; hero horizontal a todo el ancho con el titular superpuesto. nbm.org: tarjetas horizontales uniformes en cuadrícula.
- Para el Prácticum: un hero horizontal de todo el ancho con foto real de familias en el Prácticum 2026 o de la pintura existente (hero-painting.jpg) con velo suave para el titular; tarjetas de programa y conferencista con una relación de aspecto uniforme (4:3 horizontal o 4:5 vertical, una sola en todo el sitio); fotos con personas reales y con recortes que muestren manos, libros y niños aprendiendo, no solo retratos. Describir con texto alternativo. Mostrar los logotipos de los patrocinadores en escala de grises o en color con el mismo alto.

### Presentación del precio y la boleta

- Lista plana (nbm.org): tipo de boleta, edad o condición, precio. Adaptar así: "Adulto: US$30 / RD$1,800" y "Niño (incluye almuerzo): US$30 / RD$1,800".
- Políticas en viñetas inmediatamente debajo (nbm.org).
- Botón principal único y repetido (ambos sitios).
- Mencionar gratuidades y descuentos en la misma sección (St Paul's: familia, grupos, concesiones, accesibilidad). Para el Prácticum: códigos de familias CC y HomeLife, y becas.

### Apoyo, donaciones y reconocimiento

- Tarjetas iguales con una frase de impacto cada una (nbm.org); estructura de "otras formas de apoyar" en texto (nbm.org); lenguaje de propósito antes que de transacción (St Paul's).
- Reconocimiento: St Paul's agrupa el apoyo en "Corporate partnerships" y membresías; nbm.org lo coloca en "Corporate Support". No se verificó en ninguno un muro de logotipos; para el Prácticum se recomienda un bloque propio con logotipo y aporte concreto.

---

## (c) Orden recomendado de las secciones de la página

1. **Barra superior fija**: nombre "Prácticum 2027", menú corto (Boletas, Programa, Conferencista, Visita, Apoyo, Preguntas) y botón "Comprar boletas".
2. **Hero**: tema de Ciencias, una frase-resumen, "Fecha por confirmar", sede ICC, precio "US$30 / RD$1,800", botón "Comprar boletas" y enlace secundario "Avísame cuando se confirme la fecha" (correo, si se decide recopilarlo, con opt-in explícito y sin casilla premarcada).
3. **Franja de datos prácticos**: fecha, horario, lugar, precio, quiénes pueden asistir (adultos y niños).
4. **Qué es el Prácticum y por qué Ciencias**: resumen de 3 a 4 líneas con viñetas de beneficios (qué aprenderás, para quién es).
5. **Programa**: horario del día (9:00 a. m. a 4:00 p. m.) y sesiones, marcando como "por confirmar" lo pendiente.
6. **Conferencista**: foto, nombre, origen y credenciales; "por confirmar" si no está cerrado.
7. **Boletas y calculadora**: lista plana de boletas, calculadora en US$ y RD$, código promocional, qué incluye, política de cambios, botón principal; contacto humano al lado.
8. **Becas y apoyo**: tres tarjetas (solicitar beca, patrocinar una familia, patrocinar el evento) y contador de becas (solo si es real).
9. **Quienes hacen posible el Prácticum**: sede, alianzas, café, impresión y otros patrocinadores confirmados.
10. **Visita**: ICC, dirección, mapa, parqueo, accesibilidad, qué llevar.
11. **Preguntas frecuentes**: agrupadas por tema (boletas y pagos, el día del evento, niños, becas y patrocinio).
12. **Testimonios** (solo con permiso y nombre real): puede ir antes de las boletas si son sólidos.
13. **Contacto**: José Genao Pilarte, Coordinador, Classical Conversations República Dominicana; correo y teléfonos con enlace de un toque.
14. **Pie de página**: datos de la organización, políticas, preguntas, patrocinadores, redes.

Páginas adicionales: `gracias` (confirmación después del pago), formulario o página de "Solicitar una beca", y flujo de "Patrocinar una familia".

---

## Pendientes antes de implementar

- Confirmar con Claudia (CC) fecha, hora de acreditación y tema exacto; hasta entonces, mostrar "Fecha por confirmar" en todas las páginas, correos y confirmaciones.
- Decidir la política de reembolso y cambio de nombre, y si el almuerzo incluye adultos.
- Decidir moneda de cobro en Stripe (una o dos) y cómo se presenta la equivalencia; documentar la tasa usada.
- Confirmar la contribución de UNIREMHOS y de cada patrocinador y obtener autorización para mostrar logotipos.
- Revisar en navegador los detalles visuales marcados "por verificar" de nbm.org y stpauls.co.uk antes de copiar tipografías o colores.
- Texto de "Home Life Academy": versión en español del material que estaba en inglés.
