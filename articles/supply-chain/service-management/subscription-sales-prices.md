---
title: Dauerauftragsverkaufspreise
description: Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular Verkaufspreisdauerauftrag erstellten Verkaufspreiseinstellungen ab.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35f4e3f3bdbdad7a48b89bad7da96d221f09bdb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974211"
---
# <a name="subscription-sales-prices"></a>Dauerauftragsverkaufspreise   

[!include [banner](../includes/banner.md)]


Beim Erstellen eines Dauerauftrags leitet sich der Verkaufspreis von den im Formular **Verkaufspreisdauerauftrag** erstellten Verkaufspreiseinstellungen ab.

Im Formular **Verkaufspreisdauerauftrag** können sowohl Verkaufspreise für einen bestimmten Dauerauftrag als auch Verkaufspreise erstellt werden, die eine flexiblere Anwendung ermöglichen. Damit ein Verkaufspreis auf einen Dauerauftrag angewendet werden kann, müssen der Periodencode sowie die Währung des Dauerauftrags mit dem Periodencode und der Währung des Verkaufspreises identisch sein.

Bei identischem Periodencode und identischer Währung für Dauerauftrag und Verkaufspreis werden die Verkaufspreise des Dauerauftrags auf Basis der in der folgenden Tabelle aufgeführten Prioritäten ausgewählt. Ein leeres Feld wird in der Tabelle durch eine leere Zelle dargestellt, und ein "X" steht für einen Wert, der dem Wert im Dauerauftragsformular entspricht, in dem die Buchung generiert wird.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Priorität </p></th>
<th><p><strong>Kategorie</strong></p></th>
<th><p><strong>Projektkennung</strong></p></th>
<th><p><strong>Dauerauftrag</strong></p></th>
<th><p><strong>Verkaufswährung</strong></p></th>
<th><p><strong>Periodencode</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>


Beim Erstellen einer Dauerauftragsgebühr wird der Verkaufspreis mit der höchsten Genauigkeit (gemäß obiger Tabelle) als Verkaufspreis für den Dauerauftrag ausgewählt.

## <a name="update-and-index-subscription-sales-prices"></a>Aktualisieren und Indizieren von Dauerauftragsverkaufspreisen

Aktualisieren Sie zum Aktualisieren des Verkaufspreises für den Dauerauftrag den Basispreis oder den Index. Die Aktualisierung kann prozentual oder durch Angabe eines neues Werts vorgenommen werden.

## <a name="subscription-fee-sales-prices"></a>Verkaufspreise für Dauerauftragsgebühren

Beim Erstellen einer Dauerauftragsgebühr basiert der Verkaufspreis auf den Verkaufspreiseinstellungen des Dauerauftrags. Sie können entweder den Basispreis aus den Preiseinstellungen des Dauerauftrags verwenden oder indizierte Verkaufspreise erstellen.

## <a name="example"></a>Beispiel

Sie möchten für das neue Projekt "9030" Dauerauftragsverkaufspreise in Höhe von EUR 500 einrichten. Im Formular **Verkaufspreisdauerauftrag** erstellen Sie eine Verkaufspreisposition für den Dauerauftrag, wie dies in der folgenden Tabelle angegeben ist.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Gültig ab</p></th>
<th><p>Kategorie</p></th>
<th><p>Projekt</p></th>
<th><p>Dauerauftrag</p></th>
<th><p>Periodencode</p></th>
<th><p>Verkaufswährung</p></th>
<th><p>Verkaufspreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Monat</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Beachten Sie, dass die Felder **Kategorie** und **Dauerauftrag** leer sind.

Anschließend werden die folgenden Daueraufträge erstellt.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Servicedauerauftrag</p></th>
<th><p>Projekt</p></th>
<th><p>Dauerauftragsgruppe</p></th>
<th><p>Kategorie</p></th>
<th><p>Währung</p></th>
<th><p>Periodencode</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Unter1</p></td>
<td><p>UnterKat1</p></td>
<td><p>EUR</p></td>
<td><p>Monatlich</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Unter1</p></td>
<td><p>UnterKat2</p></td>
<td><p>EUR</p></td>
<td><p>Monatlich</p></td>
</tr>
</tbody>
</table>


Im nächsten Schritt werden die Dauerauftragsgebühren für die beiden Daueraufträge der Gruppe "Unter1" erstellt:

1.  Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.

2.  In der **Dauerauftragsgruppen** im Formular und klicken im Formular **Funktion** \> **Dauerauftragsgebühr erstellen**.

3.  In der **Dauerauftragsgebühr erstellen** Formular geben Sie die entsprechenden Informationen ein. Weitere Informationen finden Sie unter [Dauerauftragsgebühren-Buchungen erstellen](create-subscription-fee-transactions.md).

Für beide Daueraufträge werden Dauerauftragsgebühren mit einem Verkaufspreis von EUR 500 erstellt. Dies ist in der folgenden Tabelle dargestellt.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Projektdatum</p></th>
<th><p>Servicedauerauftrag</p></th>
<th><p>Projekt</p></th>
<th><p>Kategorie</p></th>
<th><p>Startdatum</p></th>
<th><p>Enddatum</p></th>
<th><p>Verkaufswährung</p></th>
<th><p>Verkaufspreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>UnterKat1</p></td>
<td><p>01.01.2007</p></td>
<td><p>31.03.2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.08.2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>UnterKat2</p></td>
<td><p>01.01.2007</p></td>
<td><p>31.03.2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Später entschließen Sie sich zum Angeben von Verkaufspreisen für die Kategorie "UnterKat1" des Projekts "9030". Zu diesem Zweck erstellen Sie für die Kombination aus Projekt "9030" und Gebührenkategorie "UnterKat1" eine neue Verkaufspreisposition mit einem Verkaufspreis von EUR 550. Für das Projekt "9030" sind nun zwei Verkaufspreispositionen für Daueraufträge vorhanden. Dies ist in der folgenden Tabelle dargestellt.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Gültig ab</p></th>
<th><p>Kategorie</p></th>
<th><p>Projekt</p></th>
<th><p>Dauerauftrag</p></th>
<th><p>Periodencode</p></th>
<th><p>Währung</p></th>
<th><p>Verkaufspreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.08.2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Monat</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28.08.2007</p></td>
<td><p>UnterKat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Monat</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


Sie wiederholen das oben beschriebene Verfahren und erstellen Dauerauftragsgebühren für beide Daueraufträge der Dauerauftragsgruppe "Unter1". In der folgenden Tabelle sind die Buchungen aufgeführt, die für die einzelnen Daueraufträge erstellt werden, die der Dauerauftragsgruppe zugeordnet sind.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Projektdatum</p></th>
<th><p>Dauerauftrag</p></th>
<th><p>Projekt</p></th>
<th><p>Kategorie</p></th>
<th><p>Startdatum</p></th>
<th><p>Enddatum</p></th>
<th><p>Verkaufswährung</p></th>
<th><p>Verkaufspreis</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28.07.2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>UnterKat1</p></td>
<td><p>01.01.2008</p></td>
<td><p>31.03.2008</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28.07.2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>UnterKat2</p></td>
<td><p>01.01.2008</p></td>
<td><p>31.03.2008</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


In der ersten Buchung für den Dauerauftrag 00020\_135 wird der Verkaufspreis in Höhe von EUR 550 von dem Dauerauftragsverkaufspreis abgeleitet, der für die Kombination aus diesem speziellen Projekt und der Kategorie festgelegt ist. In der zweiten Buchung für den Dauerauftrag 00021\_135 wird als Verkaufspreis für den Projektdauerauftrag der Betrag EUR 500 verwendet, da für die Kombination aus dem Projekt "9030" und der Kategorie "UnterKat2" kein Preis eingerichtet wurde.

## <a name="see-also"></a>Siehe auch

[Aktualisieren und Indizieren von Dauerauftrag-Verkaufspreisen](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]