---
title: Aktualisierungsprozess
description: Microsoft Dynamics 365 Human Resources ist ein echter Software-as-a-Service (SaaS), der kontinuierliche, eingriffsfreie Service-Updates für Anwendungs- und Plattformwechsel bietet.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14bdfa175257023ab68b4cbbda9311bfde77723050355e9d983337c9fa9eb551
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761139"
---
# <a name="update-process"></a>Aktualisierungsprozess

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources ist eine echte Software-as-a-Service (SaaS), die kontinuierliche, berührungslose Dienstupdates bietet. Diese Updates enthalten sowohl Anwendungs‑ als auch Plattformänderungen, die häufig wichtige Verbesserungen des Dienstes bewirken, einschließlich rechtlicher Aktualisierungen.

## <a name="update-policy"></a>Updaterichtlinie

Aktualisierungen werden in regelmäßigen Abständen in allen Umgebungen veröffentlicht. Human Resources wird entsprechend der [Microsoft Lifecycle-Richtlinie](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) unterstützt, die einen konsistenten und voraussehbaren Leitfaden für die Supportverfügbarkeit bietet.

## <a name="release-cadence"></a>Veröffentlichungshäufigkeit 

Human Resources-Aktualisierungen werden automatisch auf alle Umgebungen angewendet. Human Resources bietet zwei Versionstypen:

- **Dienstupdates**: Updates finden alle zwei Wochen staat und enthalten Fehlerkorrekturen und neuen Funktionen. Zu den Dienstupdates gehören auch relevante veröffentlichte Plattformupdates. Informationen zum Zeitpunkt der Veröffentlichung von Plattformupdates finden Sie unter [Tabelle 3: Plattformfreigaben](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases). Zweiwöchentliche Updates werden in allen Regionen global eingeführt. Weitere Informationen zu zweiwöchentlichen Updates finden Sie unter [Neuerungen oder Änderungen in Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Alle unterstützten Rechenzentren werden alle zwei Wochen aktualisiert, sofern nicht anders angegeben. In den USA, Australien, Europa, Vereinigtes Königreich, Asien und Kanada finden zweiwöchentliche Updates statt. 

- **Dataverse-Lösungsupdates**: Diese Updates werden nach Bedarf etwa alle sechs Wochen durchgeführt. Dazu gehören neue Entitäten und Änderungen an vorhandenen Entitäten in Dataverse. Diese Updates werden in denselben Regionen wie die zweiwöchentlichen Updates veröffentlicht. Die Replikation in allen Rechenzentren dauert ungefähr sechs Wochen. Lösungsupdates stimmen möglicherweise mit zweiwöchentlichen Dienstupdates überein.

> [!NOTE]
> Lösungsupdates sind in allen Rechenzentren verfügbar, sobald sie veröffentlicht wurden. Wenn Sie nicht darauf warten möchten, dass die Updates automatisch repliziert werden, können Sie diese Updates in jeder Umgebung in jedem Rechenzentrum manuell anwenden.

Bei Bedarf bietet Human Resources auch die folgenden Fehlerkorrekturtypen:

- **Überarbeitung (Hotfix)**: Fehlerkorrekturen, die mit oder außerhalb eines zweiwöchentliches Dienstupdates auftreten können

- **Notfall-Fix**: Proaktive und reaktive eigenständige Hotfixes, können Nur-Konfigurations‑ oder Codeänderungen zur Behebung von Problemen mit der Live-Site enthalten und unabhängig von einem zweiwöchentlichen Dienstupdate auftreten

Versionen werden in einer internen Umgebung überprüft, getestet und validiert. Nachdem die Builds genehmigt wurden, werden sie für die Produktion bereitgestellt.

## <a name="release-cadence-exceptions-in-2021"></a>Freigabe von Trittfrequenzausnahmen im Jahr 2021

Um die Feiertage zu berücksichtigen, sieht der Veröffentlichungsplan für November und Dezember 2021 wie folgt aus:

- November-Veröffentlichung: 1. November – 14. November
- Dezember-Veröffentlichung: 29. November – 12. Dezember
 
Die zweiwöchige Veröffentlichungshäufigkeit wird wie gewohnt am 10. Januar 2022 wieder aufgenommen.

## <a name="communications"></a>Kommunikation

Hier können Sie herausfinden, was für Human Resources in Arbeit ist und was wir veröffentlicht haben:

- [Dynamics 365 Human Resources-Produktplan](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365-Veröffentlichungspläne](/dynamics365/release-plans/)

- [Was ist neu oder geändert in Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemsuche in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (nur für plattformbezogene Fehler)

- [Human Resources-Blog](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer-Community](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Vorschaufunktionen in einer Sandkastenumgebung

Sie können Vorschaufunktionen in einer Sandkastenumgebung überprüfen, bevor Sie sie in Ihrer Produktionsumgebung aktivieren. Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionsverwaltungsüberblick](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau. Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar. Sobald Sie neue Funktionen im Arbeitsbereich Feature-Management sehen, können Sie diese einschalten. Einige Funktionen sind möglicherweise standardmäßig aktiviert.

Manchmal ist ein integrales Feature standardmäßig eingeschaltet und kann nicht deaktiviert werden (z.B. das Feature-Management Arbeitsbereich).

Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden. Der Arbeitsbereich Feature-Management zeigt an, wann eine Vorschaufunktion obligatorisch wird. Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen. Sie können obligatorische Funktionen nicht deaktivieren. Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.

Es wird dringend empfohlen, eine Vorschau der Funktionen in einer Sandkasten‑ oder Testumgebung anzuzeigen. Erstellen Sie am besten eine Kopie Ihrer aktuellen Produktionsumgebung oder Datenbank in einer Sandkastenumgebung, damit Sie die neuen Funktionen mit Ihren Daten optimal nutzen können.

Weitere Informationen zum Bereitstellen einer Sandkastenumgebung finden Sie unter [Human Resources-Projekt bereitstellen](hr-admin-setup-provision.md). Informationen zum Entfernen einer Testumgebung finden Sie unter [Instanz entfernen](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Fehler melden

Beim Testen der Vorschaufunktionen oder neuer Funktionen werden möglicherweise Elemente gefunden, die nicht wie erwartet funktionieren. Bitte melden Sie alle Fehler dem [Microsoft Dynamics 365 Support](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Siehe auch

[Dynamics 365 und Power Platform-Versionsveröffentlichungspläne](/dynamics365/release-plans)</br>
[Neuerungen oder Änderungen in Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Software-Lebenszyklusrichtlinie](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]