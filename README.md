# OpenClaw-AI-Lab

Dieses Projekt dokumentiert den Aufbau einer lokal betriebenen KI-Assistenten-Umgebung auf Basis meines bestehenden Home-Server-/Security-Labs. Ziel ist es, praktische Kenntnisse in Linux, Self-Hosting, API-Integration, Messaging-Systemen und IT-Sicherheit aufzubauen und besser zu verstehen, wie sich KI-Systeme kontrolliert und sicher in eine bestehende Infrastruktur einbinden lassen.

## Ziele des Projekts

- Aufbau eines lokal betriebenen KI-Assistenten
- Erweiterung einer bestehenden Server-Umgebung um eine Assistenzschicht
- praktische Integration externer APIs und Kommunikationskanäle
- Analyse von Berechtigungen, Tool-Zugriffen und Sicherheitsgrenzen
- Untersuchung, wie sich KI-Funktionalität sicher in reale Systeme einfügen lässt

## Bestandteile des Projekts

- lokal betriebene Assistenz-Plattform mit OpenClaw
- Telegram-Anbindung über einen separaten Bot
- Workspace- und Memory-Struktur für den Assistenten
- Konfiguration von Verhalten, Rollenbild und Arbeitskontext
- Festlegung von Arbeitsregeln und Sicherheitsgrenzen für den Assistenten
- API-Nutzung für Kommunikation, Suche und KI-Funktionen
- erste Tests mit TTS- und Sprachfunktionen

## Verwendete Technologien

- Ubuntu Server
- OpenClaw
- Docker
- NGINX
- Telegram Bot API
- Brave Search API
- OpenAI API
- lokale Port- und Service-Analyse

## Projektstruktur / technische Umsetzung

Das Projekt baut auf meiner bereits bestehenden Home-Server-Umgebung auf und ergänzt diese um eine lokal laufende KI-Assistenzschicht.

Vorhandene Infrastruktur aus dem Server-Lab:

- Website (Port 8080)
- App (Port 8081)
- Reverse Proxy (Port 80)
- Portainer UI (Port 9000)

Erweiterung durch das KI-Projekt:

- OpenClaw Gateway lokal auf Loopback
- OpenClaw Control UI lokal verfügbar
- Telegram-Bot als externer Kommunikationskanal
- eigener Workspace mit Memory-Dateien und Konfigurationsstruktur
- Assistent mit eigener Identität: **Delamain**

## API-Integration

Im Rahmen des Projekts wurden mehrere externe APIs praktisch eingebunden, um Kommunikations-, Such- und KI-Funktionen mit der lokalen Umgebung zu verbinden.

- **Telegram Bot API** zur Anbindung des Assistenten an einen externen Messaging-Kanal
- **Brave Search API** zur Nutzung externer Suchfunktionen innerhalb der Assistenzumgebung
- **OpenAI API** zur Einbindung von KI-Funktionen in die Assistenz-Plattform

## Sicherheitsaspekte

Ein zentraler Fokus des Projekts liegt nicht nur auf der Funktionalität, sondern auf der sicheren Einbettung eines KI-Assistenten in eine bestehende technische Umgebung.

Ein wichtiger Teil des Projekts bestand von Anfang an darin, den Assistenten nicht nur funktional einzurichten, sondern ihn kontrolliert in die Umgebung einzubetten. Dazu wurden klare Arbeitsregeln definiert, Berechtigungen bewusst eingegrenzt und für sicherheitsrelevante, externe oder potenziell riskante Änderungen ein explizites Freigabeprinzip festgelegt.

Bearbeitete bzw. beobachtete Themen:

- Trennung zwischen lokalem Systemzugriff und externer Kommunikation
- Bewertung offen erreichbarer Ports und Admin-Oberflächen
- Analyse von Service-Exposure im Zusammenspiel mit Docker und Reverse Proxy
- sichere Nutzung eines separaten Telegram-Bots statt persönlicher Messenger-Identität
- Betrachtung von Berechtigungen, Tool-Zugriffen und Assistenzgrenzen
- definierte Arbeitsregeln für den lokalen Assistenten
- Freigabeprinzip für sicherheitsrelevante oder externe Änderungen
- bewusste Begrenzung autonomer Eingriffe in produktionsnahe oder riskante Bereiche
- Einordnung von KI nicht nur als Funktionsschicht, sondern auch als zusätzlicher Sicherheits- und Architekturbaustein

## Aktueller Stand

- OpenClaw lokal eingerichtet und betriebsbereit
- Telegram-Anbindung erfolgreich umgesetzt
- Workspace, Memory und Assistenzverhalten konfiguriert
- API-Integrationen praktisch genutzt
- erste Sprach- und TTS-Experimente durchgeführt
- System- und Sicherheitsprüfung der Umgebung begonnen

## Erkenntnisse / Learnings

- Eine lokal betriebene KI ist nicht nur ein KI-Thema, sondern auch ein Infrastruktur- und Security-Thema.
- Messaging, Speicherlogik, Tools und Berechtigungen müssen genauso sauber gedacht werden wie klassische Serverdienste.
- Alte Hardware reicht aus, um sowohl Server- als auch KI-Workloads in einer praxisnahen Lernumgebung zu testen.
- Ein selbst gehosteter Assistent erweitert ein Homelab sinnvoll, wenn Sicherheit, Kontrolle und Zugriffskonzepte mitgedacht werden.
- API-Integrationen sind nicht nur funktional interessant, sondern auch sicherheitsrelevant, sobald externe Kommunikation und Systemzugriffe zusammenkommen.

## Geplante Erweiterungen

- weitere Absicherung der öffentlich erreichbaren Dienste
- bessere Trennung interner und externer Services
- Ausbau von Monitoring und Logging
- Optimierung der Sprachfunktionen
- weiterführende Automatisierung und Sicherheitsmechanismen
