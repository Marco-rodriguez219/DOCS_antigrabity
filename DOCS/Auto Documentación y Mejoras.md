Esta parte básicamente se encarga de mantener la información actualizada por si recibe algún cambio. La primera vez q se hace esta información en la hace el propio humano en la fase de preparación del Setup. 
La separamos en dos partes importantes, cumplen prácticamente la misma función, la única diferencia esta en que uno se encarga de la comunicación que existe entre distintos contenedores y la otra entre distintos módulos dentro de cada contenedor.
___
Por comodidad solo voy a desglosar uno de ellos.

```markdown
## RULES
1. PROHIBIDO crear o modificar Skills directamente — siempre mediante Artifact.
2. Si la intención es crear una Skill nueva → cargar .agents/skills/skill-rules/SKILL.md antes de continuar.
```

La primera regla es innecesaria ya que supuestamente esta ya claro en el Always on, pero debido a los pocos tokens que consumen he decidido dejarlo.
La segunda se asegura de q lean la skill en la q se expecifica como hacer una skill correctamente.
___

```markdown
## STEP BY STEP

1. Identificar la conexión
Describir exactamente qué interacción entre contenedores no está documentada.

2. Buscar Skill existente:

¿Existe ya una Skill en .agents/skills/contracts/ que debería cubrirla?

Sí → ir a paso 3a
No → ir a paso 3b
```

En esta parte se obliga a la IA a asegurarse de q no esta aqui por error y en la segunda se difiere entre si va a crear una nueva skill o solo actualizan una antigua.
___

```markdown
3a. Actualizar Skill existente.
Generar Artifact con el diff de lo que se añade a la Skill existente.

3b. Crear Skill nueva.
Cargar .agents/skills/skill-rules/SKILL.md y generar Artifact con la Skill completa en .agents/skills/contracts/

4. STOP — Aprobación humana.
PROHIBIDO continuar hasta aprobación explícita.

5. Cerrar ciclo.
Invocar /actualizar-state.
```

Se manda a cada IA a donde deba ir y se asegura de que no lo implementen sin la aprobación humana