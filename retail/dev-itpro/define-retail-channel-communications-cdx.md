---
title: Definieren Sie Einzelhandelskanalkommunikationen (Handels-Datenaustausch)
description: "Dieser Artikel enthält eine Übersicht über den Handelsdatenaustausch und deren Komponenten. Er erklärt die Rolle, die jede Komponente in der Übertragung von Daten zwischen Microsoft Dynamics 365 for Operations und Einzelhandelskanälen spielt."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 29938d962db42a521dd8dc03b8e45e0e34410e4d
ms.openlocfilehash: d3b36ec2a3f859215d93dd7ebf1f1ecfb2731c59
ms.lasthandoff: 03/31/2017


---

# <a name="define-retail-channel-communications-commerce-data-exchange"></a>Definieren Sie Einzelhandelskanalkommunikationen (Handels-Datenaustausch)

[!include[banner](../includes/banner.md)]


Dieser Artikel enthält eine Übersicht über den Handelsdatenaustausch und deren Komponenten. Er erklärt die Rolle, die jede Komponente in der Übertragung von Daten zwischen Microsoft Dynamics 365 for Operations und Einzelhandelskanälen spielt.

<a name="overview"></a>Überblick
--------

Commerce Data Exchange ist ein System, das Daten zwischen Microsoft Dynamics 365 for Operations und Einzelhandelskanälen, wie Onlineshops oder physische Shops, austauscht. Die Datenbank, die Daten für einen Einzelhandelskanal speichert, ist getrennt von der Microsoft Dynamics 365 for Operations-Datenbank. Die Kanaldatenbank enthält nur die Daten, die für Einzelhandelstransaktionen erforderlich sind. Masterdaten werden in Microsoft Dynamics 365 for Operations konfiguriert und auf Kanäle verteilt. Buchungsbezogene Daten werden im Verkaufsstelle (POS)-System oder im Onlineshop erstellt und dann auf Microsoft Dynamics 365 for Operations hochgeladen. Datenverteilung ist asynchron. Das bedeutet, der Prozess des Sammelns und Verpackens von Daten am Ursprung findet separat vom Prozess des Empfangens und des Anwendens von Daten am Ziel statt. Für einige Szenarien, wie Preis- und Lagersuchen, müssen Daten in der Echtzeit abgerufen werden. Um diese Szenarien zu unterstützen, umfasst der Commerce Data Exchange auch einen Dienst, der Echtzeitkommunikation zwischen Microsoft Dynamics 365 for Operations und einem Kanal beinhaltet. 

[![aktualisierte-Einzelhandelsgrafik](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Dienst
Die Microsoft SQL Server-Änderungsnachverfolgung in der Microsoft Dynamics 365 for Operations Datenbank wird verwendet, um die Daten zu bestimmen, die den Kanälen gesendet werden müssen. Auf Grundlage eines Verteilungszeitplans packt Microsoft Dynamics 365 for Operations die Daten und speichert sie im zentralem Speicher (Azure Blob Storage). Ein separater Stapelverarbeitungsvorgang verwendet die Commerce Data Exchange: Async Client-Bibliothek, um dieses Datenpaket in die Kanaldatenbank einzufügen. 

[![Async Dienst](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Einzelhandel-Steuerprogramm

Steuerprogrammaufträge bilden den Mechanismus für den Vertrieb bzw. die Verteilung von Daten an und von Standorten. Einzelvorgänge bestehen aus Unteraufträgen, die die Tabellen und die Tabellenfelder mit den zu verteilenden Daten definieren. Microsoft Dynamics 365 for Operations  beinhaltet vordefinierte Steuerprogramm-Aufträge und Unteraufträge, die den Wiederholungsanforderungen der meisten Organisationen entsprechen. Folgende Typen von vordefinierten Aufträgen werden erstellt:

-   **Downloadvorgang** - Downloadvorgänge senden Daten, die von Microsoft Dynamics 365 for Operations  geändert wurden, an die Kanaldatenbanken. Änderungen an den Datensätzen werden von der SQL Server-Änderungsnachverfolgung nachverfolgt.
-   **Uploadvorgang (P-Einzelvorgänge)** - Uploadvorgänge ziehen Verkaufsbuchungen aus einem Kanal in die Microsoft Dynamics 365 for Operations-Datenbank. P-Einzelvorgänge laden Daten stufenweise hoch. Wenn ein P-Einzelvorgang ausgeführt wird, überprüft die Async-Client-Bibliothek den Wiederholungszähler für Datensätze, die bereits am Standort eingegangen sind. Ein Datensatz wird nur hochgeladen, wenn sein Wiederholungszähler höher als der größte Wert ist, der gefunden wird. P-Einzelvorgänge aktualisieren keine Daten, die zuvor hochgeladen wurden.

Der Vertriebsplan wird verwendet, um die Datenübertragung manuell oder durch Ausführen einer Stapelverarbeitung in Microsoft Dynamics 365 for Operations  zu starten. Ein Vertriebsplan kann eine oder mehrere Kanaldatengruppen und mindestens einen Steuerprogrammauftrag enthalten.

## <a name="realtime-service"></a>Echtzeitservice
Commerce Data Exchange: Real-time Service ist ein integrierter Dienst, der Echtzeitkommunikation zwischen Microsoft Dynamics 365 for Operations  und den Vertriebskanälen ermöglicht. Real-time Service aktiviert einzelne POS-Computer und Onlineshops, um bestimmte Daten aus Microsoft Dynamics 365 for Operations  in der Echtzeit abzurufen. Obwohl die meisten wichtigen Funktionen in der Datenbank des lokalen Kanals ausgeführt werden können, benötigen die folgenden Szenarien direkten Zugriff auf Daten, die in Microsoft Dynamics 365 for Operations  gespeichert werden:

-   Geschenkkarten ausstellen und einlösend.
-   Treuepunkte einlösen.
-   Gutschriften ausgeben und einlösen.
-   Debitorendatensätze erstellen oder aktualisieren.
-   Erstellen, Aktualisieren und Abschließen von Aufträgen.
-   Den Bestands mit einer Bestellung oder einem Umlagerungsauftrag empfangen.
-   Bestandszählungen durchführen.
-   Verkaufsbuchungen shopübergreifend abrufen und Retourenbuchungen abschließen.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Ein vordefiniertes Echtzeit-Serviceprofil wird erstellt.




