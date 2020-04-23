---
title: Aktualisierungsprozess
description: Microsoft Dynamics 365 Human Resources ist ein echter Software-as-a-Service (SaaS), der kontinuierliche, eingriffsfreie Service-Updates für Anwendungs- und Plattformwechsel bietet.
author: andreabichsel
manager: AnnBe
ms.date: 02/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 424027e82717b8636d59289b28978d6ce3c6db4d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154504"
---
# <a name="update-process"></a>Aktualisierungsprozess

Microsoft Dynamics 365 Human Resources ist eine echte Software-as-a-Service (SaaS), die kontinuierliche, berührungslose Dienstupdates bietet. Diese Updates enthalten sowohl Anwendungs‑ als auch Plattformänderungen, die häufig wichtige Verbesserungen des Dienstes bewirken, einschließlich rechtlicher Aktualisierungen.

## <a name="update-policy"></a>Updaterichtlinie

Aktualisierungen werden in regelmäßigen Abständen in allen Umgebungen veröffentlicht. Human Resources wird entsprechend der [Microsoft Lifecycle-Richtlinie](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy) unterstützt, die einen konsistenten und voraussehbaren Leitfaden für die Supportverfügbarkeit bietet.

## <a name="release-cadence"></a>Veröffentlichungshäufigkeit

Human Resources-Aktualisierungen werden automatisch auf alle Umgebungen angewendet. Human Resources bietet zwei Versionstypen:

- **Dienstupdates**: Updates finden alle zwei Wochen staat und enthalten Fehlerkorrekturen und neuen Funktionen. Zu den Dienstupdates gehören auch relevante veröffentlichte Plattformupdates. Informationen zum Zeitpunkt der Veröffentlichung von Plattformupdates finden Sie unter [Tabelle 3: Plattformfreigaben](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Zweiwöchentliche Updates werden in allen Regionen global eingeführt. Weitere Informationen zu zweiwöchentlichen Updates finden Sie unter [Neuerungen oder Änderungen in Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Alle unterstützten Rechenzentren werden alle zwei Wochen aktualisiert, sofern nicht anders angegeben. In den USA, Australien, Europa, Vereinigtes Königreich, Asien und Kanada finden zweiwöchentliche Updates statt. 

- **Common Data Service-Lösungsupdates**: Diese Updates werden nach Bedarf etwa alle sechs Wochen durchgeführt. Dazu gehören neue Entitäten und Änderungen an vorhandenen Entitäten in Common Data Service. Diese Updates werden in denselben Regionen wie die zweiwöchentlichen Updates veröffentlicht. Die Replikation in allen Rechenzentren dauert ungefähr sechs Wochen. Lösungsupdates stimmen möglicherweise mit zweiwöchentlichen Dienstupdates überein.

> [!NOTE]
> Lösungsupdates sind in allen Rechenzentren verfügbar, sobald sie veröffentlicht wurden. Wenn Sie nicht darauf warten möchten, dass die Updates automatisch repliziert werden, können Sie diese Updates in jeder Umgebung in jedem Rechenzentrum manuell anwenden.

Bei Bedarf bietet Human Resources auch die folgenden Fehlerkorrekturtypen:

- **Überarbeitung (Hotfix)**: Fehlerkorrekturen, die mit oder außerhalb eines zweiwöchentliches Dienstupdates auftreten können

- **Notfall-Fix**: Proaktive und reaktive eigenständige Hotfixes, können Nur-Konfigurations‑ oder Codeänderungen zur Behebung von Problemen mit der Live-Site enthalten und unabhängig von einem zweiwöchentlichen Dienstupdate auftreten

Versionen werden in einer internen Umgebung überprüft, getestet und validiert. Nachdem die Builds genehmigt wurden, werden sie für die Produktion bereitgestellt.

## <a name="release-cadence-exceptions-in-2020"></a>Freigabe von Trittfrequenzausnahmen im Jahr 2020

Die folgenden Daten sind Ausnahmen vom regulären Veröffentlichungszeitplan:

| Datum | Beschreibung |
| --- | --- |
| Woche des 23. November | Keine Aktualisierungen |
| Woche des 14. Dezember | Nur kleine Aktualisierungen |
| Woche des 21. Dezember | Keine Aktualisierungen |
| Woche des 28. Dezember | Keine Aktualisierungen |

## <a name="communications"></a>Kommunikation

Hier können Sie herausfinden, was für Human Resources in Arbeit ist und was wir veröffentlicht haben:

- [Dynamics 365 Human Resources-Produktplan](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Dynamics 365-Veröffentlichungspläne](https://docs.microsoft.com/dynamics365/release-plans/)

- [Was ist neu oder geändert in Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemsuche in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (nur für plattformbezogene Fehler)

- [Human Resources-Blog](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer-Community](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Vorschaufunktionen in einer Sandkastenumgebung

Sie können Vorschaufunktionen in einer Sandkastenumgebung überprüfen, bevor Sie sie in Ihrer Produktionsumgebung aktivieren. Weitere Informationen zur Aktivierung von Funktionen finden Sie unter [Funktionsverwaltungsüberblick](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau. Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar. Sobald Sie neue Funktionen im Arbeitsbereich Feature-Management sehen, können Sie diese einschalten. Einige Funktionen sind möglicherweise standardmäßig aktiviert.

Manchmal ist ein integrales Feature standardmäßig eingeschaltet und kann nicht deaktiviert werden (z.B. das Feature-Management Arbeitsbereich).

Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden. Der Arbeitsbereich Feature-Management zeigt an, wann eine Vorschaufunktion obligatorisch wird. Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen. Sie können obligatorische Funktionen nicht deaktivieren. Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.

Es wird dringend empfohlen, eine Vorschau der Funktionen in einer Sandkasten‑ oder Testumgebung anzuzeigen. Erstellen Sie am besten eine Kopie Ihrer aktuellen Produktionsumgebung oder Datenbank in einer Sandkastenumgebung, damit Sie die neuen Funktionen mit Ihren Daten optimal nutzen können.

Weitere Informationen zum Bereitstellen einer Sandkastenumgebung finden Sie unter [Human Resources-Projekt bereitstellen](hr-admin-setup-provision.md). Informationen zum Entfernen einer Testumgebung finden Sie unter [Instanz entfernen](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Fehler melden

Beim Testen der Vorschaufunktionen oder neuer Funktionen werden möglicherweise Elemente gefunden, die nicht wie erwartet funktionieren. Bitte melden Sie alle Fehler dem [Microsoft Dynamics 365 Support](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Siehe auch

[Dynamics 365 und Power Platform-Versionsveröffentlichungspläne](https://docs.microsoft.com/dynamics365/release-plans)</br>
[Neuerungen oder Änderungen in Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Software-Lebenszyklusrichtlinie](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)
