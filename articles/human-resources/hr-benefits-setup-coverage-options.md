---
title: Abdeckungsoptionen erstellen
description: Dieser Artikel beschreibt die Deckungsoptionen in Microsoft Dynamics 365 Human Resources für die Wahl eines Teilnehmers in einem Leistungsplan oder Programm.
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
ms.openlocfilehash: 8569cabf72871396b9935a14a5637e5e645705fb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848223"
---
# <a name="create-coverage-options"></a>Abdeckungsoptionen erstellen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Die Deckungsoptionen bestimmen, wer versichert werden soll oder wie viel Deckung in einem Versicherungsplan verfügbar ist. Für einen medizinischen Plan könnten Sie z. B. eine Option **Nur Mitarbeiter**, eine Option **Mitarbeiter + 1** und eine Option **Familie** haben. Für Lebensversicherungen bieten Sie möglicherweise Deckung für **1x Gehalt** oder **2x Gehalt**.

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
   | **Status** | Der Status der Abdeckungsoption. Wenn der Status der Option "Abdeckung" auf **Inaktiv** festgelegt ist, kann die Option "Abdeckung" bei Planarten nicht ausgewählt werden. |
   | **Prozentsatz** | Der Prozentbetrag. Dieses Feld ist nur aktiv, wenn im Feld „Abdeckungscode“ die Option „%% x Gehalt“ ausgewählt wurde. |
   | **Divisor** | Der Divisor, der für die Berechnung verwendet werden soll, wenn Sie den Abdeckungscode „%% x Gehalt“ auswählen. |
   | **Mindestprozentsatz** | Der minimale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen. |
   | **Maximaler Prozentsatz** | Der maximale Prozentsatz, wenn Sie den Abdeckungscode „Prozent“ auswählen. |

4. Fügen Sie unter **Berechtigungsoptionen für persönliche Kontakte** jeder Abdeckungsoption die entsprechende Berechtigungsoption für persönliche Kontakte hinzu.

5. Geben Sie unter **Self-Service** Werte für die folgenden Felder ein:

   | Feld | Beschreibung |
   | --- | --- |
   | **Mitarbeiterbeitragsbetrag zulassen** | Legt fest, ob es den Mitarbeitern erlaubt sein soll, die Beitragshöhe im Self-Service für Leistungen zu ändern, wenn sie Leistungen auswählen. Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Parameter des Leistungsplans auf der Basis des Beitragsbetrags, den der Mitarbeiter im Self-Service für Leistungen eingibt. |
   | **Mitarbeiterdeckungsbetrag zulassen** | Gibt an, ob es Mitarbeitern erlaubt sein soll, den Deckungsbetrag im Self-Service für Leistungen zu ändern, wenn sie Leistungen auswählen. Wenn Sie dieses Kontrollkästchen aktivieren, berechnet das System die Vorteilsplanparameter basierend auf dem Abdeckungsbetrag, den der Mitarbeiter beim Mitarbeiter-Self-Service eingibt. |

6. Wählen Sie **Speichern**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
