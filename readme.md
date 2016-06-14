¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1
Porque con el hard borro el working copy y el ~1 indica que es justo el commit anterior al que quiero volver.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
git reset --hard ID_COMMIT (el que quiero recuperar)
Porque el --hard me modifica el working copy y me mueve el HEAD al commit que yo quiero recuperar.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
No, porque el commit de master ya pertenecía lo tenía la rama styled. No ha absorbido nada nuevo.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí, porque el archivo git-nuestro.md contiene información diferente en las mismas líneas en el mismo archivo
para los commits más actualizados de las ramas styled y htmlify.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, porque el conflicto con htmlify ya estaba resuelto previamente al ser absorbido por styled.

- ¿Qué comando o comandos utilizaste en el paso 25?
 git log --graph --decorate --pretty=oneline

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
Sí, porque puede avanzar la rama master hasta title sin necesidad de crear ningún nuevo nodo, simplemente
avanzando hasta su hijo, que en este caso es title.

- ¿Qué comando o comandos utilizaste en el paso 27?
git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?
git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29?
git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?
git checkout ID_COMMIT (merge que quiero rehacer, sacado de reflog)
git tag mergeRecuperado
git checkout master
git merge mergeRecuperado
git tag -d mergeRecueprado

- ¿Qué comando o comandos usaste en el paso 32?
git reflog (Saco ID del commit que quiero, el inicial)
git checkout ID_COMMIT 

- ¿Qué comando o comandos usaste en el punto 33?
git checkout ID_COMMIT (el del commit final)