---
title: " Konfigurationen für Einzelhandelsauszüge speichern"
description: Diese Prozedur zeigt Schritt für Schritt Konfigurationen für das Einzelhandelsgeschäft, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fddeb8434d916df1613d61da88110dec8fb4465
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "354712"
---
# <a name="store-configurations-for-retail-statements"></a> Konfigurationen für Einzelhandelsauszüge speichern

[!include[task guide banner](../includes/task-guide-banner.md)]

Diese Prozedur zeigt Schritt für Schritt Konfigurationen für das Einzelhandelsgeschäft, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden. Finanzdimensionen in Einzelhandelsgeschäften werden in einer anderen Prozedur abgedeckt. Für diese Prozedur wird das Demo-Unternehmen USRT verwendet.

1. Navigieren Sie zu Einzelhandel und Handel > Kanäle > Einzelhandelsgeschäfte > Alle Einzelhandelsgeschäfte.
2. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
3. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Die Einstellungen im Abschnitt "Auszug/Abschluss" wirken sich auf die Auszugserstellung, -prüfung und -buchung für den Shop aus.  Öffnen Sie den Auszug/das Nachspiel.  
    * Wählen Sie die Methode aus, die Sie verwenden möchten, um die Auszugspositionen zu gruppieren.  
    * Wählen Sie "Ja" aus, wenn nur ein Auszug pro Tag erstellt werden soll, wenn Auszüge vom Auszugserstellungsbatchauftrag erstellt werden.  
    * Das Kassensturzberechnungs-Feld definiert, ob Kassenstürze zusammen hinzugefügt werden sollen, oder ob der letzte verwendet werden soll.  
    * Wählen Sie das Sachkonto aus, um Rundungsdifferenzen darauf zu buchen.  
    * Im Feld "Maximale Rundungsdifferenz" können Sie die maximal zulässige Rundungsdifferenz eingeben.  
    * Im Buchungsfeld können Sie den maximalen gesamten Buchungsunterschied eingeben, der für einen Auszug zulässig ist.  
    * Im Schicht-Feld können Sie den maximalen gesamten Unterschied innerhalb einer Schicht für einen Auszug eingeben.  
    * Im Feld "Transaktion" können Sie die maximale gesamte Differenz in einer Auszugsposition eingeben.  
    * Im Feld "Abschlussmethode" können Sie definieren, ob Buchungen, die in einem Auszug enthalten sind, Teil einer geschlossenen Schicht sein sollen, oder ob sie beliebige Buchungen innerhalb des festgelegten Datum/Uhrzeit-Bereiches werden können.  
    * Im Feld "Ende des Arbeitstags" können Sie eine Uhrzeit eingeben, wenn Buchungen, die nach Mitternacht auftreten, zum vorhergehenden Tag gebucht werden sollen.  
    * Wählen Sie "Ja" aus, wenn Buchungen, die nach Mitternacht auftreten, als Teil des vorherigen Tages gebucht werden sollen.  
    * Wählen Sie "Ja" aus, um Aufstellungen zu erhalten, die für jede definierte Auszugsmethode erstellt werden. Dies kann hilfreich sein, wenn die Leistung der Buchung für Shops mit hohem Buchungsvolumen verbessert werden muss, da viele kleinere Auszüge erstellt werden, die parallel verarbeitet werden können.  
    * Im Feld "Standarddebitor" können Sie das Debitorenkonto auswählen, um es für Verkäufe an Laufkundschaft zu verwenden.  

