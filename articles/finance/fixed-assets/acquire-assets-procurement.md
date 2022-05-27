---
title: Erwerben von Anlagen durch Beschaffung
description: Dieser Artikel beschreibt, wie eine Integration zwischen den Modulen "Anlagevermögen" und "Kreditoren" eingerichtet wird. Dadurch können Anlagen automatisch auf Grundlage von Bestellungen oder Kreditorenrechnungen erstellt oder Anschaffungs- und Anschaffungsänderungsbuchungen für Anlagen automatisch vorgenommen werden.
author: moaamer
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b654dbf97f8d91e0a3233803ee182b1383ad317d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712089"
---
# <a name="acquire-assets-through-procurement"></a>Erwerben von Anlagen durch Beschaffung

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt, wie eine Integration zwischen den Modulen "Anlagevermögen" und "Kreditoren" eingerichtet wird. Dadurch können Anlagen automatisch auf Grundlage von Bestellungen oder Kreditorenrechnungen erstellt oder Anschaffungs- und Anschaffungsänderungsbuchungen für Anlagen automatisch vorgenommen werden. Eine Einkaufsposition erstellt eine Anlage, unabhängig von der Menge auf der Einkaufsposition. Wenn Sie mehrere Anlagen erstellen müssen, müssen Sie mehrere Einkaufspositionen erstellen.

 Für die Integration von Anlagen und Kreditoren stehen die folgenden Methoden zur Verfügung. Dabei muss für alle Anlagen die gleiche Methode verwendet werden:
-   Sie erstellen manuell eine Anlage, bevor Sie die Anlagennummer der Position in der Bestellung oder Kreditorenrechnung hinzufügen. Beim Buchen der Kreditorenrechnung erfolgt für die Anlage automatisch eine Anschaffungsbuchung. Dies ist die Standardmethode.
-   Sie erstellen manuell eine Anlage, bevor Sie die Anlagennummer der Position in der Bestellung oder Kreditorenrechnung hinzufügen. Beim Buchen der Kreditorenrechnung erfolgt keine Anschaffungsbuchung für die Anlage.
-   Eine Anlage wird automatisch erstellt, wenn Sie einen Produktzugang oder eine Kreditorenrechnung mit aktiviertem Kontrollkästchen "Neue Anlage erstellen" buchen. Beim Buchen der Kreditorenrechnung erfolgt für die Anlage automatisch eine Anschaffungsbuchung.
-   Eine Anlage wird automatisch erstellt, wenn Sie einen Produktzugang oder eine Kreditorenrechnung mit aktiviertem Kontrollkästchen "Neue Anlage erstellen" buchen. Beim Buchen der Kreditorenrechnung erfolgt keine Anschaffungsbuchung für die Anlage.

Verwenden Sie eine der ersten beiden Methoden, wenn Sie Anlagen manuell erstellen möchten, und weisen Sie anschließend die Anlagennummer der Bestellung oder Kreditorenrechnung zu. Wählen Sie eine der letzten beiden Methoden aus, wenn Sie eine flexiblere Vorgehensweise bevorzugen: Dadurch können Sie neue Anlagen je nach Situation entweder manuell oder automatisch (auf Basis der Anlageninformationen aus den Positionsartikeldetails) erstellen. 

Unabhängig davon, ob Sie Anlagen manuell erstellen oder einen flexibleren Ansatz verwenden, muss auch festgelegt werden, ob eine Anschaffungsbuchung nur im Modul "Anlagevermögen" oder beim Buchen einer Kreditorenrechnung ausgeführt werden kann. In manchen Organisationen wird als bevorzugte Vorgehensweise die manuelle Erstellung von Anschaffungen und Anschaffungsbuchungen im Modul "Anlagevermögen" mithilfe manueller Journaleinträge oder Vorschläge verwendet. 

In diesem Thema werden die Details der einzelnen Methoden erläutert.

## <a name="methods-for-manually-creating-fixed-assets"></a>Methoden zum manuellen Erstellen von Anlagen
Beim Buchen einer Kreditorenrechnung, deren Positionen eine Anlagennummer enthalten, wenn die Option "Anlagenanschaffung aus Einkauf zulassen" auf der Seite "Anlagenparameter" ausgewählt ist, wird die Anschaffung automatisch gebucht und der Status der Anlage ändert sich in "Offen". 

Sollte eine Anschaffung nicht gebucht werden können, kann entweder im Modul "Anlagen" manuell eine Anschaffungstransaktion eingegeben oder in der Erfassung "Anlagen" ein Anschaffungsvorschlag zum gleichzeitigen Erstellen mehrerer Anschaffungstransaktionen verwendet werden.

> [!NOTE]                                                                                                                              
> Ist die Ausführung von Anschaffungsbuchungen durch die Einstellungen des Moduls "Anlagevermögen" auf eine bestimmte Benutzergruppe beschränkt, müssen Sie zum Ausführen rechnungsbasierter Anschaffungsbuchungen Mitglied dieser Benutzergruppe sein.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Methoden zum automatischen Erstellen von Anlagen
Beim Buchen eines Produktzugangs, bei dem für eine Position die Option "Neue Anlage erstellen" aktiviert ist, wird eine neue Anlage mit dem Status "Noch nicht erworben" erstellt. Wird anschließend eine Kreditorenrechnung mit einer neuen Anlage gebucht, wird eine Anschaffungstransaktion für die neue Anlage gebucht, und der Status der Anlage ändert sich in "Offen", sofern "Anlagen" so konfiguriert ist, dass Anlagenanschaffungen über "Kreditoren" zulässig sind, und Sie Mitglied einer Benutzergruppe sind, die Anschaffungstransaktionen buchen kann. 

Wurde die Option "Neue Anlage?" in der Bestellposition nicht beim Buchen des Produktzugangs, aber beim Buchen der Kreditorenrechnung ausgewählt, wird die neue Anlage mit dem Status "Offen" erstellt und angeschafft, sofern "Anlagen" so eingerichtet ist, dass die Erstellung und Anschaffung zulässig ist. Wurde beim Buchen des Produktzugangs bereits eine Anlage erstellt, wird beim Buchen einer Kreditorenrechnung keine zusätzliche Anlage erstellt.

### <a name="capitalization-threshold"></a>Aktivierungsschwellenwert

Bei Verwendung einer Methode mit automatischer Erstellung und Anschaffung der Anlage kann vom System überprüft werden, ob der Einkaufsbetrag der Anlage einem angegebenen Aktivierungsschwellenwert für die Anlagenabschreibung entspricht. Ist dies der Fall die Option "Abschreibung" in den Büchern für die Anlage ausgewählt, wenn sie aus "Kreditorenkonto" erstellt wird. 

Bei einem Aktivierungsschwellenwert handelt es sich um einen Währungsbetrag, durch den bestimmt wird, ob Anlagen bei Erreichen des angegebenen Betrags abgeschrieben werden. Wird beispielsweise eine Anlage erworben, deren Einkaufspreis unter dem Aktivierungsschwellenwert liegt, wird die Anlage nicht für die Abschreibung vorgesehen. Entspricht der Einkaufspreis dagegen mindestens dem Schwellenwert, wird die Anlage zur Abschreibung vorgemerkt. 

Sie können den Aktivierungsschwellenwert auf der Seite "Anlagengruppen" einrichten.

## <a name="scenario"></a>Szenario
Im folgenden Szenario wird der vollständige Zyklus einer Anlagen- und Kreditorenintegration erläutert. Hier finden Sie Beispieleinstellungen sowie Informationen zu Anschaffungsvorschlägen. 

Für dieses Szenario ist das System folgendermaßen konfiguriert:

-   Anlagen werden automatisch beim Buchen von Produktzugängen oder Kreditorenrechnungen erstellt, das Modul "Anlagevermögen" ist jedoch so konfiguriert, dass die Ausführung von Anschaffungsbuchungen im Modul "Kreditoren" nicht zulässig ist.
-   Konten werden im Feld "Kontotyp" für die Kontentypen "Anlagenzugang" und "Anlagenabgang" auf der Seite "Artikelgruppen" angegeben.
-   Der Aktivierungsschwellenwert für die Computergruppe (COMP) ist auf 1500 festgelegt.
-   Ihre Aufgabe besteht darin, eine Bestellung für einen neuen Laptop für einen Mitarbeiter einzugeben. Anschließend muss die Bestellung gebucht und überprüft werden, ob vom Sachbearbeiter im Versand ein Produktzugang gebucht wurde. Danach muss die Kreditorenrechnung gebucht und überprüft werden, ob die Anlage "Laptop" vom Buchhalter auf den Status "Offen" aktualisiert wurde.

Verwenden Sie zunächst die Seite "Bestellung", um Details zum Laptop einzugeben, für den Kosten in Höhe von 1.600 EUR anfallen. Sie wählen Die Option "Neue Anlage?" auf dem Inforegister "Anlagen" der Bestellpositionen aus, wählen COMP als Anlagengruppe aus und speichern die Bestellung. 

Nach Eingang des Laptops wird von einem Sachbearbeiter im Versand ein Produktzugang eingegeben und gebucht, um den Eingang des Laptops zu erfassen. Die Anlage "Laptop" wird erstellt und hat den Status "Noch nicht erworben". Der Betrag übersteigt den Aktivierungsschwellenwert. Aus diesem Grund wird die Option "Abschreibung" in den Büchern für die Anlage "Laptop" ausgewählt. Die folgenden Buchungen wurden ausgeführt.

| Beschreibung                               | Konto             | Soll    | Haben   |
|-------------------------------------------|---------------------|----------|----------|
| Einkauf, Produktzugang (Einkauf)        | Nicht fakturierte Zugänge | 1600,00 |          |
| Einkauf, Produktzugang - Gegenkonto | Antizipierte Einkäufe   |          | 1600,00 |

Als Nächstes wird die Kreditorenrechnung für den Laptop gebucht. Der Status des Laptops ändert sich nicht, da das Modul "Anlagevermögen" so konfiguriert ist, dass beim Buchen einer Kreditorenrechnung keine Anlagenanschaffungsbuchungen ausgeführt werden. Die Option "Neue Anlage erstellen" wurde ausgewählt, als die Kreditorenrechnung gebucht wurde. Daher wurde das Zugangskonto "Anlage" verwendet. Das Abgangskonto "Anlage" wurde nicht verwendet, weil keine Anschaffung gebucht wurde. Dieses Konto wird später verwendet, wenn der Buchhalter der Organisation mithilfe von Anschaffungsvorschlägen eine Anschaffungstransaktion in "Anlagen" bucht. 

Die folgenden Buchungen wurden ausgeführt.

| Beschreibung                               | Konto             | Soll    | Haben   |
|-------------------------------------------|---------------------|----------|----------|
| Einkauf, Produktzugang - Gegenkonto | Antizipierte Einkäufe   | 1600,00 |          |
| Kreditorensaldo                            | Kreditoren    |          | 1600,00 |
| Einkauf, Anlagenzugang             | Computerausgabe    | 1600,00 |          |
| Einkauf, Produktzugang (Einkauf)        | Nicht fakturierte Zugänge |          | 1600,00 |

Zum Schluss überprüft der Buchhalter alle Anlagen mit dem Status "Noch nicht erworben". Daher wird auch die neue Anlage "Laptop" überprüft. Der Buchhalter öffnet anschließend über die Erfassungspositionen "Anlagen" die Seite Anschaffungsvorschläge" und erstellt Anschaffungstransaktionen für alle Anlagen, für die zwar eine Rechnung vorhanden ist, die aber noch den Status "Noch nicht erworben" besitzen. Nach dem Buchen der Erfassung ändert sich der Status der Anlage "Laptop" in "Offen". Für das Abgangskonto "Anlage" erfolgt eine Habenbuchung und für das Anlagenanschaffungskonto erfolgt eine Sollbuchung. 

Im Folgenden finden Sie Variationen dieses Szenarios:

-   Ist aufgrund der Einstellungen des Moduls "Anlagevermögen" beim Buchen von Kreditorenrechnungen die Ausführung von Anlagenanschaffungsbuchungen zulässig, muss der Buchhalter nicht auf Anschaffungsvorschläge im Modul "Anlagevermögen" zurückgreifen, da die Anschaffungsbuchung erstellt wird. Zudem werden beim Buchen der Kreditorenrechnung verschiedene Konten aktualisiert. Anstelle der Ausgaben "Computer" erfolgt für das Lagerkonto "Anlagenzugang" eine Sollbuchung und zwei zusätzliche Transaktionen finden statt: Für das Anlagenanschaffungskonto erfolgt eine Sollbuchung und für das Lagerkonto "Anlagenzugang" erfolgt eine Habenbuchung.
-   Ist die Option "Neue Anlage erstellen" beim Buchen des Produktzugangs nicht ausgewählt, wird zu dem Zeitpunkt keine Anlage erstellt. Wenn Sie die Option "Neue Anlage erstellen" vor dem Buchen der Kreditorenrechnung auswählen, wird die Anlage mit dem Status "Noch nicht erworben" erstellt. Werden beim Buchen von Kreditorenrechnungen auch Anschaffungstransaktionen gebucht, wird die Anlage mit dem Status "Offen" erstellt.
-   Betragen die Kosten für den Laptop nicht EUR 1600, sondern EUR 1400, wird der Aktualisierungsschwellenwert nicht erreicht. Daher wird die Anlage erstellt und die Option "Abschreibung" wird deaktiviert.
-   Wenn ein Rechnungsbuch verwendet wird, verwenden Sie die Erfassungsseite "Rechnungsgenehmigung", nachdem das Rechnungsbuch gebucht wurde, um den Beleg abzurufen, Sie verknüpfen die Bestellung mit der Kreditorenrechnung, wählen die Option "Neue Anlage erstellen" aus und buchen dann die Kreditorenrechnung. Sollten Sie Mitglied einer Benutzergruppe sein, die zum Erstellen von Anschaffungstransaktionen berechtigt ist, wird die Anschaffung erstellt, und die Anlage erhält den Status "Offen".
-   Geht nur eine Teilmenge ein, wird für die erste Kreditorenrechnung aufgrund der Benutzergruppeneinschränkungen keine Anlagenanschaffung erstellt. Eine Anschaffung für die zweite Kreditorenrechnung, durch die die bestellte Menge komplettiert wird, kann nur gebucht werden, wenn bereits für die erste Kreditorenrechnung eine Anschaffungsbuchung eingegeben wurde und Sie Mitglied einer Benutzergruppe sind, die zum Buchen von Anschaffungen berechtigt ist.


Weitere Informationen finden Sie unter [Anlage-Integration](fixed-asset-integration.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
