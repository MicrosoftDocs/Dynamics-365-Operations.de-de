---
title: Wartungsprognose
description: In diesem Thema wird die Wartungsprognose in Asset Management erläutert.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dd652af3100f8de59e06490443baeebca58a4dd3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838537"
---
# <a name="maintenance-forecasts"></a>Wartungsprognose

[!include [banner](../../includes/banner.md)]



Wenn Sie einen Arbeitsauftrag erstellen, erstellen Sie Arbeitsauftragseinzelvorgänge mit zugehörigen Anlagen und Wartungsauftragstypen. Wenn Sie einen Wartungsauftragstyp auswählen, der Wartungsprognosen enthält, werden die Prognosen automatisch in den Arbeitsauftrag übernommen.

Sie könnten Planungspositionen zu einem Arbeitsauftrag hinzufügen oder aus diesem löschen. Die Einrichtung des Arbeitsauftrags-Lebenszykluszustands, der zugehörige Projekttyp und die mit dem Projekttyp verbundenen Stufenregeln bestimmen, ob Sie Planungspositionen hinzufügen oder bearbeiten können. Weitere Informationen über Lebenszyklusstatus von Arbeitsaufträgen und zugehörigen Projektphasen finden Sie unter [Planungen, Arbeitsaufträge und Projekte](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Wählen Sie **Anlagenverwaltung** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge** aus.

2. Wählen Sie den Arbeitsauftrag in der Liste aus, und wählen Sie dann im Aktivitätsbereich > auf der Registerkarte **Arbeitsauftrag** > in der Gruppe **Projekt** **Planung** aus. Auf der Seite **Arbeitsauftragswartungsprognose** werden Planungspositionen des Wartungsauftragstyps, der im Arbeitsauftragseinzelvorgang ausgewählt wurde, angezeigt.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Geplante Stunden einem Arbeitsauftrag hinzufügen

1. Wählen Sie auf der Seite **Arbeitsauftrag – Wartungsprognose** einen Arbeitsauftragseinzelvorgang zum Hinzufügen einer Planung aus.

2. Wählen Sie im Inforegister **Stunden** **Hinzufügen** aus, um eine neue Position zu erstellen.

3. Wählen Sie im Feld **Kategorie** eine Kategorie aus.

4. Geben Sie die Anzahl der geplanten Stunden im Feld **Stunden** ein.

5. Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.


## <a name="add-an-items-forecast-to-a-work-order"></a>Artikelprognosen einem Arbeitsauftrag hinzufügen

Es gibt drei Möglichkeiten, einer Arbeitsauftragswartungsprognose Artikel hinzuzufügen. Sie können Positionen für Artikel (Ersatzteile) anlegen, die nicht in der Ersatzteilliste oder Anlagenstückliste enthalten sind, Ersatzteile aus der Liste der genehmigten Ersatzteile auswählen und Artikel aus der Anlagenstückliste auswählen.

- Wählen Sie auf der Seite **Arbeitsauftrag – Wartungsprognose** einen Arbeitsauftragseinzelvorgang zum Hinzufügen einer Planung aus.

- Fügen Sie auf dem Inforegister **Artikel** Artikel zur Wartungsprognose hinzu, indem Sie die geeignete Methode anwenden.

Befolgen Sie die folgenden Schritte, um eine Position für ein Ersatzteil zu erstellen, das nicht auf der Ersatzteilliste oder Anlagenstückliste ist.

1. Wählen Sie **Hinzufügen** aus.
2. Wählen Sie im Feld **Artikelnummer** den Artikel aus.
3. Geben Sie im Feld **Verkaufsmenge** die Menge ein.
4. Wählen Sie im Feld **Einheit** die Maßeinheit für die Menge aus.
5. Geben Sie in den Feldern **Einstandspreis** und **Währung** entsprechende Werte ein.
6. Wählen Sie im Feld **Abrechnungscode** einen Abrechnungscode aus.
7. Um die in den Artikelpositionen angezeigte Liste mit den Dimensionen zu ändern, wählen Sie **Inventar** > **Dimensionen anzeigen** aus, wählen Sie die Dimensionen aus und legen Sie dann die Option **Einstellungen speichern** auf **Ja** fest.

Um ein Ersatzteil aus einer genehmigten Ersatzteilliste hinzuzufügen, führen Sie die folgenden Schritte aus:

1. Wählen Sie **Ersatzteile hinzufügen** aus.
2. Wählen Sie das Ersatzteil aus, und bearbeiten Sie die zugehörigen Informationen nach Bedarf.
3. Wählen Sie **OK**.

Wenn Sie einen Artikel von der Anlagenstückliste hinzufügen möchten, führen Sie die folgenden Schritte aus:

1. Wählen Sie **Stücklistenartikel hinzufügen** aus.
2. Wählen Sie den Artikel aus, und bearbeiten Sie die zugehörigen Informationen nach Bedarf.
3. Wählen Sie **OK**.

Um einen Überblick darüber zu erhalten, wo der Artikel in der ausgewählten Position verwendet wird in Bezug auf Anlagen, Standardwerte für Wartungsauftragstypen, Ersatzteile und Arbeitsaufträge in Anlagenmanagement, wählen Sie die Option **Artikelverwendungsort** aus. Weitere Informationen über diesen Überblick finden Sie unter [Artikelverwendungsort](../controlling-and-reporting/item-where-used.md).


## <a name="add-an-expense-forecast-to-a-work-order"></a>Ausgabenprognosen einem Arbeitsauftrag hinzufügen

1. Wählen Sie auf der Seite **Arbeitsauftrag – Wartungsprognose** einen Arbeitsauftragseinzelvorgang zum Hinzufügen einer Planung aus.

2. Wählen Sie im Inforegister **Ausgaben** **Hinzufügen** aus, um eine Position zu erstellen.

3. Wählen Sie im Feld **Kategorie** eine Kategorie aus.

4. Geben Sie im Feld **Menge** die Menge ein.

5. Geben Sie in den Feldern **Einstandspreis**, **Verkaufswährung** und **Verkaufspreis** entsprechende Werte ein.

6. Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.

>[!NOTE]
>Auf dem Inforegister **Wartungsprognose – Summen** sehen Sie eine Übersicht über die Anzahl der auf jedem Inforegister angelegten Positionen, für den ausgewählten Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag. Außerdem sehen Sie eine Summe der prognostizierten Arbeitsstunden für den Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag.

Die folgende Abbildung zeigt ein Beispiel für die Seite **Arbeitsauftrag – Wartungsprognose**.

![Abbildung 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>utomatische Aktualisierung von Arbeitsauftragsprognosen

Im Anlagenmanagement können Sie Änderungen an den Arbeitsauftragsprognosen für Stundenkosten, Artikelkosten und Ausgaben, die in anderen Modulen in Microsoft Dynamics 365 for Finance and Operations aktualisiert wurden, automatisch aktualisieren. Auf diese Weise wird sichergestellt, dass in Ihren Arbeitsauftragsprognosen immer die aktuellen Einstandspreise verwendet werden. Es ist auch möglich, ähnliche Aktualisierungen für [Wartungsauftragstypprognosen](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) vorzunehmen.

1. Wählen Sie **Anlagenverwaltung** > **Periodisch** > **Planung** > **Arbeitsauftragsplanung aktualisieren** aus.

2. Im Dialogfeld **Arbeitsauftragsplanung aktualisieren** auf dem Inforegister **Einzuschließende Datensätze** können Sie bei Bedarf Auswahlmöglichkeiten für bestimmte Arbeitsaufträge oder Arbeitsauftragseinzelvorgänge hinzufügen. Klicken Sie auf **Filtern** und treffen Sie die zutreffende Auswahl.

3. Im Inforegister **Im Hintergrund ausführen** können Sie die automatische Aktualisierung bei Bedarf als Batchauftrag einrichten.

4. Klicken Sie auf **OK**, um die Aktualisierung der Prognose zu starten.


Die folgende Abbildung zeigt ein Beispiel für das Dialogfeld **Arbeitsauftragsplanung aktualisieren**.

![Abbildung 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]