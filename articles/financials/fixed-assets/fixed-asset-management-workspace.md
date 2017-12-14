---
title: Arbeitsbereich "Anlageverwaltung"
description: "Dieses Thema enthält Informationen zum Arbeitsbereich \"Anlageverwaltung\". Der Arbeitsbereich zeigt Informationen, die sich auf Anlagen beziehen, die im System eingegeben werden. Er enthält eine Überblicksansicht und eine Analyseansicht."
author: saraschi
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c544ae60433dd14d061bc1a78d5cad6577cf579d
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-management-workspace"></a>Arbeitsbereich "Anlageverwaltung"

[!include[banner](../includes/banner.md)]

Der Arbeitsbereich **Anlagenverwaltung** zeigt Informationen, die sich auf Anlagen beziehen, die im System eingegeben werden. Der Arbeitsbereich umfasst eine Überblicksansicht und eine Analyseansicht. Die Registerkarte **Meine Arbeit** zeigt Überblickskacheln, Anlagendetails und zugehörige Informationen zu Anlagen im aktuellen Unternehmen. Sie können dem Power BI-Analyseabschnitt direkt im Arbeitsbereich Analysemöglichkeiten hinzufügen. Die Registerkarte **Analyse – alle Unternehmen** verwendet die Möglichkeiten von Microsoft Power BI, um grafische Elemente anzuzeigen, die sich auf Anlagen in allen Unternehmen beziehen.

## <a name="my-work"></a>Meine Arbeit

### <a name="summary"></a>Summe

Die Kacheln im Abschnitt **Zusammenfassung** bieten einen Überblick der Anlagen. Die Informationen umfassen Metriken zu Anlagen, die noch nicht erworben wurden, Anlagen, die im laufenden Jahr erworben wurden, und Anlagen, die im laufenden Jahr entsorgt wurden. Der Abschnitt **Zusammenfassung** bietet ebenfalls schnelle Navigation zur Listenseite **Anlagevermögen**, Charge-Abschreibungsvorschlag und Anlagenerfassung.

### <a name="find-fixed-assets"></a>Anlagen suchen

Mit dem Abschnitt **Anlagen suchen** können Sie schnell nach Anlagen suchen, indem Sie die Anlagennummer, die Gruppe, den Namen, den Lagerplatz oder die zuständige Person angeben. Alle Anlagen, die den Suchkriterien entsprechen, werden in der Liste angezeigt.

In der Liste können Sie die folgenden Seiten anzeigen:

 - **Details**-Seite für die Anlage
 - Seite **Bücher** für alle Bücher, die der Anlage zugeordnet sind
 - Seite **Anlagenbewertungen**

### <a name="valuations"></a>Bewertungen

Auf der Seite **Anlagenbewertungen** können Sie auf einer Seite die wichtigsten Informationen zu einer Anlage und auch Details zu allen Büchern anzeigen, die der Anlage zugeordnet sind. Die Option **Salden** oben links auf der Seite zeigt die aktuelle Bewertung für jedes Buch an, das der Anlage zugeordnet ist. Sie können zu den Werten auch detaillierte Buchungen anzeigen, aus denen die zusammengefassten Wert bestehen. Die Option **Profil** oben links auf der Seite zeigt den Abschreibungszeitplan für jedes Buch an, das der Anlage zugeordnet ist.

Sie können auf die Seite **Anlagenbewertungen** vom Arbeitsbereich **Vermögensverwaltung** oder der Listenseite **Anlagevermögen** zugreifen.

### <a name="related-information"></a>Zugehörige Informationen

Sie können direkt zu den Seiten **Bucheinstellung**, **Abfrage von Anlagenbuchungen** und einigen Berichten navigieren, indem Sie die Links im Abschnitt **Zugehörige Informationen** des Arbeitsbereichs verwenden.

### <a name="analytics--all-companies"></a>Analyse – alle Unternehmen

Die Seite **Analyse** enthält wichtige Metriken zu Anlagen in allen juristischen Personen im System. Zugriff auf diese Registerkarte wird durch das Sicherheitsrecht "Anlagenanalyse für alle Unternehmen anzeigen" gesteuert.

Die folgende Tabelle enthält die Visualisierungen, die für jede Berichtsseite verfügbar ist.

| Berichtsseiten            | Darstellung        |
|------------------------|----------------------|
| Anlagenbewertungen | Gesamtnettobuchwert |
| Anlagenbewertungen | Nettobuchwerte nach Anlagengruppe |
| Anlagenbewertungen | Akquisitionswerte |
| Anlagenbewertungen | Abgangswerte |
| Anlagenbewertungen | Anlagendetails |
| Bewertungszuordnungen        | Gesamtnettobuchwert |
| Bewertungszuordnungen        | Anlagenstandorte |
| Bewertungszuordnungen        | Anlagendetails |

Um die Analyse mit Daten anzuzeigen, müssen Sie die AssetTransactionMeasure-Aggregatmessung auf der Seite **Entität-Speicher** aktualisieren.
