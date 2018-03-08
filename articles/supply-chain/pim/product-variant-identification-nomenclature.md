---
title: Bezeichnung der Produktvariantennummern und Namen
description: "In diesem Thema wird beschrieben, wie Sie eine Produktnummernbezeichnung einrichten können, um das feste Format [Produktmasternummer – Konfiguration – Größe – Farbe – Stil] zu ersetzen."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 3a1bfd4bd5f396c05277159ac112eaa8197d5818
ms.openlocfilehash: 067e14d8a0ab9cb5b703c1d2596dab3e20487336
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a>Bezeichnung der Produktvariantennummern und Namen

[!include[banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine Produktnummernbezeichnung einrichten können, um das feste Format [Produktmasternummer – Konfiguration – Größe – Farbe – Stil] zu ersetzen. Die neue Bezeichnung hat ein gezieltes Format, das die Produktmasternummer, aktive Produktdimensionen und Texttrennzeichen Ihrer Wahl umfasst. Darüber hinaus können Sie auch eine Bezeichnung für Produktnamen erstellen. Sie können schließlich auch eine Bezeichnung erstellen, um Konfigurationen zu identifizieren, die vom einschränkungsbasierten Produktkonfigurator erstellt werden. Diese Bezeichnungen können Attribute Ihrer Wahl enthalten.

Die neuen Bezeichnungen für Produktvariantennummern und Produktvariantennamen ermöglichen es Ihnen, Segmente in die Bezeichner für Produktvarianten einzubeziehen. Diese Segmente können die Produktmasternummer und den Produktmasternamen, die Produktdimensionskennungen und -namen, die Nummernkreise, Textkonstanten und Attribute umfassen. Mit dieser Funktionalität können Sie schnell eine bestimmte Produktvariante suchen, wenn einen Auftrag oder eine Bestellung erstellen. Sie erstellen Bezeichnungen sowohl für Produktvariantennummern als auch Produktvariantennamen mithilfe der Seite **Produktbezeichnung**. Um diese Seite zu öffnen, klicken Sie auf **Produktinformationsverwaltung** &gt; **Setup**.

## <a name="nomenclature-of-predefined-product-variants"></a>Bezeichnung der vordefinierten Produktvarianten
Produktvarianten für Produktmaster werden entsprechend einer der drei Konfigurationstechnologien generiert:

-   Vordefinierte Variante
-   Einschränkungsbasiert
-   Dimensionsbasiert

Jede Produktvariante hat eine Nummer und einen Namen, und mit den Produktvarianten-Kennungsbezeichnungen können Sie die Segmente auswählen, die in jede Produktvariantennummer oder -name einbezogen werden. Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:

-   Produktmasternummer
-   Produktmastername
-   Nummernkreiswert
-   Textkonstante
-   Produktdimensionen
    -   Konfigurationskennung oder Name
    -   Farbkennung oder Name
    -   Größenkennung oder Name
    -   Stilkennung oder Name

Nachdem Sie eine Produktvarianten-Kennungsnummernbezeichnung definieren, können Sie diese einer Produktdimensionsgruppe zuordnen. Allen Produktmastern, die auf diese Produktdimensionsgruppe verweisen, werden dann Produktvariantennummern entsprechend der Bezeichnung zugewiesen. Allerdings können Produktvarianten-Namensbezeichnungen nicht Produktdimensionsgruppen zugeordnet werden. Sie können auch eine Produktvarianten-Kennungsbezeichnung einem Produktmaster direkt zuweisen. In diesem Fall werden die Produktvarianten, die zum Produktmaster gehören, Produktvariantennummern und Namen entsprechend den Bezeichnungen zugewiesen.

### <a name="example"></a>Beispiel

Ein T-Shirt (TS1234) wird in drei Größen (S, M, L), in vier Farben (rot, grün, blau, gelb) sowie in zwei Stilen (Polo, mit V-Ausschnitt) hergestellt. Daher sind 24 Produktvarianten möglich (= 3 × 4 × 2). Sie erstellen eine Produktvarianten-Nummernbezeichnung, die die folgenden Segmente hat:

1.  Produktmasternummer
2.  Textkonstante: "-"
3.  Farbe
4.  Textkonstante: "-"
5.  Größe
6.  Textkonstante: "-"
7.  Formatvorlage

In diesem Fall ist die Produktvariantennummer für ein rotes kleines Polo-T-Shirt TS1234-rot-klein-Polo.

## <a name="nomenclature-of-constraint-based-configurations"></a>Einschränkungsbasierte Konfigurationen-Bezeichnung
Für einschränkungsbasierte Konfigurationen können Sie eine dedizierte Bezeichnung für die Konfigurationsproduktdimension erstellen. Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:

-   Nummernkreiswert
-   Textkonstante
-   Attributwert

Jede Komponente in einem Produktkonfigurationsmodell kann eine eigene Konfigurationsbezeichnung haben. Nur Attribute, die der Komponente angehören, können verwendet werden. Attribute aus Unterkomponenten oder Benutzeranforderungen können nicht verwendet werden.

### <a name="example"></a>Beispiel

Ein Produktkonfigurationsmodell hat eine Stammkomponente, die zwei Attribute hat:

-   Material (Plastik, Holz Stahl)
-   Länge (10… 100)

Sie erstellen eine Konfigurationsbezeichnung, die die folgenden Segmente hat:

1.  Attributwert: Material
2.  Textkonstante: "AAA"
3.  Attributwert: Länge

In diesem Fall ist die Konfigurationskennung für Holzmaterial mit einer Länge von 78 WoodAAA78.

## <a name="nomenclature-of-dimension-based-configurations"></a>Dimensionsbasierte Konfigurationsbezeichnung
Für dimensionsbasierte Konfigurationen können Sie eine dedizierte Bezeichnung für die Konfigurationsproduktdimension erstellen. Sie können folgende Segmente auf der Seite **Produktbezeichnungen** auswählen:

-   Nummernkreiswert
-   Textkonstante
-   Konfigurationsgruppenartikel

Sie können eine Konfigurationsbezeichnung für eine Stückliste (BOM) definieren.

### <a name="example"></a>Beispiel

Eine Stückliste besitzt vier Stücklistenpositionen, die in zwei Variantengruppen unterteilt sind:

-   Stücklistenposition: M0007, Standardgehäuse
    -   Konfigurationsgruppe: Gehäuse
-   Stücklistenposition: M0008, Spitzengehäuse
    -   Konfigurationsgruppe: Gehäuse
-   Stücklistenposition: M0021, Vordergrill Tuch
    -   Konfigurationsgruppe: Vordergrill
-   Stücklistenposition: M0022, Vordergrill Metall
    -   Konfigurationsgruppe: Vordergrill

Sie erstellen eine Konfigurationsbezeichnung, die die folgenden Segmente hat:

1.  Konfigurationsgruppe: Gehäuse
2.  Textkonstante: "&"
3.  Konfigurationsgruppe: Vordergrill

In diesem Fall ist die Konfigurationskennung für ein Standardgehäuse mit Tuchvordergrill M0007&M0021.

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a>Bezeichnung für eine Kombination mit Produktvarianten und Konfigurationen
Wenn Sie entweder die einschränkungsbasierte Konfigurationstechnologie oder die dimensionsbasierte Konfigurationstechnologie verwenden, um Produktvarianten für einen Produktmaster zu konfigurieren, können die Produktvariantennummern der Produktvarianten die Bezeichnung aus der Konfigurationsdimension umfassen. Folgen Sie diesen Schritten, um Varianten zu konfigurieren.

1.  Definieren Sie auf der Seite **Produktbezeichnung** eine Produktvarianten-Nummernbezeichnung, die die Konfigurationsdimension umfasst.
2.  Weisen Sie die Bezeichnung einer Produktdimensionsgruppe zu, die die Konfigurationsdimension besitzt.
3.  Definieren Sie eine Konfigurationsbezeichnung für die Komponenten oder die Stücklisten, die für das Konfigurieren von Produktvarianten verwendet werden.

Sie können auch eine Bezeichnungen für die Produktvariantennamen erstellen. Die Produktvariantennamen können konfiguriert werden, um die Konfigurationskennung oder den Namen zu umfassen.

### <a name="example-for-constraint-based-configurations"></a>Beispiele für einschränkungsbasierte Konfigurationen

Für dieses Beispiel können Sie eine Produktvarianten-Nummernbezeichnung verwenden, die aus den folgenden Segmenten besteht:

1.  Produktmasternummer
2.  Textkonstante "\_"
3.  Variante

Die Konfigurationsbezeichnung besteht aus den folgenden Segmenten:

1.  Attributwert: Material
2.  Textkonstante: "AAA"
3.  Attributwert: Länge

Sie geben die folgenden Werte für Segmente ein:

-   Produktmasternummer = **M0099**
-   Material = **Plastik**
-   Länge = **12**

In diesem Fall wird die Produktvariantennummer M0099\_PlasticAAA12 lauten.

### <a name="example-for-dimension-based-configurations"></a>Beispiele für einschränkungsbasierte Konfigurationen

Für dieses Beispiel können Sie eine Produktvarianten-Nummernbezeichnung verwenden, die aus den folgenden Segmenten besteht:

1.  Produktmasternummer
2.  Textkonstante "//"
3.  Variante

Die Konfigurationsbezeichnung besteht aus den folgenden Segmenten:

1.  Konfigurationsgruppe: Gehäuse
2.  Textkonstante: "&"
3.  Konfigurationsgruppe: Vordergrill

Sie geben die folgenden Werte für Segmente ein:

-   Produktmasternummer = **D0123**
-   Gehäuse = **M0008**
-   Vordergrill = **M0022**

In diesem Fall wird die Produktvariantennummer D0123//M0008&M0022 lauten.

## <a name="numbering-conflicts"></a>Anzahl von Konflikten
In einigen Fällen erzeugt eine Produktvarianten-Nummernbezeichnung, die Sie eingerichtet haben, möglicherweise keine eindeutigen Produktvariantennummern. Die Produktvariantennummern sind beispielsweise nicht eindeutig, wenn eine aktive Produktdimension nicht in der Bezeichnung für einen Produktmaster enthalten ist, der die vordefinierte Technologie für Variantenkonfiguration verwendet. Die Art, wie Sie Konflikte handhaben, ist je nach Konfigurationstechnik unterschiedlich.

### <a name="predefined-variants"></a>Vordefinierte Variante

Ein Fehler tritt auf, wenn Sie manuell oder automatisch versuchen, Produktvarianten zu erstellen, bzw. zu generieren, und mehr als eine Produktvariante letztendlich dieselbe Produktvariantennummer besitzt. Um dieses Szenarios zu vermeiden, sollten Sie alle aktiven Produktdimensionen in der Produktdimensionsgruppe verwenden. Alternativ beziehen Sie einen Nummernkreis ein, um sicherzustellen, dass die Produktvariantennummern eindeutig sind.

### <a name="constraint-based-configurations"></a>Einschränkungsbasierte Konfigurationen

Abhängig von der Bezeichung versucht das System möglicherweise, eine nicht eindeutige Produktvariantennummer zu einer Konfiguration hinzuzufügen. In diesem Fall verwendet das System stattdessen den Nummernkreis für die Konfigurationsdimension als Produktvariantennummer, und Sie erhalten eine Warnung. Um dieses Szenarios zu vermeiden, sollten Sie genügend Attribute in die Bezeichnung einbeziehen, um eindeutige Produktvariantennummern zu gewährleisten. Sie sollten auch sicherstellen, dass die Option **Wiederverwenden** für die Komponente eingeschaltet ist.

### <a name="dimension-based-configurations"></a>Dimensionsbasierte Konfigurationen

Während eines Schritts im Konfigurationsprozess schlägt das System einen Konfigurationswert gemäß der Bezeichnung vor. In diesem Schritt können Sie den Konfigurationswert manuell ändern. Wenn Sie die Konfiguration speichern, überprüft das System, dass der Konfigurationswert eindeutig ist. Wenn der Wert, den Sie eingegeben haben, nicht eindeutig ist, erhalten Sie eine Fehlermeldung. Um die Konfiguration zu speichern, müssen Sie einen eindeutigen Konfigurationswert eingeben.

<a name="see-also"></a>Siehe auch
--------

[Erstellen einer Produktnummerenbezeichnung für vordefinierte Produktvarianten](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[Erstellen einer Produktnummerenbezeichnung für konfigurierte Produktvarianten](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


