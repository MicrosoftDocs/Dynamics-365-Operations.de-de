---
title: Produktionsauftragsstatus zurücksetzen
description: In diesem Artikel wird beschrieben, wie sie den Produktionsauftragsstatus zurücksetzen.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmStatusDecrease, ProdSetupStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d50cbcb4031d5c9f2c814883afd1fb38777d2ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903955"
---
# <a name="reverse-the-production-order-status"></a>Produktionsauftragsstatus zurücksetzen

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie sie den Produktionsauftragsstatus zurücksetzen. 

Wenn Sie den Status eines Produktionsauftrags zurücksetzen, werden der Auftrag und alle mit den Arbeitsplänen zusammenhängenden Arbeitsgänge auf einen vorherigen Schritt im Produktionslebenszyklus zurückgesetzt. Beispielsweise hat ein Produktionsauftrag den Status **Eingeplant**, und Sie ändern den Status wieder in **Erstellt**. In diesem Fall muss das System den Status zuerst auf  **Vorkalkuliert** ändern. Dies ist der Status, der **Eingeplant** unmittelbar vorangeht. Dadurch kann der Status in den gewünschten Status **Erstellt** geändert werden. **Hinweis:** Sie können auch einen Auftrag, der bereits den Status **Fertigmeldung** erreicht hat, auf einen einen früheren Status zurücksetzen. Sie müssen die Vorkalkulation und die Grob- oder Feinterminierung oder beides jedoch erneut ausführen, um die Informationen zum Auftrag zu aktualisieren. Dieser Schritt ist erforderlich, da Reservierungen des verbleibenden Verbrauchs von Artikeln und betrieblichen Ressourcen ebenfalls zurückgesetzt werden müssen. Im weiteren Verlauf des Artikels wird erklärt, was passiert, wenn Sie den Status eines Produktionsauftrags auf folgende Weise zurücksetzen:

-   Von **Vorkalkuliert** auf **Erstellt**
-   Von **Eingeplant** auf **Vorkalkuliert**
-   Von **Freigegeben** auf **Eingeplant**
-   Von **Gestartet** auf **Freigegeben**

## <a name="from-estimated-to-created"></a>Von "Vorkalkuliert" auf "Erstellt"
Wenn Sie den Status eines Produktionsauftrags von **Vorkalkuliert** auf **Erstellt** zurücksetzen, wird der Artikelbedarf, der für Artikel in der Stückliste (BOM) berechnet wurde, entfernt. Lagerbuchungen in der Produktionsposition werden gelöscht, und das Feld **Rückstandsstatus** der Stücklistenpositionen der Produktion wird auf **Abgeschlossen** zurückgesetzt. Alle zugrunde liegenden Bestellungen oder Produktionsaufträge werden gelöscht, wenn die Optionen **Abgeleitete Einkäufe** und **Abgeleiteter Produktionsauftrag** aktiviert werden. Wenn Sie die Kosten des Produktionsauftrags vorkalkuliert oder manuell Artikel für die Verwendung in der Produktion reserviert haben, werden diese Buchungen ebenfalls entfernt.

## <a name="from-scheduled-to-estimated"></a>Von "Eingeplant" auf "Vorkalkuliert"
Wenn Sie den Status eines Produktionsauftrags von **Eingeplant** auf **Vorkalkuliert** zurücksetzen, werden die geplanten Start- und Enddaten und -zeiten entfernt. Kapazitätsreservierungen, die im Rahmen der Planung vorgenommen wurden, werden entfernt, und Einzelvorgänge, die bei der Feinterminierung erstellt wurden, werden gelöscht. Alle Informationen, die über Grobterminierung und Feinterminierung auf der Seite **Produktionsauftragsdetails** erfasst werden, werden zurückgesetzt.

## <a name="from-released-to-scheduled"></a>Von "Freigegeben" auf "Eingeplant"
Wenn Sie den Status eines Produktionsauftrags von **Freigegeben** auf **Eingeplant** zurücksetzen, ändert sich lediglich der Wert im Feld "Status".

## <a name="from-started-to-released"></a>Von "Gestartet" auf "Freigegeben"
Wenn Sie den Status eines Produktionsauftrags von **Gestartet** auf **Freigegeben** zurücksetzen, werden alle Artikel, die als fertig gemeldet wurden, ebenfalls zurückgesetzt. Wenn Material entnommen wurde bzw. eingehende und ausgehende Lieferungen an die Produktion erfolgt sind, werden diese Einstellungen ebenfalls zurückgesetzt. Das Feld **Rückstandsstatus** in den Stücklistenpositionen des Produktionsauftrags ändert sich von **Abgeschlossen** in **Materialverbrauch**. Wenn Zeit erfasst wurde oder Mengen als für die Arbeitsgänge im Produktionsarbeitsplan fertig gemeldet wurden, werden diese Einstellungen zurückgesetzt. Das Feld **Rückstandsstatus** ändert sich von **Abgeschlossen** in **Arbeitsplanrückmeldung** im Produktionsarbeitsplan. Die Einstellungen für alle Artikel, die als in Bearbeitung oder als Ressource in Fertigung gebucht sind, werden ebenfalls zurückgesetzt. Auf der Seite **Produktionsauftragsdetails** werden Felder zurückgesetzt, die eine Menge anzeigen, die gestartet oder als fertig gemeldet wurde. Die Datumsangaben für diese Buchungen werden auch zurückgesetzt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]