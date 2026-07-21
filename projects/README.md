# `projects/` — deja aquí tus aplicaciones

## Plug-and-play
1. Clona / abre el repo del arnés.
2. Copia o clona **tu** proyecto dentro de esta carpeta:

```bash
# ejemplo
git clone <url-de-tu-app> projects/mi-app
# o: cp -R ~/codigo/mi-app projects/mi-app
```

3. Abre este repo en Cursor (u otra IA con los bridges) y escribe en el chat, por ejemplo:

```
Hola — trabaja sobre projects/mi-app. Quiero <objetivo en una frase>.
```

El arnés se activa solo: detecta la app, mapea el stack, propone cambios y va guardando aprendizajes en `.ai/memory/` **sin que edites el arnés**.

## Reglas simples
- Un directorio = una app (`projects/api`, `projects/web`, …).
- Cualquier nombre de carpeta sirve.
- No pongas secretos en el chat; usa `.env` dentro de tu app (no se commitea si está en `.gitignore`).
- No necesitas tocar `.ai/` ni `.cursor/`.
