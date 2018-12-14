---
title: Benutzer kann auf Core HR, aber nicht auf die Onboard- oder Attract-App zugreifen
description: "In diesem Thema wird erläutert, wie das Problem gelöst wird, wenn ein Benutzer auf Microsoft Dynamics 365 for Talent Core HR, aber nicht auf die Attract- und Onboard-App zugreifen kann."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Benutzer kann auf Core HR, aber nicht auf die Onboard- oder Attract-App zugreifen

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

