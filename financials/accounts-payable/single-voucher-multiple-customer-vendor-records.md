---
title: "Einzelner Beleg mit mehreren Debitoren- oder Kreditorendatensätzen"
description: "Dieses Thema bietet einen Überblick darüber, was geschieht, wenn Sie einen einzelnen Beleg mit mehreren Debitoren- und Kreditorendatensätzen buchen. Diese Funktionalität wird in künftigen Versionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, nicht mehr zur Verfügung stehen. Folglich empfehlen wir es nicht, diese Buchungsmethode zu verwenden, wegen der Buchhaltungsauswirkungen auf die Ausgleichsverarbeitung."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 31040ff14b99a9b351268feb88698ac706befb55
ms.contentlocale: de-de
ms.lasthandoff: 06/13/2017

---

# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Einzelner Beleg mit mehreren Debitoren- oder Kreditorendatensätzen

[!include[banner](../includes/banner.md)]


Dieses Thema bietet einen Überblick darüber, was geschieht, wenn Sie einen einzelnen Beleg mit mehreren Debitoren- und Kreditorendatensätzen buchen. Diese Funktionalität wird in künftigen Versionen von Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, nicht mehr zur Verfügung stehen. Folglich empfehlen wir es nicht, diese Buchungsmethode zu verwenden, wegen der Buchhaltungsauswirkungen auf die Ausgleichsverarbeitung. 

Einige allgemeine Beispiele, in denen ein Beleg für mehrere Debitoren oder Kreditoren verwendet wird, sind unter anderem Saldo-Übertragungen zwischen Debitoren und die Ermittlung des Nettowerts von Salden zwischen Debitoren und Kreditoren in derselben Organisation. 

Ein Beleg, der mehrere Debitoren oder Kreditoren enthält, kann mithilfe einer der folgenden Methoden eingegeben werden:

-   Verwenden einer Erfassung, bei der die Option **Nur eine Belegnummer** ausgewählt ist, sodass jede Position, die der Erfassung hinzugefügt wird, auf demselben Beleg enthalten ist.
-   Verwenden eines mehrzeiligen Belegs, bei dem es kein Gegensachkonto gibt, mit mehr als einem Debitor oder Kreditor.
-   Eingeben eines Belegs, wobei das Konto und Gegenkonto Kreditor/Kreditor, Debitor/Debitor, Kreditor/Debitor oder Debitor/Kreditor sind.

In diesem Thema wird gezeigt, wie Ausgleiche verarbeitet werden, wenn ein Beleg mit mehreren Debitoren oder Kreditoren gebucht wird. Darüber hinaus bietet dieses Thema Problemumgehungen, mit denen Sie verstehen, wie Sie es vermeiden können, einen Beleg mit mehreren Debitoren und Kreditoren zu verwenden. Insbesondere gibt es Beispiele, die zwei allgemeine Ausgleichsszenarien veranschaulichen, auf die sich die Verwendung eines Belegs mit mehreren Debitoren oder Kreditoren auswirkt:

-   Skontobuchhaltung
-   Neubewertungsbuchhaltung

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Wie wirkt sich der Ausgleich auf die Verwendung eines einzigen Belegs aus
Wenn Sie einen Beleg buchen, der mehrere Debitoren- oder Kreditorendatensätze enthält, wird ein einzelner Buchhaltungsbeleg erstellt, der mehrere Debitoren- oder Kreditorenkontensalden enthält. Während des Ausgleichsprozesses werden die ursprünglichen Buchhaltungseinträge verwendet, um Buchhaltungseinträge für das Skonto, nicht realisierte Gewinne und Verluste, realisierte Gewinne und Verluste und die Entlastung des Sammelkontos des Ausgangsdokuments zu erstellen. Wenn beispielsweise ein Skonto beim Ausgleichen einer Kreditorenzahlung zu einer Rechnung in Anspruch genommen wird, muss die Skontobuchhaltung von der ursprünglichen Rechnung zum Kreditorensachkonto buchen. Wenn die ursprüngliche Rechnung in einem Beleg gebucht wurde, der mehrere Kreditorendatensätze enthält, wird die ursprüngliche Buchhaltung zusammengefasst. Da es keine Zugriffsmöglichkeit auf den detaillierten Buchhaltungseintrag für jede Kreditorenbuchung im einzelnen Beleg gibt, gibt es in diesem Fall keine Möglichkeit zu bestimmen, wie der Benutzer den Skonto buchhalterisch berücksichtigen wollte.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Ein Beleg mit mehreren Kreditoren und die Auswirkungen auf die Skontobuchhaltung

Im folgenden Beispiel werden mehrere Kreditorenrechnungen im Hauptbuch auf einem einzelnen Beleg auf der Seite **Allgemeine Erfassung** erfasst. Diese Rechnungen werden über mehrere Kontodimensionen verteilt.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Beleg** | **Kontenart** | **Konto**  | **Beschreibung** | **Soll** | **Entlastung** |
| GNJL001     | Lieferant           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Lieferant           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Lieferant           | 1001         | INV3            |           | 300,00     |
| GNJL001     | Unternehmen           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Unternehmen           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Unternehmen           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Unternehmen           | 606300-004-- | INV3            | 300,00    |            |

Nach dem Buchen wird ein Beleg erstellt.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Beleg** | **Konto**  | **Buchungstyp** | **Betrag in Buchungswährung** |
| GNJL001     | 606300-001-- | Erstellte Journale   | 50,00                              |
| GNJL001     | 606300-002-- | Erstellte Journale   | 50,00                              |
| GNJL001     | 606300-003-- | Erstellte Journale   | 200,00                             |
| GNJL001     | 606300-004-- | Erstellte Journale   | 300,00                             |
| GNJL001     | 200110-001-  | Kreditorensaldo   | -100,00                            |
| GNJL001     | 200110-001-  | Kreditorensaldo   | -200.00                            |
| GNJL001     | 200110-001-  | Kreditorensaldo   | -300,00                            |

Beachten Sie, dass der Beleg drei Einträge für den Buchungstyp des Kreditorensaldos in dem einzelnen Beleg enthält. Es gibt keine Möglichkeit, um anzugeben, dass der Soll von 50,00 für 606300-001 und der Soll von 50,00 für 606300-002 dazu vorgesehen sind, den Kreditorensaldo von 200110-001 auszugleichen. Dies liegt daran, dass der Benutzer mehrere Kreditorendatensätze in einem einzelnen Beleg eingegeben hat.

Mithilfe dieses Beispiels können wir die Auswirkung der Verwendung eines Belegs auf die nachgelagerte Ausgleichsbuchhaltung analysieren. Angenommen, Sie zahlen 197,00 der Rechnung über 200,00, indem Sie einen Skonto von 3,00 % in Anspruch nehmen. Beachten Sie, dass der Skonto-Kontowert über alle Dimensionen von den Ausgabekonten des Rechnungsbelegs hinweg zugeteilt wird. Dies ist darauf zurückzuführen, dass ein Beleg verwendet wurde, um die obige Rechnung zu buchen, ohne einen Hinweis darauf, wie der Benutzer beabsichtigte, dass die Ausgabenverteilungen mit dem Kreditorensaldo in einem einzelnen Beleg korrelieren sollen.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Beleg** | **Konto**  | **Buchungstyp**     | **Soll** | **Entlastung** |
| APPAYM001   | 200110-001-  | Kreditorensaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bank                 |           | 197.00     |
| 14000056    | 520200-001-- | Kreditorenskonto |           | 0.25       |
| 14000056    | 520200-002-- | Kreditorenskonto |           | 0.25       |
| 14000056    | 520200-003-- | Kreditorenskonto |           | 1,00       |
| 14000056    | 520200-004-- | Kreditorenskonto |           | 1.50       |
| 14000056    | 200110-001-  | Kreditorensaldo       | 3,00      |            |

Wenn der Benutzer damit unzufrieden ist, dass der Skonto über alle Ausgabenverteilungen aus der ursprünglichen Rechnung hinweg zugeteilt wird, sollten anstelle eines Belegs mehrere Belege verwendet werden, um die Rechnungen zu erfassen. Das folgende Beispiel zeigt, wie mehrere Belege im Hauptbuch eingegeben werden können, anstatt einen Beleg zu verwenden, wie am Anfang dieses Beispiels angezeigt.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Beleg** | **Kontenart** | **Konto**  | **Beschreibung** | **Soll** | **Entlastung** | **Gegenbuchungstyp** | **Gegenkonto** |
| GNJL001     | Lieferant           | 1001         | INV1            |           | 100,00     | Unternehmen          | &lt;leer&gt;:      |
| GNJL001     | Unternehmen           | 606300-001-- | INV1            |   50,00   |            | Unternehmen          | &lt;leer&gt;:      |
| GNJL001     | Unternehmen           | 606300-002-- | INV1            |   50,00   |            | Unternehmen          | &lt;leer&gt;      |
| GNJL002     | Lieferant           | 1001         | INV2            |           | 200,00     | Unternehmen          | 606300-003--       |
| GNJL003     | Lieferant           | 1001         | INV3            |           | 300,00     | Unternehmen          | 606300-004--       |

Wenn jetzt INV2 bezahlt ist, wird der folgende Eintrag vorgenommen. Beachten Sie, dass die Finanzdimensionen des Skontos den Finanzdimensionen der zugeordneten Ausgaben folgen.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Beleg** | **Konto**  | **Buchungstyp**     | **Soll** | **Entlastung** |
| APPAYM001   | 200110-001-  | Kreditorensaldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Bank                 |           | 197.00     |
| 14000056    | 520200-003-- | Kreditorenskonto |           | 3,00       |
| 14000056    | 200110-001-  | Kreditorensaldo       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Ein Beleg mit mehreren Kreditoren und die Auswirkungen auf die Buchhaltung der realisierten Gewinne/Verluste

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Beleg** | **Kontenart** | **Konto** | **Beschreibung** | **Soll** | **Entlastung** | **Kontenart** | **Konto**  |
| GNJL001     | Lieferant           | 1001        | INV1            |           | 100,00     | Unternehmen           | 606300-001-- |
| GNJL001     | Lieferant           | 1001        | INV2            |           | 200,00     | Unternehmen           | 606300-002-- |

Im folgenden Beispiel werden mehrere Kreditorenrechnungen im Hauptbuch auf einem einzelnen Beleg auf der Seite **Allgemeine Erfassung** erfasst. Diese Rechnungen werden über mehrere Kontodimensionen verteilt. Nach dem Buchen wird ein Beleg erstellt.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Beleg** | **Konto**  | **Buchungstyp** | **Betrag in Buchungswährung (EUR)** | **Betrag in Buchhaltungswährung (USD)** |
| GNJL001     | 606300-001-- | Erstellte Journale   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Erstellte Journale   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Kreditorensaldo   | -100,00                                  | -114,00                                 |
| GNJL001     | 200110-001-  | Kreditorensaldo   | -200.00                                  | -228,00                                 |

Beachten Sie, dass der Beleg zwei Einträge für den Buchungstyp des Kreditorensaldos in dem einzelnen Beleg enthält. Es gibt keine Möglichkeit anzugeben, dass das Soll für 606300-001 den Kreditorensaldoeintrag von 100,00 zu 200110-001 ausgleichen soll. Dies liegt daran, dass der Benutzer mehrere Kreditorendatensätze in einem einzelnen Beleg eingegeben hat. 

Mithilfe dieses Beispiels können wir die Auswirkung der Verwendung eines Belegs auf die nachgelagerte Ausgleichsbuchhaltung analysieren. Nehmen wir an, dass die Buchhaltungswährung USD ist und die oben genannten Buchungen in der Buchungswährung EUR gebucht wurden. Nehmen wir an, dass Sie die Rechnung über 200,00 EUR vollständig bezahlen, Sie jedoch einen realisierten Verlust feststellen, aufgrund einer Differenz im Wechselkurs zwischen dem Zeitpunkt, an dem Sie die Rechnung gebucht haben und der Bezahlung. Beachten Sie, dass der Kontowert des realisierten Verlusts über alle Dimensionen von den Ausgabekonten des Rechnungsbelegs hinweg zugeteilt wird. In diesem Fall wurden sowohl die Dimension 001 als auch 002 zugeteilt, obwohl nach der Wahrnehmung des Benutzers möglicherweise nur 002 zum Ausgabenkonto der Rechnung gehört, die beglichen wird. Dies ist darauf zurückzuführen, dass ein Beleg verwendet wurde, um die obige Rechnung zu buchen, ohne einen Hinweis darauf zu hinterlassen, wie der Benutzer beabsichtigte, dass die Ausgabenverteilungen mit dem Kreditorensaldo in einem einzelnen Beleg korrelieren sollen.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Beleg** | **Konto** | **Buchungstyp**   | **Betrag in Buchungswährung (EUR)** | **Betrag in Buchhaltungswährung (USD)** |
| APPAYM001   | 200110-001- | Kreditorensaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bank               | -200.00                                  | -230,00                                 |
| 14000056    | 801300-001- | Kursverlust | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Kursverlust | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Kreditorensaldo     |                                          | -2,00                                   |

Wenn der Benutzer damit unzufrieden ist, dass der Wechselkursverlust über alle Ausgabenverteilungen aus der ursprünglichen Rechnung hinweg zugeteilt wird, sollten anstelle eines Belegs mehrere Belege verwendet werden, um die Rechnungen zu erfassen. Das folgende Beispiel zeigt, wie mehrere Belege im Hauptbuch eingegeben werden können, anstatt einen Beleg zu verwenden, wie am Anfang dieses Beispiels angezeigt.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Beleg** | **Kontenart** | **Konto** | **Beschreibung** | **Soll** | **Entlastung** | **Gegenbuchungstyp** | **Gegenkonto** |
| GNJL002     | Lieferant           | 1001        | INV1            |           | 100,00     | Unternehmen          | 606300-001--       |
| GNJL003     | Lieferant           | 1001        | INV2            |           | 200,00     | Unternehmen          | 606300-002--       |

Wenn jetzt INV2 bezahlt ist, wird der folgende Eintrag vorgenommen. Beachten Sie, dass die Finanzdimensionen des Wechselkursverlusts den Finanzdimensionen der zugeordneten Ausgaben folgen.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Beleg** | **Konto** | **Buchungstyp**   | **Betrag in Buchungswährung (EUR)** | **Betrag in Buchhaltungswährung (USD)** |
| APPAYM001   | 200110-001- | Kreditorensaldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Bank               | -200.00                                  | -230,00                                 |
| 14000056    | 801300-002- | Kursverlust | 0,00                                     | 2.00                                    |
| 14000056    | 200110-001- | Kreditorensaldo     |                                          | -2,00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Ein Beleg für Saldo-Übertragungen und Saldierungsszenarien
Zwei häufig verwendete Szenarien, die einen Beleg verwenden, der mehrere Debitoren oder Kreditoren enthält, umfassen Saldo-Übertragungen von einem Debitor/Kreditor zu einem anderen Debitor/Kreditor sowie die Saldierung eines Debitors und Kreditors, die dieselbe Organisation sind. In den folgenden beiden Beispielen wird die bevorzugte Methode zum Eingeben dieser Szenarien in Finance and Operations als Alternative zum Eingeben in einen Beleg gezeigt. 

Eine *Saldo-Übertragung* ist ein Beleg mit mehreren Debitoren, die zum Zweck der Übertragung des Saldos von einem Debitor an einen anderen Debitor (Gleiches gilt für Kreditoren) eingegeben werden. Dieses Szenario kann auftreten, wenn die Zuständigkeit für die Zahlung der Rechnung an eine andere Partei übergeht, beispielsweise wenn ein Tochterunternehmen die Zuständigkeit auf das Mutterunternehmen verlagert. 

Dieses Beispiel geht von einem Verkauf aus, bei welchem dem Debitor ein Skonto zusteht, wenn die Zahlung innerhalb von 10 Tagen erfolgt. Der Debitor in diesem Beispiel verwendet ein Versicherungsunternehmen, das für die Bezahlung der Rechnung verantwortlich ist. Das Versicherungsunternehmen wird als zweiter Debitor im System eingerichtet. Der Saldo des ursprünglichen Debitors wird an das Versicherungsunternehmen übertragen, das die Rechnung bezahlt und dabei für die Bezahlung innerhalb der Rabattperiode ein Skonto von 2% in Anspruch nimmt. 

Zur Veranschaulichung gehen wir davon aus, dass der folgende Verkauf an den Debitor ACME erfolgt. Die folgenden Buchhaltungseinträge stellen den Verkauf dar.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Sachkonto** | **Buchungstyp** | **Soll** | **Entlastung** |
| 401100-002-023-    | Umsatzerlös          |           | 100        |
| 130100-002-        | Debitorensaldo | 100       |            |

Als Nächstes überträgt der Benutzer den fälligen Saldo von ACME an das Versicherungsunternehmen in einem Beleg in der Debitoren-Zahlungserfassung. In Finance and Operations ist das Versicherungsunternehmen als Debitor eingerichtet.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Beleg** | **Kontenart** | **Konto** | **Beschreibung** | **Soll** | **Entlastung** | **Gegenbuchungstyp** | **Gegenkonto** |
| ARPAYM001   | Kunde         | ACME        | Übertragen        |           | 100,00     | Kunde        | Versicherung          |

Beachten Sie, dass der oben genannte Eintrag in einem Belegs enthalten ist. Dieser Beleg beinhaltet zwei Debitorendatensätze. Der folgende Beleg wird erstellt, wenn der oben genannte Hauptbucheintrag gebucht wird.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Beleg** | **Konto** | **Buchungstyp** | **Betrag in Buchungswährung** |
| ARPAYM001   | 130100-002- | Debitorensaldo | 100,00                             |
| ARPAYM001   | 130100-002- | Debitorensaldo | -100,00                            |

Danach nehmen wir an, dass Sie eine Zahlung vom Versicherungsdebitor über 98,00 empfangen und Sie auswählen, ob die Zahlung mit der durch die Saldo-Übertragung erstellten Rechnung beglichen werden soll. Dies führt zum Buchen des folgenden Belegs. Es gibt möglicherweise die Erwartung, dass der Ausgleich die Finanzdimensionen aus der ursprünglichen Rechnung verwendet, aber das ist nicht möglich, weil es kein Rechnungsdokument für den Versicherungsdebitor gibt. Beachten Sie, dass standardmäßig die Verteilungsdimensionen zum Skonto von der Debitorenbuchung stammen, die aus der Übertragung erstellt wurde, nicht vom Umsatzerlöskonto der ursprünglichen Rechnung. Der Standard ist ein Ergebnis der Verwendung eines Belegs zum Übertragen der Salden.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Beleg** | **Konto** | **Buchungstyp** | **Soll** | **Entlastung** |
| ARPAYM002   | 110110-002- | Bank             | 98.00     |            |
| ARPAYM002   | 130100-002- | Debitorensaldo |           | 98.00      |

Im zugehörigen Beleg für das Skonto kommt der Standard für die Finanzdimension aus der Debitorenbuchung, die aus der Übertragung erstellt wird, da die Übertragung mehr als einen Debitor hat.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Beleg** | **Konto** | **Buchungstyp**       | **Soll** | **Entlastung** |
| ARP-00001   | 403300-002- | Debitorenskonto | 2.00      |            |
| ARP-00001   | 130100-002- | Debitorensaldo       |           | 2.00       |

Wenn der Benutzer mit dem Standard für die Finanzdimensionen für den Skonto nicht zufrieden ist, sollten anstelle eines Belegs mehrere Belege verwendet werden, um die Saldo-Übertragung zu erfassen. Dieses Szenario sollte ausgeführt werden, indem eine Gutschrift für den Debitor erstellt wird, VON dem der Saldo verschoben wurde und eine Lastschrift oder Rechnung für den Debitor erstellt wurde, ZU dem der Saldo verschoben wurde. Das folgende Beispiel zeigt, wie mehrere Belege in die Debitorenzahlungserfassung eingegeben werden können, um den Saldo zu übertragen, anstatt einen Beleg zu verwenden, wie weiter oben in diesem Beispiel gezeigt.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Beleg** | **Kontenart** | **Konto** | **Beschreibung** | **Soll** | **Entlastung** | **Gegenbuchungstyp** | **Gegenkonto** |
| ARPAYM001   | Kunde         | ACME        |                 |           | 100,00     | Unternehmen          | 401100-002-023-    |
| ARPAYM002   | Kunde         | Versicherung   |                 | 100,00    |            | Unternehmen          | 401100-002-023-    |

Das bedeutet, dass wenn der Versicherungsdebitor 98,00 mit dem Beleg ARPAYM02 bezahlt, die korrekten Finanzdimensionen aus dem Sachkontoeintrag des Belegs ARPAYM002 verwendet werden.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Beleg** | **Konto** | **Buchungstyp** | **Soll** | **Entlastung** |
| ARPAYM003   | 110110-002- | Bank             | 98.00     |            |
| ARPAYM003   | 130100-002  | Debitorensaldo |           | 98.00      |

Im zugehörigen Beleg für den Skonto werden die Finanzdimensionen aus dem ausgleichenden Umsatzerlöskonto verwendet, das auf dem Beleg von ARPAYM002 angezeigt wird.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Beleg** | **Konto**     | **Buchungstyp**       | **Soll** | **Entlastung** |
| ARP-00001   | 403300-002-023- | Debitorenskonto | 2.00      |            |
| ARP-00001   | 130100-002-     | Debitorensaldo       |           | 2.00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Ein Beleg mit einer Saldierung für mehrere Debitoren und Kreditoren
Die Saldierung kann nützlich sein, wenn eine Organisation beim selben Unternehmen einkauft, an das es auch verkauft. Anstatt die Kreditorenrechnungen zu bezahlen und auf den Empfang der Zahlung für die Debitorenrechnungen zu warten, werden die Kreditoren- und Debitorenrechnungen saldiert. Die Saldierungsbuchung wird gegenüber den ausstehenden Salden ausgeglichen. 

Um es zu veranschaulichen, nehmen wir an, dass es sich bei Kreditor 1001 und Debitor US-008 um dieselbe Entität handelt. Ihre Organisation möchte also die Kreditoren- und Debitorensalden saldieren, bevor der verbleibende Saldo bezahlt/empfangen wird. Nehmen wir also an, dass der Kundendatensatz 75,00 EUR schuldet und dem Kreditorendatensatz 100,00 EUR geschuldet wird. Das bedeutet, dass Sie es bevorzugen würden, die Salden auszugleichen und nur dem Kreditor 25,00 EUR zu bezahlen. Nehmen Sie weiterhin an, dass die Buchhaltungswährung USD ist. In diesem Fall wird eine Saldierungsbuchung in einen Beleg in der Kreditoren-Zahlungserfassung eingegeben.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Beleg** | **Kontenart** | **Konto** | **Beschreibung** | **Soll** | **Entlastung** | **Gegenbuchungstyp** | **Gegenkonto** |
| APPAYM001   | Lieferant           | 1001        | Saldierung         |  75,00    |            | Kunde        | US-008             |

Um unerwünschte Probleme bei zukünftigen Ausgleichen für diese Buchung zu vermeiden, sollten anstatt eines Belegs mehrere Belege in die Erfassung zur Aufzeichnung der Saldierungsbuchungen eingegeben werden. Beachten Sie, dass die Debitoren- und Kreditorensalden mit einem einzigen Verrechnungskonto ausgeglichen werden, um die Verwendung eines Belegs zu vermeiden, der mehrere Debitoren- und Kreditorensalden enthält.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Beleg** | **Kontenart** | **Konto** | **Beschreibung** | **Soll** | **Entlastung** | **Gegenbuchungstyp** | **Gegenkonto** |
| 001         | Kunde         | US-008      |                 |           |  75,00     | Unternehmen          | 999999---          |
| 002         | Lieferant           | 1001        |                 |  75,00    |            | Unternehmen          | 999999---          |

 




