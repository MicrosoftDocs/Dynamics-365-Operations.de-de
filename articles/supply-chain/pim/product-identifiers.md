---
title: Produktbezeichner
description: Dieses Thema enthält Informationen zu den unterschiedlichen Arten von Produktbezeichnern und erläutert, wie Sie Produktbezeichner in Ihren Produktdaten hinzufügen können.
author: cvocph
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 1e706e184f0bdf3a44e69640a85a15d9cd3d0fb2ae097d6605a9a401d6da9051
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746962"
---
# <a name="product-identifiers"></a>Produktbezeichner

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zu den unterschiedlichen Arten von Produktbezeichnern und erläutert, wie Sie Produktbezeichner in Ihren Produktdaten hinzufügen können.

Wenn Sie mit Produkten in der Produktion (BDE) oder in einem Lagerort in Microsoft Dynamics ERP oder Microsoft Dynamics CRM arbeiten, müssen Sie eine gute Strategie für die Identifizierung dieser Produkte und Produktvarianten haben.

## <a name="unique-product-numberproduct-id"></a>Eindeutige Produktnummer/Produkt-ID

In Dynamics 365 Supply Chain Management der primäre Bezeichner für ein Produkt ist die Produktnummer (d.h. die eindeutige Produkt-ID). Diese Nummer kann automatisch durch einen Nummernkreis generiert werden, oder manuell einem Produkt zugeordnet werden. Für Produktvarianten können die Zahlen durch die Produktnomenklaturvorlage definiert werden.

In vielen Fällen wird die Produktnummer ursprünglich nicht in Dynamics 365 Supply Chain Management erstellt. Stattdessen ist es mit einem Produkt in einem Produktlebenszyklussystem (PLM) oder einem  Produktdatenverwaltungssystem (PDM) zugeordnet. In diesem Fall können Sie Datenentitäten verwenden, um die Produkte und Produktvarianten zu importieren. Supply Chain Management verwendet dann die Zahlen in allen Arbeitsgängen.

Wenn Sie Supply Chain Management implementieren, sollten Sie Ihrer Strategie für Produktnummern besondere Aufmerksamkeit widmen. Ein Zahlensystem gutes verbessert Logistikflüsse und hilft verhindern Fehler. Eine gute Produktkennung ist maximal 15 Zeichen lang. Idealerweise hat diese weniger als 10 Zeichen und schließt nicht mehr als klassifizierende fünf Zeichen ein. Sie können auch Suchnamen verwenden, um Schnellsuchen zu ermöglichen. Ein Suchname ist ein zusätzlicher Name, der die Klassifizierungen eines Produkts darstellt.

Wenn Sie Microsoft Dataverse verwenden, ist die Produktnummer in Supply Chain Management auch die Produktnummer in Microsoft Dataverse. Produktvarianten werden mit Dataverse als eindeutig identifizierbare Produkte synchronisiert.

## <a name="item-number-and-product-dimensions"></a>Artikel- und Produktdimensionen

Die Artikelnummer ist de Produktbezeichner, die von einer bestimmten juristischen Person verwendet wird. Idealerweise sollte die Artikelnummer und die Produktnummer identisch sein. Wenn die Bezeichnungen pro juristische Person sich unterscheidet, wird es schwierig, dem Produkt durch die Lieferkette des Imports zu folgen und es ist mühsam, neue Prozesse neu zu bezeichnen und darauf zu verweisen. Zur Kontabilität mit früheren Versionen (das heißt mit Microsoft Dynamics AX 2009 und davor), haben wir dieses Modell bewahrt. Es wird jedoch empfohlen, dass Sie Kennungen entfernen, die für juristische Personen spezifisch sind, wenn Sie können, und dass Sie die eindeutigen Produktnummer als primäre Kennung verwenden.

Darüber hinaus kann eine Produktvariante nicht durch eine Artikelnummer eindeutig identifiziert werden. Sie erfordert immer die Kombination einer Artikelnummer und Produktdimensionen, die alle im Produktmaster definiert werden. Diese Anforderung kann lästig werden und kann die Identifizierungsprozesse verlangsamen. Aus diesem Grund wird auch empfohlen, dass Sie die eindeutigen Produktnummer statt der Artikelnummer verwenden, wenn dies möglich ist.

Viele Seiten haben weiterhin die Artikelnummer und Produktdimensionen als die primären Kennungen. Allerdings kann die Produktnummern für Suchen verwendet werden. Bei **Vertrieb und Marketing** &gt; **Einstellungen** &gt; **Suchen** &gt; **Suchparameter** öffnen, können Sie die Suche ändern, sodass sie Produktnummern anstelle der Artikelnummern als primäre Suchstrategie verwendet. Wenn Sie " **Aktivieren für Produktsuchsuche** auf die Option **Ja** festlegen, zeigt die Suche nicht nur die Produktmaster Produktvarianten an. Weitere Informationen finden Sie unter[Nach Produkten und Produktvarianten bei der Auftragserfassung suchen](search-products-product-variants.md).

Darüber hinaus sind Sie in der Lage, auf der Produktnummer, den Produktnamen sowie die Beschreibung und die Kennungen der Produktdimension Produktvariante zu finden und zu filtern. Wenn Sie eine Variante auswählen, werden die zugehörige Artikelnummer und alle Produktdimensions-IDs ausgewählt. Daher können Sie leichter die richtige Variante finden und auswählen. Diese Einstellung wird ausdrücklich empfohlen, wenn Sie Produktvarianten und die eindeutige Produktnummer als primäre Bezeichner für Produkte verwenden. Die einzige Ausnahme ist möglicherweise die Modebranche, in der es bei Geschäftsprozessen oft erforderlich ist, dass der Master vor der Auswahl einer Variante ausgewählt wird. Sie sollten diese Option sorgfältig auswerten, bevor Sie das Nummerierungssystem implementieren.

> [!NOTE]
> Die Artikelnummer für ein Produkt kann nicht geändert werden, sobald eine oder mehrere Transaktionen für dieses Produkt vorhanden sind.

## <a name="product-name-and-description"></a>Geben Sie einen Namen und eine Beschreibung ein

Der Produktname und -beschreibung sind die visuell lesbaren Bezeichner eines Produkts und können in vielen Sprachen verwaltet werden. Standardmäßig werden in Supply Chain Management alle Produktinformationen in der Standardunternehmensprache, nicht in der Sprache des Benutzers angezeigt. Allerdings werden übersetzte Produktnamen und Beschreibungen in der Kommunikation mit Debitoren und Kreditoren verwendet. Die Übersetzungen basieren auf dem Sprachcode der Debitoren- und Kreditorenkonten.

Für Produktvarianten können die Produktnamen durch die Produktnomenklaturvorlage definiert werden. Da es nicht erforderlich ist, das Produktnamen eindeutig sind, stellen Sie möglicherweise fest, dass mehrere Produkte, die denselben Namen haben.

## <a name="product-and-item-search-names"></a>Produkt- und Artikelsuchenamen

Supply Chain Management und bietet sekundären Arbeitsgänge einen Suchbegriff für Produkte sowie für Artikel anzeigen (freigegebene Produkte). Dieser Suchname muss nicht eindeutig sein, und er kann geändert werden, nachdem ein Produkt oder eine Produktvariante erstellt wurde. Es wird empfohlen, dass Sie den Suchnamen verwenden, um Produkte nach Kategorien zu suchen. Die Suchnamen ermöglichen Schnellsuchen, insbesondere in Verkaufs- und Einkaufsprozessen.

Der Suchname kann auch eine Debitoren- oder Kreditorenprodukt-ID oder irgendeine andere externe Produkt-ID enthalten, wenn diese externe ID das primäre Suchkriterium für ein Produkt ist.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Externe Produktkennungen (Debitoren- und Kreditorenkennungen)

Für freigegebene Produkte können Sie die Artikelnummern, die Artikelbeschreibungen und die Artikelnamen verwalten, die der Debitor oder Kreditor verwendet. Die Verweise werden auf externen Dokumenten angezeigt, wie Aufträgen, Bestellungen, Lieferscheinen und Rechnungen. In der aktuellen Version der erhaltenen Supply Chain Management werden die externen Verweise nicht auf Kernarbeitsgangsseiten angezeigt. Die einzige Ausnahme ist die Kreditorenartikelnummer. Diese Nummer wird im Dialogfeld **Produktinformationen** angezeigt, wenn ein Standardkreditor für das freigegebene Produkt definiert wird.

Sie können die externen Produktkennungen nach freigegebenem Produkt, freigegebener Produktvariante, Kunde, Kundengruppe, Lieferant oder Lieferantengruppe pflegen.

**Freigegebene Produkte** Auf der Seite führen Sie die folgenden Schritte aus.

- Klicken Sie im Aktivitätsbereich auf der Registerkarte **Einkauf** in der Gruppe **Zugehörige Informationen** auf **Externe Artikelbeschreibung**.
- Für Verkäufer klicken Sie im Aktivitätsbereich auf der Registerkarte **Einkauf** in der Gruppe **Zugehörige Informationen** auf **Externe Artikelbeschreibung**.

Auf der Seite **Externe Artikelbeschreibungen** können Sie die Artikelnummer des Debitors oder Kreditors einem freigegebenen Produkt zuordnen. Diese Zuordnung muss für jede juristische Person ausgeführt werden. Die folgenden Informationen können erfasst werden. Leider sind die Bezeichnungen in der aktuellen Version von Supply Chain Management etwas irreführend. Allerdings können dieser Beschriftungen in einer künftigen Version geändert werden.

| Feld | Einschließlich Debitoreninformationen | Entsprechende Kreditoreninformationen |
|-------|------------------------------------|----------------------------------|
| Externe Artikelnummer | Die Artikelnummer des Debitoren | Die Artikelnummer des Kreditors |
| Beschreibung | Der Name, den der Debitor dem Artikel zuordnet | Der Name, den der Kreditor dem Artikel zuordnet |
| Externer Artikeltext | Die Beschreibung des Artikels des Debitors | Die Artikelbeschreibung des Kreditors |

Wenn viele Kunden oder Lieferanten dieselben Artikelnummern verwenden (wie z.B. bei einer Einkaufsgemeinschaft oder einer Commerce-Gruppe), können Sie Gruppen von Kunden oder Lieferanten erstellen, um die Pflege der externen Produktkennungen zu vereinfachen.

- Für Debitorengruppen &gt; gehen Sie zu **Verkäufe** **Einstellungen** &gt; **Artikel** &gt; **Externe Artikelbeschreibung**, die Gruppen und die zugehörigen Artikelnummern erstellen und verwalten. Um Kunden einer Gruppe zuzuordnen, wechseln Sie zu **Debitoren** &gt; **Kunden** &gt; **Alle Kunden**, und geben Sie dann im Inforegister **Standardwerte für Aufträge** einen Wert im Feld **Artikel – Kundengruppe** ein.
- Für Debitorengruppen  gehen Sie zu **Einkauf und Bereitstellung**&gt;**Einrichtung**&gt;**Externe Artikelbeschreibungsgruppe**, um die Gruppen der betreffenden Artikelnummern zu erstellen und verwalten. Um Kreditoren einer Gruppe zuzuordnen, wechseln Sie zu **Kreditorenkonten** &gt; **Kreditoren** &gt; **Alle Kreditoren**, und geben Sie dann im Inforegister **Standardwerte für Bestellungen** einen Wert im Feld **Artikel – Kreditorengruppe** ein.
 
## <a name="bar-codes"></a>Strichcodes

Wenn Sie ein Strichcodescanner verwenden möchten, um Produkte zu ermitteln, muss die Produktkennung die Bedingungen des Strichcodestandards erfüllen, der verwendet wird. Daher enthalten Strichcodes in der Regel nicht die unformatierte Produktnummer, sonder eine Nummer, die speziell für die ausgewählte Strichcodetechnologie generiert ist. Sie können mehrere Strichcodes nach Strichcodetyp verwalten. Sie können sogar dieselben Strichcode mehreren Produkten zuordnen und dann die tatsächliche aktive Zuordnung auswählen, wenn Sie einen Strichcode scannen.

Bevor Sie Strichcodes definieren, können Sie ein oder mehrere Strichcode-Einstellungen definieren. Mithilfe der Strichcodeeinstellungen kann überprüft werden, dass Strichcodes den erforderlichen Richtlinien entsprechen und dass sie daher effektiv gedruckt und gescannt werden können. Sie können auch besondere Strichcodes für bestimmte Produktmengen verwalten.

Es wird empfohlen, dass Sie die Strichcodeeinstellungen verwenden, um die Codes der Global Trade Item Number (GTIN) oder der Internationalen Artikelnummer (EAN) zu verwalten.

Um Strichcodes auf der Seite **Freigegebene Produkte** auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** zu verwalten, wählen Sie **Strichcodes** aus.

## <a name="gtin-codes"></a>GTIN-Codes

Im E-Commerce ist es wichtig, dass alle Parteien eine gemeinsame Sprache finden und auf Produkte verweisen, indem ein gemeinsamer Satz an Bezeichner verwendet wird. Daher verlassen sich einige Branchen auf die [GTIN](https://www.gs1.org/id-keys/gtin), was ein globales Artikelnummernsystem ist, das von GS1 zur Verfügung gestellt wird.

Es wird empfohlen, die GTIN als Strichcode zu behalten. Allerdings können Sie dies auch auf der Seite **Artikel - GTIN** warten. Um diese Seite auf der Seite **Freigegebene Produkte** auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** zu öffnen, wählen Sie **GTIN-Codes** aus. Die GTIN wird nicht als globale Nummer gepflegt. Stattdessen erfolgt die Verwaltung nach juristischen Personen.

In Supply Chain Management definieren Sie in den Verpackungsvarianten Lagerortarbeitsgänge mithilfe bestimmter Maßeinheiten. Beispielsweise könnte ein Artikel in Artikeln, in die Bündelungen von sechs, in Ablagen oder vollständigen Paletten gelagert werden. Eine bestimmte Maßeinheit wird für jede dieser Verpackungsvarianten definiert. Da die GTIN in der Regel der Verpackungseinheit eines Produkts zugeordnet wird, können Sie auf der Seite **Artikel - GTIN** mehrere GTIN-Codes pro Produkt und pro Maßeinheit verwalten. Allerdings kann der gleiche GTIN-Code nicht mehrmals für unterschiedliche Artikel oder Produktvarianten einer juristischen Person verwendet werden.

Um **GTIN-Codes** auf der Seite **Freigegebene Produkte** auf der Registerkarte **Lagerbestand verwalten** in der Gruppe **Lagerort** zu verwalten, wählen Sie **GTIN** aus.

## <a name="external-codes"></a>Externe Codes

Externe Codes können für viele Entitäten definiert werden. Beispielsweise können Sie externe Codes definieren, um Produkte und freigegebene Produkte zu identifizieren. Diese externen Codes können verwendet werden, um statistische Codes oder Steuercodes mit freigegebenen Produkten und freigegebenen Produktvarianten zuzuordnen. Externe Codes werden nach juristischer Person und Codetyp definiert. Sie müssen in Bezug auf juristische Person, Codetyp und Tabellenverweis eindeutig sein.

Leider gibt es keine Standardfunktionalität, mit der Sie nach Produkten per externer Codes suchen können.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Datenentitäten, die verwendet werden, um Produktkennungen zu importieren und exportieren

| Entitätsname | Import-Bezeichner | Export-Bezeichner | Kommentare |
|-------------|--------------------|--------------------|----------|
| Produkte V2  | Produktnummer, Produktsuchename, Produktname, Produktbeschreibung | Produktnummer, Produktsuchename, Produktname, Produktbeschreibung | Je nach den Einstellungen der Entität und des Nummernkreises für die Produktnummer, kann die Produktnummer zum Zeitpunkt des Importvorgangs automatisch erstellt werden. |
| Produktvarianten | Produktnummer, Produktsuchename, Produktname, Produktbeschreibung | Produktnummer, Produktsuchename, Produktname, Produktbeschreibung | Abhängig von der Produktnomenklaturvorlage kann die Produktnummer zum Zeitpunkt des Importvorgangs automatisch erstellt werden. Sie können jedoch eine beliebige eindeutige Produktnummer importieren und diese Produktnummer muss der Struktur der Produktnomenklaturvorlagen nicht folgen. |
| Produktübersetzungen | Produktname, Produktbeschreibung | Produktname, Produktbeschreibung | Diese Entität überschreibt jede beliebige Sprache. Wenn der Name oder die Beschreibung der primären Sprache einer juristischen Entität überschrieben wird, wird der Name und die Beschreibung des Produkts selbst geändert. |
| Erstellung eines freigegebenen Produkts V2 | Artikelnummer, Artikelsuchename Produktnummer| Artikelnummer, Artikelsuchename Produktnummer, Produktsuchename, Produktname | Die Entität kann eine Herausforderung sein, wenn Nummernkreise während der Erstellung neuer freigegebener Produkte verwendet werden. **Artikelnummer** Nummernsequenzen und **Produktnummer** Nummernsequenzen haben einen Einfluss. Allerdings ist der Nummernkreis **Artikelnummer** pro juristische Person, für die **Produktnummer** Nummernkreis global. Es wird daher nicht empfohlen, dass Sie den Nummernkreis **Artikelnummer** verwenden, wenn Sie neue freigegebene Produkte bereitstellen. Offensichtlich, wenn die Entität verwendet wird, um ein vorhandenes Produkt freizugeben, muss die Produktnummer in der Entität zugeordnet werden. Weitere Informationen finden Sie im Abschnitt "Produkte- und Artikelnummernsequenzen" in diesem Thema. |
| Freigegebene Produktvarianten | Artikelnummer, Produktdimensionen, Produktnummer | Produktnummer, Produktsuchename, Produktname, Produktbeschreibung, Produktdimensionen | Wie **Produktvarianten**-Entität kann diese Entität verwendet werden, um neue Produkte zu erstellen, die entweder der Produktnomenklaturvorlage folgen oder eigene Produktnummern für die Variante verwenden. |
| Externe Artikelbeschreibungen für Debitoren | Debitoren-Artikelnummer, Debitorenartikelname, Debitorenbeschreibung, Debitorenkonto | Debitoren-Artikelnummer, Debitorenartikelname, Debitorenbeschreibung, Debitorenkonto | Eine Gruppe von Debitoren (beispielsweise Gesamtlayout, eine Käufervereinigung) kann in eine Gruppe zusammengefasst werden, indem die **Debitorengruppen der externen Artikelbeschreibung** verwendet. |
| Externe Artikelbeschreibungen für Kreditoren | Kreditorenartikelnummer, Kreditorenartikelname, Kreditorenbeschreibung, Kreditorenkonto | Kreditorenartikelnummer, Kreditorenartikelname, Kreditorenbeschreibung, Kreditorenkonto | Eine Gruppe von Debitoren (beispielsweise Gesamtlayout, eine Käufervereinigung) kann in eine Gruppe zusammengefasst werden, indem die **Debitorengruppen der externen Artikelbeschreibung** verwendet. |
| Artikel-Strichcode | Strichcode | Strichcode | Zum Zeitpunkt des Imports müssen Sie auf ein Barcode-Setup verweisen, das im Zielsystem definiert ist. Die importierten Barcode-Referenzen werden anhand dieses Barcode-Setups validiert und zurückgewiesen, wenn die Barcodes nicht mit den in diesem Setup definierten Anforderungen übereinstimmen. |
| Externe Codes für freigegebene Produkte | Externer Code | Externer Code, externe Codeklassen, Artikelnummer | Externe Codes sind nach juristischer Person. Für den Import müssen Sie eine definierte Codeklasse beziehen. Importieren Sie die Codeklassen, indem Sie die **Externe Codeklasse für freigegebene Produkte** verwenden. |
| Externe Codes für freigegebene Produktvarianten | Externer Code | Externer Code, externe Codeklassen, Artikelnummer, Produktdimensionen | Externe Codes sind nach juristischer Person. Für den Import müssen Sie eine definierte Codeklasse beziehen. Importieren Sie die Codeklassen, indem Sie die **Externe Codeklasse für freigegebene Produkte** verwenden. Diese Entität verweist auf Produktvarianten durch die Artikelnummer und Produktdimensionen. |
| Externe Codes für freigegebene Produktvarianten nach Produktnummerbezeichner | Externer Code | Externer Code, externe Codeklassen, Produktnummer | Externe Codes sind nach juristischer Person. Für den Import müssen Sie eine definierte Codeklasse beziehen. Importieren Sie die Codeklassen, indem Sie die **Externe Codeklasse für freigegebene Produkte** verwenden. Diese Entität verweist auf Produktvarianten durch die Produktnummer der Varianten. (Vom nächsten wichtigen Update) |
| GTIN | Nicht zutreffend | Nicht zutreffend | Es gibt zurzeit keine bestimmte Einheit, die verwendet wird, um GTIN-Codes zu exportieren oder importieren. Es wird empfohlen, dass Sie stattdessen die Entität **Artikelstrichcode** verwenden. |
| Datendienst-Kennungsentität der Entitätsbezeichner | Nicht zutreffend | Artikelnummer, Artikelsuchename, Produktsuchename, Artikelnummer des Kreditoren, Debitoren-Artikelnummer, externe Codes, GTIN-Codes, Strichcodes | Diese Entität konsolidiert alle Bezeichner in ein einziges Datenmodell, sodass eine Schnittstelle verwendet werden kann, um alle Bezeichner und ihre zugehörigen Typen zu exportieren. Verwenden Sie die Entität **Produktentitätsbezeichner-Code**, um die Bezeichnercodes und -beschreibungen zu exportieren. Verwenden Sie die Entität **Produktentitätsbezeichner-Umfang**, um zusätzliche Umfangsinformationen zu einem Bezeichner zu exportieren, wie beispielsweise die Partei, juristische Person, Menge oder Einheit. |

### <a name="product-and-item-number-sequences"></a>Artikel- und Produktdimensionen

Sie können zwei unterschiedliche Nummernkreise festlegen.

- Der Nummernkreis **Produktnummer** für die globale Produktnummer
- Der Nummernkreis **Artikelnummer** für die Artikelnummer pro juristische Person

> [!NOTE]
> Sie sollten die Artikelnummer nur als separaten Bezeichner verwenden, wenn Sie unterschiedliche juristische Personen aus verschiedenen Quellen migrieren, die verschiedene Nummerierungssysteme hatten. Sie sollten immer versuchen, einen Produktbezeichner zu verwenden, der für alle juristischen Personen eindeutig ist. Daher sollten Sie die Option **Manuell** auf **Ja** für den Nummernkreis **Artikelnummer** festlegen. Auf diese Weise folgt die Produktnummer der Artikelnummer bei der Erstellung. Wenn Supply Chain Management nicht das führende System für neue Produktnummern ist, sollten Sie die Option **Manuell** auf **Ja** für **Artikelnummer** und **Produktnummer** Nummernkreise festlegen.

Wenn Sie die Entität **Freigegebene Produkterstellung V2** verwenden, um Produkte zu erstellen, können mehrere Einstellungen sich darauf auswirken, wie die Nummernkreise verwendet werden, um die Produktnummer und Artikelnummer zu erstellen:

- Einstellungen des Nummernkreises **Produktnummer**
- Einstellungen des Nummernkreises **Artikelnummer**
- Die Zuordnung der Artikelnummer 
- Die Zuordnung der Produktnummer

Die folgende Tabelle bietet eine Übersicht über die Ergebnisse des Imports und der manuellen Erstellung bei bestimmten Kombinationen der Nummernkreis- und Feldzuordnungseinstellungen.

| Produktnummernkreis Nummersequenz | Artikelnummerennummernkreis | Modellnummer des Artikels zuordnen | Die Zuordnung der Produktnummer | Ergebnis des Entitätsimports | Ergebnis der manuellen Erstellung | Abschluss |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Manuell = Null | Manuell = Null | Keine Zuordnung | Keine Zuordnung | Produktnummern verwenden den Nummernkreis. **Produktnummer** Artikelnummern verwenden den Nummernkreis. **Artikelnummer** | Produktnummern verwenden den Nummernkreis. **Produktnummer** Artikelnummern verwenden den Nummernkreis. **Artikelnummer** | Bei dieser Konfiguration folgen die Produktnummern der Produktnummernfolge und die Artikelnummern der Artikelnummernfolge. Diese Konfiguration funktioniert jedoch nicht, wenn mehr als ein Element (Zeile) importiert werden soll. |
| Manuell = Null | Handbuch = Ja | Automatisch generieren | Keine Zuordnung | Artikelnummern verwenden Produktnummern und **Artikelnummer** den Nummernkreis. | Artikelnummern verwenden Produktnummern und **Produktnummern** den Nummernkreis. | Artikelnummern und Produktnummern folgen dem Produktnummernkreis. Dies ist der empfohlene Ansatz zum Importieren von Massenprodukten mit der Datenentität „Freigegebene Produkterstellung V2“.<br><br>Sie können diesen Ansatz nur verwenden, wenn Sie Artikel in großen Mengen importieren (mehrere Zeilen) und wenn Sie Artikel nicht über die Benutzeroberfläche erstellen. Wenn Sie sowohl den Bulk-Import als auch das Erstellen von Artikeln über die Benutzeroberfläche benötigen, verwenden Sie stattdessen die Vorgehensweise in der nächsten Zeile dieser Tabelle. Um von der Vorgehensweise beim Massenimport zur Verwendung der Benutzeroberfläche für den manuellen Import und das Erstellen von Produkten zu wechseln, müssen Sie die **Nächste Nummer** in der Sequenz der Artikelnummern manuell anpassen, damit sie mit der **Nächsten Nummer** in der Sequenz der Produktnummern übereinstimmt. Dann könnten Sie zu dem Ansatz in der nächsten Zeile dieser Tabelle wechseln. |
| Manuell = Null | Handbuch = Ja | Keine Zuordnung | Keine Zuordnung | Artikelnummern verwenden Produktnummern und **Produktnummern** den Nummernkreis. | Artikelnummern verwenden Produktnummern und **Produktnummern** den Nummernkreis. | Artikelnummern und Produktnummern verwenden den Produktnummernkreis. Diese Konfiguration funktioniert jedoch nicht, wenn mehr als ein Element (Zeile) importiert werden soll.<br><br>Sie müssen diesen Ansatz verwenden, wenn Sie sowohl Produkte über die Entitäten importieren (es kann immer nur eine Zeile importiert werden) als auch Produkte über die Benutzeroberfläche erstellen wollen. |
| Handbuch = Ja | Nicht zutreffend | Nicht zutreffend | Automatisch generieren | Sie erhalten die folgende Fehlermeldung: „Nummernkreis kann nicht erkannt werden.” | Einstellungen des Nummernkreises **Artikelnummer** | Diese Einstellung wird für den Import nicht unterstützt. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Produktentitätskennung (Export aller Produktkennungen)

Das Produktentitätsbezeichner-Modell wurde erstellt, damit für Version 1.0 von Dataverse alle Bezeichner bereitgestellt werden können, die verwendet werden, um auf ein Produkt zu verweisen. Um diese Aufgabe zu vereinfachen, werden alle Bezeichner in einer globalen Bezeichnertabelle zusammengefasst, damit sie als ein Modell exportiert werden können. Beachten Sie, dass diese Version von Dataverse nicht das Produktbezeichnermodell verwendet. Deshalb haben die Entität **Common Data Service-Bezeichnerentität der Produktentität** und dieser Prozess begrenzten praktischen Nutzen, und es ist wahrscheinlich, dass daran in Zukunft Änderungen vorgenommen werden.

Die Produktbezeichnertabelle ist eine globale Tabelle, die aus allen Bezugstabellen in der juristischen Hauptperson durch einen periodischen Batchauftrag aufgefüllt wird. Sie müssen eine juristische Person und eine Produktkategoriehierarchie als die Definition des globalen Produktmasterumfangs auswählen. Die Generierung der globalen Produktkennungstabelle wird auf Produkten beschränkt, die der ausgewählten juristischen Person und Produkten freigegeben werden, die Mitglieder der Produkthierarchie sind, die für die Rolle **Allgemeine Datendienst** der Hierarchie von Produktkategorie aktiviert ist.

Bei diesem Prozess wird vorausgesetzt, dass Produktmasterdaten in erster Linie in einer zentralen juristischen Personen verwaltet werden. (Jedoch, kann diese Person eine juristische virtuelle juristische Person sein, die verwendet wird, um globale Masterdaten zu verwalten.)

Gehen Sie folgendermaßen vor, um die Umgebung zu konfigurieren:

1. Wählen Sie die Kategoriehierarchie für Dataverse aus. Wählen Sie auf der Seite **Kategoriehierarchierolle Zuordnung** wenn keine Hierarchie der Rolle zugeordnet ist, **Allgemeiner Datendienst** aus. Sie müssen eine neue Zuordnung erstellen. Wählen Sie die Rolle **Common Data Service** aus und ordnen Sie dann die Kategoriehierarchie zu, die die Produktpalette darstellt, die mit Dataverse synchronisiert werden soll.
2. Wählen Sie die juristische Person für globale Produktmasterdaten aus. Auf der Seite **Parameter für Verwaltung von Produktinformationen** auf der Registerkarte **Produktattribute**, wählen Sie das Vorlagenunternehmen aus, in dem die Produkt- und hauptsächlich Artikelkennungen nicht verwaltet werden.
3. Definieren Sie die Kennungscodetypen und - codes, die exportiert werden sollen. Gehen Sie zu **Produktinformationsverwaltung** &gt; **Einstellungen** &gt; **Produktkennungscodes**. Um die Bezeichnercodetypen zu generieren, wählen Sie **Codes generieren** aus. Ein Codetypeintrag wird für jeden Typ zu Identifikationszwecken generiert, die in der ausgewählten juristischen Person befindet.

    Für Barcodes wird für jedes Einrichten eines Barcodes ein Codetyp generiert. Für externe Codes wird ein externer Codetyp für jede Codeklasse generiert.

    Sie können jetzt die Liste von Codetypen verwalten. Sie können Code, Name und Beschreibung ändern. Sie können auch Codetypen löschen. Codetypen, die Sie löschen, können nicht verwendet werden, um die globalen Produktentitätskennungstabellen aufzufüllen.

4. Wenn Sie mit dem Definieren der Produktbezeichner-Codetypen fertig sind, können Sie die Bezeichner in der globalen Tabelle erstellen, indem Sie den Einzelvorgang **Produktentitätsbezeichner erstellen** auf der Seite **Produktentitätsbezeichner-Codes** starten. Sie sollten diesen Einzelvorgang in einer Charge ausführen. Dieser Einzelvorgang sollte als regelmäßiger Batchauftrag eingerichtet werden, sodass die Tabelle entsprechend neuer Einträge aufgefüllt wird.

Sie können jetzt die Datenentitäten **Common Data Service-Bezeichnerentität der Produktentität**, **Produktentitätsbezeichner-Code** und **Produktentitätsbezeichner-Umfang** verwenden, um die Bezeichner für jedes beliebige Zielsystem zu exportieren.

## <a name="related-topic"></a>Verwandtes Thema

[Nach Produkten und Produktvarianten bei der Auftragserfassung suchen](search-products-product-variants.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
