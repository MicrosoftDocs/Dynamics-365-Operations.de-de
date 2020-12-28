---
title: Neuerungen oder Änderungen in Dynamics 365 Talent (7. Januar 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Talent neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
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
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461288"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Talent (7. Januar 2020)

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Talent sind.

## <a name="changes-in-attract"></a>Änderungen in Attract

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Änderungen in Onboard

Diese Version enthält kleinere Fehlerkorrekturen für Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-Änderungen

Die in diesem Abschnitt beschriebenen Änderungen gelten für Buildnummer 8.1.2697. Die Zahlen in Klammern in einigen Überschriften beziehen sich auf Supportnummern in Microsoft Dynamics Lifecycle Services (LCS).

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a>Kann keine Arbeitskräfte löschen, die keine Beschäftigungsdatensätze haben – (386157)

Diese Änderung fügt eine Löschoption im Formular **Arbeitskräfte ohne Beschäftigung** hinzu. Arbeitskräfte erscheinen in dieser Form, wenn für die Arbeitskraft keine zukünftigen, aktiven oder historischen Beschäftigungen existieren. In dieser Version ist das Löschen nur für Systemadministratoren aktiviert. In der Version nächste Woche wird jedoch die Sicherheit so aktualisiert, dass alle Benutzer mit der Rolle des Personalassistenten Mitarbeiter ohne Beschäftigung entfernen können. Sie können diese Änderungen auch manuell vornehmen, indem Sie die folgenden Schritte ausführen.

1. Gehen Sie zu **Sicherheitskonfiguration**.
2. Filtern Sie in der Registerkarte **Privilegien** die Liste der **Privilegien** nach **Arbeitskräfte pflegen**.
3. Wählen Sie in der Spalte **Verweise** **Menüpunkte anzeigen**.
4. Wählen Sie in **Menüpunkte anzeigen** **HCM-Arbeitskräfte ohne Beschäftigung**.
5. Stellen Sie die Erlaubnis zum **Löschen** auf Erteilen.
6. Wählen Sie die Registerkarte **Unveröffentlichte Objekte** aus.
7. Wählen Sie **Alle veröffentlichen** aus.
