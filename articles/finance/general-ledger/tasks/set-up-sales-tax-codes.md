---
title: Mehrwertsteuercodes einrichten
description: In diesem Artikel wird erläutert, wie Mehrwertsteuercodes in Dynamics 365 Finance eingerichtet werden.
author: twheeloc
ms.date: 09/27/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b12133583f40cc17cb85f6dbd86697592af25caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858467"
---
# <a name="set-up-sales-tax-codes"></a>Mehrwertsteuercodes einrichten

[!include [banner](../../includes/banner.md)]

In diesem Artikel wird erläutert, wie Mehrwertsteuercodes eingerichtet werden. Mehrwertsteuercodes werden für jede indirekte Steuer oder Abgabe berechnet, die die juristische Person berechnen, erfassen und den Steuerbehörden entrichten muss.

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

    Wenn auf dem Inforegister **Berechnung** im Feld **Ursprung** die Option **Betrag pro Einheit** ausgewählt ist, wird der Wert mit der Menge in der Transaktion multipliziert, um den Mehrwertsteuerbetrag zu berechnen.  Wenn der Steuercode keine auf Einheiten basierte Steuer ist, ist der Wert ein Prozentsatz, der auf den „Ursprung“ für diesen Steuercode angewendet wird, um den Mehrwertsteuerbetrag zu berechnen.     

11. Wählen Sie **Speichern** aus.
12. Schließen Sie die Seite.
13. Wählen Sie **Speichern** aus.

Ab Version 10.0.22 von Microsoft Dynamics 365 Finance können Sie mit dem Feld **Steuertyp** den Typ des Steuercodes festlegen, wenn Sie den [Steuerservice](../../localizations/global-tax-calcuation-service-overview.md) verwenden und die Funktion [**Mehrere MwSt.-Registrierungsnummern unterstützen**](../../localizations/emea-multiple-vat-registration-numbers.md) im Arbeitsbereich **Funktionsverwaltung** aktiviert ist. Folgende Werte sind verfügbar:

- Standard-MwSt.
- Reduzierte MwSt.
- MwSt. 0%
- Verbrauchssteuer
- Sonstige

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
