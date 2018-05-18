---
title: Ausgabenrichtlinien definieren
description: "Sie können Ausgabenrichtlinien definieren, die ihre Arbeitskräfte einhalten müssen, wenn sie in Microsoft Dynamics 365 for Finance and Operations Spesenabrechnungen und Reiseanforderungen eingeben und übermitteln."
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3b2a28fe6acf03e52c292048a797ce997f58bcce
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="expense-policies"></a>Ausgabenrichtlinien

[!include [banner](../includes/banner.md)]

Sie können Richtlinien definieren, an die sich die Mitarbeiter beim Eingeben und Übermitteln von Spesenabrechnungen und Reiseanforderungen zu halten haben.         
Die Implementierung von Ausgabenrichtlinien trägt zu einer Optimierung der Ausgabenverwaltung bei.         

So können Sie beispielsweise eine Richtlinie für Hotelausgaben in New York City einrichten, die festlegt, dass die Hotelkosten pro Übernachtung höchstens EUR 250 betragen dürfen.       
Wenn eine Arbeitskraft eine Spesenabrechnung oder eine Reiseanforderung übermittelt, in der der Übernachtungspreis diesen Betrag übersteigt, meldet das System dies der        
Arbeitskraft, dass der Betrag entsprechend der Richtlinie überschritten wurde. Sie können die Meldung konfigurieren, die die Arbeitskraft erhält, wenn Sie die Richtlinie definieren.        
Richtlinienregeln festlegen.      
        
Sie können drei Arten von Richtlinien definieren:         
        
- Warnung - Ermöglicht der Arbeitskraft, eine Spesenabrechnung oder eine Reiseanforderung zu übermitteln, die Ausgaben werden jedoch markiert für alle genehmigenden Personen        
  und für die spätere Berichterstellung.        

- Fehler – Verlangt, dass die Arbeitskraft vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung die Ausgaben überarbeiten, um die Einhaltung der Richtlinie zu garantieren.       
 
  - Begründung – Erfordert, dass die Arbeitskraft oder ein Manager vor dem Übermitteln der Spesenabrechnung oder der Reiseanforderung eine Begründung für eine Überschreitung des Richtlinienbetrags eingibt.        
 
  Sie können auch einen Datumsbereich einrichten, für den Ausgabenrichtlinien wirksam sind. Beispielsweise Flugtickets zwischen Dänemark      
  und New York City können während der Hauptreisezeit besonders teuer sein. Sie können eine Flugkostenregel definieren, die die      
  Flugkosten nach New York City auf einen Betrag von DKK 5000 festlegt und Sie können angeben, das diese Regeln zwischen 15. März und      
  15. September gilt.

