# ☕ Cafetería SakuraCoffee 
### Sistema de Pedidos Digitales con Código QR — Backend + Frontend

Este repositorio contiene el sistema completo de gestión y pedidos para la **Cafetería Latacunga**, incluyendo:

- 🟦 Backend en Node.js (Express + Prisma + JWT + Socket.io)  
- 🟪 Frontend en Next.js (TailwindCSS + Axios + WebSockets)  
- 🗄 Base de datos PostgreSQL  
- 📡 Actualizaciones en tiempo real  
- 🔐 Autenticación basada en tokens  

---

## 📦 Tecnologías principales

### **Backend**
- Node.js + Express  
- Prisma ORM  
- PostgreSQL  
- JWT  
- Bcrypt  
- Socket.io  
- Helmet + CORS  

### **Frontend**
- Next.js  
- React  
- TailwindCSS  
- Axios  
- Socket.io Client  
- React Hook Form  
- React Hot Toast  

---

## 🪟 Instalación en Windows

---

# 📁 1. Crear estructura del proyecto

```bash
mkdir cafeteria-latacunga
cd cafeteria-latacunga
```
## Backend
```
mkdir backend
cd backend
mkdir src prisma
cd src
mkdir controllers middlewares routes socket utils config
cd ../..
```
##Fronend
```
mkdir frontend
```
# 🔧 2. Instalación del Backend
## Entrar al backend
```
cd backend
npm init -y
npm install express cors dotenv @prisma/client jsonwebtoken bcrypt socket.io express-validator cookie-parser helmet morgan
npm install -D nodemon prisma
```
## Scripts del backend (package.json)
```
"scripts": {
  "dev": "nodemon src/app.js",
  "start": "node src/app.js",
  "prisma:studio": "prisma studio",
  "prisma:migrate": "prisma migrate dev",
  "prisma:generate": "prisma generate",
  "prisma:seed": "node prisma/seed.js"
}

```
## En CMD, desde la carpeta backend:
```
echo DATABASE_URL="postgresql://postgres:password@localhost:5432/cafeteria_db" > .env
echo PORT=5000 >> .env
echo NODE_ENV=development >> .env
echo JWT_SECRET=tu_clave_secreta_super_segura_cambiar_en_produccion_123456 >> .env
echo JWT_EXPIRES_IN=7d >> .env
echo FRONTEND_URL=http://localhost:3000 >> .env
```

## Crear archivo .gitignore
```
echo node_modules/ > .gitignore
echo .env >> .gitignore
echo dist/ >> .gitignore
echo build/ >> .gitignore
echo *.log >> .gitignore
echo .DS_Store >> .gitignore
```
## Inicializar Prisma:
```
npx prisma init
```
##  Configurar el FRONTEND
```
cd ..
cd frontend
```
## Crear el proyecto Next.js
```
npx create-next-app@latest .
```

Te va a hacer varias preguntas, **responde así:**
```
√ Would you like to use TypeScript? » No
√ Would you like to use ESLint? » Yes
√ Would you like to use Tailwind CSS? » Yes
√ Would you like to use `src/` directory? » No
√ Would you like to use App Router? » No
√ Would you like to customize the default import alias (@/*)? » No
```
## Instalar dependencias adicionales:
```
npm install axios socket.io-client @headlessui/react @heroicons/react react-hook-form react-hot-toast qrcode.react date-fns
```
## Crear archivo .env.local:
```
echo NEXT_PUBLIC_API_URL=http://localhost:5000 > .env.local
echo NEXT_PUBLIC_SOCKET_URL=http://localhost:5000 >> .env.local
echo NEXT_PUBLIC_CAFETERIA_NAME=Cafetería Latacunga >> .env.local
echo NEXT_PUBLIC_CAFETERIA_ADDRESS=Centro de Latacunga >> .env.local
```
## Crear carpetas adicionales
```
mkdir utils
mkdir hooks
mkdir contexts
mkdir components\layout
mkdir components\ui
mkdir public\images
```







