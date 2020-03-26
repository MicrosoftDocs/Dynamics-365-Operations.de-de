---
title: Neuerungen oder Änderungen in Dynamics 365 Human Resources (10. März 2020)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources neu oder geändert wurden.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c1a9f10a434343e4c9c8a42ec5c0b7a1a18ad36
ms.sourcegitcommit: 437170338c49b61bba58f822f8494095ea1308c2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/12/2020
ms.locfileid: "3124015"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Neuerungen oder Änderungen in Dynamics 365 Human Resources (10. März 2020)

Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Dynamics 365 Human Resources sind. Änderungen gelten für Build-Nummer 8.1.2985. Die Zahlen in Klammern in einigen Überschriften beziehen sich zur Referenz auf die LCS-Supportnummern.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Zugriff auf den Bericht zur Analyse der Qualifikationslücke nicht möglich (394460)

Dieser Bericht wird nicht in Dynamics 365 Human Resources unterstützt. Der Menüpunkt zum Drucken des SSRS-Berichts wird entfernt.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Falsche Meldung beim Zugriff auf die Seite Erste Schritte (417950)

Mit dieser Änderung verbirgt die Sicherheit diesen Menüpunkt, wenn Sie keinen Zugriff auf das Formular haben.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Optimierte Aufgabenpflege für Mitarbeiter (380538)

Das Wartungsformular für Arbeitsaufgaben listet alle Aufgaben für einen Mitarbeiter in Bezug auf Onboarding, Offboarding, Übergänge und Geschäftsprozesse auf. Sie können jetzt den Aufgabenstatus entweder neu zuweisen, löschen oder aktualisieren.

Beispiel: Benjamin Martin ist ein Leistungsadministrator. Während des Onboarding von Mitarbeitern werden Aufgaben für Benjamin erstellt, um die Leistungsauswahl des neuen Mitarbeiters zu überprüfen. Benjamin hat vergangene Aufgaben, die er erledigt hat, und zukünftige Aufgaben, die er erledigen muss. Benjamin beschließt, das Unternehmen zu verlassen, daher müssen seine Aufgaben entweder neu zugewiesen oder entfernt werden. Das Formular zur Aufgabenpflege (im Aktionsbereich des Formulars **Arbeitskraft**) ermöglicht es, alle Aufgaben von Benjamin einer anderen Arbeitskraft zuzuweisen oder zu entfernen.  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service Lösung ist jetzt mit den folgenden Änderungen verfügbar:

| Beschreibung | Rückgeld |
| --- | --- |
| **Stelle/Position** Entitätsänderungen | <ul><li>**Kompensationsregion** hinzugefügt</li>|
| **Dimension der Jobposition** Entität hinzugefügt | <ul><li>**Finanzdimensionen** hinzugefügt</li>
| **Arbeitskraft** Entitätsänderungen | <ul><li>**Namensfolge** hinzugefügt</li><li>**Arbeitet von zu Hause** hinzugefügt</li><li>**Sprache** hinzugefügt</li><li>**Dienstalterdatum** hinzugefügt</li><li>**Jahrestag** hinzugefügt</li><li>**Ursprüngliches Einstellungsdatum** hinzugefügt</li></ul> |
| **Beschäftigung** Entitätsänderungen | <ul><li>**Finanzdimensionen** hinzugefügt</li><li>**Kündigungsgrund** hinzugefügt</li><li>**Kündigungsdatum** umbenannt von **Übergangsdatum**</li><li>**Probezeitdatum** hinzugefügt</li></ul> |
| **Arbeitskraftadresse** Entitätsänderungen | <ul><li>**Straße** hinzugefügt</li><li>**Adresszeile 1**, **Adresszeile 2**, und **Adresszeile 3** als veraltet markiert</li></ul> |
| Neue variable Vergütung-Einrichtungsentitäten | <ul><li>**Plantyp für variable Vergütung**</li><li>**Plan für variable Vergütung**</li><li>**Übertragungsregeln**</li><li>**Variable Planstufe zur Vergütung**</li></ul> |
| Neue **Arbeitskraftkalender-Beschäftigung** Entität | <ul><li>**Arbeitkraftkalender-Entität** hinzugefügt</li></ul> |
| Neue **Lohnpositionsdetail** Entität | <ul><li>**Lohnpositionsdetail** hinzugefügt</li></ul> |
| Neue **Titel** Entität | <ul><li>**Titel** hinzugefügt</li></ul> Die neue Entität **Titel** ist enthalten in Common Data Service wird aber aktuell nicht aus den Entitäten **Berufliche Stellung** oder **Job** referenziert. |

> [!NOTE]
> Finanzielle Dimensionen für Positionen und Beschäftigung bieten eine Integration in eine Richtung für Aktualisierungen von der Personalabteilung bis Common Data Service. Aktualisierungen der Finanzdimensionen werden derzeit nicht synchronisiert von Common Data Service zu Human Resources.

In den nächsten Wochen werden diese Entitätsänderungen in allen Umgebungen verfügbar sein. So installieren Sie die neueste Common Data Service Lösung für Human Resources manuell:

1.  Gehen Sie zum [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).

2.  Wählen Sie **Umgebungen** aus.

3.  Suchen Sie die Umgebung, die Sie aktualisieren möchten. Die Umgebung sollte dem **Umgebungsname** im Abschnitt **Common Data Service Information** im Formular **Über** in Human Resources entsprechen.

4.  Wählen Sie die Umgebung aus, um die Umgebungsdetails anzuzeigen.

5.  Wählen Sie auf der Aktivitätsleiste oben **Lösungen verwalten**. Ein neues Browserfenster wird geöffnet und navigiert zu **Dynamics 365 Admin Center** im Kontext Ihrer Umgebung.

6.  Wählen Sie in der Liste **Lösung** den Eintrag **Dynamics 365 Human Resources Anker**.

7.  Wählen Sie **Aktualisierung**, um die neueste Lösung anzuwenden.

## <a name="in-preview"></a>Vorschau

Die folgenden Vorschaufunktionen sind am 3. Februar 2020 verfügbar:

- **Urlaubs- und Abwesenheitsfunktion** - Weitere Informationen finden Sie unter [Urlaub- und Abwesenheitsverwaltung, Vorschaufunktion](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Vorschaufunktion für das Leistungsmanagement** – Weitere Informationen, einschließlich bekannter Probleme, finden Sie unter [Übersicht über das Leistungsmanagement](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Bald verfügbar

### <a name="platform-update-33"></a>Plattformupdate 33

- Ganzseitige Apps (Vorschau) – Diese Vorschaufunktion, für die Sie die Funktion Gespeicherte Ansichten aktivieren müssen, ermöglicht Power Apps und Apps von Drittanbietern, die über das Dashboard als ganzseitige Erlebnisse hinzugefügt werden.

- Gespeicherte Ansichten (Vorschau) – Diese Vorschaufunktion ermöglicht gespeicherte Ansichten, was eine erhebliche Verbesserung des Personalisierungssubsystems darstellt. Mit dieser Funktion können Benutzer mehrere benannte Sätze von Personalisierungen pro Seite haben. Sie können Ansichten auch für Sicherheitsrollen veröffentlichen.

- Optimiert ist eine vonr Filtererfahrung – Diese Funktion ermöglicht eine optimierte ist eine von Filtererfahrung, die die Eingabe mehrerer Filterwerte erleichtert, einen einfacheren Mechanismus zum Entfernen einzelner oder aller Filterwerte bietet und eine kompaktere und intuitivere Visualisierung von Filterwerten ist.

- Empfohlene Felder – Benutzer müssen häufig Felder zu einem Raster oder einer Seite hinzufügen. Dies kann bei so vielen verfügbaren Feldern schwierig sein. Anstatt eine große Liste durchsuchen zu müssen, kann das System mit dieser Funktion eine Reihe empfohlener Felder anzeigen, die darauf basieren, was andere Benutzer in ähnlichen Szenarien am häufigsten hinzufügen.

- Feste Standardaktionen in Rastern – Diese Funktion stellt sicher, dass die Standardaktion in einem Raster mit einer bestimmten Spalte in einem Raster verknüpft ist, unabhängig davon, ob diese Spalte verschoben oder ausgeblendet wird.