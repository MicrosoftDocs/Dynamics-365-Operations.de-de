---
title: Mietverträge anpassen
description: In diesem Thema wird erläutert, wie Sie einen Mietvertrag anpassen. Eine Regulierung kann erforderlich sein, wenn die Mietbedingungen geändert, der Mietvertrag verlängert oder andere Umstände geändert werden.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4443787"
---
# <a name="adjust-leases"></a>Mietverträge anpassen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Mietvertrag anpassen. Eine Regulierung kann erforderlich sein, wenn die Mietbedingungen geändert, der Mietvertrag verlängert oder andere Umstände geändert werden. Das Anlagenleasing entspricht den Richtlinien, die das Thema 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842) und der International Financial Reporting Standard 16 (IFRS 16) zu Änderungen von Mietverträgen enthalten. ASC 842-20-15-1 definiert eine Mietvertragsänderung als jede Änderung der Vertragsbedingungen, die eine Änderung des Umfangs oder der Gegenleistung eines Mietvertrags bewirkt. Gemäß Paragraph 39 von IFRS 16 muss ein Mieter die Leasingverbindlichkeit neu bewerten, damit sie Änderungen der Mietzahlungen widerspiegelt.

Für Unternehmen, die ASC 842 oder IFRS 16 einhalten, wird ein Mietvertrag neu bewertet, um eine Änderung des Barwerts der zukünftigen Mindestmietzahlungen (PVFMLP) widerzuspiegeln. Wenn sich der PVFMLP erhöht, ist der erstellte Journaleintrag eine Belastung des Nutzungsrechts und eine Gutschrift auf die Leasingverbindlichkeit für die Differenz zwischen dem neuen PVFMLP und dem vorherigen PVFMLP. Wenn der PVFMLP abnimmt, ist der Journaleintrag eine Belastung der Leasingverbindlichkeit und eine Gutschrift des Nutzungsrecht am Leasingobjekt um die Differenz.

Wenn durch die Regulierung das Nutzungsrecht am Leasingobjekt über 0 (Null) hinaus verringert wird, wird der Rest dem Gewinn aus der Buchung von Mietänderungen gutgeschrieben der auf der Seite **Leasingbuchungskonten** angegen ist. Das System berücksichtigt diese Transaktionen und andere Regulierungsbuchungen wie Klassifizierungsänderungen, anfängliche direkte Kosten, Mietanreize, Vorauszahlungen und Demontagekosten, die sich aus Mietänderungen ergeben.

Für spezifische Anleitungen zu Mietregulierungstransaktionen empfehlen wir Ihnen, IFRS 16 und ASC 842 zu lesen.

Führen Sie folgende Schritte aus, um einen Mietvertrag anzupassen. Die geänderten Daten aktualisieren die Mietpläne, nachdem der Prozess „Zeitplan erstellen“ ausgeführt wurde.

1. Wechseln Sie zu **Anlagenleasing \> Mietverträge \> Mietvertragsübersicht**.
2. Wählen Sie auf der Seite **Mietvertragsübersicht** das zu anpassende Mietvertragsverhältnis und dann **Mietvertrag anpassen**.
3. Geben Sie auf der Seite **Mietvertrag anpassen** die neuen Informationen für den angepassten Mietvertrag ein.

    Beachten Sie, dass die Seite **Mietvertrag anpassen** der Seite **Mietvertrag hinzufügen** ähnelt. Ebenso wie das Anfangsdatum, das Sie beim Hinzufügen eines Mietvertrags angeben, bestimmt, wann der neue Mietvertrag beginnt, wird im Feld **Änderungsdatum** auf der Seite **Mietvertrag anpassen** bestimmt, wann der geänderte Mietvertrag beginnt. Dieses Datum darf nicht nach dem Startdatum in den Zahlungsplänen liegen.

    > [!NOTE]
    > Die **Überlegungen zur ROU**-Felder gelten für die Mietvertragsanpassung. Wenn mit dem geänderten Mietvertrag keine anfänglichen direkten Kosten, Mietanreize, Vorauszahlungen oder Demontagekosten verbunden sind, sollten Sie diese Felder leer lassen. Die ursprünglichen Beträge gelten nicht für den aktualisierten Mietvertrag. Alle zusätzlichen Kosten, die bei der Änderung des Mietvertrags anfallen, sollten auf der Seite **Mietvertrag anpassen** eingetragen werden.
    > 
    > Beispielsweise bietet ein Vermieter einen 1.000 USD-Anreiz beiZustimmung zu einer Mietvertragsverlängerung. In diesem Fall geben Sie bei Anpassung des Mietvertrags zur Berücksichtigung der Verlängerung **1.000** in dem Feld **Mietanreize** ein. Wenn mit der Mietpassung keine Anreize verbunden sind, sollten Sie alle Werte löschen, die zuvor in dieses Feld eingegeben wurden. Die gleiche Logik wird auf andere ROU-Überlegungen angewendet.

    Die Zahlungspläne des angepassten Mietvertrags sollten prospektiv erstellt werden. Zahlungsplanzeilen, die prospektiv erstellt werden, können nicht gestartet werden, bevor die Mietänderungen wirksam werden.

    Die folgenden Schritte sind nahezu identisch mit den Schritten zum erstmaligen Anerkennen eines Mietvertrags.

4. Wählen Sie **Zeitpläne erstellen** aus, um den angepassten Zahlungsplan zu generieren. Sie erhalten eine Nachricht, dass der Zahlungsplan für den Mietvertrag erstellt wurde.

    > [!IMPORTANT]
    > Bevor Sie **Zeitpläne erstellen** auswählen, stellen Sie sicher, dass das Änderungsdatum und die Zahlungspläne korrekt sind. Stellen Sie außerdem sicher, dass alle anfänglichen direkten Kosten, Mietanreize, Vorauszahlungen oder Demontagekosten nur den Kosten entsprechen, die sich aus der Anpassung ergeben.

5. Wählen Sie **Bücher** aus, um den neu erstellten Zahlungsplan anzuzeigen, und öffnen Sie die Seite **Zahlungsplan**.
6. Auf der **Zahlungsplan**-Seite können Sie die angepassten Zahlungsbeträge bearbeiten, bevor Sie den Zahlungsplan bestätigen. Um den Zeitplan zu bestätigen, wählen Sie **Zeitplan bestätigen**.

    Wenn der Zahlungsplan bestätigt wird, werden die neuen Abschreibungen auf Vermögenswerte und neue Leasingverbindlichkeiten erstellt.

7. Um den neuen Tilgungsplan für Leasingverbindlichkeiten anzuzeigen, der aus den neuen Eingaben generiert wird, schließen Sie die Seite **Zahlungsplan** und öffnen Sie die Seite **Zeitplan für die Amortisierung von Verbindlichkeiten**.
8. Um den neu generierten Anlagenabschreibungsplan anzuzeigen, öffnen Sie die Seite **Anlagenabschreibungsplan** von der **Buchdetails**-Seite.
9. Wählen Sie zum Generieren des Regulierungsjournaleintrags **Funktion \> Mietanpassung** aus. Sie erhalten eine Nachricht, dass der Regulierungsjournaleintrag erstellt wurde. 
10. Um den Journaleintrag anzuzeigen, wählen Sie **Erfassung \> Anlagenleasingerfassung** aus.
11. Um den Journaleintrag zu buchen, wählen Sie die Zeile aus und wählen Sie dann **Buchen**.

## <a name="view-lease-versions"></a>Mietvertragversionen anzeigen

Wenn ein Mietvertrag geändert wurde, können Sie die verschiedenen Versionen anzeigen. Sie können auch die historischen Zeitpläne und Details zu früheren Mietverträgen anzeigen.

1. Wählen Sie auf der Seite **Mietvertragsübersicht** den Mietvertrag und dann im Aktionsbereich die Option **Verlauf der Mietvertragsversion** aus.

    Wenn der ausgewählte Mietvertrag angepasst wurde, zeigt die Seite **Verlauf der Mietvertragsversion** die verschiedenen Versionen davon. Der ursprüngliche Mietvertrag ist mit **1** gekennzeichnet und nachfolgende Versionen haben eine aufsteigende numerische Reihenfolge.

    Für eine ausgewählte Mietvertragsversion können Sie die finanziellen Dimensionen, Vertragsdetails, den Standort und die Zahlungsplanzeilen anzeigen.

2. Öffnen Sie den geänderten Mietvertrag über die Seite **Mietvertragsübersicht**, , um historische Zeitpläne anzuzeigen, wählen Sie auf der Seite das gewünschte Buch und dann im Aktionsbereich **Buchversionsverlauf** aus.
3. Wählen Sie auf der Seite **Buchversion** die gewünschte Version und den gewünschten Zeitplan aus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]