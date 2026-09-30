# ProyectoPPI

# Sistema de reservas de tours — The Medellin Flavor

Sistema web para centralizar la gestión de tours, salidas programadas, guías, vehículos, reservas y reseñas de la agencia **The Medellin Flavor**.

## 📌 Información del proyecto

Proyecto académico desarrollado en conjunto con la agencia de tours privados **The Medellin Flavor** (Medellín, Antioquia), una agencia real que ofrece tours privados por:

- Medellín
- Guatapé
- Fincas de café
- Fincas de cacao

La agencia trabaja con guías bilingües (español/inglés) y vehículos propios (camionetas y buses, según la cantidad de personas).

## 🛠️ Tecnologías

| Capa | Tecnología |
|------|------------|
| Base de datos | MySQL |
| Backend | .NET Core |

## ❗ Descripción del problema

Actualmente, The Medellin Flavor gestiona sus tours, reservas, guías y vehículos de forma manual (mensajes, hojas de cálculo, WhatsApp), lo que genera varios problemas:

- Dificultad para controlar el cupo disponible de cada salida programada.
- No hay un registro centralizado de qué guía y qué vehículo está asignado a cada tour.
- No existe trazabilidad del historial de estados de una reserva (pendiente, confirmada, cancelada, completada).
- Las reseñas y calificaciones de los clientes no quedan vinculadas directamente a una reserva real, lo que dificulta verificar que provienen de un cliente que sí tomó el tour.

Esto hace necesario desarrollar un sistema web que centralice la gestión de tours, guías, vehículos, reservas y reseñas de la agencia.

## 🎯 Objetivos

### Objetivo general

Desarrollar un sistema web de reservas de tours para la agencia The Medellin Flavor, que permita gestionar el catálogo de tours, las salidas programadas, los guías, los vehículos y las reservas de los clientes.

### Objetivos específicos

- Diseñar y construir una base de datos relacional en **MySQL** que modele correctamente el negocio de la agencia (tours, destinos, idiomas, guías, vehículos, salidas programadas, reservas y reseñas).
- Desarrollar el backend del sistema en **.NET Core**, exponiendo la lógica de negocio necesaria para gestionar tours, reservas y usuarios.
- Permitir a los clientes consultar el catálogo de tours disponibles, realizar reservas y dejar reseñas de su experiencia.
- Permitir a los administradores gestionar el catálogo de tours, asignar guías y vehículos a cada salida, y responder las reseñas de los clientes.
- Registrar el historial de cambios de estado de cada reserva, para tener trazabilidad completa del proceso.

## 📦 Alcance

- **Usuarios y roles:** gestión de usuarios con roles de Cliente, Guía y Administrador.
- **Catálogo:** tours, categorías y destinos (un tour puede incluir varias paradas).
- **Guías:** gestión de guías y los idiomas que hablan.
- **Vehículos:** gestión de vehículos (camioneta o bus, según la capacidad requerida).
- **Salidas programadas:** programación de salidas de tours, con control de cupos disponibles.
- **Reservas:** reservas de clientes sobre una salida específica, con historial de cambios de estado.
- **Reseñas:** reseñas de clientes asociadas a una reserva real.

### Estados de una reserva

`Pendiente` → `Confirmada` → `Completada`
`Pendiente` / `Confirmada` → `Cancelada`

### Fuera de alcance

- No se incluye un módulo de pagos en línea.
- Los precios de los tours se manejan en dólares (**USD**) y pesos colombianos (**COP**).
