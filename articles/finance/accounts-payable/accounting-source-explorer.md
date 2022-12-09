---
title: Buchhaltungsquellen-Explorer
description: Dieser Artikel enthält Informationen zur Seite „Buchhaltungsquellen-Explorer“, die Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können.
author: RyanCCarlson2
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: kfend
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5bd5580dc0be37ec89e6c7934b47c7d5593d8716
ms.sourcegitcommit: 5f8f042f3f7c3aee1a7303652ea66e40d34216e3
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806432"
---
# <a name="accounting-source-explorer"></a>Buchhaltungsquellen-Explorer

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Informationen zur Seite **Buchhaltungsquellen-Explorer**, die Sie für die detaillierte Analyse der Quellinformationen hinter den Hauptbuchbuchhaltungseinträgen verwenden können.

Der **Buchhaltungsquellen-Explorer** ist eine neue Seite, die Quellinformationen anzeigt. Sie können ihn entweder als eigenständiges Tool verwenden oder die Details nach Hauptbuchbuchhaltungseinträgen analysieren. So können die Seite verwenden, um die aktuellesten Detailquellinformationen für einen Saldo in der Zwischenbilanz oder für eine Belegbuchung abzurufen. Sie können dann die Funktion **Nach MS Excel exportieren** verwenden, um die Informationen in Microsoft Excel weiter aufzuteilen (beispielsweise in einer PivotTable oder einem PivotTable-Bericht).

Die Seite **Buchhaltungsquellen-Explorer** zeigt stets denselben Gesamtbetrag pro Sachkonto wie das Hauptbuch an (beispielsweise in einer Zwischenbilanz). Wie in einer Zwischenbilanz können Sie Segmente in unterschiedlichen Spalten anzeigen. Wählen Sie einfach den entsprechenden Finanzdimensionssatz aus. 

Sie können Parameter verwenden, um ein Datumsintervall für die Analyse zu definieren. Diese Funktion ähnelt der Funktion in einer Zwischenbilanz.

Für alle Dokumente, die das Quelldokumentframework verwenden, zeigt die Seite **Buchhaltungsquellen-Explorer** zusätzliche Informationen, basierende auf der Buchhaltungsverteilungen und ggf. der Projektbuchhaltungsverteilungen. Diese Informationen enthalten Werte für **Geldbetragstyp**, **Projekt**, **Aktivität**, **Kategorie** und **Abrechnungscode**. Nachfolgend finden Sie einige Analysebeispiele:

- Abweichungen zwischen Bestellungen und Kreditorenrechnungen, da jede Abweichung durch einen Geldbetragstyp dargestellt wird (z. B. Abweichung der Belastung)
- Differenz zwischen berechenbaren Stunden und nicht-berechenbaren Stunden und Ausgaben pro Projekt, Unternehmenseinheit und Hauptkonto

Für Quelldokumente, die das Konzept der Quelldokument-Referenzidentitäten verwenden, zeigt die Seite **Buchhaltungsquellen-Explorer** noch weitere Details an, z. B. **Debitor**, **Kreditor**, **Arbeitskraft**, **Produkt**, **Menge**, **Einheitentext** und **Beschreibung**. Nachfolgend finden Sie einige Analysebeispiele:

- Hotelkosten pro Unternehmenseinheit und Hotelmarke für einen Finanzzeitraum auf der Grundlage von Spesenabrechnungen
- Rabatte nach Kreditor, Produkt, Abteilung

Für diese Dokumente können Sie von der Seite **Buchhaltungsquellen-Explorer** aus auch zum ursprünglichen Quelldokument navigieren.

> [!NOTE]
> Ab Version 10.0.31 ist ein neues Feature **Erweiterte Filterfunktion für den Buchhaltungsquellen-Explorer** verfügbar. Dieses Feature ersetzt die Schaltfläche **Aktualisieren**, um eine robustere erweiterte Abfrageumgebung bereitzustellen, die der auf der Seite **Belegbuchungen** zur Verfügung steht. Mit dem erweiterten Filter können Sie nach ähnlichen Feldern filtern wie auf der Seite **Belegbuchungsabfrage** , z. B. **Sachkonto**, **Unternehmenseinheit**, **Kostenstelle** und **Abteilung**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
