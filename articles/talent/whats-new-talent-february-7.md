---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (7. Februar 2019)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 Talent entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
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
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4005a8745e46a23fe16b94cab7b7aeb20f84035
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009761"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (7. Februar 2019)

[!include [banner](includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die in Talent entweder neu oder geändert sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

### <a name="interview-scheduling-enhancements"></a>Gesprächsplanung und -verbesserungen
Es wurden Verbesserungen an der End-to-End-Gesprächsplanungsumgebung vorgenommen. Sie können die Kalenderverfügbarkeit eines internen Kandidaten nun anzeigen und den internen Kalender des Kandidaten für Zeitplanempfehlungen verwenden. Weitere Informationen finden Sie unter [Gesprächsplanung und -rückmeldung](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Stellenausschreibung auf LinkedIn – Fehler beim Unternehmensabgleich korrigiert
Ein Problem wurde behoben, bei dem Stellen, die von Attract auf LinkedIn veröffentlicht wurden, mit einem falschen Unternehmensnamen angezeigt wurden. Weitere Informationen finden Sie unter [Erstellen, Genehmigen und Buchen von Stellen in Attract](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Stellenstandort-URL in den Administratoreinstellungen angezeigt
Die URL der Stellenstandorts-Startseite wird nun in den **Administratoreinstellungen** unter **Verwaltung der Website mit Stellenangeboten**.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

**Build 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Unterstützung für mehrere Vergütungsstufen bei Stellen
Diese Änderung ermöglicht die Definition mehrerer Vergütungsstufen für eine Stelle, wodurch unterschiedliche feste Mitarbeitervergütungsbereiche für Pläne unter Verwendung derselben Stelle genutzt werden können. 

Beispiel:    
*Stelle* - Kundenbetreuer *Verknüpfte Vergütungsstufen:* B1 und B2 - Für jede Stufe ist ein Wertebereich definiert. B1 = Min. 50.000, Mittel 60.000, Max. 75.000 und B2 = Min. 65.000, Mittel 74.000, Max. 85.000. Wenn Sie feste Vergütung für Mitarbeiter basierend auf definierten Berechtigungsregeln erstellen, kann jeder feste Plan auf dieselbe Stelle und auf verschiedenen Stufen in der Stelle verweisen. Dadurch können Pläne in unterschiedlichen Regionen/Unternehmen definiert werden und auf dieselbe Stelle, jedoch auf verschiedene Bereichen verweisen, ohne dass Stellen dupliziert werden müssen, um diese Differenzen darzustellen.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Feld „Vergütungsstufe“ wurde zur Entität „Feste Mitarbeitervergütung“ hinzugefügt 
Mit diesem Update wurde der Entität „Feste Mitarbeitervergütung“ ein Feld **Vergütungsstufe** hinzugefühgt. Durch diesen Zusatz wird es einfacher, feste Vergütungspläne zu aktualisieren. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Update der Stellenfamilie, wenn Sie neue Positionen erstellen und aktualisieren
Wenn Sie die Stelle einer Position ändern, wird die **Stellenfamilie** jetzt auf den Standardwert für die ausgewählte Stelle festgelegt.

### <a name="performance-improvements-when-rendering-workspaces"></a>Leistungsverbesserungen beim Rendern von Arbeitsbereichen
Die Analyseregisterkarten in Arbeitsbereichen werden jetzt nur geladen, wenn Sie auf die Webseiten zugreifen. Ein Indikator wird während des ersten Renderings der Seite in der oberen linken Ecke der Seite angezeigt.
