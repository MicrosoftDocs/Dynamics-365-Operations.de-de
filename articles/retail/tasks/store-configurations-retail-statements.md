--- 
title: " Konfigurationen für Einzelhandelsauszüge speichern"
description: "Diese Prozedur zeigt Schritt für Schritt Konfigurationen für das Einzelhandelsgeschäft, die sich darauf auswirken, wie Einzelhandelsauszüge erstellt und gebucht werden."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 45aa0caf6fcef4cc49952557a251dd78f816125e
ms.contentlocale: de-de
ms.lasthandoff: 11/14/2017

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


