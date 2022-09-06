---
title: Unternehmensübergreifende Datenfreigabe für Geschenkkarten
description: Dieser Artikel beschreibt, wie Sie Microsoft Dynamics 365 Commerce so konfigurieren, dass Sie die Funktionalität zur Datenfreigabe von Dynamics 365 Finance über Datenbereiche hinweg verwenden können, um Geschenkkartendaten zu synchronisieren.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387067"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Unternehmensübergreifende Datenfreigabe für Geschenkkarten

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dieser Artikel beschreibt, wie Sie Microsoft Dynamics 365 Commerce so konfigurieren, dass es die Funktionalität zur Datenfreigabe von Dynamics 365 Finance nutzt, um Geschenkkartendaten zu synchronisieren. Die Funktionalität zur Datensatzfreigabe kann dann genutzt werden, um Daten unternehmensübergreifend zwischen zwei Datenbereichen zu teilen. Auf diese Weise kann die interne Commerce-Geschenktabelle Daten zwischen zwei Unternehmensentitäten austauschen. Weitere Informationen zur unternehmensübergreifenden Datenfreigabe in Dynamics 365 Finance finden Sie unter [Unternehmensübergreifende Datenfreigabe](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

## <a name="key-terms"></a>Schlüsselbegriffe

| Zeitdauer | Description |
|---|---|
| Firma | Die juristische Person in der Dynamics 365 Finance-Umgebung. |
| Geschenkkarte | Das interne Dynamics 365 Commerce Geschenkkartenprodukt. |

## <a name="prerequisites"></a>Voraussetzungen

Benutzer müssen ihre Umgebung für die unternehmensübergreifende Datenfreigabe, wie in [Unternehmensübergreifende Datenfreigabe](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing) beschrieben, konfigurieren.

In **RetailGiftCardTable** muss das Feld **DataSharingType** auf **Duplikat** festgelegt sein, um die Freigabe doppelter Datensätze (DRS) für die Geschenkkartentabelle aktivieren. Weitere Informationen finden Sie unter [Unternehmensübergreifende Datenfreigabe für Entwickler](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev).

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Unternehmensübergreifende Datenfreigabe für Geschenkkarten konfigurieren

Gehen Sie wie folgt vor, um die unternehmensübergreifende Datenfreigabe für Geschenkkarten zu konfigurieren.

1. Gehen Sie in Commerce headquarters zu **Systemverwaltung \> Einstellungen \> Unternehmensübergreifende Datenfreigabe konfigurieren**.
1. Um einen Datenfreigabedatensatz hinzuzufügen, wählen Sie im Aktionsbereich **Neu** aus.
1. Geben Sie im Feld **Name** einen Namen für den Datenfreigabedatensatz ein (z. B. **Geschenkkarten**).
1. Wählen Sie in dem Abschnitt **Freizugebende Tabellen und Felder** **Hinzufügen** aus.
1. Geben Sie im Dialogfeld **Neue Tabelle freigeben** im Feld **Tabellenname** **RETAILGIFTCARDTABLE** ein (die Tabelle für Einzelhandelsgeschenkkarten). Das Feld **Tabellenbezeichnung** sollte automatisch auf **Geschenkkartentabelle** festgelegt sein.
1. Stellen Sie sicher, dass die Kontrollkästchen **Daten nach Unternehmen speichern**, **Hat eindeutigen Index** und **Noch nicht freigegeben** alle aktiviert sind. Die Auswahl dieser Kontrollkästchen löst Prüfungen aus, die sich auf die Funktionalität der Datenfreigabe beziehen.
1. **Tabelle hinzufügen** auswählen. Der Datensatz **Geschenkkartentabelle (RetailGiftCardTable)** sollte jetzt unter **Freizugebende Tabellen und Felder** erscheinen. Wählen Sie das Caret-Zeichen (^) aus, um alle Tabellenfelder anzuzeigen, die automatisch mit der Tabelle für die Freigabe verknüpft sind.
1. Wählen Sie im Abschnitt **Unternehmen, die die Datensätze in diesen Tabellen teilen** **Hinzufügen** aus, um ein Unternehmen hinzuzufügen, mit dem Daten geteilt werden sollen.
1. Wählen Sie in der Zeile darunter **Unternehmen** ein Unternehmen aus der Dropdownliste aus.
1. Geben Sie im Feld **Name** den Unternehmensnamen ein.
1. Wiederholen Sie die Schritte 8 bis 10, um weitere Unternehmenszeilen hinzuzufügen.
1. Wenn Sie mit dem Hinzufügen von Unternehmenszeilen fertig sind, wählen Sie im Aktionsbereich **Aktivieren** aus.
1. Sie erhalten eine Warnmeldung, die besagt: „Es wird empfohlen, diese Aktion nur außerhalb der Geschäftszeiten durchzuführen. Alle gleichzeitigen Buchungsvorgänge schlagen für Tabellen in der Richtlinie fehl. Möchten Sie den Vorgang fortsetzen?“ Wählen Sie **Ja** aus, um Ihre Zustimmung zu erteilen.
1. Sie erhalten folgende Warnmeldung: „Möchten Sie jetzt alle vorhandenen Daten in alle freigegebenen Unternehmen kopieren?“ Wählen Sie **Ja** aus, um Ihre Zustimmung zu erteilen.

Nachdem Sie beiden Meldungen zugestimmt haben, beginnen die Tabellen damit, Daten über die konfigurierten Unternehmen hinweg zu kopieren. Guthaben, die auf einer Unternehmensgeschenkkarte anfallen, sind dann für das andere Unternehmen sichtbar.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[FAQs zu Zahlungen](payments-retail.md)

[Auschecken-Modul](../add-checkout-module.md)

[Zahlungsmodul](../payment-module.md)
