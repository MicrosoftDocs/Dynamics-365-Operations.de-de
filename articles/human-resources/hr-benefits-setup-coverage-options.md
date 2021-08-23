---
title: Abdeckungsoptionen erstellen
description: Abdeckungsoptionen in Microsoft Dynamics 365 Human Resources sind Deckungsgrade für die Wahl eines Teilnehmers in einem Leistungsplan oder -programm.
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
ms.openlocfilehash: 447317d0e9cb23bea21dae448048d05a3d989c89df17e4b8ea836201c20aefff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741428"
---
# <a name="create-coverage-options"></a>Abdeckungsoptionen erstellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Die Deckungsoptionen bestimmen, wer versichert werden soll oder wie viel Deckung in einem Versicherungsplan verfügbar ist. Für einen medizinischen Plan könnten Sie beispielsweise eine **nur für Angestellte** Option, und **Angestellter + 1** Option und eine Option **Familie** haben. Für Lebensversicherungen bieten Sie möglicherweise Deckung für **1x Gehalt** oder **2x Gehalt**.

Nachdem die Optionen für die Leistungsdeckung definiert sind, können Sie diese wiederverwenden. Sie können eine Option einem oder mehreren Plänen zuordnen.

> [!IMPORTANT]
> Nachdem Sie die Abdeckungsoptionen definiert haben, hängen Sie die Abdeckungsoptionen an einen Vorteilsplantyp an. Der Plantyp wird dann einem Vorteilsplan oder ‑programm zugeordnet. Abdeckungsoptionen, die einem Plantyp zugeordnet sind, sind für alle Pläne verfügbar, die mit diesem Plantyp erstellt wurden.

## <a name="create-coverage-options"></a>Abdeckungsoptionen erstellen
1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Abdeckungsoptionen**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Abdeckungsoption** | Ein eindeutiger Name für die Abdeckungsoption. |
   | **Beschreibung** | Eine Beschreibung der Abdeckungsoption. |
   | **Abdeckungscode** | Abdeckungscodes weisen Mindest‑ und Höchstbeträge für jede berechtigten abgedeckten Personentyp zu. Ein Abdeckungscode gibt an, wer abgedeckt ist oder was die zulässige Abdeckungssumme für einen Plantyp ist. Sie können die Abdeckungssumme als Dollarbetrag oder als Prozentsatz ausdrücken. Beispiel:<ul><li>**MA+1** – Um qualifiziert zu sein, muss für den Mitarbeiter ein Unterhaltsberechtigter ausgewählt sein (wenn mehr als einer ausgewählt ist, sind sie nicht mehr qualifiziert).</li><li>**MA+Familie** – Um qualifiziert zu sein, müssen für den Mitarbeiter mindestens zwei Unterhaltsberechtigte ausgewählt werden.</li></ul> |
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
