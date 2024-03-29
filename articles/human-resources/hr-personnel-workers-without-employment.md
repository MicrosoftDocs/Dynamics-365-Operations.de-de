---
title: Arbeitskräfte ohne Beschäftigung
description: Arbeitskräfte, die nicht in der Zukunft, aktiv oder in der Vergangenheit bei Ihrer Organisation beschäftigt waren, erscheinen auf der Seite „Arbeitskräfte ohne Beschäftigung“.
author: twheeloc
ms.date: 11/03/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d3b2d5d470e780c708941fd3d08eae1a042b4c03
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689802"
---
# <a name="workers-without-employment"></a>Arbeitskräfte ohne Beschäftigung


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbeitskräfte, die keine zukünftige, aktive oder historische Beschäftigung bei Ihrer Organisation haben, erscheinen auf der Seite **Arbeiter ohne Beschäftigung**. Arbeitskräfte mit diesem Typ können erscheinen, wenn Sie Arbeitskräfte importieren, die keinen Beschäftigungsdatensatz haben, oder wenn Sie die Beschäftigung einer Arbeitskraft über **Arbeiter \> Beschäftigungshistorie löschen**.

Standardmäßig ist die Seite **Arbeitskraft ohne Beschäftigung** für die folgenden Rollen verfügbar:

- Personalassistent
- Personalmanager
- Personalbeschaffungsmitarbeiter
- Manager für Vergütung und Leistungen
- Gehaltsabrechnung Administrator
- Gehaltsabrechnung Manager
- Ausbildung Manager

In der Liste **Arbeiter ohne Beschäftigung** können Sie die aufgeführten Personen löschen. Standardmäßig ist diese Berechtigung der Rolle Human Resources Assistant zugewiesen. Sie können dieses Recht mit den folgenden Schritten an andere Rollen weitergeben:

1. Wählen Sie **Systemverwaltung** und dann **Sicherheitskonfiguration**.

2. Filtern Sie in der Registerkarte **Privilegien** die Liste der **Privilegien** nach **Arbeitskräfte pflegen**.

   [![Liste der Filterprivilegien.](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Wählen Sie in der Spalte **Verweise** **Menüpunkte anzeigen**.

4. In **Menüelemente anzeigen** wählen Sie **HcmWorkersWithoutEmployment**.

   [![Formular auswählen.](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Legen Sie die Berechtigung **Löschen** auf **Gewähren** fest.

6. Wählen Sie die Registerkarte **Unveröffentlichte Objekte** aus.

7. Wählen Sie **Alle veröffentlichen** aus.

   [![Änderungen veröffentlichen.](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
