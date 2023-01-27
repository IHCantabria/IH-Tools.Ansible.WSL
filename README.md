# Ansible WSL

Para una fácil configuración de las herramientas que solemos utilizar en el Windows Subsystem Linux, se han preparado diferentes recetas disponibles en la carpeta `playbooks`.

## Instalación

Para ejecutar los playbooks, es necesario instalar el paquete `ansible`:

```sh
sudo apt install --no-install-recommends ansible
```

## Ejecución

Para ejecutar los playbooks, se debe ejecutar el siguiente comando:

```sh
ansible-playbook -K playbooks/<playbook>.yml
```

El parámetro `-K` indica que se solicitará la contraseña del usuario para ejecutar los comandos con privilegios de administrador.

## Playbooks disponibles

- `general.yml`: Instala las herramientas generales que solemos utilizar en el WSL.
  - cdo
  - curl
  - git
  - libgdal-dev
  - nco
  - python3-pip
  - python3.10-venv
  - screen
  - vim
- `fstab.yml`: Configura el fichero `/etc/fstab` para montar los directorios compartidos de Windows.
- `node.yml`: Instala Node.js y Yarn.
- `python.yml`: Instala Python 3.6.15. (Por defecto tenemos 3.10)
- `zsh.yml`: Instala ZSH y Oh My Zsh.

## Contacto

Mantenimiento: [Felipe Maza](https://ihcantabria.com/directorio-personal/felipe-maza-fernandez/) @ [IHCantabria](https://ihcantabria.com)
