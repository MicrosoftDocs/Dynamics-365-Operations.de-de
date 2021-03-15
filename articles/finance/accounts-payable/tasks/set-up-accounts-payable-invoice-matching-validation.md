---
title: Einrichten der Kreditorenkonten-Rechnungsabgleichprüfung
description: Dieses Thema enthält Informationen darüber, wie der Kreditorenkonten-Rrechnungsabgleich eingerichtet wird.
author: abruer
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 662b080a0e87ae6ce7d89ffa848579517dd9b6a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979237"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Einrichten der Kreditorenkonten-Rechnungsabgleichprüfung

[!include [banner](../../includes/banner.md)]

Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde. Stellen Sie sicher, dass der Konfigurationsschlüssel "Belastungen" ausgewählt ist, wenn von der juristischen Person Belastungen zur Nachverfolgung von Ausgaben (wie z. B. Fracht) verwendet werden.  Beim Kreditorenrechnungsabgleich handelt es sich um den Prozess zum Abgleich der Informationen aus der Kreditorenrechnung, der Bestellung und des Produktzugangs. Unterschiede zwischen diesen Dokumenten werden als Abgleichsabweichung bezeichnet. Abgleichsabweichungen werden mit den angegebenen Toleranzen verglichen. Übersteigt die Abgleichsabweichung den Toleranzprozentsatz oder -betrag, werden auf den Seiten **Kreditorenrechnung** und **Details zum Rechnungsabgleich** Abweichungssymbole angezeigt.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Bestimmen, welche Rechnungsabgleich-Prüfung verwendet wird
Vier unterschiedliche Arten von entsprechenden Prüfungen sind verfügbar. 

- **Positionsebenenabgleichen** – Der häufigste Abgleichstyp ist Position abgleichen. Positionsabgleich kann ein zweiseitiger oder dreiseitiger Abgleich sein. Der Standardpositionsebenenabgleich kann für eine juristische Person auf der Seite **Kreditorenkontenparameter** festgelegt werden. Zweiseitiger Abgleich vergleicht den Einheitspreis der Rechnung mit dem Einheitspreis der Bestelleinheit. Der dreiseitige Abgleich vergleicht zusätzlich die Rechnungsmenge mit der abgeglichenen Produktzugangsmenge.
- **Rechnungssummenablgeich** – Die Gesamtbeträge der Rechnung werden mit den Gesamtbeträgen der Bestellung abgeglichen. Bei dieser Art von Rechnungsabgleich werden die wenigsten Details einbezogen. Deshalb können Sie mit dieser Option Steuerfunktionen zur Minimierung der Arbeitszeit einrichten, die für die Prüfung der Informationen aus dem Abgleich erforderlich ist. Sechs Summen werden verglichen, einschließlich der Zwischensumme, Gesamtrabatt, Belastungen, Mehrwertsteuer, Rundung und Rechnungsbetrag. Das System prüft, ob Werte auf der Rechnung von den erwarteten Beträgen um mehr als einen akzeptablen Wert abweichen.
- **Abgleich für Zuschläge** – Die Informationen zu Zuschlägen (Beträge) der Rechnung werden mit den Informationen zu Zuschlägen (Beträge) der Bestellung abgeglichen.
- **Preissummen für passende Positionen** – Dieser Abgleichstyp ist hilfreich für Unternehmen, die in der Regel mehrere Rechnungen für eine einzelne Bestellposition erhalten. Wenn Sie normalerweise nur eine Rechnung pro Bestellposition erhalten, ist dieser Abgleichstyp nicht erforderlich. Dieser Abgleich erfordert, dass, ein zweiseitiger oder dreiseitiger Abgleich aktiviert wird und dient als ein nicht zu überschreitender Nettobetrag, basierend auf Toleranzprozentsätzen und Beträgen.  Dieser Abgleichstyp vergleicht die Preisinformationen für den Nettobetrag der einzelnen Rechnungspositionen sowie alle ausstehenden und bereits gebuchten Rechnungspositionen mit dem Nettobetrag der entsprechenden Bestellposition. Der Nettobetrag ergibt sich aus der folgenden Formel: (Einheitspreis * Positionsmenge) + Positionszuschläge - Positionsrabatte. Bei einem Abgleich der Preissummen nach Prozentsatz vergleicht das System Werte mithilfe der Transaktionswährung. Bei einem Abgleich der Preissummen nach Menge vergleicht das System die Werte mithilfe der Buchungswährung.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Parameter für die Aktivierung des Rechnungsabgleichs einrichten
1. Wechseln Sie zu **Kreditorenkonten > Einrichtung > Kreditorenkontenparameter**
2. Wählen Sie die Registerkarte **Rechnungsprüfung**.
3. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Rechnungsabgleichvalidierung**.
    * Wählen Sie aus, ob zum Buchen einer Rechnung mit Abweichungen beim Rechnungsabgleich eine Genehmigung erforderlich sein soll. Wenn dazu **Mit Warnung zulassen** festgelegt ist, wird ein visueller Hinweis angezeigt, wenn eine Abweichung beim Rechnungsabgleich die Toleranz übersteigt. Sie sind jedoch dazu in der Lage, die Rechnung zu buchen. Um Workflows zusammen mit der Rechnungsabgleichsüberprüfung zu verwenden, stellen Sie sicher, dass das Feld **Rechnung mit Abweichungen buchen** auf **Mit Warnung zulassen** festgelegt ist, um zu vermeiden, dass Sie mehrmals genehmigen müssen.  
    * Wählen Sie im Feld **Rechnungskopf-Abgleichstatus automatisch aktualisieren** aus, ob der Abgleich während der Rechnungsdateneingabe automatisch vom System ausgeführt wird. Die empfohlene Einstellung ist **Ja**, es sei denn, Sie haben Probleme bei der Dateneingabeleistung. Das Deaktivieren der automatischen Aktualisierungen ermöglicht möglicherweise eine schnellere Systemleistung, da die Rechnungsabgleichüberprüfung während der Dateneingabe umgangen wird. Der Dateneingabesekretär muss den Abgleichungsstatus der Rechnung manuell aktualisieren, um die Rechnungsabgleich-Überprüfergebnisse anzuzeigen, wenn dieser auf **Nein** festgelegt ist.  
4. **Rechnungssummenabgleich** festlegen.
5. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen **Rechnungssummen abgleichen**, um die tatsächlichen Rechnungssummen mit den erwarteten Summen abzugleichen.
    * Wählen Sie aus, ob ein Symbol angezeigt werden soll, wenn eine Abweichung beim Rechnungsabgleich die Toleranz übersteigt. Das Symbol kann angezeigt werden, wenn eine positive Abweichung die Toleranz übersteigt oder wenn entweder eine positive oder negative Abweichung die Toleranz übersteigt.  
    * Beispiel: Der Toleranzprozentsatz ist 5 %, und der Gesamtrechnungsbetrag in der Bestellung beträgt 100,00. Folglich wird ein Preisabgleichsymbol angezeigt, wenn der Gesamtbetrag der Rechnung 105,00 übersteigt. Wenn Sie **Wenn größer oder kleiner als Toleranz** auswählen, wird das Symbol auch angezeigt, wenn der Rechnungsbetrag niedriger ist als 95,00.  
6. Wählen Sie im Feld **Rechnungssummentoleranz in Prozent** die zulässige Abweichung in Prozent, der akzeptiert werden kann. Dieser Wert ist der Standardwert für das Unternehmen. Dieser Wert kann für bestimmte Kreditoren mithilfe der Seite **Rechnungssummentoleranzen** überschrieben werden. Informationen dazu, wie der Toleranzprozentsatz für Rechnungssummen für einen bestimmten Kreditor überschrieben wird, finden Sie unter Rechnungssummenabgleich-Toleranz für Kreditoren weiter unten in diesem Thema.
7. **Preis- und Mengenabgleich** festlegen.
8. Wählen Sie im Feld **Positionsabgleichsrichtlinie** einen Wert aus, der als Standardrichtlinie für die juristische Person dienen soll, mit der Sie arbeiten. **Nicht erforderlich** bedeutet, dass keine Überprüfung von einzelnen Rechnungspositionspreisen gegenüber Bestellungspreisen oder Rechnungsmengen gegenüber Lieferscheinmengen erforderlich ist. **Zweiseitiger Abgleich** bedeutet, dass die Überprüfung von Rechnungspositionen erforderlich ist, aber nur die Bestellung und Rechnungsdokumente des Lieferanten sind an der Überprüfung beteiligt. Der Produktzugang wird bei den Abgleichüberprüfungen nicht berücksichtigt. **Dreiseitiger Abgleich** bedeutet, dass der Nettostückpreis der Rechnung mit dem Nettostückpreis der Bestellung verglichen wird und die entsprechende Produktzugangsmenge mit der Rechnungsmenge verglichen wird.
9. Wählen Sie im Feld **Überschreiben der Abgleichsrichtlinie zulassen** einen Wert, um zuzulassen, dass eine andere Abgleichsebene für einen Artikel, einen Händler sowie eine Kombination von Händler und Artikel oder Bestellposition angewendet wird. Die Positionsabgleichsrichtlinie für juristische Personen kann für einen speziellen Händler, Artikel oder eine spezielle Kombination von Händler und Artikel auf der Seite **Abgleichsrichtlinie** überschrieben werden.
    * Wenn Sie eine Positionsabgleichsrichtlinie mit zweiseitigem Abgleich oder dreiseitigem Abgleich§ verwenden, können Sie Preistoleranz-Prozentwerte für Ihre juristische Person, Artikel und Kreditoren auf der Seite **Artikelpreistoleranz** einrichten. Die Standardpreistoleranz der juristischen Person ist auf null Prozent für zweiseitigen und dreiseitigen Abgleich festgelegt. Beim Vergleich von Kreditorenrechnungen mit Bestellinformationen in Bestellungen wird nach dem entsprechenden Preistoleranz-Prozentsatz gesucht.   
10. Wählen Sie einen Wert im Feld **Preissummen abgleichen** aus, um Preissummen für Rechnungspositionen abzugleichen. Dieser Abgleichstyp ist nützlich, wenn der Händler mehrere Rechnungen für die gleiche Bestellposition sendet. Sie können die Preisinformationen für den Nettobetrag der einzelnen Rechnungspositionen sowie alle ausstehenden und bereits gebuchten Rechnungspositionen mit den Nettobetrag der entsprechenden Bestellposition vergleichen.  Optionen sind **Keine**, **Prozentsatz**, **Betrag** oder **Prozentsatz und Betrag**.
11. Wählen Sie im Feld **Toleranz für die gesamte Einkaufssumme in Prozent** einen Prozentsatz für die Abweichung aus, die Sie akzeptieren. Dieses Feld ist nur verfügbar, wenn im Feld **Preissummen abgleichen** die Optionen **Prozentsatz** oder **Prozentsatz und Betrag** ausgewählt wurden.
12. Wählen Sie im Feld **Toleranz für Preissummenabgleich** einen Betrag in der Buchhaltungswährung aus. Dieses Feld ist nur verfügbar, wenn im Feld **Preissummenabgleich** die Optionen **Betrag** oder **Prozentsatz und Betrag** ausgewählt wurden.
13. Wählen Sie im Feld **Symbol für Preissummenabgleich anzeigen** aus, wann ein Symbol angezeigt werden soll, wenn eine Abweichung beim Rechnungsabgleich für den Nettostückpreis die Toleranz übersteigt. Das Symbol kann angezeigt werden, wenn eine positive Abweichung die Toleranz übersteigt oder wenn entweder eine positive oder negative Abweichung die Toleranz übersteigt.
Beispiel: Der Toleranzprozentsatz ist 5 %, und die Positionspreissumme in der Bestellung beträgt 10,00. Folglich wird ein Preisabgleichsymbol angezeigt, wenn die Positionspreissumme der Rechnung 10,50 übersteigt. Wenn Sie **Wenn größer oder kleiner als Toleranz** auswählen, wird das Symbol auch angezeigt, wenn die Positionspreissumme auf der Rechnung kleiner als 9,50 ist.
13. Abgleich von Belastungen festlegen.
14. Aktivieren Sie das Kontrollkästchen **Belastungen abgleichen**, um basierend auf den Informationen zur Bestellung die tatsächlichen Belastungen mit den erwarteten Belastungen abzugleichen.

## <a name="set-up-unit-price-tolerance-percentages"></a>Einrichten von Einehitspreistoleranz-Prozentsätzen
Wechseln Sie zu **Kreditorenkonten > Einstellungen > Rechnungsableich > Preistoleranzen**, um die zulässige Preistoleranzen zu definieren. Wenn Sie eine Positionsabgleichsrichtlinie mit zweiseitigem Abgleich oder dreiseitigem Abgleich verwenden, können Sie Preistoleranz-Prozentwerte für Ihre juristische Person, Artikel und Kreditoren auf der Seite Artikelpreistoleranz einrichten. Beim Vergleich von Kreditorenrechnungen mit Bestellinformationen in Bestellungen wird nach dem entsprechenden Preistoleranz-Prozentsatz gesucht. Das ist die Standard-Suchreihenfolge:
* Tabelle/Tabelle
* Tabelle/Gruppe
* Tabele/Alle
* Gruppe/Tabelle
* Gruppe/Gruppe
* Gruppe/Alle
* Alle/Tabelle
* Alle/Gruppe
* Alle/Alle

Die Standardpreistoleranz für die juristische Person liegt bei 0 Prozent, und diese Preistoleranz wird auf alle Artikel sowie auf alle Konten angewendet ("Alle", "Alle"). Der Datensatz der Standardpreistoleranz für die juristische Person kann nicht gelöscht werden.

Negative Preisabweichungen sind standardmäßig zulässig. Die Eingabe eines negativen Preistoleranz-Prozentsatzes ist jedoch nicht möglich. Wählen Sie zum Nachverfolgen negativer Toleranzen auf der Seite **Kreditorenkontenparameter** im Feld **Symbol für Abgleich von Belastungen anzeigen** die Option **Wenn größer oder kleiner als Toleranz** aus. Geben Sie dann den Preistoleranz-Prozentsatz auf der Seite **Preistoleranzen** ein.

## <a name="set-up-matching-policy-override"></a>Überschreiben der Abgleichsrichtlinie einrichten

Wechseln Sie zu **Kreditorenkonten > Einrichten > Rechnungsabgleich einrichten > Abgleichsrichtlinie**, um den Standardeintrag für das Abgleichsrichtlinienfeld für Positionen in der Bestellung zu definieren. Diese Einrichtung ist optional. Mithilfe dieses Formulars können Sie einen zweiseitigen oder dreiseitigen Abgleich für Artikel, Kreditoren oder Kombinationen von Kreditoren und Artikeln einrichten. Diese Einträge ermöglichen es, präzisere Abgleichsrichtlinien als die Abgleichrichtlinie der juristischen Person festzulegen, die Sie auf der Seite **Kreditorenkontenparameter** definiert haben. Diese Standard-Positionsabgleichsrichtlinie gilt für alle Artikel und Kreditoren mit Ausnahme derer, für die in diesem Formular eine andere Positionsabgleichsrichtlinie angegeben ist.

Auf dieser Registerkarte wählen Sie **Abgleichsrichtlinienebene** aus. Wählen Sie die Ebene der Abgleichsrichtlinienhierarchie aus, für die Sie die Positionsabgleichsrichtlinien festlegen möchten.

- **Artikel und Kreditor** – Die Abgleichsrichtlinie wird für bestimmte Artikel angegeben, die bei bestimmten Kreditoren erworben werden.
- **Artkel** – Die Abgleichsrichtlinie wird für alle Artikel angegeben, die bei bestimmten Kreditoren erworben werden mit Ausnahme der Artikel, die auf den Ebenen Artikel und Kreditor angegeben werden.
- **Kreditor** – Die Abgleichsrichtlinie wird für alle Artikel angegeben, die bei bestimmten Kreditoren erworben werden mit Ausnahme der Artikel, die auf den Ebenen Artikel und Kreditor angegeben werden.
  
Die verwendete Abgleichsrichtlinie wird anhand der folgenden Hierarchie bestimmt:
  *  Artikel und Kreditor
  *  Element
  *  Lieferant
  *  Juristische Person
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Toleranzen für den Abgleich von Rechnungssummen für Kreditoren einrichten

Wechseln Sie zu **Kreditor > Einrichtung > Rechnungsabgleich einrichten > Rechnungssummentoleranzen**, um Kreditor spezifische Toleranzen für Rechnungssummenabgleich festzulegen. Zur Berechnung des Abgleichs wird der Rechnungssummentoleranz-Prozentsatz aus dem Kreditorenkonto verwendet, das auf der Kreditorenrechnung als Auftragskonto angegeben ist. Wenn für das Kreditorenkonto kein Toleranzprozentsatz für Rechnungssummen angegeben ist, wird der Rechnungssummentoleranz-Prozentsatz verwendet, der für die juristische Person auf der Seite **Kreditorenkonten-Parameter** angegeben ist.

1. Sie können für einzelne Kreditoren Toleranzen festlegen, die die Standardtoleranz überschreiben. Wählen Sie dazu **Kreditoren-Konto**.
2. Hier können Sie den Prozentsatz der Abweichung eingeben, der für diesen Kreditor akzeptiert wird.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]