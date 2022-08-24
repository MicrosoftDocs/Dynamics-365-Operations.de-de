---
title: Bereitstellung von Human Resources in der Finanzen und Betrieb-Infrastruktur
description: Dieser Artikel erläutert den Prozess der Bereitstellung einer neuen Produktionsumgebung für Microsoft Dynamics 365 Human Resources in der Finanzen und Betrieb-Infrastruktur.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2fd8176d16178ecc4ba667e5937f2cec2e0af2c3
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/03/2022
ms.locfileid: "9221591"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Bereitstellung von Human Resources in der Finanzen und Betrieb-Infrastruktur

_**Gilt für:** Human Resources auf der Infrastruktur der Finanz- und Betriebs-App_ 

> [!NOTE]
> Ab Juli 2022 können neue Human Resources Umgebungen nicht mehr in der eigenständigen Human Resources Infrastruktur bereitgestellt werden und neue Microsoft Dynamics Lifecycle Services (LCS) Projekte können dort nicht mehr erstellt werden. Debitor kann Human Resources Umgebungen in der Finanzen und Betrieb Infrastruktur bereitstellen.

Dieser Artikel erläutert den Prozess der Bereitstellung einer neuen Produktionsumgebung für Microsoft Dynamics 365 Human Resources in der Finanzen und Betrieb-Infrastruktur.

## <a name="prerequisites"></a>Voraussetzungen

Bevor Sie mit der Bereitstellung einer neuen Umgebung beginnen, müssen die folgenden Voraussetzungen gegeben sein:

- Sie haben Human Resources über einen Cloud Solution Provider (CSP) oder einen Enterprise Architecture (EA) Vertrag gekauft. Wenn Sie eine bestehende Dynamics 365-Lizenz haben, die bereits den Serviceplan Human Resources enthält, und Sie die Schritte in diesem Artikel nicht ausführen können, wenden Sie sich an den Support.
- Der globale Administrator hat sich bei [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) angemeldet und ein neues Finanzen und Betrieb Projekt erstellt.

## <a name="provision-a-human-resources-trial-environment"></a>Bereitstellen einer Human Resources-Testumgebung

> [!NOTE]
> Ab April 2022 werden die Test-Umgebungen für Human Resources nicht mehr in der Standalone-Anwendung verfügbar sein. Potenzielle Debitor, die die Funktionalitäten von Human Resources in Finanz- und Betriebs-Apps testen möchten, können den kostenlosen 30-tägigen Test zusammen mit den Demodaten nutzen. Dynamics 365 Finance wird die Funktionalitäten für Human Resources enthalten, die durch die Zusammenführung der eigenständigen Anwendung in die Finance-Infrastruktur eingebracht werden. Weitere Informationen finden Sie unter [Zusammenführung von HR-Angeboten führt Funktionalitäten für Debitor zusammen](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers). Weitere Informationen über Dynamics 365 Finance Tests finden Sie in der [Schritt-für-Schritt Anleitung](../fin-ops-core/fin-ops/get-started/before-you-buy.md).

## <a name="plan-human-resources-environments"></a>Human Resources-Umgebungen planen

Bevor Sie Ihre erste Human Resources-Umgebung erstellen, sollten Sie die Umgebungsanforderungen für Ihr Projekt sorgfältig planen. Ein Basis-Abonnement für Human Resources umfasst zwei Umgebungen: eine Produktionsumgebung und eine Standardumgebung für Akzeptanztests (Sandbox). Je nach Komplexität Ihres Projekts haben Sie die Möglichkeit, zusätzliche Umgebungen zur Unterstützung der Projektaktivitäten zu kaufen.

Hier finden Sie einige Überlegungen für zusätzliche optionale Umgebungen:

- **Datenmigration** – Die Aktivitäten zur Datenmigration ermöglichen es, Ihre Sandbox-Umgebung während des gesamten Projekts zu Testzwecken zu nutzen. Wenn Sie über eine zusätzliche Umgebung verfügen, können die Aktivitäten zur Datenmigration fortgesetzt werden, während die Test- und Konfigurationsaktivitäten gleichzeitig in einer anderen Umgebung stattfinden.
- **Integration** – Konfigurieren und testen Sie Integrationen, die native Integrationen oder angepasste Integrationen umfassen können, z.B. für die Gehaltsabrechnung, Bewerberverfolgungssysteme oder Leistungssysteme und -anbieter.
- **Schulung** – Möglicherweise benötigen Sie eine separate Umgebung, die mit einem Satz von Schulungsdaten festgelegt ist, damit Sie Ihre Mitarbeiter in der Verwendung des neuen Systems schulen können. 
- **Mehrphasiges Projekt** – Möglicherweise benötigen Sie eine zusätzliche Umgebung, um die Konfiguration, die Datenmigration, das Testen oder andere Aktivitäten in einer Projektphase zu unterstützen, die nach dem ersten Go-Live des Projekts geplant ist.
- **Entwicklung** – In der Infrastruktur von Finanzen und Betrieb können Sie die Lösung jetzt erweitern und Ihre eigenen Anpassungen entwickeln. Jeder Entwickler muss seine eigene Entwicklungsumgebung verwenden. Weitere Informationen finden Sie unter [Entwicklungsumgebungen bereitstellen und darauf zugreifen](../fin-ops-core/dev-itpro/dev-tools/access-instances.md).
- **GOLD** – Bei neuen Bereitstellungen ist es allgemein üblich, eine separate GOLD-Umgebung zu verwenden, die für die Konfiguration und Datenmigration unberührt bleibt. Diese Umgebung kann während der gesamten Implementierung verwendet werden, um andere Umgebungen zu aktualisieren. Es wird verwendet, um die neue Produktionsumgebung zu erstellen, die die Basiskonfiguration und die Datenmigration enthält. Sie können keine produktive Umgebung auf der Finanzen und Betrieb-Infrastruktur bereitstellen, bevor Sie die Bereitschaft zum Go-Live abgeschlossen haben. Weitere Informationen finden Sie unter [Vorbereiten auf den Start](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md).

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Wenn Sie über Ihre Umgebung nachdenken, empfehlen wir Ihnen den folgenden Ansatz:
>
> - Verwenden Sie Ihre Standard-Akzeptanztest-Umgebung (früher Sandbox-Umgebung) oder eine andere Umgebung, um vor dem Go-Live einen Mock-Cutover durchzuführen.
> - Führen Sie eine detaillierte Cutover-Checkliste, die alle Datenpakete enthält, die für die Migration der endgültigen Daten in die Produktionsumgebung während des Go-Live-Cutovers erforderlich sind. Diese Empfehlung ist besonders wichtig, wenn Sie keine separate GOLD Umgebung haben, um Ihre Konfigurationen zu speichern.
> - Verwenden Sie Ihre Standardumgebung für Akzeptanztests (früher Sandbox-Umgebung) oder eine andere Umgebung der Stufe 2 oder höher als TEST-Umgebung für Ihr gesamtes Projekt. Wenn Sie zusätzliche Umgebungen benötigen, kann Ihr Unternehmen diese zu zusätzlichen Kosten kaufen.

## <a name="create-an-lcs-project"></a>LCS Projekt erstellen

Um LCS für die Human Resources-Umgebung zu verwalten, müssen Sie zuerst ein LCS-Projekt erstellen. Wenn Sie Ihre Human Resources Umgebung in die Finanzen und Betrieb Infrastruktur migrieren, müssen Sie ein neues LCS Projekt für Finanz- und Betriebs-Apps erstellen. Wenn Sie bereits ein LCS Projekt für andere Finanz- und Betriebs-Apps haben, können Sie die Funktionen für Human Resources im Arbeitsbereich **Funktionsverwaltung** aktivieren. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Wenn sich ein neuer Debitor für Human Resources anmeldet, enthält das Abonnement einen Arbeitsbereich für die Implementierung. Nachdem der Debitor den Dienst aktiviert hat, muss sich der Mandant-Administrator bei <https://lcs.dynamics.com> mit seinem Mandant-Konto anmelden. Der Arbeitsbereich des Projekts wird automatisch für die Organisation erstellt. Weitere Informationen finden Sie unter [Lifecycle Services (LCS) für Finanz- und Betriebs-Apps Debitor](../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md).

> [!NOTE]
> Um eine erfolgreiche Bereitstellung zu gewährleisten, muss das Konto, das Sie für die Bereitstellung der Umgebung Human Resources verwenden, entweder der Rolle **Systemadministrator** oder der Rolle **Systemanpasser** in der Power Apps-Umgebung zugewiesen sein, die mit der Umgebung Human Resources verbunden ist. Weitere Informationen darüber, wie Sie Benutzern in Microsoft Power Platform Sicherheitsrollen zuweisen, finden Sie unter [Benutzersicherheit für Ressourcen konfigurieren](/power-platform/admin/database-security).

Bevor Sie mit dem Bereitstellen von Umgebungen beginnen können, müssen Sie den Onboarding-Prozess für LCS-Projekte abschließen. Weitere Informationen finden Sie unter [Projekt-Einführung](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md). Weitere Informationen über die Verwendung von LCS finden Sie in der [Lifecycle Services (LCS) Anleitung](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md).

## <a name="deploy-human-resources-environments"></a>Bereitstellen von Umgebungen für Human Resources

Die Bereitstellung von Finanz- und Betriebs-Apps, einschließlich Human Resources, in der Cloud erfordert, dass Sie die Umgebung und das Abonnement verstehen, in dem Sie die App bereitstellen, wer welche Aufgaben ausführen darf und welche Daten und Anpassungen Sie verwalten müssen. Wir empfehlen Ihnen, beim Bereitstellen neuer Umgebungen ein Dienstkonto anstelle eines benannten Benutzers zu verwenden. Weitere Informationen über das Bereitstellen von Umgebungen in der Finanzen und Betrieb-Infrastruktur finden Sie unter [Übersicht über die Cloud-Bereitstellung](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview).

Um eine produktive Umgebung für Human Resources in der Finanzen und Betrieb-Infrastruktur bereitzustellen, müssen Sie den Prozess der Bereitschaft für den Produktivstart abschließen. Weitere Informationen finden Sie unter [Vorbereiten auf den Start](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md). Dieser Prozess umfasst den Abonnement-Schätzer in LCS. Weitere Informationen finden Sie unter [Abonnement-Schätzer](../fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator.md).

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Integration von Microsoft Power Platform mit Human Resources

Microsoft Power Platform bietet eine Reihe von Funktionalitäten für Dynamics 365-Anwendungen über das Admin Center Power Platform. Mit Microsoft Power Platform können Sie die Nutzung von Human Resources Daten integrieren und erweitern. Informationen über die Integration von Human Resources mit Microsoft Power Platform finden Sie unter [Microsoft Power Platform Integration mit Finanz- und Betriebs-Apps](../fin-ops-core/dev-itpro/power-platform/overview.md).

## <a name="supported-geographies"></a>Unterstützte Geografien

Informationen zu den Sprachen und Regionen, die für Human Resources unterstützt werden, finden Sie unter [Global by design: Erfahren Sie mehr über unterstützte Länder und Sprachen](https://dynamics.microsoft.com/availability-reports/).

## <a name="grant-access-to-the-environment"></a>Zugriff auf die Umgebung gewähren

Standardmäßig besitzt nur der globale Administrator, von dem Enterprise Portal installiert wurde, Zugriff auf diese Anwendung. Allerdings muss zusätzliche Bewerbungsbenutzern explizit Zugriff gewährt werden. Um Zugriff zu gewähren, müssen Sie Benutzer hinzufügen und ihnen die entsprechenden Rollen in der Human Resources-Umgebung zuweisen. Weitere Informationen finden Sie unter [Neue Benutzer erstellen](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) und [Weisen Sie Benutzer Sicherheitsrollen zu](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Zusätzliche Ressourcen
In den folgenden Ressourcen erfahren Sie mehr über die Verwendung und Verwaltung von Projekten in LCS auf der Finanz- und Betriebs-App-Infrastruktur:

- [Lifecycle Services-Ressourcen](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Lifecycle Services (LCS)-Benutzerhandbuch](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Self-Service-Bereitstellung – Übersicht](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Startseite für Vorgänge der Datenbankbewegung](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
