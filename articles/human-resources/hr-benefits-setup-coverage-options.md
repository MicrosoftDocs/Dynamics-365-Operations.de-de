---
title: Abdeckungsoptionen erstellen
description: Abdeckungsoptionen in Microsoft Dynamics 365 Human Resources sind Deckungsgrade für die Wahl eines Teilnehmers in einem Leistungsplan oder -programm.
author: andreabichsel
ms.date: 04/06/2020
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
ms.openlocfilehash: d9f67a97ec57bade840e1035c6011b94427a77c4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055579"
---
# <a name="create-coverage-options"></a>Abdeckungsoptionen erstellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Abdeckungsoptionen in Microsoft Dynamics 365 Human Resources sind Deckungsgrade für die Wahl eines Teilnehmers in einem Leistungsplan oder -programm. Zu den Deckungsoptionen könnten beispielsweise gehören **Nur für Mitarbeiter** für einen medizinischen Plan oder **2x Gehalt** für eine Lebensversicherung. Nach der Definition können Sie die Optionen für die Leistungsdeckung wiederverwenden. Sie können eine Option einem oder mehreren Plänen zuordnen.

Nachdem Sie die Abdeckungsoptionen definiert haben, hängen Sie die Abdeckungsoptionen an einen Vorteilsplantyp an. Der Plantyp wird dann einem Vorteilsplan oder ‑programm zugeordnet. Abdeckungsoptionen, die einem Plantyp zugeordnet sind, sind für alle Pläne verfügbar, die mit diesem Plantyp erstellt wurden. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abdeckungsoptionen**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Abdeckungsoption** | Ein eindeutiger Name für die Abdeckungsoption. |
   | **Beschreibung** | Eine Beschreibung der Abdeckungsoption. |
   | **Abdeckungscode** | Abdeckungscodes weisen Mindest‑ und Höchstbeträge für jede berechtigten abgedeckten Personentyp zu. Ein Abdeckungscode gibt an, wer abgedeckt ist oder was die zulässige Abdeckungssumme für einen Plantyp ist. Sie können die Abdeckungssumme als Dollarbetrag oder als Prozentsatz ausdrücken. Beispiel:</br></br>- **MA+1** – Um qualifiziert zu sein, muss für den Mitarbeiter ein Unterhaltsberechtigter ausgewählt sein (wenn mehr als einer ausgewählt ist, sind sie nicht mehr qualifiziert).</br></br>- **MA+Familie** – Um qualifiziert zu sein, müssen für den Mitarbeiter mindestens zwei Unterhaltsberechtigte ausgewählt werden. |
   | **Maximale Anzahl** | Die Höchstzahl der Unterhaltsberechtigten. |
   | **Status** | Der Status der Abdeckungsoption. Wenn der Status der Abdeckungsoption auf „Inaktiv“ gesetzt ist, kann die Abdeckungsoption für die Plantypen nicht ausgewählt werden. |
   | **Prozentsatz** | Der Prozentbetrag. Dieses Feld ist nur aktiv, wenn im Feld „Abdeckungscode“ die Option „%% x Gehalt“ ausgewählt wurde. |
   | **Divisor** | Der Divisor, der für die Berechnung verwendet werden soll, wenn Sie den Abdeckungscode „%% x Gehalt“ auswählen. |
   | **Mindestprozentsatz** | Der minimale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen. |
   | **Maximaler Prozentsatz** | Der maximale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen. |

4. Fügen Sie unter **Berechtigungsoptionen für persönliche Kontakte** jeder Abdeckungsoption die entsprechende Berechtigungsoption für persönliche Kontakte hinzu.

5. Geben Sie unter **Self-Service** Werte für die folgenden Felder ein:

   | Feld | Beschreibung |
   | --- | --- |
   | **Mitarbeiterbeitragsbetrag zulassen** | Gibt an, ob Mitarbeiter den Beitragsbetrag für den Vorteils-Self-Service ändern dürfen, wenn sie Vorteile auswählen. Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Vorteilsplanparameter basierend auf dem Beitragsbetrag, den der Mitarbeiter beim Vorteils-Self-Service eingibt. |
   | **Mitarbeiterdeckungsbetrag zulassen** | Gibt an, ob Mitarbeiter den Abdeckungsbetrag für den Vorteils-Self-Service ändern dürfen, wenn sie Vorteile auswählen. Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Vorteilsplanparameter basierend auf dem Abdeckungsbetrag, den der Mitarbeiter beim Mitarbeiter-Self-Service eingibt. |

6. Wählen Sie **Speichern**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]