---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (15. Oktober 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a50819d579c0ea42aac3f9a18fbcbf0d2cb9ca26
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518109"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-15-2018"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (15. Oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.1056**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.


## <a name="changes"></a>Änderungen
Neben verschiedenen Korrekturen wurden folgende Aktualisierungen in dieser Version vorgenommen:
- Letzter gearbeiteter Tag legt nun fest, wenn ein Beschäftigungs- Enddatum fest.
- US-Kompatibilitätsreferenzen wurden entfernt bei nicht US-Unternehmen (ADA, und I9).
- Ungültige Datumsangaben (1/1/1900) werden nun auf Analyseseiten ausgeblendet.

## <a name="known-issue"></a>Bekannte Probleme

**Problem:** Wenn einer Arbeitskraft ein neuer Anhang hinzugefügt wird, werden die Schaltflächen **Neu** und **Bearbeiten** abgeblendet. **Problemumgehung:**, Bevor die Anhangsseite geöffnet wird, überprüfen Sie, dass die Infoboxen **Arbeitskraft** geschlossen werden. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)
