# Verificación de la actualización de autoría y créditos

Fecha: 4 de noviembre de 2026.
Base: el ZIP de la carpeta Git entregado por el usuario.
Resultado: CORRECTO en las dos compilaciones independientes.

## Alcance

Se retiró un nombre de la autoría, los créditos, los metadatos y las listas del
proyecto, por instrucción del autor de correspondencia. Se retiró la afiliación
que quedó sin autor y se renumeraron las cinco afiliaciones restantes. Se
ajustaron puntuación y referencias al número de autores. No se atribuyó a otra
persona el liderazgo retirado; se conservaron los créditos de apoyo de los demás.

No se modificaron resultados, código ejecutable, salidas del notebook, metadatos
del notebook, datos, ecuaciones, figuras, referencias, licencias ni financiación.
Los cambios del notebook se limitan a créditos en las celdas Markdown 02, 14 y 34.

## Compilación

Primera prueba: pdfLaTeX, BibTeX y pasadas hasta estabilizar las referencias.
Segunda prueba: descompresión del nuevo paquete en otra carpeta y compilación
únicamente con pdfLaTeX y el main.bbl incluido.

Ambas produjeron 33 páginas y 11 referencias, con el mismo texto. No se detectaron
errores, referencias sin resolver, glifos ausentes ni cajas desbordadas.
El aviso de epstopdf sobre shell escape desactivado es no bloqueante.
main.bbl se regeneró y sus bytes son idénticos a los anteriores.
Los comandos y sus códigos de salida están en BUILD_REPORT.json.

## Verificación visual

Se compararon las 33 páginas del paper: solo cambian las páginas 1 y 23.
Se compararon las 14 páginas de la presentación: solo cambia la página 1.
Las páginas modificadas se renderizaron también con Poppler y se inspeccionaron.
La presentación conserva sus fuentes, imágenes y fondo; el texto se eliminó de
las instrucciones internas del PDF, sin cubrirlo con un rectángulo.

## Paquetes y publicación

El paquete para arXiv contiene 39 archivos y main.tex/main.bbl en la raíz.
La copia del repositorio conserva los archivos de trabajo y omite .git para no
sobrescribir el historial ni la configuración de la copia local del usuario.
No se modificó GitHub, no se realizó un commit y no se depositó nada en arXiv.
La retirada afecta la versión actual de los archivos, no los commits anteriores.
