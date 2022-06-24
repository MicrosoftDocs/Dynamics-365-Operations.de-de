---
title: Übersicht über Buchungsprofile
description: In diesem Artikel wird erläutert, wie Buchungsprofile durchgehend in Microsoft Dynamics 365-Apps verwendet werden.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7ef3be13e82ff3722fc81247b5cd581b0b571b0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876123"
---
# <a name="posting-profiles-overview"></a>Übersicht über Buchungsprofile

In Apps für Finanzen und Betrieb wird der Begriff *Buchungsprofile* verwendet, um die Konfigurationen zu beschreiben, die steuern, wie Nebenbuchkonten in Hauptkonten konvertiert werden, damit sie in Transaktionen verwendet werden können, die in das Hauptbuch gebucht werden. Sie steuern beispielsweise, wie der Debitor beim Buchen einer Rechnung in ein Hauptkonto der Debitorenbuchhaltung umgewandelt wird.

Einige Module und Funktionen haben eine Seite, deren Name das Wort „Buchungsprofil“ enthält (z. B. **Buchungsprofil des Kunden** oder **Buchungsprofil des Anbieters**). Darüber hinaus verfügen einige Module über mehrere Optionen zum Konfigurieren der Hauptbuchbuchung für Transaktionen, die aus dem Nebenbuch generiert werden. Im Modul **Produktionskontrolle**, zum Beispiel, können Sie die Buchung nach Produktionsgruppe, Ressource oder Ressourcengruppe einrichten.

Beachten Sie, dass es für viele Transaktionstypen eine Alternative zu Buchungsprofilen gibt: Buchungsdefinitionen. Für unterstützte Dokumente können Sie Buchungsdefinitionen anstelle von Buchungsprofilen verwenden, um Hauptkonten und Finanzdimensionen für Buchhaltungseinträge zu klassifizieren. Wenn Sie beabsichtigen, Belastungen oder Vorbelastungen zu verwenden, ist eine Buchungsdefinition erforderlich, um die Konten für die Buchungen zu definieren.

Bevor Sie die Buchungsprofile, Buchungsdefinitionen oder die **Konten für automatische Transaktionen**-Seite konfigurieren können, müssen Sie den Kontenplan auf der Seite **Hauptbuch** in der juristischen Person konfigurieren, die Sie konfigurieren möchten.

## <a name="posting-types"></a>Buchungstypen

In Apps für Finanzen und Betrieb wird ein Buchungstyp verwendet, um eine allgemeine Kategorie für ein Soll oder ein Haben zu definieren. Diese Kategorie ist unabhängig vom Hauptkonto im Hauptbuch. Es gibt Buchungstypen für jedes Soll oder Haben im Hauptbuch.

Ein einzelner Beleg kann eine oder mehrere Buchungstypen haben. Eine Transaktion, die über ein allgemeines Journal gebucht wird, bei dem das Konto und das Gegenkonto auf **Hauptbuch** eingestellt sind, hat beispielsweise den Buchungstyp **Ledger-Journal** sowohl für Soll und Haben. Im Gegensatz dazu hat eine Kreditorenrechnung mehrere Buchungstypen. Diese Buchungstypen enthalten eine Zeile für den Kreditorensaldo und zusätzliche Zeilen für die Gegenbuchung, wie **Ledger-Journal**.

Sie können den Buchungstyp im **Buchungstyp**-Feld auf der **Allgemein**-Registerkarte der **Belegtransaktionen**-Seite anzeigen.

> [!TIP]
> Sie können die Symbolleiste **Personalisierung** benutzen, um das **Buchungstyp**-Feld in das Raster auf der **Übersicht**-Registerkarte hinzuzufügen, oder um es zu verschieben. Auf diese Weise können Sie dieses Feld beim Anzeigen von Belegen leichter zugänglich oder sichtbar machen.

## <a name="detail-settings-for-a-posting-profile"></a>Detaileinstellungen für ein Buchungsprofil 

Wenn Sie Buchungsprofile konfigurieren, definiert das **Konto-Code**-Feld die Stufe der Einstellung. Die folgenden Optionen sind verfügbar: **Tabelle**, **Gruppe** und **Alle**. Der Abgleich endet nach dem ersten Treffer, und die Reihenfolge beginnt bei der spezifischsten Ebene bis zur unspezifischsten Ebene. Obwohl das **Konto-Code**-Feld in einigen Fällen einen etwas anderen Namen haben kann, bleiben das Verhalten und die Funktion des Felds gleich. Beispielsweise enthält das Bestandsbuchungsprofil ein **Produktcode**-Feld und ein **Konto-Code**-Feld. Beide Felder haben Werte für **Tabelle**, **Gruppe** und **Alle**.

Wenn das **Hauptkonto**-Feld für ein Buchungsprofil leer gelassen wird und Sie kein Hauptkonto auf der **Konten für automatische Transaktionen**-Seite oder auf einer modulspezifischen oder funktionsspezifischen Seite konfiguriert haben, erhalten Sie eine Fehlermeldung, wenn Sie eine Transaktion buchen, die den Buchungstyp verwendet. Normalerweise lautet die Nachricht: „Das Konto für \[Buchungstyp\] kann nicht gefunden werden.“

### <a name="table-value"></a>Tabellenwert

Der **Tabelle**-Wert bezieht sich auf den Stammsatz, der dem Buchungsprofil zugeordnet ist. Jeder Tabellendatensatz ist spezifisch für einen Wert. Sie geben diesen Wert in dem Feld an, das nach dem **Konto-Code**-Feld angezeigt wird. Normalerweise wird dieses Feld als **Konto** oder **Konto-/Gruppennummer** bezeichnet. Der genaue Name variiert je nach Seite, auf der es angezeigt wird.

Wenn Sie beispielsweise mit einem Kundenbuchungsprofil arbeiten, steht der **Tabelle**-Wert für einen bestimmten Kunden. Wenn Sie daher im Feld **Kontocode** die Option **Tabelle** auswählen, müssen Sie die Debitorennummer im Feld **Konto-/Gruppennummer** auswählen.

Der **Tabelle**-Wert stellt den spezifischsten Datensatztyp dar. Das System verwendet immer diesen Wert, auch wenn Sie einen anderen Datensatz konfiguriert haben, in dem der Wert **Gruppe** oder **Alle** ausgewählt ist. Dieser Wert überschreibt auch alle Werte, die Sie als Standardwerte auf der Seite **Konten für automatische Transaktionen** erstellt haben.

Wir empfehlen nicht, den **Tabelle**-Wert als primären Mechanismus zur Verwaltung Ihrer Buchungsprofile zu verwenden, da Datenqualitätsprobleme auftreten können, wenn für jeden Stammdatensatz ein separates Buchungsprofil gepflegt wird. Außerdem ist es schwierig, für jeden Stammdatensatz ein separates Buchungsprofil zu pflegen und abzugleichen. Stattdessen sollte dieser Wert verwendet werden, um Ausnahmen in Ihren Buchungsprofilen zu verwalten.

### <a name="group-value"></a>Gruppenwert

Der **Gruppe**-Wert bezieht sich auf den Gruppierungssatz, der von dem Stammsatz unterstützt wird, der dem Buchungsprofil zugeordnet ist. Jeder Gruppendatensatz ist spezifisch für einen Wert. Sie geben diesen Wert in dem Feld an, das nach dem **Konto-Code**-Feld angezeigt wird. Normalerweise wird dieses Feld als **Konto** oder **Konto-/Gruppennummer** bezeichnet. Der genaue Name variiert je nach Seite, auf der es angezeigt wird.

Der **Gruppe** -Wert erfordert, dass Sie zuerst eine Gruppe konfigurieren und sie mit einem oder mehreren Datensätzen für das Konto verknüpfen. Der **Gruppe**-Wert ist weniger spezifisch als der **Tabelle**-Wert, aber spezifischer als der **Alle**-Wert. Wenn für eine Tabelle kein Datensatz konfiguriert wurde, versucht das System, einen Datensatz für die Gruppe zu finden, zu der der Datensatz gehört.

Wenn Sie beispielsweise mit einem Kundenbuchungsprofil arbeiten und **Gruppe** in dem **Konto-Code**-Feld auswählen, müssen Sie im **Konto-/Gruppennummer**-Feld eine Kundengruppe auswählen. Sie müssen die Kundengruppen auf der **Kundengruppe**-Seite vordefinieren und eine Kundengruppe angeben, wenn Sie einen Kunden erstellen.

Wenn Sie mehrere Hauptkonten für einen bestimmten Buchungstyp verfolgen müssen, empfehlen wir Ihnen, den **Gruppe**-Wert zu verwenden. Beispiel: Sie haben drei Hauptkonten der Debitorenbuchhaltung: eines für Stammkunden, eines für Mitarbeiter und eines für konzerninterne Verkäufe. In diesem Fall empfehlen wir, dass Sie drei Kundengruppen erstellen, um die Kunden zu segmentieren. Ordnen Sie dann jede Kundengruppe dem richtigen Hauptkonto im Kundenbuchungsprofil zu. Die folgende Tabelle zeigt die drei Kundengruppen für dieses Beispiel.

| Debitorengruppe | Name | Description |
|----------------|------|-------------|
| EXT | Externer Kunde | Diese Gruppe wird für alle standardmäßigen externen Kunden verwendet. |
| EMP | Mitarbeiter | Diese Gruppe wird für alle Mitarbeiter verwendet, die bei Ihrer Organisation einkaufen. |
| INT | Intercompany-Verkauf | Diese Gruppe wird für alle Intercompany-Kundenkonten verwendet, die mit Integrationsverkäufen und -bestellungen verwendet werden. |

Im Buchungsprofil richten Sie dann drei Zeilen ein. In jeder Zeile wählen Sie den **Gruppe**-Wert und das zugehörige Hauptkonto aus.

### <a name="all-value"></a>Alle-Wert

Der **Alle**-Wert gibt an, dass die Einstellungen für alle Datensätze gelten. Wenn Sie den **Alle**-Wert im **Konto-Code**-Feld auswählen, ist das **Konto-/Gruppennummer**-Feld nicht verfügbar, und Sie können keinen bestimmten Datensatz auswählen, auf den die Konfiguration angewendet werden soll.

Der **Alle**-Wert ist der am wenigsten spezifische Wert. Er wird nur verwendet, wenn das System keine Übereinstimmung für den **Tabelle**- oder **Gruppe**-Wert finden kann. Sie sollten den **Alle**-Wert auswählen, wenn Sie nur ein Hauptkonto für einen bestimmten Buchungstyp haben.

Wenn Sie beispielsweise mit einem Kundenbuchungsprofil arbeiten, gelten die von Ihnen angegebenen Hauptkonten für alle anderen Kunden und Kundengruppen, die keinen Datensatz für eine bestimmte Tabelle (Kunde) oder Gruppe (Kundengruppe) haben.

### <a name="category"></a>Kategorie

Bestandsbuchungsprofile haben einen zusätzlichen Wert, der für die Verkaufskategorie oder die Beschaffungskategorie spezifisch ist. Dieser Wert ähnelt dem **Tabelle**-Wert, da er nur für eine bestimmte Verkaufs- oder Beschaffungskategorie gilt.

### <a name="default-value"></a>Standardwert

Wenn Sie keinen Datensatz für einen Buchungstypen in einem Buchungsprofil erstellen, in dem das **Konto Code**-Feld auf **Alle** eingestellt ist, und das System keinen passenden Buchungsprofildatensatz für den **Gruppe**- oder **Tabelle**-Wert finden kann, kehrt das System zu dem Standardwert zurück, der auf der **Konten für automatische Transaktionen**-Seite angegeben werden kann. Weitere Informationen finden Sie unter [Konten für automatische Transaktionen](accounts-for-auto-transactions.md).

## <a name="clearing-accounts"></a>Verrechnungskonten

Der Begriff *Verrechnungskonto* wird in der Buchhaltung häufig verwendet. Einige Buchungstypen in Microsoft Dynamics 365-Apps bereinigen Konten. Mit anderen Worten, der Saldo auf dem Konto wird ausgeglichen oder storniert, wenn eine weitere Transaktion gebucht wird. Wenn Sie beispielsweise einen Produktzugang für eine Bestellung buchen, wird die Summe der geschätzten Kosten der Produkte zuzüglich Steuern und etwaiger Belastungen in den Bestellpositionen als Verbindlichkeit in den Buchungstyp für Kaufabgrenzungen gebucht. Später, wenn Sie die Bestellung fakturieren, wird der Saldo aus dem Buchungstyp für die Einkaufsabgrenzung storniert und auf das Handelskonto der Kreditorenbuchhaltung verschoben.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

Viele Module in Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce und Dynamics 365 Project Operations verfügen über ein Buchungsprofil oder zusätzliche Konfigurationen, die steuern, wie die Buchung ins Hauptbuch funktioniert. Verwenden Sie die folgenden Themen, um mehr über die Buchungsprofile und Buchungseinstellungen in jedem Modul zu erfahren:

- [Konten für automatische Buchungen](accounts-for-auto-transactions.md)
- [Kreditorenkontenbuchung](accts-payble-posting.md)
- [Debitorenbuchung](accts-recvble-posting.md)
- [Anlagenleasingbuchung](../asset-leasing/set-up-lease-posting-accts.md)
- Anlagenverwaltungsbuchung (demnächst verfügbar)
- Bargeld- und Bankverwaltung (demnächst verfügbar)
- Buchungskonten für die Währungsneubewertung (demnächst verfügbar)
- Ausgabenverwaltungsbuchung (demnächst verfügbar)
- [Anlagevermögenbuchungsprofil](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- Intercompany-Buchhaltungsbuchung (demnächst verfügbar)
- Bestandsbuchungsprofil (demnächst verfügbar)
- [Buchen von Gesamttransportkosten](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [Übersicht über Buchungsdefinitionen](posting-definitions.md)
- Produktionskontrollbuchung (demnächst verfügbar)
- Projektverwaltung und Buchhaltungsbuchung (demnächst verfügbar)
- Dienstverwaltungsbuchung (demnächst verfügbar)
- Steuerbuchung (demnächst verfügbar)
- Zeit- und Anwesenheitsbuchung (demnächst verfügbar)
- Transportverwaltungsbuchung (demnächst verfügbar)
- Buchungsprofile für die Rabattverwaltung (demnächst verfügbar)
