---
title: Buchhaltungsquellen-Explorer
description: "Dieser Artikel enthält Informationen zum Buchhaltungsquellexplorer, den Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 8913e61285d5d180883471991b659ddcb260afe3
ms.lasthandoff: 03/31/2017


---

# <a name="accounting-source-explorer"></a>Buchhaltungsquellen-Explorer

Dieser Artikel enthält Informationen zum Buchhaltungsquellexplorer, den Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können.

Der Buchhaltungsquellen-Explorer ist eine neue Seite, die Quellinformationen anzeigt. Sie können entweder Buchhaltungsquellexplorer eigenständiges als Tool verwenden oder die Details nach Hauptbuchbuchhaltungseinträgen analysieren. So können Sie Buchhaltungsquellexplorer verwenden, um über die Quellinformationen für einen Saldo im Hintersaldo oder für Belegbuchungen abzurufen. Sie können dann die Funktion "Nach Microsoft Excel exportieren" verwenden, um die Informationen in Microsoft Excel weiter aufzuteilen (beispielsweise in einer Pivottabelle oder einem PivotTable-Bericht).

Der Buchhaltungsquellen-Explorer zeigt stets denselben Gesamtbetrag pro Sachkonto wie das Hauptbuch an (beispielsweise in der Zwischenbilanz). Wie in der Zwischenbilanz können Sie Segmente in unterschiedlichen Spalten anzeigen. Wählen Sie einfach den entsprechenden Finanzdimensionssatz aus. 

Sie können Parameter verwenden, um ein Datumsintervall für die Analyse zu definieren. Diese Funktion ähnelt der Funktion in der Zwischenbilanz.

Für alle Dokumente, die das Quelldokumentframework, Gegenkonto Quellexplorershowzusätzliche Informationen, auf Grundlage Buchhaltungsverteilungen und ggf. Projektbuchhaltungsverteilungen verwenden. Diese Informationen enthalten den Geldbetrag Typ, Projekt, Kategorie, Projektvorgang und Abrechnungscode. Nachfolgend finden Sie einige Analysebeispiele:

-   Abweichungen zwischen Bestellungen und Kreditorenrechnungen, da jede Abweichung durch einen Geldbetragstyp dargestellt wird (z. B. Abweichung der Belastung)
-   Differenz zwischen berechenbaren Stunden und nicht-berechenbaren Stunden und Ausgaben pro Projekt, Unternehmenseinheit und Hauptkonto

Für Quelldokumente, die das Konzept der Quelldokument-Referenzidentitäten verwenden, zeigt der Buchhaltungsquellen-Explorer noch weitere Details an, z. B. Debitor, Kreditor, Arbeitskraft, Produkt, Menge, Einheitentext und Beschreibungen. Nachfolgend finden Sie einige Analysebeispiele:

-   Hotelkosten pro Unternehmenseinheit und Hotelmarke für einen Finanzzeitraum auf der Grundlage von Spesenabrechnungen
-   Rabatte nach Kreditor, Produkt, Abteilung

Für diese Dokumente können Sie vom Buchhaltungsquellen-Explorer aus auch zum ursprünglichen Quelldokument navigieren.


