---
title: Ausgabenrichtlinien definieren
description: In Microsoft Dynamics 365 Finance können Richtlinien festgelegt werden, an die sich die Mitarbeiter beim Eingeben und Einreichen von Spesenabrechnungen und Reiseanforderungen zu halten haben.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389714"
---
# <a name="define-expense-policies"></a>Ausgabenrichtlinien definieren

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

## <a name="policy-tips"></a>Richtlinientipps
Nachfolgend finden Sie einige Vorschläge, die Sie beim Erstellen neuer Richtlinien für Ausgabenverwaltung unterstützen. 
* Die Wirksamtkein von Richtlinien ist vom Datum abhängig und sie treten nicht in Kraft, wenn die Richtlinie mit einem Datum erstellt wird, das hinter dem Datum der Aufwendung liegt. Wenn Sie z. B.heute eine neue Richtlinie erstellen, um maximale Verpflegungsausgaben von 50 US-Dollar zu erzwingen, dann gilt diese Richtlinie für keine vorhandenen Ausgaben, die bis Gestern eingereicht werden.
* Bei Erstellung einer Richtlinie für eine Ausgabenkategorie, die aufgeschlüsselt werden kann, sollten Sie eine Bedingung für den Ausgabenpositionstyp hinzuzufügen. Einige Richtlinien wie das anfordern eines Belegt, sind möglicherweise für aufgeschlüsselte Positionen nicht sinnvoll und sollten nur auf die Kopfzeile oder eine nicht aufgeschlüsselte Position angewendet werden. 
* Ausgabenverwaltungsrichtlinien werden standardmäßig anhand der Quellenentität bewertet. Für konzerninterne Szenarien können Sie stattdessen festlegen, dass die Richtlinie anhand der Zielentität (Kreditinstanz) bewertet wird. Um die Richtlinien für die Zielentität auszuführen, aktivieren Sie die Funktion „Kostenrichtlinie gegen Ausleihen einer juristischen Person bewerten“ im Arbeitsbereich **Funktionsverwaltung**.

## <a name="when-to-evaluate-policies"></a>Wann Richtlinien ausgewertet werden sollten

In den Parametern der Ausgabenverwaltung finden Sie eine Option, mit der Sie entweder die Ausgabenverwaltungsrichtlinien auswerten könne, wenn eine Position gespeichert wird, oder wenn ein Ausgabenbeleg eingereicht wird. Wenn Sie sich entscheiden, die Auswertung beim Speichern der Position vorzunehmen, wird sichergestellt, dass Benutzer frühere Sichtbarkeit in die erforderlichen Aufgaben erhalten, um Ihren Ausgabenbericht in einem Zug abzuschließen. Andernfalls können Sie die Richtlinienbewertung zurückstellen und Zeit sparen, wenn die Überprüfung am Ende durchgeführt wird, bei der Übermittlung an den Workflow.
