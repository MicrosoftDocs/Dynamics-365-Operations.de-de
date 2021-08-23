---
title: Mehrwertsteuercodes einrichten
description: In diesem Thema wird erläutert, wie Mehrwertsteuercodes in Dynamics 365 Finance eingerichtet werden.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5ce2c8d9a117871191dd1c2d32d822bcc72d76fabaec146d9b8c27fc85dc058
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719197"
---
# <a name="set-up-sales-tax-codes"></a>Mehrwertsteuercodes einrichten

[!include [banner](../../includes/banner.md)]

In diesem Thema wird erläutert, wie Mehrwertsteuercodes eingerichtet werden. Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss.

Für diese Aufgabe wird das Demo-Unternehmen USMF verwendet.

1. Wechseln Sie zu **Navigationsbereich > Steuer > Indirekte Steuern > Mehrwertsteuer > Mehrwertsteuercodes**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Mehrwertsteuercode** einen Wert ein.
4. Geben Sie im Feld **Name** einen Wert ein.
5. Wählen Sie einen **Abrechnungszeitraum** aus, indem Sie die Pulldownliste öffnen, um anzugeben, welcher Mehrwertsteuerbehörde und in welchen Abständen diese Mehrwertsteuer gemeldet und abgeführt werden muss.
6. Wählen Sie eine **Sachkontobuchungsgruppe** aus, um die Hauptkonten anzugeben, um die Mehrwertsteuer im Hauptbuch zu buchen.
7. Erweitern Sie das Inforegister **Berechnung**. Dieses hat mehrere Felder, die steuern, wie Mehrwertsteuerbeträge berechnet werden. Füllen Sie diese Felder nach Bedarf aus.  
8. Wählen Sie im **Aktivitätsbereich** oben in der Benutzeroberfläche **Mehrwertsteuercode** aus.
9. Wählen Sie **Werte** aus.
10. Geben Sie den Wert für diesen Steuercode in der Spalte **Wert** ein.
    - Wenn auf dem Inforegister **Berechnung** im Feld „Ursprung“ die Option „Betrag pro Einheit“ ausgewählt ist, wird der Wert mit der Menge in der Transaktion multipliziert, um den Mehrwertsteuerbetrag zu berechnen.  Wenn der Steuercode keine auf Einheiten basierte Steuer ist, ist der Wert ein Prozentsatz, der auf den "Ursprung" für diesen Steuercode angewendet wird, um den Mehrwertsteuerbetrag zu berechnen.     
11. Wählen Sie **Speichern**.
12. Schließen Sie die Seite.
13. Wählen Sie **Speichern**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]