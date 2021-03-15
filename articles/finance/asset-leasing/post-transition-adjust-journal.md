---
title: Journaleinträge für die Übergangsregulierung im Anlagenleasing
description: In diesem Thema werden die Funktionen beschrieben, mit denen Sie ein Leasingportfolio auf die neuen Leasing-Rechnungslegungsstandards, des Themas 842 zur Kodifizierung von Rechnungslegungsstandards(ASC 842) und den International Financial Reporting Standard 16 (IFRS 16) umstellen können.
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
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969552"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Journaleinträge für die Übergangsregulierung im Anlagenleasing

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, mit denen Sie ein Leasingportfolio auf die neuen Leasingbuchhaltungsstandards umstellen können: Thema 842 zur Kodifizierung von Rechnungslegungsstandards (ASC 842), der Standard in den allgemein anerkannten Rechnungslegungsgrundsätzen in den USA (US-GAAP), und International Financial Reporting Standard 16 (IFRS 16).

Informationen zum Einrichten eines Buches für den Übergang zu den neuen Standards finden Sie unter [Leasingbücher einrichten](set-up-lease-books.md).

Wenn Sie einen Journaleintrag für die Übergangsregulierung erstellen, wird ein Journaleintrag generiert. Dieser Eintrag spiegelt die Auswirkungen der Erfassung des Mietvertrags auf die Bilanzberichte nach den neuen Standards zu diesem Zeitpunkt wider. Das entsprechende Aktivkonto wird an diesem Tag mit dem Buchwert belastet, und das Passivkonto wird gutgeschrieben. Die Differenz wird entweder belastet oder den Gewinnrücklagen gutgeschrieben.

Führen Sie die folgenden Schritte aus, um eine Übergangsregulierung gemäß den neuen Rechnungslegungsstandards vorzunehmen.

1. Auf der **Mietvertragsübersicht**-Seite, wählen Sie den Mietvertrag und dann **Bücher**.
2. Wählen Sie im Buch **Zahlungsplan**.
3. In dem **Zahlungsplan**-Dialogfeld wählen Sie **Bestätigen**. Schließen Sie dann das Dialogfeld.
4. Wählen Sie **Übergangsregulierung**.

    > [!NOTE]
    > Eine Übergangsregulierung kann nur für Leasingbücher erstellt werden, die einem Buch zugeordnet sind, in dem das **Übergangsbuch**-Feld ist verfügbar. Wenn der Wert im **Mietbeginn**-Feld später als das Übergangsdatum liegt, wird der Wert im Feld **Übergangsregulierung** nicht aktualisiert.

5. Um den Journaleintrag anzuzeigen, wählen Sie **Anlagenleasingerfassungen** aus.
6. Wählen Sie die neuen Erfassung aus dann **Buchen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]