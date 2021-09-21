---
title: Bestandsstatusänderung kann nicht als Arbeitstyp ausgewählt werden.
description: Sie können keine Arbeitsvorlagenposition für die Bestandsstatusänderung erstellen, da der Arbeitstyp nur von Systemprozessen verwendet wird. Wählen Sie einen anderen Arbeitstyp aus.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476478"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>In der Spalte „Arbeitstyp“ kann keine Inventarstatusänderung ausgewählt werden.

## <a name="symptoms"></a>Symptome

Beim Konfigurieren von Microsoft Dynamics 365 Supply Chain Management erhalten Sie möglicherweise die folgende Fehlermeldung:

> Sie können keine Arbeitsvorlagenposition für die Bestandsstatusänderung erstellen, da der Arbeitstyp ungültig ist. Wählen Sie einen anderen Arbeitstyp aus.

## <a name="resolution"></a>Lösung

Dieses Verhalten ist beabsichtigt. Der Arbeitstyp *Bestandsstatusänderung* wird nur von Systemprozessen verwendet. Er kann nicht konfiguriert werden. Da die Liste der Arbeitstypen als Aufzählung festgelegt ist, können die zusätzlichen Einträge nicht aus dem Dropdown-Menü **Arbeitstyp** herausgefiltert werden.
