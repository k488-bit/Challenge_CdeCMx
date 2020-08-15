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

El brote de COVID-19 ha tenido un gran impacto en nuestra vida diaria, cambiando nuestro mundo y llevándonos al camino de la adaptación. Todo esto nos llevó a obtener una nueva normalidad en distintos ámbitos como el comercio, nuestra interacción con las personas, etcétera. La principal medida de prevención es el distanciamiento social, pero ¿Qué otros aspectos influyen en el número de contagios? ¿Se puede relacionar el brote de COVID-19 con la contaminación ambiental? ¿Qué tanto impacto tienen las particulas PM2.5 y la temperatura? Exploraremos estas cuestiones para la ciudad de Monterrey, realizando un análisis con ayuda de Python a partir de los datos de contagios, contaminación, climatología y movilidad.

## Covid-19

EL COVID-19 es una enfermedad infecciosa causada por el coronavirus que se ha descubierto en diciembre de 2019 en Wuhan (China). Los coronavirus son una familia de virus que puede causar enfermedades en animales y humanos así como infecciones respiratorias que pueden ir desde el resfriado hasta enfermedades más graves. Actualmente el COVID-19 es una pandemia que afecta a muchos países del mundo de muchas maneras.

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/gh-pages/Images/Coronavirus.gif)

*Representación animada del SARS-CoV-2*

### Síntomas

Los síntomas más comunes son la fiebre, la tos seca y el cansancio. Mientras que otros menos frecuentes dolores de cabeza y de garganta, congestión nasal, la conjuntivitis, el dolor de garganta, la diarrea, la pérdida del gusto o el olfato y las erupciones cutáneas o cambios de color en los dedos de las manos o los pies. No todas las personas tienen los mismos sintomas y algunos suelen ser leves; además, se tiene gran índice de personas asintomáticas. 

Según la Organización Mundial de la Salud (OMS), alrededor del 80% de las personas se recuperan sin la necesidad de acudir a un hospital. Además, alrededor de 1 de cada 5 personas que contraen la COVID‑19 acaba presentando un cuadro grave y experimenta dificultades para respirar. Las personas que son más vulnerables, o bien, que pueden tener más probabilidades de presentar cuadros graves son los adultos mayores y/o las personas que padecen de hipertensión arterial, problemas cardíacos, pulmonares, diabetes o cáncer.

### ¿Cómo se contagia el coronavirus?

El virus se propaga de persona a persona y por tocar superficies infectadas. Cuando una persona contagiada estornuda, tose o habla, puede transmitir el coronavirus. Existen diferentes medios por los que pasa esto: los **droplet**, partículas grandes que suelen caer en el piso a unos metros de la persona que lo expulsó; los **aerosoles**, partículas de tamaño menor que quedan suspendidos en el aire; y los **fomite**, que son los objetos infectados con estas partículas. Estos últimos dependen del tiempo de vida del SARS-CoV-2 en la superficie de dicho objeto, puedes consultar estos tiempos [aquí](https://www.webmd.com/lung/how-long-covid-19-lives-on-surfaces) o [aquí](https://www.nejm.org/doi/full/10.1056/NEJMc2004973).

![](https://www.mdpi.com/viruses/viruses-07-00511/article_deploy/html/images/viruses-07-00511-g001-1024.png)

*Imagen obtenida de <https://www.mdpi.com/1999-4915/7/2/511/htm>*


## Panorama de Monterrey

Monterrey es una ciudad y capital del estado de Nuevo León. Esta ubicada al norte de México junto a la Sierra Madre Oriental ocupando una superficie total de Nuevo León de 64, 081.94 km^2. Con una Latitud: 25.6714, Longitud: -100.309 25° 40′ 17″ Norte, 100° 18′ 32″ Oeste. Tiene un clima seco muy cambiante, y cuenta con 1.136 millones de habitantes. Además es una ciudad industrializada, atrae a inversionistas y sus principales actividades son el comercio, la construcción, la manufactura.

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/gh-pages/Images/117645984_681250895804238_3205561972497632758_n.png)
*República Mexicana localizando a Monterrey, Nuevo León*

Son bien sabidas las medidas preventivas planteadas en México:
> Quédate en casa, mantén la sana distancia y 
> aplica medidas higiénicas

Nuevo León no fue la excepción a ello, [aquí](https://www.nl.gob.mx/publicaciones/cuales-son-las-medidas-de-prevencion-por-covid-19) encontrarás algunas recomendaciones publicadas por el gobierno. Hacia finales de marzo, se suspendieron las clases presenciales y las actividades no esenciales. Sin embargo, esto quizás fue apresurado.

![Casos en Mty](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Figura_Casos_Monterrey.png)

*Gráfica 1. Obtenida con datos de <https://coronavirus.gob.mx/>*

El alcalde de Monterrey anunció que las actividades económicas se reanudarían el 14 de mayo del presente año. (Ver \[forbes]) Podemos observar en la gráfica anterior que a mediados de mayo se disparó el número de casos en este municipio, pudiendo deberse a esta decisión. Por supuesto, existen muchos factores que influyen en el comportamiento de los contagios, y a continuación se analizará algunos de ellos.


## Temperatura

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Figura_Climatologia_Mty.png)

*Gráfica obtenida con datos de <https://es.climate-data.org>*

25 °C

## Contaminación del aire

La contaminación del aire representa un importante riesgo para la salud. Existen diversos factores, pero pueden resumirse en ambientales y antropogénicos. Los contaminantes que consideraremos aquí son el ozono (O3) y el material particulado 2.5 (PM2.5).



![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/pollutants_raw.png)

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/daily_mean_pollutants.png)

![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/daily_max_pollutants.png)

*Gráficos obtenidos con datos de <http://aire.nl.gob.mx/>*


## Factor social

### Movilidad

![Gráfica con datos de Apple](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Figura_Mobility_Apple.png)

*Gráfica obtenida con datos de <https://www.apple.com/covid19/mobility>*

*\* Revisar sección "Sobre estos datos" [aquí](https://www.apple.com/covid19/mobility).*

La gráfica indica que si bien al principio se redujo en gran medida la movilidad, en fechas más recientes los datos son muy próximos a los de antes de la pandemia. Si revisamos los datos que proporciona [Waze](https://www.waze.com/es/covid19) para Monterrey, se tiene un comportamiento similar. Nuevamente, se observa un cambio considerable a partir de mediados de mayo, cuando se reactivaron las actividades económicas.

Monterrey forma parte de la Zona Metropolitana de Monterrey, junto a otros 11 municipios; esta zona cuenta con 4.1 millones de habitantes. Contiguo a Monterrey se encuentra San Pedro Garza García, un municipio muy desarrollado económica, social e industrialmente. Debido a que la población de esta ciudad acostumbra viajar internacionalmente, fue aquí donde empezaron los contagios y ha sido una de las ciudades más afectadas (Ver \[infobae]). Monterrey, a causa de esta cercanía con San Pedro, tiene pequeños brotes como se observa en la _gráfica 1_ a mediados de marzo. **


## Conclusiones


## Bibliografía

** Se llegó a esta conclusión en conjunto con el equipo A08. Puedes encontrar más información sobre el COVID-19 en San Pedro [aquí]()

\[] Aerosols, Droplets, Fomites: What We Know About Transmission Of COVID-19. Recuperado el 15 de agosto del 2020 de <https://www.npr.org/sections/goatsandsoda/2020/07/06/887919633/aerosols-droplets-fomites-what-we-know-about-transmission-of-covid-19>

\[] Así es San Pedro Garza García, la ciudad más rica de México que implementó la Fase 4 de contingencia por COVID-19. Recuperado el 14 de agosto del 2020 de <https://www.infobae.com/america/mexico/2020/04/25/asi-es-san-pedro-garza-garcia-la-ciudad-mas-rica-de-mexico-que-implemento-la-fase-4-de-contingencia-por-covid-19/>

\[] Monterrey reiniciará actividades económicas el 14 de mayo, Forbes México. Recuperado el 14 de agosto del 2020 de <https://www.forbes.com.mx/economia-monterrey-reiniciara-actividades-economicas-14-mayo/>

\[] Nuevo León y sus principales sectores productivos y estratégicos. Recuperado el 14 de agosto del 2020 de <https://www.gob.mx/se/articulos/nuevo-leon-y-sus-principales-sectores-productivos-y-estrategicos>

\[] Preguntas y respuestas sobre la enfermedad por coronavirus (COVID-19). Recuperado el 14 de agosto del 2020 de <https://www.who.int/es/emergencies/diseases/novel-coronavirus-2019/advice-for-public/q-a-coronaviruses>

\[] ¿Qué causa la contaminación del aire? Recuperado el 14 de agosto del 2020 de <https://www.heraldo.es/branded/causas-de-la-contaminacion-del-aire/#:~:text=Las%20principales%20causas%20de%20la,y%20del%20transporte%20por%20carretera.>

\[] Ran Xu et al. The Modest Impact of Weather and Air Pollution on COVID-19 Transmission. Recuperado el 14 de agosto del 2020 de <https://projects.iq.harvard.edu/files/covid19/files/weather_and_covid-19_preprint.pdf>

\[] 

\[]


![](https://raw.githubusercontent.com/k488-bit/Challenge_CdeCMx/master/Images/Logo-Clubes-Negro.png)

### Challenge Equipo A09

#### Karen López / Jacqueline Reyes / Reyna Martinez
