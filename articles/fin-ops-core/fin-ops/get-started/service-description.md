---
title: Servicebeschreibung für Finanz- und Betriebs-Apps
description: Dieses Thema enthält die Servicebeschreibung für Finanz- und Betriebs-Apps.
author: tomhig
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: whigginb
ms.search.validFrom: 2021-09-03
ms.openlocfilehash: cd033cfc3df21ddac5572aa70c18db5ffe26f54e
ms.sourcegitcommit: 0abc777986112ea2332f5bf0e815b303b952356c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2022
ms.locfileid: "8656802"
---
# <a name="service-description-for-finance-and-operations-apps"></a>Servicebeschreibung für Finanz- und Betriebs-Apps

[!include[banner](../includes/banner.md)]

Finanz- und Betriebs-Apps sind Enterprise Resource Planning (ERP) Software-as-a-Service (SaaS) Angebote, die auf und für [Microsoft Azure](https://azure.microsoft.com/overview/what-is-azure/) erstellt wurden. Der Finanz- und Betriebs-App-Service bietet Unternehmen ERP-Funktionalität, die ihre individuellen Anforderungen unterstützt und ihnen hilft, sich an sich ständig ändernde Geschäftsumgebungen anzupassen, ohne dass sie die Infrastruktur verwalten müssen. Finanz- und Betriebs-Apps können einen oder mehrere der folgenden Lösungsbereiche umfassen:

- [Dynamics 365 Finance](/dynamics365/finance/)
- [Dynamics 365 Human Resources](/dynamics365/human-resources/)
- [Dynamics 365 Supply Chain Management](/dynamics365/supply-chain/)
- [Dynamics 365 Commerce](/dynamics365/commerce/)
- [Dynamics 365 Project Operations](/dynamics365/project-operations/)

Zusammen mit [Business Intelligence](/power-bi/fundamentals/power-bi-service-overview), [Infrastruktur](https://azure.microsoft.com/global-infrastructure/), [Computer](/azure/service-fabric/service-fabric-overview), und [Datenbankdienste](https://devblogs.microsoft.com/azure-sql/running-1m-databases-on-azure-sql-for-a-large-saas-provider-microsoft-dynamics-365-and-power-platform/), ermöglichen diese Apps Unternehmen die Ausführung branchenspezifischer und operativer Geschäftsprozesse. Mit Unterstützung ihres Implementierungspartners bestimmen Kunden die Konfiguration der Geschäftsanwendungslogik, die am besten zu ihren individuellen Geschäftsprozessen passt. Funktionalität und Geschäftsprozesse können durch eine oder eine Kombination der folgenden Lösungen erweitert oder erweitert werden:

- Erstellt in [Personalisierungserfahrung](personalize-user-experience.md)
- [Microsoft Power Platform](../../dev-itpro/power-platform/overview.md)-Tools
- [Visual Studio](https://visualstudio.microsoft.com)-basierend [Finanz- und Betriebs-Softwareentwicklungskit (SDK)](../../dev-itpro/dev-tools/developer-home-page.md) und [Azure DevOps Build-Automatisierung](../../dev-itpro/dev-tools/developer-home-page.md#build-automation-using-azure)
- Unabhängige Software Vendor (ISV)-Lösungen von [AppSource](https://appsource.microsoft.com/partners)

Basierend auf den Anforderungen wählen Kunden ihren Lösungsansatz. Sie arbeiten mit ihrem Implementierungspartner zusammen, um ihre Lösung zu definieren, zu entwickeln und zu testen, indem sie die Tools und Best Practices verwenden, die in [Microsoft Dynamics Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md) bereitgestellt werden. Es gibt vier gängige Szenarien:

- Finanz- und Betriebs-Apps-Standardkonfiguration (keine Erweiterungen)
- Finanz- und Betriebs-Apps-Konfiguration, die eine oder mehrere ISV-Lösungen umfasst
- Finanz- und Betriebs-Apps-Konfiguration, die eine oder mehrere kundenspezifische Erweiterungen enthält
- Finanz- und Betriebs-Apps-Konfiguration, die eine Kombination aus kundenspezifischen Erweiterungen und einer oder mehreren ISV-Lösungen enthält

Unternehmen können ihr Geschäftswachstum durch einfaches Hinzufügen von Benutzern und Geschäftsprozessen über ein einfaches, transparentes Abonnementmodell anpassen. Weitere Informationen finden Sie im [Dynamics 365-Lizenzierungshandbuch](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365).

## <a name="operating-model"></a>Betriebsmodell

Das Betriebsmodell von Finanz- und Betriebs-Apps definiert spezifische Rollen und Verantwortlichkeiten für den Kunden, den Implementierungspartner und Microsoft während des gesamten Lebenszyklus des Dienstes. Weitere Informationen finden Sie unter [Cloud-Betrieb und -Service](../../dev-itpro/lifecycle-services/cloud-operations-servicing.md).

### <a name="customer-activities"></a>Benutzerdefinierte Aktivitäten

Kunden arbeiten mit ihrem Partner und [Microsoft FastTrack](/dynamics365/fasttrack/) nach dem [Dynamics 365-Implementierungshandbuch](https://community.dynamics.com/365/dynamics-365-fasttrack/p/dynamics365implementationguide), dem [Success by Design](/dynamics365/fasttrack/success-by-design-overview)-Framework und nutzen Tools und Best-Practice-Vorlagen in [Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md), um ihre Lösung umzusetzen. Zu den gemeinsamen Aktivitäten gehören:

- Benutzeridentitäts- und Sicherheitsmanagement
- Geschäftsprozesse definieren, entwickeln und betreiben
- Erweiterungen definieren, entwickeln, testen und betreiben
- Überwachen und verwalten Sie nicht produktive Bereitstellungen
- Anwendungsupdates verwalten und Erweiterungen validieren
- Verwalten Sie ISV-Lösungen und Integrationen von Drittanbietern

### <a name="microsoft-responsibilities"></a>Microsoft-Aufgaben

Microsoft verwaltet den Finanz- und Betriebs-App-Dienst durch Bereitstellung, aktive Überwachung und Wartung von Sandbox- und Produktionsumgebungen von Kunden im Microsoft SaaS-Abonnement. Diese Verwaltung umfasst die Zuweisung der erforderlichen Systeminfrastruktur, um den Dienst auszuführen und proaktiv mit Kunden über den Zustand des Dienstes zu kommunizieren. Zu den Aufgaben gehören:

**Infrastrukturmanagement**
- Sicherheit und Isolation
- Betriebssysteme und Virtualisierung
- Server, Speicher und Netzwerke
- Stromversorgung, Netzwerk, Kühlung für Rechenzentren

**Anwendungsplattformverwaltung**
- Anwendungsüberwachung und Benachrichtigungen rund um die Uhr
- Diagnose, Plattform-Updates, Patches, Service-Updates
- Anwendungsrouting, Lastenausgleich, Standortreplikation
- Umgebungsbereitstellung und -verwaltung
- Datenbankverwaltung, hohe Verfügbarkeit (HA)/Disaster Recovery (DR), Skalierung, Betrieb
- Compute-Bereitstellung, Hochskalieren, Herunterskalieren

## <a name="system-configuration"></a>Systemkonfiguration

Finanz- und Betriebs-Apps skalieren entsprechend dem Transaktionsvolumen und der Benutzerbelastung. Jede Kundenimplementierung erzeugt eine einzigartige Lösung, die aus den folgenden Elementen besteht:

- **Datenzusammenstellung** – Ein einzigartiger Satz von Parametern, die das Verhalten, das Layout der Organisation, die Struktur der Stammdaten (wie Finanz- und Bestandsdimensionen) und die Granularität der Transaktionsverfolgung steuern.
- **Erweiterung und Konfiguration** – Erweiterungsmechanismen, die Codeerweiterungen, ISV-Lösungen und einzigartige Konfigurationen verwenden, die Workflows, Integrationen und Berichtskonfigurationen umfassen.
- **Nutzungsmuster** – Eine einzigartige Kombination aus Online- und Batch-Nutzung, zusammen mit der Möglichkeit der Integration mit vor- und nachgelagerten Systemen für einen einheitlichen Datenfluss und der Möglichkeit, basierend auf den Informationsansichten zu differenzieren, die Kunden in ihren Geschäftsprozessen verwenden.

Microsoft konfiguriert Kundenproduktionsumgebungen, die so dimensioniert sind, dass sie das Transaktionsvolumen und die Benutzergleichzeitigkeit verarbeiten. Microsoft ist für die folgenden Aufgaben verantwortlich:

- Korrekte Zuweisung der Ressourcen von Produktionsumgebungen, basierend auf den Profiling-Informationen des Kunden im [LCS-Abonnementkalkulator](../../dev-itpro/lifecycle-services/subscription-estimator.md)
- Kontinuierliche Überwachung und Diagnose der Serviceverfügbarkeit von Produktionsumgebungen
- Analysieren und Beheben von Systemleistungsproblemen mit Finanz- und Betriebs-Apps

Um sicherzustellen, dass eine Implementierung für hohe Leistung konfiguriert ist, müssen Kunden die folgenden Aufgaben ausführen:

- Geben Sie genaue Nutzungsinformationen über die Finanz- und Betriebs-App-Umsetzung im [LCS-Abonnementkalkulator](../../dev-itpro/lifecycle-services/subscription-estimator.md).
- Erstellen und testen Sie Erweiterungen für Leistung und Skalierbarkeit.
- Testen Sie die Datenkonfigurationen entsprechend auf Leistung.
- Skalierbarkeit durch [Leistungstest](https://community.dynamics.com/365/b/techtalks/posts/performance-testing-approach-april-30-2018) vor der Veröffentlichung sicherstellen.

## <a name="onboarding-and-implementation"></a>Onboarding und Implementierung

Die folgende Tabelle zeigt typische Onboarding- und Implementierungsereignisse.

| Anforderung | Erwartete Microsoft-Aktion | Erwartete Aktion des Kunden/Implementierungspartners |
|---|---|---|
| Erstangebotskauf | Ein LCS-Projekt wird nach dem Kauf des Angebots basierend auf einem vom Kunden ausgelösten Ereignis erstellt. | Gehen Sie durch den Enterprise Agreement (EA) oder Cloud Solution Provider (CSP) [kommerziellen Prozess](before-you-buy.md). Der Partner erstellt ggf. einen Mandant für den Kunden. |
| Zusatzkauf | Gewähren Sie dem Kunden Zugriff auf das Add-On, das während der Implementierung ausgewählt wird. | Nicht zutreffend |
| Ausführungsplanung und -analyse | Stellen Sie relevante Tools in LCS bereit, wie [Geschäftsprozessmodellierer (BPM)](../../dev-itpro/lifecycle-services/bpm-overview.md) und [Interoperabilität mit Azure DevOps](../../dev-itpro/lifecycle-services/synchronize-bpm-vsts.md). | Projektplanung machen, einrichten von Azure DevOps, das System-Onboarding abschließen und Administratorkonten einrichten. |

Weitere Informationen finden Sie unter [Onboarding eines Implementierungsprojekts](../imp-lifecycle/onboard.md).

## <a name="globalization"></a>Globalisierung

Finanz- und Betriebs-Apps werden aus mehreren Azure-Regionen auf der ganzen Welt bereitgestellt. Finanz- und Betriebs-Apps bieten Funktionen zur Unterstützung verschiedener Länder/Regionen und Muttersprachen. Weitere Informationen finden Sie unter [Lokalisierungs- und Regulierungsfunktionen](../../dev-itpro/lcs-solutions/country-region.md#localization-and-regulatory-features).

### <a name="countryregion-specific-considerations"></a>Landes-/regionsspezifische Betrachtungen

- Kunden in regulierten Branchen oder kommerziellen Organisationen, die mit Unternehmen in Frankreich Geschäfte machen, die eine lokale Datenresidenz erfordern, sollten [Finanzen und Betriebe in Frankreich](../../dev-itpro/deployment/france-local-deployment.md) lesen.
- Kunden, die in China tätig sind, sollten [Azure China Playbook](/azure/china/) und [Finanzen und Betriebe betrieben von 21Vianet in China](../../dev-itpro/deployment/china-local-deployment.md) überprüfen.
- Kunden, die in Russland tätig sind, sollten das [Russisches Gesetz zur Lokalisierung personenbezogener Daten](/business-applications-release-notes/october18/dynamics365-finance-operations/russian-regulations-on-prem#when-will-the-cloud-deployment-option-of-dynamics-365-for-finance-and-operations-be-generally-available-for-russia) überprüfen.

### <a name="general-data-protection-regulation-gdpr"></a>Datenschutz-Grundverordnung (DSGVO)

Für Finanz- und Betriebs-Apps fungiert Microsoft als Auftragsverarbeiter. Als Datenverarbeiter bietet Finanz- und Betriebs-App Prozesse und Funktionen, die Kunden dabei helfen, die DSGVO-Verpflichtungen als Datenverantwortlicher einzuhalten. Weitere Informationen finden Sie unter [DSGBO Überblick](../../dev-itpro/gdpr/gdpr-guide.md).

## <a name="environment-and-data-management"></a>Umgebung und Datenverwaltung

In diesem Abschnitt werden einige typische Umgebungs- und Datenverwaltungsereignisse beschrieben, die im Dienst auftreten.

### <a name="environment-and-data-management-events-for-production-instances"></a>Umgebungs- und Datenverwaltungsereignisse für Produktionsinstanzen

LCS bietet [Self-Service-Tools](../../dev-itpro/deployment/infrastructure-stack.md) und [Datenbankverschiebungsvorgänge](../../dev-itpro/database/dbmovement-operations.md), die zur Ausführung von Umgebungs- und Datenverwaltungsaufgaben verwendet werden. Im Folgenden finden Sie einige Beispiele hierfür:

**Ereignisl:** [Anfordern einer Produktionsinstanz](../imp-lifecycle/prepare-go-live.md#requesting-the-production-environment)

- Vervollständigen Sie die [Go-Live-Checkliste](../imp-lifecycle/prepare-go-live.md) und senden Sie sie an das [Microsoft FastTrack](/dynamics365/fasttrack/) Team.
- Vervollständigen Sie das [LCS-Abonnement Kalkulation](../../dev-itpro/lifecycle-services/subscription-estimator.md), bevor Sie eine Produktionsinstanz anfordern.
- Führen Sie alle Implementierungsaufgaben aus, die in der [LCS-Methodik](../../dev-itpro/lifecycle-services/create-methodology.md) definiert sind.

**Ereignis:** [Kopieren einer Sandbox-Datenbank in eine Produktionsinstanz](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Wird für einen simulierten Go-Live oder einen tatsächlichen Go-Live-Cutover durchgeführt.

**Ereignis:** [Wartungsmodus](../../dev-itpro/sysadmin/maintenance-mode.md)

1. Schalten Sie den Wartungsmodus in LCS ein.
2. Führen Sie die erforderlichen Wartungsarbeiten durch.
3. Schalten Sie den Wartungsmodus in LCS aus.

### <a name="environment-and-data-management-events-for-non-production-instances"></a>Umgebungs- und Datenverwaltungsereignisse für Nicht-Produktionsinstanzen

LCS bietet [Self-Service-Bereitstellung](../../dev-itpro/deployment/infrastructure-stack.md) und [Datenbankverschiebungsvorgänge](../../dev-itpro/database/dbmovement-operations.md), die zur Ausführung von Umgebungs- und Datenverwaltungsaufgaben verwendet werden. Im Folgenden finden Sie einige Beispiele hierfür:

**Ereignis:** [Bereitstellen einer neuen Sandbox-Instanz](../../dev-itpro/deployment/deployenvironment-newinfrastructure.md)

- Stellen Sie sicher, dass alle erforderlichen Instanzen [geplant](../imp-lifecycle/environment-planning.md) sind und dass die entsprechenden Zusatzangebote erworben wurden.
- Führen Sie den Bereitstellungsprozess in LCS aus.
- Führen Sie alle Implementierungsaufgaben aus, die in der LCS-Checklisten definiert sind.
    
>[!NOTE]
>Eine Entwicklungs-Sandbox-Umgebung ist eine virtuelle Maschine (VM), die [im Azure-Abonnement des Kunden bereitgestellt](../../dev-itpro/dev-tools/access-instances.md) und vom Kunden verwaltet wird.

**Ereignis:** [Kopieren einer goldenen Konfigurations-Datenbank von einer Sandbox zu einer Produktionsinstanz](../../dev-itpro/database/dbmovement-scenario-goldenconfig.md)

- Wird für einen simulierten Go-Live oder einen tatsächlichen Go-Live-Cutover durchgeführt.

**Vorfall:** [Wiederherstellen eines Produktions-Point-in-Time-Backups auf einer Nicht-Produktionsinstanz](../../dev-itpro/database/database-pitr-prod-sandbox.md)

- Führen Sie die [Datenbank aktualisieren](../../dev-itpro/database/database-refresh.md) Option in LCS durch.
- Nach dem Kopieren: Löschen oder verschleiern Sie sensible Daten über Skripts, passen Sie Umgebungsspezifische Anwendungskonfigurationen (z. B. Integrationsendpunkte) an und aktivieren oder fügen Sie Benutzer hinzu. Beachten Sie, dass diese Änderungen durch Anwenden von einem [Datenpaket](../../dev-itpro/data-entities/data-entities-data-packages.md#import-a-data-package) angewendet werden.

**Ereignis:** [Wiederherstellung nach Zeitpunkt der Nichtproduktionsinstanz-Datenbank](../../dev-itpro/database/database-point-in-time-restore.md)

- Akzeptieren Sie, dass der Vorgang nicht rückgängig gemacht werden kann.
- Führen Sie den Point-in-Time-Wiederherstellungsvorgang in LCS aus.

**Ereignis:** Kopieren einer Tier-2-Sandbox-Datenbank in eine Entwicklungs-Sandbox zur Fehlerbehebung und zum [Debuggen](../../dev-itpro/database/dbmovement-scenario-debugdiag.md)

- Führen Sie den Datenbankexportvorgang in LCS in der Tier-2-Sandbox-Umgebung aus.
- Importieren und aktualisieren Sie die Datenbank in der Entwicklungsumgebung.

## <a name="data-backup-and-retention"></a>Datensicherung und -Aufbewahrung

Datenbanken für Finanz- und Betriebs-App-Umgebungen im SaaS-Abonnement werden durch automatische Backups geschützt. In Produktionsumgebungen werden automatische Backups 28 Tage lang aufbewahrt, es sei denn, Microsoft führt ein Rollback durch. In Sandbox-Umgebungen (Tier 2+) werden sie sieben Tage lang aufbewahrt. Ein Rollback der Produktionsumgebung kann durchgeführt werden, wenn während eines geplanten Wartungsupdates ein Fehler auftritt.

Weitere Informationen zu automatischen Backups finden Sie unter [Automatisierte Sicherungen – Azure SQL-Datenbank und verwaltete SQL-Instanz](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).

## <a name="service-activity-responsibilities"></a>Serviceaktivitätstypen-Verantwortlichkeiten

In der folgenden Tabelle werden einige typische Szenarien und Aktivitäten für den Dienst beschrieben. Es zeigt auch an, ob Microsoft, der Kunde oder sowohl Microsoft als auch der Kunde für die Aktivitäten verantwortlich sind.

| Aktivität | Zuständigkeit von Microsoft | Zuständigkeit der Kunden |
|---|---|---|
| **Bereitstellung von Erstmandanten** | | |
| Bestimmen Sie die prognostizierte Last in LCS mithilfe des Abonnement Kalkulationstools und fordern Sie die Bereitstellung bestimmter Umgebungen an. | | X |
| Stellen Sie alle Produktionsinstanzen und Nichtproduktionsinstanzen bereit. | X | |
| Validieren Sie die bereitgestellten Produktionsinstanzen und Nichtproduktionsinstanzen bereit. | | X |
| **Dienstupdates** | |
| Wenden Sie Dienstupdates auf bestimmte Nicht-Produktions- und Produktionsinstanzen an. | X | |
| Wenden Sie Dienstaktualisierungen von LCS manuell auf Sandbox-Instanzen an. Definieren, entwickeln, testen Sie das Update, und stellen Sie das Code-Update-Paket wieder an LCS bereit. | | X |
| Fordern Sie an, dass Erweiterungsupdates auf die Produktionsinstanz angewendet werden, und planen Sie sie. | | X |
| Erstellen Sie eine Code- und Datensicherung für die Produktionsinstanz, bevor Updates angewendet werden. | X | |
| Falls ein Fehler auftritt, setzen Sie die Produktionsinstanz auf die Code- und Datensicherung zurück. | X | |
| **Datenverwaltung (Sichern, Wiederherstellen und Aktualisieren)** | | |
| Sichern Sie die Datenbank. | X | |
| Bestimmen Sie hohe Verfügbarkeit und einen Notfallwiederherstellungsplan. | X | |
| Überwachen Sie die Leistung der Produktionsinstanzdatenbank. | X | |
| Steuern Sie die Leistung der Produktionsinstanzdatenbank. | X | |
| Führen Sie eine Point-in-Time-Aktualisierung der Produktionsinstanzdatenbank auf eine Nicht-Produktionsinstanz durch. | | X |
| **Aktualisierung der Infrastruktur** | | |
| Planen Sie regelmäßige Infrastruktur-Updates. | X | |
| **Hoch- und Runterskalieren (Benutzer, Speicher und Instanzen)** | | |
| Erwerben Sie zusätzliche Benutzer und nicht produktive Add-Ons. | | X |
| Aktualisieren Sie Nutzungsänderungen im LCS Subscription Estimator-Tool. | | X |
| Melden Sie alle wesentlichen Leistungsprobleme, die sich auf die Nutzung des Dienstes auswirken. | | X |
| Verwalten Sie proaktiv die Ressourcen, die für den jeweiligen Dienst erforderlich sind. | X | |
| Untersuchen und beheben Sie Vorfälle. | X | |
| **Sicherheit (Benutzerzugriff)** | | |
| Gewähren Sie Benutzerzugriff auf den Dienst. | | X |
| Bieten Sie LCS-Projektzugriff für die Verwaltung und den Betrieb von Instanzen, die über LCS bereitgestellt wurden. | | X |
| **Produktionsinstanzen überwachen** | | |
| Produktionsinstanzen rund um die Uhr überwachen. | X | |
| Benachrichtigen Sie den Kunden proaktiv über Vorfälle, die die Produktionsinstanz betreffen. | X | |
| **Nicht-Produktionsinstanzen verwalten und überwachen** | | |
| Verwalten Sie Nicht-Produktionsinstanzen mithilfe von LCS. | | X |
| Nicht-Produktionsinstanzen überwachen. | | X |

## <a name="service-update-strategy"></a>Dienstupdatestrategie

Gemäß der [Software-Lebenszyklusrichtlinie](../../dev-itpro/migration-upgrade/versions-update-policy.md) folgen Finanz- und Betriebs-Apps der Microsoft [Richtlinie für den modernen Lebenszyklus](../../dev-itpro/migration-upgrade/versions-update-policy.md#modern-lifecycle-policy), die Produkte abdeckt, die kontinuierlich gewartet und unterstützt werden. 

Microsoft veröffentlicht jährlich acht Serviceupdates für Finanz- und Betriebs-Apps in den folgenden Monaten:

- Januar
- Februar
- April
- Mai
- Juli
- August
- Oktober
- November

>[!NOTE]
>April und Oktober sind große Funktions-Veröffentlichungszyklen. Kunden können ein einzelnes Service-Update für bis zu drei aufeinanderfolgende Update-Zyklen pausieren.

Für weitere Informationen überprüfen Sie die folgenden Themen:

- [Übersicht über Dienstupdates für One Version](../../dev-itpro/lifecycle-services/oneversion-overview.md)
- [Dienstupdates über LCS konfigurieren](../../dev-itpro/lifecycle-services/configure-service-updates.md)
- [Dienstupdates über LCS anhalten](../../dev-itpro/lifecycle-services/pause-service-updates.md)
- [Benachrichtigungen zu Dienstupdates über LCS erhalten](../../dev-itpro/lifecycle-services/notifications-service-updates.md)
- [Regressionstesttools zur Validierung von Serviceupdates](../../dev-itpro/perf-test/rsat/rsat-overview.md)
- [Dynamics 365-Roadmap und Veröffentlichungszyklus](https://dynamics.microsoft.com/roadmap/overview/)

## <a name="security-and-administrative-access"></a>Sicherheit und administrativer Zugriff Zugriff

Administratorzugriff auf eine Finanz- und Betriebs-Apps-Produktionsumgebung wird streng kontrolliert und protokolliert. Kundendaten werden gemäß den [Bedingungen für Microsoft Online Services](https://www.microsoft.com/licensing/terms/productoffering) abgewickelt. 

### <a name="customer-administrative-access"></a>Administratorzugriff für Kunden

Der Mandantenadministrator des Kunden kann auf Produktionsinstanzen oder Nichtproduktionsinstanzen zugreifen, wie in der folgenden Tabelle beschrieben:

| Umgebungstyp | Kostenträger | Ebene des Kundenzugangs |
|---|---|---|
| **Nicht-Produktion**<br>Sandkasten der Stufe 1 | Eine Nicht-Produktionsumgebung, die Kunden zu Entwicklungs-, Demonstrations- oder Schulungszwecken bereitstellen. | Eine Ebene-1-Sandbox (auch als Cloud-gehostete Umgebung bezeichnet) ist ein vom Kunden verwalteter virtueller Computer, der für das Azure-Abonnement des Kunden von LCS bereitgestellt wird. Da es sich um einen virtuellen Computer im Azure-Abonnement des Kunden handelt, hat der Kunde über Remotedesktop vollen administrativen Zugriff auf die Umgebung. |
| **Nicht-Produktion**<br>Sandbox der Stufe 2 (oder höher) | Eine Nicht-Produktionsumgebung, die Kunden für Benutzerakzeptanztests, Integrationstests, Schulungen, Staging oder andere Vorproduktionsszenarien bereitstellen. | Sandboxes der Stufe 2 und höher werden für das SaaS-Abonnement von Finanz- und Betriebs-Apps bereitgestellt. Der Zugriff auf Azure SQL-Datenbanken, die der Nicht-Produktionsumgebung zugeordnet sind, wird gewährt über [Just-In-Time-Zugriff](../../dev-itpro/database/database-just-in-time-jit-access.md). Remotedesktopzugriff ist nicht verfügbar. |
| **Produktion** | Eine Produktionsumgebung wird bereitgestellt, wenn das Projekt [für den ersten Go-Live bereit ist](/imp-lifecycle/environment-planning.md#production-system-readiness). | Produktionsumgebungen werden für das SaaS-Abonnement bereitgestellt. Der gesamte Zugriff erfolgt über den Browser, Dienstendpunkte oder LCS. |

### <a name="microsoft-administrative-access"></a>Microsoft-Administratorzugriff

Die folgende Tabelle zeigt die verschiedenen Zugriffsebenen für verschiedene Microsoft-Administratoren:

| Administrator | Kundendaten |
|---|---|
| Operations-Reaktionsteam<br>(Beschränkt auf Schlüsselpersonal) | Der Zugang wird über ein Support-Ticket gewährt. Der Zugang wird geprüft und auf die Dauer der Support-Aktivität beschränkt. |
| Microsoft-Kundensupportdienste (CSS) | Kein direkter Zugriff. Der Kunde kann die Bildschirmfreigabe verwenden, um mit Supportmitarbeitern zusammenzuarbeiten, um Probleme zu beheben. |
| Entwicklung | Kein direkter Zugriff. Das Operations-Reaktionsteam kann die Bildschirmfreigabe verwenden, um mit der Technik zusammenzuarbeiten, um Probleme zu beheben. |
| Andere in Microsoft | Kein Zugriff. |

## <a name="monitoring"></a>Überwachung

Microsoft hat in ein umfangreiches Toolset investiert, um die Produktionsinstanzen von Kunden zu überwachen und zu diagnostizieren. Microsoft überwacht die Produktionsumgebungen der Kunden 24 Stunden am Tag, 7 Tage die Woche. Weitere Informationen finden Sie unter [Produktionsunterstützung und -Überwachung](../imp-lifecycle/production-support-monitoring.md).

| Microsoft-Aufgaben | Verantwortlichkeiten des Kunden |
|---|---|
| <ul><li>Überwachen Sie die Verfügbarkeit des Dienstes.</li><li>Kontinuierliche Überwachung und Warnung durch Integritätsmetriken und Watchdogs für kritische Komponenten wie Application Object Server (AOS), Batch, Data Import/Export Framework (DIXF), Commerce und Management Reporter.</li><li>Überwachung auf Leistungseinbußen, die durch Infrastrukturdienste verursacht werden (wie Azure Active Directory \[Azure AD\] und Azure-SQL).</li><li>Wenn Microsoft feststellt, dass ein einzelner Prozess oder Chargenauftrag Abweichungen verursacht, wird dieser Prozess oder Auftrag nach der Kommunikation mit dem Kunden beendet.</li></ul> | <ul><li>Überwachen Sie Änderungen an Anwendungskonfigurationen und -erweiterungen, die Funktions- und Leistungsprobleme verursachen können.</li><li>Anwendungsfehler müssen mithilfe der Überwachungstools diagnostiziert werden. Verwenden Sie diese Tools, um von Benutzern gemeldete Leistungsabweichungen zu diagnostizieren.</li><li>Informieren Sie Microsoft, wenn das System über die prognostizierte Spitzennutzung hinaus erwartet wird.</li><li>Wenn der betreffende Dienst in der Produktionsinstanz nicht verfügbar ist, kann der Kunde LCS verwenden, um einen [Produktionsausfall](../../dev-itpro/lifecycle-services/report-production-outage.md) zu melden.</li></ul> |

Durch das Online-Einreichen von Supportanfragen über LCS ermöglichen Kunden Microsoft, schnelles und umfassendes technisches Fachwissen auf die effektivste und effizienteste Weise bereitzustellen. Obwohl eine Telefonoption verfügbar ist, sollte diese nur verwendet werden, wenn die Online-Option nicht verfügbar ist. Weitere Informationen finden Sie unter [Telefonsupportoptionen](/power-platform/admin/support-overview.md?toc=/dynamics365/fin-ops-core/dev-itpro/toc.json&bc=/dynamics365/breadcrumb/toc.json#is-there-a-phone-number-i-can-call-to-contact-support).

## <a name="incident-management"></a>Vorfallverwaltung

Microsoft reagiert und behebt Vorfälle basierend auf Schweregraden. Die Schweregrade des Vorfalls von Microsoft können während der ersten Bewertung des Vorfalls geändert werden und sobald weitere Informationen zu den Auswirkungen und dem Umfang verfügbar sind. Wenn der Vorfall gemildert wird, bleibt der Schweregrad des Vorfalls unverändert.

Weitere Informationen zu Schweregraden finden Sie unter [diese Schweregradtabelle](/power-platform/admin/support-overview#what-is-initial-response-time-and-how-quickly-can-i-expect-to-hear-back-from-someone-after-submitting-my-support-request).

## <a name="business-continuity-through-high-availability-and-disaster-recovery"></a>Geschäftskontinuität durch hohe Verfügbarkeit und Notfallwiederherstellung 

Microsoft bietet Business Continuity & Disaster Recovery für Produktionsinstanzen von Finanz- und Betriebs-Apps im Falle von Ausfällen in der gesamten Azure-Region. Weitere Informationen, einschließlich Recovery Time Objective (RTO) und Recovery Point Objective (RPO) des Dienstes, finden Sie unter [Business Continuity & Disaster Recovery](../../dev-itpro/sysadmin/business-continuity-disaster-recovery.md).

- **Hohe Verfügbarkeit** – HA-Funktionalität bietet Möglichkeiten zum Verhindern von Ausfallzeiten, die durch den Ausfall eines einzelnen Knotens in einem Azure-Rechenzentrum verursacht werden. Die Cloudarchitektur jedes Dienstes verwendet Azure-Verfügbarkeitssätze für die Computeebene, um Single-Point-of-Failure-Ereignisse zu verhindern. HA für Datenbanken wird bereitgestellt durch [Azure SQL HA-Funktionen](/azure/azure-sql/database/high-availability-sla).
- **Notfallwiederherstellung** –[Funktionen für die Azure-Notfallwiederherstellung](/azure/best-practices-availability-paired-regions) Schützen Sie jeden Dienst vor Ausfällen, die ein gesamtes Azure-Rechenzentrum betreffen. Hier sind einige dieser Funktionen:

    - Azure SQL Active-Geo-Replikation für die primäre Datenbank (Geschäftsdatenbank).
    - Georedundante Kopien von Azure Blob Storage (der Dokumentanlagen enthält) in anderen Azure-Regionen.
    - Sekundäre Region für die Azure SQL- und Azure Blob Storage-Replikationen.

Wenn Notfallwiederherstellung verwendet wird, um die Produktionsinstanz des Kunden wiederherzustellen, erfüllen Microsoft und der Kunde ihre [Vorfallmanagement](service-description.md#incident-management) Verantwortlichkeiten.

Die Notfallwiederherstellunbgspläne und -Verfahren von Microsoft werden regelmäßig im Rahmen von System and Organization Controls (SOC)-Audits überprüft. Diese Compliance-Audits belegen den technischen und verfahrenstechnischen Prozess von Microsofts DR, einschließlich Finanz- und Betriebs-Apps von Dynamics 365. [SOC-Konformität](/compliance/regulatory/offering-soc-2) Auditberichte und alle anderen Compliance-Berichte sind verfügbar auf [Complianceangebote von Microsoft Trust Center](/compliance/regulatory/offering-home).

## <a name="finance-and-operations-support-offerings"></a>Finanz- und Betriebs-Apps-Supportangebote

Technischer Support ist in Märkten verfügbar, in denen Finanz- und Betriebs-Apps-Dienstleistungen angeboten werden. [Supporterfahrungen](../../dev-itpro/lifecycle-services/lcs-support.md) werden in LCS oder Finanz- und Betriebs-Apps geboten. Im Folgenden finden Sie einige Beispiele hierfür:

- [Problemsuche](../../dev-itpro/lifecycle-services/issue-search-lcs.md) in LCS
- [Integrierter technischer Support](../../dev-itpro/lifecycle-services/support-experience.md) in Finanz- und Betriebs-Apps
- [Cloud-betriebener Support](../../dev-itpro/lifecycle-services/cloud-powered-support-lcs.md) in LCS

Microsoft bietet Finanz- und Betriebs-App-Kunden drei Supportpläne an: Premier, Professional Direct und der im Abonnement enthaltene Support. Die Höhe der Unterstützung unterscheidet sich je nach Plan. Die folgende Tabelle zeigt einen Vergleich der drei Pläne.

| Support-Funktion | Premier | Professional Direct | Abonnement |
|---|---|---|---|
| Unbegrenzte Einreichung von Break/Fix-Vorfällen | Ja | Ja | Ja |
| 24/7-Zugriff über LCS | Ja | Ja | Ja |
| Reaktionszeit bei Vorfällen | Weniger als eine Stunde | Weniger als eine Stunde | Nächster Arbeitstag |
| Beratungszeiten | Pools werden nach Vereinbarung erworben. | Nein | Nein |
| Dedizierter Support Account Manager | Ja | Nein | Nein |
| Dedizierter Support-Ingenieur | Im Rahmen einer gesonderten Vereinbarung | Nein | Nein |

Weitere Informationen finden Sie unter [Support-Übersicht](/power-platform/admin/support-overview).

### <a name="process-to-engage-support"></a>Prozess zur Einbindung des Supports

Bei Vorfällen mit Finanz- und Betriebs-Apps senden Kunden Supporttickets über LCS an Microsoft. CSS bearbeitet die Vorfälle, basierend auf dem Supportplan des Kunden und dem Schweregrad des Vorfalls, wie von CSS festgelegt.

### <a name="service-level-agreement"></a>Vereinbarung zum Servicelevel

Microsoft verpflichtet sich zu einer Verfügbarkeitsrate von 99,9 Prozent pro Monat des Dienstes. Wenn Microsoft den im Vereinbarung zum Servicelevel (SLA) beschriebenen Servicelevel für den entsprechenden Service nicht erreicht und aufrechterhält, hat der Kunde möglicherweise Anspruch auf eine Gutschrift auf einen Teil seiner monatlichen Servicegebühren für diesen Service. Informationen zum Initiieren einer Servicegutschrift finden Sie im Abschnitt Ansprüche im [SLA](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

## <a name="important-resources"></a>Wichtige Ressourcen

- **[Trustcenter](https://www.microsoft.com/trust-center)** – Holen Sie sich Informationen darüber, wo die Finanz- und Betriebs-App-Daten gespeichert werden, sowie zusätzliche Informationen zu Datenschutz, Compliance und Sicherheitsverfahren.
- **[Lizenzbedingungen und Dokumentation](https://www.microsoftvolumelicensing.com/)** – Greifen Sie schnell auf Lizenzbedingungen, -Bestimmungen und ergänzende Informationen zu, die für die Nutzung von Produkten und Diensten relevant sind, die über Microsoft-Volumenlizenzprogramme lizenziert werden.
- **[Lizenzbedingungen](https://www.microsoft.com/licensing/product-licensing/)** – Die Ressourcen auf dieser Seite definieren die Bedingungen für die Software- und Onlinedienstprodukte, die Sie über kommerzielle Microsoft-Lizenzprogramme erwerben.
- **[Microsoft-Lebenszyklusrichtlinie](/lifecycle/)** – Diese Seite bietet konsistente und vorhersehbare Richtlinien für die Verfügbarkeit von Support während der gesamten Lebensdauer eines Produkts.
- **[Lizenzierungsleitfaden](https://www.microsoft.com/licensing/docs/view/Microsoft-Dynamics-365)** – Verwenden Sie diese Anleitung, um mehr über die Lizenzierung von Dynamics 365 zu erfahren.
- **[Kundendienst](https://dynamics.microsoft.com/support/)** – Erhalten Sie branchenführenden Support für Ihre Dynamics 365-Apps.
- **[Dynamics Lifecycle Services](https://lcs.dynamics.com/)** – Verwalten Sie Ihren Anwendungslebenszyklus und gehen Sie zu vorhersehbaren, wiederholbaren und qualitativ hochwertigen Implementierungen.
- **[Dynamics 365-Implementierungsleitfaden](https://aka.ms/D365ImplementationGuideFlip)** – Der Dynamics 365-Implementierungsleitfaden dokumentiert bewährte Success by Design-Prinzipien und bietet präskriptive Anleitungen zum Entwerfen, Erstellen, Testen und Bereitstellen von Dynamics 365-Lösungen.

## <a name="definitions"></a>Definitionen

### <a name="azure-region"></a>[Azure-Region](/azure/availability-zones/az-overview#regions)

Eine geografische Region, in der ein oder mehrere Azure-Rechenzentren vorhanden sind. Beispiele sind USA und Europa.

### <a name="business-process-modeler-bpm"></a>[Geschäftsprozessmodellierer](../../dev-itpro/lifecycle-services/bpm-overview.md)

Ein Tool in LCS, das bei der Durchführung einer Fit-Gap-Analyse für eine bestimmte Implementierung hilft, indem es Geschäftsprozessdefinitionen des American Productivity & Quality Center (APQC) verwendet, die in Finanz- und Betriebs-Apps unterstützt werden.

### <a name="cloud-solution-provider"></a>Anbieter von Cloud-Lösungen

Ein Partner, der Teil des Microsoft Cloud Solution Provider (CSP)-Programms ist und Kunden mit Mehrwert-Cloud-Diensten, Support, einer Rechnung und Kundenverwaltung in großem Maßstab versorgt.

### <a name="customer"></a>Kunde

Ein Unternehmen, das Finanz- und Betriebs-Apps konsumiert und durch einen Mandanten in Office 365 dargestellt wird.

### <a name="development-environment"></a>Entwicklungsumgebung

Eine Nicht-Produktions-Sandbox-Umgebung, die zum Entwickeln von Erweiterungen verwendet wird. Kunden stellen diese Umgebung für ihr eigenes Azure-Abonnement von LCS bereit. Diese Umgebung kann auch für Demonstrations-, Schulungs- oder andere Testaufgaben verwendet werden. Es wird auch als [Ebene 1 Sandbox](../imp-lifecycle/environment-planning.md#tier-1-vs-tier-2-and-higher) bezeichnet.

### <a name="downtime"></a>Ausfallzeit

Jeder Zeitraum, in dem sich Benutzer aufgrund eines Fehlers in der nicht abgelaufenen Plattform oder der Dienstinfrastruktur nicht anmelden oder auf ihren aktiven Mandanten zugreifen können, wie Microsoft anhand der automatischen Integritätsüberwachung und der Systemprotokolle feststellt. Ausfallzeiten umfassen keine geplanten Ausfallzeiten, die Nichtverfügbarkeit von Service-Add-On-Funktionen, die Unfähigkeit, auf den Service aufgrund Ihrer Änderungen am Service zuzugreifen, oder Zeiträume, in denen die Kapazität der Skalierungseinheit überschritten wird.

### <a name="implementation-partner"></a>Implementierungspartner

Der Partner, den der Kunde auswählt, um seine Finanz- und Betriebs-Apps-Lösungen anzupassen, zu konfigurieren, zu implementieren oder zu verwalten.

### <a name="incident"></a>Vorfall

Ein Problem, auf das Kunden stoßen, während sie den Finanz- und Betriebs-Apps-Service nutzen, und für das sie ein Ticket über LCS einreichen.

### <a name="microsoft-customer-support-services-css"></a>Microsoft-Kundensupportdienste (CSS)

Das globale Microsoft-Supportteam, das sich der Bereitstellung von Qualitätsservice für Finanz- und Betriebs-Apps verpflichtet hat.

### <a name="microsoft-dynamics-lifecycle-services-lcs"></a>Microsoft Dynamics Lifecycle Services (LCS)

Das Verwaltungsportal für das Lifecycle-Management von Finanz- und Betriebs-Apps von der Testphase über die Implementierung bis hin zum Management und Support nach der Produktion. Weitere Informationen finden Sie unter [Ressourcen für Lifecycle Services](../../dev-itpro/lifecycle-services/lcs.md).

### <a name="non-production-instance"></a>Nicht-Produktionsinstanzen

Jede der folgenden Instanzen eines Dienstes, die der Kunde verwendet, um Erweiterungen zu validieren und andere Entwicklungsaufgaben auszuführen:

- **Sandkasten Stue 1** – Entwicklerinstanz (vom Kunden gehostet)
- **Sandkasten Stufe 2** – Standard-Abnahmetestinstanz
- **Sandbox-Stufen 3–5** – Add-On-Sandboxen

Weitere Informationen zu den Stufen 2 bis 5 finden Sie unter [Auswahl der richtigen Tier-2 oder höheren Umgebung](../imp-lifecycle/environment-planning.md#selecting-the-correct-tier-2-or-higher-environment).

### <a name="production-instance"></a>Produktionsinstanz

Eine Finanz- und Betriebs-Apps-Umgebung, die der Kunde nutzt, um seine täglichen Transaktionen und Geschäftsprozesse live zu verwalten.

### <a name="sandbox-environment"></a>Sandbox-Umgebung

Eine Nicht-Produktionsumgebung, die der Kunde für Demonstrationen, Schulungen, Benutzerakzeptanztests, Validierung von Erweiterungen und andere Testaufgaben verwendet.

### <a name="service"></a>Service

Alle Kerndienste, die in Finanz- und Betriebs-Apps enthalten sind.

### <a name="service-level-agreement-sla-for-microsoft-online-services"></a>Vereinbarung zum Servicelevel (SLA) für Microsoft-Onlinedienste

Das SLA gilt für Microsoft-Onlinedienste. Weitere Informationen finden Sie unter [Vereinbarung zum Servicelevel](https://www.microsoft.com/licensing/docs/view/Service-Level-Agreements-SLA-for-Online-Services).

### <a name="service-update"></a>Serviceupdate

Microsoft wartet Finanz- und Betrieb-Apps-Umgebungen auf konsistenter Basis durch Service-Updates. Kunden legen ihren eigenen Service-Update-Kalender basierend auf ihren Geschäftsanforderungen fest. Weitere Informationen finden Sie unter [Dienstupdates für eine Version](../../dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="success-by-design"></a>[Success by Design](/dynamics365/fasttrack/success-by-design-overview)

Das Framework, das eine Implementierung systematisch durch eine Reihe von Bewertungen in kritischen Phasen führt, um eine optimale Architektur, Sicherheit, Leistung und Benutzererfahrung für eine Dynamics 365-Lösung sicherzustellen.

### <a name="user"></a>Benutzer

Eine einzelne Person, die Finanz- und Betriebs-Apps-Umgebungen verwendet und mit dem Mandanten eines Kunden verknüpft ist.
