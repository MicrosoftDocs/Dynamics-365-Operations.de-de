---
title: Produktdimensionen
description: Es gibt fünf Produktdimensionen – Farbe, Konfiguration, Größe, Stil und Version. Sie kombinieren Produktdimensionen in den Dimensionsgruppen und weisen diesen Dimensionsgruppen Produktmaster zu. Diese Kombinationen der Produktdimensionen bestimmen, wie Produktvarianten definiert sind.
author: t-benebo
manager: tfehr
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bdfd9482d30bd65cf84fae032df78e1243e05239
ms.sourcegitcommit: 97d4a9bd442fe20f90605d8154c3a947c7645b37
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895448"
---
# <a name="product-dimensions"></a>Produktdimensionen

[!include [banner](../includes/banner.md)]

Es gibt fünf Produktdimensionen: Farbe, Konfiguration, Größe, Stil und Version. Sie kombinieren Produktdimensionen in den Dimensionsgruppen und weisen diesen Dimensionsgruppen Produktmaster zu. Diese Kombinationen der Produktdimensionen bestimmen, wie Produktvarianten definiert sind.

Produktdimensionen sind Merkmale, die dazu dienen, eine Produktvariante zu identifizieren. Sie können Kombinationen der Produktdimensionen verwenden, um Produktvarianten zu definieren. Um eine Produktvariante zu erstellen, müssen Sie mindestens eine Produktdimension für einen Produktmaster definieren.

## <a name="product-variants"></a>Produktvarianten

Produktvarianten werden auch als Artikel bezeichnet. Ein Artikel ist ein materielles Produkt, was ist nicht dasselbe wie eine Dienstleistung ist. Es ist es jedoch auch möglich, einen Produktmaster mit dem Servicetyp zu definieren. Wenn Sie den Typ „Dienstleistung“ verwenden, können Sie Produktvarianten angeben, die Dienstleistungen umfassen. So können Sie beispielsweise einen Produktmaster für Beratungsarbeit und Produktvarianten für Arbeit angeben, die von leitenden Beratern und von Juniorberatern ausgeführt wird.

## <a name="product-dimensions"></a>Produktdimensionen

Eine Produktvarianten kann basieren auf Produktdimensionenwerten generiert werden.

Produktdimensionswerte für die Größen‑, Farb‑ und Stilabmessungen können an folgenden Speicherorten erstellt werden:

- Seite **Größe** (**Produktinformationsverwaltung \> Einrichtung \> Dimensions‑ und Variantengruppen \> Größen**)
- Seite **Farbe** (**Produktinformationsverwaltung \> Einrichtung \> Dimensions‑ und Variantengruppen \> Farben**)
- Seite **Stil** (**Produktinformationsverwaltung \> Einrichtung \> Dimensions‑ und Variantengruppen \> Stile**)

Produktdimensionswerte für die Variantendimension werden üblicherweise entweder mithilfe des Variantenkonfigurators oder des dimensionsbasierten Konfigurators erstellt. 

Produktversionen werden normalerweise für bestimmte Versionen erstellt, wenn sich das Produkt während seines Lebenszyklus weiterentwickelt. Produktversionen werden später in diesem Thema ausführlich behandelt.

Produktdimensionen können auch auf der Seite **Produktdimensionen** erstellt und verwaltet werden, auf die Sie von folgenden Orten aus zugreifen können:

- Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Produktmaster**. Wählen Sie im Aktivitätsbereich **Produktdimensionen** aus.
- Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Alle Produkte und Produktmaster**. Wählen Sie einen Produktmaster aus. Wählen Sie im Aktivitätsbereich **Produktdimensionen** aus.
- Wechseln Sie zu **Produktinformationsverwaltung \> Freigegebene Produkte**. Wählen Sie einen Produktmaster aus. Wählen Sie im Aktivitätsbereich auf der Registerkarte **Produkt** in der Gruppe **Produktmaster** die Option **Produktdimensionen** aus.

Die Anzahl von Varianten, die Sie für einen Artikel erstellen können, hängt von der Anzahl der möglichen Produktdimensionskombinationen ab.

> [!TIP]
> Wenn Sie ein Produkt beispielsweise auf einer Auftragsposition verwenden, wählen Sie die Produktdimensionen aus, um die Produktvariante zu ermitteln, mit der Sie arbeiten möchten.

## <a name="example"></a>Beispiel

Ein Unternehmen verkauft Denim-Jeans. Für den Artikel *Jeans* werden die Produktdimensionen „Farbe“ und „Größe“ verwendet. Die Jeans wird in drei verschiedenen Farben und sechs verschiedenen Größen angeboten. Die Farben sind blau, schwarz und braun. Die Größen sind XS, S, M, L, XL und XXL. Nicht alle Größen sind in allen drei Farben verfügbar. Wenn alle Kombinationen verfügbar wären, ergäbe dies 18 unterschiedliche Jeanstypen. In diesem Beispiel werden jedoch nur die folgenden neun Produktvariantenkombinationen produziert.

| Farbe | Größe |
|-------|------|
| Blau  | XS   |
| Blau  | Sa    |
| Blau  | Mo    |
| Schwarz | Mo    |
| Schwarz | L    |
| Schwarz | XL   |
| Braun | L    |
| Braun | XL   |
| Braun | XXL  |

## <a name="the-version-product-dimension"></a>Die Produktdimension „Version“

„Version“ ist eine Produktdimension, mit der Sie mehrere Versionen eines Produkts in der gesamten Lieferkette verwalten und verfolgen können. Die Versionsverfolgung ist entscheidend für den Erfolg von Herstellern, die in einer Welt mit ständig verkürzten Produktlebenszyklen, erhöhten Qualitäts‑ und Zuverlässigkeitsanforderungen und einem erhöhten Fokus auf Produktsicherheit tätig sind.

Als Standardproduktdimension verhält sich die „Version“ ähnlich wie die vorhandenen Produktdimensionen (Größe, Stil, Farbe und Konfiguration). Daher können Sie sie neben der Verfolgung von Produktversionen auch für andere Zwecke verwenden.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Die Dimension „Version“ aktivieren

#### <a name="before-you-turn-on-the-version-dimension"></a>Bevor Sie die Dimension „Version“ aktivieren

Wenn Sie die Dimension Version aktivieren, können einige Funktionen beschädigt werden oder nicht mehr wie erwartet funktionieren, wenn Sie andere Lösungen installiert haben, die den Lagerungsdimensionen Anpassungen hinzufügen. Damit die Dimension „Version“ voll funktionsfähig ist, müssen Sie diese Lösungen möglicherweise aktualisieren, damit sie die Dimension „Version“ in ihre Verweise auf die Lagerungsdimensionen aufnehmen.

Achten Sie beim Testen Ihrer Lösungen auf Kompatibilität mit der Dimension „Version“ auf die folgenden Elemente:

1. **Funktionalität** – Am wichtigsten ist, dass alle Anpassungen, die die Lagerungsdimensionen betreffen, bewertet werden müssen, um sicherzustellen, dass sie in Verbindung mit der Dimension „Version“ funktionieren.
1. **Verweise auf die Lagerungsdimensionen** – Achten Sie auf Verweise auf die Lagerungsdimensionen (d. h. auf Orte, an denen explizit auf die Dimensionen verwiesen wird). Verweise zu `InventDimId` sollte sofort funktionieren, aber achten Sie auf Hinweise auf Stil oder Farbe. Überprüfen Sie beispielsweise die folgenden Elemente:

    - API-Aufrufe in erweiterten Klassen
    - Alle Verweise auf bestimmte Lagerungsdimensionen im Erweiterungscode (Dieser Code muss die Dimension „Version“ zusammen mit den Stil‑, Farb‑ und Größendimensionen enthalten.)

1. **Verweise auf veraltete API-Aufrufe:** Bei der Einführung der Versionsdimension hat Microsoft versucht, so wenige APIs wie möglich überflüssig zu machen. Die wenigen APIs, die veraltet sind, zeigen beim Einschalten des Konfigurationsschlüssels **Produktdimension „Version“** eine Warnung an. Aufrufe dieser API müssen in Ihren erweiterten Lösungen behoben werden, bevor Sie die Dimension „Version“ in einem Produktionssystem aktivieren. Hier sind die versionsspezifischen veralteten APIs:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Karten** – Wenn Karten die Lagerungsdimensionen verwenden, muss die entsprechende Beziehungszuordnung zu diesen Karten aktualisiert werden, sodass sie die Dimension „Version“ enthalten. Achten Sie in den erweiterten Modell‑ oder Tabellenerweiterungen auf Tabellen, in denen die Felder Lagerungsdimensionen enthalten.
1. **Microsoft Dynamics 365 Commerce-Funktionalität** – Nach dem Aktivieren wird die Dimension „Version“ im gesamten Commerce-spezifischen Code in Dynamics 365 Supply Chain Management angezeigt. Die Dimension „Version“ wird jedoch noch nicht von der Commerce-Kanaldatenbank oder in den Verkaufsstellen POS- bzw. E-Commerce-Anwendungen unterstützt. Diese Commerce-spezifischen Anwendungen unterstützen keine Benutzer, die Bestand nach Versionsdimension verkaufen/versenden oder zurückgeben/empfangen. Suchfunktionen für die Verfügbarkeit von Bestand unterscheiden keinen Bestand nach Versionsdimension in Commerce-Apps. Dieses Verhalten ähnelt dem aktuellen Verhalten der Konfigurationsdimension in Commerce.

#### <a name="turn-on-the-version-dimension"></a>Die Dimension „Version“ aktivieren

Bevor Sie die Dimension „Version“ nutzen können, muss sie auf Ihrem System aktiviert werden. Diese Aufgabe erfordert Administratorberechtigungen.

1. Wechseln Sie zu **Systemverwaltung \> Arbeitsbereiche \> Funktionsverwaltung**.
1. Aktivieren Sie die Funktion mit dem Namen *Produktdimension „Version“*. (Weitere Informationen finden Sie unter [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Setzen Sie Ihr System in den [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Gehen Sie zu **Systemadministration \> Einrichten \> Lizenzkonfiguration**.
1. Erweitern Sie auf der Registerkarte **Konfigurationsschlüssel** **Handel**, und aktivieren Sie das Kontrollkästchen für **Produktdimension – Version**.
1. Schalten Sie den [Wartungsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) aus.

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Bereiche, in denen die Dimension „Version“ nicht unterstützt wird

Die folgenden Bereiche unterstützen die Dimension „Version“ nicht, da die Einführung dieser Dimension zu wesentlichen Änderungen führen würde:

- Kostenobjekt, monatliche Abrechnung
- Kostenobjektaufstellungs-Cache
- MCR-Verkaufsstatistik pro Artikel
- Lieferantenkataloge
- EcoResProductDimensionGroupEntity

Darüber hinaus unterstützen die Funktionen zur Auftragserstellung und Auftragsabwicklung in Commerce (z. B. für POS‑, Call Center‑ und E-Commerce-Aufträge) die Dimension „Version“ nicht. Es gibt keinen bestätigten Zeitplan, wann Commerce-Bestellungen erweitert werden, um dies zu unterstützen.

### <a name="functional-characteristics-of-the-version-dimension"></a>Funktionsmerkmale der Dimension „Version“

Die Dimension „Version“ funktioniert wie die anderen Produktdimensionen. Aufgrund ihrer spezifischen Natur und der Absicht, mehrere Versionen eines Produkts zu warten und zu verfolgen, verhält es sich jedoch geringfügig anders. Hier sind einige der Unterschiede und Ähnlichkeiten:

- **Es gibt keine Versionsgruppe.**

    Obwohl das Gruppenkonzept für Größe, Farbe und Stil (Farbgruppe, Größengruppe und Stilgruppe) existiert, gibt es kein Versionsgruppenkonzept. Mit Gruppen können Sie die zutreffenden Werte vordefinieren, sodass das Produkt alle Farben in dieser Farbgruppe verwenden kann, wenn Sie beispielsweise einem Produkt eine Farbgruppe zuweisen. Dieses Konzept gilt nicht für die Versionsdimension, da die Versionen, die ein Produkt verwendet, beim Erstellen des Produkts nicht vordefiniert sind. Stattdessen werden Versionen während des Lebenszyklus des Produkts nach Bedarf erstellt. Wenn Form, Passform und Funktion des Produkts gleich bleiben, erstellen Sie in der Regel eine neue Version anstelle eines neuen Produkts.

- **Vorschläge für Produktvarianten funktionieren wie derzeit.**

    Vorschläge für Produktvarianten erstellen Vorschläge für alle Versionsdimensionswerte, genau wie für andere Dimensionen. Das Erstellen und Freigeben Produkte mit Versionsangabe erfolgt genauso wie bei Produkten, die andere Dimensionen verwenden. Wenn Sie ein Produkt mit Versionsangabe erstellen, wird die erste Version (V1) als Produktdimension erstellt und die Varianten werden freigegeben. Der neue Versionswert (V2) wird hinzugefügt und die erforderlichen Varianten werden freigegeben, wenn sich das Produkt ändert und eine neue Version benötigt wird. Es ist nicht zu erwarten, dass alle Versionen (V1, V2 und V3) im Voraus für das Produkt erstellt werden.

> [!IMPORTANT]
> Wenn Sie die Dimension „Version“ aktivieren und verwenden, funktionieren einige Lösungen, die auf die Lagerungsdimensionen verweisen, möglicherweise nicht wie erwartet. Wenden Sie sich an den unabhängigen Softwareanbieter (ISV), um diese Probleme zu bestätigen und zu beheben. Weitere Informationen finden Sie unter [Die Dimension „Version“ aktivieren](#enable-version-dim).
