---
title: Inventory Visibility App
description: Dieser Artikel beschreibt die Verwendung der Inventory Visibility App.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: db158e3b6ae76f69149db04096f99d3dc4251146
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895756"
---
# <a name="use-the-inventory-visibility-app"></a>Die Inventory Visibility-App verwenden

[!include [banner](../includes/banner.md)]


Dieser Artikel beschreibt die Verwendung der Inventory Visibility App.

Inventory Visibility bietet eine modellbasierte App zur Visualisierung. Die App enthält drei Seiten: **Konfiguration**, **Betriebliche Sichtbarkeit** und **Inventarübersicht**. Sie hat die folgenden Funktionen:

- Es bietet eine Benutzeroberfläche (UI) für die Konfiguration des Lagerbestands und der Softreservierung.
- Es unterstützt Echtzeit-Abfragen des Lagerbestands für verschiedene Dimensionen-Kombinationen.
- Es bietet eine Benutzeroberfläche für die Buchung von Reservierungsanfragen.
- Es bietet eine angepasste Ansicht des Lagerbestands für Produkte zusammen mit allen Dimensionen.

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

Wenn Sie die Registerkarte **Bestandsabfrage** wählen, fordert das System Ihre Anmeldeinformationen an, um das Inhaber-Token zu erhalten, das für die Abfrage des Inventory Visibility-Dienstes erforderlich ist. Sie können das Inhaber-Token einfach in das Feld **BearerToken** einfügen und das Dialogfeld schließen. Sie können dann eine Anfrage für eine Lagerbestandsabfrage stellen.

Wenn das Inhaber-Token nicht gültig ist oder abgelaufen ist, müssen Sie ein neues in das Feld **BearerToken** einfügen. Geben Sie die richtigen Werte **Client ID**, **Mandanten ID**, **Client Secret** ein und wählen Sie dann **Aktualisiert**. Das System wird automatisch ein neues, gültiges Träger-Token erhalten.

Um eine Lagerbestand-Abfrage zu stellen, geben Sie die Abfrage in den Anfragekörper ein. Verwenden Sie das Muster, das in [Abfrage unter Verwendung der Post-Methode](inventory-visibility-api.md#query-with-post-method) beschrieben ist.

![Einstellungen für die On-Hand-Abfrage](media/inventory-visibility-query-settings.png "Einstellungen für die On-Hand-Abfrage")

### <a name="reservation-posting"></a>Reservierungsbuchung

Verwenden Sie die Registerkarte **Reservierungsbuchung**, um eine Reservierungsanfrage zu buchen. Bevor Sie eine Reservierungsanfrage buchen können, müssen Sie die Funktion *OnHandReservation* einschalten. Weitere Informationen zu dieser Funktion finden Sie unter [Inventory Visibility Reservierungen](inventory-visibility-reservations.md).

Um eine Reservierungsanfrage zu stellen, müssen Sie einen Wert in den Anfragekörper eingeben. Verwenden Sie das Muster, das in [Ein Ereignis für Reservierungen erstellen](inventory-visibility-api.md#create-one-reservation-event) beschrieben ist. Wählen Sie dann **Posten**. Um die Details der Anfrageantwort zu sehen, wählen Sie **Details anzeigen** aus. Sie können auch den Wert `reservationId` aus den Antwortdetails abrufen.

## <a name="inventory-summary"></a><a name="inventory-summary"></a>Bestandszusammenfassung

**Bestandsübersicht** ist eine angepasste Ansicht für die Entität *Inventory OnHand Sum*. Sie bietet eine Bestandszusammenfassung für Produkte zusammen mit allen Dimensionen. Die Bestandsübersicht wird regelmäßig von der Bestandsanzeige alle 15 Minuten synchronisiert. Bevor Sie auf der Registerkarte **Bestandsübersicht** Daten sehen können, müssen Sie die Funktion *OnHandMostSpecificBackgroundService* auf der Registerkarte **Funktionsverwaltung** aktivieren und **Konfiguration aktualisieren** auswählen

> [!NOTE]
> Die Funktion *OnHandMostSpecificBackgroundService* verfolgt nur Produktänderungen, die nach dem Aktivieren der Funktion aufgetreten sind. Daten für Produkte, die sich seit dem Aktivieren des Features nicht geändert haben, werden nicht aus dem Inventarservice-Cache mit der Dataverse-Umgebung synchronisiert. Wenn auf der Seite **Bestandszusammenfassung** nicht alle erwarteten Bestandsinformationen angezeigt werden, wechseln Sie zu **Bestandsverwaltung > Regelmäßige Aufgaben > Integration** der Bestandssichtbarkeit, deaktivieren Sie den Stapelverarbeitungsauftrag und aktivieren Sie ihn erneut. Dadurch wird der anfängliche Push ausgeführt, und alle Daten werden in den nächsten 15 Minuten mit der Entität *Lagerbestandssumme* synchronisiert. Wenn Sie diese Funktion verwenden möchten, empfehlen wir Ihnen, sie zu aktivieren, bevor Sie manuelle Änderungen vornehmen und den Batchauftrag **Integration der Bestandssichtbarkeit** aktivieren.

Mit der Option **Erweiterter Filter** von Dataverse können Sie eine persönliche Ansicht erstellen, die die Zeilen anzeigt, die für Sie wichtig sind. Mit den erweiterten Filteroptionen können Sie eine breite Palette von Ansichten erstellen, von einfach bis komplex. Sie lassen Sie auch gruppierte und verschachtelte Bedingungen zu den Filtern hinzufügen. Um mehr über die Verwendung von **Erweiterter Filter** zu erfahren, siehe [Bearbeiten oder Erstellen von persönlichen Ansichten mit erweiterten Raster-Filtern](/powerapps/user/grid-filters-advanced).

Im oberen Bereich der angepassten Ansicht stehen drei Felder zur Verfügung: **Standarddimension**, **Benutzerdefinierte Dimension** und **Messung**. Mit diesen Feldern können Sie steuern, welche Spalten sichtbar sind.

Sie können die Spaltenüberschrift auswählen, um das aktuelle Ergebnis zu filtern oder zu sortieren.

Der untere Teil der angepassten Ansicht zeigt Informationen wie "50 Datensätze (29 ausgewählt)" oder "50 Datensätze." Diese Informationen beziehen sich auf die aktuell geladenen Datensätze aus dem Ergebnis mit der Option **Erweiterter Filter**. Der Text "29 ausgewählt" bezieht sich auf die Anzahl der Datensätze, die mit Hilfe des Spaltenkopf-Filters für die geladenen Datensätze ausgewählt wurden.

Unten in der Ansicht befindet sich eine Schaltfläche **Mehr laden**, mit der Sie weitere Datensätze von Dataverse laden können. Die Standardanzahl der Datensätze, die geladen wird, ist 50. Wenn Sie **Mehr laden** wählen, werden die nächsten 1.000 verfügbaren Datensätze in die Ansicht geladen. Die Zahl auf der Schaltfläche **Mehr laden** zeigt die aktuell geladenen Datensätze und die Gesamtzahl der Datensätze für das Ergebnis mit der Option **Erweiterter Filter** an.

![Lagerzusammenfassung](media/inventory-visibility-onhand-list.png "Lagerzusammenfassung")
