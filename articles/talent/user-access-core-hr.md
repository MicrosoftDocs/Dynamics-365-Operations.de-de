---
title: Benutzer kann auf Personalverwaltung aber nicht auf Onboard oder Attract zugreifen
description: In diesem Thema wird erläutert, wie das Problem gelöst wird, wenn ein Benutzer auf Microsoft Dynamics 365 Talent – Personalverwaltung aber nicht auf Attract oder Onboard zugreifen kann.
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
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461264"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Benutzer kann auf Personalverwaltung aber nicht auf Onboard oder Attract zugreifen

[!include [banner](includes/banner.md)]

**Umgebungsdetails**

- Die Microsoft Dynamics Lifecycle Services (LCS)-Bereitstellung wurde von Benutzer A ausgeführt.
- Benutzer A hat Benutzer B als Benutzer zu Microsoft Dynamics 365 Human Resources hinzugefügt.

**Abgang**

Benutzer B kann auf Personalverwaltung aber nicht auf Talent zugreifen: Attract- oder Talent: Onboard-App. Wenn der Benutzer versucht, zu **Erfahrungs-Apps** zu wechseln, wird er oder sie zu einer stattdessen zu einer Testumgebung geführt.

**Lösung**

Benutzer B müssen die Rechte zugewiesen werden, um die Microsoft Power Apps-Umgebung anzuzeigen, die Benutzer A während des Bereitstellungsprozesses erstellt hat.

Informationen dazu finden Sie im Abschnitt „Zugriff auf die Umgebung gewähren” in [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

**Langfristige Lösung**

Microsoft erwägt, die entsprechenden Rechte automatisch an Onboard oder Attact zuzuweisen, wenn ein Benutzer zu Personalverwaltung hinzugefügt wurde.
