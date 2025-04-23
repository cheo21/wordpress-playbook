# Playbook: WordPress

Este playbook de **Ansible** instala y configura una instancia de **WordPress** junto con:

- Servidor web **Apache**
- Lenguaje **PHP**
- Base de datos **MySQL Server**

Está diseñado para ejecutarse en sistemas basados en **Debian** o **RHEL** (como CentOS, Rocky Linux, AlmaLinux, etc.).

---

## ✅ Requisitos

Antes de aplicar este role, asegúrate de:

1. Tener **Ansible** instalado (`>=2.17`).
2. Haber instalado los roles de Ansible Galaxy definidos en `requirements.yml`.

### Instalación de dependencias

Este playbook depende de roles definidos en el archivo `requirements.yml`. Para instalarlos, ejecutá:

```bash
ansible-galaxy install -r ansible/requirements/roles.yml    
