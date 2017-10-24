---
title: Ausgabenrichtlinien definieren
description: "Sie können Ausgabenrichtlinien definieren, die ihre Arbeitskräfte einhalten müssen, wenn sie in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, Spesenabrechnungen und Reiseanforderungen eingeben und übermitteln."
author: saraschi2
manager: AnnBe
ms.date: 09/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 940d6f8c3d878c2c12806ad04a092856df2acb33
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="expense-policies"></a>Ausgabenrichtlinien

[!include[banner](../includes/banner.md)]

Sie können Richtlinien definieren, an die sich die Mitarbeiter beim Eingeben und Übermitteln von Spesenabrechnungen und Reiseanforderungen zu halten haben. Die Implementierung von Ausgabenrichtlinien trägt zu einer Optimierung der Ausgabenverwaltung bei. 

So können Sie beispielsweise eine Richtlinie für Hotelausgaben in New York City einrichten, die festlegt, dass die Hotelkosten pro Übernachtung höchstens EUR 250 betragen dürfen. Wenn eine Arbeitskraft eine Spesenabrechnung oder Reiseanforderung mit einem höheren Übernachtungspreis einreicht, wird die Arbeitskraft mittels einer entsprechenden Meldung darauf hingewiesen, dass der per Richtlinie festgelegte Betrag überschritten wurde. Sie können die Meldung konfigurieren, die die Arbeitskraft erhält, wenn Sie die Richtlinie definieren. 

Sie können drei Arten von Richtlinien definieren: 

 - Warnung - Ermöglicht der Arbeitskraft, eine Spesenabrechnung oder eine Reiseanforderung zu übermitteln, die Ausgaben werden jedoch markiert für alle genehmigenden Personen  
 und für die spätere Berichterstellung. 
 - Fehler – Verlangt, dass die Arbeitskraft vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung die Ausgaben überarbeiten, um die Einhaltung der Richtlinie zu garantieren. 
 - Begründung – Erfordert, dass die Arbeitskraft oder ein Manager vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung eine Begründung für eine Überschreitung des Richtlinienbetrags eingibt. 

Sie können auch einen Datumsbereich einrichten, für den Ausgabenrichtlinien wirksam sind. Zum Beispiel sind die Kosten für Flugtickets zwischen Dänemark und New York während der Hauptreisezeit besonders hoch. Sie können eine Flugkostenregel definieren, die die Kosten von Flügen nach New York City auf das Limit von DKK 5000 beschränkt, und Sie können angeben, dass diese Regel zwischen dem 15. März und dem 15. September gilt. 

