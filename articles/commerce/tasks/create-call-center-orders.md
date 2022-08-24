---
title: Callcenteraufträge erstellen
description: Dieser Artikel führt Sie Schritt für Schritt durch das Verfahren, wie ein Callcenterbenutzer in Microsoft Dynamics 365 Commerce einen Kunden nachschlägt, einen neuen Auftrag erstellt, nach einem Produkt sucht und Zahlungen vom Kunden einzieht.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228509"
---
# <a name="create-call-center-orders"></a>Callcenteraufträge erstellen

[!include [banner](../includes/banner.md)]

Dieser Artikel führt Sie Schritt für Schritt durch das Verfahren, wie ein Callcenterbenutzer in Microsoft Dynamics 365 Commerce einen Kunden nachschlägt, einen neuen Auftrag erstellt, nach einem Produkt sucht und Zahlungen vom Kunden einzieht. Diese Prozedur verwendet das Demo-Datenunternehmen USRT und wendet sich an Auftragssachbearbeiter. 

## <a name="prerequisites"></a>Voraussetzungen

Der Benutzer, der das Verfahren bearbeitet, muss als Callcenterbenutzer eingerichtet sein. Optional kann der halbjährliche Fabrikam-Katalog mit mindestens einem Quellcode veröffentlicht werden.

### <a name="add-yourself-as-a-call-center-user"></a>Fügen Sie sich als Callcenterbenutzer hinzu

Um sich selbst als Callcenterbenutzer hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Gehen Sie im Commerce headquarters zu **Einzelhandel und Handel \> Kanäle \> Callcenter \> Alle Callcenter**.
1. Wählen Sie im Feld **Benutzer** **Kanalbenutzer**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie in das Feld **Benutzer-ID** Ihre Benutzer-ID ein.
1. Geben Sie in das Feld **Namen** Ihren Benutzernamen ein. Der Benutzername kann mit der Benutzer-ID identisch sein.
1. Wählen Sie im Aktionsbereich **Speichern** aus.
1. Gehen Sie zurück zu **Einzelhandel und Handel \> Kanäle \> Callcenter \> Alle Callcenter**.
1. Wählen Sie die Retail-Channel-ID des Callcenters aus.
1. Bestätigen Sie, dass die Option **Auftragsabschluss aktivieren** auf **Ja** gestellt ist. Wenn die Option nicht angezeigt wird, können Sie diesen Schritt überspringen.

## <a name="complete-the-example-call-center-procedure"></a>Das Beispiel-Callcenterverfahren durchführen

Führen Sie die folgenden Schritte aus, um das Beispiel-Callcenterverfahren durchzuführen.

1. Navigieren Sie zu **Einzelhandel und Handel \> Kunden \> Kundendienst**.
1. Geben Sie in der Registerkarte **Kundensuche** die Suchkriterien ein, um den Kunden zu suchen. Für dieses Beispielverfahren geben Sie **Karen** ein.
1. Wählen Sie **Suchen** aus. Das Dialogfeld **Kundensuche** wird angezeigt und listet die Suchergebnisse auf.
1. Wählen Sie den Kundendatensatz für **Karen Berg** mit der Debitorenkontonummer hat **2001** und dann **Auswählen** aus.
1. Wählen Sie im Aktivitätsbereich **Neuer Auftrag** aus.
1. Wählen Sie rechts die Registerkarte **Kopfzeile**.
1. Wählen Sie im Inforegister **Lieferung** im Feld **Liefermodus** den Wert **99 Standard**.

    ![Wählen Sie ein Lieferart aus.](../media/Select_Mode_of_Delivery.png)

1. Wählen Sie rechts die Registerkarte **Positionen**.
1. Geben Sie im Abschnitt **Auftragspositionen** in der neuen Zeile für die neue Verkaufsposition im Feld **Artikelnummer** die Artikelnummer ein, nach der gesucht werden soll. Geben Sie für dieses Beispielverfahren **81327** ein und wählen Sie dann das Produkt in der Dropdownliste aus, um es dem Auftrag hinzuzufügen.
1. Geben Sie im Feld **Menge** die Verkaufsmenge ein.
1. Wählen Sie im Feld **Quellcode** den Quellcode für den Katalog aus. Wenn keine aktiven Quellcodes vorliegen, können Sie diesen Schritt überspringen.
1. Wählen Sie im Aktionsbereich **Abschließen**, um die Debitorenzahlung zu erfassen. Diese Aktion öffnet das Dialogfeld **Auftragszusammenfassung**, das den fälligen Gesamtbetrag anzeigt. Die Aktion löst auch die Berechnung etwaiger Kosten wie Versand- und Bearbeitungsgebühren aus und zeigt sie im Dialogfeld **Auftragszusammenfassung** an.

    ![Fertig-Schaltfläche.](../media/Complete_button.png)

1. Wählen Sie im Dialogfeld **Auftragszusammenfassung** auf dem Inforegister **Zahlungen** die Option **Hinzufügen** aus, um die Zahlungen zu erfassen.

    ![Dialogfeld „Auftragszusammenfassung“.](../media/order_summary.png)

1. Wählen Sie im Dialogfeld **Zahlungsinformationen des Kunden eingeben** das Feld **Zahlungsmethode** und dann die Zahlungsmethode aus. Wählen Sie für dieses Beispielverfahren **Bar** aus.
1. Geben Sie im Feld **Zahlungsbetrag** den Zahlungsbetrag ein. Geben Sie für dieses Beispiel **120,00** ein, was dem Auftragssaldo entspricht, der im Dialogfeld **Auftragszusammenfassung** angezeigt wird. Indem Sie diesen Betrag eingeben, können Sie den Auftrag als vollständig bezahlt abzuschließen.
1. Wählen Sie **OK** aus.
1. Wählen Sie **Senden**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Transaktions-E-Mails nach Lieferart anpassen](../customize-email-delivery-mode.md)

[Lieferart in POS ändern](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
