---
title: Übersicht über den Plantyp
description: Ein Plantyp in Microsoft Dynamics 365 Human Resources ist eine übergeordnete Gruppierung bestimmter Vorteilstypen.
author: twheeloc
ms.date: 08/24/2021
ms.topic: overview
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
ms.openlocfilehash: 87be947c829641ba809e6850ccf41ea6d142161d
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228959"
---
# <a name="plan-type-overview"></a>Übersicht über den Plantyp


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/preview-banner.md)]

Ein Plantyp ist eine übergeordnete Gruppierung bestimmter Vorteilstypen. Jeder Plantyp verfügt über einen Plantypcode, der Regeln für den Plantyp festlegt. Zum Beispiel würde der Plantyp **Leben – Basis** den Plantypcode **Leben** haben, da er eine Art von Lebensversicherung ist und den Regeln entsprechen muss, die für den **Lebens** plantypcode festgelegt wurden. Ein anderer Plantyp könnte **Zusätzliches Leben** sein. Dieser Plantyp hat auch den **Leben** Typenplancode.

Jeder Plantyp gibt an, ob ein Mitarbeiter sich für einen oder mehrere Pläne dieses Typs registrieren kann. Zum Beispiel könnte sich ein Mitarbeiter vermutlich sowohl für die Policen **Leben – Basis** als auch **Leben – zusätzlich** des Plantyps „Leben“ registrieren. Ein Mitarbeiter darf sich vermutlich nur für eine Police vom Typ „Medizinisch“ registrieren.

Wenn ein Plantyp Kontakte umfasst, gibt der Plantyp an, ob Kontakte Begünstigte oder Unterhaltsberechtigte sind. Zum Beispiel würde ein Plantyp **Leben – Basis** Begünstigte haben, während ein Plantyp „Medizinisch – Basis“ Unterhaltsberechtigte haben würde. In einigen Fällen hat ein Plan möglicherweise keine persönlichen Kontakte. Beispiel: ein flexibles Ausgabenkonto oder Parkgebühr.


Ein Plantyp kann Abdeckungsoptionen definieren. Die Deckungsoptionen werden auf der Seite **Deckungsoptionen** definiert. Eine Abdeckungsoption kann die Höhe des Vorteils oder die Kontakte angeben, die für den Plantyp berechtigt sind. Wenn der Kontakttyp beispielsweise **Begünstigter** ist, sollten in der Abdeckungsoption die Bedingungen festgelegt werden, die definieren, zum Erhalt welcher Vorteile der Begünstigte berechtigt ist. Wenn der Kontakttyp **Unterhaltsberechtigt** ist, sollte die Abdeckungsoption die Beziehung zwischen dem Unterhaltsberechtigten und dem Mitarbeiter definieren. 

> [!IMPORTANT]
> Die Seite **Plantypen** enthält Schlüsseldaten, die die Optionen beeinflussen, die beim Erstellen eines neuen Leistungsplans verfügbar sind:
>
> - **Plantypcode** – Dieses Feld beeinflusst, was auf der **Konfiguration** Registerkarte angezeigt wird, wenn der eigentliche Leistungsplan eingerichtet ist.  
> - **Gleichzeitige Registrierung** – Dieses Feld legt fest, ob Mehrfachregistrierungen zulässig sind. (Bei einem medizinischen Plan ist dieses Feld normalerweise auf **Eine Einschreibung** festegelegt.)
> - **Kontaktart** – Dieses Feld ermöglicht das Hinzufügen von Angehörigen oder Begünstigten zu einem Plan. Wenn es auf **Keiner** festgelegt ist, haben Mitarbeiter, die Leistungen in Anspruch nehmen, nicht die Möglichkeit, entweder einen Begünstigten oder einen Angehörigen auszuwählen.
> - **Deckungsoptionen** – Verwenden Sie dieses Feld, um die Deckungsoptionen mit den Planarten zu verknüpfen. Sie definiert entweder die Personen, die von dieser Planart abgedeckt werden, oder die Deckungssummen, die für diese Planart zur Verfügung stehen. Sie können beispielsweise festlegen, dass nur der Mitarbeiter, der Mitarbeiter und eine weitere Person oder der Mitarbeiter und seine Familie versichert sind.

## <a name="create-plan-types"></a>Plantypen erstellen

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
   | **Abdeckungsoption ändern** | Gibt an, ob ein Mitarbeiter während des Lebensereignisses die Abdeckungsoptionen ändern kann. |
   | **In neuen Plan ändern** | Gibt an, ob ein Mitarbeiter während des Lebensereignisses Pläne ändern kann. |
   | **Berechtigungsprüfung automatisch erneut öffnen** | Gibt an, ob die Berechtigungsprüfung für die Vergütungsregistrierung während des Lebensereignisses automatisch erneut geöffnet werden soll. |
   | **Lebensereignisregistrierungszeitraum** | Gibt das Berichtsfenster (in Tagen) des Lebensereignisses an. **Hinweis**: Wenn Sie keinen Betrag eingeben, geht das System davon aus, dass das Berichtsfenster null ist und verarbeitet das Lebensereignis nicht. |
   | **Kann nur von Administratoren bearbeitet werden** | Gibt an, ob Administratoren einen Plan während eines Lebensereignisses beenden oder bearbeiten können. Der Mitarbeiter kann im Arbeitsbereich **Mitarbeiter-Self-Service** keine Änderungen vornehmen. |
   | **Plan automatisch stornieren** | Gibt an, ob der Plan während eines Lebensereignisses automatisch storniert werden soll. Nachdem die Lebensereignisänderungen verarbeitet wurden, behält die Option **Plan automatisch beenden** die Planauswahl bei. Nur der Status **Bestätigt** oder **Ausgecheckt** wird entfernt. Der Plan bleibt ausgewählt. Daher verlieren Mitarbeiter, die während des Registrierungszeitraums für Lebensereignisse keine Planauswahl treffen, die Planauswahl nicht. 

5. Wählen Sie **Speichern** aus. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
