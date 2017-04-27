---
title: Produktnummerbezeichnung
description: "In diesem Thema wird beschrieben, wie Sie eine Produktnummerbezeichnung einrichten können, um das feste Format [Produktmasternummer: Konfiguration: Größe: Farbe: Stil] mit einem Zielfoirmat zu ersetzen, das Produktmasternummer, aktive Produktdimensionen und Texttrennzeichen für Ihre Auswahl enthält. Sie können auch eine Bezeichnung erstellen, um Konfigurationen zu identifizieren, die vom einschränkungsbasierten Produktkonfigurator erstellt werden. Diese Bezeichnungen können Attribute Ihrer Wahl enthalten."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220104
ms.assetid: 31c9efb4-b5f6-4af3-b884-8f1e128469bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 58afcd62e7ef317e624fd26d198c2606bf53e6a5
ms.lasthandoff: 03/31/2017


---

# <a name="product-number-nomenclature"></a>Produktnummerbezeichnung

[!include[banner](../includes/banner.md)]


In diesem Thema wird beschrieben, wie Sie eine Produktnummerbezeichnung einrichten können, um das feste Format [Produktmasternummer: Konfiguration: Größe: Farbe: Stil] mit einem Zielfoirmat zu ersetzen, das Produktmasternummer, aktive Produktdimensionen und Texttrennzeichen für Ihre Auswahl enthält. Sie können auch eine Bezeichnung erstellen, um Konfigurationen zu identifizieren, die vom einschränkungsbasierten Produktkonfigurator erstellt werden. Diese Bezeichnungen können Attribute Ihrer Wahl enthalten.

Die neue Bezeichnung  der Produktvariantennummernbezeichnung ermöglicht den Einbezug von Segmenten im Produktvariantenbezeichner. Diese Segmente können die Produktmasternummern, Produktdimensionen, Nummernkreise, Sequenzen, Textkonstanten und Attribute enthalten. Mit dieser Funktionalität können Sie schnell eine bestimmte Produktvariante suchen, wenn einen Auftrag oder eine Bestellung erstellen.

## <a name="nomenclature-of-predefined-product-variants"></a>Bezeichnung der vordefinierten Produktvarianten
Produktvarianten für Produktmaster werden entsprechend einer der drei Konfigurationstechnologien generiert:

-   Vordefinierte Variante
-   Einschränkungsbasiert
-   Dimensionsbasiert

Jede Produktvariante hat eine Nummer, und mit der Produktvariantenkennungsbezeichnung können Sie die Segmente auswählen, die in jeder Produktvariantennummer enthalten sind. Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen.

-   Produktmasternummer
-   Nummernkreiswert
-   Textkonstante
-   Produktdimensionen
    -   Variante
    -   Farbe
    -   Größe
    -   Formatvorlage

Nachdem eine Produktvariantenkennungsbezeichnung definiert wurde, kann sie einer Produktdimensionsgruppe zugewiesen werden. Anschließend stehen allen Produktmaster, die auf diese Produktdimensionsgruppe verweisen, Produktvariantennummern entsprechend der Bezeichnugn zur Verfügung. Es ist auch möglich, eine Produktvariantenkennungsbezeichnung direkt einem Produktmaster, in diesem Fall die Produktvarianten, die diesem Master gehören, Produktvariantennummern entsprechend der Bezeichnung zuzuweisen.

### <a name="example"></a>Beispiel

Ein T-Shirt (TS1234) wird in 3 verschiedenen Größen (S, M, L), 4 verschiedenen Farben (Rot, Dunkelblau, Gelb, Blau,) und 2 Typen (Polo, V-Ausschnitt) produziert, was insgesamt 24 mögliche Produktvarianten ergibt. Eine Produktvariantenkennungsnomenklatur wird mit folgenden Segmente erstellt:

1.  Produktmasternummer
2.  Textkonstante: '-'
3.  Farbe
4.  Textkonstante: '-'
5.  Größe
6.  Textkonstante: '-'
7.  Formatvorlage

Die Produktvariantennummer für Rot, Small, Polo ist: TS1234-Rot-Small-Polo.

## <a name="nomenclature-of-constraintbased-configurations"></a>Einschränkungsbasierte Konfigurationen-Bezeichnung
Für einschränkungsbasierte Konfigurationen kann eine für die dedizierte zum Konfigurationsproduktdimension angegeben werden. Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen.

-   Nummernkreiswert
-   Textkonstante
-   Attributwert 

Jede Komponente in einem Produktkonfigurationsmodell kann eine eigene Konfigurationsbezeichnung haben. Nur Attribute, die möglicherweise der Komponente angehören, werden verwendet. Attribute aus Unterkomponenten oder Benutzeranforderungen sind nicht verfügbar.

### <a name="example"></a>Beispiel

Ein Produktkonfigurationsmodell hat eine Stammkomponente mit zwei Attributen.

-   Material (Plastik, Holz Stahl)
-   Länge (10… 100)

Eine Konfigurationsbezeichnung wird nach folgenden Segmenten definiert:

1.  Attributwert: Material
2.  Textkonstante: 'AAA'
3.  Attributwert: Länge

Die Kennung für hölzernes Material mit einer Länge von 78 erhält folgende Konfiguration: ID: WoodAAA78.

## <a name="nomenclature-of-dimensionbased-configurations"></a>Dimensionsbasierte Konfigurationsbezeichnung
Für dimensionsbasierte Konfigurationen kann eine für die dedizierte zum Konfigurationsproduktdimension angegeben werden. Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen.

-   Nummernkreiswert
-   Textkonstante
-   Konfigurationsgruppenartikel

Eine Konfigurationsbezeichnung kann für eine Stückliste (BOM) definiert werden.

### <a name="example"></a>Beispiel

Eine Stückliste verfügt über 4 Stücklistenpositionen die in 2 Konfigurationsgruppen aufgeteilt werden.

-   Stücklistenposition: M0007, Standardgehäuse
    -   Konfigurationsgruppe: Gehäuse
-   Stücklistenposition: M0008, Spitzengehäuse
    -   Konfigurationsgruppe: Gehäuse
-   Stücklistenposition: M0021, Vordergrill Tuch
    -   Konfigurationsgruppe: Vordergrill
-   Stücklistenposition: M0022, Vordergrill Metall
    -   Konfigurationsgruppe: Vordergrill

Eine Konfigurationsbezeichnung wird nach folgenden Segmenten definiert:

1.  Konfigurationsgruppe: Gehäuse
2.  Textkonstante: '&'
3.  Konfigurationsgruppe: Vordergrill

Die Kennung für ein Standardgehäuse mit Tuchvordergrill ist: M0007&M0021.

## <a name="nomenclature-of-a-combination-of-product-variants-and-configurations"></a>Bezeichnung einer Kombination mit Produktvarianten und Konfigurationen
Wenn Sie entweder einschränkungsbasierte oder dimensionsbasierte Konfigurationstechnologie verwenden, um Produktvarianten für einen Produktmaster zu konfigurieren, können die Produktvarianten, Produktvariantennummern abrufen, die Bezeichnung der Konfigurationsdimension enthalten. Folgen Sie diesen Schritten, um Varianten zu konfigurieren:

1.  Definieren Sie eine Produktvariantennummernbezeichnung, die die Konfigurationsdimension auf der Seite **Produktbezeichnung** enthält.
2.  Bezeichnung einer Produktdimensionsgruppe mit der Konfigurationsdimension zuweisen.
3.  Definieren Sie eine Konfigurationsbezeichnung für die Komponenten oder die Stücklisten, die für das Konfigurieren von Produktvarianten verwendet werden.

### <a name="example-for-constraint-based-configurations"></a>Beispiele für einschränkungsbasierte Konfigurationen

In diesem Beispiel können Sie eine Produktvariantennummernbezeichnung verwenden, die aus den folgenden Segmente besteht:

1.  Produktmasternummer
2.  Textkonstante '\_'
3.  Variante

Die Konfigurationsbezeichnung kann aus den folgenden Segmenten bestehen:

1.  Attributwert: Material
2.  Textkonstante: 'AAA'
3.  Attributwert: Länge

Sie können den folgenden Werten für Segmente eingegeben:

-   Produktmasternummer = M0099
-   Material = Plastik
-   Länge = 12

Die Produktvariantennummer wird: M0099\_PlasticAAA12.

### <a name="example-for-dimension-based-configurations"></a>Beispiele für einschränkungsbasierte Konfigurationen

In diesem Beispiel können Sie eine Produktvariantennummernbezeichnung verwenden, die aus den folgenden Segmente besteht:

1.  Produktmasternummer
2.  Textkonstante: '//'
3.  Variante

Die Konfigurationsbezeichnung kann aus den folgenden Segmenten bestehen:

1.  Konfigurationsgruppe: Gehäuse
2.  Textkonstante: '&'
3.  Konfigurationsgruppe: Vordergrill

Sie können den folgenden Werten für Segmente eingegeben:

-   Produktmasternummer = D0123
-   Gehäuse = M0008
-   Vordergrill = M0022

Die Produktvariantennummer wird: D0123//M0008&M0022.

## <a name="numbering-conflicts"></a>Anzahl von Konflikten
Es ist möglich, Produktvariantennummernbezeichnungen einzurichten, die nicht zu eindeutigen Produktvariantennummern führen. So kann dies beispielsweise auftreten, wenn eine aktive Produktdimensionen nicht in der Bezeichnung für den Produktmaster enthalten ist, der vordefinierte Technologie für Variantenkonfiguration verwendet. Konflikte werden für die verschiedenen Konfigurationstechnologien unterschiedlich behandelt.

### <a name="predefined-variants"></a>Vordefinierte Variante

Ein Fehler tritt auf, wenn Sie manuell oder automatisch versuchen, Produktvarianten zu generieren, bei denen eine oder mehrere mit der gleichen Produktvariantennummer enden. Um dies zu vermeiden, sollten Sie alle aktiven Produktdimensionen in der Produktdimensionsgruppe verwenden, oder führen Sie einen Nummernkreis ein, um sicherzustellen, dass die Produktvariantennummern eindeutig sind.

### <a name="constraint-based-configurations"></a>Einschränkungsbasierte Konfigurationen

Abhängig von der Bezeichung versucht das System möglicherweise, eine nicht eindeutige Produktvariantennummer zu einer Konfiguration hinzuzufügen. In diesem Fall verwendete das System den Nummernkreis für die Konfigurationsdimension als Produktvariantennummer stattdessen. Wenn dies der Fall ist, erhalten Sie eine Warnung. Um dies zu vermeiden, sollten Sie genügend Attribute in der Bezeichnung einschließen, um die Eindeutigkeit sicherzustellen und sicherzustellen, dass die Option **Wiederverwenden** für die Komponente aktiviert ist.

### <a name="dimension-based-configurations"></a>Dimensionsbasierte Konfigurationen

Der Konfigurationsprozess enthält einen Schritt, in dem das System einen Konfigurationswert entsprechend der Bezeichnung vorschlägt. In diesem Schritt können Sie den Konfigurationswert manuell ändern. Wenn Sie die Konfiguration speichern, prüft das System, ob der Konfigurationswert eindeutig ist. Ist dies nicht der Fall, wird eine Fehlermeldung angezeigt. Sie müssen einen eindeutigen Konfigurationswert eingeben, um die Konfiguration zu speichern.



<a name="see-also"></a>Siehe auch
--------

[Erstellen einer Produktnummerenbezeichnung für vordefinierte Produktvarianten (Aufgabenleitfaden)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-predefined-product-variants/)

[Erstellen einer Produktnummerenbezeichnung für vordefinierte Produktvarianten (Aufgabenleitfaden)](http://ax.help.dynamics.com/en/wiki/create-a-product-number-nomenclature-for-configured-product-variants/)




