---
title: Einrichtung der Elektronischen Rechnungsstellung
description: Dieser Artikel bietet einen Überblick über den Prozess zur Einrichtung und Konfiguration der Elektronischen Rechnungsstellung.
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272178"
---
# <a name="electronic-invoicing-setup"></a>Einrichtung der Elektronischen Rechnungsstellung

[!include [banner](../includes/banner.md)]

Der Artikel bietet einen Überblick über die Einrichtung und Konfiguration der Elektronischen Rechnungsstellung. Sie müssen die Schritte der Einrichtung in der hier angegebenen Reihenfolge durchführen. Wenn ein Schritt obligatorisch ist, Sie ihn aber überspringen, funktioniert die Funktionalität nicht korrekt und es kommt zu mehreren Fehlern bei nachfolgenden Schritten oder bei der Verwendung der Funktionalität. 

Bevor Sie beginnen, stellen Sie sicher, dass alle Hauptkomponenten korrekt eingerichtet sind, dass Sie sich für den Regulatory Configuration Service (RCS) angemeldet haben und über eine Instanz von RCS verfügen, und dass das Add-In für die Elektronische Rechnungsstellung für Ihre Microsoft Dynamics 365 Finance- oder Dynamics 365 Supply Chain Management-Umgebung installiert ist. Weitere Informationen finden Sie unter [Elektronische Rechnungsstellung einrichten und installieren](e-invoicing-install-add-in-microservices-lcs.md).

Als nächstes legen Sie die Azure-Ressourcen fest, die die Elektronische Rechnungsstellung für ihre Arbeit benötigt. Weitere Informationen finden Sie unter [Einrichten von Azure-Ressourcen für die Elektronische Rechnungsstellung](e-invoicing-set-up-azure-resources.md).

Nachdem die Hauptkomponenten konfiguriert sind, arbeiten Sie mit RCS, um die wichtigsten logischen Komponenten der Elektronischen Rechnungsstellung festzulegen. Legen Sie zunächst die Anzahl der Service-Umgebungen fest, die Sie pflegen werden. Auf diese Weise definieren Sie die logische Daten- und Konfigurationspartitionierung, um sicherzustellen, dass Sie eine Grenze zwischen einer Entwicklungs- oder Testumgebung und den Produktionsumgebungen ziehen. Um Ihren Entwicklungsprozess flexibel festzulegen, benötigen Sie möglicherweise mehrere separate Entwicklungs- und Testumgebungen. Zusätzlich zur Definition von Umgebungen für Services legen Sie direkt von RCS aus eine Verbindung zu Ihren Geschäftsanwendungen wie Finance oder Supply Chain Management fest, um die Parameter einzurichten, die für einen ordnungsgemäßen Vorgang mit Elektronischer Rechnungsstellung erforderlich sind. Weitere Informationen über Umgebungen finden Sie unter [Serviceumgebungen](e-invoicing-service-environments.md).

Nachdem alles eingerichtet ist, können Sie Ihre eigenen Funktionen für die Globalisierung erstellen, die verschiedene Szenarien für die Verarbeitung elektronischer Belege und die Umwandlung von Daten oder für den Import der Dokumente aus dem globalen Repository definieren. Weitere Informationen über die Arbeit mit Globalisierungsfunktionen finden Sie unter [Arbeiten mit Globalisierungsfunktionen](e-invoicing-working-globalization-features.md).

Wenn Ihre Szenarien die Integration mit E-Mail oder SharePoint erfordern, um eingehende elektronische Belege zu verarbeiten, finden Sie unter [Verarbeitung eingehender elektronischer Belege](e-invoicing-process-incoming-electronic-documents.md) Informationen darüber, wie Sie diese Kanäle festlegen und nutzen können.
