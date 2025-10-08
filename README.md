# 📘 Comandos de Git para el Manejo de Ramas

## 🧩 1. Concepto de ramas en Git
Una **rama (branch)** es una línea de desarrollo independiente que permite trabajar sin afectar la rama principal (`main` o `master`).

---
### 🧩 1.1. Concepto de iniciar proyecto en Git
```Se empezara para clonar tu repo virtual al local con: git init```

```Luego seguira el comando: git clone link del repositorio que esta en tu github```
## 🌱 2. Creación de ramas
```bash
git branch <nombre_rama>          # Crea una nueva rama local
git checkout -b <nombre_rama>     # Crea y cambia a una nueva rama
git switch -c <nombre_rama>       # Crea y cambia usando el comando moderno
```

---

## 🔄 3. Cambio de ramas
```bash
git checkout <nombre_rama>        # Cambia a la rama especificada
git switch <nombre_rama>          # Alternativa moderna a checkout
```

---

## 🔍 4. Listado y visualización de ramas
```bash
git branch                        # Lista ramas locales
git branch -a                     # Muestra ramas locales y remotas
git branch -r                     # Muestra ramas remotas
git show-branch                   # Muestra ramas y commits asociados
```

---

## 🧹 5. Eliminación de ramas
```bash
git branch -d <nombre_rama>       # Elimina una rama fusionada
git branch -D <nombre_rama>       # Elimina forzadamente una rama
git push origin --delete <nombre> # Elimina una rama remota
```

---

## 🔀 6. Fusión de ramas (Merge)
```bash
git merge <nombre_rama>           # Fusiona la rama especificada
git merge --no-ff <nombre_rama>   # Crea un commit de fusión
```

---

## 🪄 7. Rebase (reorganizar commits)
```bash
git rebase <rama_base>            # Reaplica commits sobre otra rama
git rebase -i <rama>              # Reordena o combina commits
git rebase --continue             # Continúa tras resolver conflictos
git rebase --abort                # Cancela el rebase
```

---

## 🌐 8. Sincronización con ramas remotas
```bash
git push origin <nombre_rama>     # Envía una rama al remoto
git pull                          # Actualiza la rama actual
git fetch                         # Descarga referencias remotas
```

---

## 🧭 9. Renombrar ramas
```bash
git branch -m <nuevo_nombre>                # Renombra la rama actual
git branch -m <antiguo> <nuevo_nombre>      # Renombra una rama específica
```

---

## 🧰 10. Comparación de ramas
```bash
git diff <rama1> <rama2>          # Muestra diferencias entre ramas
git log <rama1>..<rama2>          # Muestra commits únicos entre ramas
```

---

## 🧭 11. Seguimiento y vinculación de ramas
```bash
git branch --set-upstream-to=origin/<rama>  # Configura seguimiento remoto
```

---

## 🧩 12. Comandos avanzados útiles
```bash
git show-branch                   # Muestra historial de ramas
git reflog                        # Muestra historial de cambios de HEAD
git cherry-pick <hash_commit>     # Copia un commit específico
git worktree add <ruta> <rama>    # Trabaja en varias ramas a la vez
git restore --source <rama> <archivo>  # Restaura archivo desde otra rama
```

---

## 🧾 13. Ejemplo de flujo completo
```bash
git switch -c feature/login       # Crear y cambiar a nueva rama
git add .                         # Agregar cambios
git commit -m "Agregar login"     # Confirmar cambios
git switch main                   # Cambiar a la rama principal
git merge feature/login           # Fusionar cambios
git push origin main              # Subir cambios al remoto
git branch -d feature/login       # Eliminar rama local
git push origin --delete feature/login  # Eliminar rama remota
```

---

## 🧠 14. Buenas prácticas
- Usa nombres descriptivos (`feature/`, `bugfix/`, `hotfix/`, `release/`).
- Borra ramas que ya no se usen.
- Sincroniza frecuentemente con `main`.
- Evita merges directos desde `main` a desarrollo.
- Usa `rebase` para mantener un historial limpio.
