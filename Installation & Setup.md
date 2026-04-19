# Installation / Setup

Diese Dokumentation beschreibt den grundlegenden Aufbau meiner lokal betriebenen KI-Assistenten-Umgebung. Das Projekt ist als praktisches Lern- und Entwicklungsprojekt angelegt und zeigt, wie sich ein KI-System kontrolliert in eine bestehende Server- und Security-Umgebung integrieren lässt.

## Voraussetzungen

Für den Aufbau der Umgebung wurden folgende Grundlagen genutzt:

- Ubuntu Server / Ubuntu Linux
- Docker
- bestehende Reverse-Proxy-Struktur mit NGINX
- lokale Server- bzw. Homelab-Umgebung
- OpenClaw als selbst gehostete Assistenz-Plattform
- ein separater Telegram-Bot für die externe Kommunikation
- API-Zugänge für externe Dienste

## Verwendete APIs

Im Rahmen des Projekts wurden mehrere externe APIs eingebunden:

- Telegram Bot API
- Brave Search API
- OpenAI API

## Ziel des Setups

Die KI-Assistenz wurde nicht isoliert aufgesetzt, sondern bewusst in eine bestehende technische Umgebung integriert. Dadurch stand nicht nur die Funktionalität im Fokus, sondern auch die Frage, wie sich ein Assistent sicher, kontrolliert und nachvollziehbar in reale Infrastruktur einfügen lässt.

## Grundaufbau

Die Umgebung basiert auf einer bereits vorhandenen Home-Server-Struktur, die um eine lokal laufende Assistenzschicht erweitert wurde.

Bereits vorhandene Komponenten:

- Website
- App
- Reverse Proxy
- Container-Umgebung
- erste Security- und Härtungsmaßnahmen

Erweiterung durch das KI-Projekt:

- lokale OpenClaw-Instanz
- lokale Web-Oberfläche / Control UI
- Telegram-Anbindung über separaten Bot
- Workspace-Struktur für Kontext, Regeln und Memory
- Integration externer APIs für Suche, Kommunikation und KI-Funktionen

## Setup-Schritte

### 1. Basisumgebung vorbereiten

Zunächst wurde eine Ubuntu-basierte Serverumgebung eingerichtet, die bereits als Home-Server- und Security-Lab genutzt wurde. In dieser Umgebung liefen bereits mehrere Services in Containern sowie ein Reverse Proxy.

### 2. OpenClaw lokal einrichten

Anschließend wurde OpenClaw als lokal betriebene Assistenz-Plattform integriert. Dabei wurden die grundlegenden Komponenten wie Gateway, lokale Oberfläche und Workspace-Struktur eingerichtet.

### 3. Assistenzkontext definieren

Ein wichtiger Teil des Setups war nicht nur die technische Installation, sondern auch die kontrollierte Einbettung des Assistenten in die Umgebung. Dazu gehörten:

- Definition eines klaren Rollenbilds
- Aufbau einer Workspace- und Memory-Struktur
- Festlegung von Arbeitsregeln
- bewusste Begrenzung von Rechten und Eingriffsmöglichkeiten
- Freigabeprinzip für sicherheitsrelevante, externe oder potenziell riskante Änderungen

### 4. Telegram als externer Kanal anbinden

Um den Assistenten auch außerhalb der lokalen Oberfläche nutzbar zu machen, wurde ein separater Telegram-Bot angebunden. Dadurch konnte die lokale Assistenzplattform kontrolliert mit einem externen Kommunikationskanal verbunden werden, ohne eine private Messenger-Identität direkt zu verwenden.

### 5. Externe APIs integrieren

Zur praktischen Erweiterung des Systems wurden mehrere APIs eingebunden:

- Telegram Bot API für den Messaging-Kanal
- Brave Search API für externe Suchfunktionen
- OpenAI API für zusätzliche KI-Funktionen

### 6. Sicherheitsprüfung des Setups

Da das Projekt an der Schnittstelle von KI und IT-Sicherheit liegt, war die Sicherheitsbetrachtung ein fester Bestandteil des Aufbaus. Dazu gehörten unter anderem:

- Prüfung öffentlich erreichbarer Dienste
- Bewertung offener Ports und Admin-Oberflächen
- Betrachtung von Berechtigungen und Tool-Zugriffen
- Analyse der Trennung zwischen lokalem Zugriff und externer Kommunikation
- Einschätzung der zusätzlichen Angriffsfläche durch API- und Messaging-Anbindung

## Charakter des Projekts

Dieses Setup ist nicht als fertiges Produkt gedacht, sondern als laufendes Praxisprojekt. Ziel ist es, technische Erfahrung in Linux, Self-Hosting, API-Integration, KI-naher Infrastruktur und Sicherheitsdenken aufzubauen und weiterzuentwickeln.
