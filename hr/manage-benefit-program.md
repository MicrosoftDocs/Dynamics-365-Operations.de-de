---
title: Definieren und Verwalten von Vorteilsprogramm ein
description: "Die Personalverwaltung stellt eine Reihe von Tools bereit, die verwendet werden können, um Vorteile, Abzüge und die Vergütungspläne der Arbeitskräfte einzurichten und zu verwalten, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet. Dieser Artikel bietet Informationen dazu, wie Vorteile eingerichtet und verwaltet werden."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Definieren und Verwalten von Vorteilsprogramm ein

Die Personalverwaltung stellt eine Reihe von Tools bereit, die verwendet werden können, um Vorteile, Abzüge und die Vergütungspläne der Arbeitskräfte einzurichten und zu verwalten, die eine Organisation für seine Arbeitskräfte anbietet oder verarbeitet. Dieses Thema enthält Informationen dazu, wie von Vorteilen eines verwaltete eingerichtet.

<a name="benefit-setup"></a>Vorteilseinstellung
-------------

Damit eine Arbeitskraft für Vorteile registriert werden kann, müssen Sie die Elemente jedes Vorteils erstellen. Diese Elemente kombinieren ähnliche Vorteilspläne und definieren Standardeinstellungen, wie Rabattsätze und Buchhaltungsdetails. Viele dieser Einstellungen können angepasst werden, wenn Arbeitskräfte später für den Vorteil registriert werden. Für jeden Vorteilsplan kann eine Organisation mehrere Registrierungssoptionen anbieten, oder eine Arbeitskraft kann die Registrierung für den Plan erlassen. 

![Vorteilsprozeßfluss ([]. /media/benefit-process-flow1.png)]". /media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Vergütungselemente
Bevor Sie damit beginnen, Vorteile zu erstellen und Arbeitskräfte dafür zu registrieren, müssen Sie die Elemente definieren, die einen Vorteil ausmachen: den Typ, den Plan und die Optionen.

-   **Typ** – Eine Reihe von Plänen für einen speziellen Vorteil, wie z. B. "Gesundheitsleistungen" oder "freies Parken".
-   **Plan** – Eine bestimmter Vorteil, der von einem externen Anbieter bezogen wird.
-   **Option** – Die Dispositionsebenen, z. B. "nur Mitarbeiter" oder "Mitarbeiter und Ehepartner".

Für jeden Vorteilstyp, wie Augen- oder Zahnmedizin, kann eine Organisation den Arbeitskräften eine oder mehrere Pläne anbieten. Für jeden Plan kann die Organisation unterschiedliche Optionen anbieten. So können Arbeitskräfte z. B. Zusatzlebensversicherungsschutz zum einfachen, doppelten oder dreifachen jährlichen Gehalt kaufen. Jede Kombination eines Plans und der Optionen wird zu einem Vorteil, für den die Arbeitskräfte sich registrieren können. 

![Vorteilsabbildung( [] . /media/benefit-pic.png)]". /media/benefit-pic.png)

## <a name="eligibility"></a>Berechtigung
Viele Faktoren bestimmen die Eignung der Arbeitskraft für unterschiedliche Arten von Vorteil, die ein Arbeitgeber anbietet. Wenn Sie einen Vorteil in Microsoft Dynamics 365 für Arbeitsgänge erstellen, können Sie den Typ Eignung festlegen, die auf diesen Vorteil gilt. 

Sie können eines Vorteils Katalogs für alle Arbeitskräfte. Beispiel Angebotparken übergibt einige Unternehmen allen Mitarbeitern als sonstiger Vorteil. Wenn Sie diesen Vorteil erstellen, legen Sie die Berechtigung auf **Alle Arbeitskräfte sind berechtigt** fest. 

Für andere Vorteile wie Schmucke und Steuerabgaben, Eignung gilt nicht zu. Molke erstellen Sie diese Arten von Vergütung, setzen Sie auf Überbrückungseignungsprozess Eignung ** **. 

Schließlich kann Vorteilseignung regelbasiert sein. Beispielsweise ein Unternehmen bietet zwei Typen Lebensversicherungsvorteil Mitarbeitern anzeigen. Exekutivmitarbeiter sind für eine Lebenversicherung freigegeben, für alle anderen Vollzeitangestellten für die andere Lebenversicherung freigegeben sind. In Dynamics 365 für Arbeitsgänge, können Sie eine Vorteilsberechtigungsregel erstellen, und alle Exekutivangestellten eine weitere Regel zu suchen, alle anderen Vollzeitangestellten suchen und gelten dann diese Regeln auf den entsprechenden Vorteil anzeigen.

## <a name="enrollment"></a>Registrierung
Nachdem Sie die Vorteile erstellt haben, die Ihre Organisation anbietet und die Berechtigung festgelegt haben, können Sie die Arbeitskräfte für Vorteile registrieren. Sie können eine einzelne Arbeitskraft für Vorteile registrieren, oder Sie können in einen einzelnen Prozesses viele Arbeitskräfte für mindestens einen Vorteilen registrieren. 

Manchmal beendet eine Organisation das Angebot eines bestimmten Vorteils. In diesem Fall müssen Sie den Vorteil und die Arbeitskräfte aktualisieren, die registriert werden. Massenvorteilsablauf können Sie das Ablaufdatum eines Vorteils und der Arbeitskraftregistrierungen für diesen Vorteil gleichzeitig ändern. Sie können auch mehrere Arbeitskräfte auswählen, die für einen Vorteil registriert sind und das Enddatum der Disposition ändern. 

Ebenso können Sie mit der Massenvorteilserweiterung das Ablaufdatum eines Vorteils und der Arbeitskraftregistrierungen für diesen Vorteil verlängern, wenn Sie beschließen, einen Vorteil länger anzubieten, als ursprünglich geplant.

<a name="see-also"></a>Siehe auch
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


