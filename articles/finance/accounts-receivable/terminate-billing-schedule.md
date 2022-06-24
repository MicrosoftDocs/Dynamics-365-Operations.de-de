---
title: Beenden von Abrechnungsplänen
description: Dieser Artikel erklärt, wie Sie Abrechnungspläne und Abrechnungseinteilungen in der Abonnementabrechnung beenden können.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 4fce23f3cf35ef8c388ce13fc422f268a2bd8e32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872556"
---
# <a name="terminate-billing-schedules"></a>Beenden von Abrechnungsplänen

[!include [banner](../includes/banner.md)]

Dieser Artikel erklärt, wie Sie Abrechnungspläne und Abrechnungseinteilungen in der Abonnementabrechnung beenden können. Wenn Sie einen Abrechnungsplan beenden, muss er den Status **Aktiv** haben. Sie kann nicht den Status **In der Warteschleife** haben. Ebenso muss eine Rechnungseinteilung, wenn Sie sie beenden, den Status **Aktiv** haben. Der Kopfbereich des Fakturierungsplans ist nicht betroffen, wenn Sie eine Fakturierungseinteilung beenden.

Um einen Rechnungsplan oder eine Rechnungseinteilung zu beenden, gehen Sie zu einer der folgenden Stellen:

- Die Seite **Alle/Aktive Fakturierungszeitpläne** Liste
- Ein spezifischer Fakturierungsplan auf der Seite **Alle Fakturierungspläne**
- Eine bestimmte Zeile des Fakturierungsplans auf der Seite **Alle Fakturierungspläne**

> [!NOTE]
> Wenn Sie mehrere Abrechnungspläne gleichzeitig kündigen möchten, verwenden Sie die Seite **Massenkündigungsverarbeitung**.

## <a name="terminate-a-billing-schedule-or-line"></a>Beenden eines Rechnungsplans oder einer Zeile

Um einen Fakturierungsplan oder eine Fakturierungseinteilung zu beenden, führen Sie diese Schritte aus.

1. Markieren Sie einen Fakturierungsplan oder eine Fakturierungseinteilung und wählen Sie dann **Beenden**. 
2. Legen Sie die Felder **Kündigungsdatum**, **Kündigungsart** und **Ursachencode** fest.
3. Legen Sie das Feld **Gutschriftoption** auf **Gutschrift erteilen** fest.
4. Wählen Sie **Beenden**.

Der Status des Abrechnungsplans ändert sich je nach der von Ihnen gewählten Terminierungsart. Wenn Sie als Beendigungsart **Restabrechnung** gewählt haben, lautet der Status aller Zeilen des Abrechnungsplans **Letzte Abrechnung**. Der Status des Abrechnungsplans bleibt **Aktiv**, bis die letzte Rechnung verarbeitet ist. Nachdem die letzte Rechnung verarbeitet wurde, wird der Status auf **Beendet** aktualisiert. Wenn Sie **Zeitplan anpassen** als Beendigungsart gewählt haben, wird der Status des Abrechnungszeitplans sofort auf **Beendet** aktualisiert.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Beenden Sie einen Fakturierungsplan oder eine Zeile und wenden Sie eine Rückerstattung an

Um einen Fakturierungsplan oder eine Fakturierungseinteilung zu beenden und eine Rückerstattung vorzunehmen, gehen Sie folgendermaßen vor.

1. Markieren Sie einen Fakturierungsplan oder eine Fakturierungseinteilung und wählen Sie dann **Beenden**.
2. Legen Sie die Felder **Beendigungsdatum**, **Beendigungstyp**, **Ursachencode** und **Guthabenoption** fest.
3. Wählen Sie **Mit Rückerstattung abschließen**. Die Seite **Massenterminierungsverarbeitung** wird angezeigt und ist so gefiltert, dass sie den Abrechnungsplan anzeigt.
4. Wählen Sie **Vorschau anzeigen**, um die Fakturierungseinteilungen anzuzeigen, und wählen Sie dann **Verarbeiten**.

Nachdem die Gutschrift verarbeitet wurde, öffnen Sie die Seite **Abrechnungsdetails anzeigen**, um die Gutschrift zu überprüfen, die auf den Abrechnungsplan angewendet wurde. Beträgt der Guthabenbetrag mehr als 0 (Null), werden alle zukünftigen nicht abgerechneten Zeilen gelöscht und durch Abrechnungsdetailzeilen ersetzt, die die negativen Beträge für das Guthaben ausweisen, das auf den Abrechnungsplan angewendet wurde.

### <a name="view-example"></a>Beispiel anzeigen

Ein Rechnungsplan enthält die folgenden Informationen:

- Das Startdatum ist der 1. Januar 2020.
- Das Enddatum ist der 31. Dezember 2020.
- Der Betrag für den Abrechnungszeitraum beträgt 100,00 pro Monat.
- Rechnungen wurden für Abrechnungszeiträume von Januar bis Juli erstellt.
- Das Vertragsende ist der 15. Juni 2020.

Wenn die Gutschriftsanpassung verarbeitet ist, werden alle zukünftigen Abrechnungszeiträume (August bis Dezember) von der Seite **Abrechnungsdetails anzeigen** entfernt. Nach dem Abrechnungszeitraum Juli wird eine Zeile für die Kreditanpassung hinzugefügt:

- 16. Juni - 31. Juli, mit einem Guthaben von 150,00

Wenn die Funktion für nicht fakturierte Umsätze verwendet wird, wird die Seite **Prüfung des Journaleintrags für nicht fakturierte Umsätze** mit dem Abschlusseintrag aktualisiert.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Beenden Sie einen Fakturierungsplan oder eine Zeile, ohne eine Gutschrift vorzunehmen

Um einen Fakturierungsfahrplan oder eine Fakturierungseinteilung zu beenden, ohne eine Gutschrift anzuwenden, führen Sie diese Schritte aus.

1. Markieren Sie einen Fakturierungsplan oder eine Fakturierungseinteilung und wählen Sie dann **Beenden**.
2. Legen Sie das Feld **Beendigungsdatum** fest.
3. Legen Sie das Feld **Kündigungsart** auf **Keine Anpassung** fest. Das Feld **Gutschriftoption** wird automatisch auf **Keine Gutschrift** festgelegt.
3. Legen Sie das Feld **Ursachencode** fest.
4. Geben Sie in das Feld **Beendigungsnotizen** alle erforderlichen Notizen ein.
5. Wählen Sie **Beenden**. 

Wenn die Kündigung verarbeitet wird, werden alle Zeilen der Rechnungsdetails nach dem Kündigungsdatum entfernt. (Zu diesen Zeilen gehört auch die Zeile, die das Beendigungsdatum enthält.) Für die beendeten Zeilen können keine Rechnungen erstellt werden. Wird der Abbruch entfernt, werden alle abgebrochenen Zeilen wieder auf der Seite **Abrechnungsdetails anzeigen** hinzugefügt und stehen für die Rechnungsstellung zur Verfügung.

## <a name="fields"></a>Felder

Die Seite **Rechnungsdetails ansehen** enthält die folgenden Felder.

| Feld | Description |
|-------|-------------| 
| Kündigungsdatum | Wählen Sie das Datum, an dem Sie einen Abrechnungszeitplan oder eine Abrechnungseinteilung beenden möchten. |
| Kündigungstyp | <p>Wählen Sie die Art der Beendigung:</p><ul><li>**Zeitplan anpassen** - Schneiden Sie die Abrechnungszeiträume für die Zeile zum Kündigungsdatum ab und ändern Sie den Status der Zeile auf **Letzte Abrechnung**. Wenn für die Zeile ein Abgrenzungsplan existiert, wird er angepasst, indem der Betrag, der nicht mehr verbucht werden darf, storniert wird. Wenn das Startdatum der Abrechnung nach dem Kündigungsdatum liegt, werden die verbleibenden Abrechnungszeiträume entfernt.</li><li>**Restliche Rechnung** - Addiert den verbleibenden Betrag für den Abrechnungszeitraum zur Kündigungsfrist und ändert den Status der Zeile in **Letzte Rechnung**. Wenn für die Zeile ein Abgrenzungsplan vorhanden ist, wird das Enddatum der Abgrenzung aktualisiert. Liegt das Startdatum der Abrechnung nach dem Kündigungsdatum, wird der Gesamtbetrag aller verbleibenden Abrechnungszeiträume zum Abrechnungszeitraum addiert und die verbleibenden Abrechnungszeiträume werden entfernt.</li><li>**Keine Anpassung** - Beenden Sie die Abrechnungsperioden für die Zeile zum angegebenen Beendigungsdatum. Es werden keine Anpassungen vorgenommen. Wenn diese Kündigungsart ausgewählt ist, wird das Feld **Gutschriftoption** auf **Keine Gutschrift** festgelegt und das Feld **Täglich wiederholen** auf **Nein**. Diese beiden Felder sind dann schreibgeschützt und können nicht mehr geändert werden.</li></ul> |
| Kreditoption | <p>Wählen Sie aus, wie das Guthaben verwendet werden soll, wenn Sie eine Abrechnungseinteilung beenden:</p><ul><li>**Gutschriftsanpassung** - Erzeugt eine Gutschriftsanpassung für einen Abrechnungsplan, wenn eine Zeile beendet wird. Die Gutschriftsanpassung erscheint in einem zukünftigen Abrechnungszeitraum für den Abrechnungsplan. Die Anpassung passt auch automatisch den Rechnungsbetrag für den nächsten Abrechnungszeitraum an, bis das Guthaben im Abrechnungsplan fertiggestellt ist.</li><li>**Gutschrift erstellen** - Erzeugt eine Gutschrift, wenn eine Rechnungseinteilung oder eine Rechnungseinteilungszeile beendet wird.</li><li>**Keine Gutschrift** - Erzeugt keine Gutschriftsanpassung oder eine Gutschrift, wenn ein Abrechnungsschema oder eine Abrechnungseinteilung beendet wird. Diese Option ist nur verfügbar, wenn Sie eine Beendigung vom Typ **Keine Anpassung** verwenden, um einen Abrechnungsplan zu beenden.</li></ul><p>Die Standardoption stammt von der Seite **Parameter für wiederkehrende Vertragsabrechnungen**.</p> |
| Ursachencode | Wählen Sie den Ursachencode für die Beendigung. |
| Beschreibung der Ursache | Die Beschreibung des Ursachencodes. |
| Kündigungshinweise | Geben Sie eventuelle Notizen zur Beendigung ein. |

<!--## Additional information-->
