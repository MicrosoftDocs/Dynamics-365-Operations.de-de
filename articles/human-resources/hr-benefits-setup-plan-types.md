---
title: Plantypen erstellen
description: Ein Plantyp in Microsoft Dynamics 365 Human Resources ist eine übergeordnete Gruppierung bestimmter Vorteilstypen. Jeder Plantyp verfügt über einen Plantypcode, der Regeln für den Plantyp festlegt.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d8db6900e6b697e988e2a7e9e31828b70e4ad0d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463911"
---
# <a name="create-plan-types"></a>Plantypen erstellen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ein Plantyp in Microsoft Dynamics 365 Human Resources ist eine übergeordnete Gruppierung bestimmter Vorteilstypen. Jeder Plantyp verfügt über einen Plantypcode, der Regeln für den Plantyp festlegt. Zum Beispiel würde der Plantyp „Leben – Basis“ den Plantypcode „Leben“ haben, da er eine Art von Lebensversicherung ist und den Regeln entsprechen muss, die für den Lebensplantypcode festgelegt wurden. Ein anderer Plantyp könnte „Leben – zusätzlich“ sein, ebenfalls mit dem Plantypcode „Leben“.

Jeder Plantyp gibt an, ob ein Mitarbeiter sich für einen oder mehrere Pläne dieses Typs registrieren kann. Zum Beispiel könnte sich ein Mitarbeiter vermutlich sowohl für die Policen „Leben – Basis“ als auch „Leben – zusätzlich“ des Plantyps „Leben“ registrieren. Ein Mitarbeiter darf sich vermutlich nur für eine Police vom Typ „Medizinisch“ registrieren.

Wenn ein Plantyp Kontakte umfasst, gibt der Plantyp an, ob Kontakte Begünstigte oder Unterhaltsberechtigte sind. Zum Beispiel würde ein Planty „Leben – Basis“ Begünstigte haben, während ein Plantyp „Medizinisch – Basis“ Unterhaltsberechtigte haben würde. In einigen Fällen hat ein Plan möglicherweise keine persönlichen Kontakte. Beispiel: ein flexibles Ausgabenkonto oder Parkgebühr.

Ein Plantyp kann Abdeckungsoptionen definieren. Die Abdeckungsoptionen werden im Formular „Abdeckungsoptionen“ definiert. Eine Abdeckungsoption kann die Höhe des Vorteils oder die Kontakte angeben, die für den Plantyp berechtigt sind. Wenn der Kontakttyp beispielsweise „Begünstigter“ ist, sollten in der Abdeckungsoption die Bedingungen festgelegt werden, die definieren, zum Erhalt welcher Vorteile der Begünstigte berechtigt ist. Wenn der Kontakttyp „Unterhaltsberechtigt“ ist, sollte die Abdeckungsoption die Beziehung zwischen dem Unterhaltsberechtigten und dem Mitarbeiter definieren. 

1. Wählen Sie im Arbeitsbereich **Vorteilsverwaltung** unter **Einstellung** die Option **Plantypen**.

2. Wählen Sie **Neu** aus.

3. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Typ des Plans** | Ein eindeutiger Name, der den Plantyp identifiziert. |
   | **Beschreibung** | Eine Beschreibung des Plantyps. |
   | **Code des Plantyps** | Wählen Sie einen Plantypcode aus der Dropdown-Liste mit den Werten aus. In der Liste der Plantypcodes werden alle Plantypen angezeigt, die in der aktuellen Version unterstützt werden. |
   | **Gleichzeitige Registrierung** | Gibt an, ob sich ein Mitarbeiter für mehrere Vorteilspläne desselben Plantyps oder nur einen Vorteilsplan pro Plantyp registrieren kann. |
   | **Kontaktart** | Gibt die Rolle des persönlichen Kontakts an. Die Werte sind: leer, Unterhaltsberechtigter und Begünstigter. Sie können das Feld **Kontaktart** leer lassen, wenn für den Plantyp kein Unterhaltsberechtigter oder Begünstigter erforderlich ist, basierend auf der Abdeckungsoption. |

4. Wählen Sie zum Konfigurieren von Lebensereignissen erst **Aktivitäten** und dann **Lebensereignisoptionen**. Geben Sie Werte für die folgenden Felder an:

   | Feld | Beschreibung |
   | --- | --- |
   | **Typ des Plans** | Der Plantyp, für den Lebensereignisoptionen konfiguriert werden sollen. |
   | **Kennung des Lebensereignistyps** | Die Kennungs des Lebensereignistyps. |
   | **Stornierung zulassen** | Gibt an, ob ein Mitarbeiter während des Lebensereignisses einen Vorteilsplan stornieren kann. |
   | **Abdeckungsoption ändern** | Gibt an, ob ein Mitarbeiter während des Lebensereignisses die Abdeckungsoptionen ändern kann. |
   | **In neuen Plan ändern** | Gibt an, ob ein Mitarbeiter während des Lebensereignisses Pläne ändern kann. |
   | **Plan automatisch stornieren** | Gibt an, ob der Plan während des Lebensereignisses automatisch storniert werden soll. |
   | **Berechtigungsprüfung automatisch erneut öffnen** | Gibt an, ob die Berechtigungsprüfung für die Vergütungsregistrierung während des Lebensereignisses automatisch erneut geöffnet werden soll. |
   | **Berichtsfenster** | Gibt das Berichtsfenster (in Tagen) des Lebensereignisses an. **Hinweis**: Wenn Sie keinen Betrag eingeben, geht das System davon aus, dass das Berichtsfenster null ist und verarbeitet das Lebensereignis nicht. |

5. Wählen Sie **Speichern**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]