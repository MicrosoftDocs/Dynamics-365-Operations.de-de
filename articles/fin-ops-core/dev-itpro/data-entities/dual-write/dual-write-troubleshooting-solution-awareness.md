---
title: Probleme bezüglich der Lösungssensitivität beheben
description: Dieses Thema enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Lösungserkennung zusammenhängen.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f9e02a6a5afe965a1707f0b04e1b4daedd4ec1df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566788"
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