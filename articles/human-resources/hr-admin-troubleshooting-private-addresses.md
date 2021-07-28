---
title: Zugriff auf private Informationen nach Sicherheitsrolle
description: In diesem Artikel wird erläutert, wie das Problem gelöst wird, wobei ein Kunde nicht auf Privatadressen zugreifen kann.
author: andreabichsel
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15616a9b3673a4c1842e389b976a80d599e2e77f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346321"
---
# <a name="access-to-private-addresses-by-security-role"></a>Zugriff auf private Adressen nach Sicherheitsrolle

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Abgang**

Nachdem ein Kunde eine Sicherheitsrolle dupliziert und sich als diese neue Rolle anmeldet, kann der Kunde die Adressen, die als privat markiert wurden, nicht sehen.

**Auflösung**

Um das Problem zu beheben, muss der Kunde diese Schritte für die duplizierte Sicherheitsrolle befolgen.

1. Wechseln Sie zu **Organisationsverwaltung \> Globales Adressbuch \> Parameter für das globale Adressbuch**.
2. Auf der Registerkarte **Sicherheit für private Standorte** verschieben Sie die neue Sicherheitsrolle von der Liste **Verfügbare Rollen** in die Liste **Ausgewählte Rollen**.
3. Wählen Sie **Speichern** aus.

![Seite „Parameter des globalen Adressbuchs“.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]