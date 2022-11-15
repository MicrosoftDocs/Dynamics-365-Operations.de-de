---
title: Debitorenteilung bei Abrechnungszeitplänen
description: In diesem Artikel wird beschrieben, wie Sie einen Kunden aufteilen, wenn die Abonnementabrechnung verwendet wird.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746314"
---
# <a name="customer-split-on-billing-schedules"></a>Debitorenteilung bei Abrechnungszeitplänen

Auf einem Abrechnungsplan ist das *Rechnungskonto* der Kunde, der die Auftragsrechnung erhält, damit er die Rechnung bezahlen kann. In einigen Szenarien kann mehr als ein Kunde eine Rechnung bezahlen. Mit der **Kundenaufteilung** Funktion können Sie weitere Kunden hinzufügen, denen derselbe Abrechnungszeitplan in Rechnung gestellt werden kann. Um diese Funktion zu aktivieren, gehen Sie zu **Abonnementabrechnung \> Wiederkehrende Vertragsabrechnung \> Konfiguration \> Wiederkehrende Vertragsabrechnungsparameter**, und stellen Sie die Option **Kundenaufteilung** auf **Ja** ein.

## <a name="customer-split-on-the-billing-schedule-header"></a>Debitorenteilung auf der Abrechnungszeitplankopfzeile

Nachdem ein Abrechnungszeitplan erstellt wurde, können weitere Kunden zum Kopf des Abrechnungszeitplans hinzugefügt werden.

Um einen Kunden hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Wählen Sie auf der Registerkarte **Abrechnungsplan** die Option **Debitorenteilung**. Die Felder **Kundenkonto** und **Name des Kundenkontos** oben geben den Kunden an, der als **Abrechnungsplankunde** zugewiesen ist.

    > [!NOTE]
    > Das hinzugefügte Kundenkonto darf nicht mit dem Rechnungskonto identisch sein.

2. Wählen Sie auf der Registerkarte **Positionen der Debitorenteilung** die Option **Position hinzufügen**.
3. Wählen Sie einen Kunden aus und geben Sie dann den Prozentsatz jeder Rechnung für diesen Kunden ein.
4. Standardmäßig werden die Start- und Enddaten des Abrechnungszeitplans als Start- und Enddaten verwendet. Geben Sie unterschiedliche Start- und Enddaten ein, wenn der neue Kunde den angegebenen Prozentsatz nur für einen Teil des Abrechnungszeitraums zahlt. Wenn der Abrechnungszeitplan beispielsweise ein Startdatum vom 1. Januar und ein Enddatum vom 31. Dezember hat und dem neuen Kunden 40 Prozent für die ersten neun Monate in Rechnung gestellt werden, geben Sie den 1. Januar als Startdatum und den 30. September als Enddatum an, und geben Sie **40.00** als Prozentsatz ein.

Sie können nur einen Kunden zu den Positionen der Debitorenteilung hinzufügen. In diesem Fall darf der eingegebene Gesamtprozentsatz 100 Prozent nicht überschreiten. Geben Sie eine Kundenreferenz und eine Kundenanforderung als Informationsfelder ein, die in der Verkaufsauftragszeile während des **Rechnung erstellen** Prozesses angezeigt werden.

Die Zeilendetails zeigen die Kontaktinformationen, die Lieferadresse, die Rechnungsadresse und die Zahlungsdetails der hinzugefügten Kunden. Diese Informationen werden auch auf dem Kundenauftrag für die Kunden angezeigt.

Wenn Sie der Kopfzeile des Abrechnungszeitplans Kundenaufteilungsinformationen hinzufügen und nicht abgerechnete Abrechnungszeitplanpositionen im Abrechnungszeitplan enthalten, erhalten Sie die folgende Meldung, in der Sie aufgefordert werden, die Änderungen rückgängig zu machen: „Möchten Sie die Änderung rückgängig machen von die Kopfzeile zu den Zeilen? Durch Änderungen werden nur die nicht fakturierten Fakturierungsplanzeilen aktualisiert.“ Wählen Sie **Ja** aus, um die Kundenaufteilungsinformationen in der Fakturierungsplanposition zu aktualisieren. Änderungen werden nicht aktualisiert, wenn die Abrechnungszeitplanposition bereits abgerechnet wurde.

Wenn ein Abrechnungszeitplan mithilfe der Option **Zeitplan kopieren** erstellt wird, werden Standardinformationen in kundengeteilte Kopfzeilen eingegeben. Es darf nicht mit dem Kundenkonto identisch sein.

Wenn der **Rechnung erstellen** Prozess abgeschlossen ist, werden mehrere Verkaufsaufträge erstellt. (Bei Verwendung der automatischen Buchung werden auch mehrere Verkaufsrechnungen erstellt.) Diese Verkaufsaufträge und Verkaufsrechnungen können in der **Rechnung** Registerkarte im Inforegister **Positionsdetails** der **Rechnungsdetails anzeigen** Seite angezeigt werden. **Mehrere** wird in der Rechnungsdetailzeile angezeigt, um anzuzeigen, dass mehrere Verkaufsaufträge und Verkaufsrechnungen erstellt wurden.

## <a name="customer-split-on-billing-schedule-lines"></a>Debitorenteilung bei Abrechnungszeitplanpositionen

Der Kundensplit kann zu einzelnen Fakturaeinteilungen hinzugefügt werden, wenn Sie nur bestimmte Fakturaeinteilungen splitten möchten. Wählen Sie das **Kundenaufteilung** Kontrollkästchen in der Zeile, und wählen Sie dann **Kundenaufteilung** im Menü für die Fakturierungsplanposition, um die Kundenaufteilungsinformationen zu aktualisieren oder einzugeben.

Die Prüfinformationen werden aktualisiert, wenn der Fakturierungsplan bereits fakturiert wurde, aber dann der Prozentsatz in der Fakturierungsplanposition geändert wurde. Alle Positionen, die nach dieser Änderung abgerechnet werden, verwenden den neuen Prozentsatz.

> [!NOTE]
> - Die Kundenaufteilungsoption kann nicht mit Lagerprodukten verwendet werden.
> - Wenn das **Nicht fakturierter Umsatz** Kontrollkästchen aktiviert ist, kann das **Kundenaufteilung** Kontrollkästchen nicht ausgewählt werden.
> - Wenn Sie die Option **Nur Einnahmenaufteilung** verwenden, hat die übergeordnete Position die **Kundenaufteilung** Option, die untergeordneten Werbebuchungen jedoch nicht.
