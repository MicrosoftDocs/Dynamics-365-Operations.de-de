---
title: Duales Schreiben – Übersicht
description: Dieser Artikel bietet einen Überblick über Dual-write, das eine Interaktion zwischen Customer-Engagement-Apps und Finanz- und Betriebs-Apps nahezu in Echtzeit ermöglicht.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 943607a3ef28db11b7bc7805257914117e6ae38c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289637"
---
# <a name="dual-write-overview"></a>Duales Schreiben – Übersicht

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Was ist Dual-Write?

Dual-write ist eine standardmäßige Infrastruktur, die eine Interaktion zwischen Customer-Engagement-Apps und Finance-and-Operations-Apps nahezu in Echtzeit ermöglicht. Wenn Daten über Kunden, Produkte, Personen und Abläufe über Anwendungsgrenzen hinweg fließen, werden alle Abteilungen eines Unternehmens in die Lage versetzt, diese Daten zu nutzen.

Dual-write bietet eine eng gekoppelte, bidirektionale Integration zwischen Finance- und Operations-Apps und Dataverse. Jede Datenänderung in Finanz- und Betriebs-Apps führt zu Schreibvorgängen in Dataverse, und jede Datenänderung in Dataverse führt zu Schreibvorgängen in Finanz- und Betriebs-Apps. Dieser automatisierte Datenfluss bietet eine integrierte Benutzererfahrung über die Anwendungen hinweg.

![Datenbeziehung zwischen Anwendungen.](media/dual-write-overview.jpg)

Dual-Write hat zwei Aspekte: einen *Infrastruktur* Aspekt und einen *Anwendung* Aspekt.

### <a name="infrastructure"></a>Infrastruktur

Die Dual-Write-Infrastruktur ist erweiterbar und zuverlässig und umfasst die folgenden Hauptmerkmale:

+ Synchroner und bidirektionaler Datenfluss zwischen Anwendungen
+ Synchronisierung zusammen mit Spiel-, Pausen- und Aufholmodi zur Unterstützung des Systems im Online- und Offline-/Asynchronmodus.
+ Fähigkeit zur Synchronisierung der Anfangsdaten zwischen den Anwendungen
+ Kombinierte Ansicht der Aktivitäts- und Fehlerprotokolle für Datenadministratoren
+ Möglichkeit, benutzerdefinierte Benachrichtigungen und Schwellenwerte zu konfigurieren und Benachrichtigungen zu abonnieren
+ Intuitive Benutzeroberfläche (UI) für Filterung und Transformationen
+ Fähigkeit, Abhängigkeiten und Beziehungen zwischen den Tabellen festzulegen und anzuzeigen
+ Erweiterbarkeit sowohl für Standard- als auch für benutzerdefinierte Tabellen und Karten
+ Zuverlässige Verwaltung des Lebenszyklus von Anwendungen
+ Out-of-Box-Einrichtungserfahrung für neue Kunden

### <a name="application"></a>Anwendung

Dual-write erstellt eine Zuordnung zwischen Konzepten in Finanz- und Betriebs-Apps und Konzepten in Customer-Engagement-Apps. Diese Integration unterstützt die folgenden Szenarien:

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


## <a name="top-reasons-to-use-dual-write"></a>Die wichtigsten Gründe für die Verwendung von Dual-Write

Dual-Write bietet Datenintegration über Microsoft Dynamics 365 Apps hinweg. Dieser robuste Rahmen verbindet Umgebungen und ermöglicht die Zusammenarbeit verschiedener Geschäftsanwendungen. Hier sind die wichtigsten Gründe, warum Sie Dual-Write verwenden sollten:

+ Duales Schreiben bietet eine eng gekoppelte, echtzeitnahe und bidirektionale Integration zwischen Finance and Opertions Apps und Kundenbindungsapps. Diese Integration macht Microsoft Dynamics 365 zum One-Stop-Shop für alle Ihre Geschäftslösungen. Kunden, die Dynamics 365 Finance und Dynamics 365 Supply Chain Management verwenden, aber für das Kundenbeziehungsmanagement (CRM) Nicht-Microsoft-Lösungen einsetzen, entscheiden sich für Dynamics 365 wegen der Unterstützung von dualem Schreiben (Dual-Write).
+ Daten von Kunden, Produkten, Operationen, Projekten und dem Internet der Dinge (Internet of Things, IoT) fließen automatisch durch Dual-Write zu Dataverse. Diese Verbindung ist nützlich für Unternehmen, die an Power Platform-Erweiterungen interessiert sind.
+ Die Dual-Write-Infrastruktur folgt dem No-Code/Low-Code-Prinzip. Es ist nur ein minimaler technischer Aufwand erforderlich, um die Standard-Tabelle-zu-Tabelle-Zuordnungen zu erweitern und um benutzerdefinierte Zuordnungen aufzunehmen.
+ Dual-Write unterstützt sowohl den Online- als auch den Offline-Modus. Microsoft ist das einzige Unternehmen, das Unterstützung für den Online- und Offline-Modus bietet.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Was bedeutet duales Schreiben für Entwickler und Architekten von Customer Engagement-Apps?

Dual-write automatisiert den Datenfluss zwischen Finanz- und Betriebs-Apps und Customer-Engagement-Apps. Duales Schreiben besteht aus zwei AppSource-Lösungen, die auf Dataverse installiert sind. Die Lösungen erweitern das Tabellenschema, die Plugins und die Workflows in Dataverse, damit sie auf ERP-Größe skaliert werden können. Für eine erfolgreiche Implementierung müssen die Entwickler und Architekten von Customer-Engagement-Apps diese Änderungen verstehen und mit ihren Kollegen von Finanz- und Betriebs-Apps zusammenarbeiten.

Um Parität mit Finanzen und Betrieb-Anwendungen zu erstellen, nimmt Dual-write einige entscheidende Änderungen im Dataverse-Schema vor. Wenn Sie den Plan verstehen, können Sie in Zukunft einige Entwurfs- und Entwicklungsarbeiten vermeiden.

+ Wenn das AppSource-Paket für duales Schreiben installiert ist, verfügt Dataverse über neue Konzepte wie Unternehmen und Partei. Diese Konzepte helfen Anwendungen, die auf Dataverse aufgebaut sind, einschließlich Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service und Dynamics 365 Field Service, nahtlos mit Finanz- und Betriebs-Apps zu interagieren.

+ Aktivitäten und Notizen werden vereinheitlicht und erweitert, um sowohl die C1 (Benutzer des Systems) als auch die C2 (Kunden des Systems) zu unterstützen.

+ Um Datenverluste bei der Währungsübertragung zwischen Finanz- und Betriebs-Apps und der Dataverse zu verhindern, können Sie die Anzahl der Dezimalstellen im Währungsdatentyp von Customer-Engagement-Apps erweitern. Die Funktion übersetzt automatisch vorhandene Zeilen auf der Metadatenebene in den neuen erweiterten Status. Während dieses Vorgangs wird der Währungswert in Dezimaldaten und nicht in Gelddaten umgerechnet, und der Währungswert unterstützt 10 Dezimalstellen. Diese Funktion ist aktiviert, und Unternehmen, die nicht mehr als 4 Dezimalstellen benötigen, müssen dies nicht aktivieren. Weitere Informationen finden Sie unter [Migration vom Währungsdatentyp für duales Schreiben](currrency-decimal-places.md).

+ [Datumsgültigkeit](../../dev-tools/date-effectivity.md) wird Dataverse hinzugefügt. Sie wird vergangene, gegenwärtige und zukünftige Daten in der gleichen Tabelle unterstützen.

+ Produkt-[Einheitenumrechnungen](../../../../supply-chain/pim/tasks/manage-unit-measure.md) werden für Produkte, Angebote, Bestellungen und Rechnungen unterstützt.

Weitere Informationen zu bevorstehenden Änderungen finden Sie unter [Neuerungen oder Änderungen beim dualen Schreiben](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

