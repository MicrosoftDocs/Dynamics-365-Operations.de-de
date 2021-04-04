---
title: Fehlerbehebung bei der Wiederbeschaffung im Lagerort
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit der Lagerort-Wiederbeschaffung in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8dfb58c9156df106f58dfdc0ee2e0ef8defb9d9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263203"
---
# <a name="troubleshoot-warehouse-replenishment"></a>Fehlerbehebung bei der Lagerort-Wiederbeschaffung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die bei der Arbeit mit der Lagerort-Wiederbeschaffung in Microsoft Dynamics 365 Supply Chain Management auftreten können.

## <a name="i-receive-the-following-error-message-work-1-cannot-be-unblocked-because-it-has-unfinished-replenishment-work"></a>Ich erhalte die folgende Fehlermeldung: „Arbeit %1 kann nicht entsperrt werden, da sie nicht beendete Wiederbeschaffung hat.“

### <a name="issue-description"></a>Problembeschreibung

Die Entnahmearbeiten sind wegen abhängiger Wiederbeschaffung blockiert.

### <a name="issue-resolution"></a>Problemlösung

Wenn Sie die Nachschubwelle verwenden und ein Lagerplatz wiederbeschafft werden muss, um den Bedarf des Quellauftrags zu erfüllen, erstellt das System sowohl die Wiederbeschaffungsarbeit als auch die Entnahmearbeiten. Es blockiert jedoch die Entnahmearbeiten, bis die Wiederbeschaffung abgeschlossen ist. Dieses Verhalten ist beabsichtigt, da der Lagerplatz nicht über genügend Bestand verfügt, solange die Wiederbeschaffung nicht abgeschlossen ist. Schließen Sie die Wiederbeschaffung ab, und verarbeiten Sie dann die Entnahmearbeiten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]