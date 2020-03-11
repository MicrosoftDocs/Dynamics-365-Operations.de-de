---
title: Überblick über die Dual-Write-Funktion
description: Dieses Thema bietet einen Überblick über Dual-Write. Dual-Write ist eine Infrastruktur, die eine Interaktion zwischen Microsoft Dynamics 365 modellgesteuerten Anwendungen und Finance and Operations Anwendungen nahezu in Echtzeit ermöglicht.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075985"
---
# <a name="dual-write-overview"></a>Dual-Write-Übersicht

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a>Was ist Dual-Write?

Dual-Write ist eine Out-of-Box-Infrastruktur, die eine nahezu Echtzeit-Interaktion zwischen modellgesteuerten Anwendungen in Microsoft Dynamics 365 und Finance and Operations Anwendungen ermöglicht. Wenn Daten über Kunden, Produkte, Personen und Abläufe über Anwendungsgrenzen hinweg fließen, werden alle Abteilungen eines Unternehmens in die Lage versetzt, diese Daten zu nutzen.

Dual-Write bietet eine eng gekoppelte, bidirektionale Integration zwischen Finance and Operations Anwendungen und Common Data Service Anwendungen. Jede Datenänderung in Finance and Operations Anwendungen führt zu Schreibvorgängen in Common Data Service, und jede Datenänderung in Common Data Service führt zu Schreibvorgängen in Finance and Operations Anwendungen. Dieser automatisierte Datenfluss bietet eine integrierte Benutzererfahrung über die Anwendungen hinweg.

![Datenbeziehung zwischen Anwendungen](media/dual-write-overview.jpg)

Dual-Write hat zwei Aspekte: einen *Infrastruktur* Aspekt und einen *Anwendung* Aspekt.

### <a name="infrastructure"></a>Infrastruktur

Die Dual-Write-Infrastruktur ist erweiterbar und zuverlässig und umfasst die folgenden Hauptmerkmale:

+ Synchroner und bidirektionaler Datenfluss zwischen Anwendungen
+ Synchronisierung zusammen mit Spiel-, Pausen- und Aufholmodi zur Unterstützung des Systems im Online- und Offline-/Asynchronmodus.
+ Fähigkeit zur Synchronisierung der Anfangsdaten zwischen den Anwendungen
+ Konsolidierte Ansicht der Aktivitäts- und Fehlerprotokolle für Datenadministratoren
+ Möglichkeit, benutzerdefinierte Benachrichtigungen und Schwellenwerte zu konfigurieren und Benachrichtigungen zu abonnieren
+ Intuitive Benutzeroberfläche (UI) für Filterung und Transformationen
+ Fähigkeit, Abhängigkeiten und Beziehungen zwischen den Entitäten festzulegen und anzuzeigen
+ Erweiterbarkeit sowohl für Standard- als auch für benutzerdefinierte Entitäten und Karten
+ Zuverlässige Verwaltung des Lebenszyklus von Anwendungen
+ Out-of-Box-Einrichtungserfahrung für neue Kunden

### <a name="application"></a>Bewerbung

Dual-Write erstellt eine Zuordnung zwischen Konzepten in Finance and Operations-Apps und Konzepten in modellgesteuerten Anwendungen in Dynamics 365. Diese Integration unterstützt die folgenden Szenarien:

+ Integrierte Masterdaten von Debitoren
+ Zugang zu Kundenkarten und Belohnungspunkten
+ Einheitliche Produktbeherrschung
+ Bewusstsein für die Organisationshierarchie
+ Integrierte Masterdaten von Kreditoren
+ Zugang zu Finanz- und Steuerdaten
+ Erfahrung mit Bedarfspreismodulen
+ Integrierte Prospect-to-Cash-Erfahrung
+ Fähigkeit, sowohl interne Anlagen als auch Kundenanlagen durch Außendienstmitarbeiter zu bedienen
+ Integrierte Procure-to-Pay-Erfahrung
+ Integrierte Aktivitäten und Notizen für Kundendaten und Dokumente
+ Fähigkeit, die Verfügbarkeit und die Details der Bestände aus dem Lagerbestand nachzuschlagen
+ Projekt-zu-Bargeld-Erfahrung
+ Fähigkeit zur Handhabung mehrerer Adressen und Rollen durch das Parteikonzept
+ Verwaltung einer einzigen Quelle für Benutzer
+ Integrierte Kanäle für Retail und Marketing
+ Sichtbarkeit von Werbeaktionen und Rabatten
+ Anfrage für Service-Funktionen
+ Rationalisierte Serviceabläufe

## <a name="top-reasons-to-use-dual-write"></a>Die wichtigsten Gründe für die Verwendung von Dual-Write

Dual-Write bietet Datenintegration über Microsoft Dynamics 365 Apps hinweg. Dieser robuste Rahmen verbindet Umgebungen und ermöglicht die Zusammenarbeit verschiedener Geschäftsanwendungen. Hier sind die wichtigsten Gründe, warum Sie Dual-Write verwenden sollten:

+ Dual-Write bietet eine eng gekoppelte, echtzeitnahe und bidirektionale Integration zwischen Finance and Operations-Anwendungen und modellgesteuerten Anwendungen in Dynamics 365. Diese Integration macht Microsoft Dynamics 365 zum One-Stop-Shop für alle Ihre Geschäftslösungen. Kunden, die Dynamics 365 Finance und Dynamics 365 Supply Chain Management verwenden, aber für das Kundenbeziehungsmanagement (CRM) Nicht-Microsoft-Lösungen einsetzen, entscheiden sich für Dynamics 365 wegen der Unterstützung von Dual-Write.
+ Daten von Kunden, Produkten, Operationen, Projekten und dem Internet der Dinge (Internet of Things, IoT) fließen automatisch durch Dual-Write zu Common Data Service. Diese Verbindung ist sehr nützlich für Unternehmen, die an Microsoft Power Platform-Erweiterungen interessiert sind.
+ Die Dual-Write-Infrastruktur folgt dem No-Code/Low-Code-Prinzip. Es ist nur ein minimaler technischer Aufwand erforderlich, um die Standard-Tabelle-zu-Tabelle-Zuordnungen zu erweitern und um benutzerdefinierte Zuordnungen aufzunehmen.
+ Dual-Write unterstützt sowohl den Online- als auch den Offline-Modus. Microsoft ist das einzige Unternehmen, das Unterstützung für den Online- und Offline-Modus bietet.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Was bedeutet Dual-Write für Benutzer und Architekten von CRM-Produkten?

Dual-Write automatisiert den Datenfluss zwischen Finance and Operations Anwendungen und Common Data Service Anwendungen. In zukünftigen Versionen werden Konzepte in modellgesteuerten Anwendungen in Dynamics 365 (z.B. Kunde, Kontakt, Angebot und Bestellung) auf Kunden des mittleren und oberen Mittelstands skaliert.

In der ersten Version wird der größte Teil der Automatisierung durch Dual-Write-Lösungen abgewickelt. In zukünftigen Versionen werden diese Lösungen Teil von Common Data Service werden. Wenn Sie die bevorstehenden Änderungen an Common Data Service verstehen, können Sie sich langfristig Aufwand sparen. Hier sind einige der entscheidenden Änderungen:

+ Common Data Service wird neue Konzepte haben, wie z.B. Firma und Partei. Diese Konzepte werden alle Anwendungen betreffen, die auf Common Data Service aufbauen, wie z.B. Dynamics 365 Marketing, Dynamics 365 Sales, Dynamics 365 Customer Service und Dynamics 365 Field Service.
+ Aktivitäten und Notizen werden vereinheitlicht und erweitert, um sowohl die C1 (Benutzer des Systems) als auch die C2 (Kunden des Systems) zu unterstützen.
+ Hier sind einige der bevorstehenden Änderungen in Common Data Service:

    - Der dezimale Datentyp wird den Gelddatentyp ersetzen.
    - Die Datumsgültigkeit wird vergangene, gegenwärtige und zukünftige Daten an der gleichen Stelle unterstützen.
    - Es wird mehr Unterstützung für Währung und Wechselkurse geben, und die **Wechselkurs** Programmierschnittstelle (API) wird überarbeitet.
    - Einheitenumrechnungen werden unterstützt.

Weitere Informationen über bevorstehende Änderungen finden Sie unter [Daten in Common Data Service - Phase 1 unf 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).
