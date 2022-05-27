---
title: Erstellen oder Bearbeiten eines Kalenders
description: Teamkalender erstellen und anpassen in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0679a69b4d607f9d466474026d5dd0ceef0dad6f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692197"
---
# <a name="view-team-and-company-calendars"></a>Team- und Unternehmenskalender anzeigen

>[!Important]
>Die in diesem Thema beschriebene Funktionalität ist derzeit für Kunden der eigenständigen Version von Dynamics 365 Human Resources verfügbar. Einige oder die gesamten Funktionen werden in einem zukünftigen Release der Finance-Infrastruktur nach Finance-Version 10.0.26 verfügbar sein.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Sie können Teamkalender und Unternehmenskalender in Dynamics 365 Human Resources anzeigen. Teamkalender zeigen nur Direktunterstellte an, wie in der Hierarchie definiert.

## <a name="view-your-team-calendar-as-an-employee"></a>Teamkalender als Mitarbeiter anzeigen

- Im **Mitarbeiter-Self-Service**-Arbeitsbereich wählen Sie **Teamabwesenheitskalender** unter **Zusammenfassung**.

## <a name="view-your-team-calendar-as-a-manager"></a>Teamkalender als Manager anzeigen

1. Wählen Sie auf der Startseite **Mitarbeiter-Self-Service** **Mein Team** aus.

2. Wählen Sie **Urlaub und Abwesenheit** und dann **Managerabwesenheitskalender anzeigen**.

Manager können auch über **Ausstehende Anfragen meines Teams**, **Genehmigte Freizeit** und **Freizeitanfragen** auf den Teamkalender zugreifen. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Zeigen Sie Ihren Abwesenheitsmanager-Kalender als Abwesenheitsmanager an

> [!NOTE]
> Um den Kalender des Abwesenheitsmanagers anzuzeigen, müssen Sie zuerst die **(Vorschau) Abwesenheitsmanager zur Verwaltung des Urlaubs** Funktion in der Funktionsverwaltung aktivieren. Weitere Informationen zur Aktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

Benutzer in der Rolle des Abwesenheitsmanagers können Urlaubsanträge in ihrem Kalender anzeigen. Wenn Sie auf den Kalender zugreifen wollen, führen sie die folgenden Schritte aus.

1. Wählen Sie im Arbeitsbereich **Mitarbeiter-Self-Service** **Abwesenheitsverwaltung** und dann **Kalender für Abwesenheitsmanager** aus.

2. Geben Sie im Feld **Datum** die gewünschten Daten ein.

3. Aktualisieren Sie die Ansichtsoptionen nach Bedarf.

Der Kalender des Abwesenheitsmanagers zeigt alle Datensätze der Mitarbeiter, die dem Abwesenheitsmanager in der Abwesenheitshierarchie berichten.

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

Die Kalenderkonfiguration auf der Seite **Urlaubs- und Abwesenheitsparameter** bestimmt die verfügbaren Ansichtsoptionen.

Sie können Kalender auch nach Manager oder Abteilung filtern. Die primäre Positionszuweisung bestimmt die Mitarbeiter, die angezeigt werden, wenn diese Filter gesetzt werden. 

> [!IMPORTANT]
> Sie können die **Unternehmensübergreifende Urlaubsansicht** Funktion in der Funktionsverwaltung aktivieren. Dann müssen Sie die Funktion auf der Seite **Freigegebene Human Resources-Parameter** aktivieren, um den Filter für juristische Personen in Kalendern anzuzeigen. Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsparameter konfigurieren](hr-leave-and-absence-parameters.md).
> 
> Sie können im Kalender nach juristischen Personen filtern. Wenn Sie alle Mitarbeiter unabhängig von der juristischen Person sehen möchten, deaktivieren Sie das Filterfeld und drücken Sie die **Eingabetaste**. 

Informationen zu Kalendereinstellungen finden Sie unter [Konfigurieren Sie die Kalenderparameter](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
