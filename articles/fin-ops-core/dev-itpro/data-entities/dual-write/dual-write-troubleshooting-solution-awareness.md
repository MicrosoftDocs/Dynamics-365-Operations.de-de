---
title: Probleme bezüglich der Lösungssensitivität beheben
description: Dieser Artikel enthält Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Lösungserkennung zusammenhängen.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c280eef995664c640e382817dda9d6e1cde154c6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871494"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Probleme bezüglich der Lösungssensitivität beheben

[!include [banner](../../includes/banner.md)]





Dieser Artikel enthält Informationen zur Problembehandlung für die Integration von dualem Schreiben zwischen Finanz- und Betriebs-Apps und Dataverse. Dieses Thema enthält besonders Informationen zur Fehlerbehebung, mit denen Sie Probleme beheben können, die mit der Lösungserkennung zusammenhängen.

> [!IMPORTANT]
> Einige der in diesem Artikel behandelten Probleme erfordern möglicherweise entweder die Systemadministratorrolle oder Microsoft Azure Active Directory (Azure AD)-Anmeldeinformationen des Mandantenadministrators. Im Abschnitt zu jedem Problem wird erläutert, ob eine bestimmte Rolle oder Anmeldeinformationen erforderlich sind.

## <a name="error-on-the-dual-write-page"></a>Fehler auf der Seite Duales Screiben

Auf der Seite **Duales Schreiben** wird möglicherweise eine Fehlermeldung angezeigt, die dem folgenden Beispiel ähnelt:

*Die Entität mit dem Namen 'msdyn\_dualwriteentitymap 'mit namemapping =' Logical 'wurde im MetadataCache nicht gefunden.*

Stellen Sie zur Behebung des Problems sicher, dass die Dual-Write-Core-Lösung in Dataverse instaliert ist. Die Dual-Write-Core-Lösung ist eine Voraussetzung für das Lösungsbewusstsein.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]