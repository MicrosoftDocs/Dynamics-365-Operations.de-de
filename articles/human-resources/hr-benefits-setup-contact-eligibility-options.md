---
title: Berechtigungsoptionen für persönliche Kontakte konfigurieren
description: Konfigurieren Sie Berechtigungsoptionen für persönliche Kontakte in Microsoft Dynamics 365 Human Resources. Persönliche Kontakte können Begünstigte oder Unterhaltsberechtigte sein.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 071523e2a1e9de6f0ed2b77e4ad6802efb0073f7
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558248"
---
# <a name="configure-personal-contact-eligibility-options"></a>Berechtigungsoptionen für persönliche Kontakte konfigurieren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema erfahren Sie, wie Sie Typen für persönliche Kontakte für die Verwendung von Vorteilen in Microsoft Dynamics 365 Human Resources konfigurieren. Persönliche Ansprechpartner sind die Personen, die von Ihren Plänen abgedeckt werden (abhängige Objekte) oder die von Ihren Plänen profitieren (Begünstigte). Angehörige sind in der Regel Ehepartner oder Kinder. Begünstigte können Ehepartner, Kinder, Trusts oder Eltern sein.

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Berechtigungsoptionen für persönliche Kontakte**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Berechtigungsoption** | Ein eindeutiger Name oder Code der Berechtigungsoption zur Identifizierung der Berechtigungsoption. |
   | **Beschreibung** | Eine kurze Beschreibung der Berechtigungsoption. |
   | **Berechtigungscode für Kontakt** | Der Systemcode, der die persönliche Berechtigungsoption am besten beschreibt. Sie haben folgende Auswahlmöglichkeiten: <ul><li>Beziehung</li><li>Student</li><li>Überschüssige abhängige Person</li><li>Überaltertes, deaktiviertes abhängiges Objekt</li></ul> |
   | **Status** | Der Status der Berechtigungsoption. Wenn der Status für eine Berechtigungsoption auf inaktiv gesetzt ist, können Sie diese Berechtigungsoption für persönliche Kontakte nicht auswählen. |
   | **Beziehung** | Gibt die Beziehung zwischen dem persönlichen Kontakt und dem Mitarbeiter an. Dieses Feld ist nur aktiv, wenn der Kontaktberechtigungscode auf „Beziehung“ gesetzt ist. |
   | **Alter** | Das maximale Alter eines berechtigten persönlichen Kontakts für den Vorteilsplan. Dieses Feld ist nur aktiv, wenn Sie eine Beziehung auswählen. Dieses Alter wird mit dem berechneten Alter des persönlichen Kontakts verglichen. Das berechnete Alter ist: (Dispositionsdatum – Geburtsdatum des persönlichen Kontakts / 365). Diese Zahl ist immer eine ganze Zahl. |

4. Wählen Sie **Speichern**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
