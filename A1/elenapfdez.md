[elenapfdez](https://github.com/elenapfdez/bitacoras-ISE-25-26-VIERNES) 

<details>
  <summary><strong>P1-Lección 1 </strong></summary>

### Paso 1: Crear discos y particiones
Desde configuración/almacenamiento creamos otro disco de 10 GB.  
En cada disco hacemos una partición de 500 MB y otra con el tamaño restante.  
Luego configuramos dos RAID1:
- RAID1 #0 → Asociado a las particiones pequeñas (500 MB), montado en `/boot`.
- RAID1 #1 → Asociado a las particiones grandes.

<p align="center">
  <img width="600" src="https://github.com/user-attachments/assets/1e368ac0-542a-4226-8ccd-7440e536f1dd" alt="RAID1 sobre /boot y resto del sistema">
</p>

---

### Paso 2: Crear y cifrar volúmenes LVM

En nuestro RAID1 #1:
- Configuramos el gestor de volúmenes físicos (LVM).
- Creamos tres volúmenes: `swap`, `home` y `root`.
- Luego, ciframos cada volumen.

<p align="center">
  <img width="600" src="https://github.com/user-attachments/assets/f4ee05f0-ac7c-445d-9650-f3a30cb2333f" alt="Volúmenes físicos">
</p>

---

### Paso 3: Montaje de volúmenes

Montamos los volúmenes cifrados:
- `/home`
- Área de intercambio (`swap`)
- `/` raíz del sistema

<p align="center">
  <img width="600" src="https://github.com/user-attachments/assets/5a173595-b757-4219-932f-dc8dd37759c7" alt="Montaje de volúmenes">
</p>

---

### Resultado final

Así queda el esquema de particionado y montaje:

<p align="center">
  <img width="800" src="https://github.com/user-attachments/assets/08a73a8e-1fd4-4b00-917d-b8d2655b7da1" alt="Esquema final particionado">
</p>

</details>
