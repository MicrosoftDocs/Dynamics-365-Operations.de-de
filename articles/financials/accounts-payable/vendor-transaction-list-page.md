---
title: Kreditorentransaktionslistenseite
description: "Dieses Thema enthält Informationen zur Kreditorentransaktionslistenseite für Microsoft Dynamics 365 for Finance and Operations."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: de-de
ms.lasthandoff: 08/31/2018

---

# <a name="vendor-transaction-list-page"></a>Kreditorentransaktionslistenseite

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Ausgleiche anzeigen

Die Registerkarte **Ansichts-Ausgleiche** im Aktivitätsbereich bietet schnellen Zugriff auf die Ausgleichshistorie und zu weiteren Informationen über die ganze Ausgleichsbuchung. Sie können zusätzliche Buchungen, die mit der ausgewählten Buchung zusammenhängen, mögliche auch anzeigen, da sie Bestandteil desselben Ausgleichs waren, oder es sind sie Zahlungen, die in derselben Zahlungserfassung erstellt wurden.

1. Wählen Sie **Kreditorenkonten \> Alle Kreditoren** aus.
2. Wählen Sie einen Kreditor aus, der Buchungen hat, und wählen Sie dann **Kreditor \> Buchungen** aus.
3. Wählen Sie eine Buchung aus, um diese genauer anzusehen.
4. Wählen Sie die Registerkarte **Ausgleiche anzeigen** im Aktivitätsbereich aus.

    Das Dialogfeld **Hiermit zeigen Sie Ausgleiche angezeigt** wird geöffnet und zeigt die ausgewählte Buchung und alle Dokumente an, die ausgeglichen werden. Dieses Dialogfeld zeigt die Ausgleichshistorieansicht, allerdings werden alle zugeordneten Dokumente einbezogen.

5. Sie können verschiedene Funktionen in diesem Formular ausführen. Wählen Sie den Bereich aus, und wählen Sie dann eine der folgenden Einstellungen ein:

   - **Buchhaltung anzeigen** - Den ausgewählten Beleg und alle damit in Verbindung stehenden Belege anzeigen Klicken Sie auf **Schließen**, um die Dialogfelder zu schließen.
   - **Exportieren** – Exportiert die ausgewählten Belege in Microsoft Excel.
   - **Zeigt zugehörige Zahlungen an** – Alle Zahlungserfassungsbuchungen, die in der Zahlungserfassung erstellt wurden, die dem ausgewählten Dokument zugeordnet sind, angezeigt. Darüber hinaus werden alle Ausgleiche, die zu den Zahlungen zugeordnet werden, angezeigt. Die Beschriftung dieses Menüs ändert auch zu**Ausgleiche anzeigen**. Wählen Sie **Ausgleiche anzeigen**, um nur die Buchungen anzuzeigen, die angezeigt wurden, als Sie zunächst das Dialogfeld **Ausgleiche anzeigen** geöffnet haben.
    - **Ausgleichen von Buchungen** – Dieses Menü wird angezeigt, wenn das ursprüngliche Dokument, das ausgewählt wurde, nicht vollständig ausgeglichen wurde. Wenn Sie diese Option auswählen, wird das Dialogfeld **Bankbuchungen** angezeigt, in dem Sie Buchungen für den Ausgleich auswählen können.
    - **Ausgleichen von Buchungen rückgängig machen** – Dieses Menü wird angezeigt, wenn das ursprüngliche Dokument, das ausgewählt wurde, vollständig ausgeglichen wurde. Wenn Sie es auswählen, wird das Dialogfeld **Ausgleiche rückgängig machen** angezeigt, in dem Sie die Ausgleiche rückgängig machen können, die für das Dokument ausgeführt wurden.

