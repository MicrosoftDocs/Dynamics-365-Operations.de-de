---
title: Benutzer kann auf Core HR, aber nicht auf die Onboard- oder Attract-App zugreifen
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, wenn ein Benutzer auf Microsoft Dynamics 365 for Talent Core HR, aber nicht auf die Attract- und Onboard-App zugreifen kann.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "855655"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Benutzer kann auf Core HR, aber nicht auf die Onboard- oder Attract-Anwendung zugreifen

[!include [banner](includes/banner.md)]

**Umgebungsdetails**

- Die Microsoft Dynamics Lifecycle Services (LCS)-Bereitstellung wurde von Benutzer A ausgeführt.
- Benutzer A hat Benutzer B als Benutzer zu Microsoft Dynamics 365 for Talent Core HR hinzugefügt.

**Abgang**

Benutzer B kann auf Core HR, aber nicht auf Talent zugreifen: Attract oder Talent: Onboard-App. Wenn der Benutzer versucht, zu **Erfahrungs-Apps** zu wechseln, wird er oder sie zu einer stattdessen zu einer Testumgebung geführt.

**Lösung**

Benutzer B müssen die Rechte zugewiesen werden, um die Microsoft PowerApps-Umgebung anzuzeigen, die Benutzer A während des Bereitstellungsprozesses erstellt hat.

Informationen dazu finden Sie im Abschnitt „Zugriff auf die Umgebung gewähren” in [Talent bereitstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Langfristige Lösung**

Microsoft erwägt, die entsprechenden Rechte automatisch an Onboard oder Attact zuzuweisen, wenn ein Benutzer zu Core HR hinzugefügt wurde.
