---
title: "Mobiler Arbeitsbereich für Projektzeiterfassung"
description: "Dieses Thema enthält Informationen zur Projektzeiterfassungs im mobilen Arbeitsbereich. Dieser Verknüpfung ermöglicht Benutzern Zeit für ein Projekt einzugeben und zu speichern, indem sie das mobile Gerät verwenden."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9bf79af6eea6f899158fc3c8d523587cb11c90ad
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="project-time-entry-mobile-workspace"></a>Mobiler Arbeitsbereich für Projektzeiterfassung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur **Projektzeiterfassungs** im mobilen Arbeitsbereich. Dieser Verknüpfung ermöglicht Benutzern Zeit für ein Projekt einzugeben und zu speichern, indem sie das mobile Gerät verwenden.

Dieser mobile Arbeitsbereich soll mit der Mobil-App für Microsoft Dynamics 365 für Unified Operations verwendet werden. 

## <a name="overview"></a>Überblick
Im Rahmen ihrer täglichen Arbeit sind Projektressourcen häufig am Stadt oder am Reisen. Der mobile Arbeitsbereich **Projektzeiterfassung** ermöglicht Benutzern, die verrechenbare oder nicht verrechenbare Zeit im Projekt auf dem mobilen Gerät ihrer Wahl einzugeben. Deshalb kann die Projektressource die Zeiterfassungen jederzeit und überall erfassen. Sie können auch Zeiterfassungen anzeige , die bereits erfasst wurden. 

Speziell im mobilen Arbeitsbereich **Projektzeiterfassung**, können Benutzer von mobilen Arbeitsbereichen diese Aufgaben ausführen:

-   Für ein beliebiges ausgewählte Datum geben Sie die Anzahl der Stunden ein, die für eine bestimmte Aufgabe aufgewendet wurden.
-   Suche über den Projektnamen oder Debitor, um das Projekts zu suchen, für das Sie eine Zeit eingeben möchten.
-   Geben Sie die Kategorie und dir Aktivität für die Zeit an, die Sie verbracht haben.
-   Erfassung der verrechenbaren oder nicht-verrechenbaren Zeit für das Projekt.
-   Geben Sie optional alle externen oder internen Kommentare ein.

## <a name="prerequisites"></a>Voraussetzungen
Die Voraussetzungen unterscheiden sich basierend auf der Version von Microsoft Dynamics 365, die für Ihre Organisation bereitgestellt wurde.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Finance and Operations verwenden
Wenn Microsoft Dynamics 365 for Finance and Operations für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator den mobilen Arbeitsbereich **Projektzeiterfassung** veröffentlichen. Anweisungen finden Sie unter [Einen mobilen Arbeitsbereich veröffentlichen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Voraussetzungen, wenn Sie Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später verwenden.
Wenn Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder später für Ihre Organisation bereitgestellt wurde, muss der Systemadministrator die folgenden Voraussetzungen erfüllen. 

<table>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementieren Sie KB 4018050.</td>
<td>Systemadministrator</td>
<td>4018050 KB ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Projektzeiterfassung</strong> enthält. Um KB 4018050 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Laden Sie den Metadatenhotfix für Microsoft Dynamics Lifecycle Services (LCS) herunter</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das die <strong>ApplicationSuite</strong> und <strong>ProjectMobile</strong> Modelle enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Das bereitstellbare Paket übernehmen</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td><strong>Mobiler Arbeitsbereich für Projektzeiterfassung</strong> veröffentlichen.</td>
<td>Systemadministrator</td>
<td>Siehe <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Einen mobilen Arbeitsbereich veröffentlichen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Herunterladen und Installieren der mobilen App

Laden Sie die mobile App für Dynamics 365 for Unified Operations herunter und installieren Sie diese:

-   [Für Androide-Smartphones](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Für iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Bei der mobile App anmelden
1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die URL Dynamics 365 ein.
3.  Bei der erstmaligen Anwendung werden Sie nach Ihrem Benutzernamen und dem Kennwort gefragt. Geben Sie Ihre Anmeldeinformationen ein.
4.  Nachdem Sie sich angemeldet haben, werden verfügbare Arbeitsbereiche für Ihr Unternehmen angezeigt. Beachten Sie, dass Sie, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, die Liste der mobilen Arbeitsbereiche aktualisieren müssen.

[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Geben Sie Zeit ein, indem Sie den mobilen Arbeitsbereich Projektzeiterfassung verwenden
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Projektzeiterfassung**.
2.  Wählen sie **Zeiterfassung** Die Kalendertagen der aktuellen Woche werden angezeigt.
3.  Für ein ausgewähltes Datum wählen Sie **Aktivitäten** &gt; **Neuer Eintrag** aus.
4.  Geben Sie die Anzahl der Stunden ein.
5.  Wählen Sie das Projekt für die Zeiterfassung aus. Sie sehen eine Liste der Projekte, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Sie unter [Mobile Plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
6.  Wenn Ihr Projekt nicht in der Liste ist, wählen Sie **Suche** aus. Suchen Sie nach Name oder Wechseln Sie zur Suche nach Projektnamen oder Debitor.
7.  Wählen Sie eine Kategorie. Sie sehen eine Liste der Kategorien, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Sie unter [Mobile Plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
8.  Wenn Ihre Kategorie nicht in der Liste ist, wählen Sie **Suche** aus. Suche nach Kategorie oder nach Kategorienamen.
9.  Wählen Sie eine Aktivität aus. Sie sehen eine Liste der Aktivitäten, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen finden Sie unter [Mobile Plattform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
10. Wenn Ihre Aktivität nicht in der Liste ist, wählen Sie **Suche** aus. Suche nach Aktivitätennummern oder nach Kostenträger.

11. Positionseigenschaft auswählen.
12. Geben Sie optional alle externen oder internen Kommentare ein.
13. Wählen Sie **Fertig**.

