---
title: Bestätigen Sie die Zahlungspläne für Mietzahlungen in einem Batch
description: In diesem Artikel wird erläutert, wie Sie mehrere Zahlungspläne in einem Batch bestätigen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymConfirmationDetails
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bd75e22f6407d6bc25a78c1dfeacf70022238e94
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895050"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Bestätigen Sie die Zahlungspläne für Mietzahlungen in einem Batch

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie mehrere Zahlungspläne in einem Batch bestätigen. Zahlungspläne werden entweder auf einer Mietvertrag-zu-Mietvertrag-Basis oder über den Bestätigungsstapelverarbeitungsvorgang bestätigt. Ein Journaleintrag kann nur für einen Mietvertrag gebucht werden, für den ein Zahlungsplan bestätigt wurde. Die Bestätigung des Zahlungsplans dient als endgültige Genehmigung der Finanzinformationen für den Mietvertrag. Alle zukünftigen Änderungen der Finanzinformationen für den Mietvertrag, wie z. B. Zahlungen und die Laufzeit des Mietvertrags, stellen eine Mietregulierung dar und sollten auf diese Weise verarbeitet werden.

Führen Sie die folgenden Schritte aus, um mehrere Zahlungspläne zu bestätigen.

1. Gehen Sie zu **Anlagenleasing \> Periodisch \> Bestätigungs-Batch**.
2. Auf der **Bestätigungs-Batch**-Seite wählen Sie **Bestätigungs-Batch** aus.
3. Filtern Sie im angezeigten Dialogfeld nach den Büchern, die Sie bestätigen möchten.

    - Um alle Bücher in einer bestimmten Leasinggruppe zu bestätigen, wählen Sie die Gruppe im **Leasinggruppe**-Feld aus.
    - Um bestimmte Bücher zu bestätigen, wählen Sie die Bücher im **Buch-ID**-Feld aus.
    - Um alle Bücher zu bestätigen, aktivieren Sie den **Für alle Bücher**-Parameter.

Informationen zu den neu bestätigten Büchern finden Sie auf der **Bestätigte Bücher**-Seite. Nachdem die Zahlungspläne bestätigt wurden, können die Journaleinträge der erstmaligen Erfassung für die Mietverträge gebucht werden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
