---
title: Bevorzugte Wartungsarbeiter einrichten
description: In diesem Thema wird erläutert, wie Sie bevorzugte Wartungsmitarbeiter im Anlagenmanagement einrichten.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887410"
---
# <a name="preferred-maintenance-workers"></a>Bevorzugte Wartungsarbeiter

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Sie können bei der Arbeitsvorbereitung einstellen, welche Wartungsmitarbeiter zu kompletten Arbeitsaufträgen zugeordnet werden. Die Verwendung dieser Funktionalität ist optional, kann Ihnen aber helfen, sich für den am besten qualifizierten Wartungstechniker zu entscheiden, um einen Auftrag auszuführen, basierend auf den Fähigkeiten und Kompetenzen des Arbeiters. Daher wird bei der Arbeitsauftragsplanung anhand des Einrichtens unter **Bevorzugte Wartungsmitarbeiter** festgelegt, ob ein bestimmter Wartungsmitarbeiter oder eine bestimmte Mitarbeitergruppe für einen Arbeitsauftrag geplant werden soll. Es werden nur Wartungsmitarbeiter geplant, die zur Planungszeit verfügbar sind. Wenn eine bevorzugte Einrichtung eines Wartungsmitarbeiters bei der Terminierung mit einem Arbeitsauftrag übereinstimmt, der Wartungsmitarbeiter aber anderen Aufträgen zugeordnet ist, wird der Arbeitsauftrag einem anderen, verfügbaren Wartungsmitarbeiter zugeordnet.

Bevor Sie bevorzugte Wartungsmitarbeiter einrichten können, müssen Sie zunächst die Wartungsmitarbeiter und Arbeitsgruppen einrichten, die zur Auswahl stehen sollen. Unter [Wartungspersonal und Arbeitsgruppen](../setup-for-objects/workers-and-worker-groups.md) finden Sie eine Beschreibung, wie Sie Wartungspersonal und Arbeitsgruppen einrichten können.

## <a name="set-up-preferred-workers"></a>Einrichten von bevorzugten Mitarbeitern

Ein bevorzugter Wartungsmitarbeiter oder eine bevorzugte Mitarbeitergruppe kann mit einer bestimmten Person in Verbindung gebracht werden.

- Handel  
- Variante der Wartungsauftragsart  
- Wartungsauftragsart  
- Wartungsjobtyp Kategorie  
- Anlage  
- Anlagenart  

oder eine Kombination dieser Auswahlmöglichkeiten. Je mehr Auswahlen Sie für den gleichen Datensatz treffen, desto spezifischer wird Ihr Setup sein.

1. Klicken Sie auf **Anlagenmanagement** > **Einrichtung** > **Arbeiter** > **Bevorzugte Wartungsmitarbeiter**.

2. Klicken Sie auf **Neu**, um einen neuen Datensatz zu erstellen.

3. Beginnen Sie mit der Erstellung eines „standardmäßigen“ Wartungsmitarbeiters oder einer Arbeitsgruppeneinrichtung, die keine Auswahl in den Feldern der obigen Aufzählungsliste hat. D.h. Sie treffen nur eine Auswahl im Feld **Bevorzugte Wartungsmitarbeitergruppe** oder im Feld **Bevorzugte Wartungsmitarbeiter**. In der folgenden Abbildung sehen Sie ein Beispiel im ersten Datensatz, in dem „Anfragen“ als bevorzugte Wartungsmitarbeitergruppe ausgewählt ist.

>[!NOTE]
>Die Standardeinstellung wird bei der Arbeitsauftragsplanung verwendet, falls keine andere, spezifischere Kombination mit dem Inhalt des Arbeitsauftrags bei der Arbeitsauftragsplanung übereinstimmt.

4. Wiederholen Sie Schritt 2, um einen neuen Datensatz zu erstellen. Nehmen Sie die erforderlichen Einstellungen vor, je nach Detaillierungsgrad des bevorzugten Mitarbeiters oder der bevorzugten Mitarbeitergruppe. *Beispiel:* In der folgenden Abbildung, im sechsten Datensatz, wird der Wartungsarbeiter Shawn Richardson als bevorzugter Arbeiter ausgewählt. Er wird automatisch bei der Terminierung eines Arbeitsauftrags ausgewählt, der die Anlage „CH-BP1-03-02“ und die Auftragsart „Anlagenbewertung“ beinhaltet, wenn er zum geplanten Zeitpunkt verfügbar ist.

>[!NOTE]
>Im Allgemeinen, wenn ein bevorzugter Wartungsmitarbeiter während der Arbeitsauftragsplanung ausgewählt wird, durchläuft das Asset Management alle **Bevorzugter Mitarbeiter** Datensätze, um nach einer möglichen Übereinstimmung zu suchen, wobei immer zuerst die spezifischste Kombination geprüft wird. Wenn keine Übereinstimmung gefunden wird, wird der „Standarddatensatz“ mit einer Auswahl entweder im Feld **Bevorzugte Wartungspersonengruppe** oder im Feld **Bevorzugte Wartungsperson** verwendet.


![Abbildung 1](media/02-work-order-scheduling.png)

Sie können auch verantwortliche Instandhaltungsmitarbeiter einrichten, die beim Anlegen einer Wartungsanforderung oder eines Arbeitsauftrags ausgewählt werden können. Unter **Alle Arbeitsaufträge** und **Alle Wartungsanforderungen** können Sie die Auswahl bei Bedarf bearbeiten. Weitere Informationen finden Sie unter [Verantwortliche Wartungsmitarbeiter](../setup-for-maintenance-requests/responsible-workers.md).

Bei der Arbeitsauftragsplanung werden verschiedene Werten berechnet, um festzustellen, welche Mitarbeiter die mit einem Arbeitsauftrag zusammenhängenden Aufgaben erledigen sollen (diese Noten werden in **Anlagenmanagementparameter** > **Auftragsplanung**Link eingerichtet). Wenn zwei oder mehr bevorzugte Wartungsmitarbeiter oder verantwortliche Wartungsmitarbeiter bei der Arbeitsauftragsplanung die gleiche Punktzahl erhalten, wird ein Mitarbeiter zufällig ausgewählt. Andernfalls ist es immer der Mitarbeiter mit der höchsten Punktzahl, der für die Erledigung eines Arbeitsauftrags vorgesehen ist.

