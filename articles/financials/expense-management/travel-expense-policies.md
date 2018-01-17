---
title: Ausgabenrichtlinien definieren
description: "Sie können Ausgabenrichtlinien definieren, die ihre Arbeitskräfte einhalten müssen, wenn sie in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, Spesenabrechnungen und Reiseanforderungen eingeben und übermitteln."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9a5ce1a3b6519b510c9f5aa5618ab91f77a2d91a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

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

