---
title: Bestätigen Sie die Zahlungspläne für Mietzahlungen in einem Batch
description: In diesem Thema wird erläutert, wie Sie mehrere Zahlungspläne in einem Batch bestätigen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9c680ea16e9f64107fde081c7e7763697356dcc1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971377"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a>Bestätigen Sie die Zahlungspläne für Mietzahlungen in einem Batch

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie mehrere Zahlungspläne in einem Batch bestätigen. Zahlungspläne werden entweder auf einer Mietvertrag-zu-Mietvertrag-Basis oder über den Bestätigungsstapelverarbeitungsvorgang bestätigt. Ein Journaleintrag kann nur für einen Mietvertrag gebucht werden, für den ein Zahlungsplan bestätigt wurde. Die Bestätigung des Zahlungsplans dient als endgültige Genehmigung der Finanzinformationen für den Mietvertrag. Alle zukünftigen Änderungen der Finanzinformationen für den Mietvertrag, wie z. B. Zahlungen und die Laufzeit des Mietvertrags, stellen eine Mietregulierung dar und sollten auf diese Weise verarbeitet werden.

Führen Sie die folgenden Schritte aus, um mehrere Zahlungspläne zu bestätigen.

1. Gehen Sie zu **Anlagenleasing \> Periodisch \> Bestätigungs-Batch**.
2. Auf der **Bestätigungs-Batch**-Seite wählen Sie **Bestätigungs-Batch** aus.
3. Filtern Sie im angezeigten Dialogfeld nach den Büchern, die Sie bestätigen möchten.

    - Um alle Bücher in einer bestimmten Leasinggruppe zu bestätigen, wählen Sie die Gruppe im **Leasinggruppe**-Feld aus.
    - Um bestimmte Bücher zu bestätigen, wählen Sie die Bücher im **Buch-ID**-Feld aus.
    - Um alle Bücher zu bestätigen, aktivieren Sie den **Für alle Bücher**-Parameter.

Informationen zu den neu bestätigten Büchern finden Sie auf der **Bestätigte Bücher**-Seite. Nachdem die Zahlungspläne bestätigt wurden, können die Journaleinträge der erstmaligen Erfassung für die Mietverträge gebucht werden.
