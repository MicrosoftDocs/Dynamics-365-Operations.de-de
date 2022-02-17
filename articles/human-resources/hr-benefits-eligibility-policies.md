---
title: Vorteilsberechtigungsrichtlinien
description: Dieses Thema informiert über Richtlinien für die Leistungsberechtigung, die festlegen, wer für bestimmte Leistungen berechtigt ist.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e1f64a0beffe12f6b4e0ad53d3bbaa96822dc7e8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066042"
---
# <a name="benefit-eligibility-policies"></a>Vorteilsberechtigungsrichtlinien


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dieses Thema informiert über Richtlinien für die Leistungsberechtigung, die festlegen, wer für bestimmte Leistungen berechtigt ist.

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

Sie definieren den Umfang der Regel innerhalb der Richtlinie. Wenn Sie beispielsweise einen Richtlinienregeltyp für die Vorteilsberechtigung mit der Bezeichnung **Führungskraft** erstellen, können Sie die Regel innerhalb dieser Richtlinie definieren. Hier kann die Regel zum Beispiel angeben, dass jede Position, die das Wort Führungskraft enthält, in diese Regel einbezogen werden soll. Nachdem Sie die Parameter der in der Richtlinie enthaltenen Regel(n) definiert haben, können Sie dem Vorteil eine bestimmte Regel zuweisen.






[!INCLUDE[footer-include](../includes/footer-banner.md)]
