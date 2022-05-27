---
title: Antizipieren von Daueraufträgen
description: Mithilfe von Servicedaueraufträgen werden Umsatzerlöse ab dem Datum, an dem eine Gebührenbuchung fakturiert wurde, manuell abgegrenzt.
author: sorenva
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ff184b24a264e37613b2302a3d92b74e870c5ac
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677337"
---
# <a name="accruing-subscriptions"></a>Antizipieren von Daueraufträgen 

[!include [banner](../includes/banner.md)]


Mithilfe von Servicedaueraufträgen werden Umsatzerlöse ab dem Datum, an dem eine Gebührenbuchung fakturiert wurde, manuell abgegrenzt.

Abgrenzungsperioden werden für die Rechnungsperiode erstellt, die für die Dauerauftragsgebühr eingerichtet wurde, und basieren auf dem Periodencode des Dauerauftrags.

Antizipierter Umsatzerlös kann abgegrenzt oder zurückgesetzt werden.

## <a name="reverse-accruals-of-credit-amounts"></a>Zurücksetzen von Abgrenzungen von Habenbeträgen

Bei einer Gutschrift bereits fakturierter Dauerauftragsbeträge stehen Ihnen drei verschiedene Methoden zur Verfügung, um die Abgrenzungsbeträge zurückzusetzen:

  - Die antizipierten Umsatzerlösbuchungen können vor dem Erstellen des Gutschriftvorschlags einzeln für die Buchung zurückgesetzt werden. Dies ist die manuelle Methode. (manuell)

  - Sie können die abgegrenzten Beträge an dem Datum, an dem die Gutschrift gebucht wird, oder am ursprünglichen Buchungsdatum der Abgrenzung zurücksetzen.

Weitere Informationen finden Sie unter [Formular "Dauerauftragsparameter"](/dynamicsax-2012//subscription-parameters-form).

## <a name="setup-requirements"></a>Einrichtungsanforderungen

Vergewissern Sie sich zum Antizipieren von Umsatzerlös, dass die folgenden Bedingungen erfüllt sind:

## <a name="account-setup"></a>Kontoeinstellungen

Die Konten **WIP - Dauerauftrag** und **Antizipierter Umsatz - Dauerauftrag** müssen im Modul **Projekt** eingerichtet sein.

Beim Buchen von antizipiertem Umsatzerlös wird das Konto **WIP - Dauerauftrag** mit dem Abgrenzungsbetrag belastet, und dem Konto **Antizipierter Umsatz - Dauerauftrag** wird der Abgrenzungsbetrag gutgeschrieben.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Einrichten von Konten für die Abgrenzung von Dauerauftragsumsatz

1.  Klicken Sie auf **Projektverwaltung und -buchhaltung** \> **Einrichten** \> **Buchung** \> **Sachkontobuchungseinstellungen**.

2.  Klicken Sie auf die Registerkarte **Umsatzerlöskonten**, und wählen Sie **WIP - Dauerauftrag** oder **Antizipierter Umsatz - Dauerauftrag**, um die Konten einzurichten.

## <a name="subscription-group-setup"></a>Einrichten der Dauerauftragsgruppe

Damit Umsatzerlöse für Daueraufträge abgegrenzt werden können, muss das Kontrollkästchen **Umsatz antizipieren** aktiviert werden. Es befindet sich im Formular **Dauerauftragsgruppen** für die Gruppe, die dem Dauerauftrag zugeordnet ist. Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Aktivieren der Abgrenzung von Umsatzerlösen für eine Dauerauftragsgruppe

Klicken Sie auf **Servicemanagement** \> **Einrichtung** \> **Daueraufträge** \> **Dauerauftragsgruppen**.

## <a name="periods"></a>Perioden

Ein Code für den Rechnungsstellungszeitraum muss eingerichtet werden. Sofern der Umsatzerlös nicht innerhalb der gleichen Zeiträume antizipiert werden soll, die auch für die Rechnungsstellung verwendet werden, muss zudem eine Abgrenzungsperiode eingerichtet werden.

Die folgenden Tabellen bieten einen Überblick über die Abgrenzungsperioden, die für die einzelnen Rechnungsstellungszeiträume eingerichtet werden können:

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Rechnungsstellungszeitraum</p></th>
<th><p>Abgrenzungsperiode</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Jahre</strong></p></td>
<td><ul>
<li><p><strong>Jahre</strong></p></li>
<li><p><strong>Quartal</strong></p></li>
<li><p><strong>Monat</strong></p></li>
<li><p><strong>Tag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Quartal</strong></p></td>
<td><ul>
<li><p><strong>Quartal</strong></p></li>
<li><p><strong>Monat</strong></p></li>
<li><p><strong>Tag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Monat</strong></p></td>
<td><ul>
<li><p><strong>Monat</strong></p></li>
<li><p><strong>Tag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Woche</strong></p></td>
<td><ul>
<li><p><strong>Tag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Tag</strong></p></td>
<td><ul>
<li><p><strong>Tag</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Die Einrichtung des Rechnungsstellungszeitraums ist ein obligatorischer Teil der allgemeinen Dauerauftrags-Gruppeneinstellungen. Sie können entscheiden, ob auch eine Abgrenzungsperiode für die Dauerauftragsgruppe eingerichtet werden soll. Wenn Sie eine Abgrenzungsperiode für die Dauerauftragsgruppe einrichten, wird diese Periode im Feld **Periodencode** vorgeschlagen. Das Feld befindet sich im Formular **Abgrenzen des Dauerauftragsumsatzerlöses**, wenn der Umsatzerlös für den Dauerauftrag abgegrenzt wird. Allerdings handelt es sich bei der Abgrenzungsperiode um optionale Informationen zur Dauerauftragsgruppe.


> [!NOTE]
> <P>Verwenden Sie den folgenden Pfad, um das Formular <STRONG>Dauerauftragsumsatz antizipieren</STRONG> zu öffnen. Klicken Sie auf <STRONG>Servicemanagement</STRONG> &gt; <STRONG>Periodisch</STRONG> &gt; <STRONG>Daueraufträge</STRONG> &gt; <STRONG>Dauerauftragsumsatz antizipieren</STRONG>.</P>


## <a name="transactions"></a>Buchungen

Sie können die Anzahl der Sachkontobuchungen bestimmen, die beim Buchen des abgegrenzten Umsatzerlöses erstellt werden. Definieren Sie für Daueraufträge, ob die Sachkontobuchungen als Summe oder pro Position erstellt werden.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Angeben der anzuzeigenden Menge an Buchungsdetails bei abgegrenzten Buchungen

1.  Klicken Sie auf **Projektverwaltung und Buchhaltung** \> **Setup** \> **Projektverwaltungs- und Buchhaltungsparameter**.

2.  Wählen Sie auf der **Registerkarte** im Feld **Rechnung** entweder **Gesamt** oder **Position** aus.


## <a name="see-also"></a>Siehe auch

[Dauerauftragsumsatz antizipieren](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]