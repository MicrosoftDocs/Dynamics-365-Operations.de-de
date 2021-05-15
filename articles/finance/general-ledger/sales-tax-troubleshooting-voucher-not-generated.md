---
title: Beleg wird nicht generiert
description: Dieses Thema enthält Informationen zur Fehlerbehebung, die helfen können, wenn ein Beleg erzeugt werden sollte, aber nicht erzeugt wird.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947646"
---
# <a name="voucher-isnt-generated"></a>Beleg wird nicht generiert

[!include [banner](../includes/banner.md)]

Wenn ein Gutschein generiert werden soll, aber auf der Seite **Gutschein-Transaktionen** keine Gutscheine angezeigt werden, führen Sie die Schritte in den folgenden Abschnitten wie erforderlich aus, um dieses Problem zu beheben.

[![Seite „Belegtransaktionen, die keine Belege haben“](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Prüfen Sie die Anwendbarkeit der Steuer

1. Gehen Sie zu **Steuern** \> **Periodische Aufgaben** \> **Untergeordnete Sachkonten-Erfassungen, die noch nicht umgelagert wurden**.
2. Wenn ein Datensatz in der Erfassung vorhanden ist, wählen Sie ihn aus und wählen Sie dann **Jetzt übertragen**.

    [![Schaltfläche „Jetzt umlagern“ auf der Seite „Noch nicht umgelagerte Journaleinträge des untergeordneten Sachkontos“](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Öffnen Sie die Seite **Gutschein-Transaktionen** erneut, um zu sehen, ob der Gutschein erzeugt wurde.

## <a name="determine-whether-customization-exists"></a>Ermitteln Sie, ob eine Anpassung vorliegt

Wenn Sie die Schritte im vorherigen Abschnitt ausgeführt haben, aber kein Problem gefunden haben, stellen Sie fest, ob eine Anpassung vorhanden ist. Wenn keine Anpassung vorhanden ist, erstellen Sie eine Microsoft Service-Anfrage für weiteren Support.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
