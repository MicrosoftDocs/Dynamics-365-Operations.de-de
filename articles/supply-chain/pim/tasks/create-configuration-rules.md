---
title: Variantenregeln erstellen
description: Diese Prozedur erstellt Konfigurationsregeln, die für eine dimensionsbasierte Konfiguration verwendet werden können, um bestimmte Kombinationen von Stücklistenpositionen zu erzwingen oder zu verhindern.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d5758b2903cd0a269f3e03e44b618c26e8b2310
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147870"
---
# <a name="create-configuration-rules"></a>Variantenregeln erstellen

[!include [banner](../../includes/banner.md)]

Diese Prozedur erstellt Konfigurationsregeln, die für eine dimensionsbasierte Konfiguration verwendet werden können, um bestimmte Kombinationen von Stücklistenpositionen zu erzwingen oder zu verhindern. Das Demodatenunternehmen, das verwendet wird, um diese Prozedur zu erstellen, ist USMF. Dies ist die siebte von acht Prozeduren die beschreibt, wie Kombinationen für eine dimensionsbasierte Konfiguration erstellt werden.

1. Wechseln Sie zu Produktinformationsverwaltung > Stücklisten und Formeln > Stücklisten.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie die Technologie BOM der dimensionsbasierten Konfiguration aus.  
3. Klicken Sie im Aktivitätsbereich auf "Optionen".
4. Klicken Sie auf "Ansicht ändern".
5. Klicken Sie auf die Kopfzeilenansicht.
    * Öffnen Sie die Kopfzeilenansicht, um auf die Konfigurationsroute FastTab zuzugreifen.  
6. Erweitern oder reduzieren Sie den Abschnitt Konfigurationsplan.
    * Der Konfigurationsroute-FastTab muss im Modus "Erweitert" sein.  
7. Configurationregeln anzeigen
8. Klicken Sie auf "Neu".
9. Markieren Sie in der Liste die ausgewählte Zeile.
10. Klicken Sie im Feld "Artikelnummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
    * Die Artikel in der aktuellen Konfigurationsgruppe werden angezeigt. Wählen Sie diejenige aus, die die Bedingung in der Regel darstellt.  
11. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
12. Wählen Sie im Feld "Methode" eine Option aus.
    * Es ist möglich, entweder eine Auswahl oder ein deselection eines Artikels aus einer anderen Konfigurationroute-Gruppe zu erzwingen.  
13. Klicken Sie im Feld Abgeleitete-Gruppe auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie die gewünschte Gruppe "Konfigurationroute" aus.  
16. Klicken Sie im Feld "Abgeleitete-Gruppenummer" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
17. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Die Artikelnummer, die abhängig von der gewählten Methode ausgewählt oder gelöscht werden soll.  
18. Schließen Sie die Seite.

