---
title: Berechtigungsoptionen für persönliche Kontakte konfigurieren
description: Dieser Artikel erklärt, wie Sie die Berechtigungsoptionen für persönliche Kontakte in Microsoft Dynamics 365 Human Resources konfigurieren.
author: twheeloc
ms.date: 08/24/2021
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
ms.openlocfilehash: 82bb7c037b4e0ab9950ce4c314c03a0f2d713bbd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895930"
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
   | **Alter** | Das maximale Alter eines berechtigten persönlichen Kontakts für den Vorteilsplan. Dieses Feld ist nur aktiv, wenn Sie eine Beziehung auswählen. Dieses Alter wird mit dem berechneten Alter des persönlichen Kontakts verglichen. Das berechnete Alter ist: (Dispositionsdatum – Geburtsdatum des persönlichen Kontakts / 365). Diese Zahl ist immer eine ganze Zahl. |

4. Wählen Sie **Speichern**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
