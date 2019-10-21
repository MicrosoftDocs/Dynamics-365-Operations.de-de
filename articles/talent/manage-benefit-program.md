---
title: Definieren und verwalten eines Vorteilprogramms
description: Die Personalverwaltung stellt eine Reihe von Tools bereit, die verwendet werden können, um Vorteile, Abzüge und die Vergütungspläne der Arbeitskräfte einzurichten und zu verwalten, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet. Dieser Artikel bietet Informationen dazu, wie Vorteile eingerichtet und verwaltet werden.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: a9a26450be97f655df8bc5983e4718341d40a2d6
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009899"
---
# <a name="define-and-manage-a-benefits-program"></a>Definieren und verwalten eines Vorteilprogramms

[!include [banner](includes/banner.md)]

Die Personalverwaltung stellt eine Reihe von Tools bereit, die verwendet werden können, um Vorteile, Abzüge und die Vergütungspläne der Arbeitskräfte einzurichten und zu verwalten, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet. Dieser Artikel bietet Informationen dazu, wie Vorteile eingerichtet und verwaltet werden.

<a name="benefit-setup"></a>Vorteile einrichten
-------------

Damit eine Arbeitskraft für Vorteile registriert werden kann, müssen Sie die Elemente jedes Vorteils erstellen. Diese Elemente kombinieren ähnliche Vorteilspläne und definieren Standardeinstellungen, wie Rabattsätze und Buchhaltungsdetails. Viele dieser Einstellungen können angepasst werden, wenn Arbeitskräfte später für den Vorteil registriert werden. Für jeden Vorteilsplan kann eine Organisation mehrere Registrierungssoptionen anbieten, oder eine Arbeitskraft kann die Registrierung für den Plan erlassen. 

[![Vorteilsprozessfluss](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Vergütungselemente

Bevor Sie damit beginnen, Vorteile zu erstellen und Arbeitskräfte dafür zu registrieren, müssen Sie die Elemente definieren, die einen Vorteil ausmachen: den Typ, den Plan und die Optionen.

-   **Typ** – Eine Reihe von Plänen für einen speziellen Vorteil, wie z. B. "Gesundheitsleistungen" oder "freies Parken".
-   **Plan** – Eine bestimmter Vorteil, der von einem externen Anbieter bezogen wird.
-   **Option** – Die Dispositionsebenen, z. B. "nur Mitarbeiter" oder "Mitarbeiter und Ehepartner".

Für jeden Vorteilstyp, wie Augen- oder Zahnmedizin, kann eine Organisation den Arbeitskräften eine oder mehrere Pläne anbieten. Für jeden Plan kann die Organisation unterschiedliche Optionen anbieten. So können Arbeitskräfte z. B. Zusatzlebensversicherungsschutz zum einfachen, doppelten oder dreifachen jährlichen Gehalt kaufen. Jede Kombination eines Plans und der Optionen wird zu einem Vorteil, für den die Arbeitskräfte sich registrieren können. 

[![Vergütungsplan](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Berechtigung
Viele Faktoren bestimmen die Eignung der Arbeitskraft für unterschiedliche Arten von Vorteil, die ein Arbeitgeber anbietet. Wenn Sie einen Vorteil in Dynamics 365 Talent erstellen, können Sie den Typ der Berechtigung festlegen, der für diesen Vorteil gilt. 

Sie können einen Vorteilskatalogs für alle Arbeitskräfte erstellen. Beispiel sind Parkausweise, die einige Unternehmen allen Mitarbeitern als sonstiger Vorteil bereitstellen. Wenn Sie diesen Vorteil erstellen, legen Sie die Berechtigung auf **Alle Arbeitskräfte sind berechtigt** fest. 

Für andere Vorteile wie Schmuck und Steuerabgaben, Eignung gilt nicht zu. Wenn Sie diese Arten von Vergütung erstellen, setzen Sie die Berechtigung auf **Berechtigungsprozess umgehen**. 

Schließlich kann Vorteilseignung regelbasiert sein. Beispielsweise ein Unternehmen bietet zwei Typen Lebensversicherungsvorteil Mitarbeitern anzeigen. Exekutivmitarbeiter sind für eine Lebenversicherung freigegeben, für alle anderen Vollzeitangestellten für die andere Lebenversicherung freigegeben sind. In Talent können Sie eine Vorteilsberechtigungsregel erstellen, um alle Exekutivmitarbeiter zu finden und eine Regel, um alle Vollzeitmitarbeiter zu finden. Sie können diese Regeln anschließend auf den entsprechenden Vorteil anwenden.

## <a name="enrollment"></a>Registrierung
Nachdem Sie die Vorteile erstellt haben, die Ihre Organisation anbietet und die Berechtigung festgelegt haben, können Sie die Arbeitskräfte für Vorteile registrieren. Sie können eine einzelne Arbeitskraft für Vorteile registrieren, oder Sie können in einen einzelnen Prozesses viele Arbeitskräfte für mindestens einen Vorteilen registrieren. 

Manchmal beendet eine Organisation das Angebot eines bestimmten Vorteils. In diesem Fall müssen Sie den Vorteil und die Arbeitskräfte aktualisieren, die registriert werden. Massenvorteilsablauf ermöglicht es Ihnen, das Ablaufdatum eines Vorteils und der Registrierung für die Arbeitskräfte zu ändern, die gleichzeitig für diesen Vorteil registriert sind. Sie können auch mehrere Arbeitskräfte auswählen, die für einen Vorteil registriert sind und das Enddatum der Disposition ändern. 

Ebenso können Sie mit der Massenvorteilserweiterung das Ablaufdatum eines Vorteils und der Arbeitskraftregistrierungen für diesen Vorteil verlängern, wenn Sie beschließen, einen Vorteil länger anzubieten, als ursprünglich geplant.

<a name="additional-resources"></a>Zusätzliche Ressourcen
--------

[Vergütungsberechtigungsrichtlinien](benefit-eligibility-policies.md)



