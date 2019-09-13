---
title: Wartungsprognose
description: In diesem Thema wird die Wartungsprognose in Asset Management erläutert.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1a416bbb79be3f25998d3c0da8d231d0df808685
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875675"
---
# <a name="maintenance-forecasts"></a>Wartungsprognose

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Wenn Sie einen Arbeitsauftrag erstellen möchten, erstellen Sie Arbeitsauftragseinzelvorgänge mit zugehörigen Anlagen und Wartungsauftragstypen. Wenn Sie einen Wartungsauftragstyp auswählen, der Wartungsprognosen enthält, werden die Prognosen automatisch in den Arbeitsauftrag übernommen.

Sie könnenin einem Arbeitsauftrag Prognosezeile hinzufügen oder löschen. Das Einrichten eines Lebenszyklusstatus von Arbeitsaufträgen, des zugehörigen Projekttyps und der mit dem Projekttyp verbundenen Stufenregeln bestimmt, ob Sie Prognosepositionen hinzufügen oder bearbeiten können. 

1. Klicken Sie auf **Anlagenmanagement** > **Allgemein** > **Arbeitsaufträge** > **Alle Arbeitsaufträge** oder **Aktive Arbeitsaufträge**.

2. Wählen Sie den Arbeitsauftrag aus der liste aus und klicken Sie auf **Planung**. In **Arbeitsauftragswartungsprognose** werden Prognosepositionen des Wartungsauftragstyps, der im Arbeitsauftrageinzelvorgang ausgewählt wurde, angezeigt.


## <a name="add-hours-forecast-to-a-work-order"></a>Geplante Stunden einem Arbeitsauftrag hinzufügen

1. Wählen Sie den Arbeitsauftragseinzelvorgang aus, den Sie einer Prognose hinzufügen möchten.

2. Klicken Sie im Inforegister **Stunden** auf **Hinzufügen**, um eine neue Position zu erstellen.

3. Wählen Sie im Feld **Kategorie** eine Kategorie aus.

4. Fügen Sie die Anzahl der geplanten Stunden im Feld **Stunden** ein.

5. Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.


## <a name="add-items-forecast-to-a-work-order"></a>Artikelprognosen einem Arbeitsauftrag hinzufügen

Es gibt drei Möglichkeiten, Artikel zu einer Arbeitsauftrags-Wartungsprognose hinzuzufügen: Sie können Positionen für Artikel (Ersatzteile) anlegen, die nicht in der Ersatzteilliste oder Anlagenstückliste enthalten sind, Ersatzteile aus der Liste der genehmigten Ersatzteile auswählen und Artikel aus der Anlagenstückliste auswählen.

1. Wählen Sie den Arbeitsauftragseinzelvorgang aus, den Sie einer Prognose hinzufügen möchten.

2. Wählen Sie im Inforegister **Artikel** aus.

3. Klicken Sie auf **Hinzufügen**, um eine neue Position für das Ersatzteil zu erstellen, das nicht auf der Ersatzteilliste oder Anlagenstückliste ist.

4. Wählen Sie im Feld **Artikelnummer** einen Artikel aus.

5. Fügen Sie die Menge in das Feld **Verkaufsmenge** ein und wählen Sie eine Mengeneinheit im Feld **Einheit**.

6. Geben Sie in die entsprechenden Felder den Einstandspreis und die Währung ein und wählen Sie einen **Abrechnungscode** aus.

7. Wenn Sie die in den Artikelpositionen angezeigte Liste mit den Dimensionen ändern möchten, klicken Sie auf **Inventar** > **Dimensionen anzeigen**, wählen Sie die Dimensionen aus und wählen Sie „Ja“ über die Umschalttaste **Einstellungen speichern**.

8. Wenn Sie ein genehmigtes Ersatzteil zur Wartungsprognose hinzufügen möchten, klicken Sie auf **Ersatzteile hinzufügen**, wählen Sie das Ersatzteil aus, bearbeiten Sie ggf. die zugehörigen Informationen und klicken Sie auf **OK**.

9. Wenn Sie Anlagenstücklistenartikel zur Prognose hinzufügen möchten, klicken Sie auf **Stücklistenartikel hinzufügen**, wählen Sie den Artikel aus, bearbeiten Sie ggf. zugehörige Informationen und klicken Sie auf **OK**.

10. Klicken Sie auf **Artikelverwendungsort**, wenn Sie einen Überblick darüber erhalten möchten, wo der Artikel auf der ausgewählten Position im Asset Management in Bezug auf Anlagen, Standardwerte für Wartungsaufträge, Ersatzteile und Arbeitsaufträge verwendet wird. 



## <a name="add-expense-forecast-to-a-work-order"></a>Ausgabenprognosen einem Arbeitsauftrag hinzufügen

1. In diesem Thema wird erläutert, wie eine Ausgabenprognose einem Arbeitsauftrag hinzugefügt wird. Wählen Sie im linken Teil des Formulars den Arbeitsauftragseinzelvorgang aus, den Sie einer Prognose hinzufügen möchten.

2. Wählen Sie im Inforegister **Ausgaben** aus.

3. Klicken Sie zum Erstellen einer neuen Position auf **Hinzufügen**.

4. Wählen Sie im Feld **Kategorie** eine Kategorie aus.

5. Geben Sie im Feld **Menge** die Menge ein.

6. Fügen Sie Einstandspreis, Verkaufswährung und Verkaufspreis in die entsprechenden Felder ein.

7. Wählen Sie im Feld **Abrechnungscode** den Belastungstyp aus, der verwendet werden soll.

>[!NOTE]
>Auf dem Inforegister **Wartungsprognose – Summen** sehen Sie eine Übersicht über die Anzahl der auf jeder Registerkarte angelegten Positionen, für den ausgewählten Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag. Außerdem sehen Sie eine Summe der prognostizierten Arbeitsstunden für den Arbeitsauftragseinzelvorgang und für den Arbeitsauftrag.

![Abbildung 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>utomatische Aktualisierung von Arbeitsauftragsprognosen

Im Asset Management können Sie Änderungen an den Arbeitsauftragsprognosen für Stundenkosten, Artikelkosten und Ausgaben, die in anderen Modulen in Dynamics 365 for Finance and Operations aktualisiert wurden, automatisch aktualisieren. Auf diese Weise wird sichergestellt, dass in Ihren Arbeitsauftragsprognosen immer die aktuellen Einstandspreise verwendet werden. Es ist auch möglich, ähnliche Aktualisierungen für [Wartungsauftragstypprognosen](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md) vorzunehmen.

1. Klicken Sie auf **Anlagenverwaltungsparameter** > **Periodisch** > **Planung** > **Arbeitsauftragsplanung aktualisieren**.

2. Im Dropdown-Dialogfeld **Arbeitsauftragsplanung aktualisieren** können Sie bei Bedarf Auswahlmöglichkeiten für bestimmte Arbeitsaufträge oder Arbeitsauftragseinzelvorgänge hinzufügen. Klicken Sie auf **Filtern**, um diese Auswahl treffen.

3. Bei Bedarf können Sie die automatische Aktualisierung als Batchauftrag auf dem Inforegister **Im Hintergrund ausführen** einrichten.

4. Klicken Sie auf **OK**, um die Aktualisierung der Prognose zu starten.


![Abbildung 2](media/07-work-orders.png)

