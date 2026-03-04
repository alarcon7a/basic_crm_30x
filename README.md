# Basic CRM 30x

Este repositorio es un ejemplo base de CRM para el programa **30x Hardcore AI**.

Está construido con:
- Next.js (App Router)
- TypeScript
- Prisma + PostgreSQL
- NeonDB como base de datos en la nube

## Funcionalidades incluidas

- Dashboard con métricas básicas
- Gestión de clientes (crear, editar, eliminar, listar)
- Registro de interacciones por cliente
- Endpoints API para clientes, interacciones y estadísticas

## Requisitos

- Node.js 20+
- npm
- Cuenta en Neon: https://neon.tech

## Configuración local

1. Instalar dependencias:

```bash
npm install
```

2. Crear archivo de entorno desde la plantilla:

```bash
cp .env.example .env
```

3. Completar variables en `.env`:

```env
DATABASE_URL="postgresql://USUARIO:PASSWORD@HOST/neondb?sslmode=require"
NEXT_PUBLIC_BASE_URL="http://localhost:3000"
```

4. Levantar el proyecto:

```bash
npm run dev
```

5. Abrir en el navegador:

`http://localhost:3000`

## Cómo crear una base de datos en NeonDB

1. Entra a https://console.neon.tech e inicia sesión.
2. Crea un nuevo proyecto (`New Project`).
3. Elige nombre del proyecto, región y versión de PostgreSQL.
4. Una vez creado, entra a la sección de conexión (`Connection Details`).
5. Copia la cadena de conexión (`Connection string`) en formato `postgresql://...`.
6. Pega esa cadena en `DATABASE_URL` dentro de tu `.env`.
7. Verifica que la URL tenga `sslmode=require`.

## Scripts

- `npm run dev`: entorno local
- `npm run build`: build de producción
- `npm run start`: correr build
- `npm run lint`: linting

## Notas

- Este proyecto está pensado como base educativa/rápida para pruebas de CRM dentro del programa 30x Hardcore AI.
- Si agregas o cambias modelos de Prisma, recuerda sincronizar schema/migraciones antes de desplegar.
