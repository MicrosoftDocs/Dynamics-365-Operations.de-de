---
title: Beheben Sie Probleme mit Erweiterungen bei Store Commerce
description: In diesem Artikel wird erläutert, wie Sie Probleme mit Erweiterungen in der Microsoft Dynamics 365 Commerce Store Commerce-App beheben.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269780"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Beheben Sie Probleme mit Erweiterungen bei Store Commerce

[!include [banner](../includes/banner.md)]

In diesem Artikel wird erläutert, wie Sie Probleme mit Erweiterungen in der Microsoft Dynamics 365 Commerce Store Commerce-App beheben.

## <a name="extensions-packages-arent-loaded"></a>Erweiterungspakete werden nicht geladen

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Erweiterungspakete werden nicht auf der Seite POS-Einstellungen \> angezeigt

Commerce Runtime-Trigger (CRT) wurden möglicherweise nicht aktualisiert, um das Erweiterungspaket einzuschließen, oder sie werden nicht bereitgestellt. Weitere Informationen finden Sie unter [Erweiterbarkeit und Trigger (CRT) der Commerce Runtime](../dev-itpro/commerce-runtime-extensibility-trigger.md).

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Erweiterungspakete werden auf der Seite POS-Einstellungen \> angezeigt, aber das Manifest wird nicht geladen

Vergewissern Sie sich, dass die Erweiterungspakete im Ordner **C:\\Programme\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Erweiterungen** vorhanden sind. Wenn die Pakete vorhanden sind, sollte dort ein **POS-Ordner** vorhanden sein, der das Manifest enthält.

Wenn kein **POS**-Ordner vorhanden ist, vergewissern Sie sich, dass das Store Commerce-Projekt korrekt auf das POS-Erweiterungsprojekt (Point of Sale) verweist. Überprüfen Sie den Projektverweispfad, und stellen Sie sicher, dass er vorhanden ist. 

In der folgenden Beispielabbildung weist das Installationsprojekt Probleme mit dem Erweiterungsprojekt auf, auf das verwiesen wird.

![Die Projektreferenz für das Store Commerce-Installationsprogramm ist ungültig.](media/ReferenceNotValid.png)

Wenn der Verweis für das Erweiterungsprojekt ordnungsgemäß hinzugefügt wird, tritt im Installationsprojekt keine Warnung oder kein Abhängigkeitsproblem auf, wie in der folgenden Beispielabbildung gezeigt.

![Die Projektreferenz für das Store Commerce-Installationsprogramm ist gültig.](media/ReferenceValid.png)
