---
title: Intercompany-Bestellungen und -Aufträge in mehreren Unternehmen erstellen
description: In diesem Artikel wird erläutert, wie Sie Intercompany-Bestellungen oder -Aufträge in mehreren Unternehmen erstellen.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6dce419126d60199bc11d4bd3209185ad779e979
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873549"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Intercompany-Bestellungen und -Aufträge in mehreren Unternehmen erstellen

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management ist nicht auf die alleinige Verwaltung eines Produktionsunternehmens und mehrerer Vertriebsunternehmen beschränkt. Alle Unternehmen mit Intercompany-Einrichtung können sowohl Vertriebs- als auch Produktionsunternehmen sein.

Kann der gleiche Artikel von mehreren Unternehmen geliefert werden, können Sie frei wählen, bei wem Sie den Artikel einkaufen möchten, und Aktualisierungen werden auch dann verarbeitet, wenn ein Auftrag in mehrere Bestellungen umgewandelt wird.

In der gleichen Weise, wie Sie automatisch eine Intercompany-Bestellung anlegen, können Sie in Ihrem Unternehmen einen Originalauftrag erstellen und diesen von mehreren Intercompany-Lieferanten erfüllen lassen, indem Sie mehr als eine Intercompany-Bestellung anlegen. Microsoft Dynamics 365 Supply Chain Management erstellt dann automatisch Intercompany-Aufträge in den Lieferantenunternehmen.

Hierfür müssen alle Unternehmen als Handelsbeziehungen eingerichtet werden. Die Lieferantenunternehmen müssen in Microsoft Dynamics 365 Supply Chain Management als Intercompany-Kreditoren eingerichtet werden, und sie müssen der primäre Lieferant für den jeweiligen Artikel sein. Im Kundenauftrag unter **Kopfzeilenansicht** müssen Sie die Felder **Intercompany-Aufträge automatisch erstellen** und **Direktlieferung** im Inforegister **Intercompany-Einstellungen** auswählen. Dies ist die Standardeinstellung.

Auftragspositionen werden in der üblichen Weise erstellt. Beim Verlassen des Datensatzes wird eine Meldung angezeigt, die Sie darüber informiert, dass Intercompany-Bestellungen und Intercompany-Aufträge erstellt wurden. Diese Meldung enthält Verknüpfungen zu den neuen Aufträgen. Öffnen Sie zum Anzeigen der in den Lieferunternehmen erstellten Intercompany-Aufträge den Originalauftrag, und klicken Sie auf der Registerkarte **Allgemein** in der Gruppe **Zugehörige Informationen** auf **Referenzen**.

Wenn Sie die Intercompany-Bestellungen für die Kreditoren öffnen, fügt Microsoft Dynamics 365 Supply Chain Management automatisch die Nummer des Originalauftrags und die Nummer der Intercompany-Aufträge für jeden Kreditor ein.

Entsprechend fügt Microsoft Dynamics 365 Supply Chain Management automatisch die Nummer des Originalauftrags und die Nummer der Intercompany-Bestellungen für jeden Kreditor ein, wenn Sie die Intercompany-Aufträge für jeden Kreditor öffnen.

> [!NOTE]
> Wenn die bestellten Artikel bei einem Intercompany-Lieferanten verfügbar sind, bei den anderen jedoch nicht, erstellt Microsoft Dynamics 365 Supply Chain Management die Intercompany-Aufträge für das Lieferantenunternehmen, bei dem der Artikel verfügbar ist, stoppt jedoch die Auftragserstellung für das andere Unternehmen. In diesem Fall wird eine Benachrichtigungsmeldung angezeigt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
