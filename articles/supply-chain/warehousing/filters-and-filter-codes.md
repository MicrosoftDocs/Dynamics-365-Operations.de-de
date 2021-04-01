---
title: Produktfilter für Lagertransaktionen konfigurieren
description: In diesem Thema wird beschrieben, wie Produktfilter und Filtercodes konfiguriert werden, um Lagerartikel in einem Lagerort in Kategorien einzuteilen. Sie können Filter auch verwenden, um anzugeben, welche Debitoren einen bestimmten Artikel bestellen können und welche Artikel von einem bestimmten Kreditor erworben werden können.
author: Mirzaab
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSFilters,WHSFilterGroupTable,EcoResProductDetailsExtended,WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: dbf92c5e199ecadb3e4f7c6130427d449ef5b6c8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251768"
---
# <a name="configure-product-filters-for-warehouse-transactions"></a>Produktfilter für Lagertransaktionen konfigurieren

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie Produktfilter und Filtercodes konfiguriert werden, um Lagerartikel in einem Lagerort in Kategorien einzuteilen. Sie können Filter auch verwenden, um anzugeben, welche Debitoren einen bestimmten Artikel bestellen können und welche Artikel von einem bestimmten Kreditor erworben werden können.

Darüber hinaus können Sie Produktfilter einrichten und verwenden, um Lagerartikel in einem Lagerort automatisch zu organisieren und gefilterte Artikel in Filtergruppen zusammenzufassen. Filter können verwendet werden, um Artikel in Kategorien für Handhabungs-, Kauf- und Verkaufsprozesse einzuteilen. Möglicherweise möchten Sie Artikel gruppieren oder voneinander trennen, wenn die Art und Weise, wie sie behandelt werden, auf Gewicht oder Handhabungsbeschränkungen basiert. Sie können auch angeben, bei welchen Kunden oder Lieferanten ein Artikel gekauft oder verkauft werden kann.

## <a name="prerequisites"></a>Voraussetzungen

In der folgenden Tabelle werden die Voraussetzungen angezeigt, die vorhanden sein müssen, bevor Sie beginnen können.

| Voraussetzung | Anweisungen |
|---|---|
| Bevor Sie beginnen, Produkte auf der Seite **Details für freigegebene Produkte** zu konfigurieren, müssen Sie die Lagerverarbeitung für die Speicherdimensionsgruppe des Produkts aktivieren. | Gehen Sie zu **Produktinformationsverwaltung \> Setup \> Dimensions- und Variantengruppen \> Speicherdimensionsgruppen**, und wählen oder erstellen Sie eine Speicherdimensionsgruppe, in der die Option **Lagerverwaltungsprozesse verwenden** auf *Ja* gesetzt ist. |
| Wenn Sie Kundenfilter und/oder Lieferantenfilter verwenden, müssen Sie deren Verwendung in den Lagerverwaltungsparametern aktivieren. | Wechseln Sie zu **Lagerortverwaltung \> Einstellungen \> Lagerortverwaltungsparameter**. Auf der Registerkarte **Produktfilter** setzen Sie die Option **Debitorenfilter aktivieren** und/oder **Kreditorenfilter aktivieren** auf *Ja*. |

## <a name="set-up-product-filters"></a>Produktfilter einrichten

Produktfilter bieten bis zu 10 Merkmalen von **Filtertiteln**, bei denen es sich um Aufzählungswerte handelt. Diese Aufzählungswerte stehen beim Erstellen eines Produktfilters zur Auswahl. Die Aufzählungswerte *Code 1* bis *Code 10* sind systemdefiniert und repräsentieren ein bestimmtes Merkmal oder Attribut eines Artikels. Beispielsweise kann *Code 1* Artikel darstellen, die eine Gefahrstoffklassifizierung haben. *Code 2* kann Artikel darstellen, die nur Lieferanten kaufen können. Produktfilter definieren dann den spezifischen **Filtercode**-Wert, der mit einem **Filtertitel**-Wert verknüpft ist.

1. Gehen Sie zu **Lagerortverwaltung \> Setup \> Produktfilter \> Produktfilter**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Produktfilter zum Raster hinzuzufügen.
1. Wählen Sie im Feld **Filtertitel** einen Wert aus.
1. Geben Sie im Feld **Filtercode** einen Wert ein.

    ![Einrichten eines Produktfilters](media/Product_Filters10.png "Einrichten eines Produktfilters")

1. Geben Sie im Feld **Beschreibung** einen Namen für den Code ein. Beispielsweise könnte *Code 2* Kreditoren darstellen. Anschließend können Sie einen Produktfilter für einen bestimmten Kreditor oder eine bestimmte Gruppe von Kreditoren erstellen. Weitere Informationen finden Sie im Abschnitt [Einrichten von Kreditorenfiltercodes](#vendor-product-filters) weiter unten in diesem Thema.

    ![Produktfilter einrichten](media/Product_Filters.png "Produktfilter einrichten")

## <a name="set-up-product-filter-groups"></a>Produktfiltergruppen einrichten

Sie können Filtergruppen verwenden, um Filtercodes zu gruppieren. Dies ist hilfreich, wenn eine Gruppe in einer Abfrage in einer Lagerplatzdirektive verwendet wird und Sie nach der Gruppe anstelle von einer Reihe von Codes suchen möchten. Jede Filtergruppe wird einer Artikelgruppe zugeordnet.

> [!IMPORTANT]
> Nicht alle Produktfiltergruppen sind für Filtercodes verfügbar, die höher als sind *Code 4* (also *Code 5* bis *Code 10*). Beispielsweise wird bei freigegebenen Produkten die Gruppierung der Filtercodes nicht aktualisiert, obwohl alle Produktfiltercodes hinzugefügt werden. Dieses Verhalten wird möglicherweise in späteren Versionen aktualisiert.

Gehen Sie zum Einrichten von Filtergruppen folgendermaßen vor.

1. Gehen Sie zu **Lagerortverwaltung \> Setup \> Produktfilter \> Produktfiltergruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Geben Sie in die Felder **Gruppe 1** und **Gruppe 2** die Namen ein, die verwendet werden, um Artikel zu kategorisieren.
1. Wählen Sie auf dem Inforegister **Details** die Option **Neu** aus, um eine Position hinzuzufügen.
1. Geben Sie in die Felder **Startdatum/-uhrzeit** und **Enddatum/-uhrzeit** Start- und Enddatum für die Filtergruppe ein.
1. In dem Feld **Artikelgruppe** wählen Sie die Artikelgruppe aus, auf die der Produktfilter angewendet werden soll.
1. In den Feldern **Code 1** bis **Code 10** Wählen Sie die Filtercodes aus, die nach Bedarf in die Gruppe aufgenommen werden sollen.

    ![Artikelgruppe](media/ProdFilterGroup.png "Artikelgruppe")

> [!NOTE]
> Wenn Sie eine Fehlermeldung erhalten, wenn Sie die Seite schließen, fehlt möglicherweise eine Codeeinstellung. Auf der Seite **Artikelgruppen** können Sie die Codes für eine Artikelgruppe obligatorisch machen, indem Sie die Kontrollkästchen **Filtercode 1 für Artikelgruppe zuweisen**, **Filtercode 2 für Artikelgruppe zuweisen** usw. aktivieren.

## <a name="set-up-filter-codes-on-item-groups"></a>Einrichten von Filtercodes für Artikelgruppen

Wenn Sie Filtercodes für eine Artikelgruppe eingerichtet haben, können Sie die Codes erstellen, die für Produkte in der Artikelgruppe erforderlich sind.

Um Filtercodes für Artikelgruppen einzurichten, führen Sie folgende Schritte aus.

1. Gehen Sie zu **Lagerverwaltung \> Setup \> Bestand \> Artikelgruppen**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um eine Artikelgruppe zu erstellen.
1. Geben Sie im Feld **Artikelgruppe** einen Namen ein.
1. Geben Sie im Feld **Name** eine Beschreibung ein.
1. Aktivieren Sie im Inforegister **Lagerort** unter **Filter erforderlich** die Kontrollkästchen für die Filtercodes, die für Produkte angegeben werden müssen, die der Artikelgruppe zugeordnet sind.

    Um ein freigegebenes Produkt zu aktualisieren, öffnen Sie dessen Seite **Details für freigegebene Produkte**, und wählen Sie dann im Aktionsbereich die Option **Bearbeiten** aus. Die Filter, die den Codes zugeordnet sind, werden dann im Inforegister **Lagerort** verfügbar.

    ![Artikelgruppen](media/ItemGroup10.png "Artikelgruppen")

1. In dem Abschnitt **Artikelgruppenfilter** aktivieren Sie die Kontrollkästchen für die Filter, die übereinstimmen müssen, damit die Filtergruppe die Standardfiltergruppe für einen Artikel ist.

    Wenn beispielsweise die Kontrollkästchen **Filtercode 1 verwenden** und **Filtercode 2 verwenden** aktiviert werden, dann müssen Filtercode 1 und 2 des Artikels mit den Einstellungen der Filtergruppe für die Artikelgruppe übereinstimmen, bevor die Filtergruppe ausgewählt werden kann. Wenn Sie einen neuen Artikel erstellen, ist die ausgewählte Filtergruppe die Standardfiltergruppe in den Feldern **Gruppe 1** und **Gruppe 2** des Inforegisters **Lagerort** auf der Seite **Details für freigegebene Produkte**.

> [!IMPORTANT]
> Produktfiltercodes sind nur für Artikel aktiviert, die eine erweiterte Lagerortverwaltung verwenden.

## <a name="specify-filter-codes-for-released-products"></a>Angeben von Filtercodes für freigegebene Produkte

Um Filtercodes für freigegebene Produkte anzugeben, führen Sie folgende Schritte aus. Sie können beispielsweise Filtercodes verwenden, um gefährliche Produkte zu gruppieren, die bestimmte Kreditoren kaufen.

1. Wechseln Sie zu **Produktinformationsverwaltung \> Produkte \> Freigegebene Produkte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um ein Produkt zu erstellen.
1. In dem Dialogfeld **Neues freigegebenes Produkt** geben Sie die Daten ein, die zum Erstellen der Basis eines neuen Produkts erforderlich sind, und wählen Sie dann **OK** aus.

    Produktfiltercodes sind nur aktiviert, wenn die an das Produkt angehängte Artikelgruppe für Filtercodes konfiguriert wurde.

    Weitere Informationen finden Sie unter [Ein neues Produkt erstellen](../pim/tasks/create-new-product.md).

1. Auf dem Inforegister **Lagerort** unter **Produktfiltercodes** wählen Sie Filtercodes für die Felder **Code 1** bis **Code 10** nach Bedarf aus, um Filtercodes für das Produkt anzugeben.

## <a name="set-up-generally-available-items"></a>Einrichten von allgemein verfügbaren Artikeln

Sie können bestimmte Lagerartikel nur für Debitoren oder Kreditoren oder für Debitoren und Kreditoren bereitstellen.

> [!NOTE]
> Für jeden Artikel, den Sie als allgemeinen verfügbar einrichten, gelten Debitorenfilter und Kreditorenfilter nicht.

Zum Einrichten allgemein verfügbarer Artikel führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Lagerortverwaltung \> Setup \> Produktfilter \> Allgemein verfügbare Produkte**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus, um einen Datensatz zu erstellen.
1. In dem Feld **Debitor oder Kreditor** den Eintrag *Debitor*, *Kreditor* oder *Alle* aus, um die Artikel für Debitoren, Kreditoren oder beide verfügbar zu machen.
1. Geben Sie im Feld **Startdatum/-uhrzeit** das Datum und die Uhrzeit ein, zu der der Artikel verfügbar sein wird.
1. Wählen Sie im Feld **Artikelgruppe** die Artikelgruppe aus.
1. Wählen Sie in den Feldern **Code 1** bis **Code 10** die Filtercodes aus, um die Artikel zu beschränken, die allgemein verfügbar sind.

    Wenn Sie eine Artikelgruppe auswählen, legen Sie diese Gruppe an Artikeln als allgemein verfügbar fest. Durch das Auswählen von Filtercodes in diesen Feldern beschränken Sie die Artikel, die verfügbar sind.

## <a name="set-up-customer-product-filters"></a>Produktfilter für Debitoren einrichten

Sie können diese optionale Prozedur verwenden, um Artikel anzugeben, die für einen Debitor zusätzlich zu den Artikeln verfügbar sein sollen, die über die Filtereinstellung auf der Seite **Allgemein verfügbare Artikel** bereitgestellt werden. Sie können mehrere Filter für einen einzelnen Debitor einrichten.

Gehen Sie zum Einrichten von Debitorenfiltercodes folgendermaßen vor.

1. Wechseln Sie zu **Vertrieb und Marketing \> Debitoren \> Alle Debitoren**.
1. Wählen Sie einen Debitor aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Debitor** in der Gruppe **Einrichten** auf **Produktfilter**.
1. Wählen Sie auf der Seite **Produktfiltercodes** im Aktivitätsbereich **Neu** aus.
1. Geben Sie in die Felder **Startdatum/-uhrzeit** und **Enddatum/-uhrzeit** Start- und Enddatum für die ausgewählte Artikelgruppe ein.
1. Wählen Sie im Feld **Artikelgruppe** die Artikelgruppe aus.
1. Wählen Sie in den Feldern **Code 1** bis **Code 10** die Filtercodes aus, die als Kriterien verwendet werden sollen, um die Artikel einzuschränken, die für Debitoren in der ausgewählten Artikelgruppe verfügbar sind. Sie müssen für jeden Filtercode, der für die Artikelgruppe eingerichtet ist, eine Auswahl treffen.

## <a name="set-up-vendor-product-filters"></a><a name="vendor-product-filters"></a>Produktfilter für Kreditoren einrichten

Sie können diese optionale Prozedur verwenden, um Artikel anzugeben, die für einen Kreditor zusätzlich zu den Artikeln verfügbar sein sollen, die über die Filtereinstellung auf der Seite **Allgemein verfügbare Artikel** bereitgestellt werden. Sie können mehrere Filter für einen einzelnen Kreditor einrichten.

Gehen Sie zum Einrichten von Kreditorenfiltercodes folgendermaßen vor.

1. Gehen Sie zu **Beschaffung \> Kreditoren \> Alle Kreditoren**.
1. Wählen Sie einen Kreditor aus.
1. Klicken Sie im Aktivitätsbereich auf der Registerkarte **Kreditor** in der Gruppe **Einrichten** auf **Produktfilter**.
1. Wählen Sie auf der Seite **Filtercodes** im Aktivitätsbereich **Neu** aus.
1. Geben Sie in die Felder **Startdatum/-uhrzeit** und **Enddatum/-uhrzeit** Start- und Enddatum für die ausgewählte Artikelgruppe ein.
1. Wählen Sie im Feld **Artikelgruppe** die Artikelgruppe aus.
1. Wählen Sie in den Feldern **Code 1** bis **Code 10** die Filtercodes aus, die als Kriterien verwendet werden sollen, um die Artikel einzuschränken, die für Kreditoren in der ausgewählten Artikelgruppe verfügbar sind. Sie müssen für jeden Filtercode, der für die Artikelgruppe eingerichtet ist, eine Auswahl treffen.

> [!NOTE]
> Die Einrichtung von Kreditorenproduktfiltern gilt für freigegebene Produkte, bei denen Lagerverwaltungsprozesse für die zugehörige Speicherdimensionsgruppe aktiviert sind. Die Filtercodes werden verwendet, um zu bestimmen, ob das System es Benutzern ermöglicht, einen bestimmten Artikel von einem bestimmten Kreditoren zu kaufen, wenn sie Bestellpositionen erstellen. Microsoft Dynamics 365 Supply Chain Management bietet Methoden für die Handhabung der Kreditorengenehmigung. Wenn ein oder mehrere freigegebene Produkte vorhanden sind, bei denen das Feld **Überprüfung genehmigter Kreditoren** auf *Nur Warnung* oder *Nicht erlaubt* gesetzt ist, können beide Kreditorengenehmigungsmethoden für diese Artikel aktiviert werden. Diese Situation kann Probleme verursachen, wenn Benutzer Bestellpositionen erstellen.

## <a name="see-also"></a>Siehe auch

[Weitere Informationen finden Sie im Blogbeitrag zu Filtercodes für WMS-aktivierte Lagerorte](http://blog.dynamics-for-operations.com/2017/09/26/wms-warehouse-filter-codes/)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]