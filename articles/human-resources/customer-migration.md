---
title: Human Resources Kundenmigration FAQ
description: Dieser Artikel beantwortet häufig gestellte Fragen zur Migration von Microsoft Dynamics 365 Human Resources auf die fusionierte Infrastruktur für Finanzen und Betrieb.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151081"
---
# <a name="human-resources-customer-migration"></a>Human Resources Kundenmigration

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Wie sollten Dynamics 365 Human Resources-Debitor die Umstellung auf die Finanzen und Betrieb-Infrastruktur planen?

Zwei Kategorien von Microsoft Dynamics 365 Human Resources-Kunden sind davon betroffen und müssen Änderungen vornehmen, um sicherzustellen, dass sie auf der neuesten Infrastruktur für Finanzen und Vorgänge sind:

- Debitoren, die Dynamics 365 Human Resources verwenden und über keine anderen Apps für Vorgänge in Dynamics 365 verfügen
- Debitoren, die sowohl Dynamics 365 Human Resources als auch Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce oder Dynamics 365 Project Operations verwenden

Unabhängig von der Kategorie, zu der sie gehören, müssen Debitor Daten in eine neu erstellte Umgebung in der Finanzen und Betrieb Infrastruktur verschieben und überprüfen, ob die Zusammenführung erfolgreich abgeschlossen wurde.

In Zukunft wird die App Dynamics 365 Human Resources über eine eigene Umgebung für Finanzen und Vorgänge verfügen, die von den anderen Apps für Vorgänge getrennt ist. Auf diese Weise kann der Debitor die Vorteile der Erweiterungsmöglichkeiten nutzen, ohne seine aktuellen Daten zusammenführen zu müssen. Microsoft wird Tools und eine Sandbox-Umgebung bereitstellen, mit denen Debitor die Datenmigration testen und validieren kann, bevor sie in eine Produktionsumgebung überführt wird. Das Tool wird einen nahezu automatisierten Prozess ermöglichen und zwischen August und November 2022 verfügbar sein.

Debitor, die andere Apps in der Infrastruktur von Finanzen und Betrieb verwenden, haben die Möglichkeit, ihre Human Resources Daten mit einer bestehenden Umgebung zusammenzuführen. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Wann werden die Debitor auf die Finanzen und Betrieb-Infrastruktur umgestellt?

Der Übergang für jedes Unternehmen hängt von der aktuellen Konfiguration und der Bereitschaft des Unternehmens ab, auf die Finanzen und Betrieb-Infrastruktur umzusteigen. Wir empfehlen dem Debitor, mit seinem Microsoft-Partner zusammenzuarbeiten, um den besten Weg zu finden.

- Unternehmen, die das Modul **Human Resources** in Dynamics 365 Finance verwenden, können die neuen Funktionalitäten von Dynamics 365 Human Resources im Rahmen des regelmäßigen Aktualisierungsprozesses von One Version aktivieren. Die neuen Funktionen werden voraussichtlich ab Januar 2022 allgemein verfügbar sein.
- Organisationen, die Dynamics 365 Human Resources verwenden, haben Zugriff auf Tools, mit denen sie die Zusammenführung der Infrastruktur abschließen können. Microsoft wird mit den Debitor bei der Umstellung zusammenarbeiten, um eine Unterbrechung des Services zu vermeiden. Für die Umstellung haben die Debitor 12 bis 18 Monate Zeit, ab dem Zeitpunkt, an dem das Tool für die Migration verfügbar ist.
- Organisationen, die sowohl Dynamics 365 Human Resources als auch das Modul **Human Resources** verwenden, können ihre eigenständige Human Resources-Infrastruktur auf die Finanzen und Betrieb-Infrastruktur übertragen. Eine weitere Möglichkeit ist die Verwendung des Merge Tools, um die Umgebungen in eine einzige Umgebung zu bringen. Es gibt keine Vorgabe oder einen Zeitrahmen für die Zusammenführung der beiden Umgebungen.

Für aktuelle Informationen überprüfen Sie regelmäßig die [Release-Pläne](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Benötigen die Debitor weiterhin angepasste Integrationen zwischen Dynamics 365 Human Resources und dem Human Resources Modul?

- Debitor, die sowohl Dynamics 365 Human Resources als auch andere Infrastrukturumgebungen für Finanzen und Vorgänge haben, die derzeit integriert sind, müssen die beiden Umgebungen nach der Zusammenführung weiterhin integrieren.
- Debitor, die sich dafür entscheiden, ihre Dynamics 365 Human Resources-Umgebung von ihrer bestehenden Finanz- und Betriebs-App-Umgebung getrennt zu halten, müssen die Umgebungen weiterhin integrieren, damit die Daten in beiden Umgebungen verfügbar sind.
- Die Debitor können weiterhin den Data Integrator verwenden, um Daten zwischen den beiden Umgebungen zu kopieren. Debitor, die nach der Migration Daten in einer einzigen Umgebung zusammenführen, müssen die Daten nicht mehr integrieren, da sich alle Daten in einer einzigen Datenbank befinden werden.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Werden die ISV-Lösungen des Debitors automatisch migriert?

Die Migrationserfahrung für jede Lösung eines unabhängigen Softwareanbieters (ISV) variiert je nach Integrationsmethode der Lösung. Microsoft wird eng mit ISVs zusammenarbeiten, um einen reibungslosen Übergang zur Finanzen und Betrieb-Infrastruktur zu ermöglichen. Viele ISV-Lösungen bauen auf Dataverse auf, indem sie Funktionalitäten von Microsoft Power Platform nutzen. Diese Lösungen hängen von der Dataverse Integration zwischen der Dynamics 365 Human Resources Umgebung und der Dataverse Umgebung ab. Die Dataverse-Integration wird im Rahmen der Zusammenlegung der Infrastruktur veraltet. In der Infrastruktur von Finanzen und Betrieb sind neue Dual-write Zuordnungen geplant, die die Funktionalität der Dataverse-Integration ersetzen sollen.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Wie wird sich der Data Integrator, der Daten zwischen Dynamics 365 Human Resources und anderen Dynamics 365 Apps verschiebt, auswirken?

Nachdem Debitor in die Finanzen und Betrieb-Infrastruktur umgezogen ist, muss er weiterhin Daten zwischen den beiden Umgebungen integrieren. Debitor kann weiterhin den Data Integrator verwenden, um diese Datenmigrationsaufgaben durchzuführen. Debitor, die planen, ihre Dynamics 365 Human Resources-Umgebung von ihrer bestehenden Umgebung für Finanz- und Betriebs-Apps getrennt zu halten, müssen die Daten zwischen den beiden Umgebungen weiterhin integrieren. Für Debitor, die die beiden Umgebungen zu einer einzigen Umgebung zusammenführen, ist eine Integration zwischen den beiden Umgebungen nicht mehr erforderlich.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Wie werden die Daten zwischen Dynamics 365 Human Resources auf der Finanzen und Betrieb Infrastruktur und Dataverse nach der Migration verschoben?

Die derzeitige Dataverse-Integration zwischen Dynamics 365 Human Resources und Dataverse wird als Teil der Infrastruktur für Finanzen und Betrieb veraltet. Es ist geplant, Dual-write Maps einzuführen, um die Entitäten von Finance und Operations den Dataverse-Tabellen zuzuordnen. Die Debitor werden entscheiden müssen, welche Dual-write Zuordnungen für ihre Implementierung erforderlich sind. Wir empfehlen, virtuelle Tabellen für Integrationen und ISV-Lösungen zu verwenden, es sei denn, es besteht eine besondere geschäftliche Notwendigkeit, die Daten in Dataverse zu duplizieren, um die Geschäftslogik auszuführen.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Wie wirkt sich die Migration auf Dataverse-Erweiterungen für Dynamics 365 Human Resources aus?

Die Debitor müssen auf eine Sandbox-Umgebung migrieren, bevor sie ihre Produktionsumgebung umstellen können. Wenn Debitor seine Sandbox-Umgebung migriert, muss er eine Kopie seiner Dataverse-Umgebung erstellen, um eine Verbindung zur neuen, migrierten Finanzen und Betrieb-Umgebung herzustellen. Wir empfehlen, dass ein Debitor sowohl die Daten als auch die Lösungen für die Umgebung kopiert, damit sie der aktuellen Produktionsumgebung des Debitors entsprechen.

Wenn die Debitor bereit sind, ihre produktive Dynamics 365 Human Resources-Umgebung zu migrieren, wird Microsoft automatisch die Datenbank und den Azure Blob-Storage migrieren. Die migrierte Datenbank und der migrierte Speicher verweisen die neue Umgebung auf der Finanzen und Betrieb-Infrastruktur auf dieselbe Produktionsumgebung Dataverse. Bevor die Daten weiterhin nach Dataverse kopiert werden können, müssen die Debitor alle Dual-write Zuordnungen aktivieren, die für ihre Integrationen, Erweiterungen und ISV-Lösungen, die auf Dataverse aufbauen, erforderlich sind.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Werden Microsoft Power Platform-Komponenten, die für Dynamics 365 Human Resources erstellt wurden, automatisch funktionieren, nachdem die Migration der Infrastruktur abgeschlossen ist?

Apps, die in Power Apps erstellt werden, Flows, die in Power Automate erstellt werden, und andere Microsoft Power Platform Anpassungen sind wie Dataverse Erweiterungen. Während der Migration der Produktionsumgebungen des Debitors gibt es keine Auswirkungen auf die Dataverse-Umgebungen, einschließlich aller Erweiterungen. Apps, Flows und andere Anpassungen der Power Microsoft Plattform sollten weiterhin funktionieren, ohne dass eine zusätzliche Konfiguration erforderlich ist.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Was geschieht mit den Entitäten der virtuellen Tabelle Dataverse für Dynamics 365 Human Resources während der Migration?

Wenn Debitor seine Dynamics 365 Human Resources-Umgebung in die Finanzen und Betrieb-Infrastruktur migriert, bleibt die Umgebung mit der Dataverse-Umgebung verbunden, die derzeit mit Dynamics 365 Human Resources verbunden ist. Die virtuellen Dataverse-Tabellen, die in der Umgebung erstellt wurden, werden weiterhin funktionieren, ohne dass eine zusätzliche Konfiguration erforderlich ist. Die virtuellen Tabellen müssen möglicherweise in der Dataverse-Umgebung, die mit der bestehenden Finanzen und Betrieb-Umgebung eines Debitors verbunden ist, neu erstellt werden.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Wie funktioniert eine Integration, die die Applicant Tracking System (ATS) API, die Payroll API, die virtuellen Tabellen von Dataverse für Dynamics 365 Human Resources oder andere Entitäten in der Dataverse Web-API verwendet, nachdem die Zusammenführung der Infrastruktur abgeschlossen ist?

Wenn Debitor seine Dynamics 365 Human Resources-Umgebung in die Finanzen und Betrieb-Infrastruktur migriert, bleibt die Umgebung mit der Dataverse-Umgebung verbunden, die derzeit mit Dynamics 365 Human Resources verbunden ist. Alle Integrationen, die für die Web-API Dataverse entwickelt wurden, funktionieren auch nach der Migration weiter.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Unser Unternehmen hat die angepasste Sicherheit in Dynamics 365 Human Resources konfiguriert. Werden sie auch nach Abschluss der Migration der Infrastruktur noch angewendet?

Ja, angepasste Sicherheitskonfigurationen werden bei der Datenmigration berücksichtigt.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Werden die Workflows in Dynamics 365 Human Resources automatisch migriert?

Ja, Workflow-Konfigurationen, Workflow-Verlauf und laufende Workflows werden in die zusammengeführte Infrastruktur migriert.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Werden gespeicherte Ansichten in Dynamics 365 Human Resources automatisch migriert?

Ja, gespeicherte Ansichten werden in die zusammengeführte Infrastruktur migriert.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Werden Funktionen, die in Dynamics 365 Human Resources aktiviert sind, nach der Zusammenlegung der Infrastruktur automatisch verfügbar sein?

- Für Debitor, die das Modul **Human Resources** verwenden, werden Funktionen, die nur in Dynamics 365 Human Resources verfügbar sind, über die Funktionsverwaltung verwaltet. Normalerweise sind diese Funktionen nicht standardmäßig aktiviert. Alle Funktionen, die standardmäßig aktiviert werden müssen, werden dokumentiert.
- Für Debitor, die Dynamics 365 Human Resources verwenden, werden Funktionen in der Infrastruktur verfügbar sein. Alle Funktionen, die nicht verfügbar sind, werden dokumentiert. Alle Funktionen der Funktionsverwaltung, die in der aktuellen Dynamics 365 Human Resources-Umgebung aktiviert sind, werden auch in der fusionierten Infrastruktur aktiviert. Weitere Informationen finden Sie unter [Funktionsverwaltung – Übersicht](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Was geschieht mit BYOD-Datenbanken während der Migration?

Import- und Exportkonfigurationen für Bring Your Own Database (BYOD) werden in die Finanzen und Betrieb-Infrastruktur migriert.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Gibt es Auswirkungen auf die Azure-Region, wenn die Umgebung des Debitors migriert wird?

Die Dynamics 365 Human Resources-Umgebung bleibt bei der Migration in derselben Azure-Region. Wenn eine Umgebung in eine andere Azure-Region verschoben werden muss, müssen die Debitor die Standardschritte für die Migration in eine neue Region befolgen, nachdem die Migration abgeschlossen ist.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Was passiert mit Azure Data Lakes während der Migration?

Alle Exporte, die derzeit für Azure Data Lake in Finanz- und Betriebs-Apps konfiguriert sind, bleiben auch nach der Migration unverändert.

> [!NOTE]
> Dual-write Maps müssen aktiviert werden, um weiterhin Daten aus der Umgebung von Human Resources in Dataverse zu schreiben.

Debitor, die Human Resources-Daten in den Data-Lake exportieren möchten, können diese Funktion nach Abschluss der Migration zur Infrastruktur für Finanzen und Vorgänge aktivieren. Weitere Informationen finden Sie unter [Data-Lakes – Azure Architecture Center](/azure/architecture/data-guide/scenarios/data-lake).

Debitor kann mehrere Umgebungen für Finanzen und Vorgänge mit demselben Data-Lake verknüpfen. Jede Umgebung wird jedoch auf einen anderen Ordner und Container verweisen. Debitor, die planen, die Umgebungen später zusammenzuführen, sollten ihre Vorgehensweise sorgfältig planen.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Welche Migration ist erforderlich, wenn ein Debitor derzeit das Human Resources-Modul verwendet?

Bei Debitor, die das Modul **Human Resources** verwenden, wird die neue Funktion aus Dynamics 365 Human Resources über den Standardprozess der Versionsverwaltung auf ihre Umgebung angewendet. Die Debitor können davon ausgehen, dass die neuen Funktionen in ihrer Umgebung mit jedem Update zur Verfügung stehen werden. Kunden können die Funktionsverwaltung nutzen, um die Funktionen zu aktivieren. Die Debitor sollten planen, diese neuen Funktionen mit den Prozessen zu validieren, die sie bereits In-Place haben und für die Validierung anderer Aktualisierungen in ihrer Umgebung verwenden.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Was geschieht mit angepassten Integrationen in externe Systeme?

Der Debitor muss seine Integrationen in die Finanz- und Betriebs-Umgebung migrieren. Da der Endpunkt dieser Umgebung ein anderer ist, müssen die Debitor möglicherweise die Integrationen aktualisieren oder ändern, damit sie auf die neue Umgebung verweisen. Diese Aufgabe wird in erster Linie ein manueller Prozess sein, und die erforderlichen Änderungen hängen von der Architektur der Integration ab. Debitor sollten mit ihrem Microsoft-Partner zusammenarbeiten, um den besten Ansatz für die Verschiebung von Integrationen zu ermitteln.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Was geschieht mit den Microsoft Power Platform- (Dataverse-) Erweiterungen, wenn ein Debitor eine Dynamics 365 Human Resources-Umgebung mit einer bestehenden Finanzen und Betrieb-Umgebung zusammenführt?

Wenn sich Debitor dafür entscheidet, eine Dynamics 365 Human Resources-Umgebung und eine bestehende Finanzen und Betrieb-Umgebung nach der Migration zu einer einzigen Dataverse-Instanz zusammenzulegen, müssen die Dataverse-Umgebungen im Rahmen des Zusammenlegungsprozesses kombiniert werden. Diese Aufgabe erfordert, dass alle Apps, die mit Power Apps erstellt wurden, und alle anderen Anpassungen in der neuen Umgebung neu bereitgestellt werden.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Was geschieht mit den Belegen während der Migration?

Wenn Debitor seine Dynamics 365 Human Resources-Umgebung in die Finanzen und Betrieb-Infrastruktur migriert, verbleiben die Belege im bestehenden Dokumentenspeicher und werden automatisch der neuen Umgebung in der Finanzen und Betrieb-Infrastruktur zugeordnet.

In einer zukünftigen Version werden neue Entitäten für die Daten bereitgestellt. Nach dieser Änderung können Debitor, die sich dafür entscheiden, ihre Dynamics 365 Human Resources-Umgebung mit einer bestehenden Finanz- und Betriebs-Umgebung zusammenzuführen, Belege exportieren und in die bestehende Umgebung verschieben.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Was geschieht nach der Migration mit den Batchaufträgen, die in Dynamics 365 Human Resources konfiguriert wurden?

Batch-Aufträge müssen in der Finanz- und Betriebs-Umgebung neu konfiguriert werden. Die Debitor müssen jeden Batchauftrag bewerten und ihn mit der aktuellen Liste der Batchaufträge in der Finanz- und Betriebs-Umgebung vergleichen. Debitor sollten auch den gesamten Batchplan analysieren, wenn sie die beiden Sätze von Batchaufträgen zusammenführen, um festzustellen, ob Änderungen am Batchplan, den Prioritäten oder den Batchgruppen vorgenommen werden sollten.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Wie wird sich die Migration auf das LCS-Projekt für Dynamics 365 Human Resources auswirken?

Die Debitor müssen ein neues Microsoft Dynamics Lifecycle Service (LCS) Projekt erstellen und als Produkt Finanz- und Betriebs-Apps und als Projekttyp **Implementierung** auswählen. Außerdem ist ein neues Feld für den Unterprojekttyp verfügbar, wenn ein LCS-Projekt erstellt wird. Die Debitor müssen die Option Dynamics 365 Human Resources auswählen, um ein bestehendes Human Resources LCS Projekt in die Finanzen und Betrieb Infrastruktur zu migrieren.

Die Funktionen der Finanzen und Betrieb LCS Projekte unterscheiden sich von den Funktionen der Human Resources LCS Projekte.

Um in Betrieb zu gehen, müssen neue Debitor die folgenden Aufgaben erledigen:

- Vervollständigen Sie das Projekt-Onboarding.
- Vervollständigen Sie die Methodik.
- Füllen Sie einen Schätzer für das Abonnement aus.
- Vervollständigen Sie den Prozess der Bereitschaft zum Go-Live.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Wie wird der Business Process Modeler migriert?

Die Debitor müssen ihre Business Process Modeler Bibliothek aus dem Human Resources LCS Projekt exportieren und in das Finanzen und Betrieb LCS Projekt importieren. Außerdem müssen die Debitor die Hilfe-Einstellungen in der Anwendung aktualisieren, damit sie auf das neue LCS-Projekt verweisen.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Wie wirkt sich die Migration auf den Service-Update-Prozess aus?

Nach der Migration haben die Debitor viel mehr Flexibilität für Application Lifecycle Management (ALM) und Service-Updates. Service-Updates werden nicht mehr automatisch auf Human Resources Umgebungen angewendet. Stattdessen wird der Dienst den Aktualisierungsprozessen und -funktionen des One Version Service folgen, und es werden Konfigurationsoptionen für Aktualisierungen über LCS aktiviert.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Haben die Debitor Anspruch auf FastTrack-Unterstützung bei der Zusammenführung der Infrastruktur?

Microsoft legt derzeit noch fest, welche Tools und Ressourcen von FastTrack zur Verfügung gestellt werden, um bei der Zusammenführung zu helfen.

## <a name="licensing-impact"></a>Auswirkungen auf die Lizenzierung

Weitere Informationen zu den Auswirkungen auf die Lizenzierung finden Sie unter [Dynamics 365 Human Resources Infrastruktur-Zusammenführung FAQ](hr-infrastructure-merge-faq.md#licensing-impact).
