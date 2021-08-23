---
title: Erstellen einer Umgebung im Power Apps Admin Center nicht möglich
description: In diesem Artikel wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft Power Apps Admin Center erstellen kann.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ca9e3db374c46dd00f0bb2f1f655e9acaf87fcfd2699f94c6703905d544cd84
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745717"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Erstellen einer Umgebung im Power Apps Admin Center nicht möglich

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Abgang**

- Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft Power Apps Admin Center erstellen.
- Der Benutzer verfügt nicht über eine Lizenz, die das Recht zum Erstellen von Umgebungen einräumt.

**Lösung**

Stellen Sie sicher, dass der Mandantenadministrator dem Benutzer, der die Umgebung erstellt, eine gültige Power Apps-P2-Lizenz zugewiesen hat. Folgende Microsoft Dynamics-Servicepläne bieten Berechtigungen zum Erstellen von Umgebungen:

| Gesamtprodukt-Lagermengeneinheit (SKU)       | Power Apps P2-Serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365-Plan – Enterprise Edition | Power Apps for Dynamics 365 |

Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen Power Apps Plan 2 SKUs. Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.

1. Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Human Resources bereitstellen](/dynamics365/unified-operations/talent/provisioning-talent).


[!INCLUDE[footer-include](../includes/footer-banner.md)]