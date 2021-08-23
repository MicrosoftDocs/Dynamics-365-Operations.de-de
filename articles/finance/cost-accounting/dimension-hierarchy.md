---
title: Dimensionshierarchie
description: Dieses Thema bietet Informationen über Dimensionshierarchien. Sie verwenden eine Dimensionshierarchie, um die Berichtsstruktur, Kostenrichtlinien sowie die Sicherheitseinstellungen zu in der Kostenrechnung zu definieren.
author: AndersGirke
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimensionHierarchy,
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 40ae7b61537cdcd1934056b9e289f342e96b57d3eebe5a6e713b2db91310ed9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766974"
---
# <a name="dimension-hierarchy"></a>Dimensionshierarchie

[!include [banner](../includes/banner.md)]

Dieses Thema bietet Informationen über Dimensionshierarchien. Sie verwenden eine Dimensionshierarchie, um die Berichtsstruktur, Kostenrichtlinien sowie die Sicherheitseinstellungen zu in der Kostenrechnung zu definieren.  

## <a name="overview"></a>Überblick

Dimensionshierarchien werden an verschiedenen Stellen in der Kostenrechnung verwendet. Mit einer Dimensionshierarchie können Sie die folgenden Informationen definieren:

-  Die Berichtsstruktur, die zu den Anforderungen der Organisation passt
-  Kostenrichtlinien
-  Die Sicherheitseinrichtung

Dies ist ein Beispiel einer Dimensionshierarchie.

![Beispiel einer Dimensionshierarchie.](./media/dimension-hierarchy.png)

Eine Dimensionshierarchie kann für die folgenden Dimensionstypen erstellt werden:

-  Kostenelementdimensionen
-  Kostenobjektdimensionen
-  Statistische Dimensionen

> [!NOTE]
> - Sie können mehrere Dimensionshierarchien für dieselbe Dimension erstellen, wenn unterschiedliche Perspektiven erforderlich sind.
> - Eine Dimensionshierarchie kann nur einer Dimension zugeordnet werden.
> - Eine Dimensionshierarchie kann beliebige Ebenen in der Struktur haben. Alle Ebenen sind im Arbeitsbereich **Kostensteuerung** verfügbar. Wenn Sie Microsoft Excel oder Microsoft Power BI für Berichtszwecke verwenden, werden nur die ersten 15 Ebenen der Dimensionshierarchie exportiert. Diese Einschränkung ist notwendig, da Excel und Power BI ein festgelegtes Schema erfordern.
> - Eine Dimensionshierarchie ist nicht Datumswirksam. Daher wird jede Änderung an einer Dimensionshierarchie sofort im Datensatz gespeichert, und Sie können das Vorher-Datum mit dem Nachher-Datum vergleichen.

## <a name="dimension-hierarchy-type"></a>Dimensionshierarchietyp

Wenn Sie eine neue Dimensionshierarchie erstellen, müssen Sie einen Hierarchietyp auswählen. Wechseln Sie zu **Kostenrechnung** > **Dimensionen** > **Dimensionshierarchien**. Klicken Sie auf **Neu** und wählen Sie einen Dimensionshierarchietyp aus. Sie können entweder **Dimensionskategorisierungshierarchie** oder **Dimensionsklassifizierungshierarchie** auswählen.

### <a name="dimension-categorization-hierarchy"></a>Dimensionskategorisierungshierarchie

Der Typ **Dimensionskategorisierungshierarchie** wird für Berichterstellungszwecke verwendet. Er unterstützt nur die Kostenelementdimensionen. Bei Auswahl dieses Typs gelten folgende Regeln:

-  Ein Dimensionsmitglied kann der Hierarchiestruktur mehrmals zugeordnet werden.
-  Sie können ein Kostenelement-Dimensionsmitglied in verschiedenen Knoten einfügen, indem Sie dem Blattknoten ein Kostenverhalten zuweisen.

### <a name="dimension-classification-hierarchy"></a>Dimensionsklassifizierungshierarchie

Der Typ **Dimensionsklassifizierungshierarchie** wird zur Regeldefinition und zu Berichterstellungszwecken verwendet. Er unterstützt alle Dimensionen, wie Kostenobjekte, Kostenelemente und statistischen Dimensionen. Wenn Sie diesen Typ auswählen, kann ein Dimensionsmitglied der Hierarchiestruktur nur einmal zugeordnet werden.

## <a name="create-and-maintain-a-dimension-hierarchy"></a>Erstellen und pflegen einer Dimensionshierarchie

Eine Dimensionshierarchie wird als Baumstruktur mit Knoten- und Blattknotenbeziehungen erstellt.

-  Ein Knoten kann 1:_n_ Subknoten haben.
-  Einem Knoten kann nicht gleichzeitig untergeordnete Knoten und Blattnoten zugewiesen werden.
-  Ein Blattknoten kann nur der niedrigsten Ebene in der Hierarchie zugewiesen werden.

### <a name="example"></a>Beispiel

Ein Einzelhandelsunternehmen hat die folgende Organisationsstruktur: Finanzen und Personalverwaltung sind Abteilungen unter Verwaltung und Montage sowie Verpackung sind Abteilungen unter Produktion sind.

![Beispiel einer Organisationsstruktur.](./media/dimension-hierarchy-org.png)

Eine Kostenobjektdimension stellt alle Kostenstellen in der Organisation dar.

- Kostenobjektdimension
    - Kostenstellen

Die Kostenobjektdimension, die alle Kostenstellen darstellt, kann wie hier angezeigt eingerichtet werden.

| Kostenstellen | Beschreibung |
|--------------|-------------|
| CC001        | Personalverwaltung          |
| CC002        | Finanzen     |
| CC003        | Steuerl. Buchung         |
| CC007        | AR/AP       |
| CC005        | Montage    |
| CC006        | Verpackung   |

Eine Kostenelementdimension stellt alle Kostenelemente in der Organisation dar.

- Kostenelementdimension
    - Kostenelemente

Die Kostenelementdimension, die alle Kostenelemente darstellt, kann z eingerichtet hier angezeigt werden.

| Kostenelemente | Beschreibung |
|---------------|-------------|
| 10001         | Elektrizität |
| 10010         | Reinigung    |
| 10011         | Heizung     |
| 40001         | COGS (Wareneinsatz)        |

Eine Dimensionshierarchie, die die Meldeanforderungen der Organisation erfüllt, kann wie hier gezeigt eingerichtet werden.

**Dimensionshierarchiedetails**

| Dimensionshierarchiename | Dimensionen    | Dimensionshierarchie-Typname      | Zugriffslistenhierarchie |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisation             | Kostenstellen | Dimensionsklassifizierungshierarchie | Nr.                    |

Die Dimensionshierarchie für die Berichtserstellung kann beispielsweise wir hier angezeigt eingerichtet werden.

**Dimensionsmitgliedsbereiche**

|   Knoten           |   Ausgangsdimensionsmitglied   |   Zieldimensionsmitglied   |
|-------------------|---------------------------|-------------------------|
| Organisation      |                           |                         |
| &nbsp;&nbsp;Verwaltung         |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finanzen   | CC002                     | CC003                   |
|                   | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personalverwaltung        | CC001                     | CC001                   |
| &nbsp;&nbsp;Produktion    |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Verpackung | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montage  | CC006                     | CC006                   |

Eine Dimensionshierarchie, die die Meldeanforderungen der Organisation erfüllt, kann wie hier gezeigt eingerichtet werden.

**Dimensionshierarchiedetails**

| Dimensionshierarchiename | Dimensionen     | Dimensionshierarchie-Typname      |
|--------------------------|---------------|------------------------------------|
| Kostenverhalten            | Kostenelemente | Dimensionsklassifizierungshierarchie |

Die Dimensionshierarchie für die Richtlinie kann beispielsweise eingerichtet hier angezeigt werden.

**Dimensionsmitgliedsbereiche**

|   Knoten           |   Ausgangsdimensionsmitglied   |   Zieldimensionsmitglied   |
|-------------------|---------------------------|-------------------------|
| Kostenverhalten     |                           |                         |
| &nbsp;&nbsp;Fixkosten    | 10001                     | 10011                   |
| &nbsp;&nbsp;Variable Kosten | 40001                     | 40010                   |

> [!NOTE]
> Unter **Dimensionsmitgliedsbereiche** kann ein Knoten 1:_n_ -Dimensionsmitgliedsbereiche enthalten. Sie können Dimensionsmitgliedskennungen einfügen, die noch nicht als Dimensionsmitglieder vorhanden sind. Durch diesen Ansatz wird die Hierarchie zukunftssicher.  

### <a name="copy-a-hierarchy"></a>Eine Hierarchie kopieren

Sie können eine aktuelle Dimensionshierarchie als Ausgangspunkt für eine neue Dimensionshierarchie kopieren. Diesen Ansatz kann nützlich sein, wenn Sie die vorherige Dimensionshierarchie mit der neuen Dimensionshierarchie vergleichen möchten.

### <a name="rearrange-nodes-in-a-hierarchy"></a>Neu anordnen von Knoten in einer Hierarchie

Sie können einen Knoten innerhalb der aktuellen Struktur nach oben oder unten verschieben. Auf diese Weise können Sie die Reihenfolge der Knoten für die Berichterstellung im Arbeitsbereich **Kostensteuerung** anpassen.

Verschieben Sie einen Knoten an einen neuen Standort in der Hierarchie, indem Sie den Zielknoten auswählen. Es gibt zwei Möglichkeiten, um einen Knoten zu verschieben:

- **Nach unten verschieben** – Verschiebt den ausgewählten Knoten aus der aktuellen Position in der Hierarchie, und fügt ihn **unter** dem ausgewählten Zielknoten ein.
- **Verschieben hinter** – Verschiebt den ausgewählten Knoten aus der aktuellen Position in der Hierarchie, und fügt ihn **hinter** dem ausgewählten Zielknoten auf seiner Hierarchieebene ein.

> [!NOTE] 
> Die Reihenfolge der Knoten wird nicht gewahrt, wenn Sie Daten nach Excel oder Power BI exportieren, da diese Tools standardmäßig eine alphanumerische Sortierreihenfolge verwenden. Sie sollten den Auftrag manuell anpassen.

## <a name="define-dimension-hierarchies-for-reporting"></a>Dimensionshierarchien für die Berichterstellung definieren

Dimensionshierarchien sind wichtig für die Berichterstellung. Damit können Sie die bestimmte Struktur definieren, die für die jeweilige Organisation passt. Die Aggregationen, die auf Knotenebene der Dimensionshierarchie erfolgen, lassen Projektbeteiligten auf jeder Ebene der Organisation Daten auf jeder Ebene sehen.

Dimensionshierarchien sind in den folgenden Berichtstools verfügbar. Dieser Ansatz stellt die Konsistenz in der Berichtsstruktur sicher.

- Arbeitsbereich **Kostensteuerung** (Client)

    - Konfigurationsgesteuert

- Arbeitsbereich **Kostensteuerung** (mobile Anwendung):

    - Konfigurationsgesteuert

- Excel

    - Bietet eine Option zur Auswahl bestimmter Dimensionshierarchien pro Exportdefinition:

        - Eine Kostenelement-Dimensionshierarchie (obligatorisch)
        - Eine Kostenobjekt-Dimensionshierarchie (optional)
        - Eine statistische Dimensionshierarchie (optional)

- Power BI:

    - Alle Dimensionshierarchien sind verfügbar.
    
Wenn Sie Berichte erstellen, indem Sie Excel oder Power BI verwenden, werden nur die ersten 15 Ebenen der Dimensionshierarchien exportiert. Diese Einschränkung ist notwendig, da Excel und Power BI ein festgelegtes Schema erfordern. Wenn eine Hierarchie über mehr als 15 Ebenen verfügt, werden diese zusätzlichen Ebenen nicht exportiert. Die normalisierte Tabelle enthält einen Datensatz für jedes Dimensionsmitglied in der Hierarchie. Aus diesem Grund wird die Aggregation automatisiert. Durch dieses Verhalten wird sichergestellt, dass die Salden auf jeder der 15 verfügbaren Ebenen der Hierarchie noch richtig sind.

Das folgende Beispiel veranschaulicht, wie eine Dimensionshierarchie in der Berichtsstruktur aussehen kann.

| Kostenobjekt-Dimensionshierarchie – Ebene 1 | Kostenobjekt-Dimensionshierarchie – Ebene 2 | Kostenobjekt-Dimensionshierarchie – Ebene 3 | Kostenobjekt-Dimensionshierarchie – Ebene 4 | Kostenobjekt-Dimensionshierarchie – Ebene 15 |
|-------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------------------------|--------------------------------------------|
| Organisation                              | Verwaltung                                     | Finanzen                                   | CC002                                     |                                            |
| Organisation                              | Verwaltung                                     | Finanzen                                   | CC003                                     |                                            |
| Organisation                              | Verwaltung                                     | Finanzen                                   | CC007                                     |                                            |
| Organisation                              | Verwaltung                                     | Personalverwaltung                                        | CC001                                     |                                            |
| Organisation                              | Produktion                                | Verpackung                                 | CC005                                     |                                            |
| Organisation                              | Produktion                                | Montage                                  | CC006                                     |                                            |

### <a name="update-the-dimension-hierarchies-that-are-used-for-reporting"></a>Aktualisieren der Dimensionshierarchien, die für die Berichterstellung verwendet werden 

Im Laufe der Zeit müssen die Dimensionshierarchien, die in den zuvor genannten Berichtstools verwendet werden, aktualisiert werden. Sie können Dimensionshierarchien aktualisieren, indem Sie den Client aktualisieren.

- **Arbeitsbereich** Kostensteuerung (Client)
- **Kostensteuerung** Arbeitsbereich (mobile Anwendung)

Aktualisierungen der Dimensionshierarchien werden alle 24 Stunden durch einen zuvor zwischengespeicherten Einzelvorgang vorgenommen. Nachdem die exportierten Daten aktualisiert wurden, stehen die aktualisierten Dimensionshierarchien in den folgenden Tools zur Verfügung:

- Excel
- Power BI

> [!NOTE] 
> Um die Aktualisierung des Dimensionshierarchie-Caches manuell zu starten, können Sie für die Dimensionshierarchie oder die Hierarchien, die aktualisiert werden müssen, einen neuen Export in Excel erstellen.

## <a name="define-dimension-hierarchies-for-cost-policies"></a>Definieren Sie für diese Dimensionshierarchien die Kostenrichtlinien

Kostenrechnung besteht aus mehreren Richtlinien, in denen detaillierte Regeln definiert werden. Sie müssen mindestens eine Dimensionshierarchie für die folgenden Richtlinien definieren:

- Kostenverhalten
- Kostenverteilung
- Kostenzuweisung
- Kostenaufschlüsselung

Dimensionshierarchien vereinfachen die Regelerstellung. Um nicht für jedes Dimensionsmitglied Regeln erstellen zu müssen, können Sie Aggregationen von Dimensionsmitgliedern nutzen, die von den Dimensionshierarchieebenen bereitgestellt werden. Wenn Sie über überlappende Regeln verfügen, müssen Sie bestimmte Regeln definieren, die das System bei der Gemeinkostenberechnung berücksichtig.

### <a name="example-define-a-cost-behavior-policy"></a>Beispiel: Definieren Sie eine Kostenverhaltensrichtlinie

Eine neue Kostenverhaltensrichtlinie wird erstellt und entsprechende Dimensionshierarchien werden der Richtlinie wie hier angezeigt zugeordnet.

**Kostenverhaltensrichtlinie**

| Richtlinienname   | Kostenelement-Dimensionshierarchie | Kostenobjekt-Dimensionshierarchie | Buchhaltungswährung |
|---------------|----------------------------------|---------------------------------|---------------------|
| Kostenverhalten | Kostenverhalten                    | Organisation                    | USD                 |

**Regeln**

| Kostenelement-Dimensionshierarchieknoten | Kostenobjekt-Dimensionshierarchieknoten | Fester Prozentsatz | Fester Betrag | Gültig ab | Gültig bis |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|----------|
| Fixkosten                            | Organisation                         | 100,00           | 0,00         | 1/1/2017   | Nie    |
| 10001                                 | Organisation                         | 0,00             | 150,00       | 1/1/2017   | Nie    |
| 10001 (\*)                             | Finanzen                              |                  | 50,00        | 1/1/2017   | Nie    |
| Kostenverhalten oder variable Kosten (\*\*)   | Organisation                         | 0,00             | 0,00         | 1/1/2017   | Nie    |

\* Der Knoten für variable Kosten ist nicht erforderlich. Wenn Kosten nicht als Fixkosten klassifiziert sind, müssen sie variable Kosten sein.

\*\* Eine detaillierte Regel wird für die Kombination des Kostenfaktormitglieds 10001 und alle Kostenobjektmitgliedern, die unter der Finanzhierarchieebene (CC002, CC003, CC007) zusammengefasst werden, erstellt.

Die vorhergehenden Regeln zeigen die Flexibilität, die Dimensionshierarchien bereitstellen. Durch das Festlegen allgemeiner Regeln definieren, können Sie Wartung minimieren. Sie können anschließend detaillierte Regeln definieren, die zu einer bestimmte geschäftliche Zielsetzung passen.

Wenn die Dimensionshierarchien, die in Regeln verwendet werden, aktualisiert werden, setzt das System die Aktualisierungen automatisch um.

Wenn eine Ebene der Granularität in den Regeln nicht mehr erforderlich ist, kann die Regel ablaufen.

Beispielsweise wird eine bestimmte Kostenverhaltensregel für den Finanzkostenobjekt-Dimensionshierarchieknoten nicht mehr benötigt. Klicken Sie in diesem Fall auf **Regel ablaufen lassen**, um die Regel ablaufen zu lassen.

| Kostenelement-Dimensionshierarchieknoten | Kostenobjekt-Dimensionshierarchieknoten | Fester Prozentsatz | Fester Betrag | Gültig ab | Gültig bis  |
|---------------------------------------|--------------------------------------|------------------|--------------|------------|-----------|
| Fixkosten                            | Organisation                         | 100,00           | 0.00         | 1/1/2017   | Nie     |
| 10001                                 | Organisation                         | 0.00             | 150,00       | 1/1/2017   | Nie     |
| 10001                                 | Finanzen                              |                  | 50,00        | 1/1/2017   | 20/1/2017 |
| Kostenverhalten oder variable Kosten        | Organisation                         | 0.00             | 0.00         | 1/1/2017   | Nie     |

Jede Gemeinkostenberechnung, die nach dem 20. Januar 2017 ausgeführt wird, berücksichtigt diese Regel nicht mehr.

> [!NOTE] 
> Die Felder **Gültig ab** und **Gültig bis** sind datumwirksam und zeitwirksam. Sie können die Regel ablaufen lassen und am gleichen Tag eine neue Gemeinkostenberechnung ausführen.

## <a name="define-dimension-hierarchies-for-security-setup"></a>Definieren Sie Dimensionshierarchien für die Sicherheitseinrichtung

Kostenrechnungsdaten sollen für alle Manager bereitgestellt werden, die für eine Berichtseinheit zuständig sind. In der Kostenrechnungsterminologie wird eine Berichtseinheit durch ein Kostenobjekt oder als Satz von Kostenobjekten dargestellt.

Möglicherweise sind alle Manager in der Lage, auf sehr vertrauliche Unternehmensdaten, wie Umsatzerlöse und Gewinnspannen zuzugreifen. Daher ist es wichtig, dass die Sicherheit eingerichtet wird, damit die Manager nur die Daten anzeigen, die für sie relevant sind. Um die Datensicherheit zu steuern, definieren Sie Dimensionshierarchien.

- Die Verwendung von Dimensionshierarchien gilt nur, wenn der Dimensionswert, der in der Dimensionshierarchiereferenz ausgewählt wird, eine Kostenobjektdimension ist.
- Nur eine Dimensionshierarchie kann pro Kostenobjektdimension in der Zugriffslistenhierarchie aktiviert werden.

**Dimensionshierarchiedetails**

| Dimensionshierarchiename | Dimensionen    | Dimensionshierarchie-Typname      | Zugriffslistenhierarchie |
|--------------------------|--------------|------------------------------------|-----------------------|
| Organisation             | Kostenstellen | Dimensionsklassifizierungshierarchie | **Ja**               |

Ein neues Inforegister **Benutzer** ist im Hierarchie-Designer verfügbar. Hier können Sie einen oder mehrere Benutzerkennungen an jedem Knoten in die Hierarchie einfügen.

**Benutzer- und Dimensionsmitgliedsbereiche**

|   Knoten         |   Benutzerkennung        |   Von-Dimensionsmitglied   |   Zieldimensionsmitglied   |
|-----------------|------------------|---------------------------|-------------------------|
| Organisation    | Benjamin, Claire |                           |                         |
| &nbsp;&nbsp;Verwaltung         | April            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Finanzen   | Alicia           | CC002                     | CC003                   |
|                 |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Personalverwaltung        | Arnie            | CC001                     | CC001                   |
| &nbsp;&nbsp;Produktion    | David            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;Verpackung | Ellen            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;Montage  | Chris            | CC006                     | CC006                   |

> [!NOTE] 
> Kostenbuchhalter sollten der höchsten Ebene der Hierarchie zugewiesen werden, damit sie alle Einträge in der Kostenrechnung anzeigen können.

Um die Zugriffslistenhierarchie und die Sicherheitseinstellungen zu aktivieren, wechseln Sie zu **Kostenrechnung** > **Einstellungen** > **Parameter** > **Allgemeines** Wählen Sie den Parameter **Anzeigezugriff für Kostenobjektdimensionsmitglieder zulassen**

Die Einstellungen für die Zugriffslistenhierarchie werden verwendet, um die Daten zu steuern, die in den folgenden Bereichen angezeigt wird:

- Arbeitsbereich **Kostensteuerung** (Client)

    - Daten in Formularen, die verwendet werden, um Details zu Szenarien anzuzeigen

- Arbeitsbereich **Kostensteuerung** (mobile Anwendung):

    - Salden in Karten

- Power BI:

    - Daten, die in Power BI-Visualisierungen angezeigt werden
    - Power BI-Datenvisualisierungen, die im Client der Dynamics 365 Finance eingebettet werden

> [!NOTE] 
> - Bevor sich die Zugriffslistenhierarchie auf Daten in Power BI auswirken kann, müssen die Zugriffslistenhierarchie und Sicherheit auf Zeilenebene in Power BI zugeordnet werden. Weitere Informationen finden Sie unter [Sicherheit für das Kostenrechnungs-Inhaltspack einrichten](../../fin-ops-core/dev-itpro/analytics/setup-security-cost-accounting-content-pack.md).
> - Die Zugriffslistenhierarchie hilft nicht bei der Sicherheit des Exports der Daten in Excel. Daher sollte dieses Berichtstool nur von Kostenbuchhaltern und Managern verwendet werden, die vollen Zugriff zum Anzeigen der Daten haben.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]