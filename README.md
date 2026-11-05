# Póster oficial del Coloquio de Invierno 2026

Póster oficial del Coloquio de Invierno 2026 en Ingeniería para la Innovación
Tecnológica, del Posgrado en Ingeniería para la Innovación Tecnológica de la
[Universidad Autónoma de Zacatecas](https://innovaciontecnologica.uaz.edu.mx/).

El proyecto está escrito en LaTeX vertical en formato A0. `main.tex` utiliza
`fondo.pdf` como fondo a página completa y presenta una evaluación del semirango
BF-suitable. La figura `Fig01.png`, la tabla de lectura aproximada y la
referencia bibliográfica forman parte del póster; verifica los valores con los
datos originales antes de presentarlos como resultados definitivos.

## Compilar

Desde esta carpeta, ejecuta:

```sh
latexmk -pdf -interaction=nonstopmode main.tex
```

El resultado será `main.pdf`. Edita los títulos y textos de ejemplo en `main.tex`;
mantén `fondo.pdf` y las imágenes usadas junto al archivo fuente para que se
incluyan al compilar.

## Guía para un póster científico

- **Define el mensaje central.** Resume en una frase qué pregunta aborda el
	trabajo y cuál es su principal hallazgo. El título debe ser específico y
	fácil de entender a distancia.
- **Sigue un recorrido lógico.** Presenta el contexto y el objetivo, explica el
	método, muestra los resultados, interprétalos en la discusión y cierra con
	conclusiones relacionadas directamente con el objetivo.
- **Haz que el resumen sea autónomo.** Incluye el problema, el objetivo, el
	método, uno o dos resultados cuantitativos y la conclusión principal.
- **Prioriza evidencia visual.** Usa figuras y tablas con ejes, unidades,
	leyendas y pies que se entiendan por sí solos. Cita cada figura en el texto y
	evita repetir en párrafos todos los datos que ya muestra una gráfica.
- **Facilita la lectura rápida.** Organiza el contenido en columnas, usa
	encabezados descriptivos y párrafos breves, deja espacio en blanco y mantén
	contraste suficiente entre texto y fondo. Comprueba que tamaños, etiquetas y
	referencias se lean al tamaño de impresión A0.
- **Cuida la validez.** Distingue resultados medidos, simulados y estimados;
	no presentes lecturas visuales aproximadas como datos exactos. Incluye las
	limitaciones relevantes y cita las fuentes utilizadas.
- **Revisa antes de imprimir.** Comprueba ortografía, nombres y afiliaciones,
	referencias cruzadas, resolución de imágenes, márgenes y que el PDF final sea
	de una sola página A0.

## Agregar una figura

Coloca el archivo de imagen en esta carpeta y dentro del entorno `figure` usa:

```latex
\begin{figure}[htbp]
	\centering
	\includegraphics[width=\linewidth]{Fig01.png}
	\caption{Descripción breve de la figura.}
	\label{fig:mi-figura}
\end{figure}
```

Puedes citarla en el texto con `Figura~\ref{fig:mi-figura}`. Para incluir
referencias, añade una entrada `\bibitem{clave}` dentro de
`thebibliography` y cítala con `\cite{clave}`.