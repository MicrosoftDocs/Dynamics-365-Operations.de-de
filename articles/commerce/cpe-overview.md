---
title: Commerce-Vorschauumgebung – Übersicht
description: Dieses Thema enthält eine Übersicht der Microsoft Dynamics 365 Commerce-Vorschauumgebung.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906069"
---
# <a name="commerce-preview-environment-overview"></a>Commerce-Vorschauumgebung – Übersicht

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dieses Thema enthält eine Übersicht der Microsoft Dynamics 365 Commerce-Vorschauumgebung.

## <a name="overview"></a>Übersicht

Die Commerce-Vorschauumgebung ist eine optionale End-to-End-Vorschauumgebung von Dynamics 365 Commerce, mit der potenzielle Debitoren das Commerce-Produkt testen können, bevor es der Öffentlichkeit zugänglich gemacht wird.

Abgesehen von einigen geringfügigen Einschränkungen, die sich nicht auf Features oder Funktionen auswirken, bietet die Commerce-Vorschauumgebung die vollständige Commerce-Erfahrung und kann von Kunden und Implementierungspartnern verwendet werden, um das Produkt zu bewerten, Feedback zu geben und Anpassungs-/Lückenanalysen durchzuführen.

## <a name="limitations-of-the-commerce-preview-environment"></a>Einschränkungen der Commerce-Vorschauumgebung

Obwohl die Commerce-Vorschauumgebung alle Commerce-Funktionen und -Funktionen bietet, gibt es einige geringfügige Einschränkungen:

- Obwohl die Commerce-Vorschauumgebung selbst keine geografischen Einschränkungen aufweist, können Komponenten der Umgebung, wie z. B. Retail Cloud Scale Unit (RCSU) und E-Commerce-Anwendungen nur in den USA bereitgestellt werden.
- Die Verwendung der Commerce-Vorschauumgebung ist auf 30 Tage ab dem Datum der Bereitstellung von E-Commerce beschränkt.
- Die Commerce-Vorschauumgebung kann nur in einer Umgebung erfolgreich bereitgestellt und initialisiert werden, die die Demo-Topologie verwendet, in der alle Komponenten einer Umgebung in einer einzelnen virtuellen Maschine (VM) bereitgestellt werden. Die Hauptbeschränkung dieser OneBox-VM-Topologie ist die Anzahl der gleichzeitigen Benutzer, die die Vorschauumgebung unterstützen kann.
- Die Commerce-Vorschauumgebung kann nur bis zur allgemeinen Verfügbarkeit (GA) des Commerce-Produkts evaluiert werden. Neue Demo-Umgebungen werden nach GA verfügbar sein.

## <a name="get-started"></a>Erste Schritte

Informationen zum Bereitstellen der Commerce-Vorschauumgebung finden Sie unter [Stellen Sie eine Commerce-Vorschauumgebung bereit](provisioning-guide.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Bereitstellen einer Commerce-Vorschauumgebung](provisioning-guide.md)

[Konfigurieren einer Commerce-Vorschauumgebung](cpe-post-provisioning.md)

[Konfigurieren optionaler Funktionen für eine Commerce-Vorschauumgebung](cpe-optional-features.md)

[Commerce-Vorschauumgebung – FAQ](cpe-faq.md)
