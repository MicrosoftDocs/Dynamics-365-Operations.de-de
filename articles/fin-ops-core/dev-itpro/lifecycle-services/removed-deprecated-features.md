---
title: Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)
description: In diesem Thema werden die Funktionen beschrieben, die aus Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder entfernt werden sollen.
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: abf7a1a0a75ac3098efeeab3df65481999b69acc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687877"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>Entfernte oder veraltete Funktionen in Lifecycle Services (LCS)

[!include[banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die für Microsoft Dynamics Lifecycle Services (LCS) entfernt wurden oder veraltet sind.

- Eine Funktion *entfernt* ist nicht mehr im Dienst verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll Ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen.

## <a name="october-2019-announcements"></a>Oktober 2019 Ankündigungen

### <a name="flowchart-diagrams-in-business-process-modeler"></a>Flussdiagramme im Geschäftsprozessmodellierer

<table>
<tbody>
<tr>
<td><strong>Grund für veralteten Zustand/Entfernung</strong></td>
<td>Die Flowchart-Diagrammkomponente im Geschäftsprozessmodellierer (BPM) wird nicht mehr empfohlen, da das Legacy-Design zu einer geringen Nutzung geführt hat.</td>
</tr>
<tr>
<td><strong>Ersetzt durch eine andere Funktion?</strong></td>
<td>Nein</td>
</tr>
<tr>
<td><strong>Betroffene Bereiche</strong></td>
<td>Geschäftsprozessmodellierer</td>
</tr>
<tr>
<td><strong>Status</strong></td>
<td>Veraltet: Die Flussdiagrammkomponente in BPM wird voraussichtlich im Jahr 2020 entfernt. Folgende Funktion wird nicht mehr verfügbar sein:
<ul>
<li>Alle Flussdiagramme sind schreibgeschützt und können nicht bearbeitet werden. Die Formeigenschaften, die Flussdiagrammaktivitäten zugeordnet sind, sind ebenfalls nicht verfügbar. Diese Flussdiagramme umfassen sowohl automatisch generierte Standardflussdiagramme als auch benutzerdefinierte Flussdiagramme, die auf der Grundlage dieser Standardflussdiagramme geändert werden.</li>
<li>Die Prozessschritte sind schreibgeschützt und können nicht bearbeitet werden.</li>     
<li>Die Funktion zur Analyse älterer Anpassungen/Lücken ist nicht verfügbar. Daher wird keine Lückenliste automatisch erstellt oder steht für den Export zur Verfügung.
<p><strong>Hinweis:</strong> Diese Funktion war zuvor veraltet und wurde durch Microsoft Azure DevOps-Integrationen ersetzt.</p>
</li>
<li>Der Versionsverlauf des Flussdiagramms ist nicht verfügbar.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]