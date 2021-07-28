---
title: Arbeitskräfte ohne Beschäftigung
description: Arbeitskräfte, die nicht in der Zukunft, aktiv oder in der Vergangenheit bei Ihrer Organisation beschäftigt waren, erscheinen im Formular Arbeitskräfte ohne Beschäftigung.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71cb119e533e64b14badf65f55e8c4d5aa4c4b2f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356583"
---
# <a name="workers-without-employment"></a>Arbeitskräfte ohne Beschäftigung

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Arbeitskräfte, die keine zukünftige, aktive oder historische Beschäftigung bei Ihrer Organisation haben, erscheinen im Formular **Arbeiter ohne Beschäftigung**. Arbeitskräfte mit diesem Status können erscheinen, wenn Sie Arbeitskräfte ohne Datensatz importieren, oder wenn Sie die Beschäftigung einer Arbeitskraft über **Arbeiter > Beschäftigungshistorie** löschen.

Standardmäßig ist das Formular **Worker ohne Beschäftigung** für die folgenden Rollen verfügbar:

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