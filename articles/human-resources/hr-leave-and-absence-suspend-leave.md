---
title: Beurlaubung aussetzen
description: Sie können in Dynamics 365 Human Resources eine Beurlaubung für einen Mitarbeiter aussetzen.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SuspendLeave, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9c8262fb34175f6f9326d6be82c922b2170fc5a7
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805259"
---
# <a name="suspend-leave"></a>Urlaub aussetzen

>[!Important]
>Die in diesem Artikel beschriebene Funktionalität ist derzeit für Kunden der eigenständigen Version von Dynamics 365 Human Resources verfügbar. Einige oder die gesamten Funktionen werden in einem zukünftigen Release der Finance-Infrastruktur nach Finance-Version 10.0.26 verfügbar sein.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können eine Beurlaubung für einen Mitarbeiter aussetzen, um zu verhindern, dass Urlaubsrückstellungen für ausgewählte Urlaubstypen verarbeitet werden.

## <a name="suspend-leave-and-absence-for-an-employee"></a>Abwesenheit und Urlaub für einen Mitarbeiter aussetzen

1. Wählen Sie im Datensatz des Mitarbeiters **Abweseneheit** aus.

2. Wählen Sie **Urlaub aussetzen**.

3. Wählen Sie **Neu** aus.

4. In dem Dialogfeld **Urlaubsrückstellung aussetzen** wählen Sie im Dialogfeld **Urlaub aussetzen** zusammen mit **Anfangsdatum** und **Endtermin**.

5. Optional können Sie einen **Kommentar** für die Aussetzung hinzufügen. 

Wenn Rückstellungen bearbeitet werden, während der Urlaub des Mitarbeiters ausgesetzt ist, werden keine Rückstellungen für die Arten des suspendierten Urlaubs gebildet.

> [!NOTE]
> Urlaubsanträge setzen Anträge auf arbeitsfreie Zeit aus. Anträge auf arbeitsfreie Zeit setzen jedoch keine Urlaubsanträge aus.

## <a name="see-also"></a>Siehe auch

- [Urlaubs- und Abwesenheitsübersicht](hr-leave-and-absence-overview.md)
- [Urlaubs- und Abwesenheitstypen konfigurieren](hr-leave-and-absence-types.md)
- [Urlaubs- und Abwesenheitspläne antizipieren](hr-leave-and-absence-accrue.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
