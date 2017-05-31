---
title: "Startseite für Dynamics 365 for Operations Mobile App"
description: In diesem Thema wird die Microsoft Dynamics 365 for Operations Mobile App beschrieben und Links zu Ressourcen bereitgestellt, die Sie bei der Implementierung in der Organisation helfen.
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5962fa36b061382e7f0ad55c08c81ac2cebc047d
ms.contentlocale: de-de
ms.lasthandoff: 05/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Startseite für Dynamics 365 for Operations Mobile App

[!include[banner](../includes/banner.md)]


In diesem Thema wird die Microsoft Dynamics 365 for Operations Mobile App beschrieben und Links zu Ressourcen bereitgestellt, die Sie bei der Implementierung in der Organisation helfen.

<a name="overview"></a>Überblick
--------

Die Microsoft Dynamics 365 for Operations Mobile App ermöglicht es Ihrer Organisation, Geschäftsprozesse auf mobilen Geräten bereitzustellen. Nachdem Ihr IT-Administrator die Funktion mobiler Arbeitsbereich in Ihrer Organisation bereitgestellt hat, können sich Benutzer bei der App anmelden und sofort damit beginnen, Geschäftsprozesse über ihre mobile Geräte auszuführen. Die Dynamics 365 for Operations mobile App umfasst folgende Funktionen, die helfen, die Produktivität zu steigern:

-   Benutzer können Geschäftsdaten anzeigen, bearbeiten und ausführen, selbst wenn die Netzwerkverbindung unterbrochen ist oder ihre mobilen Geräte vollständig offline sind. Wenn ein Gerät eine Netzwerkverbindung erneut einrichtet, werden die Offline-Vorgänge automatisch mit Dynamics 365 for Operations synchronisiert.
-   IT-Administratoren oder Entwickler können mobile Arbeitsbereiche erstellen und veröffentlichen, die auf die Organisation zugeschnitten wurden. Die App verwendet die vorhandenen Codeanlagen. Daher müssen Sie den Validierungsprozess, Geschäftslogik oder Sicherheitskonfiguration nicht erneut implementieren.
-   IT-Administratoren oder -Entwickler entwerfen einfach mobile Arbeitsbereiche, indem sie den Arbeitsbereichdesigner zum Anzeigen und Klicken verwenden, der im Dynamics 365 for Operations Webclient enthalten ist.
-   IT-Administratoren oder Entwickler können die Offline-Funktionalität von Arbeitsbereichen optional optimieren, indem das Geschäftslogikerweiterbarkeitsframework verwendet wird. Da Daten weiter verarbeitet werden, wenn ein Gerät offline ist, bleiben die mobilen Szenarien erhalten. auch wenn die Geräte keine permanente Netzwerkkonnektivität haben.

## <a name="elements-of-the-mobile-app"></a>Elemente der mobilen App
Die Navigation in der mobilen App besteht aus vier einfachen Konzepten: Dashboard, Arbeitsbereiche, Seiten und Aktivitäten. 

[![Navigationskonzepte in der mobilen App](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   Wenn Sie die App starten, gehen Sie zu **Dashboard**.
-   Auf dem Dashboard können Sie eine Liste der **Arbeitsbereiche** sehen, die in Ihrer Dynamics 365 for Operations-Umgebung veröffentlicht werden.
-   In jedem Arbeitsbereich können Sie eine Liste der **Seiten** finden, die für diesen Arbeitsbereich verfügbar sind.
-   Auf einer Seite können Sie Daten anzeigen, die aus mindestens einer Seiten in Dynamics 365 for Operations gesammelt wurden.
-   Von einer Seite können Sie auch zu anderen Seiten für zugehörige Daten navigieren, wie Entitätsdetails oder Positionen.
-   Auf einer Seite können Sie eine Liste **Aktivitäten** finden, die für diese Seite verfügbar sind.
-   Mit Aktivitäten können Sie vorhandenen Daten erstellen oder bearbeiten.

## <a name="implementation-process"></a>Implementierungsprozess
Die folgende Abbildung veranschaulicht den Prozess zum Implementieren der Dynamics 365 for Operations mobilen App in Ihrer Organisation. 

![Implementierungsprozess für mobile Apps](./media/mobile-implementation-process_4.png)

Die folgende Tabelle umfass Links zu Ressourcen, die Ihnen bei der Implementierung von Microsoft Dynamics 365 for Operations mobile App in Ihrer Organisation helfen. Die Nummern in der ersten Spalte entsprechen den nummerierten Schritten in der vorherigen Abbildung.

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
<td>Implementieren Sie Dynamics 365 for Operations für Ihre Organisation.</td>
<td>Wenn Sie nicht bereits Dynamics 365 for Operations in Ihrer Organisation bereitgestellt haben, gehen Sie zu  <a href="../deployment/deploy-demo-environment.md">Microsoft Dynamics 365 for Operations bereitstellen, Testumgebung</a>.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Systemadministrator</td>
<td>Laden Sie KBs herunter und installieren Sie diese, die den mobilen Arbeitsbereich aktivieren, der von Microsoft bereitgestellt wird.</td>
<td>Siehe Abschnitt &quot;Voraussetzungen&quot; im Thema zum mobilen Arbeitsbereich, den Ihre Organisation verwenden möchte:
<ul>
<li><a href="/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Mobiler Arbeitsbereich für die Kostensteuerung</a></li>
<li><a href="/dynamics365/operations/supply-chain/inventory/inventory-on-hand-mobile-workspace">Verfügbarer Lagerbestand, mobiler Arbeitsbereich</a></li>
<li><a href="/dynamics365/operations/supply-chain/sales-marketing/sales-orders-mobile-workspace">Aufträge, mobiler Arbeitsbereich</a></li>
<li><a href="/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Mobiler Arbeitsbereich für Kreditorenzusammenarbeit</a></li>
<li><a href="/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Mobiler Arbeitsbereich für Projektzeiterfassung</a></li>
<li><a href="/dynamics365/operations/financials/expense-management/expense-management-mobile-workspace">Mobiler Arbeitsbereich für Spesenverwaltung</a></li>
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
<td>Nutzen Sie Dynamics 365 for Operations mobiles Framework, um benutzerdefinierte mobile Arbeitsbereiche zu erstellen.</td>
<td><ul>
<li><a href="mobile-platform.md">Mobiles Framework für Dynamics 365 for Operations</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Dynamics 365 for Operations Arbeitsbereich X++-APIs</a></li>
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
<td>Wenden Sie das Bereitstellungspaket an, das die benutzerdefinierten Arbeitsbereiche enthält, die vom ISV bereitgestellt werden.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Anwenden eines Bereitstellungspaket auf einem Microsoft Dynamics 365 for Operations-System</a></td>
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
<td>Laden Sie Dynamics 365 for Operations mobile App herunter und installieren Sie diese.</td>
<td><ul>
<li>Für Android - <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations im Google Play Store</a></li>
<li>Für iPhone: <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations im iTunes-App-Store</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Benutzer</td>
<td>Melden Sie sich an und nutzen Sie Dynamics 365 for Operations mobile App. Die App umfasst die mobilen Arbeitsbereiche, die veröffentlicht wurden.</td>
<td>Um eine Liste der mobilen Arbeitsbereiche anzuzeigen, die von Microsoft bereitgestellt werden, gehen Sie zu <a href="mobile-workspaces-released.md">Mobile Arbeitsbereiche, die vor kurzem für die mobile App von Dynamics 365 for Operations veröffentlicht wurden</a>
</td>
</tr>
</tbody>
</table>






