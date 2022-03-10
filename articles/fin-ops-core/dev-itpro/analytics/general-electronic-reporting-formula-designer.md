---
title: Formeldesigner in der elektronischen Berichterstellung (EB)
description: In diesem Thema werden allgemeine Informationen zur Verwendung des Formel-Designers bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eec63fb1782c5afed0320eb841b6bfc92af31a691731ef6bac5d00ed442c0dcd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777403"
---
# <a name="formula-designer-in-electronic-reporting-er"></a>Formeldesigner in der elektronischen Berichterstellung (EB)

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie den Formel-Designer in der elektronischen Berichterstattung (ER) verwendet wird. Wenn Sie ein Format für ein bestimmtes elektronisches Dokument in EB entwerfen, können Sie Formeln zum Transformieren von Daten verwenden, sodass sie den Anforderungen für die Dokumenterfüllung und Formatierung zu entsprechen. Diese Formeln ähneln Formeln in Microsoft Excel. Unterschiedliche Arten von Funktionen werden in den Formeln unterstützt: Text, Datum und Uhrzeit, Mathematisches, Logisches, Informationen und Datentypumrechnung sowie andere domänenspezifische Funktionen des Unternehmens.

## <a name="formula-designer-overview"></a>Formeldesignerübersicht

EB unterstützt den Formeldesigner. Daher können Sie zum Zeitpunkt des Entwurfs Ausdrücke konfigurieren, die für folgende Aufgaben zur Laufzeit verwendet werden können:

- Transformation Sie Daten, die von einer Anwendungsdatenbank empfangen werden und in ein EB-Datenmodell eingegeben werden sollen, das so konzipiert wurde, dass es als Datenquelle für EB-Formate dient. (Diese Transformationen können beispielsweise Filterung, Gruppierung und Datentypkonvertierung umfassen.)
- Formatieren Sie Daten, die an ein generierendes elektronisches Dokument in Übereinstimmung mit dem Layout und den Bedingungen eines spezifischen EB-Formats übermittelt werden müssen. (Die Formatierung kann beispielsweise in Übereinstimmung mit der angeforderten Sprache oder Kultur oder der Codierung erfolgen).
- Steuern Sie den Prozess der Erstellung elektronischer Dokumente. (Die Ausdrücke können beispielsweise die Ausgabe bestimmter Elemente des Formats aktivieren oder deaktivieren, abhängig von der Verarbeitung von Daten. Sie können auch den Dokumenterstellungsprozess unterbrechen oder Nachrichten an Benutzer auslösen.)

Sie können die Seite **Formeldesigner** öffnen, wenn Sie irgendeine der folgenden Aktionen ausführen:

- Binden von Datenquellenartikeln zu den Datenmodellkomponenten.
- Binden von Datenquellenartikeln zu den Datenformatkomponenten.
- Verwaltung von berechneten Feldern, die Teil von Datenquellen sind, abschließen.
- Definition von Sichtbedingungen für Benutzereingabeparameter.
- Entwurf der Umwandlungen des Formats.
- Definition der Aktivierung von Bedingungen für die Komponenten des Formats.
- Definition von Dateinamen für die DATEIkomponenten des Formats.
- Definition der Bedingungen für Prozesssteuerprüfungen.
- Definition der Nachrichtentextes für Prozesssteuerprüfungen.

## <a name="data-binding"></a><a name="Binding"></a>Datenbindung

Der EB-Formeldesigner kann verwendet werden, um einen Ausdruck zu definieren, der Daten transformiert, die von Datenquellen empfangen werden, sodass die Daten beim Datenkonsument in folgender Art zur Laufzeit eingegeben werden können:

- von Anwendungsdatenquellen und Laufzeitparametern zum ER-Datenmodell
- Von einem ER-Datenmodell zu einem ER-Format
- von Anwendungsdatenquellen und Laufzeitparametern zum ER-Format

Die folgende Abbildung zeigt das Design eines Ausdrucks dieses Typs. In diesem Beispiel wird durch den Ausdruck der Wert des Felds **Intrastat.AmountMST** der Intrastat-Tabelle auf zwei Dezimalstellen gerundet und dann der gerundete Wert zurückgegeben.

[![Datenbindungsausdruck.](./media/picture-expression-binding.jpg)](./media/picture-expression-binding.jpg)

Die folgende Abbildung zeigt, wie ein Ausdruck dieses Typs verwendet werden kann. In diesem Beispiel wird das Ergebnis des entworfenen Ausdrucks in die Komponente **Transaction.InvoicedAmount** des Datenmodells **Steuererklärungsmodell** eingegeben.

[![Datenbindungausdruck, der verwendet wird.](./media/picture-expression-binding2.jpg)](./media/picture-expression-binding2.jpg)

Zur Laufzeit rundet die entworfene Formel `ROUND (Intrastat.AmountMST, 2)` den Wert des Felds **AmountMST** für jeden Datensatz in der Intrastat-Tabelle auf zwei Dezimalstellen. Sie gibt dann den gerundeten Wert in der Komponente **Transaction.InvoicedAmount** des Datenmodells **Steuererklärung** ein.

## <a name="data-formatting"></a><a name="Transformation"></a>Datenformatierung

Der ER-Formeldesigner kann verwendet werden, um einen Ausdruck zu definieren, der Daten umwandelt, die von den Datenquellen empfangen werden, sodass die Daten als Teil zum Erstellen eines elektronischen Dokuments gesendet werden können. Möglicherweise haben Sie Formatierung, die als eine typische Regel angewendet werden muss, die für ein Format erneut verwendet werden muss. In diesem Fall können Sie diese Formatierung einmal in der Formatkonfiguration einführen, als benannte Transformation, die einen Formatierungsausdruck hat. Diese benannte Transformation kann dann mit vielen Formatkomponenten verknüpft werden, wobei die Ausgabe gemäß dem Formatierungsausdruck formatiert werden muss, den Sie erstellt haben.

Die folgende Abbildung zeigt das Design einer Umwandlung dieses Typs. In diesem Beispiel kürzt die **TrimmedString**-Tansformation eingehende Daten des Datentyps *Zeichenfolge*, indem führende und nachfolgende Leerzeichen entfernt werden. Sie gibt dann einen gekürzten Zeichenfolgenwert zurück.

[![Transformation.](./media/picture-transformation-design.jpg)](./media/picture-transformation-design.jpg)

Die folgende Abbildung zeigt, wie die Umwandlung dieses Typs verwendet werden kann. In diesem Beispiel senden mehrere Formatkomponenten Text als Ausgabe an das generierende elektronische Dokument zur Laufzeit. Alle diese Formatkomponenten verweisen auf die Transformation **TrimmedString** nach Name.

[![Transformation, die verwendet wird.](./media/picture-transformation-usage.jpg)](./media/picture-transformation-usage.jpg)

Wenn Formatkomponenten, wie beispielsweise die Komponente **partyName** in der vorausgehenden Abbildung, auf die Transformation **TrimmedString** verweisen, übermittelt die Transformation Text als Ausgabe an das generierende elektronische Dokument. Dieser Text umfasst keine vor- und nachgestellten Leerzeichen.

Wenn Sie eine Formatierung haben, die einzeln angewendet werden muss, kann sie als einzelner Ausdruck der Bindung einer bestimmten Formatkomponente eingeführt werden. Die folgende Abbildung zeigt einen Ausdruck dieses Typs. In diesem Beispiel wird die Formatkomponente **partyType** an die Datenquelle über einen Ausdruck gebunden, der die eingehenden Daten aus dem Feld **Model.Company.RegistrationType** in der Datenquelle in Text in Großbuchstaben konvertiert. Der Ausdruck sendet dann diesen Text als Ausgabe an das elektronische Dokument.

[![Anwenden der Formatierung auf eine einzelne Komponente.](./media/picture-binding-with-formula.jpg)](./media/picture-binding-with-formula.jpg)

## <a name="process-flow-control"></a><a name="Validation"></a>Prozessflusssteuerung

Der EB-Formeldesigner kann verwendet werden, um Ausdrücke zu definieren, die den Prozessfluss zum Generieren elektronischer Dokumenten steuern. Die folgenden Aufgaben können ausgeführt werden:

- Definiert Bedingungen, wenn ein Dokumentenerstellungsprozess gestoppt werden muss.
- Geben Sie Ausdrücke an, die entweder Nachrichten für den Benutzer über beendete Prozess erstellen oder Ausführungsprotokollnachrichten zum fortlaufenden Prozess der Berichterstellung auslösen.
- Geben Sie die Dateinamen zum Generieren elektronischer Dokumente an, und steuern Sie die Bedingungen ihrer Erstellung.

Jede Regel der Prozessflusssteuerung ist als einzelne Prüfung entworfen. Die folgende Abbildung zeigt die Überprüfung dieses Typs. Ist hier eine Erläuterung der Konfiguration in diesem Beispiel:

- Die Überprüfung wird ausgewertet, wenn der **INSTAT** Knoten während der Generierung der XML-Datei erstellt wird.
- Wenn die Transaktionsliste leer ist, stoppt die Überprüfung den Ausführungsprozess und gibt **FALSCH** zurück.
- Die Prüfung gibt eine Fehlermeldung zurück, der den Text der Beschriftung SYS70894 in der bevorzugten Sprache des Benutzers umfasst.

[![Prüfung.](./media/picture-validation.jpg)](./media/picture-validation.jpg)

Der EB-Formeldesigner wird auch verwendet, um einen Dateinamen für ein generierendes elektronisches Dokument zu generieren und den Dateierstellungsprozess zu steuern. Die folgende Abbildung zeigt das Design einer Prozessablaufsteuerung dieses Typs. Ist hier eine Erläuterung der Konfiguration in diesem Beispiel:

- Die Liste der Datensätze aus der Datenquelle **model.Intrastat** wird in Chargen aufgeteilt. Jede Charge enthält bis zu 1.000 Datensätze.
- Die Ausgabe erstellt eine ZIP-Datei, die eine Datei im XML-Format für jede Charge enthält, die erstellt wurde.
- Ein Ausdruck gibt einen Dateinamen für das Generieren von elektronischen Dokumenten zurück, indem er den Dateinamen und die Dateinamenerweiterung verkettet. Für die zweite und alle nachfolgenden Chargen enthält der Dateiname die Chargenkennung als Suffix.
- Ein Ausdruck aktiviert (durch Rückgabe von **WAHR**) den Dateierstellungsprozess für Chargen, die mindestens einen Datensatz beinhalten.

[![Prozessflusssteuerung.](./media/picture-file-control.jpg)](./media/picture-file-control.jpg)

## <a name="document-content-control"></a><a name="Enabled"></a>Inhaltskontrolle von Dokumenten

Der EB-Formeldesigner kann verwendet werden, um Ausdrücke zu konfigurieren, die steuern, welche Daten zur Laufzeit in generierten elektronischen Dokumenten platziert werden. Die Ausdrücke können die Ausgabe bestimmter Elemente des Formats aktivieren oder deaktivieren, je nach Verarbeitungsdaten und konfigurierter Logik. Diese Ausdrücke können für ein einzelnes Formatelement im Feld **Aktiviert** auf der Registerkarte **Zuordnung** auf der Seite **Arbeitsgangdesigner** als logische Bedingung eingegeben werden, die den Booleschen Wert zurückgibt: Sie können die Ausdrücke als logische Bedingung eingeben, die einen *booleschen* Wert zurückgibt:

- Wenn die Bedingung **True** zurückgibt, wird das aktuelle Formatelement ausgeführt.
- Wenn die Bedingung **False** zurückgibt, wird das aktuelle Formatelement übersprungen.

Die folgende Abbildung zeigt Ausdrücke dieses Typs. (Version 11.12.11 der Formatkonfiguration **ISO20022 Kreditübertragung (NO)**, die von Microsoft bereitgestellt wird, wird als Beispiel verwendet.) Die Formatkomponente **XMLHeader** ist so konfiguriert, dass sie die Struktur der Kreditübertragungsnachricht gemäß den XML-Nachrichtenstandards von ISO 20022 beschreibt. Die **XMLHeader/Document/CstmrCdtTrfInitn/PmtInf/CdtTrfTxInf/RmtInf/Ustrd** Formatkomponente wird konfiguriert, um das **Ustrd** XML-Element zur generierten Nachricht hinzuzufügen und die Überweisungsinformationen in einem unstrukturierten Format als Text der folgenden XML-Elemente zu platzieren:

- Die Komponente **PaymentNotes** wird verwendet, um den Text von Zahlungshinweisen zu generieren.
- Die Komponente **DelimitedSequence** generiert kommagetrennte Rechnungsnummern aus, die zur Abrechnung der aktuellen Überweisung verwendet werden.

[![Komponenten PaymentNotes und DelimitedSequence.](./media/GER-FormulaEditor-ControlContent-1.png)](./media/GER-FormulaEditor-ControlContent-1.png)

> [!NOTE]
> Die Komponenten **PaymentNotes** und **DelimitedSequence** werden mithilfe eines Fragezeichens gekennzeichnet. Ein Fragezeichen zeigt an, dass die Verwendung einer Komponente an Bedingungen geknüpft ist. In diesem Fall basiert die Verwendung der Komponenten auf den folgenden Kriterien:
>
> - Der Ausdruck `@.PaymentsNotes <> ""`, der für die Komponente **PaymentNotes** (durch Zurückgeben von **TRUE**) definiert wird, ermöglicht, dass das **Ustrd** XML-Element mit dem Text zu Zahlungshinweisen ausgefüllt wird, wenn dieser Text für die aktuelle Überweisung nicht leer ist.
>
>    [![Ausdruck für die PaymentNotes-Komponente.](./media/GER-FormulaEditor-ControlContent-2.png)](./media/GER-FormulaEditor-ControlContent-2.png)
>
> - Der für die Komponente **DelimitedSequence** definierte Ausdruck `@.PaymentsNotes = ""` ermöglicht (durch Zurückgeben von **TRUE**) die Auffüllung des **Ustrd**-XML-Elements mit einer durch Kommata getrennten Liste mit Rechnungsnummern, die zur Abrechnung der aktuellen Überweisung verwendet werden, wenn der Text dieser Zahlungshinweise für diese Überweisung leer ist.
>
>    [![Ausdruck für die DelimitedSequence-Komponente.](./media/GER-FormulaEditor-ControlContent-3.png)](./media/GER-FormulaEditor-ControlContent-3.png)
> 
> Basierend auf dieser Einstellung, die für jede Debitorenzahlung generiert wird, enthält das **Ustrd** XML-Element entweder den Text von Verwendungszwecken oder, wenn dieser Text leer ist, eine durch Kommata getrennte Liste mit Rechnungsnummern, die zur Begleichung dieser Zahlung verwendet werden.

## <a name="validation-of-configured-formulas"></a><a name="TestFormula"></a>Validierung von konfigurierten Formeln

Wählen Sie auf der Seite **Formel-Designer** die Option **Test** aus, um zu überprüfen, wie die konfigurierte Formel funktioniert.

[![Wählen Sie Test, um eine Formel zu validieren.](./media/ER-FormulaTest-Start.png)](./media/ER-FormulaTest-Start.png)

Wenn die Werte von Formelargumenten erforderlich sind, können Sie das Dialogfeld **Testausdruck** über die Seite **Formel-Designer** öffnen. In den meisten Fällen müssen diese Argumente manuell definiert werden, da die konfigurierten Bindungen zur Entwurfszeit nicht ausgeführt werden. Die Registerkarte **Testergebnis** auf der Seite **Formel-Designer** zeigt das Ergebnis der Ausführung der konfigurierten Formel an.

Das folgende Beispiel zeigt, wie Sie die für die Außenhandelsdomäne konfigurierte Formel testen können, um sicherzustellen, dass der Intrastat-Warencode nur Ziffern enthält.

Wenn Sie diese Formel testen, können Sie das Dialogfeld **Testausdruck** verwenden, um den Wert des Intrastat-Warencodes zum Testen anzugeben.

[![Angabe des Intrastat-Warencodes zum Testen.](./media/ER-FormulaTest-Start-EnterArguments.png)](./media/ER-FormulaTest-Start-EnterArguments.png)

Nachdem Sie den Intrastat-Warencode angegeben und **OK** ausgewählt haben, wird auf der Registerkarte **Testergebnis** auf der Seite **Formel-Designer** das Ergebnis der Ausführung der konfigurierten Formel angezeigt. Sie können dann bewerten, ob das Ergebnis akzeptabel ist. Wenn das Ergebnis nicht akzeptabel ist, können Sie die Formel aktualisieren und erneut testen.

[![Testergebnis.](./media/ER-FormulaTest-Result.png)](./media/ER-FormulaTest-Result.png)

Einige Formeln können zur Entwurfszeit nicht getestet werden. Beispielsweise kann eine Formel ein Ergebnis eines Datentyps zurückgeben, der auf der Registerkarte **Testergebnis** nicht angezeigt werden kann. In diesem Fall erhalten Sie eine Fehlermeldung, die besagt, dass die Formel nicht getestet werden kann.

[![Fehlermeldung.](./media/ER-FormulaTest-Error.png)](./media/ER-FormulaTest-Error.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)
- [Formelsprache in der elektronischen Berichterstellung](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]