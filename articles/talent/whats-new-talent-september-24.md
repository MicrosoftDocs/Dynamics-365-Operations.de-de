---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (24. September 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aeb75fe4c775b9003c6429de536498f495224098
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304537"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a>Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (24. September 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.1015.0**

In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.

## <a name="currency-added-to-benefits"></a>Währung zu den Vergütungen hinzugefügt

Vorteilspläne wurden aktualisiert, um die Währung des Vorteils einzubeziehen. Dieses neue Feld ist auch für Vergütungen für registrierte Arbeitskräfte verfügbar. Dieses neue Feld ist ein Teil der Liste Vergütungen verwalten und zeigt eine Liste der Vorteile des Sicherheitsrechts an.

## <a name="update-proration-process--leave-and-absence"></a>Antizipierungen für Urlaub und Abwesenheit aktualisieren

Organisationsprämienfreizeit unterschiedlich auf der Basis, wenn Mitarbeiter das Unternehmen wechseln‌ das Unternehmen eintreten. Für Mitarbeiter, die die Organisation verlassen, müssen möglicherweise einige die Prämie im Feld Kündigungsdatum beendet werden, während andere erst am letzten Arbeitstag den,  Abgrenzungsprozess beenden. Diese Änderungen gibt Organisationen die Möglichkeit, auszuwählen, wann die Registrierung für den Kündigungsprozesses beendet wird. Diese neue Optionen sind Teil der Rechte, um einer Arbeitskraft zu kündigen und eine Arbeitskraft  vom Manager-Self-Service zu kündigen. 

## <a name="other-changes"></a>Andere Änderungen

Diese Version enthält eine Reihe zusätzlicher Fehlerkorrekturen.

## <a name="known-issue"></a>Bekannte Probleme

-   **Abgang:**, Wenn einer Arbeitskraft ein neuer Anhang hinzugefügt wird, werden die Schaltflächen **Neu** und **Bearbeiten** abgeblendet. **Problemumgehung:**, Bevor die Anhangsseite geöffnet wird, überprüfen Sie, dass die Infoboxen **Arbeitskraft** geschlossen werden. Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert. (Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)
