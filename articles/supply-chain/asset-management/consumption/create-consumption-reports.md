---
title: Verbrauchsberichte erstellen
description: In diesem Artikel wird erläutert, wie Verbrauchsberichte in der Anlagenverwaltung erstellt werden.
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 136d6248db8012e5870e0627ddbd3703aa63703b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852899"
---
# <a name="create-consumption-reports"></a>Verbrauchsberichte erstellen

[!include [banner](../../includes/banner.md)]

 

Wenn Sie Verbrauchserfassungen für Arbeitsaufträge in der Anlagenverwaltung erstellt und gebucht haben, sind zwei Berichte für die Anzeige von Verbrauchsdetails verfügbar.


## <a name="asset-consumption-report"></a>Anlage – Verbrauchsbericht

Wenn Sie den Verbrauch für Arbeitsaufträge gebucht haben, können Sie einen Anlagenverbrauchsbericht drucken. Im Bericht werden die Stunden, Stundenkosten, Artikelkosten und Aufwendungen, die für Anlagen gebucht wurden, angezeigt.

1. Klicken Sie auf **Anlagenmanagement** > **Berichte** > **Anlagen** > **Anlagenverbrauch**.

2. Wählen Sie im Dialogfeld **Anlagenverbrauch** die Parameter und die Detailebene für die Anzeige aus, indem Sie **Ja** bei den relevanten Umschaltschaltflächen auswählen und eine funktionale Standortebene im Abschnitt **Anzeigen** einfügen.
    - Sie können das Feld **Ebenen** verwenden, um anzugeben, wie detailliert die Anlagenpositionen bezüglich der funktionalen Standorte sein sollen. 
    
        Wenn Sie beispielsweise die Zahl „1“ im Feld eingeben und eine funktionale Standortstruktur auf mehreren Ebenen haben, werden alle Anlagen für einen funktionalen Standort auf der höchsten Ebene angezeigt, und daher wird eine Position von den funktionalen Standorten auf einer niedrigeren Ebene hinzugefügt. 
        
        Wenn Sie die Zahl „0“ im Feld **Ebenen** eingeben, wird ein detailliertes Ergebnis mit allen Anlagen für alle funktionalen Standortebenen angezeigt, denen sie zugeordnet sind. 
        
    - Wählen Sie **Ja** bei der **Summe für alle Unteranlagen**-Umschaltschaltfläche aus, um Summen für jede Unteranlage im Bericht anzuzeigen.

3. Wählen Sie ein Datumsintervall im Abschnitt **Datumsangaben** aus.

4. Wählen Sie im Inforegister **Ziel** aus, ob Sie den Bericht auf dem Bildschirm anzeigen, ihn drucken oder als Datei oder E-Mail speichern möchten.

5. Bei Bedarf können Sie auswählen, dass bestimmte Anlagen im Bericht angezeigt werden. Klicken Sie im Inforegister **Einzuschließende Datensätze** auf **Filtern**, und fügen die Anlagen hinzu, die im Bericht enthalten sein sollen.

6. Klicken Sie auf **OK**, um den Bericht zu generieren.


## <a name="work-order-consumption-report"></a>Arbeitsauftrags-Verbrauchsbericht

Wenn Sie den Verbrauch für Arbeitsaufträge gebucht haben, können Sie einen Arbeitsauftrags-Verbrauchsbericht drucken. Im Bericht werden die Stunden, Stundenkosten, Artikelkosten und Aufwendungen, die für Arbeitsaufträge gebucht wurden, angezeigt.

1. Klicken Sie auf **Anlagenverwaltung** > **Berichte** > **Arbeitsaufträge** > **Arbeitsauftragsverbrauch**.

2. Wählen Sie im Dialogfeld **Arbeitsauftragsverbrauch** die Parameter aus, die im Bericht enthalten sein sollen, indem Sie **Ja** bei den relevanten Umschaltschaltflächen im Abschnitt **Anzeigen** auswählen.

3. Wählen Sie ein Datumsintervall im Abschnitt **Datumsangaben** aus.

4. Wählen Sie im Inforegister **Ziel** aus, ob Sie den Bericht auf dem Bildschirm anzeigen, ihn drucken oder als Datei oder E-Mail speichern möchten.

5. Bei Bedarf können Sie auswählen, dass bestimmte Arbeitsaufträge im Bericht angezeigt werden. Klicken Sie im Inforegister **Einzuschließende Datensätze** auf **Filtern**, und fügen die Arbeitsaufträge hinzu, die im Bericht enthalten sein sollen.

6. Klicken Sie auf **OK**, um den Bericht zu generieren.


>[!NOTE]
>Sie können auch einen [Arbeitsauftragsbericht](../work-orders/work-order-report.md) generieren, der zusätzliche Arbeitsauftragseinzelheiten enthält.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]