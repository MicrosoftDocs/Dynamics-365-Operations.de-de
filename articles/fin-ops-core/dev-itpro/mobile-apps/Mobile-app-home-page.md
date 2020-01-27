---
title: Startseite der mobilen App
description: In diesem Thema wird die Finance and Operations Mobile-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.
author: sericks007
manager: AnnBe
ms.date: 11/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: aaff4e3b3bfb079e183a12a5a85e452eed6df51d
ms.sourcegitcommit: e30ced8f136ef23017d2d8215a756236e42eec25
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853931"
---
# <a name="mobile-app-home-page"></a>Startseite der mobilen App

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Finance and Operations Mobile-App beschrieben. Zudem werden Links zu Ressourcen bereitgestellt, die bei der Implementierung in der Organisation helfen.

<a name="overview"></a>Übersicht
--------

Die mobile App ermöglicht es Ihrer Organisation, Geschäftsprozesse auf mobilen Geräten bereitzustellen. Nachdem Ihr IT-Administrator den mobilen Arbeitsbereich für Ihre Organisation bereitgestellt hat, können sich Benutzer bei der App anmelden und sofort damit beginnen, Geschäftsprozesse über ihre mobilen Geräte auszuführen. Die mobile App umfasst folgende Funktionen, die helfen, die Produktivität zu steigern:

- Benutzer können Geschäftsdaten anzeigen, bearbeiten und ausführen, selbst wenn die Netzwerkverbindung unterbrochen ist oder ihre mobilen Geräte vollständig offline sind. Wenn ein Gerät eine Netzwerkverbindung erneut einrichtet, werden die Offline-Vorgänge automatisch synchronisiert.
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

[![Implementierungsprozess für mobile Apps](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

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
<td>Finance and Operations-App in Ihrer Organisation implementieren.</td>
<td><ul><li>Wenn Sie noch keine Version von Microsoft Dynamics 365 bereitgestellt haben, siehe <a href="../deployment/deploy-demo-environment.md">Eine Demoumgebung bereitstellen</a>.</li><li>Um eine Liste mobiler Arbeitsbereiche anzuzeigen, die verwendet werden können, siehe <a href="mobile-workspaces-released.md">Vor Kurzem freigegebene mobile Arbeitsbereiche</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemadministrator</td>
<td><strong>Falls Sie Microsoft Dynamics 365 for Operations Version 1611 verwenden:</strong>Laden Sie KBs herunter und installieren Sie diese. Sie aktivieren die mobilen Arbeitsbereiche, die von Microsoft bereitgestellt werden.</td>
<td>Weitere Informationen finden Sie in folgenden Themen:
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Mobiler Arbeitsbereich für die Kostensteuerung</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Mobiler Arbeitsbereich für Lagerbestand</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Aufträge, mobiler Arbeitsbereich</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobiler Arbeitsbereich für Kreditorenzusammenarbeit</a></li>
<li><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Mobiler Arbeitsbereich für Projektzeiterfassung</a></li>
<li><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Mobiler Arbeitsbereich für Spesenverwaltung</a></li>

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
<td>Nutzen Sie die mobile Plattform, um benutzerdefinierte mobile Arbeitsbereiche zu erstellen.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobile Plattform</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>ISV</td>
<td>Erstellen Sie ein Bereitstellungspaket, das benutzerdefinierte mobile Arbeitsbereiche enthält, und laden Sie das Paket zu Microsoft Dynamics Lifecycle Services (LCS) hoch.</td>
<td><a href="../deployment/create-apply-deployable-package.md">Ein bereitstellbares Paket erstellen</a></td>
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
<td><a href="publish-mobile-workspace.md">Veröffentlichen eines mobilen Arbeitsbereichs</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Benutzer</td>
<td>Laden Sie die mobile App herunter, und installieren Sie diese.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations-App für Android</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations-App für iOS</a><BR/>
(Windows Phone nicht unterstützt)
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

## <a name="troubleshooting"></a>Problembehandlung
[Mobile Plattformressourcen](platform/mobile-platform-home-page.md#troubleshooting-the-app)
