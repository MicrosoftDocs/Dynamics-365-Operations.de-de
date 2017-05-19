---
title: Kostengruppen
description: "Kostengruppen bilden die Grundlage für die Segmentierung und Analyse von Kostenbeiträgen in den berechneten Kosten eines produzierten Artikels – beispielsweise Kostenbeiträge für Material, Arbeit oder Gemeinkosten. Die Segmentierung von Kostengruppen wird in Produktionsumgebungen auch als Kostenaufschlüsselung, Kostenzerlegung oder Kostenklassifizierung bezeichnet."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMCostGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3592f3c076681c5b755b62383212bbe6d158f62d
ms.contentlocale: de-de
ms.lasthandoff: 04/25/2017


---

# <a name="cost-groups"></a>Kostengruppen

[!include[banner](../includes/banner.md)]


Kostengruppen bilden die Grundlage für die Segmentierung und Analyse von Kostenbeiträgen in den berechneten Kosten eines produzierten Artikels – beispielsweise Kostenbeiträge für Material, Arbeit oder Gemeinkosten. Die Segmentierung von Kostengruppen wird in Produktionsumgebungen auch als Kostenaufschlüsselung, Kostenzerlegung oder Kostenklassifizierung bezeichnet. 

Die Segmentierung von Kostengruppen wird in Produktionsumgebungen auch als Kostenaufschlüsselung, Kostenzerlegung oder Kostenklassifizierung bezeichnet. Es gibt viele Einsatzmöglichkeiten für die Kostengruppensegmentierung. Nachfolgend finden Sie einige Beispiele:

-   Segmentieren von Kosten für unterschiedliche Materialtypen (beispielsweise Zutaten und Verpackungsmaterial für Konserven) auf Basis der den Artikeln zugewiesenen Kostengruppen.
-   Segmentieren von Kosten für verschiedene Typen von betrieblichen Ressourcen (beispielsweise verschiedene Arten von Arbeiten oder Maschinen) auf Basis der Kostengruppen, die den mit betrieblichen Ressourcen und Arbeitsgängen des Arbeitsplans in Verbindung stehenden Kostenkategorien zugewiesen sind.
-   Segmentieren von Kosten für Rüst- und Ausführungszeit bei Arbeitsgängen des Arbeitsplans auf Basis der Kostengruppen, die den mit den Arbeitsgängen des Arbeitsplans in Verbindung stehenden Kostenkategorien zugewiesen sind.
-   Segmentieren von Kosten für verschiedene Arten von Gemeinkosten (beispielsweise arbeits- oder maschinenbezogene Gemeinkosten) auf Basis der Kostengruppen, die in den Einstellungen für den Nachkalkulationsbogen indirekten Kosten zugewiesen sind.
-   Verwendung als Grundlage für die Berechnung verschiedener Typen von Produktionsgemeinkosten in den Einstellungen des Nachkalkulationsbogens. Dazu können unterschiedliche Gemeinkosten im Zusammenhang mit der Weiterleitung von Informationen zu betrieblichen Ressourcen oder zu Rüst- und Ausführungszeiten gehören. Gemeinkosten für die Produktion können sich auch auf Kostenbeiträge für Komponentenmaterial beziehen. Diesem Ansatz liegt eine Lean Manufacturing-Philosophie zugrunde, bei der keine Weiterleitung von Informationen erforderlich ist.

Die Kostengruppensegmentierung wird auf die berechneten Kosten eines produzierten Artikels angewendet – unabhängig davon, ob diese Berechnung auf den Standardkosten oder auf den geplanten Kosten basiert. Auf der Seite **Zusammenfassung** wird diese Segmentierung nach Kostengruppe, nach Ebene oder nach Kostengruppe und Ebene angezeigt. 

Diese Möglichkeit zur ebenenübergreifenden Beibehaltung der Kostengruppensegmentierung in einer Produktstruktur wird als *Aufteilung* bezeichnet. Die Aufteilung gilt nur für produzierte Artikel, die ein Lagermodell für Standardkosten verwenden. Ohne Aufteilung werden die Kosten für eine produzierte Komponente als Materialkostenbeitrag behandelt. Mit dem Lagerparameter für die Kostenaufschlüsselung nach Nebenbuch wird angegeben, dass die Kostengruppensegmentierung in Standardkostenberechnungen ebenenübergreifend verwendet wird. Ohne Angabe von Ebenen wird die Kostengruppensegmentierung dagegen lediglich für die Berechnung einer einzelnen Ebene verwendet. So wird beispielsweise auf der Seite **Kostenaufschlüsselung nach Kostengruppe** die Kostengruppensegmentierung für Standardkostenartikel über mehrere Ebenen angezeigt. 

Die Kostengruppensegmentierung kann auch auf die Abweichungen bei Standardkostenartikeln angewendet werden. Durch einen zweiten Lagerparameter wird angegeben, ob Abweichungen nach Kostengruppe erfasst oder lediglich zusammengefasst werden. 

Eine Kostengruppe kann zur weiteren Segmentierung mit einem Kostengruppentyp sowie mit einem gewünschten Verhalten versehen werden.

-   **Kostengruppentyp** – Jeder Kostengruppe muss ein Kostengruppentyp zugewiesen werden, durch den angegeben wird, ob sich die Kostengruppe auf "Direktmaterialien", "Direktfertigung" oder "Direktes Outsourcing" bezieht, oder um sie als "Indirekt" oder "Nicht definiert" zu kennzeichnen. Eine als "Direktmaterialien" festgelegte Kostengruppe kann Artikeln zugewiesen werden. Eine Kostengruppe vom Typ "Direktfertigung" kann Kostenkategorien zugewiesen werden. Eine direkte Kostengruppe "Direktes Outsourcing" kann einem Produkttyp "Service" zugewiesen werden, die es Ihnen ermöglicht, Kosten zu klassifizieren, die dem Dienstleistungseinkauf zu Fremdarbeitsaktivitäten zugeordnet sind. Eine Kostengruppe vom Typ "Indirekt" kann indirekten Kosten für (Zu-)Sätze zugewiesen werden. Eine Kostengruppe vom Typ "Nicht definiert" kann Artikeln, Kostenkategorien oder indirekten Kosten zugewiesen werden. Die Zuweisung eines Kostengruppentyps erfüllt mehrere Zwecke. Erstens: Sie schränkt die Möglichkeit zum Zuweisen einer Kostengruppe sowie die Möglichkeit zum Anzeigen einer Liste mit anwendbaren Kostengruppen ein. Zweitens: Sie ermöglicht eine zusätzliche Segmentierung für die Erstellung von Berichten. Drittens: Sie kann zum Zuweisen von Sachkonten für Abweichungen verwendet werden.
-   **Verhalten** − Jeder Kostengruppe kann optional ein Verhalten zugewiesen werden, mit dem festgelegt wird, ob sich die Kostengruppe auf Fixkosten oder auf variable Kosten bezieht. Kostengruppen ohne Verhaltenswert gelten als variable Kosten. Die Zuweisung eines Verhaltens wirkt sich lediglich auf die Berichterstellung aus. So können beispielsweise Kosten mit einer Segmentierung für Fixkosten und für variable Kosten sowohl im Nachkalkulationsbogen als auch auf der Seite **Kostenaufschlüsselung nach Kostengruppe** angezeigt werden. Wenn Sie jeder Kostengruppe einen Gewinnvorgabe-Prozentsatz zuweisen, kann über die Herstellkostenkalkulation die Berechnung eines vorgeschlagenen Verkaufspreises auf Basis eines Kosten-plus-Aufschlag-Ansatzes bereitgestellt werden.





