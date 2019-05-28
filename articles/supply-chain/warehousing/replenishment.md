---
title: Wiederbeschaffung
description: Dieser Artikel beschreibt die Wiederbeschaffungsstrategien, die für Lagerorte, die die Funktionen der Lagerortverwaltung verwenden, verfügbar sind.
author: Mirzaab
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 90043
ms.assetid: 49fa97eb-8e10-49a5-9261-1e393159f178
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37a5509b6161caffa8f3ab65f1fd8378966c2c30
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558272"
---
# <a name="replenishment"></a>Wiederbeschaffung

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt die Wiederbeschaffungsstrategien, die für Lagerorte, die die Funktionen der Lagerortverwaltung verwenden, verfügbar sind. Die Informationen in diesem Artikel gelten nicht für die Lagerort-Lösung, die in der Lagerverwaltung verfügbar ist.

Die folgenden Wiederbeschaffungsstrategien sind verfügbar:

- **Wellenbedarfsbeschaffung** – Diese Strategie erstellt Wiederbeschaffungsarbeit für ausgehende Aufträge oder Ladungen, sollte kein Bestand verfügbar sein, wenn Arbeit durch die Welle erstellt wird. Beispielsweise kann Wiederbeschaffungsarbeit erstellt werden, sollte die für einen Auftrag erforderliche Menge nicht verfügbar sein, wenn eine Welle verarbeitet wird.
- **Min./Max.-Auffüllung** – Diese Strategie verwendet minimale und maximale Lagergrenzen, um zu bestimmen, wann Lagerplätze aufgefüllt werden müssen. Die Artikel- und Lagerplatzkriterien definieren den Lagerbestand, der für die Auffüllung ausgewertet wird. Vorlagen für Min./Max.-Auffüllung sind der Hauptmechanismus zur Verwaltung optimaler Level in Entnahmeorten. Um sicherzustellen, dass genügend Komissionierlagerbestand für den Serienbedarf verfügbar ist, können Sie die Bedarfsauffüllung als Ergänzung zwischen Min./Max.-Auffüllungszyklen verwenden.
- **Ladungsbedarfs-Wiederbeschaffung** – Diese Strategie summiert den Bedarf für verschiedene Ladungen und erstellt Wiederbeschaffungsarbeit, die erforderlich ist, um die relevanten Entnahmeorte aufzufüllen. Diese Strategie hilft sicherzustellen, dass die Ladungen, die erstellt werden, nach der Freigabe dem Lager entnommen werden können.
- **Sofortige Wiederbeschaffung** – Diese Strategie füllt Bestand auf, bevor eine Welle ausgeführt wird, wenn die Zuteilung für eine Richtlinienposition mit einer Wiederbeschaffungsvorlage fehlschlägt. 

Alle vier Strategien erstellen Wiederbeschaffungsarbeit, basierend auf einer Wiederbeschaffungsvorlage.

## <a name="wave-demand-replenishment"></a>Wellenbedarfsbeschaffung
Eine Wellenbedarfswiederbeschaffung erstellt Wiederbeschaffungsarbeit basierend auf dem Bedarf, sollte die notwendige Menge für Produktionsaufträge, Kanbans, ausgehende Aufträge oder Ladungen während der Arbeitserstellung einer Welle nicht verfügbar sein. Die Wiederbeschaffungsvorlage enthält Informationen zu den Kriterien von Artikel, der Maßeinheit, der Bedarfserhöhung und dem Lagerplatz. 

Lagerplatzrichtlinien dienen zum Bestimmen, welcher Lagerort wieder aufgefüllt werden soll. Verknüpfen Sie diese Lagerplatzrichtlinien mit der Wiederbeschaffungsvorlage mithilfe des Feldes **Richtliniencode**. Wenn das Feld **Richtliniencode** nicht festgelegt ist, werden Abfragen verwendet, um zu bestimmen, welche Lagerplatzrichtlinie verwendet werden soll. Beachten Sie, wenn eine Richtlinie nicht in der Wiederbeschaffungsvorlage angegeben ist und die Lagerplatzrichtlinie einen Richtliniencode besitzt, wird die Lagerplatzrichtlinie ignoriert, auch wenn die Abfrage in der Lagerplatzrichtlinie korrekt ist. Entnahmeortrichtlinien werden verwendet, um zu bestimmen, wo der Bestand für die Wiederbeschaffung entnommen werden soll. 

Zusätzlich zur Erstellung einer Vorlage, müssen Sie einige Wiederbeschaffungseinstellungen in der Wellenvorlage angeben. Die Wellenvorlage sollte einen Wellenschritt für Wiederbeschaffung enthalten, der nur ausgeführt wird, wenn die Zuordnung eines Artikels nicht erfolgreich ist. Dieser Wiederbeschaffungswellenschritt verwendet einen Wellenschrittcode, um zu bestimmen, welche Wiederbeschaffungsvorlage verwendet werden soll. Wenn ein Wiederbeschaffungswellenschritt vorhanden ist, müssen Sie zusätzlich sicherstellen, dass **Auffüllen** im Abschnitt **Methoden** der Wellenvorlage ausgewählt ist. 

Die Seite **Wiederbeschaffungsvorlage** enthält ein Kontrollkästchen **Wellenbedarf die Nutzung nicht reservierter Mengen gestatten**. Aktivieren Sie dieses Kontrollkästchen, wenn die Bedarfswiederbeschaffung in der Lage sein soll, nicht reservierte Mengen aus Arbeit, die über die ausgewählte Wiederbeschaffungsvorlage generiert wurde, abzuziehen. Um die Bedarfswiederbeschaffungsvorlage für diese Logik zu aktivieren, muss das Kontrollkästchen für jede bestehende Wiederbeschaffungsvorlage festgelegt werden. Wenn die Bedarfswiederbeschaffung am Lagerort ausgelöst wurde, wird der Bedarf von den bestehenden Wiederbeschaffungsarbeiten mit nicht reservierten Mengen abgezogen, wenn die Arbeit auf einer Wiederbeschaffungvorlage mit aktivierten Kontrollkästchen **Wellenbedarf die Nutzung nicht reservierter Mengen gestatten** stammt.

Bedarfswiederbeschaffung wird für Aufträge, Umlagerungsaufträge, Produktionsaufträge und Kanbans unterstützt. 

## <a name="minmax-replenishment"></a>Min./Max.-Auffüllung
In der Min./Max.-Auffüllung wird der Bestand so aufgefüllt, dass er zwischen den minimalen und maximalen Grenzen liegt, die eingerichtet wurden. In der Regel erfolgt dieser Vorgang einmal täglich, um sicherzustellen, dass alle Entnahmeorte maximal gefüllt sind, ehe die Entnahme beginnt. 

Die Mindest- und Höchstbeträge sind in einer Wiederbeschaffungsvorlage festgelegt. Viele andere Einstellungen in der Vorlage ähneln den Einstellungen in Vorlagen, die in der Wellenbedarfsbeschaffung verwendeten werden. Die Vorlage sollte eine Position für jeden Artikel und Lagerplatz enthalten. Wenn Sie die Wiederbeschaffung über einen Stapelverarbeitungsauftrag ausführen, bewertet Microsoft Dynamics 365 for Finance and Operations, ob die Wiederbeschaffung in der Reihenfolge erforderlich ist, in der die Positionen zusammengefasst sind. 

Beachten Sie, dass die Min./Max.-Auffüllungsstrategie keine leere Stelle auffüllen kann, bis der Lagerplatz als fester Lagerort für den Artikel festgelegt ist. Wenn der Lagerplatz, der aufgefüllt werden muss, kein fester Lagerort ist, kann das System nicht ermitteln, welcher Artikel aufgefüllt werden soll. Daher wird zumindest ein gewisser Lagerbestand benötigt, bevor die Wiederbeschaffung stattfinden kann.

## <a name="load-demand-replenishment"></a>Ladungsbedarfs-Wiederbeschaffung
Ladungsbedarfs-Wiederbeschaffung summiert den Bedarf für verschiedene Ladungen und erstellt Wiederbeschaffungsarbeit, die erforderlich ist, um die relevanten Entnahmeorte aufzufüllen. Die Ladungsbedarfs-Wiederbeschaffung entspricht in vielerlei Hinsicht der Wellenbedarfsbeschaffung. Der Hauptunterschied ist, wie und wann Ladungsbedarfs-Wiederbeschaffung und Wellenbedarfsbeschaffung ausgeführt werden. Ebenso wie Min./Max.-Auffüllung, wird Ladungsbedarfs-Wiederbeschaffung über eine Stapelverarbeitung ausgeführt. Um die Stapelverarbeitung einzurichten, wählen Sie auf der Seite **Ladungsbedarfs-Wiederbeschaffung** die zu verwendende Wiederbeschaffungsvorlage und legen eine Filterabfrage fest, die spezifiziert, welche Ladungen zum Bestimmen des Bedarfs verwendet werden. Die Lagerplatzabfrage definiert die Lagerplätze, von denen alle verfügbaren Menge abgezogen werden, um dem zusammengeführten Bedarf an Ladungen zu entsprechen.

## <a name="immediate-replenishment"></a>Sofortige Wiederbeschaffung
Anstatt den Bedarf am Ende eines Zuteilungsprozesses zu bestimmen und die Wiederbeschaffung auf Basis der summierten Menge durchzuführen, können Sie Strategie der sofortigen Wiederbeschaffung verwenden. Mit dieser Strategie können Sie den Bestand sofort wiederbeschaffen, wenn eine Richtlinienposition fehlschlägt. Deshalb können Sie die Wiederbeschaffung so einrichten, dass sie auf bestimmte Einheiten beschränkt ist, und so, dass dabei Mengen verwendet werden, die für bestimmte Lagerplätze festgelegt wurden.

## <a name="replenishment-prerequisites"></a>Wiederbeschaffungsvoraussetzungen

|      Voraussetzung       |                                                                                                                                Beschreibung                                                                                                                                 |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|          Artikel           |                                                                                                        Der Artikel muss für Lagerortverwaltungsprozesse aktiviert werden.                                                                                                        |
|        Lagerort        | Der Lagerort muss für Lagerortverwaltungsprozesse aktiviert werden. Um einen Lagerort für Lagerortverwaltungsprozesse auf der Seite <strong>Lagerorte</strong> zu aktivieren, wählen Sie den Lagerort und dann die Option <strong>Lagerortverwaltungsprozesse verwenden</strong> aus. |
| Wiederbeschaffungsvorlagen |                                                                   Mindestens eine Wiederbeschaffungsvorlage muss für Min./Max.-Auffüllung, Wellenbedarfsbeschaffung oder Ladungsbedarfs-Wiederbeschaffung eingerichtet werden.                                                                   |
|        Lagerplätze        |                                                                                                       Lagerplätze müssen erstellt und mit einem Lagerplatzprofil verknüpft werden.                                                                                                       |
|    Lagerplatzprofile    |                                                                                                        Lagerplatzprofile sind erforderlich, um Lagerplätze zu erstellen.                                                                                                        |
|   Lagerplatzrichtlinien   |                                                       Lagerplatzrichtlinien sind erforderlich, um die Arbeit zu den Lagerplätzen zu leiten, an denen eine Wiederbeschaffung benötigt wird und zu Lagerplätzen, aus denen der Bestand stammt.                                                        |
|     Arbeitsvorlagen      |                                                   Arbeitsvorlagen des Typs <strong>Wiederbeschaffung</strong> sind erforderlich, um Wiederbeschaffungsarbeit zu erstellen, damit der Bestand an die gewünschten Lagerplätze verschoben werden kann.                                                    |

