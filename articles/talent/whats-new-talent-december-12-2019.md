---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (10. Dezember 2019)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Talent neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528170"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (10. Dezember 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Talent neu oder geändert wurden.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2660. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Arbeitsbereich für die Funktionsverwaltung

Der Arbeitsbereich **Funktionsverwaltung** bietet eine Liste der in jedem Release ausgelieferten Features. Standardmäßig sind neue Funktionen ausgeschaltet. Sie können den Arbeitsbereich verwenden, um sie zu aktivieren und die Dokumentation für sie anzuzeigen. Weitere Informationen zur Feature-Verwaltung finden Sie unter [Feature-Verwaltung Übersicht](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle neuen Funktionen bleiben mindestens 30 Tage und in der Regel 30-60 Tage in der Vorschau. Die wichtigsten Funktionen sind in der Regel im Oktober und April eines jeden Jahres nach dem Vorschauzeitraum verfügbar. Sobald Sie neue Funktionen im Arbeitsbereich **Feature-Management** sehen, können Sie diese einschalten. Einige Funktionen sind möglicherweise standardmäßig aktiviert.
 
Manchmal ist ein integrales Feature standardmäßig eingeschaltet und kann nicht deaktiviert werden (z.B. das **Feature-Management** Arbeitsbereich).
 
Sobald eine Funktion allgemein verfügbar ist, kann sie in Produktionsumgebungen ein- und ausgeschaltet werden. Der Arbeitsbereich **Feature-Management** zeigt an, wann eine Vorschaufunktion obligatorisch wird. Dieses Datum ist in der Regel der 1. Oktober oder 1. April, um mit den halbjährlichen Release-Plänen übereinzustimmen. Sie können obligatorische Funktionen nicht deaktivieren. Bis es obligatorisch wird, können Sie eine Funktion in allen Umgebungen ein- und ausschalten.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Optimiertes Formular für Arbeitskräfte wurde in den Arbeitsbereich „Funktionsverwaltung“ verschoben (390583)

Mit dieser Änderung kann das optimierte Formular für Arbeitskräfte jetzt im Arbeitsbereich **Funktionsverwaltung** aktiviert werden. Diese Funktion wurde aus dem Formular **Systemparameter** in **Systemverwaltung** verschoben.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Verhindern, dass HcmWorkerPayrollInfo-Datensätze ohne Wert für Arbeitskräfte geschrieben werden (394526)

Mit dieser Version werden **HcmWorkerPayrollInfo**-Datensätze in diesem Szenario nicht länger ohne Verweis auf die Arbeitskraft erstellt. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Das der Aktion zugeordnete Nachrichtenprotokoll wird nicht aufgefüllt, wenn die Aktion nicht abgeschlossen werden kann (374007).

Diese Version enthält eine Änderung zum Auffüllen des Aktionsnachrichtenprotokolls, wenn eine Aktion in bestimmten Szenarien fehlschlägt. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Batch-Job-Erstellung für Common Data Service Integration (388030)

Mit dieser Änderung werden Batchaufträge für die Common Data Service-Integration erstellt, wenn der Dienst aktiviert ist.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Zusätzliche Listenwerte für Entnahmen in benutzerdefinierten Feldern werden nach dem Klicken auf Übernehmen im Formular Benutzerdefinierte Felder (379599) nicht in Common Data Service angezeigt.

Mit dieser Änderung werden neue Listenwerte für Entnahmen, die in Talent eingegeben wurden, jetzt mit Common Data Service synchronisiert, wenn Sie Ihre Änderungen übernehmen.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Aktualisierung zu Common Data Service, bei der die Transaktionsentität „Bankgeschäft verlassen“ in eine Einfügung in Talent geändert wird (352938)

Diese Änderung behebt ein Problem, bei dem durch eine Aktualisierung einer Transaktion zum Verlassen eines Bankgeschäfts ein neuer Datensatz in Talent erstellt wird.

## <a name="in-preview"></a>Vorschau

Vorschaufunktionen werden nur in **Sandbox**-Umgebungen aktiviert.

### <a name="print-performance-reviews"></a>Leistungsbeurteilungen drucken

Weitere Informationen finden Sie unter [Leistungsbeurteilungen drucken](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in Dynamics 365: Plan der 2. Veröffentlichungswelle 2019.

