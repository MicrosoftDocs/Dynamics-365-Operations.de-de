---
title: "Erstellen einer Umgebung im PowerApps Admin Center nicht möglich"
description: "In diesem Thema wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft PowerApps Admin Center erstellen kann."
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
ms.openlocfilehash: 6f9b7ceef6895b295e6ae5a50d8ac7970497efe5
ms.contentlocale: de-de
ms.lasthandoff: 12/04/2018

---

# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>Erstellen einer Umgebung im PowerApps Admin Center nicht möglich

[!include [banner](includes/banner.md)]

**Abgang**

- Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft PowerApps Admin Center erstellen.
- Eine Lizenz, die Benutzern das Recht zum Ausführen des Umgebungserstellungsschritts gibt, ist dem Benutzer, der diesen Schritt ausführt, nicht direkt zugewiesen worden.

**Lösung**

Stellen Sie sicher, dass der Mandantenadministrator eine gültige PowerApps P2-Lizenz direkt dem Benutzer zugewiesen hat, der den Umgebungserstellungsschritt ausführt. Hier sind die Microsoft Dynamics-Servicepläne, die Ihnen dieses Recht gewähren.

| Gesamtprodukt-Lagermengeneinheit (SKU)       | PowerApps P2-Serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365-Plan – Enterprise Edition | PowerApps for Dynamics 365 |

Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen PowerApps Plan 2-SKUs. Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.

1. Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Talent bereitstellen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

