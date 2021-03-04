---
title: Daten aus Attract und Onboard exportieren
description: Exportieren Sie Daten aus Dynamics 365 Talent – Attract und Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461226"
---
# <a name="export-data-from-attract-and-onboard"></a>Daten aus Attract und Onboard exportieren

[!include [banner](includes/banner.md)]

Wie in [Ruhestand Dynamics 365 Talent: Attract und Dynamics 365 Talent: OnboardApps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps) angekündigt, ziehen wir Dynamics 365 Talent: Attract und Dynamics 365 Talent: Onboard am 1. Februar 2022 zurück. Um die Migration auf ein anderes Produkt zu erleichtern, bieten beide Apps jetzt Datenexportfunktionen.

## <a name="export-data-from-attract"></a>Daten aus Attract exportieren

Sie können Ihre Daten exportieren, ohne den Zugriff auf Ihre Umgebung einzuschränken. Möglicherweise möchten Sie dies zu Testzwecken ausführen oder um unsere Datenstruktur verstehen. Wenn Sie zur Migration bereit sind, beschränken Sie den Zugriff auf Ihre Attract-Umgebung mithilfe der Anweisungen nach diesem Verfahren. Stellen Sie sicher, dass Sie Ihre Daten erneut exportieren. 

1. Gehe zu [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Unter **Datenexport** wählen Sie **Datenexport anfordern**.

   ![[Einen Datenexport bei Attract anfodern](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Wenn das Meldungsfeld **Ihre Anfrage wird bearbeitet** erscheint, wählen Sie **OK**. Der Datenexport kann je nach Exportgröße bis zu 20 Minuten dauern.

4. Wenn Ihr Export abgeschlossen ist, wählen Sie die Schaltfläche **Herunterladen** daneben. 

   >[!NOTE]
   >Alle Datenexporte sind sieben Tage lang verfügbar, danach läuft der Link **Herunterladen** ab.</br>
   
Der Download enthält eine ZIP-Datei mit Ihren Attract-Daten, einschließlich der folgenden Ordner:

| Ordnername | Beschreibung |
| --- | --- |
| Administratoreinstellungen | Konfigurationen des Attract Admin Center. |
| Kandidaten | Alle Kandidaten, die zu Jobs oder Talentpools hinzugefügt wurden. |
| E-Mail-Vorlagen | Alle E-Mail-Vorlagen, die für die Umgebung konfiguriert wurden. |
| Jobangebotsvorlagenpaket | Alle erstellten Jobangebotspaketvorlagen sowie die zugehörigen Konfigurationen. |
| Regelsätze für Jobangebote |  Alle Regelsatzdateien, die zur Angebotsverwaltung hochgeladen wurden. |
| Jobangebotsvorlagen | Alle Jobangebot-Dokumentvorlagen, die für die Umgebung erstellt wurden. |
| Jobangebote | Alle erstellten Jobs. Gelöschte Jobs werden nicht exportiert. Die Unterordner enthalten Bewerbungsunterlagen mit Unterordnern für Bewerbungsanlagen und Angebotspakete, sofern zutreffend. |
| Jobangebotsvorlagen | Stellenprozessvorlagen, die in der Umgebung konfiguriert wurden. |
| Talentpools | Alle erstellten Talentpools, ihre Beitragslisten und die Kandidatenlisten für die Talentpools. |
| Arbeitskräfte | Liste aller Mitarbeiter, die in der Umgebung anwesend sind, sowie deren Rollen. |
| (Stammordner) | Eine JSON-Schemadatei, die die Datenstrukturfelder beschreibt. |

### <a name="restrict-access-to-attract"></a>Zugriff auf Attract beschränken

Wenn Sie zur Migration bereit sind, hindern Sie Nicht-Administratoren daran, auf Ihre Attract-Umgebung zuzugreifen, und exportieren Sie Ihre Daten.

>[!IMPORTANT]
>Die Einschränkung des Zugriffs auf Ihre Attract-Umgebung ist dauerhaft und kann nicht rückgängig gemacht werden. Wenn Sie möchten, dass Benutzer ohne Administratorrechte weiterhin auf Ihre Umgebung zugreifen können, überspringen Sie diesen Schritt.

1. Gehe zu [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Um zu verhindern, dass Nicht-Administratoren auf Ihre Attract-Umgebung zugreifen, klicken Sie unter **Zugriff auf diese App beschränken** auf **Zugriff jetzt beschränken**. Durch das Einschränken des Zugriffs werden auch alle aktiven Jobs, die veröffentlicht wurden, gelöscht.

   ![[Nicht-Admin-Zugriff auf Attract beschränken](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Wenn Sie die Warnung **Dies ist eine permanente Veränderung** sehen, wählen Sie **Zugriff einschränken**, um Nicht-Administrator-Benutzer dauerhaft aus dieser Umgebung auszuschließen. Wenn Sie diesen Schritt nicht ausführen möchten, wählen Sie **Abbrechen**.

   ![[Warnung, dass die Einschränkung des Zugriffs eine permanente Änderung ist](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Administratoren können weiterhin auf die Datenexport- und Personenberichtseiten zugreifen, nachdem Sie den Zugriff auf die Attract-Umgebung eingeschränkt haben.

## <a name="export-data-from-onboard"></a>Daten aus Onboard exportieren

Wenn Sie bereit sind, können Sie Vorlagen, Handbücher und Kandidatendaten von Onboard herunterladen.

1. Gehe zu [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Unter **Datenexport** wählen Sie **Datenexport anfordern**. 

   ![[Einen Datenexport von Onboard exportieren](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Wenn das Meldungsfeld **Ihre Anfrage wird bearbeitet** erscheint, wählen Sie **OK**. Der Datenexport kann je nach Exportgröße bis zu 20 Minuten dauern.

4. Wenn Ihr Export abgeschlossen ist, wählen Sie die Schaltfläche **Herunterladen** daneben. 

   ![[Datenexport aus Onboard herunterladen](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Ihr Datenexport ist sieben Tage lang verfügbar. Nach sieben Tagen ist der Link **Herunterladen** abgelaufen und Sie müssen einen neuen Export anfordern, wenn Sie Ihre Daten erneut herunterladen müssen. Wenn Sie einen neuen Datenexport starten, laufen alle vorhandenen Downloads ab, wenn der neue Export erfolgreich war.

Der Download ist eine .zip-Datei, die Folgendes enthält:

- Ein **Vorlagen**-Ordner, der Ihre Onboard-Vorlagen im Word-Dokumentformat enthält.

- Ein **Guides**-Ordner, der Ihre Onboard-Guides im Word-Dokumentformat enthält.

## <a name="see-also"></a>Siehe auch

[Einstellen von Dynamics 365 Talent: Attract und Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)

[!INCLUDE[footer-include](../includes/footer-banner.md)]