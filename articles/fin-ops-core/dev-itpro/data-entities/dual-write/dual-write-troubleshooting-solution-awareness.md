---
title: Probleme bezüglich der Lösungssensitivität beheben
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Lösungserkennung zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: ec5afd92a71c8b12c913de78a513abb0959df88a
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782060"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Probleme bezüglich der Lösungssensitivität beheben

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse. Dieses Thema enthält besonders Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Lösungserkennung zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Thema behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD) Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="error-on-the-dual-write-page"></a>Fehler auf der Seite Duales Screiben

Auf der Seite **Duales Schreiben** wird möglicherweise eine Fehlermeldung angezeigt, die dem folgenden Beispiel ähnelt:

*Die Entität mit dem Namen 'msdyn\_dualwriteentitymap 'mit namemapping =' Logical 'wurde im MetadataCache nicht gefunden.*

Stellen Sie zur Behebung des Problems sicher, dass die Dual-Write-Core-Lösung in Dataverse instaliert ist. Die Dual-Write-Core-Lösung ist eine Voraussetzung für das Lösungsbewusstsein.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]