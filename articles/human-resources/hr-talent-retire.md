---
title: Ausscheiden von Dynamics 365 Talent - Attract und Onboard Apps
description: Dieser Artikel beschreibt die Außerbetriebnahme der Apps Dynamics 365 Talent - Attract und Onboard.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 3039b0a837335a777cdd6ff22b8b6e7c014ef956
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845083"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract und Onboard Apps Ausscheiden


Im Dezember 2019 haben wir angekündigt, dass die Apps Dynamics 365 Talent - Attract und Onboard am 1. Februar 2022 aus dem Verkehr gezogen werden, sodass unsere Debitor zwei Jahre Zeit haben, um zu planen.

Weitere Informationen über die Außerbetriebnahme dieser Apps finden Sie unter:
 - [Zurücksetzen von Dynamics 365 Talent - Attract und Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Mit Dynamics 365 Human Resources eine erfolgreichere Belegschaft aufbauen](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Wir werden auch weiterhin Dynamics 365 Human Resources unterstützen, damit unsere Debitor die Einblicke in die Belegschaft erhalten, die sie benötigen, um datengesteuerte Mitarbeitererlebnisse in verschiedenen Bereichen zu schaffen, wie z.B.:

- Vergütung
- Leistungen
- Beurlaubung und Abwesenheit
- Compliance
- Payroll
- Leistungsfeedback
- Schulung und Zertifizierung
- Self-Service-Programme

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent Apps Ausmusterung FAQ

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Wie sieht die Benutzererfahrung für die beiden Apps Dynamics 365 Talent - Attract und Onboard ab dem 1. Februar 2022 aus?

Die Benutzer können die Anwendungen nicht nutzen und werden auf eine Ausstiegsseite umgeleitet.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Können Debitor nach dem 1. Februar 2022 weiterhin Daten für die beiden Apps Dynamics 365 Talent - Attract und Onboard exportieren?
  
Nein, die Ausmusterung wurde im Dezember 2019 angekündigt und die erforderlichen Funktionalitäten für den Export wurden bis zum 1. Februar 2022 bereitgestellt. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Werden die Daten des Debitors, die sich auf die beiden Dynamics 365 Talent - Apps Attract und Onboard in Dataverse beziehen, nach dem 1. Februar 2022 gelöscht?

Nein, die Dataverse-Entitäten bleiben auch nach der Ausmusterung in der Microsoft Dataverse-Umgebung des Debitors, es sei denn, die Human Capital Management Talent-Lösung wird gelöscht oder deinstalliert.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Ich kenne den Namen der Umgebung von Talent. Wie kann ich die Attract- und Onboard-Daten in Dataverse sehen?

1.  Melden Sie sich bei Power Apps an: https://make.powerapps.com
2.  Wählen Sie die Umgebung, in der Sie die Attract- und Onboard-Daten sehen möchten.
3.  Gehen Sie zu **Dataverse >Tabellen**. 
4.  Geben Sie „msdyn_“ in **Suchen** ein. Wenn Sie die Liste der Tabellen sehen, die mit „msdyn_“ + Tabellennamen (Beispiel: msdyn_candidate), dann haben Sie die Umgebung mit Attract- und Onboard-Daten gefunden.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Ich kenne den Namen der Talent-Umgebung nicht. Wie kann ich die Umgebung mit den Daten für die Anwendungen Dynamics 365 Talent: Attract und Dynamics 365 Talent: Onboard finden?

1)  Melden Sie sich im Admin-Center Power Platform an: https://admin.powerplatform.microsoft.com/
2)  Wählen Sie **Umgebungen** aus.
3)  Wählen Sie eine bestimmte Umgebung zur Auswertung aus.
4)  Wählen Sie **Ressourcen > Dynamics 365 Apps**.
5)  Wenn Sie sehen, dass die **HCM Talent** Lösung installiert ist, sollten in dieser Umgebung Attract und Onboard Daten gespeichert sein. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> Die **HCM Talent** Lösung wird auch in Dynamics 365 Human Resources verwendet.
