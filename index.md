Sobre los contagios de COVID-19 en Monterrey
===================

### Contenido
- COVID-19
  * Síntomas
  * ¿Cómo se contagia el coronavirus?
- Panorama de Monterrey
- Temperatura
- Contaminación del aire
- Factor social

El brote de COVID-19 ha tenido un gran impacto en nuestra vida diaria, cambiando nuestro mundo y llevándonos al camino de la adaptación en distintos ámbitos como el comercio, nuestra interacción con las personas, etcétera. La principal medida de prevención es el distanciamiento social, una atinada decisión de las autoridades frente a tan difícil reto, pero ¿Qué otros aspectos influyen en el número de contagios? ¿Se puede relacionar el brote de COVID-19 con la contaminación ambiental? ¿Qué tanto impacto tienen las particulas PM 2.5 y la temperatura? Exploraremos estas cuestiones para la ciudad de Monterrey, realizando un análisis con ayuda de Python a partir de los datos de contagios, contaminación, climatología y movilidad.

## COVID-19

El COVID-19 es una enfermedad infecciosa causada por el coronavirus que se ha descubierto en diciembre de 2019 en Wuhan (China). Los coronavirus son una familia de virus que puede causar enfermedades en animales y humanos así como infecciones respiratorias que pueden ir desde el resfriado hasta enfermedades más graves. Actualmente el Covid-19 es una pandemia que afecta a muchos países.

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/gh-pages/Images/Coronavirus.gif)

*Representación animada del SARS-CoV-2*

### Síntomas

Los síntomas más comunes son la fiebre, la tos seca y el cansancio. Mientras que otros menos frecuentes dolores de cabeza y de garganta, congestión nasal, la conjuntivitis, el dolor de garganta, la diarrea, la pérdida del gusto o el olfato y las erupciones cutáneas o cambios de color en los dedos de las manos o los pies. No todas las personas tienen los mismos sintomas y algunos suelen ser leves; además, se tiene un gran índice de personas asintomáticas. 

Según la Organización Mundial de la Salud (OMS), alrededor del 80% de las personas se recuperan sin la necesidad de acudir a un hospital. Además, alrededor de 1 de cada 5 personas que contraen COVID‑19 acaba presentando un cuadro grave y experimenta dificultades para respirar. Las personas que son más vulnerables, o bien, que pueden tener más probabilidades de presentar cuadros graves son los adultos mayores y/o las personas que padecen de hipertensión arterial, problemas cardíacos, pulmonares, diabetes o cáncer.

### ¿Cómo se contagia el coronavirus?

El virus se propaga de persona a persona y por tocar superficies infectadas. Cuando una persona contagiada estornuda, tose o habla, puede transmitir el coronavirus. Existen diferentes medios por los que pasa esto: los **droplet**, partículas grandes que suelen caer en el piso a unos metros de la persona que los expulsó; los **aerosoles**, partículas de tamaño menor que quedan suspendidas en el aire; y los **fomite**, que son los objetos infectados con estas partículas. Estos últimos dependen del tiempo de vida del SARS-CoV-2 en la superficie de dicho objeto, puedes consultar estos tiempos [aquí](https://www.webmd.com/lung/how-long-covid-19-lives-on-surfaces) o [aquí](https://www.nejm.org/doi/full/10.1056/NEJMc2004973).

![](https://www.mdpi.com/viruses/viruses-07-00511/article_deploy/html/images/viruses-07-00511-g001-1024.png)

*Imagen obtenida de <https://www.mdpi.com/1999-4915/7/2/511/htm>*

Es por esto que se propuso el distanciamiento social y las medidas de higiene, para no entrar en contacto con estos patógenos. Además, se corre un mayor riesgo en reuniones en lugares cerrados o con mala ventilación, debido a que los aerosoles se mantienen en el aire por horas. 


## Panorama de Monterrey

Monterrey es una ciudad y capital del estado de Nuevo León. Esta ubicada al norte de México junto a la Sierra Madre Oriental ocupando una superficie total de Nuevo León de 64, 081.94 km^2. Con una Latitud: 25.6714, Longitud: -100.309 25° 40′ 17″ Norte, 100° 18′ 32″ Oeste. Tiene un clima seco muy cambiante, y cuenta con 1.136 millones de habitantes. Además es una ciudad industrializada, atrae a inversionistas y sus principales actividades son el comercio, la construcción, la manufactura.

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/gh-pages/Images/117645984_681250895804238_3205561972497632758_n.png)
*República Mexicana localizando a Monterrey, Nuevo León*

Son bien sabidas las medidas de prevención planteadas en México:
> Quédate en casa, mantén la sana distancia y 
> aplica medidas higiénicas

Nuevo León no fue la excepción a ello, [aquí](https://www.nl.gob.mx/publicaciones/cuales-son-las-medidas-de-prevencion-por-covid-19) encontrarás algunas recomendaciones publicadas por el gobierno. Hacia finales de marzo, se suspendieron las clases presenciales y las actividades no esenciales. Sin embargo, esto quizás fue apresurado.

![Gráfica 1](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Figura_Casos_Monterrey.png)

*Gráfica 1. Obtenida con datos de <https://coronavirus.gob.mx/>*

El alcalde de Monterrey anunció que las actividades económicas se reanudarían el 14 de mayo del presente año \[7]. Podemos observar en la gráfica anterior que a mediados de mayo se disparó el número de casos en este municipio, pudiendo deberse a esta decisión. Por supuesto, existen muchos factores que influyen en el comportamiento de los contagios, y a continuación se analizará algunos de ellos.


## Temperatura

A los 25 °C se muestra un decremento en la reproducción de casos \[11]. Verificamos la climatología en Monterrey, realizando una gráfica que se muestra a continuación.

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Figura_Climatologia_Mty.png)

*Gráfica obtenida con datos de <https://es.climate-data.org>*

Podemos observar que en Monterrey se tienen veranos largos, comúnmente con temperaturas mayores a 25 °C. Sin embargo, recordando la gráfica 1, los casos han aumentado considerablemente a mediados de mayo; esto indica que hay otros factores más importantes. Es posible que los casos de COVID-19 hubieran aumentado aún más de no ser por las temperaturas altas que se suelen presentar.

## Contaminación del aire

Hay fuerte evidencia de que la contaminación del aire representa un importante riesgo para la salud, [aquí](https://vizhub.healthdata.org/gbd-compare/) se pueden ver algunos datos de manera interactiva, al seleccionar `risk air pollution`. Los contaminantes que consideraremos aquí son el ozono O3 y el material particulado PM 2.5.

Se sabe que la exposición a contaminantes como NO2, SO2 y PM 2.5 cotribuye a enfermedades cardiovasculares, reduce la función pulmonar y causa enfermedades respiratorias \[3]. "Cuando el tracto respiratorio es expuesto al ozono se produce daño en el mismo, el alcance dependerá de la concentración de ozono, la duración de la exposición, los patrones de exposición y la ventilación. \[...] Estos efectos aumentan la susceptibilidad a las infecciones respiratorias. El ozono reduce la función pulmonar y hace más difícil la respiración profunda y vigorosa" \[10]. En concreto, el ozono y PM 2.5 llegan hasta la zona alveolar de los pulmones, lo que provoca una gran susceptabilidad a patógenos.

Además, Abraham Ortínez de la Coordinación General de Contaminación y Salud Ambiental INECC México, indica que "la exposición a partículas finas (PM2.5), ozono y otros componentes del aire contaminado provocan procesos de estrés oxidante e inflamación de las vías respiratorias y los pulmones ocasionando efectos adversos a la salud de las personas en el corto y largo plazo y alteran de manera importante la respuesta del sistema inmunológico" \[12]

Conticini et al \[4] concluyó que las concentraciones de contaminantes son un potencial contribuidor a la tasa de mortalidad por COVID-19 presente en la región de estudio, al norte de Italia.

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/pollutants_raw.png)

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/daily_mean_pollutants.png)

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/daily_max_pollutants.png)

*Gráficos obtenidos con datos de <http://aire.nl.gob.mx/>*

Tomando en cuenta estos niveles de contaminantes en Monterrey, veamos lo que significan estos niveles tan altos de acuerdo con Cole M et al (2020) \[3] para el caso de Países Bajos:

>  Usando datos secundarios y administrativos encontramos evidencia convincente de una relación positiva entre la contaminación del aire, en particular las concentraciones de PM 2.5, y los casos de COVID-19, hospitalizacioes y defunciones. Esta relación persiste después de controlar una amplia gama de variables explicativas. Nuestros resultados indican que un aumento de 1 μ/m3 en las concentraciones de PM 2.5 se asocia con 9.4 casos más de COVID-19, 3.0 hospitalizaciones más y 2.3 fallecidos más.


## Factor social

### Movilidad

![Gráfica con datos de Apple](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Figura_Mobility_Apple.png)

*Gráfica obtenida con datos de <https://www.apple.com/covid19/mobility>. Puedes verla animada [aquí](https://github.com/k488-bit/Challenge_CdeCMx/blob/master/Images/Animation_apple.gif)*

*\* Revisar sección "Sobre estos datos".*

La gráfica indica que, si bien al principio de la contingencia se redujo en gran medida la movilidad, en fechas más recientes los datos son muy próximos a los de antes de la pandemia. Al revisar los datos que proporciona [Waze](https://www.waze.com/es/covid19) para Monterrey, se tiene un comportamiento similar. Nuevamente, se observa un cambio considerable a partir de mediados de mayo, cuando se retomaron las actividades económicas.

Monterrey forma parte de la Zona Metropolitana, junto a otros 11 municipios. Contiguo a Monterrey se encuentra San Pedro Garza García, un municipio muy desarrollado económica, social e industrialmente. Debido a que la población de esta ciudad acostumbra viajar internacionalmente por su condición socioeconómica, San Pedro reportó el doceavo caso a nivel nacional el 4 de marzo y ha sido una de las ciudades más afectadas (Ver \[2]). Monterrey, a causa de esta cercanía con San Pedro, presentó pequeños brotes como se observa en la _gráfica 1_ en el mes marzo. **



## Bibliografía

** Se llegó a esta conclusión en conjunto con el equipo A08. Puedes encontrar más información sobre el COVID-19 en San Pedro [aquí]()

\[1] Aerosols, Droplets, Fomites: What We Know About Transmission Of COVID-19. Recuperado el 15 de agosto del 2020 de <https://www.npr.org/sections/goatsandsoda/2020/07/06/887919633/aerosols-droplets-fomites-what-we-know-about-transmission-of-covid-19>

\[2] Así es San Pedro Garza García, la ciudad más rica de México que implementó la Fase 4 de contingencia por COVID-19. Recuperado el 14 de agosto del 2020 de <https://www.infobae.com/america/mexico/2020/04/25/asi-es-san-pedro-garza-garcia-la-ciudad-mas-rica-de-mexico-que-implemento-la-fase-4-de-contingencia-por-covid-19/>

\[3] Cole, Matthew & Ozgen, Ceren & Strobl, Eric. (2020). **Air Pollution Exposure and COVID-19**. Disponible en <https://www.researchgate.net/publication/342233489_Air_Pollution_Exposure_and_COVID-19>

\[4] E. Conticini, B. Frediani, D. Caro **Can atmospheric pollution be considered a co-factor in extremely high level of SARS-CoV-2 lethality in Northern Italy?** Recuperado el 14 de agosto del 2020 de <https://www.sciencedirect.com/science/article/pii/S0269749120320601#cebib0010>

\[5] E. E. Félix-Arellano, A. Schilman, M. Hurtado-Díaz et al **Revisión rápida: contaminación del aire y morbimortalidad por Covid-19** Salud Publica Mex. 2020.

\[6] F. Dutheil, J. S. Baker, V. Navel **Covid-19 as a factor influencing air pollution?** Disponible en <https://www.sciencedirect.com/science/article/pii/S0269749120316468>

\[7] Monterrey reiniciará actividades económicas el 14 de mayo, Forbes México. Recuperado el 14 de agosto del 2020 de <https://www.forbes.com.mx/economia-monterrey-reiniciara-actividades-economicas-14-mayo/>

\[8] Nuevo León y sus principales sectores productivos y estratégicos. Recuperado el 14 de agosto del 2020 de <https://www.gob.mx/se/articulos/nuevo-leon-y-sus-principales-sectores-productivos-y-estrategicos>

\[9] Preguntas y respuestas sobre la enfermedad por coronavirus (COVID-19). Recuperado el 14 de agosto del 2020 de <https://www.who.int/es/emergencies/diseases/novel-coronavirus-2019/advice-for-public/q-a-coronaviruses>

\[10] ¿Qué es el ozono? Recuperado el 14 de agosto del 2020 de <http://www.aire.cdmx.gob.mx/descargas/noticias/que-es-ozono/que-es-ozono.pdf>

\[11] Ran Xu et al. **The Modest Impact of Weather and Air Pollution on COVID-19 Transmission** Disponible en <https://projects.iq.harvard.edu/files/covid19/files/weather_and_covid-19_preprint.pdf>

\[12]Webinar Gobernanza de la Calidad del Aire y Salud, Organización Panamericana de la Salud. **¿Qué nos dice el Monitoreo de la Calidad del Aire en el Contexto del COVID-19?** Abraham Ortínez, Coordinación General de Contaminación y Salud Ambiental INECC México.


![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Logo-Clubes-Negro.png)

### Challenge Equipo A09

#### Karen López / Jacqueline Reyes / Reyna Martinez
