--- 
title: Mehrwertsteuercodes einrichten
description: "Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9d55964a8d29d84198a90634e4337db115fe686d
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-tax-codes"></a>Mehrwertsteuercodes einrichten

[!include[task guide banner](../../includes/task-guide-banner.md)]

Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss.

Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.



1. Wechseln Sie zu "Steuer" > "Indirekte Steuern" > "Mehrwertsteuer" > "Mehrwertsteuercodes".
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Mehrwertsteuercode" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Wählen Sie einen Abrechnungszeitraum aus, um anzugeben, welche Mehrwertsteuerbehörde und in welchen Abständen diese Mehrwertsteuer gemeldet und abgeführt werden muss.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Wählen Sie eine "Sachkontobuchungsgruppe" aus, um die Hauptkonten anzugeben, um die Mehrwertsteuer im Hauptbuch zu buchen.
8. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Erweitern Sie das Inforegister "Berechnung".
    * Das Inforegister "Berechnung" hat mehrere Felder, die steuern, wie Mehrwertsteuerbeträge berechnet werden.  
11. Klicken Sie im Aktivitätsbereich auf "Mehrwertsteuercode".
12. Klicken Sie auf "Werte".
13. Markieren Sie in der Liste die ausgewählte Zeile.
14. Geben Sie den Wert für diesen Steuercode ein.
    * Wenn im Inforegister "Berechnung" im Feld "Ursprung" die Option "Betrag pro Einheit" ausgewählt ist, wird der Wert um die Menge in der Transaktion multipliziert, um den Mehrwertsteuerbetrag zu berechnen.  Wenn der Steuercode keine auf Einheiten basierte Steuer ist, ist der Wert ein Prozentsatz, der auf den "Ursprung" für diesen Steuercode angewendet wird, um den Mehrwertsteuerbetrag zu berechnen.     
15. Klicken Sie auf "Speichern".
16. Schließen Sie die Seite.
17. Klicken Sie auf "Speichern".


