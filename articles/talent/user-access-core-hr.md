---
title: Benutzer kann auf Core HR, aber nicht auf Onboard oder Attract zugreifen
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, wenn ein Benutzer auf Microsoft Dynamics 365 Talent – Core HR, aber nicht auf die Attract- und Onboard-App zugreifen kann.
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
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009305"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Benutzer kann auf Core HR, aber nicht auf Onboard oder Attract zugreifen

[!include [banner](includes/banner.md)]

**Umgebungsdetails**

- Die Microsoft Dynamics Lifecycle Services (LCS)-Bereitstellung wurde von Benutzer A ausgeführt.
- Benutzer A hat Benutzer B als Benutzer zu Microsoft Dynamics 365 Talent: Core HR hinzugefügt.

**Abgang**

Benutzer B kann auf Core HR, aber nicht auf Talent zugreifen: Attract oder Talent: Onboard-App. Wenn der Benutzer versucht, zu **Erfahrungs-Apps** zu wechseln, wird er oder sie zu einer stattdessen zu einer Testumgebung geführt.

**Lösung**

Benutzer B müssen die Rechte zugewiesen werden, um die Microsoft PowerApps-Umgebung anzuzeigen, die Benutzer A während des Bereitstellungsprozesses erstellt hat.

Informationen dazu finden Sie im Abschnitt „Zugriff auf die Umgebung gewähren” in [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langfristige Lösung**

Microsoft erwägt, die entsprechenden Rechte automatisch an Onboard oder Attact zuzuweisen, wenn ein Benutzer zu Core HR hinzugefügt wurde.
