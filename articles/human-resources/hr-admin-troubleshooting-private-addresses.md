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
ms.openlocfilehash: 21919e0bf75a5a47fc64b87410ccd75ff34259fb1c8c2bc1aa82318dcd0572b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719115"
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