# 📚 PMA Blog de Aprendizaje - Backend

## 📖 Descripción

Este es el backend del Blog de Aprendizaje desarrollado como parte del Plan de Mejoramiento Aplicado (PMA). 

La aplicación proporciona una API RESTful robusta y segura para gestionar publicaciones académicas, permitiendo crear, leer, actualizar y eliminar contenido educativo con funcionalidades avanzadas como:

- ✅ Gestión completa de publicaciones académicas
- ✅ Sistema de comentarios interactivo
- ✅ Carga y gestión de imágenes
- ✅ Validación de datos y manejo de errores
- ✅ Rate limiting para seguridad
- ✅ CORS configurado para desarrollo
- ✅ Base de datos MongoDB con Mongoose

## 🚀 Tecnologías Utilizadas

- **Node.js** - Entorno de ejecución
- **Express.js** - Framework web
- **MongoDB** - Base de datos NoSQL
- **Mongoose** - ODM para MongoDB
- **Multer** - Manejo de archivos
- **Helmet** - Seguridad HTTP
- **CORS** - Cross-Origin Resource Sharing
- **Morgan** - Logging de requests
- **Express Validator** - Validación de datos
- **Express Rate Limit** - Limitación de requests

## 📋 Requisitos Previos

- Node.js (v16 o superior)
- MongoDB (local o remoto)
- npm o yarn

## ⚙️ Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/Elux-2021572/backend_EduExpanse.git
   cd backend_EduExpanse
   ```

2. **Instalar dependencias**
   ```bash
   npm install
   ```

3. **Configurar variables de entorno**
   ```bash
   cp .env.example .env
   ```
   Editar el archivo `.env` con tus configuraciones:
   - `URI_MONGO`: Cadena de conexión a MongoDB
   - `PORT`: Puerto del servidor (por defecto 3000)
   - `CORS_ORIGIN`: Orígenes permitidos para CORS

4. **Iniciar MongoDB**
   Asegúrate de que MongoDB esté ejecutándose

## 🏃‍♂️ Ejecución

### Desarrollo
```bash
npm run dev
```

### Producción
```bash
npm start
```

## 📁 Estructura del Proyecto

```
├── configs/
│   ├── data/
│   │   ├── blog.publications.json
│   │   └── Blog.postman_collection.json
│   ├── mongo.js
│   └── server.js
├── public/
│   └── uploads/
│       └── publications/
├── src/
│   ├── middlewares/
│   │   ├── delete-file-on-error.js
│   │   ├── handle-errors.js
│   │   ├── multer-uploads.js
│   │   ├── publication-validator.js
│   │   ├── rate-limit-validator.js
│   │   └── validate-fields.js
│   └── publications/
│       ├── publication.controller.js
│       ├── publication.model.js
│       └── publication.routes.js
├── .env.example
├── .gitignore
├── index.js
├── package.json
└── README.md
```

## 🛠️ API Endpoints

### Publicaciones

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| GET | `/blog/v1/publication` | Obtener todas las publicaciones |
| GET | `/blog/v1/publication/:id` | Obtener publicación por ID |
| POST | `/blog/v1/publication` | Crear nueva publicación |
| PUT | `/blog/v1/publication/:id` | Actualizar publicación |
| DELETE | `/blog/v1/publication/:id` | Eliminar publicación |
| POST | `/blog/v1/publication/:id/comment` | Agregar comentario |

## 🔧 Configuración de Desarrollo

### Variables de Entorno

| Variable | Descripción | Valor por Defecto |
|----------|-------------|-------------------|
| `PORT` | Puerto del servidor | 3000 |
| `NODE_ENV` | Entorno de ejecución | development |
| `URI_MONGO` | URI de MongoDB | mongodb://localhost:27017/blog_aprendizaje |
| `CORS_ORIGIN` | Orígenes permitidos para CORS | http://localhost:5173 |

## 🛡️ Seguridad

- **Helmet**: Configuración de headers de seguridad HTTP
- **Rate Limiting**: Limitación de requests por IP
- **CORS**: Configurado para orígenes específicos
- **Validación de datos**: Validación completa de inputs
- **Manejo de errores**: Sistema robusto de manejo de errores

## 📝 Licencia

Este proyecto está bajo la Licencia ISC.

## 👥 Contribución

Este es un proyecto académico desarrollado como parte del PMA. Para contribuciones:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📞 Contacto

**Desarrollador**: Emilio Lux
**Email**: emiliojo.lux@gmail.com
**Proyecto**: [https://github.com/Elux-2021572/backend_EduExpanse](https://github.com/Elux-2021572/backend_EduExpanse)
