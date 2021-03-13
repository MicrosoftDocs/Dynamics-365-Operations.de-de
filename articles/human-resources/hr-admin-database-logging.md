---
title: Datenbankprotokollierung konfigurieren und verwalten
description: Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen.
author: andreabichsel
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 50346cc495fe08f49137dba59dbcbb3f7f838c7b
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129278"
---
# <a name="configure-and-manage-database-logging"></a>Datenbankprotokollierung konfigurieren und verwalten

Sie können Änderungen an Tabellen und Feldern in Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen. In diesem Thema wird beschrieben, wie:

- Verwalten Sie Sicherheit und Leistung für die Datenbankprotokollierung
- Datenbankprotokollierung einrichten
- Bereinigen Sie Datenbankprotokolle

## <a name="overview-of-database-logging"></a>Übersicht über die Datenbankprotokollierung

Sie können Änderungen an Tabellen und Feldern in Microsoft Dynamics 365 Human Resources mit Datenbankprotokollierung verfolgen. Diese Änderungen umfassen das Einfügen, Aktualisieren oder Löschen. Die Datenbankprotokollierung speichert eine Aufzeichnung der Änderungen an Tabellen oder Feldern in der Datenbankprotokolltabelle.

Die geschäftlichen Verwendungen der Datenbankprotokollierung umfassen:

- Erstellen eines Überwachungsdatensatzes mit Änderungen an bestimmten Tabellen, die vertrauliche Informationen enthalten.
- Verfolgung einzelner Transaktionen. Die Datenbankprotokollierung dient nicht zur Verfolgung automatisierter Transaktionen, die in Stapeljobs ausgeführt werden.

## <a name="security-for-database-logging"></a>Sicherheit für die Datenbankprotokollierung

Datenbankprotokolle können sensible Daten enthalten. Beschränken Sie den Zugriff auf Sicherheitsrollen, die Zugriff auf die Protokolldaten benötigen.

## <a name="database-logging-and-performance"></a>Datenbankprotokollierung und Leistung

Die Datenbankprotokollierung kann zwar aus geschäftlicher Sicht hilfreich sein, sie kann allerdings auch eine hohe Ressourcenauslastung sowie einen hohen Verwaltungsaufwand bedeuten. Die Leistungsbeeinträchtigungen der Datenbankprotokollierung umfassen:

- Die Datenbankprotokolltabelle kann schnell wachsen und die Größe der Datenbank erhöhen. Das Wachstum hängt von der Menge der protokollierten Daten ab, die Sie behalten möchten. Standardmäßig verwaltet die Datenbankprotokolltabelle nur 30 Tage Protokolldaten. 

- Die Datenbankprotokollierung kann sich nachteilig auf lang laufende automatisierte Prozesse auswirken, z. B. auf lang laufende Datenimporte.

### <a name="best-practices"></a>Optimale Verfahren

Wählen Sie zum Eingrenzen der Anzahl von Protokolleinträgen und zur Steigerung der Leistung nur die jeweils gewünschten Felder für die Protokollierung und keine vollständigen Tabellen aus. Um die Gesamtleistung aufrechtzuerhalten, ist die Datenbankprotokollierung auf 20 Tabellen beschränkt.

> [!NOTE]
> Für einzelne Feldern können nur Aktualisierungen protokolliert werden.

## <a name="set-up-database-logging"></a>Datenbankprotokollierung einrichten

Sie können den Assistent **Protokollieren von Datenbankänderungen** zum Einrichten der Datenbankprotokollierung verwenden. Der Assistent bietet eine flexible Möglichkeit, die Protokollierung für Tabellen oder Felder einzurichten.

1. Gehen Sie zu **Systemadministration> Links> Datenbank> Datenbankprotokoll einrichten**. Wählen Sie **Neu** aus, um den Assistent **Protokollieren von Datenbankänderungen** zu starten.
2. Schließen Sie den Assistenten ab.

## <a name="clean-up-database-logs"></a>Bereinigen Sie Datenbankprotokolle

Sie können alle oder einen Teil der Datenbankprotokolle mit den folgenden Optionen löschen:

- Wählen Sie alle Protokolle für eine bestimmte Tabelle aus.
- Wählen Sie bestimmte Arten von Datenbankprotokollen aus.
- Wählen Sie ein Datum und eine Uhrzeit aus, zu der ein Protokoll erstellt wurde.

Gehen Sie zum Einrichten der Datenbankprotokoll-Bereinigung folgendermaßen vor: 

1. Gehen Sie zu **Systemadministration> Links > Datenbank > Datenbankprotokoll einrichten**. Wählen Sie **Protokoll bereinigen**.

2. Wählen Sie eine Methode zum Auswählen der zu löschenden Protokolle aus, indem Sie eine der folgenden Optionen eingeben:

   - Tabellenkennung (ID)
   - Art des Protokolls
   - Erstellungsdatum und -uhrzeit

3. Verwenden Sie die **Bereinigung des Datenbankprotokolls** Registerkarte, um festzulegen, wann die Protokollbereinigungsaufgabe ausgeführt werden soll. Standardmäßig sind Datenbankprotokolle 30 Tage lang verfügbar.
