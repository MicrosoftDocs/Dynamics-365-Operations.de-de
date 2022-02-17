---
title: Dynamics 365 Finance und Dynamics 365 Supply Chain Management in der Community Cloud (GCC) der US-Regierung
description: Dieses Thema bietet Informationen über Microsoft Dynamics 365 US Government-Produkte, die qualifizierten staatlichen und privaten Einrichtungen zur Verfügung stehen.
author: hasaid
ms.date: 11/12/2021
ms.topic: article
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2021-11-09
ms.openlocfilehash: 0c8b88e5d190f6dc9beb9342909d1e489d4af10b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062285"
---
# <a name="dynamics-365-finance-and-dynamics-365-supply-chain-management-in-us-government-community-cloud-gcc"></a>Dynamics 365 Finance und Dynamics 365 Supply Chain Management in der Community Cloud (GCC) der US-Regierung

[!include [banner](../includes/banner.md)]



Ausgewählte Microsoft Dynamics 365 US Government-Regierungsprodukte stehen qualifizierten staatlichen und privaten Einrichtungen zur Verfügung. Diese Entitäten sind auf die folgenden Typen beschränkt:

- US-Bundes-, Staats-, Kommunal-, Stammes- und Gebietsentitäten
- Private Unternehmen, die Dynamics 365 US Government verwenden, um Lösungen für Behörden oder qualifizierte Mitglieder der Cloud-Community bereitzustellen
- Private Unternehmen mit Kundendaten, die behördlichen Vorschriften unterliegen, und Dynamics 365 US Government ist der geeignete Dienst, um die behördlichen Anforderungen zu erfüllen

Informationen finden Sie unter [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government).

## <a name="onboarding"></a>Einarbeitung

Um das anfängliche Onboarding für ein Implementierungsprojekt in Microsoft Dynamics Lifecycle Services (LCS) abzuschließen, folgen Sie den Anweisungen in [Onboarding eines Implementierungsprojekts](../../../fin-ops-core/fin-ops/imp-lifecycle/onboard.md). Verwenden Sie jedoch nicht den Link zu öffentlichen LCS, der in dieser Anleitung bereitgestellt wird. Verwenden Sie stattdessen die folgende URL, um LCS für die US Government Community Cloud (GCC) zu öffnen: <https://gov.lcs.microsoftdynamics.us>.

Befolgen Sie nach Abschluss des anfänglichen Onboardings die Anweisungen in [Projekt-Onboarding](../lifecycle-services/project-onboarding.md). Verwenden Sie noch einmal [LCS für GCC](https://gov.lcs.microsoftdynamics.us) anstelle von öffentlichen LCS.

## <a name="environment-deployment"></a>Bereitstellen der Umgebung

Nachdem Sie das Projekt-Onboarding abgeschlossen haben, können Sie sich die zusätzlichen Funktionalitäten von LCS ansehen, die in [Lifecycle Services (LCS) für Apps für Finanzen und Betrieb Kunden](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) beschrieben sind. Fahren Sie dann mit der Umgebungsbereitstellung fort.

- Um von Microsoft verwaltete Umgebungen über LCS bereitzustellen, folgen Sie den Anweisungen in [Lifecycle Services (LCS) für Apps für Finanzen und Betrieb Debitor](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md#new-deployment-experience).
- Informationen zu cloud-gehosteten Umgebungen finden Sie unter [Entwicklungsumgebungen bereitstellen und darauf zugreifen](../../../fin-ops-core/dev-itpro/dev-tools/access-instances.md). Sie müssen auch den Resource Manager-Onboarding-Prozess für Ihre Connectors abschließen, wie in [Onboardingprozess von Azure Resource Manager für Lifecycle Services-Projekte der US-Regierung abschließen](arm-onbarding-us-goverment.md) beschrieben.

> [!NOTE]
> Für LCS-Projekte der US-Regierung werden nur Azure Government-spezifische Azure-Abonnements unterstützt.

## <a name="features-that-arent-available"></a>Nicht verfügbare Funktionen

Einige Funktionen stehen nicht für die Bereitstellung in GCC zur Verfügung oder können nicht mit Dynamics 365 in GCC verwendet werden. Zum Beispiel werden Azure DevOps-Dienste in GCC nicht verfügbar sein. Allerdings können lokale Azure DevOps oder öffentliche Azure DevOps-Dienste genutzt werden. Ausführliche Informationen zur Verfügbarkeit von Funktionen finden Sie unter [Verfügbarkeit von Geschäftsanwendungen für US-Regierung](https://aka.ms/BAPFunctionalParity).

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="are-dynamics-365-finance-and-dynamics-365-supply-chain-management-supported-in-gcc-high"></a>Werden Dynamics 365 Finance und Dynamics 365 Supply Chain Management in GCC-High unterstützt?

Nein Werden Dynamics 365 Finance und Dynamics 365 Supply Chain Management nur in GCC unterstützt?

### <a name="can-i-use-public-azure-devops-with-finance-and-supply-chain-management-in-gcc"></a>Kann ich öffentliche Azure DevOps mit Finance und Supply Chain Management in GCC verwenden?

Ja, Sie können öffentliche Azure DevOps-Services verwenden, wenn Sie keine Anforderungen an eine vom Federal Risk and Authorization Management Program (FEDRAMP) zertifizierte Lösung haben. Alternativ können Sie Azure DevOps Server verwenden.

### <a name="can-i-deploy-a-cloud-hosted-environment-tier-1-development-environment-on-an-azure-commercial-subscription"></a>Kann ich eine Stufe-1-Entwicklungsumgebung einer cloud-gehosteten Umgebung mit einem Azure Commercial-Abonnement bereitstellen?

Nein In [LCS für GCC](https://gov.lcs.microsoftdynamics.us) müssen Sie ein Azure Government-Abonnement verwenden, um eine in der Cloud gehostete Umgebung bereitzustellen.

### <a name="what-can-i-do-if-i-need-a-package-from-the-shared-asset-library-but-it-isnt-available-in-lcs-for-gcc"></a>Was kann ich tun, wenn ich ein Paket aus der Shared Asset Library benötige, dieses aber nicht in LCS für GCC verfügbar ist?

Sie können das gleiche Paket aus der Shared Asset Library in [öffentlichen LCS](https://lcs.dynamics.com) herunterladen. Alternativ kann Ihnen Ihr Partner beim Herunterladen des Pakets helfen.

### <a name="is-the-code-upgrade-tool-available-in-gcc"></a>Ist das Code-Upgrade-Tool in GCC verfügbar?

Nein, das Code-Upgrade-Tool ist derzeit nicht in GCC verfügbar. Sie können jedoch ein potenzielles Projekt in [öffentlichen LCS](https://lcs.dynamics.com) erstellen und das Code-Upgrade-Tool verwenden. Beachten Sie, dass Sie in potenziellen Projekten keine Umgebungen bereitstellen können.

### <a name="can-my-partner-open-a-support-ticket-on-my-behalf"></a>Kann mein Partner in meinem Namen ein Support-Ticket eröffnen?

Ja. Wenn Ihr Partner jedoch eine Nicht-GCC-Identität verwendet, wird das Support-Ticket an die öffentliche Support-Warteschlange weitergeleitet. Wir empfehlen, dass Sie die GCC-Berechtigung des Kunden in LCS verwenden, um Support-Tickets zu öffnen.

## <a name="see-also"></a>Siehe auch

- [Dynamics 365 US Government](/power-platform/admin/microsoft-dynamics-365-government)
- [Verfügbarkeit von Geschäftsanwendungen für US-Regierung](https://aka.ms/BAPFunctionalParity).
- [Lifecycle Services (LCS)-Benutzerhandbuch](../../../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Cloudbereitstellung – Übersicht](../../../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
