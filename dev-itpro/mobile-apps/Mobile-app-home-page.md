---
title: Mobile App-Startseite
description: In diesem Thema wird die mobile Microsoft Dynamics 365 for Unified Operations-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28T00:00:00.000Z
ms.translationtype: HT
ms.sourcegitcommit: 9ea9eb66abf7898ce735e1204259fcc9b9523c52
ms.openlocfilehash: 8674a237878d4358c7f9ce4d4dfcace302536063
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="mobile-app-home-page"></a>Mobile App-Startseite

[!include[banner](../includes/banner.md)]

In diesem Thema wird die mobile Microsoft Dynamics 365 for Unified Operations-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.

> [!NOTE]
> Die mobile App wurde zuvor als *Microsoft Dynamics 365 for Finance and Operations* bezeichnet.

<a name="overview"></a>Überblick
--------

Die mobile App ermöglicht es Ihrer Organisation, Geschäftsprozesse auf mobilen Geräten bereitzustellen. Nachdem Ihr IT-Administrator den mobilen Arbeitsbereich für Ihre Organisation bereitgestellt hat, können sich Benutzer bei der App anmelden und sofort damit beginnen, Geschäftsprozesse über ihre mobilen Geräte auszuführen. Die mobile App umfasst folgende Funktionen, die helfen, die Produktivität zu steigern:

- Benutzer können Geschäftsdaten anzeigen, bearbeiten und ausführen, selbst wenn die Netzwerkverbindung unterbrochen ist oder ihre mobilen Geräte vollständig offline sind. Wenn ein Gerät eine Netzwerkverbindung erneut einrichtet, werden Offline-Datenoperationen automatisch mit Dynamics 365 for Finance and Operations, Enterprise-Edition oder Microsoft Dynamics 365 for Finance and Operations synchronisiert.
- IT-Administratoren oder Entwickler können mobile Arbeitsbereiche erstellen und veröffentlichen, die auf die Organisation zugeschnitten wurden. Die App verwendet die vorhandenen Codeanlagen. Daher müssen Sie den Validierungsprozess, Geschäftslogik oder Sicherheitskonfiguration nicht erneut implementieren.
- IT-Administratoren oder -Entwickler können ganz einfach mobile Arbeitsbereiche entwerfen, indem sie den Arbeitsbereichdesigner zum Anzeigen und Klicken verwenden, der im Webclient enthalten ist.
- IT-Administratoren oder Entwickler können die Offline-Funktionalität von Arbeitsbereichen optional optimieren, indem das Geschäftslogikerweiterbarkeitsframework verwendet wird. Da Daten weiter verarbeitet werden, wenn ein Gerät offline ist, bleiben die mobilen Szenarien erhalten. auch wenn die Geräte keine permanente Netzwerkkonnektivität haben.

## <a name="elements-of-the-mobile-app"></a>Elemente der mobilen App
Die Navigation in der mobilen App besteht aus vier grundlegenden Konzepten: Dashboard, Arbeitsbereiche, Seiten und Aktivitäten. 

[![Navigationskonzepte in der mobilen App](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. Wenn Sie die App starten, gehen Sie zu **Dashboard**.
2. Auf dem Dashboard wird eine Liste der veröffentlichten **Arbeitsbereiche** angezeigt.
3. In jedem Arbeitsbereich können Sie eine Liste der **Seiten** finden, die für diesen Arbeitsbereich verfügbar sind.
4. Nachdem Sie auf einer Seite sind, können Sie eine Reihe von Aktivitäten ausführen. Nachfolgend finden Sie einige Beispiele:

    - Zeigen Sie detaillierte Daten an.
    - Navigieren Sie zu anderen Seiten mit zugehörige Daten wie Entitätsdetails oder Positionen.
    - Zeigen Sie eine Liste mit **Aktivitäten** an, die für die Seite verfügbar sind. Mit Aktivitäten können Sie vorhandenen Daten erstellen oder bearbeiten.

## <a name="implementation-process"></a>Implementierungsprozess
Die folgende Abbildung veranschaulicht den Prozess des Implementierens beider mobiler Arbeitsbereiche, die von Microsoft und benutzerdefinierten mobilen Arbeitsbereichen bereitgestellt werden. 

![Implementierungsprozess für mobile Apps](./media/Mobile-implementation-process-5.png)

Die folgende Tabelle enthält Links zu Ressourcen, die Ihnen beim Implementieren beider mobilen Arbeitsbereiche helfen, die von Microsoft und benutzerdefinierten mobilen Arbeitsbereichen bereitgestellt werden. Die Nummern in der ersten Spalte entsprechen den nummerierten Schritten in der vorherigen Abbildung.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Schritt</th>
<th>Rolle</th>
<th>Vorgang</th>
<th>Ressourcen, die Ihnen beim Erfüllen der Aktivität helfen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Systemadministrator</td>
<td>Implementieren Sie Finance and Operations in Ihre Organisation.</td>
<td><ul><li>Wenn Sie noch keine Version von Microsoft Dynamics 365 bereitgestellt haben, siehe <a href="../deployment/deploy-demo-environment.md">Erstellen einer Demoumgebung</a>.</li><li>Um eine Liste mobiler Arbeitsbereiche anzuzeigen, die verwendet werden können, siehe <a href="mobile-workspaces-released.md">Vor Kurzem freigegebene mobile Arbeitsbereiche</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemadministrator</td>
<td><strong>Wenn Sie Microsoft Dynamics 365 for Finance and Operations, Version 1611, verwenden:</strong> Laden und installieren Sie KBs, die die von Microsoft bereitgestellten mobilen Arbeitsbereiche aktivieren.</td>
<td>Weitere Informationen finden Sie in folgenden Themen:
<ul>

<li><a href="/dynamics365/unified-operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobiler Arbeitsbereich für die Kostensteuerung</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Mobiler Arbeitsbereich für Lagerbestand</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Aufträge, mobiler Arbeitsbereich</a></li>
<li><a href="/dynamics365/unified-operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobiler Arbeitsbereich für Kreditorenzusammenarbeit</a></li>
<li><a href="/dynamics365/unified-operations/financials/project-management/project-time-entry-mobile-workspace">Mobiler Arbeitsbereich für Projektzeiterfassung</a></li>
<li><a href="/dynamics365/unified-operations/financials/expense-management/expense-management-mobile-workspace">Mobiler Arbeitsbereich für Spesenverwaltung</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Systemadministrator</td>
<td>Veröffentlichen Sie die mobilen Arbeitsbereiche, die von Microsoft zur Verfügung gestellt werden.</td>
<td><a href="publish-mobile-workspace.md">Mobilen Arbeitsbereich veröffentlichen</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Entwickler oder unabhängiger Softwarehersteller (ISV)</td>
<td>Nutzen Sie das mobile Framework, um benutzerdefinierte mobile Arbeitsbereiche zu erstellen.</td>
<td><ul>
<li><a href="mobile-platform.md">Mobiles Framework</a></li>
<li><a href="mobile-workspace-xpp-apis.md">Arbeitsbereich-X++-APIs</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Erstellen eines Bereitstellungspaket, das benutzerdefinierte mobile Arbeitsbereiche enthält, und laden Sie das Paket zu den Microsoft Dynamics Lifecycle Services (LCS) hoch.</td>
<td><a href="../deployment/create-apply-deployable-package.md">Ein Bereitstellungspaket erstellen</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Systemadministrator</td>
<td>Wenden Sie das Bereitstellungspaket an, das die benutzerdefinierten Arbeitsbereiche enthält, die vom unabhängigen Softwareanbieter (ISV) bereitgestellt werden.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Bereitstellbare Pakete übernehmen</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Systemadministrator</td>
<td>Veröffentlichen Sie die benutzerdefinierten mobilen Arbeitsbereiche, die von ISV zur Verfügung gestellt werden.</td>
<td><a href="publish-mobile-workspace.md">Mobilen Arbeitsbereich veröffentlichen</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Benutzer</td>
<td>Laden Sie die mobile App herunter, und installieren Sie diese.</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">Für Android-Smartphones</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">Für iPhones</a></li></ul>
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Benutzer</td>
<td>Melden Sie sich an, und verwenden Sie die mobile App. Die App umfasst die mobilen Arbeitsbereiche, die vom Systemadministrator veröffentlicht wurden.</td>
<td>Um eine Liste mobiler Arbeitsbereiche anzuzeigen, die von Microsoft bereitgestellt werden, rufen Sie <a href="mobile-workspaces-released.md">Vor Kurzem freigegebene mobile Arbeitsbereiche</a> auf.
</td>
</tr>
</tbody>
</table>

