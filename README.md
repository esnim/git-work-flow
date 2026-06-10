## Iniciar versión

```
git checkout develop
```
```
git pull origin develop
```

<br>

## Crear una feature branch

```
git checkout -b feature/vX.Y
```

<br>

## Opcional (backup temprano)

```
git push -u origin feature/vX.Y
```

<br>

## Realizar cambios

```
git add .
```
```
git commit -m "feat"
```

<br>

## Enviar cambios a GitHub

```
git push origin feature/vX.Y
```

<br>

## Continuar trabajando (backup rápido)

```
git add . && git commit -m "wip: respaldo de trabajo en progreso" && git push
```

Notas:

Usar solo en ramas feature/*.

El código puede estar incompleto o roto.

Sirve como backup inmediato.

Más adelante se pueden hacer commits prolijos (feat, fix, docs).

<br>

## Ver commits

```
git log --oneline -5
```

<br>

## Cerrar una versión

```
git checkout develop
```
```
git pull origin develop
```
```
git merge feature/vX.Y
```
```
git push origin develop
```
```
git tag -a vX.Y.0 -m "Release vX.Y.0"
```
```
git push origin vX.Y.0
```
```
git push origin --delete feature/vX.Y
```
```
git branch -d feature/vX.Y
```

<br>

## Recordatorio rápido

- Commits por bloque lógico.

- Mensajes claros (add:, fix:, docs: o wip:).

- Push cuando te sirva (backup / continuidad).

- Merge recién cuando esté cerrada la versión.

- Docs antes del tag.

<br>

## Referencias

- [Git branching model](https://nvie.com/posts/a-successful-git-branching-model/)
- [Git branching strategies](https://www.atlassian.com/git/tutorials/using-branches/merge-strategy)
- [Git tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

<br>

## Tipos de commits recomendados

### feat
Agrega una funcionalidad nueva o amplía una existente.

<br>

### fix
Corrige un bug o un comportamiento incorrecto.

<br>

### docs
Cambios solo en documentación (.md, README, notas).

<br>

### style
Cambios de estilo visual o formato sin afectar lógica.

<br>

### refactor
Reorganización de código sin cambiar comportamiento.

<br>

### chore
Cambios de mantenimiento o soporte que no son feature ni bugfix.

Incluye: assets (imágenes, favicon), config, scripts, limpieza, tooling, estructura de archivos.

<br>

### test (opcional)
Agrega o modifica tests.

<br>

### build (opcional)
Cambios relacionados a build, bundling o dependencias.

<br>

### wip (uso temporal)
Trabajo en progreso que no está listo todavía.

*Recomendado solo en features, no en develop/main.*

<br>

## Regla práctica final (para no dudar)

<table>
  <tbody>
    <tr>
      <td>¿Agrega algo nuevo?</td>
      <td>feat</td>
    </tr>
    <tr>
      <td>¿Arregla algo roto?</td>
      <td>fix</td>
    </tr>
    <tr>
      <td>¿Solo documentación?</td>
      <td>docs</td>
    </tr>
    <tr>
      <td>¿Solo estilo visual?</td>
      <td>style</td>
    </tr>
    <tr>
      <td>¿Reorganiza código?</td>
      <td>refactor</td>
    </tr>
    <tr>
      <td>¿Assets / config / orden?</td>
      <td>chore</td>
    </tr>
    <tr>
      <td>¿Incompleto?</td>
      <td>wip</td>
    </tr>    
  </tbody>
</table>
