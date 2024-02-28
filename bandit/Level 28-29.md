## Objetivo
There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.
## Datos de acceso
AVanL161y9rsbcJIsFHuw35rjaOM19nR
## Solución

Clonar repo
```
git clone ssh://bandit28git@localhost:2220/home/bandit28-git/repo
bandit28@bandit:/tmp/gitdiego$ cd repo
bandit28@bandit:/tmp/gitdiego/repo$ git log
commit 14f754b3ba6531a2b89df6ccae6446e8969a41f3 (HEAD -> master, origin/master, origin/HEAD)
Author: Morla Porla <morla@overthewire.org>
Date:   Thu Oct 5 06:19:41 2023 +0000

bandit28@bandit:/tmp/gitdiego/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: xxxxxxxxxx
bandit28@bandit:/tmp/gitdiego/repo$ git checkout f08b9cc63fa1a4602fb065257633c2dae6e5651b
bandit28@bandit:/tmp/gitdiego/repo$ cat README.md
# Bandit Notes
Some notes for level29 of bandit.

## credentials

- username: bandit29
- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

```

## Notas adicionales
Git checkout cambiar a otra rama
## Referencias
