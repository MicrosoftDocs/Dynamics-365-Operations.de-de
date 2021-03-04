---
title: Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (15. November 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent – Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461275"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a>Neuerungen oder Änderungen in Dynamics 365 Talent – Core HR (15. November 2018)

**Build 8.1.2045**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="other-changesfixes"></a>Andere Änderungen/Korrekturen

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a>Aktuelle Position des Mitarbeiters kann nicht zu einer zukünftigen offenen Position geändert werden

Eine Änderung ist vorgenommen worden, um Positionsübertragungen zu ermöglichen, wenn die Position erst in der Zukunft verfügbar ist. 

### <a name="position-does-not-display-when-creating-a-new-employee"></a>Position wird nicht angezeigt, wenn ein neuer Mitarbeiter erstellt wird

Eine Änderung ist vorgenommen worden, um alle offenen Positionen anzuzeigen, die für die Zuweisung zur Verfügung stehen, wenn neue Mitarbeiter in Talent eingestellt werden. Hierzu zählen historische Positionen oder wenn die Positionen in die Zukunft vordatiert wurden. Positionen werden jetzt korrekt basierend auf dem Beschäftigungsstartdatum angezeigt. 

### <a name="termination-date-is-displaying-based-on-user-settings"></a>Kündigungsdatum wird basierend auf den Benutzereinstellungen angezeigt

Eine Änderung ist an der Liste früherer Mitarbeiter vorgenommen worden, um sämtliche Zeitzonenabweichungen für die bevorzugte Zeitzone der Mitarbeiter zu berücksichtigen, wenn das Kündigungsdatum angezeigt wird.

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a>Links für mir zugewiesene Arbeitsaufgaben zeigen nicht die richtigen Informationen an

Mit dieser Änderung wird die Navigation zu den Details der einzelnen Arbeitsaufgaben in der Liste die richtigen Informationen für die ausgewählte Aufgabe anzeigen. Dieses Problem ist nur bei erweiterten Sicherheitsoptionen aufgetreten.


## <a name="known-issue"></a>Bekannte Probleme

- **Abgang**: Wenn sie einer Arbeitskraft einen neuen Anhang hinzufügen, sind die Schaltflächen **Neu** und **Bearbeiten** ausgegraut. 
- **Problemumgehung:**, Bevor die Anhangseite geöffnet wird, stellen Sie sicher, dass die Infoboxen auf der Seite **Arbeitskraft** geschlossen sind. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]