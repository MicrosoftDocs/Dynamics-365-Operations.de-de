---
title: Überblick Integration Dynamics 365 Commerce und Microsoft Teams
description: Dieses Thema bietet einen Überblick über die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021988"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Überblick Integration Dynamics 365 Commerce und Microsoft Teams

[!include [banner](includes/banner.md)]

Dieses Thema bietet einen Überblick über die Integration von Microsoft Dynamics 365 Commerce und Microsoft Teams.

Dynamics 365 Commerce wird in Teams integriert, um Debitoren und ihren Mitarbeitern zu helfen, die Produktivität zu verbessern, indem die Aufgabenverwaltung zwischen den beiden Anwendungen synchronisiert wird. Mit der nahtlosen Aufgabenverwaltung, die durch die Integration von Commerce und Teams bereitgestellt wird, können Filialleiter und Mitarbeiter Aufgabenlisten erstellen, Aufgaben mehreren Filialen zuweisen und den Status von Aufgaben in verschiedenen Shops von beiden Anwendungen aus verfolgen.

Die Integration von Commerce und Teams ist ab der Version 10.0.18 von Commerce verfügbar.

## <a name="key-features"></a>Schlüsselfeatures

Hier sind einige der wichtigsten Funktionen, welche die Integration von Commerce und Microsoft Teams bietet:

- Die Bereitstellung von Teams durch die Nutzung genau definierter Informationen aus Commerce nutzen, z. B. die Organisationsstruktur und Informationen zu Shops, Mitarbeitern, Berechtigungen und dem geschäftlichen Kontext.
- Synchronisieren Sie problemlos laufende Änderungen (z. B. neu hinzugefügte Filialen oder neu eingestellte Mitarbeiter) zwischen Commerce und Teams, behalten Sie jedoch Commerce als Hauptquelle für Organisationsstrukturdaten bei.
- Integrieren Sie die Aufgabenverwaltung zwischen Commerce und Teams, um Filialmitarbeitern, Filialleitern, Regionalmanagern und Kommunikationsmanagern bei der Verwaltung von Aufgaben in beiden Anwendungen zu helfen.

## <a name="prerequisites-for-using-integration-features"></a>Voraussetzungen für die Verwendung von Integrationsfunktionen

Die folgenden Voraussetzungen müssen erfüllt sein, bevor Sie mit der Verwendung von Microsoft Teams-Integrationsfunktionen beginnen können:

- Microsoft 365 Business-Standardlizenz (diese Lizenz enthält Teams)
- Azure Active Directory (Azure AD)-Konten für alle Filialleiter und Mitarbeiter
- POS-Systeme (Point of Sale), die mit Azure AD-Authentifizierung konfiguriert sind

## <a name="conceptual-architecture"></a>Konzeptionelle Architektur

Die folgende Abbildung zeigt die konzeptionelle Architektur der Integration von Dynamics 365 Commerce und Microsoft Teams am Beispiel eines Shops in San Francisco. Sowohl Teams als auch die Commerce-POS-Anwendung verwenden Microsoft Planner als Repository, sodass von Teams veröffentlichte Aufgaben in der POS-Anwendung angezeigt werden und von Filialleitern in der POS-Anwendung erstellte Ad-hoc-Aufgaben in Teams angezeigt werden, was zu einer nahtlosen Aufgabenverwaltung zwischen den Anwendungen führt.    

![Architektur der Integration von Commerce und Teams](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Integration von Dynamics 365 Commerce und Microsoft Teams aktivieren](enable-teams-integration.md)

[Microsoft Teams aus Dynamics 365 Commerce bereitstellen](provision-teams-from-commerce.md)

[Aufgabenverwaltung zwischen Microsoft Teams und Dynamics 365 Commerce POS synchronisieren](synchronize-tasks-teams-pos.md)

[Benutzerrollen in Microsoft Teams verwalten](manage-user-roles-teams.md)

[Shops und Teams zuordnen, wenn in Microsoft Teams bereits Teams vorhanden sind](map-stores-existing-teams.md)

[Integration von Dynamics 365 Commerce und Microsoft Teams – FAQ](teams-integration-faq.md)
