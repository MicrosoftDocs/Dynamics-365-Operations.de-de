---
title: Umsatzsteuererklärung für Deutschland
description: Dieses Thema enthält Informationen zum Generieren von QR-Rechnungen (QR-Slips) und zum Verarbeiten eingehender QR-Rechnungen.
author: v-lurodi
manager: AnnBe
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Germany
ms.author: v-lenest
ms.search.validFrom: 2019-06-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 089178474c44ce4efa3c74a4183e2a80b68d9303
ms.sourcegitcommit: baab88d037ebf26e6c8822d96056e5ee475877aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "3369575"
---
# <a name="vat-declaration-for-germany"></a>Umsatzsteuererklärung für Deutschland

[!include [banner](../includes/banner.md)]


In diesem Thema wird erläutert, wie Sie die Mehrwertsteuererklärung für juristische Personen in Deutschland einrichten und erstellen.

Weitere Informationen zur Einrichtung der Mehrwertsteuererklärung finden Sie unter [MwSt-Berichterstattung für Europa](emea-vat-reporting.md).

## <a name="set-up-sales-tax-reporting-codes-for-vat-reporting"></a>Mehrwertsteuer-Codes für Mehrwertsteuererklärung einrichten

Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuer-Erklärungscodes einrichten](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md) befolgen. Die folgende Tabelle enthält ein Beispiel für Umsatzsteuer-Berichtscodes für Deutschland.

<table width="614">
<thead>
<tr>
<td width="75">
<p><strong>Code</strong></p>
</td>
<td width="340">
<p><strong>Beschreibung</strong></p>
</td>
<td width="95">
<p><strong>Element in der XML-Datei der Umsatzsteuererklärung</strong></p>
</td>
<td width="104">
<p><strong>Steuerbemessungsgrundlage oder Steuerbetrag</strong></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td colspan="4" width="614">
<p><strong>Steuerfreier Verkauf mit Vorsteuerabzug für innergemeinschaftliche Lieferungen (&sect;4, Nr. 1b des UStG [Umsatzsteuergesetz</strong><strong> oder </strong><strong>Mehrwertsteuergesetz])</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>41</p>
</td>
<td width="340">
<p>Innergemeinschaftlicher Versand (&sect;4, Nr. 1b des UStG) für Kunden mit Steuerregistrierung.</p>
</td>
<td width="95">
<p>Kz41</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>44</p>
</td>
<td width="340">
<p>Innergemeinschaftliche Lieferungen von Neufahrzeugen an Kunden ohne Umsatzsteuer-Identifikationsnummer.</p>
</td>
<td width="95">
<p>Kz44</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>49</p>
</td>
<td width="340">
<p>Innergemeinschaftliche Lieferungen von Neufahrzeugen außerhalb eines Unternehmens.</p>
</td>
<td width="95">
<p>Kz49</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>43</p>
</td>
<td width="340">
<p>Zusätzliche steuerfreie Verkäufe mit Vorsteuerabzug (z. B. Exporte).</p>
</td>
<td width="95">
<p>Kz43</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><strong>Steuerfreie Verkäufe ohne Vorsteuerabzug (z. B. Verkäufe nach &sect;4, Nr. 8 bis 28 des UStG)</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>48</p>
</td>
<td width="340">
<p>Steuerfreier Verkauf ohne Vorsteuerabzug.</p>
</td>
<td width="95">
<p>Kz48</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><strong>Steuerpflichtiger Umsatz</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>81</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</p>
</td>
<td width="95">
<p>Kz81</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>181</p>
</td>
<td width="340">
<p>Steuerbetrag für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</p>
</td>
<td width="95">
<p>Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>86</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</p>
</td>
<td width="95">
<p>Kz86</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>186</p>
</td>
<td width="340">
<p>Steuerbetrag für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</p>
</td>
<td width="95">
<p>Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>35</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für Lieferungen oder Leistungen zu anderen Steuersätzen.</p>
</td>
<td width="95">
<p>Kz35</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>36</p>
</td>
<td width="340">
<p>Steuerbetrag für Lieferungen oder Leistungen zu anderen Steuersätzen.</p>
</td>
<td width="95">
<p>Kz36</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>77</p>
</td>
<td width="340">
<p>Lieferungen von land- und forstwirtschaftlichen Betrieben nach &sect;24 des UStG an Kunden mit einer Umsatzsteuer-Identifikationsnummer.</p>
</td>
<td width="95">
<p>Kz77</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>76</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</p>
</td>
<td width="95">
<p>Kz76</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>80</p>
</td>
<td width="340">
<p>Steuerbetrag des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</p>
</td>
<td width="95">
<p>Kz80</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><strong>Innergemeinschaftliche Akquisitionen und Mehrwertsteuer für solche Akquisitionen</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>91</p>
</td>
<td width="340">
<p>Steuerfreie innergemeinschaftliche Akquisitionen.</p>
</td>
<td width="95">
<p>Kz91</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>89</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</p>
</td>
<td width="95">
<p>Kz89</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>189</p>
</td>
<td width="340">
<p>Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</p>
</td>
<td width="95">
<p>Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>93</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</p>
</td>
<td width="95">
<p>Kz93</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>193</p>
</td>
<td width="340">
<p>Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</p>
</td>
<td width="95">
<p>Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>95</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</p>
</td>
<td width="95">
<p>Kz95</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>98</p>
</td>
<td width="340">
<p>Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</p>
</td>
<td width="95">
<p>Kz98</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>94</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</p>
</td>
<td width="95">
<p>Kz94</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>96</p>
</td>
<td width="340">
<p>Steuerbetrag für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</p>
</td>
<td width="95">
<p>Kz96</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><strong>Zusätzliche Informationen zum Vertrieb</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>42</p>
</td>
<td width="340">
<p>Lieferungen des ersten Kunden für gemeinschaftsinterne Dreieckstransaktionen (&sect;25b des UStG).</p>
</td>
<td width="95">
<p>Kz42</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>60</p>
</td>
<td width="340">
<p>Steuerpflichtiger Umsatz des ausführenden Unternehmers, für den der Leistungsempfänger die Steuer schuldet, gemäß &sect;13b (5) des UStG.</p>
</td>
<td width="95">
<p>Kz60</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>21</p>
</td>
<td width="340">
<p>Sonstige nicht steuerpflichtige Dienstleistungen gemäß &sect;18b, Satz 1, Nr. 2 des UStG.</p>
</td>
<td width="95">
<p>Kz21</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>45</p>
</td>
<td width="340">
<p>Sonstige nicht steuerpflichtige Verkäufe (wenn der Erfüllungsort nicht in Deutschland liegt).</p>
</td>
<td width="95">
<p>Kz45</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><strong>Begünstigter als Steuerschuldner (&sect;13b des UStG)</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>46</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</p>
</td>
<td width="95">
<p>Kz46</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>47</p>
</td>
<td width="340">
<p>Steuerbetrag für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</p>
</td>
<td width="95">
<p>Kz47</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>73</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</p>
</td>
<td width="95">
<p>Kz73</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>74</p>
</td>
<td width="340">
<p>Steuerbetrag des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</p>
</td>
<td width="95">
<p>Kz74</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>84</p>
</td>
<td width="340">
<p>Steuerbemessungsgrundlage für andere Dienstleistungen (&sect;13b (2), Nr. 1, 2 und 4 bis 11 des UStG).</p>
</td>
<td width="95">
<p>Kz84</p>
</td>
<td width="104">
<p>Steuerbasis</p>
</td>
</tr>
<tr>
<td width="75">
<p>85</p>
</td>
<td width="340">
<p>Steuerbetrag für andere Dienstleistungen (&sect;13b (2), Nr. 1, 2 und 4 bis 11 des UStG).</p>
</td>
<td width="95">
<p>Kz85</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><strong>Abzugsfähige Vorsteuerbeträge</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>66</p>
</td>
<td width="340">
<p>Steuer auf Eingaben aus Rechnungen anderer Unternehmen (&sect;15, Absatz 1, Nr. 1 des UStG).</p>
</td>
<td width="95">
<p>Kz66</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>61</p>
</td>
<td width="340">
<p>Vorsteuerbetrag aus innergemeinschaftlichen Erwerb von Gegenständen (&sect;15, Absatz 1, Nr. 3 des UStG).</p>
</td>
<td width="95">
<p>Kz61</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>62</p>
</td>
<td width="340">
<p>Anfallender Umsatzsteuerimport(&sect;15, Absatz 1, Nr. 2 des UStG).</p>
</td>
<td width="95">
<p>Kz62</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>67</p>
</td>
<td width="340">
<p>Vorsteuerbeträge aus Dienstleistungen im Sinne von &sect;13b des UStG (&sect;15, Absatz 1, Klausel 1, Nr. 4 des UStG).</p>
</td>
<td width="95">
<p>Kz67</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>63</p>
</td>
<td width="340">
<p>Vorsteuerbeträge, die nach allgemeinen Durchschnittssätzen berechnet werden (&sect;23 und &sect;23A des UStG).</p>
</td>
<td width="95">
<p>Kz63</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>64</p>
</td>
<td width="340">
<p>Korrektur des Vorsteuerabzugs (&sect;15A des UStG).</p>
</td>
<td width="95">
<p>Kz64</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>59</p>
</td>
<td width="340">
<p>Vorsteuerabzug für innergemeinschaftliche Lieferungen neuer Fahrzeuge außerhalb eines Unternehmens (&sect;2A des UStG) und Kleinunternehmen im Sinne von &sect;19 (1) des UStG (&sect;15 (4A) des UStG).</p>
</td>
<td width="95">
<p>Kz59</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><strong>Sonstige Steuerbeträge</strong></p>
</td>
</tr>
<tr>
<td width="75">
<p>65</p>
</td>
<td width="340">
<p>Steuern aufgrund von Änderungen in der Form der Besteuerung und Nachsteuer auf besteuerte Anzahlungen usw. aufgrund von Änderungen des Steuersatzes.</p>
</td>
<td width="95">
<p>Kz65</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>69</p>
</td>
<td width="340">
<p>Steuerbeträge, die auf Rechnungen falsch oder unplausibel ausgewiesen sind (&sect;14c des UStG) sowie Steuerbeträge, die in Übereinstimmung mit &sect;6A (4), Satz 2; &sect;17 (1), Satz 6 und &sect;25b (2) des UStG <strong>geschuldet</strong> sind oder <strong>geschuldete Steuerbeträge</strong> von einem Outsourcer oder Lagerhalter gemäß &sect;13A (2) 1, Nr. 6 des UStG.</p>
</td>
<td width="95">
<p>Kz69</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>39</p>
</td>
<td width="340">
<p>Abzug der vereinbarten Sondervorauszahlung für eine langfristige Verlängerung (die in der Regel erst in der letzten Vorankündigung des Steuerzeitraums erfolgt).</p>
</td>
<td width="95">
<p>Kz39</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
<tr>
<td width="75">
<p>83</p>
</td>
<td width="340">
<p>Gesamtbetrag der Mehrwertsteuer (Mehrwertsteuer-Vorauszahlung oder Mehrwertsteuerüberschuss).</p>
<p>Bei der Umsatzsteuererklärung im XML-Format wird der Wert in diesem Feld automatisch als Summe der Berichtscodes 181, 186, 36, 80, 189, 193, 98, 96, 47, 74 und 85 abzüglich der Berichtscodes 66, 61, 62, 67, 63, 64, 59, 69 und 39 berechnet.</p>
</td>
<td width="95">
<p>Kz83</p>
</td>
<td width="104">
<p>USt.-Betrag</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>

> [!NOTE]
> Beispiele für Formen von Mehrwertsteuererklärungen, die Deklarationszeilencodes enthalten, finden Sie unter [Formulare im Mehrwertsteuerverfahren für das Jahr 2020](https://umsatzsteuer-voranmeldung-2020.taxpool.net/Umsatzsteuer-Voranmeldung-2020.pdf).

## <a name="set-up-sales-tax-codes"></a>Mehrwertsteuercodes einrichten

Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuercodes für MwSt-Berichterstattung](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) und [Mehrwertsteuerübersicht](../general-ledger/indirect-taxes-overview.md) befolgen.

> [!NOTE]
> In einer deutschen juristischen Entität sollten Umsatzsteuerkennzeichen für steuerfreie Verkäufe nach folgenden Regeln eingerichtet werden:
>
> - Der Steuersatz beträgt mehr als 0 (Null).
> - Das Steuerkennzeichen ist als **Befreit** auf der **Umsatzsteuergruppen**-Seite gekennzeichnet.

## <a name="create-a-vat-declaration-in-xml-format"></a><a name= "createvatdecxmlformat"></a>Erstellen einer Umsatzsteuererklärung im XML-Format

1. In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in der **Bibliothek der freigegebenen Anlagen** laden Sie die neuesten Versionen der Konfigurationen für die elektronische Berichterstattung (ER) für das Format der Umsatzsteuererklärung herunter:

    - **Elster (DE)**

    Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2. Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer-Erklärungscodes**.
3. Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.
4. Wechseln Sie zu **Steuer \> Erklärungen \> Mehrwertsteuer \> Mehrwertsteuer für Abrechnungszeitraum melden**.
5. Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder ein.

| **Feld**                 | **Beschreibung**                                                                                                                                                                                                                                                                         |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ausgleichsperiode         | Wählen Sie den gewünschten Berichtszeitraum aus.                                                                                                                                                                                                                                                 |
| Startdatum                 | Geben Sie das erste Datum des zu berechnenden Mehrwertsteuer-Abrechnungszeitraums an, um die Mehrwertsteuer zu berechnen. Dieser Wert entspricht dem Datum im Feld **Vom** auf der **Mehrwertsteuer-Abrechnungszeitraum**-Seite.                                                                                 |
| Buchungsdatum          | Geben Sie das Datum an, für das die Mehrwertsteuererklärung berechnet wird. Der aktuelle Wert ist das aktuelle Datum. Die Mehrwertsteuerzahlung wird für alle Buchungen berechnet, die im Abrechnungszeitraum gebucht wurden.                                                                                  |
| Mehrwertsteuer, Zahlungsversion | Wählen Sie den Mehrwertsteuer-Ausgleichstyp. Wenn diese Umsatzsteuerabrechnung die erste Umsatzsteuerabrechnung für den Zeitraum ist, wählen Sie **Original**. Wenn bereits eine Umsatzsteuerabrechnung generiert wurde, wählen Sie **Neueste Korrekturen**. Weitere Informationen finden Sie unter [Eine Mehrwertsteuerzahlung erstellen](../general-ledger/tasks/create-sales-tax-payment.md). |

6. Wählen Sie **OK**.
7. Im Dialogfeld **Deutsche Mehrwertsteuererklärung** stellen Sie die folgenden Felder ein.

| **Feld**                      | **Beschreibung**                                                                                                                                                 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektronisches Steuerdokument erstellen | Setzen Sie diese Option auf **Ja**, um ein elektronisches Dokument zu erstellen, das die Details des Berichts enthält.                                                            |
| Separat übermittelte Dokumente | Setzen Sie diese Option auf **Ja**, wenn der gedruckte Bericht nicht zusammen mit dem elektronischen Dokument eingereicht wird. In der XML-Datei sollte der Code Kz22 den Wert **1** haben. |

8. Wählen Sie **OK**. Auf der **Elektronisches Steuererklärungsprotokoll**-Seite (**Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**) wird eine neue Zeile erstellt.

![Seite „Protokoll der elektronischen Steuererklärung“](media/1_Electronic_tax_declaration_log.png)

## <a name="preview-the-xml-file"></a>Vorschau der XML-Datei

1. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**.
2. Auf der Seite **Protokoll der elektronischen Steuererklärung**, wählen Sie die **Vorschau**-Registerkarte, um eine Vorschau der gemeldeten Werte anzuzeigen.
3. Um die XML-Datei zur weiteren Übermittlung (außerhalb des Systems) zu überprüfen oder zu speichern, wählen Sie die Zeile auf der **Protokoll der elektronischen Steuererklärung**-Seite, und wählen Sie dann das Büroklammersymbol in der oberen rechten Ecke.
4. Die **Handhabung von Dokumenten**-Seite erscheint und zeigt die generierte Datei. Wählen Sie **Öffnen** oben auf der Seite, um die Datei in der Anwendung zu öffnen, die der XML-Erweiterung in Ihrem System zugeordnet ist.

## <a name="submission-the-vat-declaration-to-elster"></a>Senden Sie die Umsatzsteuererklärung an ELSTER

ELSTER (Elektronische Steuererklärung) ist ein deutsches Online-Finanzamt, das vom Bundeszentralen Finanzamt für die Online-Einreichung von Steuererklärungen konzipiert wurde.

Im [Entwicklerbereich](https://www.elster.de/elsterweb/entwickler/infoseite/download_eric_28.) auf der ELSTER-Website finden Sie Beispiele, die zeigen, wie Entwickler mit ELSTER Rich Client (ERiC) interagieren können, um Mehrwertsteuererklärungen im XML-Dateiformat einzureichen. Beispiele werden für C++, C\# und Java bereitgestellt. Um auf diesen Bereich der Website zugreifen zu können, müssen Sie [als Entwickler registriert](https://www.elster.de/elsterweb/registrierung-entwickler) sein. Ein Beispiel könnte Ihnen helfen, Ihre eigene ausführbare Datei zu erstellen, mit der Sie XML-Dateien über ERiC senden können. Um eine ausführbare Datei zum Senden von XML-Dateien an ELSTER zu verwenden, müssen Sie ERiC Dynamics Link Libraries (DLLs) herunterladen.

Weitere Informationen zu ERiC-Versionen finden Sie unter [ELSTER-Website](https://www.elster.de/elsterweb/entwickler/infoseite/eric).

## <a name="example"></a><a name="example"></a> Beispiel

Das folgende Beispiel zeigt, wie Sie Umsatzsteuerkennzeichen und Umsatzsteuerberichtscodes einrichten, Transaktionen buchen und die deutsche Umsatzsteuererklärung erstellen können.

1. Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuercodes** und richten Sie die folgenden Umsatzsteuerkennzeichen ein.

| **Mehrwertsteuercode** | **Prozentsatz** | **Beschreibung**                                                                       |
|--------------------|----------------|---------------------------------------------------------------------------------------|
| VAT19              | 19             | Inlandsverkäufe mit einer Quote von 19 Prozent.                                               |
| VAT7               | 7              | Inlandsverkäufe mit einer Quote von 7 Prozent.                                                |
| InVAT19            | 19             | Inlandseinkäufe mit einer Quote von 19 Prozent.                                           |
| InVAT7             | 7              | Inlandseinkäufe mit einer Quote von 7 Prozent.                                            |
| EU19               | 19             | EU-Einkäufe mit einer Quote von 19 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist. |
| EU7                | 7              | EU-Einkäufe mit einer Quote von 7 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist.  |
| EUS                | 19             | EU-Verkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.                               |
| THIRD              | 19             | Exportverkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.                           |

2. Auf der **Mehrwertsteuercodes**-Seite weisen Sie auf dem Inforegister **Berichtseinstellungen** den Mehrwertsteuercodes Berichtscodes zu.

Die folgende Tabelle zeigt, wie Sie die Mehrwertsteuer-Berichtscodes den Mehrwertsteuercodes zuweisen.

| **Mehrwertsteuercode** | **Steuerpflichtiger Umsatz** | **Steuerfreier Verkauf** | **Mehrwertsteuer** | **Steuerpflichtige Einkäufe** | **Vorsteuer** | **Steuerpflichtiger Import** | **Erwerbsteuer (USA)** | **Erwerbsteuerausgleich** |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| VAT19              | 81                |                   | 181                   |                       |                          |                    |             |                    |
| VAT7               | 86                |                   | 186                   |                       |                          |                    |             |                    |
| InVAT19            |                   |                   |                       |                       | 66                       |                    |             |                    |
| InVAT7             |                   |                   |                       |                       | 66                       |                    |             |                    |
| EU19               |                   |                   |                       |                       |                          | 89                 | 189         | 61                 |
| EU7                |                   |                   |                       |                       |                          | 93                 | 193         | 61                 |
| EUS                |                   | 41                |                       |                       |                          |                    |             |                    |
| THIRD              |                   | 43                |                       |                       |                          |                    |             |                    |

> [!NOTE]
> Die vorhergehende Konfiguration ist nur ein Beispiel und hängt von der Struktur der Mehrwertsteuercodes ab, die verwendet werden. Damit Werte für die Mehrwertsteuererklärung berechnet und übertragen werde, müssen Sie für jeden Steuercode, der im Mehrwertsteuerzahlungsprozess verwendet wird, einen entsprechenden Mehrwertsteuer-Erklärungscode in einem oder mehreren Feldern der Registerkarte **Berichteinstellung** festlegen.

3. Wechseln Sie zu **Steuer \> Einstellung \> Mehrwertsteuer \> Einrichtung der elektronischen Steuererklärung**.
4. Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.
5. Führen Sie die folgenden Buchungen aus. Informationen zu Kundenrechnungen finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**. Kreditorenrechnungen wechseln Sie zu **Kreditorenkonten \> Rechnungen \> Rechnungserfassung**.

| **Datum**        | **Buchungstyp**      | **Nettobetrag** | **Mehrwertsteuerbetrag** | **Mehrwertsteuercode** | **Erwartete Steuerbemessungsgrundlage – Berichtscode** | **Erwarteter Steuerbemessungsbetrag – Berichtscode** |
|-----------------|---------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| 1. Januar 2020 | Debitorenrechnung          | 100            | 19             | VAT19              | 81                                     | 181                                      |
| 1. Januar 2020 | Kreditorenrechnung (EU)       | 100            | 7              | EU7                | 93                                     | 193 – Steuerpflichtig 61 – Steuerabzug     |
| 1. Januar 2020 | Debitorenrechnung (EU)     | 100            | 0              | EUS                | 41                                     | Nicht zutreffend                           |
| 1. Januar 2020 | Debitorenrechnung (Export) | 100            | 0              | THIRD              | 43                                     | Nicht zutreffend                           |

6. Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.
7. Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.

    - **Ausgleichsperiode:** Mo
    - **Von Datum** = 1/1/2020

8. Wählen Sie **OK**.
9. Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.
10. Wählen Sie **OK**.
11. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.
12. Auf der **Protokoll der elektronischen Steuererklärung**-Seite, wählen Sie die **Allgemein**-Registerkarte und überprüfen die allgemeinen Informationen.

![Seite „Protokoll der elektronischen Steuererklärung“, Registerkarte „Allgemein“](media/2_Electronic_tax_declaration_log.png)

13. Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.

![Vorschau des Protokolls der elektronischen Steuererklärung](media/3_Electronic_tax_declaration_log.png)

14. Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.
15. Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.

![XML-Datei](media/4_XML_file.png)

### <a name="correction-transactions"></a>Korrekturtransaktionen

1.  Wählen Sie eine neue Transaktion aus. Informationen zur Buchung einer Kundenrechnung finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**.

| **Datum**        | **Buchungstyp**        | **Nettobetrag** | **Mehrwertsteuerbetrag** | **Mehrwertsteuercode** | **Erwartete Steuerbemessungsgrundlage – Berichtscode** | **Erwarteter Steuerbemessungsbetrag – Berichtscode** |
|-----------------|-----------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| 1. Januar 2020 | Debitorenrechnung (Inland) | 100            | 7              | VAT7               | 86                                     | 186                                      |

2. Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.
3. Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.

    - **Ausgleichsperiode:** Mo
    - **Von Datum** = 1/1/2020

4. Wählen Sie **OK**.
5. Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.
6. Wählen Sie **OK**.
7. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.
8. Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.

![Vorschau des Protokolls der elektronischen Steuererklärung](media/5_Electronic_tax_declaration_log.png)

Beachten Sie, dass eine Korrekturtransaktion zur Erklärung in Codes **86** und **83** hinzugefügt wird.

9. Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.
10. Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.

![XML-Datei](media/6_XML_file.png)

Beachten Sie, dass eine Korrekturtransaktion zur Erklärung in Codes **86** und **83** hinzugefügt wird.

## <a name="review-sales-tax-report-amounts"></a>Überprüfen Sie die Beträge des Umsatzsteuerberichts 

Sie können den Umsatzsteuerbetrag optional im SSRS-Bericht überprüfen.

### <a name="set-up-the-report-layout-for-sales-tax-authorities"></a>Richten Sie das Berichtslayout für die Umsatzsteuerbehörden ein

1. Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuerbehörden**.
2. Wählen Sie auf der Seite **Mehrwertsteuer-Behörden** die Mehrwertsteuerbehörde, die für den Mehrwertsteuer-Abrechnungszeitraum in den Mehrwertsteuercodes verwendet wird.
3. Im **Berichtslayout**-Feld wählen Sie **Deutsches Steuererklärungslayout**.

### <a name="generate-a-sales-tax-payment-and-print-the-german-sales-tax-report"></a><a name="generatesalestaxpayment"></a> Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus

Berechnen Sie am Ende des MwSt.-Berichtszeitraums die Mehrwertsteuerbeträge für den Abrechnungszeitraum.

1. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.
2. Im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld stellen die erforderlichen Felder wie [vorhin](#createvatdecxmlformat) beschrieben ein.
3. Wählen Sie **OK**.
4. Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld legen Sie die **Elektronisches Steuerdokument erstellen**-Option auf **Nein** fest.
5. Wählen Sie **OK** aus, um die Mehrwertsteuerzahlung zu generieren und den Bericht zu überprüfen.

Wenn Sie Transaktionen wie in Schritt 5 des [Beispiels](#example) zu Beginn dieses Themas buchen, werden die folgenden Daten angezeigt.

![Generierter deutscher Mehrwertsteuerbericht, Seite 1](media/7_Sales_tax_reporting.png)

![Generierter deutscher Mehrwertsteuerbericht, Seite 2](media/8_Sales_tax_reporting.png)

### <a name="print-a-sales-tax-payment-report-from-a-sales-tax-payment"></a>Drucken Sie einen Mehrwertsteuerzahlungsbericht aus einer Mehrwertsteuerzahlung

1. Wechseln Sie zu **Steuer** \> **Anfragen und Berichte** \> **Mehrwertsteuerzahlungen**.
2. Auf der **Mehrwertsteuerzahlung**-Seite wählen Sie den Datensatz aus und wählen dann **Bericht drucken** aus.
3. Stellen Sie im Dialogfeld die Felder wie im vorherigen Abschnitt beschrieben ein und wählen Sie dann **OK**.

### <a name="report-sales-tax-for-the-settlement-period"></a>Umsatzsteuer für Abrechnungszeitraum melden

Sie können den deutschen Mehrwertsteuerbericht auch mit der **Umsatzsteuer für Abrechnungszeitraum melden**-Anfrage erstellen.

1. Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.
2. Im **Umsatzsteuer für Abrechnungszeitraum melden**-Dialogfeld, stellen Sie die **Ausgleichsperiode** und die **Anfangsdatum**-Felder wie im Abschnitt [Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus](#generatesalestaxpayment) weiter oben in diesem Thema beschrieben ein.
3. Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:

- **Original** – Einen Mehrwertsteuerbericht generieren für die erste gebuchte Ausgleichsberechnung für das Periodenintervall.
- **Korrekturen** – Einen Mehrwertsteuerbericht generieren für nachfolgende Ausgleichsberechnungen für das Periodenintervall.
- **Gesamtliste** – Erstellen Sie einen Bericht für alle Verkaufstransaktionen für den Zeitraum. Diese Transaktionen umfassen ursprüngliche und korrigierte Transaktionen.

4. Wählen Sie **OK**.
5. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.
6. Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Original** aus.
7.  Drucken Sie den Bericht aus und überprüfen Sie die Daten.

| **Berichtscode** | **Mehrwertsteuerbetrag** |
|--------------------|----------------------|
| 41                 | 100                  |
| 43                 | 100                  |
| 61                 | 7                    |
| 81                 | 100                  |
| 93                 | 100                  |
| 181                | 19                   |
| 193                | 7                    |

8. Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.
9. Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Neueste Korrekturen** aus.
10. Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.
11. Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Korrekturen** aus. Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

| **Berichtscode** | **Mehrwertsteuerbetrag** |
|--------------------|----------------------|
| 86                 | 100                  |
| 186                | 7                    |

12. Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.
13. Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Gesamtliste** aus. Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.

| **Berichtscode** | **Mehrwertsteuerbetrag** |
|--------------------|----------------------|
| 41                 | 100                  |
| 43                 | 100                  |
| 61                 | 7                    |
| 81                 | 100                  |
| 86                 | 100                  |
| 93                 | 100                  |
| 181                | 19                   |
| 186                | 7                    |
| 193                | 7                    |
