---
title: Definieren Sie Einzelhandelskanalkommunikationen (Handels-Datenaustausch)
description: "Dieser Artikel enthält eine Übersicht über den Handelsdatenaustausch und deren Komponenten. Von Konten für die Rolle, der jede Komponente in die Übertragung von Daten aus Microsoft Dynamics 365 für Arbeitsgänge und Einzelhandelskanäle wiedergibt."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
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

Dieser Artikel enthält eine Übersicht über den Handelsdatenaustausch und deren Komponenten. Von Konten für die Rolle, der jede Komponente in die Übertragung von Daten aus Microsoft Dynamics 365 für Arbeitsgänge und Einzelhandelskanäle wiedergibt.

<a name="overview"></a>Überblick
--------

Handels-Datenaustausch ist ein System, das Daten zwischen Dynamics 365 für Einzelhandelskanäle, wie Arbeitsgänge und Onlineshops physische oder Shops umgelagert werden. Die Datenbank, die Daten für einen Einzelhandelskanal speichert, ist getrennt von den Dynamics 365 für Arbeitsgangsdatenbank. Die Kanaldatenbank enthält nur die Daten, die für Einzelhandelstransaktionen erforderlich sind. Stammdaten werden in Dynamics 365 für Vorgänge konfiguriert und verteilt den Kanälen. Buchungsbezogene Daten werden im Verkaufsstelle System (POS)- oder im Onlineshop erstellt hochgeladen und dann zu Dynamics 365 für Arbeitsgänge. Datenverteilung ist asynchron. Das bedeutet, der Prozess des Sammelns und Verpackens von Daten am Ursprung findet separat vom Prozess des Empfangens und des Anwendens von Daten am Ziel statt. Für einige Szenarien, wie Preis- und Lagersuchen, müssen Daten in der Echtzeit abgerufen werden. Um diese Szenarien zu unterstützen, enthält Handels-Datenaustausch auch einen Service der Echtzeitkommunikation zwischen Dynamics 365 für Arbeitsgänge und eines Kanals aktiviert. 

![aktualisierte-EinzelhandelGrafik( [] . /media/updated-retail-graphic.png)]". /media/updated-retail-graphic.png)  

## <a name="async-service"></a>Async Dienst
Microsoft SQL Server-Änderungsnachverfolgung im Dynamics 365 für Arbeitsgangsdatenbank wird verwendet, um die Daten zu bestimmen, die zu den Kanälen gesendet werden müssen. Auf Basis eines Verteilungszeitplan Dynamics speichert 365 für Arbeitsgangspakete die Daten und der Lagerung (Azure der zentralen BLOB-Speicher). Ein separater Stapelverarbeitungsvorgang verwendet die Commerce Data Exchange: Async Client-Bibliothek, um dieses Datenpaket in die Kanaldatenbank einzufügen. 

[![Async Service](./media/async-300x239.png)](./media/async.png)

### <a name="retail-scheduler"></a>Einzelhandel-Steuerprogramm

Steuerprogrammaufträge bilden den Mechanismus für den Vertrieb bzw. die Verteilung von Daten an und von Standorten. Einzelvorgänge bestehen aus Unteraufträgen, die die Tabellen und die Tabellenfelder mit den zu verteilenden Daten definieren. Dynamics 365 für Arbeitsgänge umfasst vordefinierten Steuerprogramm Einzelvorgänge und Untereinzelvorgänge ein, die die Wiederholungsbedingungen der meisten Organisationen entsprechen. Folgende Typen von vordefinierten Aufträgen werden erstellt:

-   ** Downloadeinzelvorgänge ** - Downloadeinzelvorgänge senden Daten, die von Microsoft Dynamics 365 für Arbeitsgänge zu den Kanaldatenbanken geändert hat. Änderungen an den Datensätzen werden von der SQL Server-Änderungsnachverfolgung nachverfolgt.
-   ** Uploadeinzelvorgänge (P-Einzelvorgänge) - Uploadeinzelvorgänge** ziehen Verkaufsbuchungen aus in einem Kanal das Dynamics 365 für Arbeitsgangsdatenbank. P-Einzelvorgänge laden Daten stufenweise hoch. Wenn ein P-Einzelvorgang ausgeführt wird, überprüft die Async-Client-Bibliothek den Wiederholungszähler für Datensätze, die bereits am Standort eingegangen sind. Ein Datensatz wird nur hochgeladen, wenn sein Wiederholungszähler höher als der größte Wert ist, der gefunden wird. P-Einzelvorgänge aktualisieren keine Daten, die zuvor hochgeladen wurden.

Der Verteilungszeitplan wird verwendet, um die Datenübertragung manuell oder indem entweder einen Stapelverarbeitungsauftrag auszuführen, in Dynamics 365 für Arbeitsgänge geplant wird. Ein Vertriebsplan kann eine oder mehrere Kanaldatengruppen und mindestens einen Steuerprogrammauftrag enthalten.

## <a name="realtime-service"></a>Echtzeit-Service
Handels-Datenaustausch: Echtzeit-Service integrierter ist ein Dienst, der Echtzeitkommunikation zwischen Dynamics 365 für Arbeitsgänge und Einzelhandelskanäle bereitstellt. Echtzeit-Service aktiviert einzelne POS-Computer und -Onlineshops, um bestimmte Daten von Microsoft Dynamics 365 für Arbeitsgänge in die Echtzeit abzurufen. Zwar werden die meisten entscheidenden Arbeitsgänge in der Datenbank des lokalen Kanal ausgeführt werden können, müssen die folgenden Szenarien Direktzugriff zu den Daten, die in Arbeitsgängen für Dynamics 365 gespeichert wird:

-   Geschenkkarten ausstellen und einlösend.
-   Treuepunkte einlösen.
-   Gutschriften ausgeben und einlösen.
-   Debitorendatensätze erstellen oder aktualisieren.
-   Erstellen, Aktualisieren und Abschließen von Aufträgen.
-   Den Bestands mit einer Bestellung oder einem Umlagerungsauftrag empfangen.
-   Bestandszählungen durchführen.
-   Verkaufsbuchungen shopübergreifend abrufen und Retourenbuchungen abschließen.

[![Real-time Service](./media/rts.png)](./media/rts.png) 

Ein Echtzeit-Service-Profil vordefiniertes wird erstellt.


