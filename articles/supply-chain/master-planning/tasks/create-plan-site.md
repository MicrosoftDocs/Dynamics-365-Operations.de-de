--- 
title: "Einen Plan für einen Standort erstellen"
description: "Der Produktionsplaner berechnet das Material und die Kapazitätsanforderungen für die Produktion eines bestimmten Artikels."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-plan-for-a-site"></a>Einen Plan für einen Standort erstellen

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Der Produktionsplaner berechnet das Material und die Kapazitätsanforderungen für die Produktion eines bestimmten Artikels. Nachdem die Beschaffungsvorschläge erstellt wurden, findet er die Aufträge am Standort, für den er plant und die Aufträge umwandelt, beginnend mit den dringenden Aufträgen. Die dringendsten Aufträge sind diejenigen, die zum aktuellen Datum umgewandelt werden müssen. Verwenden Sie das Demodatunternehmen USMF, um diese Aufgaben auszuführen.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>Erstellen Sie einen Materialien- und Kapazitätsplan für einen Artikel
1. Klicken Sie auf "Produktprogrammplanung".
    * Sie müssen zum standardmäßigen Dashboard navigieren.  
2. Klicken Sie auf "Ausführen".
3. Erweitern Sie den Abschnitt "Einzuschließende Datensätze".
4. Klicken Sie auf "Filter".
5. Markieren Sie in der Liste die ausgewählte Zeile.
6. Geben Sie im Feld "Kriterien" einen Wert ein.
    * Beispiel: D0001  
7. Klicken Sie auf "OK".
8. Klicken Sie auf "OK".
    * Das kann einige Minuten in Anspruch nehmen.  
9. Aktualisieren Sie die Seite.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>Identifizieren Sie die dringenden Bestellvorschläge für den Artikel
1. Öffnen Sie den Spaltenfilter "Artikelnummer".
2. Verwenden Sie den Filteroperator "Beginnt mit", um einen Filter auf das Feld "Artikelnummer" mit einem Wert von "D0001" anzuwenden.
3. Öffnen Sie den Spaltenfilter "Auftragsdatum".
4. Wenden Sie einen Filter auf das Feld "Auftragsdatum" an, mit einem Wert des aktuellen Datums, mithilfe des Filteroperators "Ist genau".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>Wandeln Sie alle dringenden Aufträge für den Artikel um
1. Markieren Sie alle Zeilen in der Liste, oder heben Sie die Markierung auf.
2. Klicken Sie auf "Umwandeln".
3. Klicken Sie auf "OK".


