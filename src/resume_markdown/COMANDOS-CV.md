# Comandos para generar el CV (inglés y español)

Correr desde la raíz del repositorio (`resume-markdown/`).

## Requisitos

- `python3` con el paquete `markdown` instalado (ya está en el sistema).
- Chromium o Chrome para la conversión a PDF. En esta máquina está en `/snap/bin/chromium`
  (si tenés Chrome/Chromium en otra ruta, pasarla con `--chrome-path=...`; el tool
  también intenta detectarlo solo si no le pasás el flag).

## Generar el CV en inglés

```bash
PYTHONPATH=src python3 -m resume_markdown build src/resume_markdown/resume.md --css src/resume_markdown/resume.css --lang en --chrome-path=/snap/bin/chromium
```

Genera `src/resume_markdown/resume.html` y `src/resume_markdown/resume.pdf`.

## Generar el CV en español

```bash
PYTHONPATH=src python3 -m resume_markdown build src/resume_markdown/resume-es.md --css src/resume_markdown/resume.css --lang es --chrome-path=/snap/bin/chromium
```

Genera `src/resume_markdown/resume-es.html` y `src/resume_markdown/resume-es.pdf`.

## Renombrar a los nombres de entrega

El build deja los PDFs como `resume.pdf` / `resume-es.pdf`; la convención del repo
es renombrarlos así:

```bash
mv src/resume_markdown/resume.pdf "src/resume_markdown/CARDELLI, Ramiro - CV.pdf"
mv src/resume_markdown/resume-es.pdf "src/resume_markdown/CARDELLI, Ramiro - CV (ES).pdf"
```

## Todo junto

```bash
PYTHONPATH=src python3 -m resume_markdown build src/resume_markdown/resume.md --css src/resume_markdown/resume.css --lang en --chrome-path=/snap/bin/chromium && \
PYTHONPATH=src python3 -m resume_markdown build src/resume_markdown/resume-es.md --css src/resume_markdown/resume.css --lang es --chrome-path=/snap/bin/chromium && \
mv src/resume_markdown/resume.pdf "src/resume_markdown/CARDELLI, Ramiro - CV.pdf" && \
mv src/resume_markdown/resume-es.pdf "src/resume_markdown/CARDELLI, Ramiro - CV (ES).pdf"
```

## Notas

- El `RuntimeWarning: 'resume_markdown.__main__' found in sys.modules...` es inofensivo.
- El build también regenera los `.html`; van junto con los cambios.
- Los PDFs renombrados pisan los PDFs trackeados en git (quedan en el historial).
- Verificar el resultado (opcional):

  ```bash
  pdfinfo "src/resume_markdown/CARDELLI, Ramiro - CV.pdf" | grep -E 'Pages|Page size'
  pdftotext "src/resume_markdown/CARDELLI, Ramiro - CV (ES).pdf" - | head -20
  ```
