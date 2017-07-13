---
title: "Verlängerung der Steuerschuld | Microsoft Doc."
description: "In diesem Thema wird erläutert, wie die Verlagerung der Steuerschuld für europäische Länder eingerichtet wird."
author: epodkolz
manager: AnnBe
ms.date: 05/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 6cb473962f40ed9ef2f5f807f089098764f47009
ms.openlocfilehash: b3c94fa73410d9bdcaaec11dee04a7a239e4d45a
ms.contentlocale: de-de
ms.lasthandoff: 06/14/2017

---

# <a name="reverse-charge-vat"></a>Verlagerung der Steuerschuld
In diesem Thema wird ein allgemeiner Ansatz zum Einrichten der Verlagerung der Steuerschuld für europäischer Länder beschrieben.

Die Verlagerung der Steuerschuld ist ein Steuerschema, das die Zuständigkeit für die Buchhaltung und das Melden der Mehrwertsteuer vom Verkäufer auf den Einkäufer von Waren und/oder Dienstleistungen verschiebt. Daher melden Empfänger von Waren und/oder Dienstleistungen die Ausgangssteuer (in der Rolle eines Verkäufers) sowie die Vorsteuer (in der Rolle des Einkäufers) in ihrer MwSt.-Abrechnung.

Die Europäischen Union (EU) Directive ermöglicht es Mitgliedsstaaten zu ermitteln, wie die allgemeinen Anforderungen in lokale Anforderungen angepasst werden. Daher wird die das Schema der Verlagerung der Steuerschuld in einigen Ländern nur für einige Waren und/oder Dienstleistungen implementiert, und es gibt zusätzliche Bedingungen oder Schwellenwerte bei Umsatzbeträgen. In anderen Ländern hängt die Zuständigkeit für die Mehrwertsteuer-Zahlung vom Status des Lieferanten und des Käufers ab. Wenn der Käufer verpflichtet ist, die MwSt. zu bezahlen, muss diese Tatsache eindeutig auf der Rechnung angegeben werden, die vom Lieferanten gestellt wird. So müssen z. B. die Worte "Verlagerung der Steuerschuld" auf der Rechnung vorkommen und es muss angegeben werden, welche Positionen vom Steuerschuldumkehrschema erfasst werden. 

Um die Verlagerung der Steuerschuld anzuwenden, müssen Sie die folgende Einrichtung abschließen.

## <a name="set-up-sales-tax-codes"></a>Mehrwertsteuercodes einrichten
Es wird empfohlen, dass Sie separate Mehrwertsteuercodes für Einkaufsarbeitsgänge und Vertriebsarbeitsgänge verwenden.

<table>
<body>
<tr>
<td><strong>Mehrwertsteuercode für Umsätze</strong></td>
<td>Erstellen Sie einen Mehrwertsteuercode für Arbeitsgänge mit Verlagerung der Steuerschuld (<strong>Steuer</strong> > <strong>Indirekte Steuern</strong> > <strong>Mehrwertsteuer</strong> > <strong>Mehrwertsteuercodes</strong>).
</td>
</tr>
<tr>
<td><strong>Mehrwertsteuercode für Einkäufe</strong></td>
<td><p>Erstellen Sie positive und negative Mehrwertsteuercodes für die Verlagerung der Steuerschuld für Einkäufe (<strong>Steuern</strong> > <strong>Indirekte Steuern</strong> > <strong>Mehrwertsteuer</strong> > <strong>Mehrwertsteuercodes</strong>).</p>
<ol>
<li>Erstellen Sie einen Mehrwertsteuercode mit positivem Wert.</li>
<li>Erstellen Sie einen Mehrwertsteuercode mit negativem Wert. Legen Sie die <strong>Negativen Mehrwertsteuersatz zulassen</strong>-Option auf <strong>Ja</strong> fest.
Sie müssen diesen negativen Mehrwertsteuercode einer Artikel-Mehrwertsteuergruppe zuordnen und anschließend diese Artikel-Mehrwertsteuergruppe den Artikeln zuordnen, für die die Verlagerung der Steuerschuld gilt.</li>
</ol>
<p>Weitere Informationen finden Sie im nächsten Abschnitt "Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten".</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Mehrwertsteuergruppen und Artikel-Mehrwertsteuergruppen einrichten
Es wird empfohlen, dass Sie separate Mehrwertsteuergruppen für Einkaufsarbeitsgänge und Vertriebsarbeitsgänge verwenden.

<table>
<tr>
<td><strong>Mehrwertsteuergruppen für Verkäufe</strong></td>
<td>Erstellen Sie eine Mehrwertsteuergruppe für Verkaufsarbeitsgänge mit Verlagerung der Steuerschuld (<strong>Steuer</strong> > <strong>Indirekte Steuern</strong> > <strong>Mehrwertsteuer</strong> > <strong>Mehrwertsteuergruppen</strong>). Geben Sie auf der Registerkarte <strong>Einstellungen</strong> den Mehrwertsteuercode für die Verlagerung der Steuerschuld in dieser Gruppe an. Aktivieren Sie die Kontrollkästchen <strong>Befreit</strong> und <strong>Verlagerung der Steuerschuld</strong> für den Mehrwertsteuercode.</td>
</tr>
<tr>
<td><strong>Mehrwertsteuergruppen für Einkäufe</strong></td>
<td>Erstellen Sie eine Mehrwertsteuergruppe für Einkaufsarbeitsgänge mit Verlagerung der Steuerschuld (<strong>Steuer</strong> > <strong>Indirekte Steuern</strong> > <strong>Mehrwertsteuer</strong> > <strong>Mehrwertsteuergruppen</strong>). Geben Sie auf der Registerkarte <strong>Einstellungen</strong> die positiven und negativen Mehrwertsteuercodes in dieser Gruppe an. Aktivieren Sie das Kontrollkästchen <strong>Verlagerung der Steuerschuld</strong> für den Mehrwertsteuercode mit negativem Wert.</td>
</tr>
<tr>
<td><strong>Artikel-Mehrwertsteuergruppen</strong></td>
<td>Erstellen oder aktualisieren Sie die Artikel-Mehrwertsteuergruppe mit dem Mehrwertsteuercode mit negativem Wert (<strong>Steuer</strong> > <strong>Indirekte Steuern</strong> > <strong>Mehrwertsteuer</strong> > <strong>Artikel-Mehrwertsteuergruppen</strong>). Sie müssen den Produkten und Kategorien, für die die Verlagerung der Steuerschuld gilt, die Artikel-Mehrwertsteuergruppe zuweisen.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a>Einrichten von Verlagerungen der Steuerschuldgruppen
Auf der Seite **Artikelgruppen für die Verlagerung der Steuerschuld** (**Steuer** > **Einstellungen** > **Mehrwertsteuer** > **Artikelgruppen für die Verlagerung der Steuerschuld**) können Sie Gruppen von Produkten bzw. Diensten oder Einzelprodukte bzw. -dienste definieren, auf die die Verlagerung der Steuerschuld angewendet werden kann. Definieren Sie für jede Artikelgruppen für die Verlagerung der Steuerschuld die Liste der Artikel, Artikelgruppen oder Kategorien für Verkäufe und/oder Einkäufe.

## <a name="set-up-reverse-charge-rules"></a>Regeln für die Verlagerungen der Steuerschuld einrichten
Auf der Seite **Regeln für die Verlagerung der Steuerschuld** (**Steuer** > **Einstellungen** > **Mehrwertsteuer** > **Verlagerung der Steuerschuld**) können Sie die Anwendbarkeitsregeln zu Einkaufs- und Vertriebszwecke definieren. Sie können einen Satz von Regeln für die Verlagerung der Steuerschuld konfigurieren. Legen Sie für jede Regel die folgenden Felder fest:

- **Dokumenttyp** – Wählen Sie **Bestellung**, **Kreditorenrechnungserfassung**, **Auftrag**, **Freitextrechnung**, **Debitorenrechnungserfassung** und/oder **Kreditorenrechnung** aus.
- **Lander/Region des Partners** – Wählen Sie **Inland**, **EU** oder **Ausland** aus. Falls die Regel für alle Handelspartner unabhängig vom Land oder der Region ihrer Adresse gilt, wählen Sie **Alle** aus.
- **Inländische Lieferadresse** – Aktivieren Sie dieses Kontrollkästchen, um die Regel auf Lieferungen im gleichen Land oder der gleichen Region anzuwenden. Dieses Kontrollkästchen kann nicht für die Dokumenttypen **Kreditorenrechnungserfassung** und **Debitorenrechnungserfassung** aktiviert werden.
- **Artikelgruppe für Verlagerung der Steuerschuld** – Wählen Sie die Gruppe aus, auf die die Regel angewendet werden kann.
- **Schwellenwertbetrag** – Das Schema der Verlagerung der Steuerschuld wird nur dann bei einer Rechnung angewendet, wenn der Wert der Artikel und/oder Services in der Gruppe der Verlagerung der Steuerschuld das hier angegebene Limit überschreitet.

Sie können die Felder **Gültigkeitsdatum** und **Ablaufdatum** verwenden, um den Zeitraum festzulegen, in dem die Regel gültig ist.

Darüber hinaus können Sie angeben, ob eine Benachrichtigung angezeigt wird und die Dokumentposition mit der Mehrwertsteuergruppe für Verlagerungen der Steuerschuld aktualisiert wird, wenn die Bedingung für diese Dokumentposition erfüllt wird. Die folgenden Optionen sind verfügbar:

- **Keine** – Die Dokumentposition wird nicht aktualisiert.
- **Bestätigung** – Eine Benachrichtigung wird angezeigt, um zu bestätigen, dass die Verlagerung der Steuerschuld angewendet werden kann.
- **Satz** – Die Dokumentposition wird ohne zusätzliche Benachrichtigung aktualisiert.

## <a name="set-up-default-parameters"></a>Einrichten von Standardparametern
Um die Funktionen zu aktivieren, legen Sie auf der Seite **Hauptbuchparameter** auf der Registerkarte **Verlagerung der Steuerschuld** die Option **Verlagerung der Steuerschuld aktivieren** auf **Ja** fest. Wählen Sie in den Feldern **Mehrwertsteuergruppe für Bestellung** und **Mehrwertsteuergruppe für Auftrag** die standardmäßigen Mehrwertsteuergruppen aus. Wenn eine Anwendbarkeitsbedingung für die Verlagerung der Steuerschuld erfüllt wird, wird die Bestellposition für den Auftrag oder die Bestellung mit diesen Mehrwertsteuergruppen aktualisiert.

## <a name="reverse-charge-on-a-sales-invoice"></a>Verlagerung der Steuerschuld für eine Verkaufsrechnung
Bei Aufträgen mit dem Schema der Verlagerung der Steuerschuld stellt der Verkäufer keine Mehrwertsteuer in Rechnung. Stattdessen gibt die Rechnung die Artikel, für die die Verlagerung der Steuerschuld gilt, und den Gesamtbetrag der Verlagerung der Steuerschuld an.

Wenn eine Verkaufsrechnung mit Verlagerung der Steuerschuld gebucht wird, weisen die Mehrwertsteuerbuchungen Steuerart **Mehrwertsteuer** sowie Null Mehrwertsteuer aus, und das Kontrollkästchen **Verlagerung der Steuerschuld** ist aktiviert.

## <a name="reverse-charge-on-a-purchase-invoice"></a>Verlagerung der Steuerschuld für eine Einkaufsrechnung
Für Bestellungen mit dem Schema der Verlagerung der Steuerschuld agiert der Käufer, der die Rechnung mit der Verlagerung der Steuerschuld erhält, für MwSt.-Buchhaltungszwecke als Einkäufer und Verkäufer.

Wenn eine Einkaufsrechnung mit Verlagerung der Steuerschuld gebucht wird, werden zwei Mehrwertsteuerbuchungen erstellt. Eine Buchung hat Steuerart die **Vorsteuer**. Die zweite Buchung hat die Steuerart **Mehrwertsteuer** und das Kontrollkästchen **Verlagerung der Steuerschuld** ist aktiviert.

