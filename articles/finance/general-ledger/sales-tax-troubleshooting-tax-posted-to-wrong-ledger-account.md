---
title: Die Steuer wird auf das falsche Sachkonto im Beleg gebucht
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die helfen können, wenn die Steuer auf das falsche Sachkonto im Beleg gebucht wird.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6834b460d3a78e47edb2edb7a72651e8454bf0ac
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343813"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Die Steuer wird auf das falsche Sachkonto im Beleg gebucht

[!include [banner](../includes/banner.md)]

Während der Buchung wird die Steuer möglicherweise auf das falsche Sachkonto im Beleg gebucht. Um dieses Problem zu beheben, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus. Die Beispiele in diesem Thema verwenden einen Verkaufsauftrag als Geschäftsdokument.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Suchen Sie das Steuerkennzeichen der fehlerhaft gebuchten steuerlichen Transaktion

1. Wählen Sie auf der Seite **Gutschein-Transaktionen** die Transaktion aus, mit der Sie arbeiten möchten, und wählen Sie dann **Gebuchte Mehrwertsteuer**.

    [![Schaltfläche „Gebuchte Mehrwertsteuer“ auf der Seite „Gutscheintransaktionen“.](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Überprüfen Sie den Wert im Feld **Verkaufssteuer-Code**. In diesem Beispiel ist es **VAT 19**.

    [![Umsatzsteuer-Codefeld auf der Seite „Gebuchte Umsatzsteuer“.](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Prüfen Sie die Buchungsgruppe des Sachkontos für das Steuerkennzeichen

1. Wechseln Sie zu **Steuern** \> **Direkte Steuern** \> **Umsatzsteuer** \> **Umsatzsteuercodes**.
2. Suchen und wählen Sie den Steuercode und überprüfen Sie den Wert im Feld **Sachkonto-Buchungsgruppe**. In diesem Beispiel ist es **Mehrwertsteuer**.

    [![Feld „Buchungsgruppe des Sachkontos“ auf der Seite „Mehrwertsteuer-Codes“.](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. Der Wert im Feld **Sachkonto-Buchungsgruppe** ist eine Verknüpfung. Um die Details der Konfiguration der Gruppe zu sehen, wählen Sie den Link. Alternativ können Sie das Feld auswählen und halten (oder mit der rechten Maustaste darauf klicken) und dann **Details anzeigen** wählen.

    [![Befehl „Details anzeigen“.](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Überprüfen Sie im Feld **Zahlbare Mehrwertsteuer**, ob die Kontonummer entsprechend der Art der Transaktion korrekt ist. Wenn dies nicht der Fall ist, wählen Sie das richtige Konto aus, auf das gebucht werden soll. In diesem Beispiel soll die Mehrwertsteuer des Verkaufsauftrags auf das Konto 222200 Umsatzsteuerverbindlichkeit gebucht werden.

    [![Feld „Umsatzsteuerverbindlichkeit“ auf der Seite „Sachkontobuchungsgruppen“.](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    Die folgende Tabelle enthält Informationen zu den einzelnen Feldern auf der Seite **Sachkonten-Buchungsgruppen**.

    | Feld                  | Beschreibung |
    |------------------------|-------------|
    | Mehrwertsteuer      | Das Hauptkonto für ausgehende Mehrwertsteuern, die an die Steuerbehörde zu zahlen sind. |
    | Vorsteuer   | Das Hauptkonto für eingehende Steuern, die von der Steuerbehörde empfangen werden. |
    | Erwerbsteuerabgaben        | Das Hauptkonto, das verwendet wird, um abzugsfähige Nutzungssteuern zu buchen, die Kreditor nicht geltend machen oder an die Steuerbehörde melden, als Teil der EU-Reverse-Charge-Steuer auf Waren und Dienstleistungen (GST)/Harmonisierte Mehrwertsteuer (HST). **Steuer verwenden** – Wählen Sie für das Mehrwertsteuer-Kennzeichen in der Mehrwertsteuergruppe, die in der Transaktion verwendet wird. Dieses Feld ist nicht verfügbar, wenn **Steuerungsregeln für die Mehrwertsteuer anwenden** auf der Seite **Hauptbuch-Parameter** ausgewählt ist. |
    | Gegenkonto Erwerbsteuerabgaben        | Das Hauptkonto, das verwendet wird, um eingehende Nutzungssteuern zu buchen, die an die Steuerbehörden zu zahlen sind. |
    | Ausgleichskonto     | Das Hauptkonto, das verwendet wird, um den Nettosaldo der Sachkonten zu buchen, die in den Feldern **Gebrauchssteuer zahlbar** und **Verkaufssteuer forderbar** angegeben sind. |
    | Kreditorenskonto   | Das Hauptkonto, das zum Buchen eines Skontos für Mehrwertsteuerkennzeichen verwendet wird, die mit dieser Buchungsgruppe verbunden sind. |
    | Kundenfall-Rabatt | Das Hauptkonto, das zum Buchen eines Skontos für Mehrwertsteuerkennzeichen verwendet wird, die mit dieser Buchungsgruppe verbunden sind. |

    Weitere Informationen finden Sie unter [Sachkonto-Buchungsgruppen für Mehrwertsteuer festlegen](tasks/set-up-ledger-posting-groups-sales-tax.md).

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Debuggen im Code, um Dimensionen des Sachkontos zu prüfen

Im Code wird das Buchungskonto durch die Dimension des Ledgers bestimmt. Die Ledger Dimension speichert die Datensatz-ID eines Kontos in der Datenbank.

1. Fügen Sie für einen Verkaufsauftrag einen Haltepunkt bei den Methoden **Steuer::saveAndPost()** und **Steuer::post()** ein. Achten Sie auf den Wert von **\_ledgerDimension**.

    [![Beispiel für einen Verkaufsauftragscode mit Haltepunkt.](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Fügen Sie für eine Einkaufsbestellung einen Haltepunkt bei den Methoden **TaxPost::saveAndPost()** und **TaxPost::postToTaxTrans()** ein. Achten Sie auf den Wert von **\_ledgerDimension**.

    [![Beispiel für einen Code zur Einkaufsbestellung mit Haltepunkt.](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Führen Sie die folgende SQL-Abfrage aus, um den Anzeigewert des Kontos in der Datenbank zu finden, basierend auf der Datensatz-ID, die von der Dimension „Ledger“ gespeichert wird.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Anzeigewert der Datensatz-ID.](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Untersuchen Sie den Callstack, um herauszufinden, wo der Wert **_ledgerDimension** zugewiesen ist. Normalerweise ist der Wert von **TmpTaxWorkTrans**. In diesem Fall sollten Sie einen Haltepunkt bei **TmpTaxWorkTrans::insert()** und **TmpTaxWorkTrans::update()** einfügen, um herauszufinden, wo der Wert zugeordnet wurde.

## <a name="determine-whether-customization-exists"></a>Ermitteln Sie, ob eine Anpassung vorliegt

Wenn Sie die Schritte in den vorherigen Abschnitten ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist. Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
