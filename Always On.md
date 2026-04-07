En esta parte vamos a discutir sobre el por que de algunas reglas:

```markdown
## RULES

1. Leer STATE.md antes de actuar.
Antes de cualquier acción, leer STATE.md para entender el estado actual del proyecto.
```

Es importante para q justo al contexto del propio mensaje pueda saber en q parte del proyecto esta, evita errores de falta de contexto.
___

```markdown
2. Toda tarea sigue su pipeline.

Si el humano aún no ha aprobado el Implementation Plan → leer y cumplir /pipeline-desing
Si el humano ha aprobado el Implementation Plan → leer y cumplir /pipeline-build
Si no está claro en qué fase estás → STOP y preguntar al humano
```

Separa la tarea en dos bloques, con sus reglas especificas, y para no suturar la memoria con ambas reglas, solo le descarga las reglas necesarias cuando sea necesario.
___

```markdown
3. PROHIBIDO modificar .agents/skills/ directamente.

4. Toda creación o actualización de Skills debe proponerse mediante Artifact y esperar aprobación humana.
```

Evita que por fallos de la IA esta cambie cosas importantes sin la aprobación humana, esta mas relacionado con reglas más avanzadas dentro de las pipelines.
___

```markdown
5. Kill-switch
Si un error se repite → incrementar contador en STATE.md.

[INTENTO 1/3] → continuar
[INTENTO 2/3] → continuar con precaución
[INTENTO 3/3] y fallo → PROHIBIDO seguir. Cambiar estado a [BLOQUEADO por BUCLE], generar Artifact con el log del error y STOP total hasta respuesta humana.
```

Evita q la IA entre en un bucle infinito de errores, es importante q este en el Always On aunque no este siempre implementándose para evitar errores.