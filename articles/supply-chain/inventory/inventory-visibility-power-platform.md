---
title: Inventory Visibility App
description: Dieser Artikel beschreibt die Verwendung der Inventory Visibility App.
author: yufeihuang
ms.date: 09/15/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 674adb70cc4372a8c5ca8c75ed3ef840d8ec7b79
ms.sourcegitcommit: d2046cad5de570e6302a4390b41881a7ecb12e26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/15/2022
ms.locfileid: "9520863"
---
# <a name="use-the-inventory-visibility-app"></a>Die Inventory Visibility-App verwenden

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Verwendung der Inventory Visibility App.

Inventory Visibility bietet eine modellbasierte App zur Visualisierung. Die App enthält drei Seiten: **Konfiguration**, **Betriebliche Sichtbarkeit** und **Inventarübersicht**. Sie hat die folgenden Funktionen:

- Es bietet eine Benutzeroberfläche (UI) für die Konfiguration des Lagerbestands und der Softreservierung.
- Es unterstützt Echtzeit-Abfragen des Lagerbestands für verschiedene Dimensionen-Kombinationen.
- Es bietet eine Benutzeroberfläche für die Buchung von Reservierungsanfragen.
- Es bietet eine Ansicht des Lagerbestands für Produkte zusammen mit allen Dimensionen.
- Es bietet eine Ansicht einer Liste des Lagerbestands für Produkte zusammen mit vordefinierten Dimensionen.


## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, installieren Sie das Bestandsanzeige-Add-In und richten es wie in [Bestandsanzeige installieren und einrichten](inventory-visibility-setup.md) beschrieben ein.

## <a name="open-the-inventory-visibility-app"></a>Die Bestandsanzeige-App öffnen

Um die Bestandsanzeige-App zu öffnen, melden Sie sich bei Ihrer Power Apps-Umgebung an und öffnen die **Bestandsanzeige**.

## <a name="configuration"></a><a name="configuration"></a>Variante

Die Seite **Konfiguration** der Bestandsanzeige-App hilft Ihnen, die Konfiguration des Lagerbestands und der Softreservierung festzulegen. Nach der Installation des Add-Ins enthält die Standardkonfiguration eine Standardeinrichtung von Microsoft Dynamics 365 Supply Chain Management (die Datenquelle `fno`). Sie können die Standardeinstellung überprüfen. Anschließend können Sie die Konfiguration basierend auf Ihren geschäftlichen Anforderungen und den Bestandsbuchungsanforderungen Ihres externen Systems ändern, um die Art und Weise zu standardisieren, in der Bestandsänderungen in den verschiedenen Systemen gebucht, organisiert und abgefragt werden können.

Ausführliche Informationen zur Konfiguration der Lösung finden Sie unter [Bestandsanzeige konfigurieren](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Operative Sichtbarkeit

Die Seite **Betriebliche Sichtbarkeit** liefert die Ergebnisse einer Echtzeit-Abfrage des Lagerbestands, basierend auf verschiedenen Dimensionskombinationen. Wenn die Funktion *OnHandReservation* eingeschaltet ist, können Sie auch Reservierungsanfragen von der Seite **Operative Sichtbarkeit** aus stellen.

### <a name="on-hand-query"></a>Lagerbestand-Abfrage

Die Registerkarte **Auf-Hand-Abfrage** zeigt die Ergebnisse einer Echtzeit-Abfrage des Lagerbestands an.

Wenn Sie die Registerkarte **Bestandsabfrage** der Seite **Operative Sichtbarkeit** öffnen, fordert das System Ihre Anmeldeinformationen an, damit es das Inhaber-Token erhält, das für die Abfrage des Dienstes Inventory Visibility erforderlich ist. Sie können das Inhaber-Token einfach in das Feld **BearerToken** einfügen und das Dialogfeld schließen. Sie können dann eine Anfrage für eine Lagerbestandsabfrage stellen.

Wenn das Inhaber-Token nicht gültig ist oder abgelaufen ist, müssen Sie ein neues in das Feld **BearerToken** einfügen. Geben Sie die richtigen Werte **Client ID**, **Mandanten ID**, **Client Secret** ein und wählen Sie dann **Aktualisiert**. Das System wird automatisch ein neues, gültiges Träger-Token erhalten.

Um eine Lagerbestand-Abfrage zu stellen, geben Sie die Abfrage in den Anfragekörper ein. Verwenden Sie das Muster, das in [Abfrage unter Verwendung der Post-Methode](inventory-visibility-api.md#query-with-post-method) beschrieben ist.

![Einstellungen für die On-Hand-Abfrage](media/inventory-visibility-query-settings.png "Einstellungen für die On-Hand-Abfrage")

### <a name="reservation-posting"></a>Reservierungsbuchung

Verwenden Sie die Registerkarte **Reservierungsbuchung** auf der Seite **Operative Sichtbarkeit**, um eine Reservierungsanfrage zu stellen. Bevor Sie eine Reservierungsanfrage buchen können, müssen Sie die Funktion *OnHandReservation* einschalten. Weitere Informationen zu dieser Funktion und wie Sie sie einschalten können, finden Sie unter [Reservierungen für Inventory Visibility](inventory-visibility-reservations.md).

Um eine Reservierungsanfrage zu stellen, müssen Sie einen Wert in den Anfragekörper eingeben. Verwenden Sie das Muster, das in [Ein Ereignis für Reservierungen erstellen](inventory-visibility-api.md#create-one-reservation-event) beschrieben ist. Wählen Sie dann **Posten**. Um die Details der Anfrageantwort zu sehen, wählen Sie **Details anzeigen** aus. Sie können auch den Wert `reservationId` aus den Antwortdetails abrufen.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Bestandszusammenfassung

Die Seite **Bestandszusammenfassung** bietet eine Bestandszusammenfassung für Produkte zusammen mit allen Dimensionen. Es handelt sich um eine angepasste Ansicht für die Entität *Inventory OnHand Sum*. Die Bestandszusammenfassung wird regelmäßig von der Bestandstransparenz synchronisiert.

Um die Seite **Bestandszusammenfassung** zu aktivieren und die Synchronisierungshäufigkeit festzulegen, gehen Sie wie folgt vor:

1. Öffnen Sie die Seite **Konfiguration**.
1. Öffnen Sie die Registerkarte **Funktionsverwaltung und -einstellungen**.
1. Stellen Sie den Umschalter für die Funktion **OnHandMostSpecificBackgroundService** auf *Ja*.
1. Wenn die Funktion aktiviert ist, wird der Abschnitt **Dienstkonfiguration** verfügbar und enthält eine Zeile zum Konfigurieren der Funktion **OnHandMostSpecificBackgroundService**. Mit dieser Einstellung können Sie die Häufigkeit auswählen, mit der Bestandszusammenfassungsdaten synchronisiert werden. Verwenden Sie die **Hoch**- und **Runter**-Schaltflächen in der Spalte **Wert**, um die Zeit zwischen den Synchronisierungen zu ändern (die bis zu 5 Minuten betragen kann). Wählen Sie dann **Speichern** aus.

    ![Die Einstellung OnHandMostSpecificBackgroundService](media/inventory-visibility-ohms-freq.png "Die OnHandMostSpecificBackgroundService Einstellung")

1. Wählen Sie **Konfiguration aktualisieren**, um alle Änderungen zu speichern.


> [!NOTE]
> Die Funktion *OnHandMostSpecificBackgroundService* erfasst nur Änderungen im Lagerbestand, die nach dem Einschalten der Funktion aufgetreten sind. Daten für Produkte, die sich seit dem Aktivieren des Features nicht geändert haben, werden nicht aus dem Inventarservice-Cache mit der Dataverse-Umgebung synchronisiert. Wenn Ihre **Bestandsübersichtsseite** nicht alle von Ihnen erwarteten Bestandsinformationen anzeigt, öffnen Sie Supply Chain Management, gehen Sie zu **Bestandsverwaltung > Periodische Aufgaben > Inventory Visibility-Integration**, deaktivieren Sie den Chargen-Auftrag und aktivieren Sie ihn erneut. Dadurch wird der erste Push durchgeführt, und alle Daten werden in den nächsten 15 Minuten mit der Entität *Bestandssumme* synchronisiert. Wenn Sie die Funktion *OnHandMostSpecificBackgroundService* nutzen möchten, empfehlen wir Ihnen, sie zu aktivieren, bevor Sie Änderungen am Lagerbestand erstellen und den Chargeauftrag **Inventory Visibility-Integration** aktivieren.

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-the-inventory-visibility-onhand-query"></a>Vorladen einer rationalisierten Abfrage des Lagerbestands

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management speichert eine Vielzahl von Informationen über Ihren aktuellen Lagerbestand und stellt sie für eine Vielzahl von Zwecken zur Verfügung. Viele alltägliche Vorgänge und die Integration von Drittparteien erfordern jedoch nur eine kleine Teilmenge dieser Details, und die Abfrage des Systems für alle diese Details kann zu großen Datasets führen, deren Montage und Übertragung Zeit in Anspruch nimmt. Daher kann der Dienst Inventory Visibility periodisch einen optimierten Satz von Daten zum Lagerbestand abrufen und speichern, um diese optimierten Informationen kontinuierlich verfügbar zu machen. Die gespeicherten Details zum Lagerbestand werden anhand konfigurierbarer Geschäftskriterien gefiltert, um sicherzustellen, dass nur die wichtigsten Informationen enthalten sind. Da die gefilterten Lagerbestandslisten lokal im Inventory Visibility Dienst gespeichert sind und regelmäßig aktualisiert werden, unterstützen sie einen schnellen Zugriff, Datenexporte bei Bedarf und eine optimierte Integration mit externen Systemen.

> [!NOTE]
> Die aktuelle Vorschauversion dieser Funktion kann nur vorgeladene Ergebnisse liefern, die Standort und Ort enthalten. Es wird erwartet, dass Sie in der endgültigen Version der Funktion andere Dimensionen auswählen können, die mit den Ergebnissen vorgeladen werden sollen.

Die Seite **Zusammenfassung der Inventory Visibility vorladen** bietet eine Ansicht für die Entität *Ergebnisse der vorgeladenen Indexabfrage*. Im Gegensatz zur Entität *Bestandsübersicht* bietet die Entität *Bestandsindexabfrage Ergebnisse vorladen* eine Bestandsliste für Produkte zusammen mit ausgewählten Dimensionen. Inventory Visibility synchronisiert die vorgeladenen Zusammenfassungsdaten alle 15 Minuten.

Um die Daten auf der Registerkarte **Zusammenfassung der Inventory Visibility vorladen** anzuzeigen, müssen Sie die Funktion *OnHandIndexQueryPreloadBackgroundService* auf der Registerkarte **Funktionsverwaltung** der Seite **Konfiguration** aktivieren und dann **Konfiguration aktualisieren** wählen (siehe auch [Inventory Visibility konfigurieren](inventory-visibility-configuration.md)).

> [!NOTE]
> Wie bei der Funktion *OnhandMostSpecificBackgroudService* verfolgt die Funktion *OnHandIndexQueryPreloadBackgroundService* nur Änderungen im Lagerbestand, die aufgetreten sind, nachdem Sie die Funktion eingeschaltet haben. Daten für Produkte, die sich seit dem Aktivieren des Features nicht geändert haben, werden nicht aus dem Inventarservice-Cache mit der Dataverse-Umgebung synchronisiert. Wenn auf der Seite **Bestandszusammenfassung** nicht alle erwarteten Bestandsinformationen angezeigt werden, wechseln Sie zu **Lagerverwaltung > Regelmäßige Aufgaben > Integration** der Bestandssichtbarkeit, deaktivieren Sie den Stapelverarbeitungsauftrag und aktivieren Sie ihn erneut. Damit wird der erste Push durchgeführt und alle Daten werden in den nächsten 15 Minuten mit der Entität *On-Hand Index Query Preload Results* synchronisiert. Wenn Sie diese Funktion verwenden möchten, empfehlen wir Ihnen, sie zu aktivieren, bevor Sie manuelle Änderungen vornehmen und den Batchauftrag **Integration der Bestandssichtbarkeit** aktivieren.

## <a name="filter-and-browse-the-inventory-summaries"></a><a name="additional-tip-for-viewing-data"></a>Filtern und durchsuchen Sie die Zusammenfassungen des Bestands

Mit der Option **Erweiterter Filter** von Dataverse können Sie eine persönliche Ansicht erstellen, die die Zeilen anzeigt, die für Sie wichtig sind. Mit den erweiterten Filteroptionen können Sie eine breite Palette von Ansichten erstellen, von einfach bis komplex. Sie lassen Sie auch gruppierte und verschachtelte Bedingungen zu den Filtern hinzufügen. Mehr über die Verwendung des erweiterten Filters erfahren Sie unter [Bearbeiten oder erstellen Sie persönliche Ansichten mit erweiterten Rasterfiltern](/powerapps/user/grid-filters-advanced).

Die Seite **Bestandsübersicht** bietet oberhalb des Rasters drei Felder (**Standarddimension**, **Benutzerdefinierte Dimension** und **Messung**), mit denen Sie steuern können, welche Spalten sichtbar sind. Sie können auch eine beliebige Spaltenüberschrift auswählen, um das aktuelle Ergebnis nach dieser Spalte zu filtern oder zu sortieren. Der folgende Screenshot verdeutlicht die Dimensionen, die Filterung, die Anzahl der Ergebnisse und die Felder „Mehr laden“, die auf der Seite **Bestandsübersicht** verfügbar sind.

![Die Seite Bestandsübersicht.](media/inventory-visibility-onhand-list.png "Die Seite Bestandsübersicht")

Da Sie die Dimensionen, die für das Laden der Zusammenfassungsdaten verwendet werden, im Voraus definiert haben, werden auf der Seite **Vorladen der Inventory Visibility Zusammenfassung** dimensionsbezogene Spalten angezeigt. *Die Dimensionen sind nicht anpassbar&mdash;das System unterstützt nur Standort- und Ortsdimensionen für vorgeladene Lagerbestände.* Die Seite **Zusammenfassung der Inventory Visibility vorladen** bietet Filter, die denen auf der Seite **Zusammenfassung des Bestands** ähneln, außer dass die Dimensionen bereits ausgewählt sind. Der folgende Screenshot zeigt die Filterfelder, die auf der Seite **Zusammenfassung der Inventory Visibility vorladen** verfügbar sind.

![Die Seite Zusammenfassung der Inventory Visibility vorladen.](media/inventory-visibility-preload-onhand-list.png "Die Übersichtsseite „Inventory Visibility“ vorladen")

Am unteren Rand der Seiten **Zusammenfassung der Inventory Visibility vorladen** und **Zusammenfassung des Bestands** finden Sie Informationen wie „50 Datensätze (29 ausgewählt)“ oder „50 Datensätze“. Diese Informationen beziehen sich auf die aktuell geladenen Datensätze aus dem Ergebnis mit der Option **Erweiterter Filter**. Der Text "29 ausgewählt" bezieht sich auf die Anzahl der Datensätze, die mit Hilfe des Spaltenkopf-Filters für die geladenen Datensätze ausgewählt wurden. Es gibt auch eine Schaltfläche **Weitere laden**, mit der Sie weitere Datensätze von Dataverse laden können. Die Standardanzahl der geladenen Datensätze ist 50. Wenn Sie **Mehr laden** wählen, werden die nächsten 1.000 verfügbaren Datensätze in die Ansicht geladen. Die Zahl auf der Schaltfläche **Mehr laden** zeigt die aktuell geladenen Datensätze und die Gesamtzahl der Datensätze für das Ergebnis mit der Option **Erweiterter Filter** an.
