--- 
title: "Einrichten der Kreditorenrechnungs-Abgleichüberprüfung"
description: "Für diese Erfassung wird das Demo-Unternehmen USMF verwendet."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7a26a057b524f162e4b288b88e8c30f7c5db7a45
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Einrichten der Kreditorenrechnungs-Abgleichüberprüfung

[!include [task guide banner](../../includes/task-guide-banner.md)]

Für diese Erfassung wird das Demo-Unternehmen USMF verwendet. Die Kreditorenleiter- oder Buchhaltungsleiterrolle würde diese Schritte ausführen. Stellen Sie zu Beginn sicher, dass der Konfigurationsschlüssel "Rechnungsabgleich" ausgewählt wurde. Stellen Sie sicher, dass der Konfigurationsschlüssel "Belastungen" ausgewählt ist, wenn von der juristischen Person Belastungen zur Nachverfolgung von Ausgaben (wie z. B. Fracht) verwendet werden.  Beim Kreditorenrechnungsabgleich handelt es sich um den Prozess zum Abgleich der Informationen aus der Kreditorenrechnung, der Bestellung und des Produktzugangs. Unterschiede zwischen diesen Dokumenten werden als Abgleichsabweichung bezeichnet. Abgleichsabweichungen werden mit den angegebenen Toleranzen verglichen. Übersteigt die Abgleichsabweichung den Toleranzprozentsatz oder -betrag, werden in den Formularen "Kreditorenrechnung" und im Formular "Details zum Rechnungsabgleich" Abweichungssymbole angezeigt.

1. Wechseln Sie zu Kreditoren > Einstellung > Kreditorenparameter.
2. Klicken Sie auf die Registerkarte "Rechnungsprüfung".
3. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Rechnungsabgleichüberprüfung aktivieren".
    * Wählen Sie aus, ob zum Buchen einer Rechnung mit Abweichungen beim Rechnungsabgleich eine Genehmigung erforderlich sein soll. Wenn dazu "Mit Warnung zulassen" festgelegt ist, wird ein visueller Hinweis angezeigt, wenn eine Abweichung beim Rechnungsabgleich die Toleranz übersteigt. Sie sind jedoch dazu in der Lage, die Rechnung zu buchen. Um Workflows zusammen mit der Rechnungsabgleichsüberprüfung zu verwenden, stellen Sie sicher, dass das Feld "Rechnung mit Abweichungen buchen" auf "Mit Warnung zulassen" festgelegt ist, um zu vermeiden, dass Sie mehrmals genehmigen müssen.  
    * Wählen Sie im Feld "Rechnungskopf-Abgleichstatus automatisch aktualisieren" aus, ob der Abgleich während der Rechnungsdateneingabe automatisch vom System ausgeführt wird. Die empfohlene Einstellung ist "Ja", es sei denn, Sie haben Probleme bei der Dateneingabeleistung. Das Deaktivieren der automatischen Aktualisierungen ermöglicht möglicherweise eine schnellere Systemleistung, da die Rechnungsabgleichüberprüfung während der Dateneingabe umgangen wird. Der Dateneingabesekretär muss den Abgleichungsstatus der Rechnung manuell aktualisieren, um die Rechnungsabgleich-Überprüfergebnisse anzuzeigen, wenn dieser auf "Nein" festgelegt ist.  
4. Schalten Sie die Erweiterung des Abschnitts "Rechnungssummenabgleich" ein/aus.
5. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen "Rechnungssummen abgleichen", um die tatsächlichen Rechnungssummen mit den erwarteten Summen abzugleichen.
    * Wählen Sie aus, ob ein Symbol angezeigt werden soll, wenn eine Abweichung beim Rechnungsabgleich die Toleranz übersteigt. Das Symbol kann angezeigt werden, wenn eine positive Abweichung die Toleranz übersteigt oder wenn entweder eine positive oder negative Abweichung die Toleranz übersteigt.  
    * Beispiel: Der Toleranzprozentsatz ist 5 %, und der Gesamtrechnungsbetrag in der Bestellung beträgt 100,00. Folglich wird ein Preisabgleichsymbol angezeigt, wenn der Gesamtbetrag der Rechnung 105,00 übersteigt. Wenn Sie "Wenn größer oder kleiner als Toleranz" auswählen, wird das Symbol auch angezeigt, wenn der Rechnungsbetrag niedriger ist als 95,00.  
6. Geben Sie im Feld "Rechnungssummentoleranz in Prozent" eine Zahl ein.
7. Schalten Sie die Erweiterung des Abschnitts "Preis- und Mengenabgleich" ein/aus.
    * Wählen Sie im Feld "Positionsabgleichsrichtlinie" einen Wert aus, der als Standardrichtlinie für die juristische Person dienen soll, mit der Sie arbeiten. "Nicht erforderlich" bedeutet, dass keine Überprüfung von einzelnen Rechnungspositionspreisen gegenüber Bestellungspreisen oder Rechnungsmengen gegenüber Lieferscheinmengen erforderlich ist. "Zweiseitiger Abgleich" bedeutet, dass die Überprüfung von Rechnungspositionen erforderlich ist, aber nur die Bestellung und Rechnungsdokumente des Lieferanten sind an der Überprüfung beteiligt. Der Produktzugang wird bei den Abgleichüberprüfungen nicht berücksichtigt. "Dreiseitiger Abgleich" bedeutet, dass der Nettostückpreis der Rechnung mit dem Nettostückpreis der Bestellung verglichen wird und die entsprechende Produktzugangsmenge mit der Rechnungsmenge verglichen wird.  
    * Wenn Sie eine Positionsabgleichsrichtlinie mit "Zweiseitigem Abgleich" oder "Dreiseitigem Abgleich" verwenden, können Sie Preistoleranz-Prozentwerte für Ihre juristische Person, Artikel und Kreditoren auf der Seite "Artikelpreistoleranz" einrichten. Beim Vergleich von Kreditorenrechnungen mit Bestellinformationen in Bestellungen wird nach dem entsprechenden Preistoleranz-Prozentsatz gesucht.  
8. Wählen Sie im Feld "Positionsabgleichsrichtlinie" eine Option aus.
    * Wählen Sie im Feld "Überschreiben der Abgleichsrichtlinie zulassen" einen Wert, um zuzulassen, dass eine andere Abgleichsebene für einen Artikel, einen Händler sowie eine Kombination von Händler und Artikel oder Bestellposition angewendet wird. Die Positionsabgleichsrichtlinie für juristische Personen kann für einen speziellen Händler, Artikel oder eine spezielle Kombination von Händler und Artikel auf der Seite "Abgleichsrichtlinie" überschrieben werden.  
    * Wählen Sie einen Wert im Feld "Preissummen abgleichen" aus, um Preissummen für Rechnungspositionen abzugleichen. Dieser Abgleichstyp ist nützlich, wenn der Händler mehrere Rechnungen für die gleiche Bestellposition sendet. Sie können die Preisinformationen für den Nettobetrag der einzelnen Rechnungspositionen sowie alle ausstehenden und bereits gebuchten Rechnungspositionen mit den Nettobetrag der entsprechenden Bestellposition vergleichen.  
9. Wählen Sie im Feld "Preissummen abgleichen" eine Option aus.
10. Geben Sie im Feld "Toleranz für die Einkaufspreissumme" eine Zahl ein.
11. Schalten Sie die Erweiterung des Abschnitts "Abgleich von Belastungen" ein/aus.
12. Aktivieren Sie das Kontrollkästchen "Belastungen abgleichen", um basierend auf den Informationen zur Bestellung die tatsächlichen Belastungen mit den erwarteten Belastungen abzugleichen.
13. Schließen Sie die Seite.


