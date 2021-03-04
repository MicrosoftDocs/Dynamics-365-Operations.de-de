---
title: Behebung von Problemen in der diskreten Fertigung
description: Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der diskreten Fertigung auftreten können.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 604e0c3406b15d885991fcb067e93ef83533e3b0
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516788"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Fehlersuche in der diskreten Fertigung

Dieses Thema beschreibt, wie Sie Probleme beheben können, die bei der Arbeit mit der diskreten Fertigung auftreten können.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Ich erhalte die folgende Fehlermeldung: „Die Prozesse der Lagerortverwaltung werden derzeit verwendet. Wenn Arbeitszeilen noch nicht registriert sind, können Sie die erstellte Arbeit und alle Lade- oder Versandzeilen stornieren und dann mit dem Kommissionier- oder Versandprozess fortfahren.“

### <a name="issue-description"></a>Problembeschreibung

Dieses Problem tritt auf, wenn Sie versuchen, Arbeit für eine Zeile zu reservieren oder freizugeben, aber die Bestandstransaktion den Status *Entnommen* hat, was bedeutet, dass das Material entnommen wurde.

### <a name="issue-resolution"></a>Problemlösung

Um dieses Problem zu beheben, führen Sie einen der folgenden Schritte aus.

- Ändern Sie den Status des Produktionsauftrags zurück auf *Geschätzt* oder *Freigegeben*.
- Öffnen Sie die Detailseite für den betreffenden Produktionsauftrag. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Lagerort** in der Gruppe **Anhalten** die Option **Anhalten und Entnehmen**, um alle entnommenen Transaktionen zu entnehmen. Wählen Sie dann **Stopp entfernen**, um den Produktionsauftrag zu bearbeiten.

Hier eine Erklärung der Funktionen *Auspicken* und *Stopp*:

- **Entnehmen** - Diese Funktion kehrt den Status von Bestandstransaktionen für Stücklisten- und Formelzeilen um, die einen Status von *Kommissioniert* bis *Auf Bestellung* haben. Wenn die Arbeit für die Rohmaterialkommissionierung abgeschlossen ist, wird der Status der Zeilen auf *Kommissioniert* festgelegt. Dieser Status verhindert, dass der Produktionsauftrag auf den Status *Erstellt* zurückgesetzt wird. In diesem Fall können Sie die Funktion *Entnahme rückgängig machen* verwenden, um die Vorgänge aus dem Status *Entnahme rückgängig machen* zurückzusetzen und dann den Produktionsauftrag auf den Status *Created* zurückzusetzen.
- **Anhalten** - Diese Funktion legt ein **Angehalten** Flag für den Produktionsauftrag fest, um jede Statusaktualisierung des Auftrags zu verhindern. Sie finden das Flag **Angehalten** auf dem Inforegister **Lagerort** der Detailseite des Produktionsauftrags.

> [!NOTE]
>
> - Die Schaltflächen sind nur sichtbar, wenn der Produktionsauftrag für Elemente erstellt wird, die für Lagerprozesse aktiviert sind.
> - Die Gruppe **Anhalten** ist nur auf der Registerkarte **Lagerort** im Aktivitätsbereich der Seite mit den Produktionsauftragsdetails sichtbar. Sie ist auf dem Inforegister **Lagerort** der Listenseite **Produktionsaufträge** nicht sichtbar.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>Der passende Ressourcenname wird nicht aktualisiert, nachdem ich einen Namen einer Arbeitskraft im globalen Adressbuch geändert habe.

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie einen Namen einer Arbeitskraft im globalen Adressbuch ändern, wird der passende Ressourcenname nicht im Ressourcengruppenstamm aktualisiert.

### <a name="issue-resolution"></a>Problemlösung

Dieses Szenario wird derzeit nicht unterstützt. Um das Problem zu beheben, müssen Sie den Ressourcennamen manuell aktualisieren.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Wenn ich einen neuen Produktionsauftrag erstelle, erhalte ich nicht die folgende Meldung: „Fügen Sie die aktive Version von Stückliste und Arbeitsplan ein?“

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie einen neuen Produktionsauftrag erstellen, werden nach Eingabe der Elementnummer die Felder **Standort** und **Lagerort** automatisch auf den Standard-Standort und den Standard-Lagerort festgelegt, die auf der Seite **Standard-Auftragseinstellungen** für den Artikel der fertigen Ware definiert sind. Zusätzlich werden die aktive Stückliste und der Arbeitsplan automatisch eingetragen. Sie erhalten nicht die folgende Meldung, die Sie zur Eingabe dieser Werte auffordert:

> Aktive Version für Stückliste und Arbeitsplan einfügen?

### <a name="issue-resolution"></a>Problemlösung

Sie werden nicht aufgefordert, Stückliste und Arbeitsplan einzugeben, wenn Sie ein Produkt auswählen, für das ein Standort und ein Lagerort auf der Seite **Standardauftragseinstellungen** festgelegt sind. Sie werden nur aufgefordert, wenn diese Werte nicht für das ausgewählte Produkt definiert sind.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Produktionsaufträge werden nicht auf der Seite Markierung angezeigt.

### <a name="issue-description"></a>Problembeschreibung

Einige Produktionsaufträge werden nicht auf der Seite **Beschriftung** angezeigt.

### <a name="issue-resolution"></a>Problemlösung

Produkte, die die folgende Konfiguration haben, sind nicht für die Markierung verfügbar. Daher werden sie nicht auf der Seite **Beschriftung** angezeigt:

- Die Produkte sind als Produkte vom Typ *Artikelgewicht* definiert.
- Sie sind für die erweiterten Lagerort-Prozesse aktiviert.
- Sie sind so konfiguriert, dass sie nach dem Prinzip *Standardkosten* gesteuert werden.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Wenn ich versuche, einen Produktionsauftrag zu beenden, erhalte ich die folgende Fehlermeldung: „Der Wert für die Berechnung der Stückliste consumptionCost muss bei der Ausgabe aus dem Bestand negativ sein.“

Dieses Problem wurde in Version 10.0.15 behoben.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Wenn ich den Status eines Produktionsauftrags von Als fertig gemeldet auf Beenden ändere, erhalte ich folgende Fehlermeldung: „Aktualisierungskonflikt. Die Standardkosten stimmen nicht mit dem finanziellen Bestandswert nach der Aktualisierung überein“ und „In der Funktion InventCostMovement.checkVariance ist ein kritischer Fehler aufgetreten.“

Dieses Problem tritt auf, weil die zugrunde liegenden Daten von einem anderen Prozess geändert wurden. Der Prozess versucht bis zu fünf Mal, die Daten zu aktualisieren. Wenn der Konflikt nach fünf Versuchen immer noch besteht, erhalten Sie die folgenden Fehlermeldungen:

> Aktualisierungskonflikt. Die Standardkosten stimmen nicht mit dem Wert des finanziellen Bestands nach der Aktualisierung überein.

> Es ist ein kritischer Fehler in der Funktion InventCostMovement.checkVariance aufgetreten.

Dieses Verhalten ist beabsichtigt. Um das Problem zu beheben, setzen Sie den Batch-Job fort. Er sollte zu Ende laufen.

Wenn der Batch-Job nach der Wiederaufnahme immer wieder fehlschlägt, überprüfen Sie, ob die Rundungsgenauigkeit für die Standardwährung des Ledgers mit der Rundung übereinstimmt, die auf die Werte in der Tabelle InventSum angewendet wird. Wenn die Rundungsgenauigkeit auf einen nicht konformen Wert geändert wurde, müssen Sie sie wahrscheinlich wieder auf einen konformen Wert ändern. Suchen Sie nach **ModifiedDateTime**. In diesem Fall zeigt der Wert typischerweise an, dass die Rundungsgenauigkeit kürzlich geändert wurde.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Bei der Freigabe an einen Lagerort erhalte ich die folgende Fehlermeldung: „Element RM konnte nicht vollständig reserviert werden. Stellen Sie sicher, dass die volle Menge verfügbar ist, oder reservieren Sie die Elemente manuell, wenn das Feld Reservierung in der Stückliste-Zeile auf Manuell oder Gestartet festgelegt ist. Der Auftrag konnte nicht an das Lagerort freigegeben werden, da einige Materialien nicht reserviert werden konnten.“ Der Status wird jedoch auf Freigegeben aktualisiert.

### <a name="issue-description"></a>Problembeschreibung

Wenn bei der Freigabe eines Produktionsauftrags nicht alle Elemente der Stückliste physisch verfügbar sind und die Richtlinie **Freigeben an Lagerort** auf *Vollständige Reservierung erforderlich* auf dem Produktionsauftrag festgelegt ist, erhalten Sie die folgende Fehlermeldung:

> Element RM konnte nicht vollständig reserviert werden. Stellen Sie sicher, dass die volle Menge verfügbar ist, oder reservieren Sie die Elemente manuell, wenn das Feld Reservierung in der Stückliste-Zeile auf Manuell oder Gestartet festgelegt ist. Der Auftrag konnte nicht für den Lagerort freigegeben werden, weil einige Materialien nicht reserviert werden konnten.

### <a name="issue-resolution"></a>Problemlösung

Dieses Verhalten ist gewollt und funktioniert wie erwartet.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Wenn ich versuche, einen Produktionsauftrag zu beenden und als erledigt zu melden, erhalte ich die folgende Fehlermeldung: „Die gesamte Warenmenge, die für die Produktion als fertig gemeldet wird, ist %1. Die Rückmeldung für den letzten Vorgang ist insgesamt 0,00.“

### <a name="issue-description"></a>Problembeschreibung

Wenn Sie versuchen, einen Bericht als fertiggestellte Erfassung auf einen Produktionsauftrag zu buchen, erhalten Sie die folgende Fehlermeldung:

> Gesamte als fertig gemeldete Gutmenge für die Produktion wird %1 sein. Die Rückmeldung für den letzten Vorgang ist insgesamt 0,00.

### <a name="possible-cause"></a>Mögliche Ursache

Dieses Problem tritt auf, wenn die Mengen, die in den letzten Vorgängen gebucht wurden, falsch waren. Wenn z.B. die Produktion gestartet wird, aber die Menge, die gestartet werden muss, nicht zugeordnet ist, wird die Arbeitsplan-Erfassung ohne Zeilen gebucht. Um die Situation zu bestätigen, öffnen Sie den Produktionsauftrag, und wählen Sie dann im Aktivitätsbereich auf der Registerkarte **Ansicht** die Option **Arbeitsplan**.

### <a name="workaround"></a>Problemumgehung

Sie können dieses Problem beheben, indem Sie zusätzliche Erfassungen für die Vorgänge buchen, für die die Erfassungen nicht korrekt gebucht wurden. Starten Sie den Produktionsauftrag neu und wählen Sie, um die zusätzlichen Erfassungen zu buchen. Durch diese Aktion wird der Produktionsauftrag nicht gestartet, aber die Erfassungen werden gebucht. Der Arbeitsplan sollte dann die gebuchten Mengen anzeigen, und Sie sollten die Produktionsaufträge erfolgreich beenden können.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Kann ich einen Produktionsauftrag als beendet melden, während ich die Fehlermenge melde, aber nicht, während ich die Zeit- oder Materialmenge melde?

Sie können die Fehlermenge eines Produktionsauftrags nicht melden, wenn Sie nicht auch die Warenmenge melden. Dieses Szenario wird **nicht** unterstützt. Wenn Sie versuchen, den Produktionsauftrag zu beenden, schlägt die Bericht-als-erledigt-Aktualisierung schließlich fehl, und Sie erhalten die folgende Fehlermeldung:

> Fertigmeldungsmenge fehlt.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Kann ich die Seriennummern der fertigen Ware gegen die Seriennummern der verbrauchten Ware verfolgen?

Sie können die Seriennummern von fertiger Ware nicht gegen die Seriennummern von Material abgleichen, das ein Produktionsauftrag verbraucht, um diese fertige Ware herzustellen. Dieses Szenario wird derzeit nicht unterstützt. Die Abhilfe besteht darin, Produktionsaufträge für eine Menge von 1 zu erstellen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]