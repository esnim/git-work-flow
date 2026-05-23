## Iniciar versión

```git checkout develop```

```git pull origin develop```


---


## Crear una feature branch

```git checkout -b feature/vX.Y```


---


## Opcional (backup temprano)

```git push -u origin feature/vX.Y```


---


## Realizar cambios

```git add .```
```git commit -m "feat"```


---


## Enviar cambios a GitHub

```git push origin feature/vX.Y```


---


## Continuar trabajando (backup rápido)

```git add . && git commit -m "wip: respaldo de trabajo en progreso" && git push```

Notas:

Usar solo en ramas feature/*.

El código puede estar incompleto o roto.

Sirve como backup inmediato.

Más adelante se pueden hacer commits prolijos (feat, fix, docs).


---


## Ver commits

```git log --oneline -5```


---


## Cerrar una versión

```git checkout develop```

```git pull origin develop```

```git merge feature/vX.Y```

```git push origin develop```

```git tag -a vX.Y.0 -m "Release vX.Y.0"```

```git push origin vX.Y.0```

```git branch -d feature/vX.Y```

```git push origin --delete feature/vX.Y```


---


## Recordatorio rápido

Commits por bloque lógico

Mensajes claros (add:, fix:, docs: o wip:)

Push cuando te sirva (backup / continuidad)

Merge recién cuando esté cerrada la versión

Docs antes del tag


---


## Referencias

- [Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)
- [Git branching strategies](https://www.atlassian.com/git/tutorials/using-branches/merge-strategy)
- [Git tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)


---


## Tipos de commits recomendados

### feat

Cuándo usarlo:

Agrega una funcionalidad nueva o amplía una existente.



### fix

Cuándo usarlo:

Corrige un bug o un comportamiento incorrecto.



### docs

Cuándo usarlo:

Cambios solo en documentación (.md, README, notas).



### style

Cuándo usarlo:

Cambios de estilo visual o formato sin afectar lógica.



### refactor

Cuándo usarlo:

Reorganización de código sin cambiar comportamiento.



### chore

Cuándo usarlo:

Cambios de mantenimiento o soporte que no son feature ni bugfix.

Incluye:

assets (imágenes, favicon)

config

scripts

limpieza

tooling

estructura de archivos

Ejemplos:

chore: agrega favicon y logos
chore: organiza estructura de assets



### test (opcional)

Cuándo usarlo:

Agrega o modifica tests.



### build (opcional)

Cuándo usarlo:

Cambios relacionados a build, bundling o dependencias.

Ejemplos:

build: ajusta configuración de webpack

build: actualiza dependencias del proyecto

### wip (uso temporal)

Cuándo usarlo:

Trabajo en progreso que no está listo todavía.

⚠️ Recomendado solo en features, no en develop/main.



## Regla práctica final (para no dudar)

¿Agrega algo nuevo? → feat

¿Arregla algo roto? → fix

¿Solo docs? → docs

¿Solo estilo visual? → style

¿Reorganiza código? → refactor

¿Assets / config / orden? → chore

¿Incompleto? → wip
