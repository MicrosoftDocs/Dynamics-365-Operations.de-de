---
title: Lohnintegrationsparameter
description: Dieses Thema beschreibt die Lohnintegrationsparameter in Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37d4dc52e7fe5ddd95f43d98267db819a275bd92
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069856"
---
# <a name="payroll-integration-parameters"></a>Lohnintegrationsparameter


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Vor der Verwendung der Dynamics 365 Human Resources-Lohnintegration müssen Sie die in diesem Thema beschriebenen Parameter einrichten.

## <a name="enable-payroll-address"></a>Lohnadresse aktivieren

Um die Lohnadresse verwenden zu können, müssen Sie diese im [Formular für gemeinsame Parameter](hr-setup-shared-parameters.md) auf der Registerkarte „Lohnintegration“ aktivieren.

## <a name="define-the-identification-type"></a>Kennungstyp festlegen

Um die Kennungstyp-ID in der [Entität „Mitarbeiter der Lohnbuchhaltung“](hr-admin-integration-payroll-api-payroll-employee.md) anzeigen zu lassen, müssen Sie [Personalverwaltungsparameter für jedes Unternehmen konfigurieren](hr-setup-shared-parameters.md).

1. Wählen Sie im Arbeitsbereich **Vergütungsverwaltung** unter Links die Option **Personalverwaltungsparameter** aus. 
2. Geben Sie auf der Registerkarte **Lohnintegration** den Wert der folgenden Felder ein.

| Feld | Beschreibung |
| --- | --- |
| Kennungstypen in der Lohnverarbeitung verwenden | Wenn diese Option ausgewählt ist, wird die ausgewählte Typ-ID in der Entität „Mitarbeiter der Lohnbuchhaltung“ angezeigt. |
| Kennungstyp | Der Identifikationstyp, der im Feld **mshr_payrollemployeeentityid** der [Entität „Mitarbeiter der Lohnbuchhaltung“](hr-admin-integration-payroll-api-payroll-employee.md) angezeigt werden soll. |

## <a name="see-also"></a>Siehe auch

[Einführung Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
