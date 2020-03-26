---
title: Kreditsperren für Aufträge verwalten
description: In diesem Thema wird das Einrichten von Regeln beschrieben, mit denen ein Debitorenauftrag auf Kredit gehalten wird.
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a0e006be8a72f35d6c6009ca9d67d083b8fac89
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124253"
---
# <a name="credit-holds-for-sales-orders"></a>Kreditsperren für Aufträge verwalten
[!include [banner](../includes/banner.md)]

In diesem Thema wird das Einrichten von Regeln beschrieben, mit denen ein Debitorenauftrag auf Kredit gehalten wird. Die Sperrregeln für das Kreditmanagement können für einen einzelnen Debitor oder eine Gruppe von Debitoren gelten. Sperrregeln definieren Reaktionen auf die folgenden Umstände:

1. Anzahl der überfälligen Tage
2. Kontostatus
3. Zahlungsbedingungen
4. Kreditlimit abgelaufen
5. Überfälliger Betrag
6. Auftragsbetrag
7. Teil des verfügbaren verwendeten Guthabens

Darüber hinaus gibt es zwei Parameter, die zusätzliche Szenarien steuern, die einen Debitorenauftrag blockieren

1. Änderung der Zahlungsbedingungen
2. Änderung der Ausgleichsrabatte

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Sperr- und Ausschlussregeln einrichten

Wenn ein Debitor eine Verkaufstransaktion einleitet, werden die Informationen im Auftrag anhand einer Reihe von Sperrregeln überprüft, anhand derer entschieden wird, ob dem Debitor ein Guthaben gewährt und der Verkauf fortgesetzt werden soll. Sie können auch Ausschlüsse definieren, die die Sperrregeln außer Kraft setzen und die Verarbeitung eines Auftrags ermöglichen. Sie können Sperr- und Ausschlussregeln auf der Seite **Kreditmanagement > Einstellungen > Einstellung des Kreditmanagements > Sperrregeln** einrichten.

### <a name="days-overdue"></a>Überfällige Tage

Öffnen Sie die Registerkarte **Tage überfällig**, wenn die Sperrregel für Debitoren mit einer oder mehreren Rechnungen gilt, die für eine bestimmte Anzahl von Tagen überfällig sind.
1. Wählen Sie den Debitorenbereich aus, für den diese Regel **Gültig für** gilt.
   - Wählen Sie **Tabelle**, wenn die Regel für einen bestimmten Debitor gilt.
   - Wählen Sie **Gruppe**, wenn die Regel auf Debitorengruppenebene angewendet wird. 
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt.
2. Wenn Sie den Bereich angegeben haben, müssen Sie die **Kontengruppe** angeben, die wird in dem Bereich verwendet wird.
   - Für den Bereich **Tabelle** bietet die Suche eine Liste der Debitoren zur Auswahl. 
   - Wählen Sie eine **Gruppe**, wenn die Regel für eine Debitorenkreditgruppe gilt.
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt. 
3. Wählen Sie **Risikogruppe**, um Kriterien für die Anwendung einer Kreditmanagement-Sperre auf Kunden zu verwenden, die nach einem gemeinsamen Satz von Faktoren gruppiert sind, wie z. B. ihr Dun- und Bradstreet-Rating, die Anzahl der Jahre, die sie im Geschäft sind, die Zeit, die sie Ihr Kunde sind, und so weiter.  
4. Wählen Sie die Art der Regel aus, die Sie einrichten. Die Option **Sperrung** erstellt eine Regel, die eine Bestellung sperrt. Die Option **Ausschluss** erstellt eine Regel, die eine andere Regel vom Sperren einer Bestellung ausschließt. 
5. Wählen Sie einen **Werttyp** aus. Der Standardeintrag ist eine feste Anzahl von Tagen. Wenn Sie einen Ausschluss erstellen, können Sie stattdessen eine feste Anzahl von Tagen oder einen Betrag angeben. 
6. Geben Sie die Anzahl der Tage **Überfällig** ein, die für die ausgewählte Sperrregel zulässig sind, bevor eine Bestellung zur Überprüfung in die Warteschleife für das Kreditmanagement gestellt wird. Die Anzahl der überfälligen Tage entspricht einer zusätzlichen Anzahl von Kulanztagen, die zu der Anzahl von Tagen nach dem Fälligkeitsdatum hinzuaddiert werden, die die Rechnung haben kann, bevor sie als überfällig angesehen wird. Wenn Sie den **Werttyp** als Betrag für einen Ausschluss angegeben haben, dann geben Sie einen Betrag und eine Währung für diesen Betrag ein.

### <a name="accounts-status"></a>Kontostatus

Öffnen Sie die Registerkarte **Kontostatus**, wenn die Sperrregel für einen Debitoren mit dem ausgewählten Kontostatus gilt.
1. Wählen Sie die Art der Regel aus, die Sie einrichten.  Die **Sperrung** erstellt eine Regel, die eine Bestellung sperrt. Die Option **Ausschluss** erstellt eine Regel, die eine Regel vom Sperren einer Bestellung ausschließt. 
2. Wähle den **Kontostatus** aus, der die Regel veranlasst, einen Kundenauftrag zurückzuhalten oder auszuschließen.

### <a name="terms-of-payment"></a>Zahlungsbedingungen

Wählen Sie **Zahlungsbedingungen**, wenn die Sperrregel für die ausgewählte Zahlungsbedingung gilt.
1. Wählen Sie die Art der Regel aus, die Sie einrichten.  Die **Sperrung** erstellt eine Regel, die eine Bestellung sperrt. Die Option **Ausschluss** erstellt eine Regel, die eine Regel vom Sperren einer Bestellung ausschließt. 
2. Wählen Sie die **Zahlungsbedingung** aus, die die Regel veranlassen, einen Auftrag zurückzuhalten oder auszuschließen.

### <a name="credit-limit-expired"></a>Kreditlimit abgelaufen

Öffnen Sie die Registerkarte **Kreditlimit abgelaufen**, wenn die Sperrregel für Kreditoren mit abgelaufenen Kreditlimits gilt.
1. Wählen Sie den Debitorenbereich aus, für den diese Regel **Gültig für** gilt.
   - Wählen Sie **Tabelle**, wenn die Regel für einen bestimmten Debitor gilt.
   - Wählen Sie **Gruppe**, wenn die Regel auf Debitorengruppenebene angewendet wird. 
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt.
2. Sobald Sie den Bereich angegeben haben, müssen Sie die **Kontengruppe** angeben, die im Bereich verwendet wird.
   - Für den Bereich **Tabelle** bietet die Suche eine Liste der Debitoren zur Auswahl. 
   - Wählen Sie eine **Gruppe**, wenn die Regel für eine Kreditverwaltungsgruppe für Debitoren gilt.
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt. 
3. Wählen Sie eine **Risikogruppe**, um die Liste der Debitoren, die für das Kreditmanagement reserviert werden, weiter einzuschränken. 
4. Wählen Sie die Art der Regel aus, die Sie einrichten. 
   - Wählen Sie **Sperrung**, um eine Regel zu erstellen, die eine Bestellung sperrt. 
   - Wählen Sie **Ausschluss**, um eine Regel zu erstellen, die eine andere Regel vom Sperren einer Bestellung ausschließt. 
5. Geben Sie die **Tage Kreditlimit abgelaufen** für die ausgewählte Sperrregel an, bevor eine Bestellung im Kreditmanagement gehalten wird. Die Anzahl der überfälligen Tage gibt zusätzliche Kulanztage an, die zu der Anzahl der Tage hinzuaddiert werden, an denen das Kreditlimit abgelaufen ist.

### <a name="overdue-amount"></a>Überfälliger Betrag

Öffnen Sie die Registerkarte **Überfälliger Betrag**, wenn die Sperrregel für Kunden mit überfälligen Beträgen gilt.
1. Wählen Sie den Debitorenbereich aus, für den diese Regel **Gültig für** gilt.
   - Wählen Sie **Tabelle**, wenn die Regel für einen bestimmten Debitor gilt.
   - Wählen Sie **Gruppe**, wenn die Regel auf Debitorengruppenebene angewendet wird. 
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt.
2. Sobald Sie den Bereich angegeben haben, müssen Sie die **Kontengruppe** angeben, die im Bereich verwendet wird.
   - Für den Bereich **Tabelle** bietet die Suche eine Debitorensuche. 
   - Wählen Sie eine **Gruppe**, wenn die Regel für eine Kreditverwaltungsgruppe für Debitoren gilt.
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt. 
3. Wählen Sie eine **Risikogruppe**, wenn Sie die Liste der Debitoren, die für das Kreditmanagement reserviert werden, weiter einschränken möchten. 
4. Wählen Sie die Art der Regel aus, die Sie einrichten. 
   - Wählen Sie **Sperrung**, um eine Regel zu erstellen, die eine Bestellung sperrt. 
   - Wählen Sie **Ausschluss**, um eine Regel zu erstellen, die eine andere Regel vom Sperren einer Bestellung ausschließt. 
5. Geben Sie **Überfälliger Betrag** für die ausgewählte Sperrregel an, bevor eine Bestellung im Kreditmanagement zur Überprüfung gehalten wird. 
6. Wählen Sie den **Werttyp**, der die Art des Werts festgelegt, mit dem auch geprüft wird, wie viel von dem Kreditlimit verwendet wurde. Sperrregeln erfordern einen Prozentsatz, aber ein Ausschluss kann einen festen Betrag oder Prozentsatz haben. Die Schwelle bezieht sich auf das Kreditlimit.
7. Geben Sie den Wert **Kreditlimitschwelle** für die ausgewählte Regel ein, bevor ein Kunde das Kreditmanagement einstellt. Dies kann ein Betrag oder ein Prozentsatz sein, der auf dem im Wertetyp ausgewählten Wertetyp basiert.
8. Die Regel prüft, ob der **Überfällige Betrag** und die **Kreditlimitschwelle** überschritten ist. 

### <a name="sales-order"></a>Auftrag 

Wählen Sie **Auftrag**, wenn die Sperrregel für den Wert des Auftrags gilt.
1. Wählen Sie den Debitorenbereich aus, für den diese Regel **Gültig für** gilt.
   - Wählen Sie **Tabelle**, wenn die Regel für einen bestimmten Debitor gilt.
   - Wählen Sie **Gruppe**, wenn die Regel auf Debitorengruppenebene angewendet wird. 
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt.
2. Sobald Sie den Bereich angegeben haben, müssen Sie die **Kontengruppe** angeben, die im Bereich verwendet wird.
   - Für den Bereich **Tabelle** bietet die Suche eine Debitorensuche. 
   - Wählen Sie eine **Gruppe**, wenn die Regel für eine Kreditverwaltungsgruppe für Debitoren gilt.
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt. 
3. Wählen Sie eine **Risikogruppe**, wenn Sie die Liste der Debitoren, die für das Kreditmanagement reserviert werden, weiter einschränken möchten. 
4. Wählen Sie die Art der Regel aus, die Sie einrichten.  
   - Wählen Sie **Sperrung**, um eine Regel zu erstellen, die eine Bestellung sperrt. 
   - Wählen Sie **Ausschluss**, um eine Regel zu erstellen, die eine andere Regel vom Sperren einer Bestellung ausschließt. 
5. Geben Sie den **Auftragsbetrag** für die ausgewählte Sperrregel an, bevor eine Bestellung im Kreditmanagement gehalten wird. 

Die Auftragsregel enthält eine zusätzliche Einstellung, die alle anderen Regeln außer Kraft setzt. Um einen Ausschluss zu erstellen, durch den der Auftrag freigegeben wird, ohne dass andere Regeln wirksam werden, markieren Sie das Kontrollkästchen **Auftragskommissionierung** in der Ausschlusszeile.

### <a name="credit-limit-used"></a>Verwendetes Kreditlimit

Wählen Sie **Kreditlimit verwendet**, wenn die Sperrregel für den genutzten Kreditlimitbetrag des Debitor gilt.
1. Wählen Sie den Debitorenbereich aus, für den diese Regel **Gültig für** gilt.
   - Wählen Sie **Tabelle**, wenn die Regel für einen bestimmten Debitor gilt.
   - Wählen Sie **Gruppe**, wenn die Regel auf Debitorengruppenebene angewendet wird. 
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt.
2. Sobald Sie den Bereich angegeben haben, müssen Sie die **Kontengruppe** angeben, die im Bereich verwendet wird.
   - Für den Bereich **Tabelle** bietet die Suche eine Debitorensuche. 
   - Wählen Sie eine **Gruppe**, wenn die Regel für eine Kreditverwaltungsgruppe für Debitoren gilt.
   - Wählen Sie alle **Alle**, wenn die Regel für alle Debitoren gilt. 
3. Wählen Sie eine **Risikogruppe**, wenn Sie die Liste der Debitoren, die für das Kreditmanagement reserviert werden, weiter einschränken möchten. 
4. Wählen Sie die Art der Regel aus, die Sie einrichten.
   - Wählen Sie **Sperrung**, um eine Regel zu erstellen, die eine Bestellung sperrt. 
   - Wählen Sie **Ausschluss**, um eine Regel zu erstellen, die eine andere Regel vom Sperren einer Bestellung ausschließt. 
5. Wählen Sie die **Restschwelle**, die den Prozentsatz des Kreditlimits definiert, der den Auftrag blockiert. Wenn der Wert einer Bestellung den Betrag des verwendeten Kreditlimits über den Prozentsatz erhöht, wird die Bestellung gesperrt. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Einen Auftrag auf der Grundlage anderer Kriterien in die Warteschleife setzen
  
### <a name="rank-payment-terms"></a>Rangfolge der Zahlungsbedingungen erstellen  

Sie können die Ausführung der Kreditkontrollregeln erzwingen, wenn Zahlungsbedingungen geändert werden. Sie müssen die Zahlungsbedingungen bewerten und ihnen einen Bewertungswert zuweisen. Wenn Sie die Zahlungsbedingungen der Bestellung in Zahlungsbedingungen ändern, die höher als die alten Zahlungsbedingungen eingestuft sind, wird die Bestellung an das Kreditmanagement gesendet und muss genehmigt werden.

Sie können die Rangfolge der Zahlungsbedingungen auf der Seite **Kreditmanagement > Setup > Kreditmanagementsetup > Rangzahlungsbedingungen** einrichten.

1. Wählen Sie die Zahlungsbedingungen aus dem zu ordnenden Feld **Zahlungsbedingungen** aus; Wenn Sie einen Begriff auswählen, wird die Beschreibung im Feld **Beschreibung** angezeigt.
2. Wählen Sie den Rang des Begriffs im Feld **Rang** aus. Die Werte sind alle relativ zueinander, sodass Sie 1,2,3 oder 10,20,30 verwenden können. Sie können für die meisten Zahlungsbedingungen auch denselben Wert verwenden, sodass nur ein oder zwei Zahlungsbedingungen die Bonitätsprüfung auslösen.

### <a name="rank-settlement-discounts"></a>Rangfolge für Rabattausgleiche erstellen   

Sie können die Ausführung der Kreditkontrollregeln erzwingen, wenn Ausgleichsrabatte geändert werden. Sie müssen die Ausgleichsrabatte sortieren und ihnen einen Bewertungswert zuweisen. Wenn Sie die Ausgleichsrabatte der Bestellung in Ausgleichsrabatte ändern, die höher als die alten Ausgleichsrabatte eingestuft sind, wird die Bestellung an das Kreditmanagement gesendet und muss genehmigt werden.

Sie können die Rangfolge der Zahlungsbedingungen auf der Seite **Kreditmanagement > Setup > Kreditmanagementsetup > Rangausgleichsrabatte** einrichten.

1. Wählen Sie das **Skonto**, das Sie sortieren möchten. Die **Beschreibung**des Abrechnungsrabattes wird angezeigt.
2. Wählen Sie den Wert **Rang** aus. Die Werte sind alle relativ zueinander, sodass Sie 1,2,3 oder 10,20,30 verwenden können. Sie können für die meisten Ausgleichsrabatte auch denselben Wert verwenden, sodass nur ein oder zwei Ausgleichsrabatte die Bonitätsprüfung auslösen.

## <a name="sequence-the-application-of-rules"></a>Reihenfolge der Anwendung von Regeln

Die Regeln werden in einer bestimmten Reihenfolge ausgeführt, die Sie an die Anforderungen Ihrer Organisation anpassen. 

- Mit einer Instanz der Ausschlussregeln für Aufträge können Sie alle Regeln außer Kraft setzen, die einen Auftrag blockieren könnten. Erstellen Sie eine Kundenauftragsausschlussregel und markieren Sie die Option **Auftrag freigeben**. Die Bestellung wird nicht zurückgestellt, wenn diese Ausschlussregel wahr ist, und es werden keine anderen Regeln überprüft.
- Sperrregeln können die Bestellung zurückstellen.
- Ausschlussregeln werden nach Sperrregeln ausgeführt. Ausschlussregeln wirken sich nur auf die Regel aus, für die sie definiert sind. 
- Sperr- und Ausschlussregeln werden in der Reihenfolge Tabelle, Gruppe und Alle ausgeführt. Aufgrund dieser Verarbeitungsreihenfolge ist es möglich, dass auf der Ebene „Alle“ eine Sperrregel vorhanden ist, die nicht ausgeführt wird, da auf der Ebene „Tabelle“ oder „Gruppe“ eine Ausschlussregel ausgeführt wird.
- Ausschlüsse setzen die Sperrregel nicht außer Kraft, wenn sie sich auf derselben Ebene befinden. Beispielsweise überschreibt eine Ausschlussregel auf Gruppenebene die Sperrregel auf Gruppenebene nicht. Sie müssen keine Ausschlüsse auf der Ebene „Alle“ einrichten, außer wie oben mit der einen Instanz der Ausschlussregel für Aufträge angegeben. 

Das Verhalten der Regel **Kreditlimit verwendet** ändert sich basierend auf den Einstellungen für die Parameter **Kreditlimit für Auftrag prüfen**, der sich im Parameterformular „Kredit und Inkasso“ befindet.
- Wenn der Parameter auf Nein gesetzt ist, wird die Regel für das verwendete Kreditlimit nicht ausgeführt.
- Wenn der Parameter auf Ja gesetzt ist und die **Meldung bei Überschreitung des Kreditlimits** auf Warnung eingestellt ist, erhalten Sie eine Warnung, wenn das Kreditlimit überschritten wird. Die Regeln **Kreditlimit verwendet** werden ausgeführt, um festzustellen, ob Regeln vorhanden sind, die ausgeführt werden sollen. In diesem Szenario würden Sie jedoch normalerweise keine Regeln hinzufügen.
- Wenn der Parameter auf Ja gesetzt ist und die **Meldung bei Überschreitung des Kreditlimits** auf Fehler gesetzt ist, dann wird das Kreditlimit überprüft und die Bestellung wird gesperrt, wenn das Kreditlimit überschritten wird. Darüber hinaus werden die Regeln **Kreditlimit verwendet** ausgeführt, um festzustellen, ob zusätzliche Regeln vorhanden sind, die ausgeführt werden sollen. Eine Fehlermeldung wird nicht angezeigt, aber der Sperrgrund **Kreditlimit überschritten** wird angezeigt. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Einstellungen, die die Art und Weise ändern, in der eine Bestellung gesperrt wird

Aufträge können auch dann vom Kreditmanagement ausgeschlossen werden, wenn Regeln vorhanden sind. 

- Wenn Sie die Einstellungen **Kunde vom Kreditmanagement ausschließen** in **Alle Kunden > Kunde auswählen > Kredit und Inkasso** auf **Ja** ändern, dann werden keine Aufträge für diesen Kunden bearbeitet
- Wenn Sie den Wert **Vom Kreditmanagement ausschließen** im **Auftragskopf**in der **Inforegister für die Kreditverwaltung** zu **Ja** ändern, werden die Kreditverwaltungsregeln nicht verarbeitet. Diese Einstellung kann nur vom Kreditkaufmann oder Kreditmanager vorgenommen werden.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Bearbeitung von gesperrten Aufträgen über die Kreditmanagement-Sperrliste

In der Kreditmanagement-Sperrliste können Kreditmanager alle gesperrten Aufträge anzeigen und die Sperren entfernen, wenn die Kreditprobleme behoben wurden. Die Seite **Halteliste für das Kreditmanagement** zeigt alle Aufträge an, die gesperrt wurden. Sie können die Warteliste auf der Seite **Alle Kredite halten** (**Kreditmanagement > Kreditmanagement-Sperrliste> Alle Sperrlisten**) anzeigen.
Kundenaufträge von allen juristischen Personen werden an dieselbe Kreditverwaltungs-Sperrliste gesendet. Auf diese Weise erhalten Sie eine zentrale Ansicht aller Transaktionen, die Ihre Aufmerksamkeit erfordern. Benutzer sehen nur die Informationen für die juristischen Personen, auf die sie zugreifen können.

Ein Auftrag kann aus folgenden Gründen in die Warteliste aufgenommen werden:
1. Der Debitor hat eine Rechnung, die für eine bestimmte Anzahl von Tagen überfällig ist. 
2. Die Bestellung hat einen bestimmten Kontostatus.
3. Die Bestellung hat bestimmte Zahlungsbedingungen.
4. Der Debitor hat ein abgelaufenes Kreditlimit.
5. Der Debitor hat einen überfälligen Betrag und bestimmten Prozentsatz seines Kreditlimits verwendet
6. Der Auftrag überschreitet einen bestimmten Betrag.
7. Der Debitor hat einen bestimmten Prozentsatz seines Kreditlimits überschritten.
8. Die Zahlungsbedingungen weichen von den Standard-Zahlungsbedingungen für den Debitor ab.
9. Die Ausgleichsrabatte weichen vom Standardausgleichsrabatt für den Debitor ab.

Der Sperrgrund wird für jeden Auftrag in der Sperrliste angezeigt. Wenn es mehr als einen Grund für die Sperre gibt, wird der Grund als **Mehrere** angezeigt. Sie können das Menü **Sperrgründe** im Aktionsbereich verwenden, um alle Gründe anzuzeigen, warum der Auftrag gesperrt wurde. Sie können auch die **Blockierungsgründe** in einer FactBox anzeigen.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Aufträge aus der Sperrliste zur Bearbeitung freigeben

Wenn Sie die Gründe für die Sperre untersucht und behoben haben, können Sie die Kundenaufträge zur weiteren Verarbeitung freigeben.

1) Wählen Sie eine Position in der Sperrliste aus. Sie können mehrere Aufträge freigeben, indem Sie mehr als eine Zeile auswählen.
2) Wählen Sie einen **Grund für die Freigabe** für den Auftrag, der zur Freigabe ausgewählt wurde.  
3) Geben Sie **Prüfdatum** für jeden Auftrag ein, der zur Freigabe ausgewählt wurde.  
4) Wählen aus dem Menü **Freigabe** im Aktionsbereich, um eine Bestellung freizugeben. Dieses Menü ist nur verfügbar, nachdem Transaktionen ausgewählt wurden. Dem Benutzer werden zwei Optionen angeboten:
   - Wählen Sie **Mit Buchung**, um die Sperre zu entfernen und das Dokument zu buchen, indem Sie denselben Buchungsprozess verwenden, der ausgeführt wurde, als der Auftrag gesperrt wurde. Wenn beispielsweise die Auftragsbestätigung gesperrt wurde, wird die Auftragsbestätigung nach der Freigabe abgeschlossen. Das Auftragsbuchungsformular wird angezeigt, damit der Benutzer die Bestätigung buchen kann.
   - Wählen Sie **Ohne Buchung**, um die Sperre ohne weitere Bearbeitung zu entfernen. Der Auftrag kann manuell gebucht werden.

### <a name="rejecting-orders-in-the-hold-list"></a>Aufträge in der Warteliste ablehnen
Sie können das Menü **Ablehnen** im Aktionsbereich verwenden, um einen Auftrag abzulehnen
1. Wählen Sie eine Position in der Sperrliste aus. Sie können mehrere Aufträge freigeben, indem Sie mehr als eine Zeile auswählen.
2. Die Bestellung wird aus der Sperrliste entfernt und der Auftragskopf wird aktualisiert, um anzuzeigen, dass die Bestellung abgelehnt wurde.

### <a name="automatically-releasing-credit-management-holds"></a>Automatische Freigaben von Kreditmanagementsperren
Aufträge werden basierend auf den Sperrregeln in die Sperrliste aufgenommen. Einige Gründe für die Sperren können sich jedoch im Laufe der Zeit ändern, wenn der Auftrag für einen bestimmten Zeitraum in der Sperrliste verbleibt. Beispielsweise kann ein Kunde seine Rechnung bezahlen und so sein Kreditlimit aufheben. 

Sie können das Menü **Zur Freigabe auswerten** verwenden, um die Aufträge in der Sperrliste zu überprüfen und automatisch freizugeben, wenn der Grund für die Sperrung behoben wurde.
1.  Das Menü **Zur Freigabe auswerten** auswählen
2.  Wählen Sie **Sperrregeln verarbeiten**, um alle Aufträge zu überprüfen. Wählen Sie **Sperrregeln für ausgewählte Zeilen verarbeiten**, um nur die von Ihnen ausgewählten Zeilen zu überprüfen.
3. Ein Schieberegler wird angezeigt, mit dem Sie einen einzelnen Debitor auswählen können. Lassen Sie das Debitorendropdown für alle Debitoren leer. 
4. Wenn Sie auf OK klicken, wird der Prozess im Hintergrund ausgeführt und Sie können weitere Aufgaben ausführen. Wenn Sie die Stapelverarbeitung auswählen, bevor Sie auf OK klicken, wird der Prozess im Stapel ausgeführt, wenn Sie auf OK klicken. Es kann einige Zeit dauern, bis die in der Liste der gesperrten Bestellungen verarbeitet ist. Aktualisieren Sie den Status der Bestellungen mit Aktualisieren. 
5.  Wenn ein Sperrgrund für eine Bestellung nicht mehr gilt, wird der Sperrgrund als ungültig betrachtet und Sie sehen beim Anzeigen der Sperrgründe kein Häkchen neben dem Grund mehr.
6.  Wenn alle Sperrgründe beseitigt sind, wird ein neuer Grund **Bereit zur Freigabe** zur Liste der Sperrgründe hinzugefügt. Der Auftrag kann automatisch freigegeben werden.
7.  Wenn die Parameter **Automatisch freigeben** in der Registerkarte **Kredit und Inkasso > Einstellungen> Kredit und Inkassoparameter> Kredit > Automatische Freigabe** auf **Mit Buchung** gesetzt ist, werden Sie aufgefordert, das Buchungsformular für das gesperrte Dokument zu verwenden.
8.  Wenn die Parameter **Automatisch freigeben** in der Registerkarte **Kredit und Inkasso > Einstellungen> Kredit und Inkassoparameter> Kredit > Automatische Freigabe** auf **Mit Buchung** gesetzt ist, werden Sie aufgefordert, das Buchungsformular für das gesperrte Dokument zu verwenden.

### <a name="credit-management-approval-workflow"></a>Workflow zur Genehmigung des Kreditmanagements

Sie können auch **Kreditmanagement-Workflows** erstellen, um die Freigabe von Kreditsperren zu kontrollieren. Sobald Sie den Workflow mit der Seite **Kreditmanagement > Einstellung > Kreditmanagement-Workflows** eingerichtet haben, werden die zur Freigabe oder Ablehnung markierten Aufträge an den Workflow gesendet, wo sie zuerst genehmigt werden müssen, bevor sie freigegeben oder abgelehnt werden. 

Wenn Sie die Aufgaben zur Freigabe mit Buchung oder Freigabe ohne Buchung in Ihren Workflow aufnehmen, gibt die Workflow-Genehmigung auch den Auftrag frei. Wenn der Freigabeprozess jedoch aufgrund fehlender Einrichtungsinformationen oder anderer Ursachen fehlschlägt, müssen Sie den Auftrag aus dem Workflow zurückrufen, das Problem beheben, das den Fehler verursacht hat, und den Auftrag erneut an den Workflow senden.

Wenn Sie die Aufgaben zur Freigabe mit Buchung oder Freigabe ohne Buchung nicht in Ihren Workflow aufnehmen, können Sie den Auftrag nach Abschluss der Genehmigung über den Workflow-Genehmigungsprozess einfach manuell freigeben.

### <a name="forced-credit-hold"></a>Erzwungenes Halten von Krediten  
  
Manchmal müssen Aufträge gesperrt werden, obwohl die Bestellung nicht den Kriterien der Sperrregeln entspricht. Beispielsweise kann ein Kreditmanager über ein nicht kreditbezogenes Problem beim Debitor benachrichtigt werden und entscheiden, Aufträge sofort manuell zu sperren, bis das Problem behoben ist. Sie können einen Auftrag manuell in die Warteschleife zwingen, wenn diese Situation eintritt.

1. Öffnen Sie den Auftrag, den Sie sperren möchten.  
2. Wählen Sie **Erzwungenes Halten von Krediten** in der Registerkarte **Kreditmanagement** im Aktionsbereich **Kreditmanagement**.
3. Wählen Sie einen **Grund für erzwungenes Halten**.
4. Klicken Sie auf **OK.** Der Auftrag wird an die Kreditmanagement-Sperrliste zurückgegeben.

Sie können auch das Sperren mehrerer Aufträge mit der Seite **Kreditmanagement > Regelmäßige Aufgaben> Erzwungenes Halten von Krediten** erzwingen. So können Sie beispielsweise alle Aufträge für einen bestimmten Debitor sperren.
1. Wählen Sie einen **Grund für erzwungenes Halten**. 
2. Klicken Sie auf **Einzuschließende Datensätze**, um die Aufträge auszuwählen, die gesperrt werden sollen. 
3. Klicken Sie auf **OK**, um die ausgewählten Aufträge zu bearbeiten.

Gesperrte Kundenaufträge können nicht mit dem Workflow verarbeitet werden.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Freigeben von Aufträgen, die der Kreditmanagement-Sperrliste mit einer erzwungenen Kreditsperre hinzugefügt wurden
Kundenaufträge mit einem Grund für erzwungenes Halten können nicht automatisch freigegeben werden. Wenn der Auftrag gesperrt wurde und Sie einen Prozess verwendet haben, der Aufträge automatisch freigibt, wird der Auftrag als **Bereit zur Freigabe** angezeigt und bleibt in der Warteliste. Sie müssen das Menü **Freigabe** verwenden, um die Bestellung freizugeben.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Freitext-Rechnungen, Aufträge und Unterstützung von Projektrechnungen im Kreditmanagement 
Das Kreditmanagement kann derzeit nur für Aufträge verwendet werden. Freitext-Rechnungen, Point-of-Sales-Aufträge und Call-Center-Aufträge verwenden die temporären Kreditlimits und Versicherungen/Garantien, die Sie zur Anpassung des Kreditlimits hinzufügen. Sie verwenden die Sperrregeln nicht und werden nicht in die Sperrliste aufgenommen, wenn ein Problem mit dem Kreditlimit vorliegt.

Projektrechnungen werden im Kreditmanagement nicht unterstützt.
