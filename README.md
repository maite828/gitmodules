## gitmodules

[![Version](https://img.shields.io/badge/version-2021.5-blue)](https://github.com/maite828/gitmodules.git)
[![Version](https://img.shields.io/badge/module_A-2.7.0-yellow)](https://github.com/maite828/module_A.git)
[![Version](https://img.shields.io/badge/module_B-1.6.0-yellow)](https://github.com/maite828/module_B.git)

# CONTAINER MODULE  
#### https://pypi.org/manage/project/gitmodules_mercurio/releases/
gitmodules_mercurio[module_A==2.7.0,module_B==1.6.0]==2021.5.post12
gitmodules_mercurio[module_A==2.6.0,module_B==1.5.0]==2021.5.post10

#### Instalación de new módulo:
```sh 
git submodule add -b main ssh://git@github.com:maite828/module_A.git module_A
```                                         
#### Actualización de módulos:
```sh
git submodule update --init && git submodule update --remote --recursive
```
## TESTS
- [instalar padre con version]
   ```sh
   pip install  gitmodules_mercurio==2021.5.post12
   ```
- [instalar padre sin version]
  ```sh 
  pip install gitmodules_mercurio
  ```
- [instalar hijos]
  ```sh 
  pip install gitmodules_mercurio[module_A]
  pip install gitmodules_mercurio[module_A,module_B]
  pip install gitmodules_mercurio[all]
  ```
- [instalar un módulo de una versión padre anterior] (# en este ejemplo, la última version es 2021.5.post12)
  ```sh
  pip install gitmodules_mercurio[module_A]==2021.5.post10
  ```
- [instalar dos módulo de una versión padre anterior] (# en este ejemplo, la última version es 2021.5.post12)
  ```sh 
  pip install gitmodules_mercurio[module_A,module_B]==2021.5.post10
  ```
- [instalar padre e hijos de versión padre anterior] (# en este ejemplo, la última version es 2021.5.post12)
  ```sh 
  pip install gitmodules_mercurio[all]==2021.5.post10
  ```
- [instalar módulos sueltos] (# con version, sustituye version actual)
  ```sh
  pip install module_A==2.7.0
  pip install module_B==1.5.0
  ```
- [utilidad]
  ```sh 
  ll .venv/lib/python3.6/site-packages/
  rm -rf .venv/lib/python3.6/site-packages/git*
  rm -rf .venv/lib/python3.6/site-packages/module*
  ```
