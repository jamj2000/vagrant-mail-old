# Escenario base para servicios de e-mail

## Descripción del escenario

El escenario que se despliega consta de los siguientes nodos:

| Nodo    | IP          | Descripción          |
| ------- | ----------- | -------------------- |
| dns     | 172.31.0.10 | Servidor DNS         |
| correo1 | 172.31.0.11 | Servidor de correo 1 |
| correo2 | 172.31.0.12 | Servidor de correo 2 |

Falta por configurar:

- BIND: Zona de búsqueda directa
- Postfix
- Dovecot


## Utilización básica del escenario

### Desplegar y configurar el escenario base

~~~
vagrant up
ssh-add ~/.vagrant.d/insecure_private_key
~~~

### Utilizar el servidor DNS del escenario

~~~
sudo ./utils/dns-escenario.sh
~~~

### Desechar el escenario correctamente

Cuando termines de trabajar con el escenario, puedes desecharlo haciendo lo siguiente:

~~~
vagrant destroy -f
sudo ./utils/dns-sistema.sh
~~~


