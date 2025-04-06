# 📝 CRUD de Mensajes con JSP, MySQL y Maven

Este proyecto es una aplicacion web simple desarrollada con **JSP**, **Servlets**, **MySQL** y **Maven**. Permite realizar operaciones **CRUD** (Crear, Leer, Actualizar y Eliminar) sobre mensajes almacenados en una base de datos MySQL. Permite crear, visualizar, editar y eliminar mensajes. Proyecto estructurado con Maven y con diseño responsivo usando Bootstrap.

---

## 🚀 Tecnologías utilizadas

- Java 8+
- JSP (JavaServer Pages)
- Servlets
- Maven
- MySQL
- Bootstrap 5
- Apache Tomcat 9+

---

## 🖼️ Capturas de Pantalla

### 📋 Vista Principal
Muestra la lista de mensajes con las opciones de editar o eliminar:  
![image](https://github.com/user-attachments/assets/576efad0-393f-4042-8847-dcc318fae3d7)
![image](https://github.com/user-attachments/assets/8a02c1bd-4c3e-4941-9da0-84f8af496757)
![image](https://github.com/user-attachments/assets/194d086b-04e2-44c1-9645-f6d0d1ec1023)




---

### ✏️ Formulario de Edición
Cuando se da clic en "Editar" en el mensaje creado por JUAAAN2:  
![image](https://github.com/user-attachments/assets/827b9e25-cd53-4c85-b5ce-b3c70a1e48bf)



---


## ⚙️ Cómo ejecutar el proyecto

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/NombreDelRepo.git
   ```

2. Abre el proyecto en tu IDE (recomendado: NetBeans o IntelliJ con soporte Maven).

3. Asegúrate de tener MySQL corriendo y crea una base de datos llamada `mensaje_db`.

4. Ejecuta el siguiente script SQL para crear la tabla:
   ```sql
CREATE DATABASE mensajes_db;
CREATE TABLE mensajes_db.mensajes(
	id_mensaje INT NOT NULL AUTO_INCREMENT,
    /*
  seleccionamos la db (mensajes_db) y ponemos el nombre de la taba (mensajes)*/
    mensaje VARCHAR(280) NOT NULL,
	autor_mensaje VARCHAR(45) NOT NULL,
    fecha_creacion datetime NOT NULL,
    PRIMARY KEY (id_mensaje)
);
   ```

5. Configura las credenciales de tu base de datos en el archivo `Conexion.java`.

6. Ejecuta el proyecto con Tomcat y accede a:
   ```
   http://localhost:8080/Mensajes/
   ```

---

## 🧩 Estructura del Proyecto

```
Mensajes/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/mensajesapp/
│   │   │       ├── Conexion.java
│   │   │       ├── Mensajes.java
│   │   │       ├── MensajesDAO.java
│   │   │       └── MensajesService.java
│   │   └── webapp/
│   │       ├── index.jsp
│   │       ├── editar.jsp
│   │       └── eliminar.jsp
├── pom.xml
```

---

## 💡 Fragmento destacado

```jsp
<div class="d-flex gap-2">
    <a href="editar.jsp?id=<%=mensaje.getId()%>&mensaje=<%=mensaje.getMensaje()%>&autor=<%=mensaje.getAutor()%>" 
       class="btn btn-outline-primary btn-sm">
       Editar
    </a>
    <a href="eliminar.jsp?id=<%=mensaje.getId()%>" class="btn btn-outline-danger btn-sm">
       Eliminar
    </a>
</div>
```

---

## 🧠 Aprendizajes

- Conexión y uso de base de datos MySQL desde Java
- CRUD con JSP y Servlets
- Uso de Maven para gestión de dependencias
- Integración de Bootstrap en aplicaciones web Java

---

## 👨‍💻 Autor

**Juan Diego Suárez Barberan**  
📧 juandisuarez87@hotmail.com  
🎓 Escuela Politécnica Nacional  
🔗 [LinkedIn](https://www.linkedin.com/in/suarezjuandb)

---

## 📌 Nota

Este proyecto forma parte del curso de Java que estoy desarrollando en GitHub: [CursoJava](https://github.com/juansuarezb/CursoJava). Para fines de presentación, este proyecto se publica en un repositorio separado.
