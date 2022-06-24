---
title: Fahrten verwalten
description: Dieser Artikel beschreibt, wie Sie mit Fahrten arbeiten. Eine Fahrt stellt normalerweise ein Schiff dar. Abhängig von Ihren Praktiken und Verfahren kann sie jedoch auch einen Lieferanten, eine Einkaufsbestellung oder einen anderen Artikel darstellen, der für Ihr Unternehmen sinnvoll ist.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 43f28a7e30dbbe15bb02d26483289f25515fcfca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905862"
---
# <a name="manage-voyages"></a>Fahrten verwalten

[!include [banner](../../includes/banner.md)]

Eine Fahrt stellt normalerweise ein Schiff dar. Abhängig von Ihren Praktiken und Verfahren kann sie jedoch auch einen Lieferanten, eine Einkaufsbestellung oder einen anderen Artikel darstellen, der für Ihr Unternehmen sinnvoll ist.

Die Seite **Alle Fahrten** enthält Details zur Fahrt, Informationen zur Lieferung und Kalkulation sowie Informationen zu Artikeln, Einkaufsbestellungen und Umlagerungsaufträgen. Um die Seite **Alle Fahrten** zu öffnen, gehen Sie auf **Gesamttransportkosten \> Fahrten \> Alle Fahrten**. Diese Seite zeigt eine Liste aller aktuellen Fahrten an. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Fahrten zu erstellen, zu löschen und mit ihnen zu arbeiten. Wählen Sie eine beliebige Fahrt in der Liste aus, um ihre Details anzuzeigen.

> [!NOTE]
> Transportcontainer und Paletten sind mit einer Fahrt verknüpft. Kaufzeilen sind mit einem Transportcontainer verknüpft. Wenn Transportcontainer und Paletten ausgeschaltet sind, können sie auch direkt mit einer Fahrt verknüpft werden. Außerdem werden Kosten, die hier eingegeben werden, auf alle angehängten Kauf-Zeilen umgelegt.

## <a name="action-pane"></a>Aktivitätsbereich

Der Aktivitätsbereich der Seite **Fahrtn** bietet Schaltflächen, mit denen Sie mit einer ausgewählten Fahrt arbeiten können. Jede Schaltfläche führt eine einzelne Aktion aus. Der Aktivitätsbereich enthält auch Registerkarten, von denen jede wiederum eine Reihe von zugehörigen Schaltflächen bereitstellt. Sofern nicht anders angegeben, sind alle Schaltflächen und Registerkarten sowohl in der Listenansicht der Seite **Alle Fahrten** als auch in der Detailansicht für eine einzelne ausgewählte Fahrt verfügbar.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Schaltflächen, die direkt im Aktivitätsbereich erscheinen

Die folgende Tabelle beschreibt die Schaltflächen, die direkt im Aktivitätsbereich verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Neue | Erstellen Sie eine Fahrt. <!-- KFM: Link to scenario --> |
| Löschen | Löschen Sie die aktuelle Fahrt. Es können nur Fahrten gelöscht werden, die einen Fahrtenstatus von *Bestätigt* haben. Nachdem eine Fahrt den Hafen verlassen und Waren in Zustellung verarbeitet hat, kann sie nicht mehr gelöscht werden. |
| Seereisebearbeitung | Öffnen Sie die Seite **Fahrt-Editor**, wo Sie Kauf-Zeilen für die Fahrt hinzufügen oder entfernen, neue Container erstellen und Details der Fahrt selbst ändern können. |
| Seereisekosten | Öffnen Sie die Seite **Fahrtkosten**, auf der Sie die Kalkulationen für alle Waren der Fahrt anzeigen und hinzufügen können. Wenn Fahrtkosten manuell zur Fahrt hinzugefügt werden, werden sie automatisch auf der Seite **Kostenabfrage** hinzugefügt und auf jede Ware gemäß der Methode aufgeteilt, die auf der Seite **Fahrtkosten** angegeben ist. |

### <a name="buttons-on-the-voyage-tab"></a>Schaltflächen auf der Registerkarte Fahrt

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Fahrt** des Aktivitätsbereichs verfügbar sind. Diese Registerkarte ist nur verfügbar, wenn Sie in der Listenansicht der Seite **Alle Fahrten** arbeiten.

| Schaltfläche | Beschreibung |
|---|---|
| Versandcontainer | Öffnen Sie eine Seite, die alle Transportcontainer anzeigt, die mit der ausgewählten Fahrt verbunden sind. Es kann ein Container oder viele Container sein. |
| Folio | Öffnen Sie eine Seite, die alle Paletten anzeigt, die mit der ausgewählten Fahrt verknüpft sind. Es kann eine oder mehrere Paletten geben. |

### <a name="buttons-on-the-manage-tab"></a>Schaltflächen auf der Registerkarte Manage

Die folgende Tabelle beschreibt die Aktionen, die auf der Registerkarte **Verwalten** des Aktivitätsbereichs verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Belege empfangen | Aktualisieren Sie die Fahrt, so dass die Option **Dokumente empfangen** auf *Ja* festgelegt ist. Mit dieser Schaltfläche können Sie den Artikel und/oder die Kauf-Zeile sperren, so dass sie nicht weiter aktualisiert werden können. |
| Unterwegs | Aktualisieren Sie das Feld **Fahrtstatus** auf den Status in Zustellung, der auf der Seite **[Parameter für Gesamttransportkosten](landed-cost-parameters.md)** festgelegt ist. Für diesen Vorgang gibt es keine weitere Logik. Eine Fahrt kann auch automatisch auf den In-Transit-Status aktualisiert werden, basierend auf den Einstellungen im [Tracking-Control-Center](delivery-information-setup.md).
| Bereit für die Nachkalkulation | Aktualisieren Sie das Feld **Fahrtstatus** auf den Status „bereit für die Kalkulation“, der auf der Seite **[Gesamttransportkosten-Parameter](landed-cost-parameters.md)** festgelegt ist. Eine Fahrt kann kalkuliert werden, wenn alle Rechnungen bearbeitet wurden (sowohl Lagerrechnungen als auch Fahrtkostenrechnungen) und die Waren eingegangen sind. Wenn die geschätzten Kosten, die mit einer Fahrt verbunden sind, nicht kalkuliert wurden, tritt ein Fehler auf, wenn Sie versuchen, die Kalkulation einer Fahrt zu bearbeiten. |
| Mit Kosten | Bereinigen Sie alle Unregelmäßigkeiten in der Kalkulation, nachdem eine Rechnung für alle Einkaufsbestellungen und Fahrten vorliegt. Wenn Sie diese Schaltfläche wählen, erscheint die Dialogbox **Fahrt aktualisieren - kalkuliert**. Dort können Sie auswählen, dass zum Standard-Finanzdatum gebucht werden soll oder ein Buchungsdatum angeben und dann die Aktion ausführen. Sie können die Aktion so oft wiederholen, wie Sie wollen. Sie können auch die Dialogbox **Fahrt aktualisieren - kalkuliert** verwenden, um einen Zeitplan für die Ausführung der Aktion als periodische Aufgabe (Batch-Job) einzurichten. Wir empfehlen Ihnen, die Aktion regelmäßig auszuführen, indem Sie sie als Batch-Job festlegen. |
| Zugangsliste buchen | Buchen Sie eine Eingangsliste für alle Zeilen der Einkaufsbestellung in der Fahrt.  |
| Produktzugang buchen | Buchen Sie einen Wareneingang für alle Zeilen der Einkaufsbestellung in der Fahrt. Der Wareneingangsprozess für die Bestellzeilen, die mit einer Fahrt verbunden sind, wird nur verwendet, wenn die Waren **nicht** durch die Waren in Zustellung gehen. Wenn die Waren die Waren-in-Zustellung-Verarbeitung durchlaufen, erhalten Sie einen Fehler, wenn Sie versuchen, den Wareneingang für eine Einkaufsbestellung zu buchen.  |
| Rechnung buchen | Buchen Sie eine Rechnung für alle Zeilen der Einkaufsbestellung in der Fahrt. Wenn die Waren auf der Fahrt eine Waren in Zustellung durchlaufen, werden die Zeilen der Einkaufsbestellung in Rechnung gestellt, bevor der Empfangsprozess abgeschlossen ist. Wenn die ursprüngliche Bestellung fakturiert wird, werden die Waren in Zustellung erstellt, die mit den ursprünglichen Einkaufsbestellungen verbunden sind. Diese Aufträge können dann vom Lagerort entgegengenommen werden.  |
| Umlagerungsauftrag versenden | Buchen Sie eine Umlagerungsauftrags-Fahrt für alle Transportauftragszeilen in der Fahrt. Wenn diese Schaltfläche ausgewählt ist, stehen nur Umlagerungsaufträge zur Aktualisierung zur Verfügung. |
| Umlagerungsauftrag empfangen | Buchen Sie einen Transportauftragseingang für alle Transportauftragszeilen in der Fahrt. |
| Waren in Zustellung empfangen | Empfangen Sie alle Transportauftragszeilen, die sich in der Fahrt in Zustellung befinden. Diese Schaltfläche ist eine von drei Optionen, die für den Empfang von Waren in Zustellung auf einer Fahrt zur Verfügung stehen. (Die anderen beiden Optionen sind die Schaltfläche **Wareneingangserfassung erstellen**, die später in dieser Tabelle beschrieben wird, und die Warehouse Management Mobile App). Diese Option ist die einfachste und verarbeitet die Waren in Zustellung aus dem Lagerort in Zustellung in das endgültige Ziellager. Wenn Sie mehr Kontrolle über den Prozess haben möchten, verwenden Sie die Wareneingangserfassung oder ein mobiles Gerät, um den Eingang der Waren zu verarbeiten. |
| Automatische Kosten suchen | Finden Sie alle relevanten Kosten für die Fahrt. Wenn diese Kalkulationen bereits gefunden oder aktualisiert wurden, erhalten Sie die folgende Meldung: „Es existieren nicht kalkulierte Kostenzeilen. Möchten Sie diese überschreiben?“ Es werden alle Kosten gefunden, die zum Zeitpunkt der Erstellung nicht mit der Fahrt verknüpft waren. Fahrtkosten, die an eine Fahrt angehängt sind und die kalkuliert wurden, werden nicht überschrieben. |
| Eingangserfassung erstellen | <p>Öffnen Sie das Dialogfeld **Ankunftserfassung erstellen**, in dem Sie eine Wareneingangserfassung erstellen können, die einen Lagerplatz angibt. Das Dialogfeld bietet die folgenden Optionen:</p><ul><li>**Erstellen aus Waren in Zustellung** oder **Erstellen aus Umlagerungsauftrag** - Das Label für diese Option ändert sich, je nachdem, ob Sie den Prozess Waren in Zustellung verwenden. Legen Sie sie auf *Ja* fest, um eine Seite für die Wareneingangserfassung zu öffnen, mit der Sie eine Standard-Erfassung für die Waren in Zustellung, die mit der Fahrt verbunden sind, verarbeiten können. Wenn der Artikel bereits im endgültigen Ziellagerort eingegangen ist, wird er nicht zu den Zeilen der Wareneingangserfassung hinzugefügt.</li><li>**Menge initialisieren** - Legen Sie diese Option auf *Ja* fest, um die Menge zu initialisieren, die empfangen wird, basierend auf der Menge der Waren, die in der Zeile der Fahrt angegeben ist. Wenn die Zeile der Fahrt teilweise empfangen wurde, ist diese Menge die Restmenge. Wir empfehlen, diese Option auf *Ja* festzulegen.</li><li>**Erstellen aus Auftragszeilen** - Legen Sie diese Option auf *Ja* fest, um den Wert aus den Auftragszeilen zu übernehmen.</li></ul><p>Diese Schaltfläche ist eine von drei Optionen, die für den Empfang von Waren auf einer Fahrt zur Verfügung stehen. (Die anderen Optionen sind die **Waren in Zustellung empfangen**-Schaltfläche, die weiter oben in dieser Tabelle beschrieben wurde, und die Warehouse Management Mobile App.)</p> |
| Kosten antizipieren | Sie können Kosten anfallen lassen, wenn für eine Kostenart ein Hauptbuchkonto für die Belastung angegeben ist. Diese Schaltfläche wird typischerweise verwendet, wenn sich der Bestand in Zustellung befindet oder wenn Waren eingegangen sind und in Rechnung gestellt wurden. |
| Kosten aggregieren | Verschieben Sie die Kalkulationen von der Ebene des Transportcontainers auf die Ebene der Fahrt. Sie können diese Schaltfläche in einem Szenario mit gemeinsam genutzten Serviceen/Versand verwenden, in dem sich mehrere Entitäten einen Transportcontainer oder Kartonplatz teilen. Die Fahrt hat z. B. einen 40-Fuß-Transportcontainer und einen 20-Fuß-Transportcontainer, und die Aufteilung erfolgt nach Volumen. In diesem Fall könnten die Waren/Entitäten, die sich den Platz im 20-Fuß-Transportcontainer teilen oder nutzen, benachteiligt werden. Um die Kosten gerecht zu verteilen, möchten einige Organisationen die Kosten auf die Fahrt übertragen und sie auf der Grundlage der Umlagemethode auf Fahrtebene verteilen. |
| Reisevorlage ändern | Öffnen Sie ein Dialogfeld, in dem Sie die Vorlage für die Route ändern können. Nachdem Sie die Vorlage geändert haben, werden die Kalkulationen für die Fahrt gelöscht. Daher müssen Sie eventuell **Autokalkulationen finden** (siehe die Beschreibung weiter oben in dieser Tabelle) wählen oder die Kosten manuell neu hinzufügen. |

### <a name="buttons-on-the-general-tab"></a>Schaltflächen auf der Registerkarte Allgemein

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Allgemein** des Aktivitätsbereichs verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Zugangsliste | Öffnen Sie eine Liste der Produkteingänge für alle Zeilen der Einkaufsbestellung in der Fahrt.  Wenn noch keine Wareneingangslisten bearbeitet wurden, ist diese Schaltfläche nicht verfügbar. |
| Produktzugang | Öffnen Sie den Produkteingangsdatensatz für die Zeilen der Einkaufsbestellung, die mit der Fahrt verbunden sind, wenn dieser Datensatz verwendet wird. Wenn noch keine Wareneingänge gebucht wurden, ist diese Schaltfläche nicht verfügbar. Der Wareneingangsprozess wird nicht verwendet, wenn Sie die Waren in Zustellung verwenden. |
| Wareneingang | Öffnen Sie die Wareneingangserfassung, wenn sie verwendet wird. |
| Nachverfolgung | Öffnen Sie die Seite **Eingangsverfolgung**, auf der Sie das erwartete Ankunftsdatum von Waren in einem Transportcontainer und einer Fahrt aktualisieren können und anschließend die erwarteten Liefertermine von Einkaufsbestellungen aktualisieren können. |
| Kostenabfrage | <p>Öffnen Sie die Seite **Kostenabfrage**, auf der alle Kalkulationen einer Fahrt angezeigt werden.</p><p>Wählen Sie **Ansicht** im Aktivitätsbereich, um die Ansicht anzupassen. Sie können jede der Ebenen sowie den Artikel und den Code der Kalkulation anzeigen.</p><p>Auf der Seite **Kostenabfrage** werden nur Kostenartencodes angezeigt, die in direktem Zusammenhang mit Transaktionen im Bestand stehen. Indem Sie Kostenartencodes entfernen, können Sie die Seite durch Gruppierung von Kalkulationen anpassen. Diese Funktionalität kann nützlich sein, wenn Sie Größen und Farben verwenden.</p><p>Die Seite **Kostenabfrage** zeigt nur Kostenartencodes an, bei denen das Feld **Belastung** auf *Artikel* festgelegt ist.</p> |
| Waren in Zustellung-Aufträge | Öffnen Sie die Seite **Waren in Zustellung**, die nur die Waren in Zustellung für die ausgewählte Fahrt anzeigt. |

## <a name="lines-view"></a>Ansicht Zeilen

Um die Ansicht **Linien** zu öffnen, öffnen Sie eine Fahrt und wählen dann die Registerkarte **Linien** oben rechts in der Kopfzeile der Fahrt.

### <a name="information-on-the-voyage-header-fasttab"></a>Informationen zum Inforegister der Fahrt-Kopfzeile

Das **Fahrtkopf** Inforegister in der **Zeilen**-Ansicht einer Fahrt enthält grundlegende Informationen, die die Fahrt beschreiben. Viele der Felder, die auf dieser Inforegisterkarte erscheinen, erscheinen auch in der Ansicht **Kopfzeile**, wie später in diesem Artikel beschrieben.

### <a name="information-on-the-voyage-lines-fasttab"></a>Informationen auf der Inforegisterkarte Fahrtzeilen

Das Inforegister **Fahrt-Linien** in der Ansicht **Linien** einer Fahrt bezieht sich auf die Fahrtdetails und die Informationen zur Kalkulation, die auf der Ebene der Fahrt gelten. Hier können Sie die Transportcontainer, Paletten und Artikel überprüfen, die an die Fahrt angehängt sind. Der Preis und die Menge der Artikel auf der Fahrt werden ebenfalls angezeigt. Sie können jeden aufgelisteten Transportcontainer oder jede Palette anzeigen, indem Sie den entsprechenden Link auswählen.

### <a name="information-on-the-line-details-fasttab"></a>Informationen auf dem Inforegister Details der Zeile

Die **Liniendetails** Inforegister in der **Linien**-Ansicht einer Fahrt bietet weitere Informationen über die Linie, die aktuell auf der **Fahrt-Linien** Inforegister ausgewählt ist. Beachten Sie, dass dieses Inforegister Details über die Position enthält, die jede Zeile im Container einnimmt, sowie ihre deklarierte Menge.

## <a name="header-view"></a>Kopfzeilenansicht

Um die Ansicht **Kopfzeile** zu öffnen, öffnen Sie eine Fahrt, und wählen Sie dann die Registerkarte **Kopfzeile** oben rechts in der Überschrift der Fahrt.

### <a name="settings-on-the-general-fasttab"></a>Einstellungen auf der Registerkarte Allgemein

Die folgende Tabelle beschreibt die Felder, die auf dem Inforegister **Allgemein** in der Ansicht **Kopfzeile** einer Fahrt verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Seereise | Geben Sie die Fahrt- oder Flugnummer ein. |
| Buchungsreferenz | Wenn Ihr Verlader oder Versandzentrum eine Referenznummer zur Identifizierung der Fahrt bereitstellt (d.h. die interne Referenz des Verladers oder Versandzentrums), geben Sie diese hier ein. |
| Schiff | Geben Sie das Schiff ein oder wählen Sie es aus. Wenn das Schiff nicht als Wert aufgeführt ist, können Sie die Schiffs-ID als freien Text eingeben. In diesem Fall wird die Haupttabelle nicht aktualisiert, so dass die Schiffs-ID später in diesem Feld ausgewählt werden kann. |
| Externe Seereise-ID | Geben Sie die öffentlich verfügbare ID für die Fahrt ein (z. B. die Flugnummer). |
| Master-Luftfrachtbrief/-Frachtbrief | Geben Sie die Nummer des Master-Luftfrachtbriefs oder des Konnossements ein. Sie können diesen Wert beim Luftfrachtversand angeben. |
| Haus-Luftfrachtbrief/-Frachtbrief | Geben Sie den Haus-Luftfrachtbrief oder das Konnossement für den Transportcontainer ein. |
| Vermietung | Aktivieren Sie dieses Kontrollkästchen, um anzugeben, dass es sich bei dem Container um einen Mietcontainer handelt, der zurückgegeben werden muss. |
| Beschreibung | Geben Sie eine Beschreibung der Fahrt ein, um sie leichter erkennen zu können. |
| Seereisestatus | Der Status der Fahrt. Werte umfassen *Erstellt*, *In Transit*, *Dokumente erhalten* und *Kalkuliert*. Dieses Feld wird nicht auf Basis einer Logik berechnet. Es wird nur über die Buchungsaktion aktualisiert. Der Wert *Kalkuliert* zeigt an, dass eine Rechnung für den Bestand und alle Kosten der Fahrt eingegangen ist. Solange keine Rechnung eingegangen ist, kann eine Fahrt nicht den Status *Kalkuliert* erreichen. |
| Bestellungsstatus | Der höchste Status, der unter allen Einkaufsbestellungen, die mit der Fahrt verbunden sind, erreicht wurde. |
| Belege empfangen | Ein Wert, der angibt, ob Ihre Firma alle Dokumente erhalten hat, die mit der Fahrt verbunden sind. Um den Wert zu ändern, wählen Sie **Dokumente erhalten** in der Gruppe **Fahrtaktualisierung** auf der Registerkarte **Verwalten** des Aktivitätsbereichs. |
| Versandunternehmen | Wählen Sie die Reederei für diese Fahrt aus. Dieses Feld kann zur Ermittlung der Autokalkulation verwendet werden. |
| Name | Der Name der Firma, die im Feld **Schiffsgesellschaft** ausgewählt ist. |
| Verbrauchsberechnung | In diesem Feld kann eine Messung in einer Autokalkulation angegeben werden. Messungen werden oft von Unternehmen verwendet, die das individuelle Volumen oder Gewicht der Waren nicht kennen, aber eine genauere Aufteilung benötigen, als sie die Menge oder Quantität bietet. Der Spediteur stellt das Gewicht oder die kubische Messung zur Verfügung, und Sie können es entweder auf der Ebene eines Artikels oder der Einkaufsbestellung einlagern. Es kann automatisch aktualisiert werden, wenn der Parameter ausgewählt ist, oder es kann manuell eingegeben werden. |
| Maßeinheit | Die Maßeinheit, die für die Zahl im Feld **Messung** gilt. |
| Anzahl der Paletten | Geben Sie die Anzahl der Paletten in der Zeile für die Fahrt an. Dieses Feld wird automatisch aktualisiert, wenn die Option **Anzahl der Kartons automatisch aktualisieren** auf der Registerkarte **Allgemein** der Seite **Gesamttransportkostenparameter** auf *Ja* festgelegt ist. |

### <a name="settings-on-the-delivery-fasttab"></a>Einstellungen auf dem Inforegister Lieferung

Die folgende Tabelle beschreibt die Felder, die auf dem Inforegister **Lieferung** in der Ansicht **Kopfzeile** einer Fahrt verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Datum und Uhrzeit der Erstellung | Das Datum und die Uhrzeit, zu der der Datensatz der Fahrt erstellt wurde. |
| Ab Werk-Datum | Dieses Feld wählt das früheste Ab-Werk-Datum unter den Einkaufsbestellungen aus, die mit der Fahrt verknüpft sind. Das Ab-Werk-Datum ist in der Kopfzeile der Einkaufsbestellung verfügbar und wird mit Hilfe der Funktion zur Nachverfolgungssteuerung aktualisiert. |
| Versanddatum | Das geschätzte Datum, an dem das Flugzeug oder Schiff den Ursprungsort verlässt. |
| Abgangsdatum | Das Abfahrtsdatum ist normalerweise das Datum, an dem das Flugzeug oder Schiff den Überseehafen tatsächlich verlässt. Das Schiffsdatum und das Abfahrtsdatum müssen nicht übereinstimmen. Das Feld **Abfahrtsdatum** dient nur zu Informationszwecken. Es wird nicht verwendet, um das voraussichtliche Lieferdatum zu schätzen. Die Funktion zur Kontrolle der Sendungsverfolgung wird verwendet, um das voraussichtliche Lieferdatum zu schätzen, und dieses Feld kann so festgelegt werden, dass es automatisch von der Funktion zur Kontrolle der Sendungsverfolgung ausgefüllt wird. |
| In Shop-Datum | Dieses Feld wählt das früheste Datum aus, an dem die Waren aus den Einkaufsbestellungen, die mit der Fahrt verknüpft sind, zum Verkauf zur Verfügung stehen werden. |
| Vorkalkuliertes Lieferdatum | Das geschätzte Lieferdatum ist normalerweise das Datum, an dem die Waren im Lagerort eintreffen sollen. Dieses Feld dient nur zu Informationszwecken. Es wird nicht für die Produktprogrammplanung für Waren verwendet. Das voraussichtliche Lieferdatum in der Zeile der Einkaufsbestellung wird für die Produktprogrammplanung für Waren auf einer Fahrt verwendet und mit Hilfe der Funktion zur Nachverfolgungssteuerung aktualisiert. Dieses Feld kann so festgelegt werden, dass es von der Tracking Control Funktion ausgefüllt wird. |
| Tatsächliches Lieferdatum | Das früheste Lieferdatum, basierend auf den Waren, die mit der Fahrt verbunden sind. |
| ETA am Versandport. | Geben Sie das Datum ein, an dem Sie erwarten, dass die Fahrt am Lieferhafen ankommt, basierend auf den Informationen, die von Ihrem Spediteur bereitgestellt wurden. |
| Ursprüngliche Belege empfangen | Geben Sie das Datum ein, an dem die Originaldokumente empfangen wurden. |
| Vom Broker empfohlen | Geben Sie das Datum ein, an dem der Broker benachrichtigt wurde. |
| Gesendetes Original-Konnossement | Geben Sie das Datum ein, an dem das Originalkonnossement verschickt wurde. |
| Warenfreigabe | Geben Sie das Datum ein, an dem die Waren aus dem Zoll freigegeben wurden. |
| Debitorentermin | Geben Sie das Datum des Kundentermins ein, d. h. das Datum, an dem Sie erwarten, dass der Kunde die Waren in Besitz nimmt. |
| Auslieferung am Lagerort | Geben Sie das Datum ein, an dem die Waren an den Lagerort geliefert wurden. |
| Überprüfungsdatum | Geben Sie das Verifizierungsdatum ein. |
| Lieferanweisungen | Geben Sie das Datum ein, an dem die Lieferanweisungen empfangen wurden. |
| Lieferart | Dieses Feld enthält Informationen über die Methode, mit der die Fahrt geliefert wird, und die Auswahl der Autokalkulationen, die mit dieser Liefermethode verbunden sind. |
| Von-Port | Der Lieferhafen, von dem die Fahrt ausgeht. |
| Bis-Port | Der Lieferhafen, an dem die Fahrt ankommt. Die Transportcontainer können verschiedene Häfen haben, da das Schiff möglicherweise in mehreren Häfen anhält. Durch die Überprüfung des „An“-Hafens auf der Ebene des Transportcontainers stellen Sie genaue Hafenangaben für jeden Transportcontainer auf einer Fahrt bereit. Die Autokalkulation, die mit der Fracht verbunden ist, wird anhand der Kombination aus dem Transportcontainer-Typ, dem „An“-Hafen und dem „Von“-Hafen ermittelt. |
| Lokale Weiterleitung | Dieses Feld dient nur zu Informationszwecken. Der lokale Spediteur sollte aus der Lieferantentabelle wählbar sein. |
| Datum des lokalen Transports | Das Datum, für das der Nahverkehr gebucht ist. Dieses Feld kann dem Lagerort bei seiner Planung helfen. |
| Uhrzeit des lokalen Transports | Die Zuteilung von Zeitfenstern, für die der Nahverkehr gebucht ist. Dieses Feld kann dem Lagerort bei seiner Planung helfen. |
| Reisevorlage | Die Fahrtenvorlage, die für die Fahrt angegeben wird. Die Fahrtenvorlage wird verwendet, um den „An“- und „Von“-Hafen des Transportcontainers und der Fahrt einzugeben. Diese Werte helfen wiederum, die Autokalkulationen zu identifizieren, die mit der Fahrt verbunden sind. |

### <a name="settings-on-the-other-fasttab"></a>Einstellungen auf dem anderen Inforegister

Die folgende Tabelle beschreibt die Felder, die auf dem Inforegister **Sonstiges** in der Ansicht **Kopfzeile** einer Fahrt verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Bemerkungen | Geben Sie zusätzliche Informationen ein, die sich auf die Fahrt beziehen. |
| Bewertungsdatum | Wählen Sie das früheste Ab-Werk-Datum für die Einkaufsbestellungen, die mit der Fahrt verknüpft sind. |
| Ausstehende Seereise | Damit können Sie angeben, ob die Sendung oder die Fahrt bereits abgefahren ist. Es dient nur zu Informationszwecken.  |
| Transportcontainer umbenennen | Bei Fahrten, die mehr als einen Container haben, die Anzahl der Container, die noch nicht eingegangen sind. |

## <a name="voyage-update-periodic-tasks"></a>Periodische Aufgaben der Fahrtaktualisierung

Das Modul **Gesamttransportkosten** enthält mehrere periodische Aufgaben, die verschiedene Aspekte von Fahrten aktualisieren können. Um diese periodischen Aufgaben auszuführen oder zu planen, gehen Sie zu **Gesamttransportkosten \> Periodische Aufgaben \> Fahrtaktualisierung**, und wählen Sie dann einen der folgenden Aufgabentypen:

- **Eingehende Dokumente** - Mit dieser Aufgabe können Sie **Eingehende Dokumente** auf *Ja* für mehrere Fahrten gleichzeitig festlegen. Verwenden Sie die Einstellungen **Filter**, um die Menge der Fahrten festzulegen, die Sie aktualisieren möchten.
- **Im Transit** - Mit dieser Aufgabe können Sie das Feld **Fahrtstatus** auf den Status in Zustellung festlegen, der auf der Seite **[Gesamttransportkosten-Parameter](landed-cost-parameters.md)** für mehrere Fahrten gleichzeitig festgelegt ist. Verwenden Sie die Einstellungen **Filter**, um die Menge der Fahrten festzulegen, die Sie aktualisieren möchten.
- **Bereit zur Kalkulation** - Mit dieser Aufgabe können Sie das Feld **Fahrtstatus** auf den Status „Bereit zur Kalkulation“ festlegen, der auf der Seite **[Gesamttransportkosten-Parameter](landed-cost-parameters.md)** für mehrere Fahrten gleichzeitig festgelegt wird. In der Regel werden Sie diese Aufgabe so festlegen, dass sie nach einem regelmäßigen Zeitplan abläuft.
- **Kalkuliert** - Mit dieser Aufgabe können Sie das Feld **Fahrtstatus** auf den kalkulierten Status festlegen, der auf der Seite **[Gesamttransportkosten-Parameter](landed-cost-parameters.md)** für mehrere Fahrten gleichzeitig festgelegt ist, sofern sie kalkuliert, aber noch nicht auf der Fahrt aktualisiert wurden. In der Regel werden Sie diese Aufgabe so festlegen, dass sie nach einem regelmäßigen Zeitplan abläuft.
