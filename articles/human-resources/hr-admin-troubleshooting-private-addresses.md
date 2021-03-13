---
title: Zugriff auf private Informationen nach Sicherheitsrolle
description: In diesem Artikel wird erläutert, wie das Problem gelöst wird, wobei ein Kunde nicht auf Privatadressen zugreifen kann.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6598094e7877a30c35e1b03794f82c8a4ec001a7
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112641"
---
# <a name="access-to-private-addresses-by-security-role"></a>Zugriff auf private Adressen nach Sicherheitsrolle

**Abgang**

Nachdem ein Kunde eine Sicherheitsrolle dupliziert und sich als diese neue Rolle anmeldet, kann der Kunde die Adressen, die als privat markiert wurden, nicht sehen.

**Auflösung**

Um das Problem zu beheben, muss der Kunde diese Schritte für die duplizierte Sicherheitsrolle befolgen.

1. Wechseln Sie zu **Organisationsverwaltung \> Globales Adressbuch \> Parameter für das globale Adressbuch**.
2. Auf der Registerkarte **Sicherheit für private Standorte** verschieben Sie die neue Sicherheitsrolle von der Liste **Verfügbare Rollen** in die Liste **Ausgewählte Rollen**.
3. Wählen Sie **Speichern**.

![Seite „Parameter des globalen Adressbuchs”](media/GAD-parameters.png)
