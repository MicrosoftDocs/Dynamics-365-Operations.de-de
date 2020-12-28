---
title: Erstellen oder Bearbeiten eines Kalenders
description: Teamkalender erstellen und anpassen in Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2ec767a868d5c76b57465c451b8cc893b8b0a56b
ms.sourcegitcommit: ffb5998e611b83c2e4f98323f39e3e8f6419c652
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2020
ms.locfileid: "4418763"
---
# <a name="view-team-and-company-calendars"></a>Team- und Unternehmenskalender anzeigen

Sie können Teamkalender und Unternehmenskalender in Dynamics 365 Human Resources anzeigen. Teamkalender zeigen nur Direktunterstellte an, wie in der Hierarchie definiert.

## <a name="view-your-team-calendar-as-an-employee"></a>Teamkalender als Mitarbeiter anzeigen

1. Im **Mitarbeiter-Self-Service**-Arbeitsbereich wählen Sie **Teamabwesenheitskalender** unter **Zusammenfassung**.

## <a name="view-your-team-calendar-as-a-manager"></a>Teamkalender als Manager anzeigen

1. Wählen Sie auf der Startseite **Mitarbeiter-Self-Service** **Mein Team** aus.

2. Wählen Sie **Urlaub und Abwesenheit** und dann **Managerabwesenheitskalender anzeigen**.

Manager können auch über **Ausstehende Anfragen meines Teams**, **Genehmigte Freizeit** und **Freizeitanfragen** auf den Teamkalender zugreifen. 

## <a name="view-a-company-calendar"></a>Einen Unternehmenskalender anzeigen

Personen, die in der Personalabteilung tätig sind, können Unternehmenskalender anzeigen. In den Unternehmenskalendern werden alle Mitarbeiter angezeigt. Standardmäßig zeigt der Kalender das heutige Datum plus 28 Tage an, Sie können jedoch den Datumsbereich ändern. Sie können den Kalender auch nach **Name**, **Personalnummer** und **Abwesenheitstyp** filtern.

1. In dem Arbeitsbereich **Urlaub und Abwesenheit** wählen Sie **Verknüpfen**.

2. Wählen Sie **Urlaubs- und Abwesenheitskalender**.

Personalrollen können auch über auf den Unternehmenskalender **Urlaubs- und Abwesenheitsanträge**, **Genehmigte Freizeit**, und **Freizeitanfragen** zugreifen. 

Kalender enthalten jetzt zusätzliche Filter und Optionen. Alle Kalender enthalten Ansichtsoptionen für:

- Genehmigte Anforderungen
- Ausstehende Anträge
- Mitarbeiter mit Urlaubsanträgen
- Mitarbeiter ohne Urlaubsanträge
- Mitarbeiter-Geburtstage
- Anforderungen von arbeitsfreier Zeit 
- Beurlaubungsanforderungen

Die Kalenderkonfiguration in den Parametern Urlaub und Abwesenheit bestimmt die verfügbaren Ansichtsoptionen.

Sie können Kalender auch nach Manager oder Abteilung filtern. Die primäre Positionszuweisung bestimmt die Mitarbeiter, die angezeigt werden, wenn diese Filter gesetzt werden. 

>[!IMPORTANT]
>Urlaub und Abwesenheit wird in verschiedenen Unternehmen derzeit in der Vorschau angezeigt. Sie müssen es in Ihrer **Sandbox**-Umgebung aktivieren. Weitere Informationen zum Aktivieren der Vorschaufunktionen finden Sie unter [Funktonen verwalten](hr-admin-manage-features.md).<br><br>
>Dann müssen Sie die Funktion in **Freigegebene Human Resources-Parameter** aktivieren, um den Filter für juristische Personen in Kalendern anzuzeigen. Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsparameter konfigurieren](hr-leave-and-absence-parameters.md).<br><br>
>Sie können im Kalender nach juristischen Personen filtern. Wenn Sie alle Mitarbeiter unabhängig von der juristischen Person sehen möchten, deaktivieren Sie das Filterfeld und drücken Sie die Eingabetaste. 

Informationen zu Kalendereinstellungen finden Sie unter [Konfigurieren Sie die Kalenderparameter](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

