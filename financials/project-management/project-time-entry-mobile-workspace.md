---
title: "Mobiler Arbeitsbereich für die Projektzeiterfassung für die Microsoft Dynamics 365 for Operations-App"
description: "Dieses Thema enthält Informationen zur Projektzeiterfassungs im mobilen Arbeitsbereich. Dieser Verknüpfung ermöglicht Benutzern Zeit für ein Projekt einzugeben und zu speichern, indem sie das mobile Gerät verwenden."
author: annbe
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e3e0be36c045acc3750efbb739d79d81ab937c65
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="project-time-entry-mobile-workspace"></a>Mobiler Arbeitsbereich für Projektzeiterfassung

[!include[banner](../includes/banner.md)]

"[!include[banner](../includes/banner.md)]"


Dieses Thema enthält Informationen zur Projektzeiterfassung im mobilen Arbeitsbereich für Dynamics 365 for Operations mobile App. Dieser Verknüpfung ermöglicht Benutzern Zeit für ein Projekt einzugeben und zu speichern, indem sie das mobile Gerät verwenden.

<a name="overview-of-the-project-time-entry-mobile-workspace"></a>Übersicht über die Projektzeiterfassung im mobilen Arbeitsbereich
---------------------------------------------------

Im Rahmen ihrer täglichen Arbeit sind Projektressourcen häufig am Stadt oder am Reisen. Der mobile Arbeitsbereich **Projektzeiterfassung** ermöglicht Benutzern, die verrechenbare oder nicht verrechenbare Zeit im Projekt auf dem mobilen Gerät ihrer Wahl einzugeben. Deshalb kann die Projektressource die Zeiterfassungen jederzeit und überall erfassen. Sie können auch Zeiterfassungen anzeige , die bereits erfasst wurden. 

Speziell enthält der mobile Arbeitsbereich **Projektzeiterfassung** diese Funktionen:

-   Für ein beliebiges ausgewählte Datum geben Sie die Anzahl der Stunden ein, die für eine bestimmte Aufgabe aufgewendet wurden.
-   Suche über den Projektnamen oder Debitor, um das Projekts zu suchen, für das Sie eine Zeit eingeben möchten.
-   Geben Sie die Kategorie und dir Aktivität für die Zeit an, die Sie verbracht haben.
-   Erfassung der verrechenbaren oder nicht-verrechenbaren Zeit für das Projekt.
-   Geben Sie optional alle externen oder internen Kommentare ein.

Um den mobilen Arbeitsbereich **Projektzeiterfassung** zu implementieren, finden Sie die Details in den folgenden Abschnitten in diesem Thema.

## <a name="prerequisites"></a>Voraussetzungen
Bevor Sie den mobilen Arbeitsbereich **Projektzeiterfasssung** verwenden können, überprüfen Sie, ob Ihr Systemadministrator die folgenden Voraussetzungen bereitgestellt hat.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Voraussetzung</th>
<th>Rolle</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations Version 1611 mit Plattformaktualisierung 3 oder späterem muss implementiert werden.</td>
<td>Systemadministrator</td>
<td>Wenn Sie nicht bereits Dynamics 365 for Operations in Ihrer Organisation bereitgestellt haben, sollte Ihr Systemadministrator <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations bereitstellen, Testumgebung</a> sehen.</td>
</tr>
<tr class="even">
<td>4018050 KB muss implementiert werden.</td>
<td>Systemadministrator</td>
<td>4018050 KB ist ein X++-Aktualisierungs- oder -Metadatenhotfix, der den mobilen Arbeitsbereich <strong>Projektzeiterfassung</strong> enthält. Um KB 4018050 muss Ihr Systemadministrator folgende Schritte ausführen.
<ol>
<li>Herunterladen von KB 4018050 von Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installieren Sie den Metadatenhotfix</a>.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Erstellen eines zur Bereitstellung geeigneten Paket</a>, das die <strong>ApplicationSuite</strong> und <strong>ProjectMobile</strong> Modelle enthält und laden Sie dann das zur Bereitstellung geeignete Paket in LCS hoch.</li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Anwenden eines Bereitstellungspaket</a> auf einem Microsoft Dynamics 365 for Operations-System</li>
</ol></td>
</tr>
<tr class="odd">
<td>Der mobile Arbeitsbereich <strong>Projektzeiterfassung</strong> muss in der Dynamics 365 for Operations Mobile App veröffentlicht sein.</td>
<td>Systemadministrator</td>
<td><ol>
<li>Starten Sie Dynamics 365 for Operations in Ihrem Browser.</li>
<li>Auf der Seite <strong>Systemparameter</strong> wählen Sie auf der Registerkarte <strong>Verwalten von mobilen Arbeitsbereichen</strong> den Arbeitsbereich <strong>Projektzeiterfassung</strong> aus.</li>
<li>Klicken Sie auf <strong>Mobilen Arbeitsbereich veröffentlichen</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>Laden Sie Dynamics 365 for Operations mobile App herunter und installieren Sie diese.
Laden Sie die App im App Store herunter und installieren Sie die Microsoft Dynamics 365 for Operations-App.

-   Für Android - [Dynamics 365 for Operations im Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Für iPhone: [Dynamics 365 for Operations im iTunes-App-Store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Melden Sie sich an und nutzen Sie Dynamics 365 for Operations mobile App.
1.  Starten Sie die App auf Ihrem mobilen Gerät.
2.  Geben Sie die Dynamics 365 for Operations URL ein.
3.  Geben Sie das Unternehmen ein. Geben Sie beispielsweise **USMF** ein.
4.  Wenn Sie sich zum ersten Mal anmelden, werden Sie nach einem Benutzernamen und einem Kennwort für Ihr Microsoft Dynamics 365 for Operations Konto gefragt. Geben Sie Ihre Anmeldeinformationen ein.
5.  Nachdem Sie sich angemeldet haben, sehen Sie verfügbaren Arbeitsbereiche für Ihr Unternehmen. Beachten Sie, dass, wenn Ihr Systemadministrator einen neuen Arbeitsbereich später veröffentlicht, aktualisieren Sie die Liste der Arbeitsbereiche.

[![Zum Aktualisieren ziehen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Geben Sie Zeit ein, indem Sie den mobilen Arbeitsbereich Projektzeiterfassung verwenden
1.  Wählen Sie auf Ihrem mobilen Gerät den Arbeitsbereich **Projektzeiterfassung**.
2.  Wählen sie **Zeiterfassung** Sie finden die Kalendertagen der aktuellen Woche.
3.  Für ein ausgewähltes Datum wählen Sie **Aktivitäten** &gt; **Neuer Eintrag** aus.
4.  Geben Sie die Anzahl der Stunden ein.
5.  Wählen Sie das Projekt für die Zeiterfassung aus. Sie sehen eine Liste der Projekte, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sollten Entwickler sehen [Dynamics 365 for Operations mobile Plattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
6.  Wenn Ihr Projekt nicht in der Liste ist, wählen Sie **Suchen** aus, um eine Suche in Dynamics Online 365 for Operations auszuführen. Suchen Sie nach Name oder Wechseln Sie zur Suche nach Projektnamen oder Debitor.
7.  Wählen Sie eine Kategorie. Sie sehe eine Liste der Kategorien, die in der App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sollten Entwickler sehen [Dynamics 365 for Operations mobile Plattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
8.  Wenn Ihre Kategorie nicht in der Liste ist, wählen Sie **Suchen** aus, um eine Suche in Dynamics Online 365 for Operations auszuführen. Suche nach Kategorie oder nach Kategorienamen.
9.  Wählen Sie eine Aktivität aus. Sie sehen eine Liste der Aktivitäten, die in Ihrer App zur Offline-Nutzung geladen werden. Standardmäßig sind 50 Artikel geladen, aber ein Entwickler kann diese Nummer ändern. Weitere Informationen sollten Entwickler sehen [Dynamics 365 for Operations mobile Plattform](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform).
10. Wenn Ihre Aktivität nicht in der Liste ist, wählen Sie **Suchen** aus, um eine Suche in Dynamics Online 365 for Operations auszuführen. Suche nach Aktivitätennummern oder nach Kostenträger.
11. Positionseigenschaft auswählen.
12. Geben Sie optional alle externen oder internen Kommentare ein.
13. Wählen Sie **Fertig**.






