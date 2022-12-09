---
title: Berechtigungsoptionen für persönliche Kontakte konfigurieren
description: Dieser Artikel erklärt, wie Sie die Berechtigungsoptionen für persönliche Kontakte in Microsoft Dynamics 365 Human Resources konfigurieren.
author: twheeloc
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803883"
---
# <a name="configure-personal-contact-eligibility-options"></a>Berechtigungsoptionen für persönliche Kontakte konfigurieren


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Artikel erfahren Sie, wie Sie Typen für persönliche Kontakte für die Verwendung von Vorteilen in Microsoft Dynamics 365 Human Resources konfigurieren. Persönliche Ansprechpartner sind die Personen, die von Ihren Plänen abgedeckt werden (abhängige Objekte) oder die von Ihren Plänen profitieren (Begünstigte). Angehörige sind in der Regel Ehepartner oder Kinder. Begünstigte können Ehepartner, Kinder, Trusts oder Eltern sein.

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
   | **Alter** |Gibt das maximale Alter eines berechtigten persönlichen Kontakts für den Vorteilsplan an. Dieses Feld ist nur aktiv, wenn Sie eine Beziehung auswählen. Dieses Alter wird mit dem berechneten Alter des persönlichen Kontakts verglichen. Das berechnete Alter ist: (Dispositionsdatum – Geburtsdatum des persönlichen Kontakts / 365). Diese Zahl ist immer eine ganze Zahl.
Bei der Option für die Berechtigung **volljähriger abhängiger privater Kontakte** ist das Alter in diesem Feld das Mindestalter. Beispiel: Wenn das Alter in der Option **Volljähriger abhängige Person** auf 18 festgelegt ist, werden die als abhängigen Personen von der Berechtigungsoption erfasst, die als volljährige abhängige Person gekennzeichnet und 18 Jahre oder älter sind.  |

4. Wählen Sie **Speichern** aus. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
