---
title: "Ressourcenfähigkeiten"
description: "«»Dieser Artikel enthält Informationen zu Ressourcenfunktionen. Eine Funktion ist die Fähigkeit einer betrieblichen Ressource, eine bestimmte Aktivität auszuführen. Der Artikel wird beschrieben, wie Funktionen und zugehörige Konzepte, wie Leistungsfähigkeitsebene und Priorität, verwendet werden, damit entsprechende Ressourcen für eine Aktivität verwendet werden können."
author: sorenva
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 29c42feec36f7fe1fc00918a8c24e42de8a6dda2
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="resource-capabilities"></a>Ressourcenfähigkeiten

[!include[banner](../includes/banner.md)]


«»Dieser Artikel enthält Informationen zu Ressourcenfunktionen. Eine Funktion ist die Fähigkeit einer betrieblichen Ressource, eine bestimmte Aktivität auszuführen. Der Artikel wird beschrieben, wie Funktionen und zugehörige Konzepte, wie Leistungsfähigkeitsebene und Priorität, verwendet werden, damit entsprechende Ressourcen für eine Aktivität verwendet werden können.

Eine Funktion ist die Fähigkeit einer betrieblichen Ressource, eine bestimmte Aktivität auszuführen. Einer betrieblichen Ressource kann mehr als eine Fähigkeit zugewiesen werden, und eine Fähigkeit kann mehr als einer Ressource zugewiesen werden. Funktionen können Ressourcen auch temporär zugewiesen werden, indem ein Startdatum und Enddatum für die Funktionszuweisung definiert wird. Wenn die Funktionen für eine Ressource abläuft, kann die Ressource nicht für ein Projekt oder eine Produktion eingeplant werden, die diese Funktion erfordert. Eine Funktion, die abgelaufen ist, kann wieder erneuert werden. Sie können Funktionen löschen, sofern diese nicht in einer Arbeitsplanzuordnung enthalten oder Teil eines Produktionsarbeitsplans eines aktiven Produktionsauftrags sind. Gehen Sie beim Löschen von Funktionen also immer mit Bedacht vor. Sie können stattdessen erwägen, das Ablaufdatum der Ressourcen anzupassen, die über die jeweilige Funktion verfügen. Funktionen können allen Typen von Ressourcen zugewiesen werden: Tool, Händler, Maschine, Lagerplatz oder Personal.

## <a name="level"></a>Ebene
Mehrere Ressourcen verfügen oft über die gleiche funktionale Funktion jedoch auf unterschiedlichen Ebenen der Fertigkeiten (beispielsweise Stärke, Verarbeitungsgeschwindigkeit oder Genauigkeit). Wenn Sie eine also eine Fähigkeit einer Ressource zuweisen, können Sie einen **Ebenen**wert angeben. Die Ebene ist ein einfacher numerischer Wert. Wenn Sie angeben, dass eine Funktion eine Ressourcenanforderung für einen Produktionsarbeitsplan ist, kann ein Wert für die **Mindestanforderung** für diese Funktion angeben werden. Das Planungsmodul wählt dann nur Ressourcen aus, die die erforderliche Fähigkeit auf einer Ebene haben, die der Ebene entsprechen oder die minimale Ebene überschreitet, die für die Ressourcenanforderung angegeben ist.

## <a name="priority"></a>Priorität
Betriebliche Ressourcen, die die gleichen Funktionen haben, können einer Priorität zugewiesen werden. Wenn dann mehrere Ressourcen Funktionen aufweisen, die den Planungsbedarf auf der erforderlichen Ebene erfüllen und freie Kapazität aufweisen, kann das Planungsmodul unter diesen Ressourcen auswählen. Wenn **Priorität** im Feld auf der **Primäre Ressourcen-Auswahl** auf der **Planungsparameter** Seite aktiviert ist, wird die Ressource, die die höchste Priorität hat (dem niedrigsten numerischen Wert im Feld **Priorität**) bei der Planung zuerst ausgewählt.

## <a name="resource-requirements"></a>Ressourcenanforderungen
Beim Definieren von Ressourcenanforderungen für einen Produktionsarbeitsplan können Sie eine oder mehrere Funktionen als Anforderungen angeben. Bei der Produktionsplanung werden die in den Ressourcenanforderungen des Produktionsarbeitsplans definierten Funktionen mit den Funktionen verglichen, die für die Ressourcen definiert sind. Ressourcen, deren Funktionen die Anforderungen erfüllen, werden ausgewählt. Wenn mehrere Ressourcen dieselbe funktionale Funktion aufweisen, jedoch unterschiedliche Leistungsfähigkeiten (wie Stärke, Verarbeitungsgeschwindigkeit oder Genauigkeit) haben, können Sie entweder mehrere Funktionen definieren oder die Funktionsebene verwenden, um die Funktion der Ressource zu qualifizieren. Hier ist ein Beispiel:

-   Für einen Arbeitsplan wird die Zeit für den Bohrprozess auf 10 Einheiten pro Stunde festgelegt, aber die Anforderung selbst ist als "Bohren" definiert.
-   Sie haben zwei Bohrmaschinen, M1 und M2.
-   Die Bohrfunktion wird beiden Ressourcen, der Maschine M1 und der Maschine M2, zugewiesen.
-   Die Maschine M1 kann zwei Einheiten pro Stunde und die Maschine M2 elf Einheiten pro Stunde bohren.

In diesem Beispiel können beide Maschinen vom Planungsmodul ausgewählt werden, weil beide die die Grundanforderungsfunktion (Bohren) erfüllen. Allerdings kann die Maschine M1 nur zwei Einheiten pro Stunde bohren. Da dieser Satz viel geringer ist als die 10 Einheiten pro Stunde, die im Arbeitsplan angegeben werden, wird die Maschine M1 Produktionsprobleme verursachen, wenn sie ausgewählt wird. Es gibt zwei Möglichkeiten, um dieses Problem zu lösen und sicherzustellen, dass die Maschine M2 stattdessen ausgewählt wird.:

-   Erstellen Sie zwei separate Funktionen: Bohren mit niedriger Geschwindigkeit und Bohren mit hoher Geschwindigkeit. Definieren Sie Bohren mit niedriger Geschwindigkeit als Bohren mit einer Prozesszeit von einer bis neun Einheiten pro Stunde. Für das Bohren mit hoher Geschwindigkeit wird für den Bohrprozess ein Zeitwert von 10 bis 19 Einheiten pro Stunde definiert. Weisen Sie der Maschine M1 das Bohren mit niedriger Geschwindigkeit zu und der Maschine M2 das Bohren mit hoher Geschwindigkeit. Ändern Sie schließlich die Ressourcenfunktionsanforderung im Arbeitsplan auf Bohren mit hoher Geschwindigkeit. Schließlich ändern Sie die Ressourcenfunktionsanforderung im Arbeitsplan an. Bohren Das Planungsmodul wählt dann die richtige Maschine aus (M2).
-   Verwenden Sie die Funktionsstufe, um die Bohrfunktion zu qualifizieren, die den Bohrmaschinen zugewiesen wird. Geben Sie an, dass die bohrende Maschine M1 die Funktion auf eine Ebene von 2,0 hat und dass die M2-Maschine die Funktion Bohren auf eine Ebene von 11,0 hat. Geben Sie dann die an, dass 10,0 die Untergrenze ist, die für die bohrende Funktionsanforderung im Arbeitsplan erforderlich ist. Das Planungsmodul bestimmt dann, dass nur die M2-Maschine die Ressourcenanforderungen erfüllt.

## <a name="competencies-for-human-resources"></a>Kompetenzen für Personalverwaltung
Wenn Sie betriebliche Ressourcen vom Typ **Personalverwaltung** besitzen, die mit Arbeitskräfte in der Personalverwaltung verknüpft sind, können Sie die Kompetenzen der Arbeitskräfte auch nutzen, wenn Sie die Ressourcenanforderungen für einen Produktionsarbeitsplan definieren. Das bedeutet, dass Sie auch Anforderungen für bestimmte Qualifikationen, Kurse, Zertifizierungen oder Titel definieren können. Das Planungsmodul kann dann Ressourcen auswählen, die mit Arbeitskräften verknüpft sind und die Auswahl wird dann auf den Kompetenzen dieser Arbeitskräfte basieren. Die Kompetenzen werden unter Personalverwaltung und nicht auf der Seite **Ressourcenfähigkeiten** eingerichtet. Wenn Sie Fähigkeiten, Kurse, Zertifizierungen oder Titel als Ressourcenanforderungen definieren, müssen Sie die Personalverwaltungsfunktion verwenden und jede Ressource vom Typ **Personalverwaltung** mit einer Arbeitskraft verknüpfen. Wenn Sie die Personalverwaltungsfunktion nicht verwenden, können Sie Fähigkeiten auf der Seite **Ressourcenfähigkeiten** definieren, die denen im Modul "Personalverwaltung" ähneln oder entsprechen. Die Seite **Ressourcenfähigkeit** enthält jedoch keine Option zum Verwalten der Qualifikationen, Kurse, Zertifizierungen oder Titel.




