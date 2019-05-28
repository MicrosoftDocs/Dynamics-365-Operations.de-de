---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (27. November 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 11/27/2018
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
ms.search.validFrom: 2018-11-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 81ea0e4f4878d1967234c597504071ce464a22c5
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518102"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-november-27-2018"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (27. November 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2064**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.


## <a name="changes"></a>Änderungen

### <a name="unable-to-create-a-note-in-case-management"></a>Erstellen einer Notiz in Anfrageverwaltung nicht möglich

Eine Änderung ist für ein Problem vorgenommen worden, das beim Versuch auftritt, eine Notiz im Anfrageprotokoll der Anfrageverwaltung zu bearbeiten oder zu erstellen.

### <a name="misspelled-word-on-the-analytics-tab-in-the-compensation-workspace"></a>Falsch geschriebenes Wort auf der Analyseregisterkarte im Kompensationsarbeitsbereich 

Eine Änderung ist vorgenommen wurden, um die Rechtschreibung von „Nationalität” im Kompensationsanalysediagramm im Kompensationsarbeitsbereich zu korrigieren.

### <a name="employee-self-service-workspace-not-displaying-when-a-user-isnt-assigned-to-a-worker"></a>Mitarbeiter-Self-Service-Arbeitsbereich wird nicht angezeigt, wenn ein Benutzer keiner Arbeitskraft zugewiesen wurde 

Eine Änderung ist vorgenommen worden, wenn der Arbeitsbereich **Mitarbeiter-Self-Service** als Anfangsseite beim Start für einen Benutzer ausgewählt ist, dem keine Arbeitskraft zugewiesen ist. In diesem Fall wird das Standarddashboard angezeigt.

### <a name="leave-and-absence-error-object-reference-not-set-to-an-instance-of-an-object"></a>Urlaubs- und Abwesenheitsfehler: Objektverweis ist nicht auf eine Instanz eines Objekts festgelegt worden

Änderungen sind bei Urlaub und Abwesenheit vorgenommen worden, um diesen Fehler zu korrigieren, nachdem Urlaubs- und Abwesenheitsdatensätze in der Liste **Mir zugewiesen Arbeitsaufgaben** genehmigt sind.

### <a name="unable-to-recall-an-image-workflow"></a>Ein Bildworkflow kann nicht abgerufen werden

Nach dem Abruf eines Bildworkflows wird der Workflow auf „Storniert” festgelegt und die vorhandene Anforderung kann im Mitarbeiter-Self-Service-Arbeitsbereich gelöscht werden.

### <a name="rehired-employees-or-contractors-show-up-multiple-times-after-termination"></a>Erneut eingestellte Mitarbeiter oder Auftragnehmer werden mehrere Male nach Kündigung angezeigt 

Mit diesem Update werden gekündigte Mitarbeiter, die erneut eingestellt werden, nur einmal in der beendeten Liste angezeigt. 

## <a name="known-issue"></a>Bekannte Probleme

- **Abgang**: Wenn sie einer Arbeitskraft einen neuen Anhang hinzufügen, sind die Schaltflächen **Neu** und **Bearbeiten** ausgegraut. 
- **Problemumgehung:**, Bevor die Anhangseite geöffnet wird, stellen Sie sicher, dass die Infoboxen auf der Seite **Arbeitskraft** geschlossen sind. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)
