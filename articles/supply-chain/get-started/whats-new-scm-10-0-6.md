---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.6. (November 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Supply Chain Management 10.0.6 neu oder geändert wurden.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428752"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.6. (November 2019)

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Supply Chain Management 10.0.6 entweder neu oder geändert sind. Diese Version hat eine Build-Nummer von 10.0.234. Während das allgemeine Verfügbarkeitsdatum im November liegt, sind die neuen Funktionen für die vorzeitige Veröffentlichung im Oktober verfügbar. Weitere Informationen zur Version 10.0.6 finden Sie unter [zusätzliche Ressourcen](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>Produktkonfigurationsmodelle V2 Datenentität

Eine zweite Version für die Dateneinheit Produktkonfigurationsmodelle wird veröffentlicht (als Produktkonfigurationsmodelle V2 bezeichnet). Die Standardvorlage 418-Produktkonfigurationsmodelle muss ebenfalls so sein, dass sie die neue Datenentität Produktkonfigurationsmodelle V2 in den Import/Export-Framework-Vorlagen verwendet. Die Vorlage wird nicht automatisch aktualisiert, sodass Sie die Vorlage manuell von der Standardeinstellung laden müssen. Die V2-Entität exportiert eine Zeile als separate Datei in einen Anhang anstatt inline, wodurch die Größenbeschränkungen der V1-Entität gelöst werden. 
 
Was müssen Sie tun, um diese Änderung vorzunehmen?
-    Da die V1-Entität veraltet ist, sollten Sie mit der Migration von V1 auf V2 beginnen. Wenn Sie die Vorlage 418-Produktkonfigurationsmodelle verwenden, können Sie auf die Schaltfläche Standardvorlagen laden klicken und die Vorlage 418 – Produktkonfigurationsmodelle neu laden.
-    Wenn Sie die Kompatibilität mit vorhandenen Systemen beibehalten möchten, können Sie die vorhandene Vorlage und die (veraltete) V1-Entität vorerst weiter verwenden, bis Sie Ihre Integrationen in die neue Vorlage verschieben. 

## <a name="feature-management-enhancements"></a>Funktionsverwaltungsverbesserungen
Mit der Funktionsverwaltung können Sie jetzt standardmäßig alle neuen Funktionen aktivieren, eine Bestätigung zum Aktivieren einer Funktion anfordern und alle Funktionen aktivieren, die noch nicht aktiviert wurden. 


## <a name="purchase-agreement-responsible-party"></a>Zuständige Partei für Kaufvertrag
Sie haben jetzt die Möglichkeit, primäre und sekundäre Verantwortliche auf dem Klassifizierungsformular für Kaufverträge und den daraus resultierenden Kaufverträgen zu definieren.  Dadurch erhält der Benutzer Zugriff darauf, wer die Vereinbarungen überwacht.

## <a name="rfq-link-on-the-purchase-order-line"></a>Angebotsanforderung auf der Bestellungszeile
Sie können einen Referenzlink aus den Bestellpositionen zu den entsprechenden Angebotsanforderungs-Zeilen hinzufügen, aus denen sie stammen, sodass der Benutzer problemlos die unterstützende Angebotsanfrage erhalten kann.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="bug-fixes"></a>Fehlerkorrekturen
Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.6 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7) an.

### <a name="platform-update-30"></a>Plattformupdate 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 enthält das Plattform-Update 30. Weitere Informationen zum Plattform-Update 30 finden Sie unter [Was ist neu oder geändert in Platform Update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: 2019 Veröffentlichungsplan Welle 2
Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Testen Sie [Dynamics 365: 2019 Release Welle 2 Plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Das Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Thema [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]