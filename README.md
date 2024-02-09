# Event Management API

Welcome to the Event Management API documentation! This API is built using Laravel and is designed to help you manage
events and attendees seamlessly. Below, you'll find information on the key features, relationships, and functionalities
of this API.

## Table of Contents

1. [Features](#features)
2. [Relationships](#relationships)
3. [Notification](#notification)
4. [Background Queue](#background-queue)
5. [Authentication](#authentication)
6. [Authorization](#authorization)

## Features

- Users can register, login, and logout.
- Users can create and attend events.
- Event owners (users) can manage their own events.
- Attendees are users who are attending events.
- Email notification is sent to attendees 24 hours before the event.

## Relationships

- **Event-User Relationship:** Each event is associated with a user who is the owner of the event.
- **Event-Attendee Relationship:** Each event can have multiple attendees (users).
- **Attendee-User Relationship:** An attendee is a user going to an event.

## Notification

The application automatically notifies attendees about upcoming events within the next 24 hours via email.

## Background Queue

To efficiently handle the notification process, a custom command has been implemented to run the notification process as
a background queue. This ensures a seamless user experience and optimal performance.
