---
title: Die Steuer wird nicht berechnet oder der Steuerbetrag ist Null
description: Dieser Artikel enthält Informationen zur Fehlerbehebung, die helfen können, wenn der Steuerbetrag 0 (Null) ist oder die Steuer nicht berechnet wird.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: f2a5bb0d1cef93ec1fea2e21c1750fe94a454c18
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849843"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a>Die Steuer wird nicht berechnet oder der Steuerbetrag ist Null

[!include [banner](../includes/banner.md)]

Eine Transaktion kann einen Zeilenbetrag haben, der nicht 0 (Null) ist, aber entweder wird die Steuer nicht berechnet oder der berechnete Steuerbetrag ist 0. Um dieses Problem zu beheben, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus.

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a>Überprüfen Sie, ob die Steuerkennzeichen in der Transaktion korrekt ausgewählt sind

Wenn die Transaktion nicht die richtigen Steuerkennzeichen auswählt oder wenn sie keine Steuerkennzeichen auswählt, werden keine Steuern für sie berechnet. Führen Sie diese Schritte aus, um zu überprüfen, ob die Steuerkennzeichen von der Transaktion korrekt ausgewählt wurden. 

1. Stellen Sie in der Zeile der Transaktion auf dem Inforegister **Zeilendetails**, auf der Registerkarte **Einrichten**, im Abschnitt **Mehrwertsteuer** sicher, dass die richtigen Mehrwertsteuergruppen in den Feldern **Element Mehrwertsteuergruppe** und **Mehrwertsteuergruppe** ausgewählt sind. Wenn die richtigen Steuergruppen nicht ausgewählt sind, wählen Sie sie aus.

    [![Felder „Element Mehrwertsteuergruppe und Mehrwertsteuergruppe“.](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)

2. Gehen Sie zu **Steuern** \> **Direkte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuergruppen**.
3. Wählen Sie die entsprechende Mehrwertsteuergruppe und notieren Sie sich dann auf dem Inforegister **Einrichten** das Steuerkennzeichen im Feld **Umsatzsteuerkennzeichen**.

    [![Mehrwertsteuergruppen Seite.](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)

4. Gehen Sie zu **Steuern** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Element Mehrwertsteuergruppen**.
5. Wählen Sie das entsprechende Element Mehrwertsteuer-Gruppe und stellen Sie dann im Inforegister **Einrichten** sicher, dass das Steuerkennzeichen im Feld **Steuerkennzeichen** mit dem Steuerkennzeichen der Mehrwertsteuergruppe übereinstimmt.

    [![Element Mehrwertsteuergruppen Seite.](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)

6. Wenn die Steuerkennzeichen nicht übereinstimmen, aktualisieren Sie das Mehrwertsteuerkennzeichen für eine der Gruppen.

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a>Überprüfen Sie, dass die ausgewählten Steuerkennzeichen nicht befreit sind und dass sie den richtigen Wert für den Steuersatz haben

Wenn die Steuerkennzeichen befreit sind oder der Steuersatz 0 (Null) ist, ist das Ergebnis der Steuerberechnung 0. Führen Sie diese Schritte aus, um festzustellen, ob die ausgewählten Steuerkennzeichen befreit sind und um zu überprüfen, ob der richtige Steuersatz auf sie angewendet wird.

1. Gehen Sie zu **Steuern** \> **Direkte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuergruppen**.
2. Wählen Sie die entsprechende Mehrwertsteuergruppe aus und stellen Sie dann im Inforegister **Einrichtung** sicher, dass das Kontrollkästchen **Befreit** deaktiviert ist. Wenn er ausgewählt ist, löschen Sie ihn.

    [![Kontrollkästchen „Befreit“ auf der Seite „Mehrwertsteuergruppen“.](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)

3. Wechseln Sie zu **Steuern** \> **Direkte Steuern** \> **Umsatzsteuer** \> **Umsatzsteuercodes**.
4. Wählen Sie das entsprechende Mehrwertsteuerkennzeichen und überprüfen Sie, ob der Wert des Steuersatzes im Feld **Wert** nicht 0 (Null) ist. Wenn es 0 ist, aktualisieren Sie das Feld, so dass es auf den richtigen Steuersatz festgelegt ist.

    [![Feld „Wert“ auf der Seite „Werte für Mehrwertsteuer-Code“.](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a>Bestimmen Sie, ob Null der korrekte Steuerbetrag ist

In einigen Szenarien ist ein Steuerwert von 0 (Null) korrekt. Führen Sie diese Schritte aus, um festzustellen, ob 0 der richtige Steuerbetrag für Ihre Transaktion ist.

1. Gehen Sie zu **Hauptbuch** \> **Hauptbuch einrichten** \> **Hauptbuch-Parameter**.
2. Stellen Sie auf der Registerkarte **Mehrwertsteuer** im Feld **Berechnungsmethode** sicher, dass **Gesamt** ausgewählt ist.

    [![Feld „Berechnungsmethode“ auf der Seite „Parameter Hauptbuch“.](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)

3. Wechseln Sie zu **Steuern** \> **Direkte Steuern** \> **Umsatzsteuer** \> **Umsatzsteuercodes**.
4. Wählen Sie das entsprechende Umsatzsteuerkennzeichen, wählen Sie **Berechnung** \> **Margenbasis**, und überprüfen Sie, ob die Margenbasis auf **Nettobetrag des Rechnungssaldos** oder **Rechnungssumme inkl. sonstiger Umsatzsteuerbeträge** festgelegt ist. Für weitere Informationen, siehe [Rechnungssumme inkl. sonstiger Mehrwertsteuerbeträge](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).
5. Wenn in den Schritten 2 und 4 die richtigen Werte festgelegt wurden, stellen Sie fest, ob der Gesamtbetrag der Transaktion 0 (Null) ist. Wenn der Gesamtbetrag 0 ist, ist ein Steuerbetrag von 0 das erwartete Ergebnis. Da die Steuerberechnung auf dem Gesamtbetrag des Rechnungssaldos basiert und dieser Betrag nicht zeilenweise ist, wird jeder Zeile nach der Steuerberechnung der Steuerbetrag von 0 zugewiesen.

## <a name="determine-whether-customization-exists"></a>Ermitteln Sie, ob eine Anpassung vorliegt

Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist. Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
