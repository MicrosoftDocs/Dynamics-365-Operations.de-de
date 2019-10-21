---
title: 'Analytische Berichte in Microsoft Dynamics 365 Talent: Attract nutzen'
description: 'In diesem Thema werden die möglichen analytischen Berichte für Einstellungsprozess-Einblicke in Microsoft Dynamics 365 Talent: Attract beschrieben'
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: be62fe9a5021cfa83a465d316b182c0a154c0c50
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010008"
---
# <a name="use-analytic-reports"></a>Analytische Berichte verwenden

Analytische Berichte in Microsoft Dynamics 365 Talent: Attract ermöglichen eine standardmäßige Lösung (OOTB) für die Gewinnen von Einblicken in den Einstellungsprozess. Verfügbare Funktionen umfassen:

- **Stellen-Analyse** – Klicken Sie auf die Registerkarte **Analyse**  innerhalb einer Stelle, um die Metrik des Bewerbers für die Stelle zu sehen.
- **Analysehub:**  Klicken Sie auf **Analyse** auf der linken Navigation für die aggregierte Metrik innerhalb der Stellen.
- **Benutzerspezifische Sicherheit** Der Zugriff auf die Berichte wird durch Attract [Rollen](security-attract.md)  und die Stellenteilnehmerrolle gesteuert.
- **Übergreifende Filterung:** Klicken Sie auf die graphischen Elemente im Bericht, um andere Metriken anzuzeigen, die nach ausgewählten Daten gefiltert werden.

>[!NOTE] 
>- Diese Funktion befindet sich derzeit in der [Vorschau](access-preview-feature.md). Um sie zu testen, müssen Sie das [**Umfassendes Einstellungs-Add-On**](attract-comprehensive-hiring.md) haben.
>- Alle öffentlichen Vorschauberichte werden in Englisch angezeigt.
>- Berichte werden alle 3 Stunden aktualisiert. Die letzte Aktualisierungszeit  (in der lokalen Zeitzone) befindet sich am oberen Rand des Berichts. Aktualisierungszeiten sind ungefähre Angaben und basieren auf dem Datenvolumen und der Ressourcenauslastung in Ihrer Region.

## <a name="job-analytics"></a>Stellenanalysen

Stellen-Analyse-Berichte  geben eine Momentaufnahme des Einstellungsprozesses für eine Stelle.  Entscheidende Metrik enthalten:

- Aktive Bewerber nach Phase
- Bewerber-Quelle
- Bewerbertyp (intern versus extern)

## <a name="analytics-hub"></a>Analyse-Hub

Analyse-Hub-Berichte erstellen Daten der Stellen, um Trends im Einstellungsprozess darzustellen. Attract umfasst zwei OOTB-Berichte: Pipeline-Zusammenfassung und Trichter-Analyse.

### <a name="pipeline-summary"></a>Pipeline – Zusammenfassung

Der Pipeline-Zusammenfassungsbericht fasst Daten für offene Stellen zusammen. Entscheidende Metrik enthalten:

- Bewerber über alle Stellen nach Phasen
- Bewerber-Quelle
- Offene Stellen nach Funktionsstufe

### <a name="funnel-analysis"></a>Trichteranalysen

Der Trichter-Analysebericht fasst Daten für Stellen zusammen, die als besetzt abgeschlossen wurden. Entscheidende Metrik enthalten:

- Benötigte Zeit für die Besetzung der Stelle
- Umrechnungsmetrik (mit Maus darüber fahren)
- Angebotakzeptanzrate

Hinweis: Um die Zeit der Einstellung möglichst genau zu berichten, ist die Nutzung der [Angebotsverwaltung](offer-setup.md) empfohlen, eine Funktion, die Teil es empfohlen, die als Teil des umfassenden Einstellungs-Add-On verfügbar ist.

>[!TIP] 
>Probieren Sie, für zusätzliche Informationen mit der Maus über die Grafik zu fahren. Fahren Sie beispielsweise über **Aktive Bewerber** zeigen die Grafiken die durchschnittlichen Tage in der Phase an. Durch Analysieren dieser Informationen gewinnt man Einblicke, die zentral sind, um die notwendige Zeit für die Einstellung zu reduzieren und Personalbeschaffer die Möglichkeit zu geben, sich darauf zu konzentrieren, die erforderliche Zeit für jede Phase zu reduzieren.

## <a name="user-specific-security"></a>Benutzerspezifische Sicherheit

Attract Berichte stehen für die [Rollen](security-attract.md) Administratoren, nur Lesezgriffe, Personalbeschaffer und zukünftige Vorgesetzte bereit. Nicht zugewiesene Benutzer haben keinen Zugriff auf die Analyse-Berichtsseiten (Stellen-Analyse und Analyse-Hub).

Stellen-Analyse Berichte zeigen Daten für die ausgewählte Stelle. Analyse-Hub-Berichte umfassen Daten über alle Stellen, die ein Benutzer anzeigen kann. Benutzer, die sowohl "Meine Stellen" und "Alle Stellen" auf der Stellenseite anzeigen können, haben im Analyse-Hub die gleichen Ansichten zur Verfügung.

## <a name="cross-filter"></a>Übergreifende Filter

Eine der tollen Funktionen von Power BI ist die Art, wie alle Grafiken auf einer Berichtsseite untereinander verbunden sind. Wenn Sie einen Datenpunkt auf einem der grafischen Elemente auswählen, ändern alle anderen grafischen Elemente auf der Seite, die diese Datenenänderung basierend auf dieser Auswahl enthalten. Mehr Informationen und ein Beispiel finden Sie unter [Wie Grafiken mit einem Filter in einem Power BI Bericht miteinander verbunden sind](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)

## <a name="export-to-excel"></a>Nach Excel exportieren

Um Berichtsdaten in Excel anzuzeigen, können Sie auf das Optionsmenü (drei Punkte) in einer Grafik klicken und **Zugrunde liegende Daten exportieren** auswählen. Exportierte Daten werden als gefiltert exportiert und berücksichtigen die Benutzerberechtigungen in Attract. Weitere Informationen finden Sie unter [Exportieren von Daten aus Visualisierungen](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
