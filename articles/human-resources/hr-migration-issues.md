---
title: Bekannte Probleme bei der Zusammenführung der Dynamics 365 Human Resources Infrastruktur
description: Dieser Artikel listet Probleme auf, die während der Zusammenführung der Microsoft Dynamics 365 Human Resources Infrastruktur auftreten.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752689"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Bekannte Probleme bei der Zusammenführung der Dynamics 365 Human Resources Infrastruktur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Freigegebene Dataverse-Umgebungen

Das Framework für duales Schreiben unterstützt das Verknüpfen von zwei Finanz- und Betriebs-App-Umgebungen mit derselben Dataverse Umgebung nicht. Wenn Sie eine Dataverse Umgebung haben, die mit den beiden folgenden Elementen freigegeben ist, müssen Sie entweder die Dataverse-Umgebung duplizieren oder sie aufteilen:

- Eine Finanz- und Betriebs-App
- Eine aktuelle Human Resources-Umgebung

## <a name="environment-type-requirements"></a>Anforderungen an den Umgebungstyp

Die folgenden Umgebungstypen sind erforderlich, bevor Sie die Migration durchführen können:

- Wenn Sie keine eigenständigen Sandbox-Umgebungen haben, müssen Sie zur Überprüfung der Migration eine erstellen.
- Wenn Sie über mehrere eigenständige Produktionsumgebungen verfügen, kann eine davon migriert werden. Wenden Sie sich an den Microsoft Support, um die anderen Umgebungen als Sandboxen zu kennzeichnen.

## <a name="teams-integration"></a>Teams-Integration

Die bestehende Human Resources-App in Teams wird derzeit auf eine Microsoft Power Platform Lösung umgestellt. Weitere Informationen finden Sie unter [Human Resources App in Teams](hr-admin-teams-leave-app.md).

