---
title: Übersicht über den Optimierungsratgeber
description: Dieser Artikel beschreibt, wie Sie den Optimierungsberater verwenden können, um eine optimale Konfiguration von Finanzen und Betrieb zu gewährleisten.
author: roxanadiaconu
ms.date: 07/23/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: fb71453c37572c4956d98d4309d3526a7fbc1124
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109039"
---
# <a name="optimization-advisor-overview"></a>Übersicht über den Optimierungsratgeber

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie Sie den Optimierungsberater verwenden können, um eine optimale Konfiguration von Finanzen und Betrieb zu gewährleisten.

## <a name="overview"></a>Übersicht

Falsche Konfiguration und Einstellung eines Moduls können die Verfügbarkeit von Anwendungsfunktionen, die Systemleistung und das reibungslose Funktionieren von Unternehmensabläufen beeinträchtigen. Die Qualität von Geschäftsdaten (beispielsweise die Korrektheit, Vollständigkeit und Sauberkeit der Daten) wirkt sich auch auf die Systemleistung und beispielsweise die Entscheidungsfähigkeit oder Produktivität einer Organisation aus.

Der Arbeitsbereich **Optimierungsratgeber** ist ein Tool, mit dem durch Poweruser, Business Analysten, Funktionsberater und IT-Supportfunktionen Probleme in der Modulkonfiguration und in Geschäftsdaten identifiziert werden können. Optimierungsratgeber schlägt Verfahren für Modulkonfiguration vor und bezeichnet die Daten, die veraltet oder falsch sind.

Optimierungsratgeber führt in regelmäßigen Zeitabständen eine Gruppe von Regeln für bewährte Methoden aus. Ein Standardregelsatz ist verfügbar, allerdings können auch Benutzer Regeln erstellen, die spezifisch auf die Anpassungen, Lösungen von den unabhängigen Softwareherstellern (ISVs) und Geschäftsdaten bestimmt sind. Weitere Informationen zum Erstellen von Regeln finden Sie unter [Regeln für Optimierungsberater erstellen](./create-rules-optimization-advisor.md).

Wenn ein Verstoß einer Regel erkannt wird, wird eine Optimierungsverkaufschance generiert und wird im Arbeitsbereich **Optimierungsratgeber** angezeigt. Ein Benutzer kann entsprechenden Korrektur-Aktivitäten direkt im Formular **Optimierungsratgeber** ausführen.

Verkaufschancen können abhängig vom Typ der Rüstzeit und Daten oder unternehmensübergreifend unternehmensspezifisch sein, die geprüft werden soll. Unternehmensübergreifende Verkaufschancen können alle Unternehmen angezeigt werden. Um die Verkaufschancen für ein bestimmtes Unternehmen anzuzeigen, müssen Sie zuerst das Unternehmen auswählen.

Standardsicherheits-Richtlinien gelten für Optimierungsverkaufschancen. Beispielsweise sind die Optimierungsverkaufschancen, die der Variante des **Lagerortverwaltung** zugeordnet sind, nur für Benutzer sichtbar, die den Zugriff zur Lagerortverwaltung haben und die Einstellung ändern.

Wenn Sie für manche Optimierungsverkaufschancen Maßnahmen ergreifen, berechnet das System die Auswirkungen der Verkaufschance in Bezug auf die Verringerung in der Laufzeit von Geschäftsprozessen. Leider ist diese Funktion nicht für alle Optimierungsverkaufschancen verfügbar.

Um mehr über den Optimierungsberater zu erfahren, sehen Sie sich das kurze [Optimierungsberater in Dynamics 365 Finance](https://www.youtube.com/watch?v=MRsAzgFCUSQ) Video an.

## <a name="optimization-rules"></a>Optimierungsregeln

Um die vollständige Liste der Optimierungsratgeberregeln anzuzeigen und zu sehen, wie oft die Regeln bewertet werden, wechseln Sie zu **Systemverwaltung** &gt; **Periodische Aufgaben** &gt; **Diagnoseüberprüfungsregeln verwalten**. Nur Regeln, die den Status **Aktiv** besitzen, werden ausgewertet. Die Bewertungshäufigkeit kann auf **Täglich**, **Wöchentlich**, **Monatlich** oder **Ungeplant** festgelegt werden.

Um die Bewertung von ungeplanten Regeln auszulösen, oder um periodische Regeln außerhalb des vordefinierten Zeitplans neu zu bewerten, wechseln Sie zu **Systemverwaltung** &gt; **Periodische Aufgaben** &gt; **Diagnoseüberprüfungsregel planen**. Im Dialogfeld **Diagnoseregelprüfung** wählen Sie eine Bewertungshäufigkeit aus. Alle Regeln, die die angegebenen Häufigkeit haben, werden neu bewertet.

Der aktuelle Satz von Optimierungsregeln kann in die folgenden Kategorien unterteilt werden.

### <a name="module-configuration-and-setup"></a>Modul-Einrichtung und -Konfiguration

Die Einrichtung der Lagerortverwaltung ist ein komplizierter Prozess. Um den Prozess zu vereinfachen, sind einige Regeln eingeführt worden, um die Korrektheit der Einstellungen zu überprüfen. Beispielsweise prüft eine Regel die Einstellung von Lagerortlagerplatzdirektiven für feste Produktvariantenlagerplätze für Aufträge und Umlagerungsaufträge.

Darüber hinaus überprüfen einige Regeln, ob mehrere Regeln-Funktionen, die ausgeführt wurden, geplant werden. Beispielsweise bestimmt eine Regel, ob Sie das Modul **Produktprogrammplanung** verwenden. Wenn die Regel festlegt, dass Sie das Modul nicht verwenden, wird eine Optimierungsverkaufschance  generiert, dass Sie die Planungsprozesse deaktivieren.

### <a name="system-configuration"></a>Systemkonfiguration

Wenn bestimmte Funktionen, die durch einen Konfigurationsschlüssel gesteuert wird, nicht verwendet werden, wird ein Optimierungsverkaufschancen-Bericht generiert, um vorzuschlagen, dass Sie den Variantenschlüssel deaktivieren. Beispiele von Konfiguration sind **Artikelgewicht**, **Budgetplanung**, **Projekt** und **Liste der genehmigten Kreditoren**.

### <a name="business-data-consistency-and-cleanup"></a>Datenkonsistenz und -Bereinigung

Wenn Masterdaten nicht korrekt sind (beispielsweise, wenn Sie Maßeinheitsumrechnungen für Einheiten aufweisen, die noch nicht definiert wurden, oder wenn Sie Maßeinheitsumrechnungen haben, die durch eine Division 0 haben \[Null\]), wird ein Optimierungsverkaufschancen-Bericht generiert, so dass Sie die Daten korrigieren. 

Wenn Sie zu viele Stapelverarbeitungsauftragsverlaufinträge haben, werden veraltete Artikel, geschlossene verfügbare Einträge für Lagerort aktivierte Artikel, usw. haben oder wenn diese Einträge und Artikel zu alt sind, werden Optimierungsverkaufschancen generiert, aus der Sie Daten bereinigen. Wenn Sie Ihre Daten führen, bereinigen Sie, Sie kann festgestellt, zur Verbesserung gesamte Systemleistung.

### <a name="best-practices"></a>Optimale Verfahren

Wenn Sie mehrere Verfahren nicht entsprechend den Geschäftsprozessen ausführen (beispielsweise, wenn Sie Bestandsvorabschluss ausführen, bevor der Bestand geschlossen ist, oder wenn Sie die geplanten Charge für die Erfassung im untergeordneten Sachkontos-Chargen-Übertragung), informieren Optimierungsverkaufschancen Sie die Abfrage und Verfahren, dass Sie ihn folgen.

## <a name="optimization-opportunities"></a>Optimierungsmöglichkeiten

Um die Optimierungsverkaufschancen anzuzeigen, die während der Bewertung der Optimierungsregeln generiert werden, öffnen Sie den Arbeitsbereich **Optimierungsberater**.

In diesem Arbeitsbereich können Sie weitere Informationen zu einer Verkaufschance anzeigen, indem Sie **Weitere Informationen** auswählen. Wenn Sie möchten, dass das System Aktivitäten ausführt und die Einstellung korrigiert. müssen Sie die entsprechenden Seiten nicht öffnen, wählen Sie **Aktion ausführen**.

Es gibt keinen Workflow für Optimierungsverkaufschancen. Nachdem Sie **Aktionen ausführen** augewählt haben oder einen Navigationspfad verwenden, der im Dialogfeld **Weitere Informationen** angegeben wird, verschwindet die Optimierungsverkaufschance aus der Liste. Wenn die Korrektur nicht vollständig ein Problem löst, wird die Verkaufschance erneut das nächste Mal generiert, an der die Regel ausgewertet wird.

Wenn eine Verkaufschance nicht für Ihre Rolle gilt, können Sie **Kontrollkästchen von meiner Liste** auswählen. Auch wenn die Regel nach dieser Verkaufschance erneut später ausgelöst wurde, finden Sie die Verkaufschance nicht in der Liste.

Um die Bewertung bestimmter Regeln zu deaktivieren, wählen Sie die Verkaufschance aus, die durch die Regel generiert wurde, und wählen dann **Analyse deaktivieren** aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Regeln für Optimierungsratgeber erstellen](./create-rules-optimization-advisor.md)

[Optimierungsberater in Dynamics 365 Finance (Video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
