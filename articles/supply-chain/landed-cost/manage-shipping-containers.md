---
title: Verwalten von Transportcontainern
description: Dieses Thema beschreibt, wie Sie mit Transportcontainern arbeiten. Transportcontainer werden verwendet, um Waren zusammenzufassen, die physikalisch zusammengehören. Sie werden auch in Fällen verwendet, in denen die Kosten nur auf diese Waren aufgeteilt werden müssen, normalerweise weil sie physisch zusammen sind.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ac88f8e3b8cf305a5bd247e7ed6b14b23ad85499
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686768"
---
# <a name="manage-shipping-containers"></a>Verwalten von Transportcontainern

[!include [banner](../../includes/banner.md)]

Transportcontainer werden verwendet, um Waren zusammenzufassen, die physikalisch zusammengehören. Sie werden auch in Fällen verwendet, in denen die Kosten nur auf diese Waren aufgeteilt werden müssen, normalerweise weil sie physisch zusammen sind.

Um Waren über die Transportcontainer-Seite anzuzeigen und zu bearbeiten, gehen Sie auf **Gesamttransportkosten \> Transportcontainer \> Alle Transportcontainer**. Die Seite **Alle Transportcontainer** zeigt eine Liste aller verfügbaren Transportcontainer. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um Transportcontainer zu erstellen, zu löschen und mit ihnen zu arbeiten. Wählen Sie einen beliebigen Transportcontainer in der Liste aus, um seine Details auf der Seite **Versandcontainer** anzuzeigen.

Der obere Teil der Transportcontainer-Detailseite zeigt Transportcontainer- und Kalkulationsinformationen an. Der Bereich **Zeilen** zeigt die Paletten, Artikel und Einkaufsbestellungen oder Umlagerungsaufträge an, die an den Container angehängt sind.

## <a name="action-pane"></a>Aktivitätsbereich

Der Aktivitätsbereich auf den Seiten **Alle Transportcontainer** und **Versandcontainer** enthält Schaltflächen, mit denen Sie mit einem ausgewählten Transportcontainer arbeiten können. Jede Schaltfläche führt eine einzelne Aktion aus. Der Aktivitätsbereich enthält auch Registerkarten, von denen jede wiederum eine Reihe von zugehörigen Schaltflächen bereitstellt. Sofern nicht anders angegeben, sind alle Schaltflächen und Registerkarten, die in den folgenden Unterabschnitten beschrieben werden, sowohl in der Listenansicht (d.h. auf der Seite **Alle Transportcontainer**) als auch in der Detailansicht (d.h. auf der Seite **Versandcontainer**) verfügbar.

### <a name="buttons-on-the-manage-tab"></a>Schaltflächen auf der Registerkarte Manage

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Verwalten** des Aktivitätsbereichs verfügbar sind.

| Schaltfläche | Beschreibungen |
|---|---|
| Zugangsliste buchen | Buchen Sie eine Bonliste, oder zeigen Sie die Wareneingangslisten für alle Zeilen der Einkaufsbestellung im Transportcontainer an. Wenn Sendungen mit mehreren Firmen verwendet werden, wird für jede Firma ein neues Dialogfenster zum Buchen einer Bonliste geöffnet. |
| Produktzugang buchen | Buchen Sie einen Wareneingang für alle Zeilen der Einkaufsbestellung im Transportcontainer. |
| Rechnung buchen | Buchen Sie eine Rechnung für alle Zeilen der Einkaufsbestellung im Transportcontainer. Bei Sendungen mit mehreren Firmen wird für jede Firma ein neues Dialogfeld für die Rechnungsbuchung geöffnet. |
| Umlagerungsauftrag versenden | Buchen Sie einen Umlagerungsauftragsversand für alle Umlagerungsauftragszeilen im Transportcontainer. Nur die Zeilen im Transportcontainer, die eine Art von Umlagerungsauftrag sind, erscheinen in dem Dialogfenster. |
| Umlagerungsauftrag empfangen | Buchen Sie einen Transportauftragseingang für alle Transportauftragszeilen im Transportcontainer. Das Empfangsdialogfeld ist die einfachste Möglichkeit, Waren in einem Transportcontainer oder auf einer Fahrt zu empfangen, und ist eine von drei verfügbaren Optionen. Sie können auch über Wareneingangserfassungen oder die Verarbeitung mit mobilen Geräten empfangen. |
| Eingangserfassung erstellen | Sie können eine Wareneingangserfassung für Organisationen generieren, indem Sie erweiterte Funktionen für Lagerorte verwenden. Die Optionen sind _Menge initialisieren_ (empfohlen), und entweder _Erstellen aus Waren in Zustellung_ oder _Erstellen aus Einkaufsbestellungen_. Die letzten beiden Optionen hängen davon ab, ob die Verarbeitung von Waren in Zustellung verwendet wird. |
| Umbenennen | Öffnen Sie ein Dialogfeld, in dem Sie einen ausgewählten Transportcontainer umbenennen können. |
| Reisevorlage ändern | Ändern Sie die Route-Vorlage. Nachdem Sie die Route-Vorlage geändert haben, müssen Sie möglicherweise **Autokalkulationen finden** wählen oder die Kalkulationen erneut manuell hinzufügen, da die Versandkosten gelöscht werden. |
| In Vermietung konvertieren | Wandeln Sie einen ausgewählten Transportcontainer in einen Miet-Transportcontainer um. |

### <a name="buttons-on-the-general-tab"></a>Schaltflächen auf der Registerkarte Allgemein

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Allgemein** des Aktivitätsbereichs verfügbar sind.

| Schaltfläche | Beschreibungen |
|---|---|
| Zugangsliste | Buchen Sie eine Eingangsliste für alle Zeilen der Einkaufsbestellung im Transportcontainer. Wenn Fahrten mit mehreren Firmen verwendet werden, wird für jede Firma ein neues Dialogfeld für die Buchung der Eingangsliste geöffnet. |
| Produktzugang | Zeigen Sie den Wareneingangsdatensatz an, wenn er verwendet wird. Der Wareneingangsprozess wird nur verwendet, wenn die Waren nicht die Waren in Zustellung-Funktionalität verwenden. |
| Wareneingang | Zeigen Sie die Wareneingangserfassung für den Transportcontainer an, wenn dieses Journal verwendet wird. |
| Teilstrecken | Abschnitte werden verwendet, um separate Teile einer Route zu identifizieren. Vorlaufzeiten können mit jedem Abschnitt verknüpft werden, um die Sendungsverfolgung zu erleichtern. Weitere Informationen finden Sie unter [Einrichten von Routen mit mehreren Abschnitten](multi-leg-journey-setup.md). |
| Nachverfolgung | Anzeigen oder Aktualisieren der Sendungsverfolgung. |
| Waren in Zustellung-Aufträge | Sie können die Seite **Waren in Zustellung** direkt aus dem Container öffnen. Diese Seite zeigt nur die Waren in Zustellung für den ausgewählten Transportcontainer an. |

## <a name="header-view"></a>Kopfzeilenansicht

Um die Ansicht **Kopfzeile** zu öffnen, öffnen Sie einen Transportcontainer und wählen dann die Registerkarte **Kopfzeile** oben rechts in der Überschrift des Transportcontainers.

### <a name="settings-on-the-general-fasttab"></a>Einstellungen auf der Registerkarte Allgemein

Die folgende Tabelle beschreibt die Einstellungen, die auf der Registerkarte **Allgemein** des Inforegisters der Ansicht **Kopf** eines Transportcontainers verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Versandcontainer | Der Name des Transportcontainers. |
| Seereise | Die Fahrt, die mit dem Transportcontainer verbunden ist. |
| Versandcontainertyp | Geben Sie den Transportcontainer-Typ ein. Dieses Feld muss festgelegt werden. Sie können es verwenden, um die Kosten für die Fracht zu bestimmen, indem Sie z. B. die Autokalkulation auswählen, die mit dem Transportcontainer-Typ verbunden ist. |
| Schiff | Geben Sie das Schiff ein oder wählen Sie es aus. Wenn das Schiff nicht als Wert aufgeführt ist, können Sie die Schiffs-ID als freien Text eingeben. In diesem Fall wird die Haupttabelle nicht aktualisiert, so dass die Schiffs-ID später in diesem Feld ausgewählt werden kann. Für weitere Informationen siehe [Schiffe](shipping-information-setup.md#vessels). |
| Einheitstyp | Einheitentypen werden als zusätzliches Mittel zur Gruppierung und Identifizierung von Transportcontainern verwendet. Sie werden auf der Transportcontainer-Seite angezeigt und ausgewählt. Weitere Informationen finden Sie unter [Einrichtung von Einheitentypen](shipping-container-setup.md#unit-types). |
| Kühlungsart | Kühltypen werden als zusätzliches Mittel zur Gruppierung und Identifizierung von Transportcontainern, meist Kühlcontainern, verwendet. Sie werden auf der Transportcontainer-Seite angezeigt und ausgewählt. Weitere Informationen finden Sie unter [Kühltypen festlegen](shipping-container-setup.md#refrigeration-types). |
| Verbrauchsberechnung | Mit diesem Feld kann eine Messung im Modul **Gesamttransportkosten** angegeben werden. Kennzahlen werden oft von Organisationen verwendet, die das individuelle Volumen oder Gewicht von Waren nicht kennen, aber eine genauere Aufteilung benötigen, als die Menge oder Quantität liefert. Die Spedition stellt das Gewicht in Kilogramm oder die kubische Messung zur Verfügung, und Sie können es entweder auf der Ebene eines Artikels oder der Einkaufsbestellung einlagern. Es kann automatisch aktualisiert werden, wenn der Parameter ausgewählt ist, oder es kann manuell eingegeben werden. |
| Maßeinheit | Die Maßeinheit, die für die Zahl im Feld **Messung** gilt. |
| Tatsächliches Gewicht | Sie können das tatsächliche Gewicht des Kartons oder Behälters erfassen. Dieser Wert kann zur Überprüfung gegen das maximale Gewicht verwendet werden, das beim Einrichten eines Transportcontainers erlaubt ist. |
| Anzahl der Kartons | Die Anzahl der Kartons wird automatisch aktualisiert, wenn der Parameter ausgewählt ist. |
| Warenbeschreibung | Eine Beschreibung der Waren kann im Kopf des Transportcontainers oder der Palette ausgewählt werden. Sie dient dazu, eine Fahrt, einen Transportcontainer oder eine Palette von Waren zu identifizieren. Weitere Informationen finden Sie unter [Beschreibung der Waren](shipping-information-setup.md#description-of-goods). |
| Haus-Luftfrachtbrief/-Frachtbrief | Sie können den Haus-Luftfrachtbrief oder das Konnossement für den Transportcontainer angeben. |
| Bemerkungen | Zusätzliche Informationen, die sich auf den Transportcontainer beziehen. |
| Retourfähig | Ein Wert, der angibt, ob der Transportcontainer nach der Fahrt zurückgegeben werden kann. |
| Seereisestatus | Der Status der Route, die mit dem Transportcontainer verknüpft ist. |
| Bestellungsstatus | Der Status der Einkaufsbestellung, die mit dem Transportcontainer verknüpft ist. |

### <a name="settings-on-the-delivery-fasttab"></a>Einstellungen auf dem Inforegister Lieferung

Die folgende Tabelle beschreibt die Einstellungen, die auf der Registerkarte **Lieferung** des Inforegisters der Ansicht **Kopf** eines Transportcontainers verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Datum und Uhrzeit der Erstellung | Das Datum und die Uhrzeit, zu der der Container erstellt wurde. |
| Ab Werk-Datum | Dieses Datum wird in der Regel der Fabrik/dem Lieferanten mitgeteilt, um anzugeben, wann Sie erwarten, dass die Waren das Werksgelände verlassen. Wenn Sie mit einer Fabrik in Asien arbeiten, wird dieses Datum oft anstelle des Datums benötigt, zu dem Sie die Waren erwarten. (Im Gegensatz dazu ist bei einer lokalen Lieferung das Datum, bis zu dem Sie die Waren erwarten, erforderlich). Dieses Feld kann aus den Zeilen der Einkaufsbestellung in der Transportcontainer-Liste ausgefüllt werden. Sie können es hier auch manuell eingeben. |
| Versanddatum | Dieses Datum kann auf dem Dokument der Einkaufsbestellung ausgedruckt werden. Es informiert die Fabrik/den Lieferanten normalerweise über das Datum, bis zu dem die Waren an den Hafen geliefert werden sollen. Dieses Feld dient nur zu Informationszwecken. Es wird nicht verwendet, um das voraussichtliche Lieferdatum der Waren im Transportcontainer abzuschätzen. Dieses Feld kann so festgelegt werden, dass es automatisch aktualisiert wird, wenn die Tracking-Kontrollseite aktualisiert wird. |
| In Shop-Datum | Das früheste Datum, an dem die Waren aus den Einkaufsbestellungen, die mit der Fahrt verknüpft sind, zum Verkauf zur Verfügung stehen.|
| Vorkalkuliertes Lieferdatum | Normalerweise ist dies das Datum, an dem die Waren im Lagerort eintreffen sollen. Dieses Feld dient nur zu Informationszwecken. Es wird nicht zur Berechnung der Produktprogrammplanung auf den Zeilen der Einkaufsbestellung im Transportcontainer verwendet. Das erwartete Lieferdatum auf den Zeilen der Einkaufsbestellung wird durch die Verfolgungssteuerung aktualisiert. Dieses Feld kann so festgelegt werden, dass es aktualisiert wird, wenn die Tracking-Kontrollseite aktualisiert wird. |
| Abgangsdatum | Normalerweise das Datum, an dem das Flugzeug oder Schiff den Überseehafen tatsächlich verlässt. |
| ETA am Versandport. | Das geschätzte Ankunftsdatum im Zielhafen („An“ Hafen). |
| Ursprüngliche Belege empfangen | Optional: Aktualisieren Sie das Datum, an dem die Originaldokumente empfangen wurden. |
| Vom Broker empfohlen | Wahlweise: Aktualisieren Sie das Datum, an dem der Broker benachrichtigt wurde. |
| Gesendetes Original-Konnossement | Optional: Aktualisieren Sie das Datum, an dem das Originalkonnossement gesendet wurde. |
| Warenfreigabe | Wahlweise: Aktualisieren Sie das Datum, an dem die Waren freigegeben wurden. |
| Debitorentermin | Optional: Aktualisieren Sie das Datum des Termins beim Kunden. |
| Auslieferung am Lagerort | Optional: Aktualisieren Sie das Datum, an dem die Waren an den Lagerort geliefert wurden. |
| Überprüfungsdatum | Optional: Aktualisieren Sie das Datum der Überprüfung. |
| Lieferanweisungen | Optional: Aktualisieren Sie das Datum der Lieferanweisungen. |
| Von-Port | Der Hafen, von dem aus die Artikel verschickt werden. |
| Bis-Port | An Hafen, an den die Artikel verschickt werden sollen. |
| Lokale Weiterleitung | Dieses Feld dient nur zu Informationszwecken. Der lokale Spediteur sollte aus der Lieferantentabelle wählbar sein. |
| Datum des lokalen Transports | Geben Sie das Datum ein, für das der lokale Transport gebucht ist. Dieses Feld kann dem Lagerort bei seiner Planung helfen. |
| Uhrzeit des lokalen Transports | Geben Sie das Zeitfenster ein. Dieses Feld kann dem Lagerort bei seiner Planung helfen. |
| Reisevorlage | Die Fahrtenvorlage, die für die Fahrt angegeben wird. Die Route-Vorlage enthält die Details des „An“- und „Von“-Hafens sowie die Vorlaufzeiten, die mit der Tracking-Kontrolle des Transportcontainers verbunden sind. |

### <a name="settings-on-the-other-fasttab"></a>Einstellungen auf dem anderen Inforegister

Die folgende Tabelle beschreibt die Einstellungen, die auf der Inforegisterkarte **Andere** der Ansicht **Kopf** eines Transportcontainers verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Vermietung | Ein Wert, der angibt, ob der Transportcontainer ein Miet-Transportcontainer ist. Mit Mietcontainern können Kalkulationen verbunden sein. |
| In Vermietung konvertiert | Ein Wert, der angibt, ob der Transportcontainer in einen Mietversandcontainer umgewandelt wurde. Mit Mietcontainern können Kalkulationen verbunden sein. |
| Ursprüngliche Seereise | Wenn der Transportcontainer auf eine neue Fahrt gebracht wurde, die ursprüngliche Fahrt. |
| Verwendet | Verwenden Sie dies, um zu erfassen, ob ein Miet-Transportcontainer verwendet wurde. Es dient nur zu Informationszwecken. |
| Erwartetes Verladungsdatum | Das Datum, an dem der Transportcontainer voraussichtlich mit Waren geladen wird. |
| Unsere Seriennummer | Geben Sie die Seriennummer ein, die Ihre Firma intern für den Transportcontainer verwendet. |
| Seriennummer der Reederei | Geben Sie die Seriennummer ein, die die Firma oder der Agent der Reederei für den Transportcontainer vergeben hat. |
| Anwendungsdatum des Prüfungszertifikats | Das Datum, an dem eine Untersuchung für den Transportcontainer beantragt wurde. |
| Eingangsdatum des Prüfungszertifikats | Das Datum, an dem das Zertifikat für die Untersuchung erhalten wurde. |
| Ablaufdatum des Prüfungszertifikats | Das Datum, an dem das Zertifikat für die Untersuchung abläuft. |
| Prüfungszertifikatsnummer | Die Zertifikatsnummer des Zertifikats, das nach einer Untersuchung ausgestellt wurde. |

## <a name="lines-view"></a>Ansicht Zeilen

Um die Ansicht **Linien** zu öffnen, öffnen Sie einen Transportcontainer und wählen dann die Registerkarte **Linien** oben rechts in der Überschrift des Transportcontainers.

### <a name="information-on-the-shipping-container-fasttab"></a>Informationen zum Inforegister Transportcontainer

Die Inforegister-Registerkarte **Versandcontainer** in der Ansicht **Zeilen** zeigt Informationen über die Palette an. Die meisten dieser Informationen erscheinen auch in der Ansicht **Kopfzeile**, wie weiter oben in diesem Thema beschrieben.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Informationen und Schaltflächen auf dem Inforegister Zeilen

Das Inforegister **Zeilen** in der Ansicht **Zeilen** zeigt Details zu jeder vollen oder teilweisen Zeile der Einkaufsbestellung, die im aktuellen Transportcontainer enthalten ist.

Die folgende Tabelle beschreibt die Schaltflächen, die auf der Registerkarte **Zeilen** des Inforegisters in der Ansicht **Zeilen** verfügbar sind.

| Schaltfläche | Beschreibung |
|---|---|
| Entfernen | Entfernen Sie die ausgewählte Zeile der Einkaufsbestellung aus der Fahrt. |
| Bestand \>-Transaktionen | Zeigen Sie Bestandstransaktionen für die ausgewählte Zeile der Einkaufsbestellung an. Beachten Sie, dass bei Waren in Zustellung auch die ursprüngliche Bestellung und die Bestellungen von Waren in Zustellung angezeigt werden. |
| Bestand \> Dimensionen anzeigen | Öffnet ein Dialogfeld, in dem Sie die Bestandsdimensionen auswählen können, die für die angezeigten Transaktionen erscheinen. |
| Aktualisier. | Informationen aktualisieren, die sich auf den Zeilenbetrag, das Gewicht oder das Volumen der ausgewählten Zeile der Einkaufsbestellung beziehen. |

### <a name="information-on-the-lines-details-fasttab"></a>Informationen auf dem Inforegister Zeilen-Details

Das Inforegister **Zeilen-Details** in der Ansicht **Zeilen** zeigt Details zur Zeile der Einkaufsbestellung an, die gerade auf dem Inforegister **Zeilen** ausgewählt ist.
