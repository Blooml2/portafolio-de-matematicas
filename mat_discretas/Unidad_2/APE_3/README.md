# 📝 APE 3 — Unidad 2

<div align="center">

![](https://img.shields.io/badge/Secci%C3%B3n-APE%203-0d6efd?style=flat-square)

</div>

---
[APE 3 Completo](APE3.pdf)

Ejercicios personales:

5.1 FASE 5: Los estudiantes investigan y presentan de forma participativa las leyes
y propiedades adicionales mediante ejemplos prácticos.
GUÍA DE INVESTIGACIÓN Y PRESENTACIÓN: LEYES Y PROPIEDADES
ADICIONALES DEL ÁLGEBRA BOOLEANA
1. TEOREMA DEL CONSENSO DUAL (DUAL CONSENSUS THEOREM)
Definición y Explicación
Mientras que el teorema del consenso estándar opera sobre una suma de productos, el
Teorema del Consenso Dual se aplica directamente a expresiones en forma de producto
de sumas (POS). Este teorema establece que en una combinación de tres variables lógicas
sumadas en parejas, uno de los términos de la multiplicación es completamente
redundante y puede ser eliminado sin alterar el comportamiento o resultado de la función.
Identidad Matemática
(A + B) · (A' + C) · (B + C) = (A + B) · (A' + C)
Donde A' significa "A negado".
Demostración intuitiva
Analicemos el término (B + C). Si tanto B como C son verdaderos (1), este paréntesis es
verdadero. Sin embargo, debido a que la variable A debe tomar obligatoriamente un valor
binario (ya sea 1 o 0), su presencia en los dos primeros términos ((A + B) y (A' + C))
forzará a que uno de ellos dependa exclusivamente de los valores de B o C. Esto hace que
el tercer paréntesis sea una repetición lógica que no aporta nueva información.
Ejercicio Práctico Resuelto
Enunciado: Simplificar la siguiente expresión lógica utilizada para el control de un
circuito de automatización:
F = (X + Y) · (X' + Z) · (Y + Z)

Solución Paso a Paso

<img width="767" height="232" alt="image" src="https://github.com/user-attachments/assets/05630b42-ff9c-47f1-a08b-7665975708f9" />

<img width="785" height="382" alt="image" src="https://github.com/user-attachments/assets/2debf887-1ea5-4a79-94d4-ea1a7c5a6c0c" />

Resultado Simplificado:
F = (X + Y) · (X' + Z)
Aplicación en la Vida Real y Conexión con Diseño Digital
En el diseño de hardware y circuitos lógicos integrados, implementar la función original:
F = (X + Y) · (X' + Z) · (Y + Z)
requiere físicamente tres compuertas OR independientes que luego conectan sus salidas
a una compuerta AND de tres entradas.
Al aplicar el Teorema del Consenso Dual, optimizamos el circuito reduciéndolo a sólo
dos compuertas OR y una compuerta AND de dos entradas.
 FEIRNNR - Carrera de Computación
2. ÁLGEBRA BOOLEANA GENERAL: LEYES DE DE MORGAN
Definición y Explicación
Las Leyes de De Morgan son herramientas fundamentales para la transformación de
compuertas lógicas y la simplificación de condiciones complejas. Explican la
equivalencia matemática que existe al distribuir o retirar una negación (operador NOT)
de un paréntesis que contiene operaciones OR o AND.
Identidades Matemáticas
Primera Ley:
(A · B)' = A' + B'
(La multiplicación negada se convierte en suma de variables negadas)
Segunda Ley:
(A + B)' = A' · B'
(La suma negada se convierte en multiplicación de variables negadas)
Ejercicio Práctico Resuelto
Enunciado: Un sistema de desarrollo de software cuenta con la siguiente condición
lógica anidada:
if not (status == "active" and points > 100):

Solución Paso a Paso

<img width="765" height="446" alt="image" src="https://github.com/user-attachments/assets/18962d72-080e-421b-bc57-0eac3953abc9" />

<img width="787" height="240" alt="image" src="https://github.com/user-attachments/assets/0369e745-f18f-4c46-bdab-d658fdc39d1f" />

3. TEOREMA DE EXPANSIÓN DE SHANNON (SHANNON'S EXPANSION
THEOREM)
Definición y Explicación
Propuesto por Claude Shannon, este teorema establece que cualquier función booleana
compleja puede ser descompuesta en subfunciones más pequeñas mediante el aislamiento
de una variable de control.
Identidad Matemática
F(X1, X2, ..., Xn) = X1 · F(1, X2, ..., Xn) + X1' · F(0, X2, ..., Xn)
Ejercicio Práctico Resuelto
Enunciado: Expandir la siguiente función lógica con respecto a la variable B:
F(A, B, C) = A · B + A' · C

Solución Paso a Paso

<img width="762" height="453" alt="image" src="https://github.com/user-attachments/assets/d3e206c0-f99c-4f1d-84be-6307f04bd0bd" />

<img width="773" height="185" alt="image" src="https://github.com/user-attachments/assets/a4aab524-274b-49c7-ab7c-b5ab1f90b0fc" />


Resultado de la Expansión
F(A, B, C) = B · (A + C) + B' · (A' · C)
Aplicación en la Vida Real y Conexión con Arquitectura de Computadores
En la ecuación resultante de la expansión, la variable B funciona exactamente como la
línea de selección (Select) de un multiplexor de 2 a 1:
• Si B = 1, el multiplexor da paso a los datos de la subfunción (A + C).
• Si B = 0, el multiplexor da paso a los datos de la subfunción (A' · C).
Esta propiedad es crítica para las FPGAs (Field Programmable Gate Arrays) y chips
programables modernos, donde las funciones lógicas se implementan mediante LUTs
(Look-Up Tables) basadas en el Teorema de Shannon.

5.2 FASE 5: Práctica de implementación de funciones booleanas usando únicamente
compuertas NAND o NOR (puertas universales)

Ejercicio 1 - COMPUERTAS NAND

<img width="760" height="262" alt="image" src="https://github.com/user-attachments/assets/e38f0a27-cdf0-4519-9fb3-4f2e868d8fed" />

Circuito

<img width="688" height="222" alt="image" src="https://github.com/user-attachments/assets/833d11a4-3bf2-42ea-9d3d-ba03ccf6269c" />

Ejercicio 2 – COMPUERTAS NAND

<img width="747" height="273" alt="image" src="https://github.com/user-attachments/assets/bf1716f9-00de-44b4-9648-18cd83ff7cba" />

Circuito

<img width="612" height="270" alt="image" src="https://github.com/user-attachments/assets/1e90d2bb-2bea-4fe0-abc7-b309c3fae429" />

Ejercicio 3 – COMPUERTAS XOR

<img width="693" height="238" alt="image" src="https://github.com/user-attachments/assets/811e8128-69f5-4f85-aead-af0f4db3d4ba" />

Circuito

<img width="667" height="215" alt="image" src="https://github.com/user-attachments/assets/e695459e-efdb-4b38-83f4-bf927e795cda" />


5.3 FASE 5: Los equipos elaboran un informe reflexivo sobre la optimización lógica
en sistemas computacionales
Informe Reflexivo: Optimización Lógica en Sistemas Computacionales y su
Impacto Ambiental
Introducción
La optimización lógica es una técnica fundamental en el diseño de sistemas
computacionales y circuitos digitales. Consiste en simplificar expresiones booleanas para
reducir la cantidad de compuertas lógicas y componentes electrónicos necesarios para
implementar una determinada función. Este proceso no solo mejora el rendimiento de los
sistemas, sino que también contribuye a disminuir costos de fabricación, consumo
energético y efectos ambientales asociados a la producción tecnológica.
Desarrollo
Los sistemas computacionales modernos dependen de millones de circuitos electrónicos
que procesan información mediante operaciones lógicas. Cuando una expresión booleana
se simplifica utilizando métodos como el Álgebra de Boole o los Mapas de Karnaugh, se
reduce el número de compuertas requeridas para construir un circuito. Esta reducción
implica un diseño más eficiente y menos complejo.
Desde el punto de vista económico, la optimización lógica permite disminuir la cantidad
de materiales utilizados durante la fabricación de circuitos integrados. Al necesitar menos
componentes electrónicos, los costos de producción, ensamblaje y mantenimiento
también se reducen. Esto resulta especialmente importante en la industria tecnológica,
donde pequeñas mejoras en el diseño pueden generar grandes ahorros cuando se fabrican
miles o millones de dispositivos.
En cuanto al consumo energético, un circuito simplificado requiere menos transistores
activos para realizar la misma función. Como consecuencia, se reduce la energía eléctrica
consumida durante el funcionamiento del sistema. Esta característica es fundamental en
dispositivos portátiles, centros de datos y equipos de procesamiento de alta demanda,
donde la eficiencia energética representa un factor crítico para el rendimiento y la
sostenibilidad.
Además, la optimización lógica tiene una relación directa con la reducción de la huella
ambiental. La fabricación de componentes electrónicos requiere materias primas, energía
y procesos industriales que generan emisiones contaminantes. Al disminuir la cantidad
de elementos necesarios para construir un circuito, también se reduce el consumo de
recursos naturales y la generación de residuos electrónicos. De esta manera, la
optimización lógica contribuye indirectamente a la protección del medio ambiente y al
desarrollo de tecnologías más sostenibles.
Reflexión Crítica
El análisis realizado permite comprender que la optimización lógica no debe considerarse
únicamente como una herramienta matemática o técnica para simplificar circuitos. Su
impacto trasciende el ámbito computacional y alcanza aspectos económicos, energéticos
y ambientales. Como estudiante de Computación, considero que aprender técnicas de
simplificación booleana es esencial, ya que permite desarrollar soluciones más eficientes
y responsables.
En la actualidad, donde el uso de la tecnología crece constantemente, los profesionales
de la informática y la electrónica tienen la responsabilidad de diseñar sistemas que
aprovechen mejor los recursos disponibles. Cada compuerta eliminada mediante una correcta optimización representa una oportunidad para reducir costos, ahorrar energía y
disminuir el impacto ambiental de los dispositivos tecnológicos.
Conclusión
La optimización lógica constituye una herramienta clave en el diseño de sistemas
computacionales modernos. La simplificación de expresiones booleanas permite reducir
la complejidad de los circuitos, disminuir costos de fabricación y mejorar la eficiencia
energética de los dispositivos. Asimismo, contribuye a reducir la huella ambiental al
requerir menos materiales y recursos durante los procesos de producción. Por estas
razones, la optimización lógica no solo representa una mejora técnica, sino también una
práctica alineada con los principios de sostenibilidad y responsabilidad tecnológica que
deben caracterizar a los profesionales de la Computación.

5.4 Práctica integradora: cada equipo resuelve un caso aplicado a la computación
(diseño de un sumador binario de 1 bit, un comparador digital, o un
codificador/decodificador) aplicando todas las técnicas de simplificación
aprendidas.

Diseño de un sumador binario de 1 bit

<img width="770" height="390" alt="image" src="https://github.com/user-attachments/assets/b09baae5-aa4e-4cd3-805c-75a64c93189d" />

Tabla de Verdad

<img width="752" height="316" alt="image" src="https://github.com/user-attachments/assets/700c1435-9c5e-4390-886e-a7c446ed5f62" />

Función boolena

<img width="688" height="240" alt="image" src="https://github.com/user-attachments/assets/735244cc-cb50-4917-865a-3734d0d6dd45" />

Simplificación con mapas de Karnaugh

<img width="777" height="795" alt="image" src="https://github.com/user-attachments/assets/28cb1cfa-34d7-4d6b-a15a-2080c8aa83c3" />

Algebra de Boole

<img width="767" height="707" alt="image" src="https://github.com/user-attachments/assets/45a1f591-313a-4548-9b34-767d15db5d27" />

Diseño del circuito

<img width="778" height="760" alt="image" src="https://github.com/user-attachments/assets/fe0838d8-682f-432a-a300-d5ea5e282814" />

<img width="522" height="706" alt="image" src="https://github.com/user-attachments/assets/718ccfd8-7278-4806-97e7-37cbd6b12587" />

---

<div align="center">
<a href="../README.md">⬅️ Volver a Unidad 2</a>
</div>
