---
title: Erstellen einer Umgebung im Power Apps Admin Center nicht möglich
description: In diesem Thema wird erklärt, was zu tun ist, wenn der Administrator keine Umgebung im Microsoft Power Apps Admin Center erstellen kann.
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
ms.openlocfilehash: 5923c59ab5dde13fed0483972e76634031404fd8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773218"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Erstellen einer Umgebung im Power Apps Admin Center nicht möglich

[!include [banner](includes/banner.md)]

**Abgang**

- Der Mandanten-/Umgebungsadministrator kann keine Umgebung im Microsoft Power Apps Admin Center erstellen.
- Eine Lizenz, die Benutzern das Recht zum Ausführen des Umgebungserstellungsschritts gibt, ist dem Benutzer, der diesen Schritt ausführt, nicht direkt zugewiesen worden.

**Lösung**

Stellen Sie sicher, dass der Mandantenadministrator eine gültige Power Apps P2-Lizenz direkt dem Benutzer zugewiesen hat, der den Umgebungserstellungsschritt ausführt. Hier sind die Microsoft Dynamics-Servicepläne, die dieses Recht gewähren.

| Gesamtprodukt-Lagermengeneinheit (SKU)       | Power Apps P2-Serviceplan  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365-Plan – Enterprise Edition | Power Apps for Dynamics 365 |

Beachten Sie, dass verschiedene Microsoft Office-SKUs auch das Recht bereitstellen, zusammen mit den eigenständigen Power Apps Plan 2 SKUs. Der wichtige Aspekt ist, dass einer dieser SKUs vorhanden sein muss.

1. Gehe zu [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments).
2. Erstellen Sie die Umgebungen, indem Sie in die Anweisungen befolgen in [Talent bereitstellen](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).
