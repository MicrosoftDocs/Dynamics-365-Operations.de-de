---
title: Produktbezogene Übersetzungen – FAQ
description: In diesem Thema wird beschrieben, wie Übersetzungen für Produkte, Produktdimensionswerte und Produktattribute verwaltet werden.
author: cvocph
manager: tfehr
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList, EcoResProductListPage, EcoResProductVariants, EcoResProductDetailsExtended, EcoResProductCreate, EcoResProductDetails, RetailSizeGroupTable, RetailStyleGroupTable, RetailColorGroupTable, PCTranslationLanguageLookup, EcoResProductCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 424919625f39127a1b2dcc6be446d01804f79f7e
ms.sourcegitcommit: 3cc289399e8879b499e31a9559e1031d6ca8570a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885968"
---
# <a name="product-related-translations-faq"></a>Produktbezogene Übersetzungen – FAQ

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Übersetzungen für Produkte, Produktdimensionswerte und Produktattribute verwaltet werden. 

<a name="what-product-related-data-can-be-translated"></a>Welche produktbezogenen Daten können übersetzt werden?
--------------------------------------------

Sie können Übersetzungen für folgende produktbezogene Informationen erstellen:
-   Namen und Beschreibungen von Produkten.
-   Beschreibungen, Anzeigenamen und Hilfetext von Produktattributwerten.
-   Namen und Beschreibungen von Produktdimensionswerten.

Sie können die produktbezogenen Informationen in jede Sprache übersetzen, die auf der Seite **Textübersetzung** verfügbar ist. Weitere Informationen finden Sie im Abschnitt **Wie erstelle ich Übersetzungen für produktbezogene Informationen**.

## <a name="where-can-i-view-the-translated-information"></a>Wo kann ich die übersetzten Informationen anzeigen lassen?
Sie können Übersetzungen von produktbezogenen Informationen in jedem externen Quelldokument anzeigen, beispielsweise in einer Rechnung, falls es in einer Sprache verfasst ist, für die Übersetzungen verfügbar sind.

## <a name="how-do-i-create-translations-for-product-related-information"></a>Wie erstelle ich Übersetzungen für produktbezogene Informationen?
Gehen Sie folgendermaßen vor, um Übersetzungen für ein Produkt zu erstellen:
1.  Klicken Sie auf **Produktinformationsverwaltung** &gt; **Allgemein** &gt; **Freigegebene Produkte**.
2.  Wählen Sie ein Produkte, und klicken Sie im Aktivitätsbereich in der Gruppe **Sprache** auf **Übersetzung**.
3.  Wählen Sie auf der Seite **Textübersetzung** im Feld **Sprache** die Sprache aus. Um weitere Sprachen hinzuzufügen, erweitern Sie das Feld **Sprache** und klicken anschließend auf **OK**.
4.  Geben Sie in der Gruppe **Übersetzter Text** im Feld **Beschreibung** und **Produktname** die Übersetzungen ein.

Gehen Sie folgendermaßen vor, um Übersetzungen für Produktattribute zu erstellen:
1.  Klicken Sie auf **Produktinformationsverwaltung** &gt; **Allgemein** &gt; **Freigegebene Produkte**.
2.  Unter **Einstellungen** klicken Sie auf **Attribute** und klicken dann auf **Attribute**.
3.  Auf der Seite **Attribute** klicken Sie auf **Übersetzen**.
4.  Wählen Sie auf der Seite **Textübersetzung** im Feld **Sprache** die Sprache aus. Um weitere Sprachen hinzuzufügen, erweitern Sie das Feld **Sprache** und klicken anschließend auf **OK**.
5.  Geben Sie in der Gruppe **Übersetzter Text** im Feld **Beschreibung**, **Produktname** und **Hilfetext** die Übersetzungen ein.

Gehen Sie folgendermaßen vor, um Übersetzungen für Produktdimensionswerte zu erstellen:
1.  Klicken Sie auf **Produktinformationsverwaltung** &gt; **Allgemein** &gt; **Freigegebene Produkte**.
2.  Wählen Sie eine Produkt und klicken dann auf **Produktdimension**.
3.  Wählen Sie einen der Links für die Produktdimensionen aus: **Konfigurationen**, **Größen**, **Farben** oder **Stil**.
4.  Wählen Sie einen Dimensionswert aus, und klicken Sie anschließend auf **Übersetzen**.
5.  Wählen Sie auf der Seite **Textübersetzung** im Feld **Sprache** die Sprache aus. Um weitere Sprachen hinzuzufügen, erweitern Sie das Feld **Sprache** und klicken anschließend auf **OK**.
6.  Geben Sie in der Gruppe **Übersetzter Text** in den Feldern **Name** und **Beschreibung** die Übersetzung ein.

## <a name="can-the-names-of-product-variants-be-translated"></a>Können die Namen von Produktvarianten übersetzt werden?
Produktvarianten basieren auf den Dimensionen eines freigegebenen Produkts. Produktvariantennamen basieren auf einer Kombination von Dimensionswerten. Wenn die Dimensionswerte, die einer Produktvariante zugeordnet sind, übersetzt werden, wird der Name der Produktvariante in der übersetzten Version angezeigt.  

**Beispiel**  

Ihr Produkt ist ein T-Shirt, das in verschiedene Größen und Farben erhältlich ist, und die verschiedenen Namen basieren auf den folgenden Details:
-   Produktnummer: \#3
-   Dimensionen: Größe und Farbe
-   Größendimensionswerte: Klein, mittel, groß
-   Farbdimensionswerte: Rot, grün, schwarz

Der Name einer Produktvariante, die auf den Dimensionswerten "Klein" und "Rot" basiert, ist **\#3:Small:Red**.  

Ein Debitor möchte mehrere kleinere, rote T-Shirts kaufen und der Name des T-Shirts muss auf Französisch in der Rechnung angezeigt werden. Sie übersetzen die Dimensionswerte "Klein" und "Rot" in Französisch und der Name der Produktvariante ist **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tipp</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Um die bevorzugte Sprache eines Debitors festzulegen, führen Sie folgende Schritte aus:
<ol><br/><li>Klicken Sie auf <strong>Vertrieb und Marketing</strong> &gt; <strong>Allgemein</strong> &gt; <strong>Debitoren</strong> &gt; <strong>Alle</strong> <strong>Debitoren</strong>.</li>
<li>Doppelklicken Sie auf ein Debitorenkonto, um die Seite <strong>Debitor</strong> zu öffnen. Wählen Sie auf der Registerkarte <strong>Allgemeines</strong> im Feld <strong>Sprache</strong> die gewünschte <strong>Sprache</strong> aus.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Was passiert, wenn ein Debitor eine bevorzugte Sprache hat, für die keine Übersetzungen verfügbar sind?
Wenn Übersetzungen nicht in der bevorzugten Sprache des Debitors verfügbar sind, werden die Namen und Beschreibungen in der globalen Sprache des eigenen Unternehmens angezeigt.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Kann ich Übersetzungen für eine Reihe von Dimensionswerten gleichzeitig verwalten?
Dimensionswerte sind produktspezifisch und Sie können die Übersetzungen für die Dimensionswerte für jedes Produkt verwalten. Wenn Sie jedoch eine Dimensionswertgruppe erstellen und Übersetzungen für die Werte in der Wertsgruppe erstellen, erleichtert dies, die Übersetzungen zu verwalten.   

**Beispiel**  

Das Unternehmen produziert T-Shirts in verschiedenen Formaten, jedes Format ist in den Größen Klein, Mittel und Groß verfügbar. Die Größen werden in einer Dimensionswertgruppe gesammelt. Wenn ein neues T-Shirt Format hinzugefügt wird, können Sie es der Dimensionswertgruppe zuordnen, die für Größen verwendet wird, sodass alle Größen für das Produkt verfügbar sind. Sie können auchÜbersetzungen für die Größen in der Dimensionswertgruppe jederzeit hinzufügen oder ändern.  

Ein Dimensionswert, der einem Produkt eine Dimensionsvariantnegruppe zugeordnet ist, muss vom Produktvariantengruppe verwaltet werden.   
Gehen Sie folgendermaßen vor, um eine Dimensionswertgruppe zu erstellen.
1.  Klicken Sie auf **Produktinformationsmanagement** &gt; **Einstellungen** &gt; **Variantengruppen**.
2.  Wählen Sie **Größe** **Gruppen**, **Farbgruppen**, oder **Stilgruppen**.
3.  Klicken Sie auf **Neu**, und dann geben Sie den Namen für die Gruppe in den Feldern **Größe** **Gruppe**, **Farbgruppe** oder **Stilgruppe** ein. Klicken Sie auf **Größen**, **Farben**, oder **Stil**, um Positionen für die Gruppen zu erstellen.
4.  Klicken Sie auf den Seiten **Größe** **Gruppe**-Positionen, **Farbe** **Gruppe** **-Positionen** oder **Stilgruppenpositionen** auf **Neu**, und erstellen Sie dann die Größen, Farben und Stile für die Gruppen.

Um Übersetzungen für Werte in einer Dimensionswertgruppe zu verwalten, führen Sie diese Schritte aus:
1.  Führen Sie die Schritte des vorherigen Verfahrens zum Erstellen einer Dimensionswertgruppe, aus, um die Seite **Größengruppenpositionen** **Farbgruppenpositionen** oder **Positionen von Stilgruppen** zu öffnen.
2.  Klicken Sie auf **Textübersetzung**. Geben Sie auf der Seite **Textübersetzung** in der Gruppe **Übersetzter Text** in den Feldern **Name** und **Beschreibung** die Übersetzungen ein.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Wann können Übersetzungen von produktbezogenen Informationen verwaltet werden?
Übersetzungen von produktbezogenen Informationen können jederzeit verwaltet werden. Wenn Übersetzungen für einen Dimensionswert aktualisiert werden, der einem Produkt zugeordnet ist, werden die Produktdaten aktualisiert, unabhängig davon, ob das Produkt Transaktionen hat.





