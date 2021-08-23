---
title: Abstimmen eines Bankkontos
description: In diesem Thema wird beschrieben, wie ein Bankkonto abgestimmt wird.
author: panolte
ms.date: 07/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e06a38a19a16a07d77d0c9aceaa4e3206646dd0561996681b417b785058f3938
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739358"
---
# <a name="reconcile-a-bank-account"></a>Abstimmen eines Bankkontos

[!include[banner](../includes/banner.md)]

Wenn Sie einen Bankauszug erhalten, sollten Sie Bankbuchungen der juristischen Person mit den Buchungen im Bankauszug regelmäßig abstimmen.

Ein Bankauszug kann nicht mit einem Bankkonto abgestimmt werden, wenn eine der per Scheck oder Einzahlungsbeleg erfolgten Zahlungen, die in dem Auszug aufgeführt sind, aktuell den Status **Storno ausstehend** hat. Nach der Buchung oder Ablehnung einer Scheckrückbuchung oder einer Bankeinzahlungsbeleg-Stornierung durch einen Prüfer lautet der Status nicht mehr **Storno ausstehend**, und das Bankkonto kann abgestimmt werden.

1.  Gehen Sie zu **Bargeld- und Bankverwaltung** \> **Bankkonten** \> **Bankkonten**. Wählen Sie das Bankkonto aus, das mit dem Bankauszug abzustimmen ist, und wählen Sie **Abstimmen** > **Kontoabstimmung** aus.

2.  Geben Sie Informationen in die Felder **Datum des Bankauszugs** und **Bankauszug** ein. Im Feld **Endsaldo** können Sie den Saldo des Bankkontos eingeben, so wie dieser auf dem Bankauszug angezeigt wird.

3.  Wählen Sie **Buchungen**, um die Seite **Kontoabstimmung** zu öffnen.

4.  Aktivieren Sie für jede im Bankauszug vorhandene Buchung das Kontrollkästchen **Verrechnet**, sofern der Betrag in Dynamics 365 Finance dem Betrag auf dem Bankauszug entspricht. Sie können auch den Wert im Feld **Bankbuchungsart** eingeben oder ändern. Dieser Feldwert ist für die Bankbuchungsstatistik sowie für einige andere Berichte relevant.
    

    > [!NOTE]
    > <P>Aktivieren Sie das Kontrollkästchen <STRONG>Verrechnet</STRONG> nicht für Buchungen, die nicht auf dem Bankauszug enthalten sind. Diese Buchungen werden so lange auf dieser Seite angezeigt, bis sie mit einem künftigen Bankauszug abgestimmt wurden.</P>
    > <P>Das Kontrollkästchen <STRONG>Verrechnet</STRONG> ist nicht verfügbar, wenn die Buchung den Status <STRONG>Storno ausstehend</STRONG> besitzt. Buchungen können diesen Status haben, wenn Finance so eingerichtet ist, dass Stornierungen vor dem Buchen erst zwecks Genehmigung weitergeleitet werden müssen. Nach der Buchung oder Ablehnung der Rückbuchung oder Stornierung durch einen Prüfer lautet der Status nicht mehr <STRONG>Storno ausstehend</STRONG>, und der Bankauszug kann mit dem Bankkonto abgestimmt werden.</P>

    
    Um das Kontrollkästchen **Verrechnet** für ein Intervall mit Schecks auszuwählen, die alle im Kontoauszug angezeigt werden, wählen Sie **Scheckintervall markieren** aus, und geben Sie anschließend das Intervall an.

5.  Wenn der Betrag für eine Bankkontobuchung nicht dem Buchungsbetrag auf dem Bankauszug entspricht, geben Sie den Korrekturbetrag in das Feld **Korrekturbetrag** ein.
    

    > [!NOTE]
    > <P>Ist der Finanzzeitraum für die zu korrigierende Buchung bereits abgeschlossen, steht das Feld <STRONG>Korrekturbetrag</STRONG> nicht zur Verfügung. Erstellen Sie stattdessen eine Position, die ein Buchungsdatum hat, das in einem offenen Finanzzeitraum für die Korrektur liegt. In diesem Fall müssen Sie die Finanzdimensionen, die bei der ursprünglichen Buchung verwendet wurden, und auch das Gegenhauptkonto hinzufügen.</P>



6.  Erstellen Sie Buchungen für Einträge (wie Gebühren und Zinsen), die sich zwar auf dem Bankauszug befinden, aber nicht in Finance erfasst sind. Geben Sie die **Bankbuchungsart** und entsprechende Finanzdimensionen ein.

7.  Während die Buchungen im Bankauszug als **Verrechnet** markiert sind, nähert sich der Betrag im Feld **Nicht abgestimmt**, das bei Änderungen fortlaufend neu berechnet wird, dem Wert Null. Wenn der Wert Null erreicht ist, wählen Sie **Konto ausgleichen** aus, um die Abstimmung und die Buchungen und Korrekturen, die Sie erstellt haben, zu buchen.
    
    Nach der Buchung der Abstimmung können die einbezogenen Buchungen nicht mehr überarbeitet oder korrigiert werden, und sie werden auch nicht mehr für künftige Kontoabstimmungen angezeigt.

8.  Verwenden Sie zur Anzeige von Bankbuchungen, die noch nicht abgestimmt wurden, den Bericht **Nicht abgestimmte Bankbuchungen**. Um den Bankauszug für ein Bankkonto anzuzeigen, verwenden Sie den Bericht **Bankauszug**.

## <a name="cancel-bank-statement-reconciliation"></a>Bankauszugsabstimmung stornieren 

Die Funktion „Bankauszugsabstimmung stornieren“ ermöglicht es Ihnen, den Vorgang der Bankauszugsabstimmung zu stornieren. Um diese Funktion zu verwenden, aktivieren Sie die Funktion **Bankauszugsabstimmung stornieren** im Arbeitsbereich **Funktionsverwaltung**. Sie müssen zudem den Parameter **Bankauszugsbearbeitung zulassen** aktivieren. Wechseln Sie hierzu zu **Bargeld- und Bankverwaltung > Einstellungen > Bargeld- und Bankverwaltungsparameter > Bankabstimmung**.
 
Bankauszugsabstimmungen können nur in der chronologischen Reihenfolge storniert werden, in der sie eingegeben wurden. Wenn eine Bankauszugsabstimmung storniert wird, werden neue Buchungen und Korrekturen storniert und alle weiteren Buchungen werden als nicht abgestimmt markiert.
 
Um die Bankauszugsabstimmung stornieren, wählen Sie den Bankauszug aus, und wählen Sie **Bankauszug > Abstimmung stornieren**. Geben Sie auf der Seite **Abstimmung stornieren** den **Ursachencode**, einen **Kommentar zur Ursache** und das **Stornierungsdatum** an. Wählen Sie **OK**, um die Stornierung zu starten. Beachten Sie, dass das Datum der Bankauszugsstornierung am oder nach dem Bankauszugsdatum liegen muss. Nachdem die Bankauszugsabstimmung storniert wurde, wird das Feld **Stornierungsdatum** für den Bankauszug mit dem angegebenen **Stornierungsdatum** aktualisiert. Wählen Sie die Schaltfläche **Buchungen** aus, um die Buchungen anzuzeigen, für die die Abstimmung storniert wurde.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]