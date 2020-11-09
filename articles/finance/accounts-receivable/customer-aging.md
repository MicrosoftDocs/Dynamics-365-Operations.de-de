---
title: Debitorenfälligkeitsbericht
description: Im Debitorenfälligkeitsbericht werden die von Debitoren fälligen Salden sortiert nach Datumsintervall oder Zahlungsfrist angezeigt.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: e43aef72b7d65db1dcb014dfada5233ac051ba7c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2020
ms.locfileid: "4013052"
---
# <a name="customer-aging-report"></a>Debitorenfälligkeitsbericht 

Im **Debitorenfälligkeitsbericht** werden die von Debitoren fälligen Salden sortiert nach Datumsintervall oder Zahlungsfrist angezeigt.

Wenn dieser Bericht generiert wird, werden die folgenden Standardparameter angezeigt. Sie können mithilfe der Parameter die Daten filtern, die im Bericht angezeigt werden. Weitere Informationen finden Sie unter [Einrichten von Auflistungen](set-up-collections.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Feld</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Abrechnungsklassifizierung</strong></p></td>
<td><p>Wählen Sie die in den Bericht einzuschließenden Abrechnungsklassifizierungen aus.</p>
<div class="alert">

**Hinweis:** Dieses Steuerelement ist nur verfügbar, wenn der Konfigurationsschlüssel <STRONG>Öffentlicher Sektor</STRONG> ausgewählt wurde.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Transaktionen ohne Abrechnungsklassifizierung einbeziehen</strong></p></td>
<td><p>Wenn dieses Kontrollkästchen aktiviert ist, werden alle Buchungen ohne zugewiesene Abrechnungsklassifizierungen im Bericht angezeigt.</p>
<div class="alert">

**Hinweis:** Dieses Steuerelement ist nur verfügbar, wenn der Konfigurationsschlüssel <STRONG>Öffentlicher Sektor</STRONG> ausgewählt wurde.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Fälligkeit per</strong></p></td>
<td><p>Geben Sie das Datum ein, das für den aktuellen Fälligkeitsbereich verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Saldo per</strong></p></td>
<td><p>Geben Sie das Datum ein, für das die Debitorensalden angezeigt werden sollen. Dies wird auch als Abschnittsdatum für Buchungen bezeichnet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Startdatum</strong></p></td>
<td><p>Geben Sie ein Datum ein, das im ersten Periodenintervall oder in der Zahlungsfrist liegt und in den Bericht einbezogen werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Kriterien</strong></p></td>
<td><p>Wählen Sie den Datumstyp aus, auf dem der Bericht basieren soll.</p>
<ul>
<li><p><strong>Buchungsdatum</strong> – Das Buchungsdatum der ausgewählten Buchungen. Dies kann z. B. ein Rechnungsdatum sein, das die Grundlage für die Berechnung des Fälligkeitsdatums ist.</p></li>
<li><p><strong>Fälligkeitsdatum</strong> – Das Fälligkeitsdatum der Buchungen, basierend auf den Zahlungsbedingungen.</p></li>
<li><p><strong>Dokumentdatum</strong> – Ein benutzerdefiniertes Dokumentdatum, das die Grundlage für die Berechnung des Fälligkeitsdatums bildet.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Zahlungsfristdefinition</strong></p></td>
<td><p>Wählen Sie eine Zahlungsfristdefinition aus. Das Feld <strong>Intervall</strong> wird bei Auswahl einer Zahlungsfristdefinition nicht verwendet.</p>
<p>Zahlungsfristdefinitionen mit mehr als sechs Zahlungsfristen können im gedruckten Bericht nicht verwendet werden.</p>
<div class="alert">

**Hinweis:** Sie können Zahlungsfristen auf der Seite <STRONG>Zahlungsfristdefinitionen</STRONG> einrichten.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Beschreibung der Zahlungsfrist drucken</strong></p></td>
<td><p>Wählen Sie <strong>Ja</strong> aus, um Zahlungsfristbeschreibungen im Bericht am Anfang jeder Zahlungsfristspalte einzuschließen. Wählen Sie <strong>Nein</strong> aus, um den Bericht ohne Spaltenüberschriften zu drucken.</p></td>
</tr>
<tr class="even">
<td><p><strong>Intervall</strong></p></td>
<td><p>Definieren Sie die zu verwendende Periode durch Eingeben der Anzahl der Tages- oder Monatseinheiten in jeder Periode. Wenn beispielsweise Zahlungsfristinformationen nach Woche angezeigt werden sollen, geben Sie in dieses Feld den Wert 7 ein, und wählen Sie im Feld <strong>Tag/Monat</strong> den Eintrag <strong>Tag</strong> aus.</p>
<div class="alert">

**Hinweis:** Die in diesem Feld eingegebenen Informationen werden nur verwendet, falls keine Zahlungsfristdefinition ausgewählt wurde. Andernfalls wird die Druckrichtung in der Zahlungsfristdefinition definiert.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Tag/Monat</strong></p></td>
<td><p>Wählen Sie die Einheit aus (entweder <strong>Tag</strong> oder <strong>Monat</strong>), mit der die Periode im Feld <strong>Intervall</strong> definiert wird.</p></td>
</tr>
<tr class="even">
<td><p><strong>Druckrichtung</strong></p></td>
<td><p>Wählen Sie aus, ob die Berechnung der Salden und das Drucken des Fälligkeitsberichts für vergangene oder zukünftige Perioden erfolgen soll. Die Datumsangaben werden relativ zum im Feld <strong>Saldo per</strong> ausgewählten Datum ausgewertet. Wählen Sie <strong>Rückwärts</strong> aus, um Informationen zu vergangenen Perioden anzuzeigen. Wählen Sie <strong>Vorwärts</strong> aus, um Informationen zu zukünftigen Perioden anzuzeigen.</p>
<div class="alert">
  
<STRONG>Hinweis:</STRONG> Die in diesem Feld eingegebenen Informationen werden nur verwendet, falls keine Zahlungsfristdefinition ausgewählt wurde.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Detaildaten</strong></p></td>
<td><p>Aktivieren Sie dieses Kontrollkästchen, um die Buchungen aufzulisten, die in den im Bericht angezeigten Salden enthalten sind.</p></td>
</tr>
<tr class="even">
<td><p><strong>Beträge in Buchungswährung einbeziehen</strong></p></td>
<td><p>Aktivieren Sie dieses Kontrollkästchen, um zusätzlich zu Beträgen in der Buchhaltungswährung Beträge in der Buchungswährung einzubeziehen. Wenn dieses Kontrollkästchen nicht aktiviert ist, werden die Beträge im Bericht nur in der Buchhaltungswährung angezeigt.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Negativer Saldo</strong></p></td>
<td><p>Aktivieren Sie dieses Kontrollkästchen, um Debitorenkonten mit negativen Salden einzubeziehen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Konten mit Nullsaldo ausschließen</strong></p></td>
<td><p>Aktivieren Sie dieses Kontrollkästchen, um Debitorenkonten mit Nullsaldo auszuschließen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Zahlungspositionierung</strong></p></td>
<td><p>Aktivieren Sie dieses Kontrollkästchen, um nicht ausgeglichene Zahlungen anzuzeigen. Diese werden in der ersten Spalte des Berichts angezeigt.</p></td>
</tr>
</tbody>
</table>

