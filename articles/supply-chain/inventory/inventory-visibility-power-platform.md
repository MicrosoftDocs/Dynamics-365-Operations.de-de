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
ms.openlocfilehash: 9886ddbf0b072283cffd73d4bfdc20835ccb3b7c
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762699"
---
# <a name="use-the-inventory-visibility-app"></a>Die Inventory Visibility-App verwenden

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Verwendung der Inventory Visibility App.

Inventory Visibility bietet eine modellbasierte App zur Visualisierung. Die App enthält drei Seiten: **Konfiguration**, **Betriebliche Sichtbarkeit** und **Inventarübersicht**. Sie hat die folgenden Funktionen:

- Es bietet eine Benutzeroberfläche (UI) für die Konfiguration des Lagerbestands und der Softreservierung.
- Es unterstützt Echtzeit-Abfragen des Lagerbestands für verschiedene Dimensionen-Kombinationen.
- Es bietet eine Benutzeroberfläche für die Buchung von Reservierungsanfragen.
- Es bietet eine Ansicht des Lagerbestands für Produkte zusammen mit allen Dimensionen.
- Es bietet eine Ansicht einer Liste des Lagerbestands für Produkte zusammen mit vordefinierten Dimensionen. Die verfügbare Listenansicht kann entweder eine vollständige Zusammenfassung oder ein vorab geladenes Ergebnis einer verfügbaren Abfrage sein.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie beginnen, installieren Sie das Bestandsanzeige-Add-In und richten es wie in [Bestandsanzeige installieren und einrichten](inventory-visibility-setup.md) beschrieben ein.

## <a name="open-and-authenticate-the-inventory-visibility-app"></a><a name="open-authenticate"></a>Öffnen und authentifizieren Sie die Bestandsanzeige-App

Gehen Sie wie folgt vor, um die Bestandsanzeige-App zu öffnen und zu authentifizieren.

1. Melden Sie sich bei Ihrer Power Apps-Umgebung an.
1. Die **Bestandsanzeige**-App öffnen.
1. Öffnen Sie die **Operative Sichtbarkeit** Seite aus dem linken Bereich.
1. Wählen Sie die Schaltfläche **Einstellungen** (Rad-Symbol) oben auf der Seite aus.
1. Geben Sie im Dialogfeld **Einstellungen** die **Client-ID**,**Mandanten-ID**, und **Client-Geheimnis** Werte ein, die Sie notiert haben, als Sie [Bestandsanzeige installiert und eingerichtet haben](inventory-visibility-setup.md).
1. Wählen Sie die **Aktualisieren** Schaltfläche neben dem Feld **Bearertoken** aus. Das System generiert basierend auf den von Ihnen eingegebenen Informationen ein neues Bearertoken.

    ![Einstellungen für die On-Hand-Abfrage.](media/inventory-visibility-query-settings.png "Einstellungen für die On-Hand-Abfrage")

1. Wenn Sie ein gültiges Bearertoken erhalten, schließen Sie das Dialogfeld. Der Bearertoken läuft nach einiger Zeit ab. Daher müssen Sie es gelegentlich aktualisieren, wenn Sie die Konfiguration aktualisieren, Daten bereitstellen oder Daten abfragen müssen.

## <a name="configure-the-inventory-visibility-app"></a><a name="configuration"></a>Konfigurieren Sie die Bestandsanzeige-App

Die Seite **Konfiguration** der Bestandsanzeige-App hilft Ihnen, die Konfiguration der allgemeinen Datenverwaltung und der Funktion festzulegen. Nach der Installation des Add-Ins enthält die Standardkonfiguration eine Standardeinrichtung von Microsoft Dynamics 365 Supply Chain Management (die Datenquelle `fno`). Sie können die Standardeinstellung überprüfen. Anschließend können Sie die Konfiguration basierend auf Ihren geschäftlichen Anforderungen und den Bestandsbuchungsanforderungen Ihres externen Systems ändern, um die Art und Weise zu standardisieren, in der Bestandsänderungen in den verschiedenen Systemen gebucht, organisiert und abgefragt werden können.

Ausführliche Informationen zur Konfiguration der Lösung finden Sie unter [Bestandsanzeige konfigurieren](inventory-visibility-configuration.md).

## <a name="operational-visibility"></a>Operative Sichtbarkeit

Die Seite **Betriebliche Sichtbarkeit** liefert die Ergebnisse einer Echtzeit-Abfrage des Lagerbestands, Reservierungsbuchung und Zuteilung basierend auf verschiedenen Dimensionskombinationen. Wenn die Funktion *OnHandReservation* [eingeschaltet](inventory-visibility-configuration.md) ist, können Sie auch Reservierungsanfragen von der Seite **Operative Sichtbarkeit** aus teilen.

### <a name="on-hand-query"></a>Lagerbestand-Abfrage

Die Registerkarte **Auf-Hand-Abfrage** der Seite **Operative Sichtbarkeit** lässt Sie den Lagerbestand in Echtzeit abfragen. Gehen Sie folgendermaßen vor, um eine Abfrage einzurichten und auszuführen.

1. Die **Bestandsanzeige**-App öffnen.
1. Öffnen Sie die **Operative Sichtbarkeit** Seite aus dem linken Bereich.
1. Auf der Registerkarte **Onhand-Abfrage** geben Sie die **Organisations-ID**, **Standort-ID**, und **Lagerort-ID** Werte ein, die Sie abfragen möchten.
1. Geben Sie im Feld **Produkt ID** eine oder mehrere Produkt-IDs ein, um eine genaue Übereinstimmung für Ihre Suchanfrage zu erhalten. Wenn Sie das Feld **Produkt ID** leer lassen, enthalten die Ergebnisse alle Produkte am angegebenen Standort und Standort.
1. Um ein detaillierteres Ergebnis zu erhalten (z. B. eine Ansicht nach Dimensionswerten wie Farbe und Größe), wählen Sie Gruppieren-nach-Dimensionen im Feld **Ergebnis gruppieren nach** aus.
1. Um Elemente zu finden, die einen bestimmten Dimensionswert haben (z. B. Farbe = Rot), wählen Sie die Dimension im Feld **Abmessungen filtern** aus und geben Sie dann einen Dimensionswert ein.
1. Wählen Sie **Abfrage**. Sie erhalten entweder eine Erfolgsmeldung (grün) oder eine Fehlermeldung (rot). Wenn die Abfrage fehlschlägt, überprüfen Sie Ihre Abfragekriterien und stellen Sie sicher, dass Ihr [Bearertoken](#open-authenticate) nicht abgelaufen ist.

Eine andere Möglichkeit, eine verfügbare Abfrage durchzuführen, besteht darin, direkte API-Anforderungen zu stellen. Sie können entweder `/api/environment/{environmentId}/onhand/indexquery` oder `/api/environment/{environmentId}/onhand` verwenden. Weitere Informationen finden Sie unter [Inventory Visibility öffentliche APIs](inventory-visibility-api.md).

### <a name="reservation-posting"></a>Reservierungsbuchung

Verwenden Sie die Registerkarte **Reservierungsbuchung** auf der Seite **Operative Sichtbarkeit**, um eine Reservierungsanfrage zu stellen. Bevor Sie eine Reservierungsanfrage buchen können, müssen Sie die Funktion *OnHandReservation* einschalten. Weitere Informationen zu dieser Funktion und wie Sie sie einschalten können, finden Sie unter [Reservierungen für Inventory Visibility](inventory-visibility-reservations.md).

> [!NOTE]
> Die Möglichkeit, eine Soft-Reservierung über die Benutzeroberfläche vorzunehmen, soll es Ihnen ermöglichen, die Funktion zu testen. Jede weiche Reservierungsanforderung sollte mit einer Transaktionsauftragszeilenänderung (Erstellung, Änderung, Löschung usw.) verknüpft sein. Daher empfehlen wir Ihnen, nur weiche Reservierungen vorzunehmen, die mit einer Backend-Bestellung verknüpft sind. Weitere Informationen finden Sie unter [Reservierungen in Inventory Visibility](inventory-visibility-reservations.md).

Befolgen Sie diese Schritte, um eine Anfrage für eine weiche Reservierung über die Benutzeroberfläche zu veröffentlichen.

1. Die **Bestandsanzeige**-App öffnen.
1. Öffnen Sie die **Operative Sichtbarkeit** Seite aus dem linken Bereich.
1. Legen Sie auf der **Reservierungsbuchung** Registerkarte im Feld **Menge** die Menge an, die Sie vorläufig reservieren möchten.
1. Löschen Sie das **Aktivieren Sie negatives Inventar, um Überverkäufe zu unterstützen** Kontrollkästchen, um zu verhindern, dass der Bestand überverkauft oder überreserviert wird.
1. Wählen Sie im Feld **Operator** die Datenquelle und das physikalische Maß aus, die für die vorläufig reservierte Menge gelten.
1. Geben Sie die **Organizations-ID**, **Standort-ID**, **Lagerort-ID**, und **Produkt-ID** Werte an, die Sie abfragen möchten.
1. Um ein genaueres Ergebnis zu erhalten, wählen Sie eine Datenquelle, Dimensionen und Dimensionswerte aus.

Eine andere Möglichkeit, eine weiche Reservierung zu posten, besteht darin, direkte API-Anfragen zu stellen. Verwenden Sie das Muster, das in [Ein Ereignis für Reservierungen erstellen](inventory-visibility-api.md#create-one-reservation-event) beschrieben ist. Wählen Sie dann **Posten**. Um die Details der Anfrageantwort zu sehen, wählen Sie **Details anzeigen** aus. Sie können auch den Wert `reservationId` aus den Antwortdetails abrufen.

### <a name="allocation"></a>Zuteilung

Informationen zum Verwalten von Zuordnungen über die Benutzeroberfläche und APIs finden Sie unter [Bestandsanzeige Bestandszuordnung](inventory-visibility-allocation.md).

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

## <a name="preload-a-streamlined-on-hand-query"></a><a name="preload-streamlined-onhand-query"></a>Vorladen einer rationalisierten Abfrage des Lagerbestands

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: Preview until further notice -->

Supply Chain Management speichert eine Vielzahl von Informationen über Ihren aktuellen Lagerbestand und stellt sie für eine Vielzahl von Zwecken zur Verfügung. Viele alltägliche Vorgänge und die Integration von Drittparteien erfordern jedoch nur eine kleine Teilmenge dieser Details, und die Abfrage des Systems für alle diese Details kann zu großen Datasets führen, deren Montage und Übertragung Zeit in Anspruch nimmt. Daher kann der Dienst Inventory Visibility periodisch einen optimierten Satz von Daten zum Lagerbestand abrufen und speichern, um diese optimierten Informationen kontinuierlich verfügbar zu machen. Die gespeicherten Details zum Lagerbestand werden anhand konfigurierbarer Geschäftskriterien gefiltert, um sicherzustellen, dass nur die wichtigsten Informationen enthalten sind. Da die gefilterten Lagerbestandslisten lokal im Inventory Visibility Dienst gespeichert sind und regelmäßig aktualisiert werden, unterstützen sie einen schnellen Zugriff, Datenexporte bei Bedarf und eine optimierte Integration mit externen Systemen.

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
