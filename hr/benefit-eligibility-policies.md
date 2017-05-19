---
title: Vorteilsberechtigungsrichtlinien
description: "Dieser Artikel enthält Informationen zu Vorteilseberechtigungspolicen fest, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 076b4f14a09698b6a0e2f5f3dd4f74ef5b673a8d
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="benefit-eligibility-policies"></a>Vorteilsberechtigungsrichtlinien

[!include[banner](includes/banner.md)]


Dieses Themal enthält Informationen zu Vorteilseberechtigungspolicen, die Sie dabei unterstützen festzulegen, wer für bestimmte Vorteile berechtigt ist.

Wenn Sie Vorteile erstellen, müssen Sie entscheiden, welche Vorteile für welche Mitarbeiter zur Verfügung stehen. Die folgende Tabelle zeigt Beispiele für Vorteile, die Sie vielleicht bestimmten Mitarbeitern zugänglich machen möchten.

| Vorteil          | Vorteil ist verfügbar für |
|------------------|---------------------------------|
| Krankenversicherung | Alle Mitarbeiter                   |
| Mobiltelefon     | Verkaufspersonal, Führungskräfte         |
| Parkausweise   | Führungskräfte                      |

Die folgenden Komponenten werden verwendet, um Berechtigungsrichtlinien zu erstellen:

-   Richtlinienregeltypen
-   Vorteilsberechtigungsrichtlinien

Durch Richtlinienregeltypen werden die Abfrageparameter definiert, die beim Entwickeln bestimmter Richtlinienregeln verwendet werden. Wenn Sie Richtlinienregeltypen erstellt haben, können Sie Berechtigungsrichtlinien für Vorteile erstellen. Über die Richtlinien können Sie eine Regelsammlung erstellen, die für eine oder mehrere juristische Personen gilt. Innerhalb jeder Richtlinie können Sie jeden der eben erstellten Richtlinienregeltypen für die Vorteilsberechtigung anzeigen. 

Sie definieren den Umfang der Regel innerhalb der Richtlinie. Wenn Sie beispielsweise einen Richtlinienregeltyp für die Vorteilsberechtigung mit der Bezeichnung **Führungskraft** erstellen, können Sie die Regel innerhalb dieser Richtlinie definieren. Hier kann die Regel zum Beispiel angeben, dass jede Position, die das Wort "Führungskraft" enthält, in diese Regel einbezogen werden soll. Nachdem Sie die Parameter der in der Richtlinie enthaltenen Regel(n) definiert haben, können Sie dem Vorteil eine bestimmte Regel zuweisen.

<a name="see-also"></a>Siehe auch
--------

[Definieren und verwalten eines Vorteilprogramms](manage-benefit-program.md)




