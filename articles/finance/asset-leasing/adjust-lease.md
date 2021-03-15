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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32d99d9e90b65f7cac74176d21fa4b053ae8f62c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130754"
---
# <a name="adjust-leases"></a>Mietverträge anpassen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie einen Mietvertrag anpassen. Eine Regulierung kann erforderlich sein, wenn die Mietbedingungen geändert, der Mietvertrag verlängert oder andere Umstände geändert werden. Das Anlagenleasing entspricht den Richtlinien, die das Thema 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842) und der International Financial Reporting Standard 16 (IFRS 16) zu Änderungen von Mietverträgen enthalten. ASC 842-20-15-1 definiert eine Mietvertragsänderung als jede Änderung der Vertragsbedingungen, die eine Änderung des Umfangs oder der Gegenleistung eines Mietvertrags bewirkt. Gemäß Paragraph 39 von IFRS 16 muss ein Mieter die Leasingverbindlichkeit neu bewerten, damit sie Änderungen der Mietzahlungen widerspiegelt.

Für Unternehmen, die ASC 842 oder IFRS 16 einhalten, wird ein Mietvertrag neu bewertet, um eine Änderung des Barwerts der zukünftigen Mindestmietzahlungen (PVFMLP) widerzuspiegeln. Wenn sich der PVFMLP erhöht, ist der erstellte Journaleintrag eine Belastung des Kontos für das Nutzungsrecht am Leasingobjekt und eine Gutschrift auf das Konto der Ausrüstungs-Leasingverbindlichkeit für die Differenz zwischen dem neuen PVFMLP und dem vorherigen PVFMLP. Wenn der PVFMLP abnimmt, ist der Journaleintrag eine Belastung des Kontos der Ausrüstungs-Leasingverbindlichkeit und eine Gutschrift auf das Konto für das Nutzungsrecht am Leasingobjekt um die Differenz.

Wenn durch die Regulierung das Nutzungsrecht am Leasingobjekt über 0 (Null) hinaus verringert wird, wird der Rest dem Gewinn aus der Buchung von Mietänderungen gutgeschrieben der auf der Seite **Leasingbuchungskonten** angegen ist. Das System berücksichtigt diese Transaktionen und andere Regulierungsbuchungen wie Klassifizierungsänderungen, anfängliche direkte Kosten, Mietanreize, Vorauszahlungen und Demontagekosten, die sich aus Mietänderungen ergeben.

Für spezifische Anleitungen zu Mietregulierungstransaktionen empfehlen wir Ihnen, IFRS 16 und ASC 842 zu lesen.

## <a name="lease-adjustment-wizard"></a>Mietvertragsregulierungsassistent

Führen Sie die folgenden Schritte aus, um einen Mietvertrag anzupassen. Die geänderten Daten werden Mietpläne aktualisieren, sobald Sie über den Assistenten **Mietvertragsregulierung** gebucht haben. Sie können Ihre Arbeit jederzeit speichern und den Assistenten schließen, um später zurückzukehren und die Arbeit fortzusetzen.

Führen Sie zum Öffnen des Assistenten **Mietvertragsregulierung** aus der Mietvertragsübersicht folgende Schritte aus.

1. Wechseln Sie zu **Anlagenleasing \> Mietverträge \> Mietvertragsübersicht**. 
2. Wählen Sie den anzupassenden Mietvertrag aus, und wählen Sie dann **Regulierungsassistent** aus.
3. Befolgen Sie die Anweisungen des Assistenten, um die erforderlichen Änderungen einzugeben.

Führen Sie zum Öffnen des Assistenten **Mietvertragsregulierung** über die Seite **Mietvertragsregulierungen** die folgenden Schritte aus, um eine Regulierung vorzunehmen, die bereits ausgeführt wird.

1.  Rufen Sie **Mieten \> Mietverträge \> Mietvertragsregulierungen** auf.
2.  Wählen Sie einen Mietvertrag mit dem Regulierungsstatus **In Bearbeitung** und anschließend **Regulierungsassistent** aus.
3.  Geben Sie in den Feldern **Änderungsstartdatum** und **Buchungsdatum** die entsprechenden Daten ein.
4.  Wählen Sie **Weiter**.

    Der Mietvertrag wird nun der Seite **Mietvertragsregulierungen** hinzugefügt, auf der Sie die neuen Informationen dazu eingeben können.

    Nachdem der Mietvertrag angepasst wurde, gelten die Felder für Überlegungen zum Nutzungsrecht. Wenn mit dem geänderten Mietvertrag keine anfänglichen direkten Kosten, Mietanreize, Vorauszahlungen oder Demontagekosten verbunden sind, sollten Sie diese Felder leer lassen. Die ursprünglichen Beträge gelten nicht für den aktualisierten Mietvertrag. 

    Beispielsweise bietet ein Vermieter einen 1.000 USD-Anreiz beiZustimmung zu einer Mietvertragsverlängerung. In diesem Fall geben Sie bei Anpassung des Mietvertrags zur Berücksichtigung der Verlängerung **1.000** in dem Feld **Mietanreize durch Anpassung** ein.

    In den Zahlungsplanpositionen werden jetzt alle Zahlungen aus dem Monat und späteren Monaten im Feld **Änderungsstartdatum** angezeigt. Da Änderungen perspektivisch sind, können Zahlungsplanpositionen nicht beginnen, bevor die Änderung beginnt. Rufen Sie die Seite **Verlauf der Mietvertragsversion** auf, um Zahlungsplanpositionen vor dem Startdatum der Änderung anzuzeigen.

8.  Wählen Sie **Weiter**.

    Auf der nächsten Seite werden wichtige Details zur erwarteten Mietvertragsregulierung angezeigt, z. B. die Buchwerte der Leasingverbindlichkeit vor der Änderung und der neuen erwarteten Leasingverbindlichkeit nach der Änderung. Die Seite zeigt auch eine Vorschau des Journaleintrags für die erwartete Mietvertragsregulierung an.

9.  Wählen Sie **An Workflow übermitteln** aus, um die Mietvertragsregulierung an das Workflowsystem zu übermitteln, wenn der Mietvertragsregulierungsworkflow aktiv ist, und die Regulierung noch nicht genehmigt wurde. Weitere Informationen zum Verwenden des Mietvertragsregulierungsworkflows finden Sie unter [Mietvertragsregulierungsworkflow verwenden](use-create-lease-wrkflw.md).

    > [!NOTE]
    > Zu diesem Zeitpunkt berechnet das System die Regulierungsvariablen neu, um zu überprüfen, ob seit der ersten Berechnung der Regulierungsübersicht und des Regulierungsjournaleintrags keine Mietvertragstransaktionen gebucht wurden. Wenn sich Werte ändern, wird das Regulierungsübersichtsraster aktualisiert, und Sie können die Informationen überprüfen, bevor Sie die Mietvertragsregulierung erneut an das Workflow-System senden.

10. Wenn ein Workflow nicht aktiv ist oder die Mietvertragsregulierung genehmigt wurde, wählen Sie **Fertig stellen** aus, um die Änderungen zu verarbeiten und den Regulierungsjournaleintrag zu buchen.

    > [!NOTE] 
    > Zu diesem Zeitpunkt berechnet das System die Regulierungsvariablen neu, um zu überprüfen, ob seit der ersten Berechnung der Regulierungsübersicht und des Regulierungsjournaleintrags keine Mietvertragstransaktionen gebucht wurden. Wenn sich Werte ändern, wird das Regulierungsübersichtsraster aktualisiert, und Sie können die Änderungen überprüfen, bevor Sie **Fertig stellen** auswählen. Wenn der Workflow aktiv ist und die Mietvertragsregulierung genehmigt wurde, wird durch Änderungen an der Regulierungsübersicht der Genehmigungsstatus auf **Nicht übermittelt** zurückgesetzt. In diesem Fall sollten Sie die Mietvertragsregulierung erneut an das Workflow-System senden.

    Der Regulierungsstatus ist nun auf der Seite **Mietvertragsregulierungen** auf **Abgeschlossen** gesetzt.

    Sie können auf der Seite **Mietvertragsregulierungen** weiterhin die Inforegister **Regulierungsübersicht** und **Vorschau des Regulierungseintrags** einsehen. Die Mietvertragsdetails und Datumsinformationen werden im Versionsverlauf dieses Mietvertrags angezeigt.

    Mithilfe der geänderten Informationen werden jetzt eine neue Mietvertragsversion und ein neuer Satz von Zeitplänen erstellt. 

13. Rufen Sie den Mietvertrag auf, und wählen Sie anschließend **Bücher** aus, um sich die neuen Zeitpläne anzeigen zu lassen.
14. Wählen Sie **Zahlungsplan** aus, um sich den neu generierten Zahlungsplan anzeigen zu lassen.
15. Um den neuen Tilgungsplan für Leasingverbindlichkeiten anzuzeigen, der aus den neuen Informationen generiert wird, schließen Sie die Seite **Zahlungsplan**, und öffnen Sie die Seite **Zeitplan für die Amortisierung von Verbindlichkeiten**.
16. Um den neu generierten Anlagenabschreibungsplan anzuzeigen, öffnen Sie die Seite **Anlagenabschreibungsplan** von der **Buchdetails**-Seite.
17. Wählen Sie zum Anzeigen des Regulierungsjournaleintrags **Erfassung \> Anlagenleasingerfassung** aus.

## <a name="cancel-a-lease-adjustment"></a>Eine Mietvertragsregulierung abbrechen

Führen Sie die folgenden Schritte aus, um eine laufende Mietvertragsregulierung zu löschen.

1.  Rufen Sie **Mieten \> Mietverträge \> Mietvertragsregulierungen** auf.
2.  Wählen Sie die laufende Mietvertragsregulierung aus, um sie abzubrechen.
3.  Wählen Sie **Regulierung abbrechen** aus. 
4.  Wählen Sie **OK**.

    > [!NOTE] 
    > Wenn Sie **Abbrechen** im Assistenten **Mietvertragsregulierung** auswählen, setzen Sie die letzte Änderung, die Sie im Assistenten abgeschlossen haben, zurück, entfernen jedoch keine laufenden Regulierungen.

## <a name="use-the-lease-adjustment-workflow"></a>Den Mietvertragsregulierungsworkflow verwenden

In diesem Abschnitt wird die Verwendung des Workflows zur Mietvertragsregulierung erläutert. Mithilfe des Workflows zur Mietvertragsregulierung können Sie Mietvertragsregulierungen auf konsistente Weise verwalten, indem Sie eine Reihe von Genehmigungsschritten bereitstellen und diese bestimmten Benutzern zuweisen, die eine Mietvertragsregulierung genehmigen, bevor sie rechtskräftig wird. Sobald die Mietvertragsregulierung im Workflow genehmigt wurde, können Sie den Assistenten **Mietvertragsregulierung** zum Abschließen der Mietvertragsregulierung nutzen.

1.  Rufen Sie **Mieten \> Mietverträge \> Mietvertragsregulierungen** auf, um eine Mietvertragsregulierung zur Genehmigung einzureichen.
2.  Wählen Sie die Mietvertrags-ID der Mietvertragsregulierung aus, und wählen Sie dann **Regulierungsassistent** aus.
3.  Wählen Sie auf der letzten Seite des Assistenten **Zur Genehmigung senden** aus.
4.  Geben Sie einen Kommentar zur Regulierung ein, und wählen Sie dann **OK** aus.

    Der Workflow-Status wird in **Ausstehende Genehmigung** geändert, und alle Felder im Assistenten sind für die Bearbeitung gesperrt.

5.  Rufen Sie **Mieten \> Mietverträge \> Mietvertragsregulierungen** auf, um die Mietvertragsregulierung zu genehmigen.
6.  Wählen Sie die Mietvertrags-ID der Mietvertragsregulierung aus, und überprüfen Sie die Inforegister **Regulierungsübersicht** und **Vorschau des Regulierungseintrags**.
7.  Wählen Sie **Workflow \> Genehmigt** aus.

    Der Workflowstatus ist nun auf der Seite **Mietvertragsregulierungen** auf **Genehmigt** gesetzt. Zu diesem Zeitpunkt kann die Mietvertragsregulierung über den Regulierungsjournaleintrag gebucht werden.

8.  Rufen Sie **Mieten \> Mietverträge \> Mietvertragsregulierung** auf, um die Mietvertragsregulierung weiter zu verarbeiten und den Regulierungseintrag zu buchen.
9.  Wählen Sie die Mietvertrags-ID der Mietvertragsregulierung aus, und wählen Sie dann **Regulierungsassistent** aus.
10. Wählen Sie **Weiter** aus, bis Sie die letzte Seite des Assistenten erreichen, und wählen Sie dann **Fertig stellen** aus.

Das System berechnet die Buchwerte des Mietvertrags neu, um sicherzustellen, dass die genehmigten Regulierungsvariablen aktuell sind. Bei Änderungen wird der Genehmigungsstatus auf **Entwurf** zurückgesetzt, und Sie sollten die Mietvertragsregulierung erneut an das Workflow-System übermitteln.

## <a name="view-lease-versions"></a>Mietvertragversionen anzeigen

Wenn ein Mietvertrag angepasst wurde, können Sie sich die verschiedenen Versionen anzeigen lassen. Sie können auch die historischen Zeitpläne und Details zu früheren Mietverträgen anzeigen.

1. Wählen Sie auf der Seite **Mietvertragsübersicht** den Mietvertrag und dann im Aktionsbereich die Option **Verlauf der Mietvertragsversion** aus.

    Wenn der ausgewählte Mietvertrag angepasst wurde, zeigt die Seite **Verlauf der Mietvertragsversion** die verschiedenen Versionen an. Der ursprüngliche Mietvertrag ist mit **1** gekennzeichnet und nachfolgende Versionen haben eine aufsteigende numerische Reihenfolge.

    Für eine ausgewählte Mietvertragsversion können Sie die finanziellen Dimensionen, Vertragsdetails, den Standort und die Zahlungsplanzeilen anzeigen.

2. Öffnen Sie den geänderten Mietvertrag über die Seite **Mietvertragsübersicht**, , um historische Zeitpläne anzuzeigen, wählen Sie auf der Seite das gewünschte Buch und dann im Aktionsbereich **Buchversionsverlauf** aus.
3. Wählen Sie auf der Seite **Buchversion** eine Version und einen Zeitplan aus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]