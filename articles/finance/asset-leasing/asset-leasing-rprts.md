---
title: Anlagenleasing-Berichte
description: In diesem Thema werden die im Analgenleasing verfügbaren Berichte aufgelistet und kurz beschrieben.
author: moaamer
manager: Ann Beebe
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ab55d778f55c3ec96141c4f868724af1e11aed09
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229573"
---
# <a name="asset-leasing-reports"></a>Anlagenleasing-Berichte

[!include [banner](../includes/banner.md)]

In diesem Thema werden die im Analgenleasing verfügbaren Berichte aufgelistet und kurz beschrieben. Die meisten Berichte werden angezeigt, indem diese oder ähnliche Schritte ausgeführt werden, wie angegeben). 

- Um die meisten Analgenleasing-Berichte anzuzeigen, gehen Sie zu **Anlagenleasing > Anfragen und Berichte > Leasingberichte** und wählen Sie dann einen Bericht zum Anzeigen aus. Für die Berichte, für die ein anderer Auswahlpfad erforderlich ist, sind die Schritte zum Öffnen des Berichts in der Beschreibung dieses Berichts enthalten. 
- Wenn Sie einen zu druckenden Bericht auswählen, wird eine Parameterseite geöffnet, auf der Sie die im Bericht enthaltenen Informationen filtern können. Geben Sie Filterkriterien ein und wählen Sie dann **OK**, um den Bericht zu generieren. Der generierte Bericht zeigt Informationen an, die zu den von Ihnen angegebenen Filter passen.

## <a name="asset-movement"></a>Anlagenbewegung
Der Bericht über die Umlagerung von Vermögenswerten dient als fortlaufender Bericht für das Nutzungsrecht am Leasingobjekt für jeden Mietvertrag. Mit diesem Bericht können Sie die Anlagentransaktionen eines Mietvertrags während eines bestimmten Zeitraums anzeigen. Der Bericht enthält die folgenden Felder. 

|     Berichtsfelder                  |     Beschreibung                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Anfangsdatum              |     Das Startdatum der frühesten Version des Mietvertrags.                     |   
|     Mietdauer                     |     Die Mietdauer der frühesten Version des Mietvertrags.                            |
|     Kurzfristiger Mietvertrag               |     Wenn der Mietvertrag als kurzfristiger Mietvertrag eingestuft ist, wird **Ja** angezeigt.         |
|     Leasingobjekt von geringem Wert                |     Wenn der Mietvertrag als ein Mietobjekt von geringem Wert eingestuft ist, wird **Ja** angezeigt.          |
|     Anfängliches Nutzungsrecht am Leasingobjekt     |     Der ursprüngliche Wert des Nutzungsrechts am Mietobjekt aus dem Journaleintrag der erstmaligen Erfassung.      |
|     Anfangssaldo              |     Der Nettobuchwert des Nutzungsrechtsvermögens zum **Startdatum**.                         |
|     Abschreibungsausgaben der Periode    |     Die Höhe des Abschreibungsaufwands innerhalb des für den Bericht festgelegten Datumsbereichs.        |
|     Kumulierte Abschreibung       |     Die Höhe der kumulierten Abschreibungen zum **Startdatum**.                               |
|     Dauerhafte Wertminderung                     |     Der Betrag, um den die Anlage innerhalb des für den Bericht festgelegten Datumsbereichs gemindert wurde.               |
|     Änderungen                  |     Die Anzahl der Anpassungen des Nutzungsrechts zwischen den Datumsparametern.                            |
|     Nettobuchwert                 |     Der endgültige Nettobuchwert des Nutzungsrechtsvermögens, der der Nettobetrag der kumulierten Abschreibungen zum **Enddatum** ist.    |

## <a name="differences-report"></a>Bericht zu Unterschieden
Der Bericht „Unterschiede“ zeigt die Unterschiede zwischen Informationen, die in das Mietvertrag-Import-Framework geladen wurden, und den Informationen, die derzeit im System vorhanden sind. Auf diese Weise können Sie vergleichen, was über das Mietvertrags-Import-Framework angepasst, aktualisiert oder hinzugefügt wurde.  

Die Werte im Bericht variieren je nach ausgewähltem Mietvertrag. Der Bericht zeigt nur die Felder an, die sich von den aktuellen im System und den Staging-Tabellen unterscheiden. Der alte Wert ist der aktuelle Wert im System oder der vorherige Wert im System, je nachdem, ob der Importvorgang ausgeführt wurde. Der neue Wert zeigt den Wert in der Staging-Tabelle an, der den alten Wert ersetzt.

## <a name="five-years-undiscounted-payment-forecast"></a>Nicht diskontierte Zahlungsplanung für fünf Jahre
Der Prognosebericht für fünf Jahre nicht diskontierte Zahlungen zeigt die prognostizierten nicht diskontierten Mietzahlungen, die in den Nächsten fünf Jahren ab dem in den Berichtsparametern angegebenen Datum zu zahlen sind. Der Bericht enthält die folgenden Felder. 

|     Berichtsfelder         |     Beschreibung                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Beschreibung des Mietvertrags     |     Die Beschreibung des Mietvertrags aus dem Header des Mietvertrags.                                                      |
|     Mietvertragskennung              |     Die eindeutige Mietvertragskennung.                                                                              |
|     Buch                  |     Das der Buch-ID zugeordnete Leasingbuch.                                                         |
|     Kostenklassifizierung        |     Die Klassifizierung des Mietvertrags.                                                                  |
|     Buchungsebene         |     Die Ebene, auf der dieser Mietvertrag gebucht wird.                                                         |
|     Währung              |     Die Währung des Mietvertrags.                                                                        |
|     Aktuell               |     Die Summe aller Mietzahlungen, die innerhalb der nächsten 12 Monate ab dem Bilanzstichtag zu zahlen sind.          |
|     13–24 Monate          |     Die Summe aller Mietzahlungen, die innerhalb der nächsten 13 und 24 Monate ab dem Bilanzstichtag zu zahlen sind.           |
|     25–36 Monate          |     Die Summe aller Mietzahlungen, die innerhalb der nächsten 25 und 36 Monate ab dem Bilanzstichtag zu zahlen sind.           |
|     37–48 Monate          |     Die Summe aller Mietzahlungen, die innerhalb der nächsten 37 und 48 Monate ab dem Bilanzstichtag zu zahlen sind.           |
|     49–60 Monate          |     Die Summe aller Mietzahlungen, die innerhalb der nächsten 49 und 60 Monate ab dem Bilanzstichtag zu zahlen sind.           |
|     Danach            |     Die Summe aller Mietzahlungen, die ab dem 61 Monat ab dem Bilanzstichtag zu zahlen sind.              |

## <a name="gaap-cash-flows-report"></a>GAAP-Cashflow-Bericht
Der GAAP-Offenlegungsbericht erfüllt die in 842-20-50-4 (g) (1) angegebene US-GAAP-Offenlegungspflicht. Um diesen Bericht anzuzeigen, gehen Sie zu **Anlagen-Leasing > Anfragen und Berichte > Angaben > GAAP – Cashflows**. 

|     Berichtsfelder                                 |     Beschreibung                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Anfangsdatum <br> Bis-Datum                        |     Definiert einen Datumsbereich, der verwendet wird, um die im Bericht enthaltenen Informationen einzuschränken.      |
|     Juristische Person                                  |     Die mit den Mietverträgen verbundene juristische Person.                                      |
|     Mietvertragstyp                                    |     Die Einstufung des Mietvertrags als finanziell oder operativ.           |
|     Mietvertragskennung                                      |     Die eindeutige Mietvertragskennung.                                                      |
|     Beschreibung des Mietvertrags                             |     Die Beschreibung des Mietvertrags aus dem Header des Mietvertrags.                              |
|     Leasingbuch                                    |     Das Leasingbuch, auf das sich die Zeile bezieht.                        |
|     Buchungsebene                                 |     Jedes Buch, das einer Anlage zugeordnet ist, wird für eine bestimmte Buchungsebene eingerichtet, die ein übergeordnetes Abschreibungsziel aufweist.                          |
|     Mietvertragsgruppe                                   |     Die Gruppe, an die der Mietvertrag gebunden ist.                                     |
|     Währung                                      |     Die Abkürzung für die verwendete Transaktionswährung. Alle Berichte konvertieren die Transaktionswährung in die Berichtswährung.                      |
|     Finanzierungsleasing – Operativer Cashflow         |     Die Summe der gesamten gebuchten variablen Zahlungen und der gesamten aus dem Tilgungsplan gebuchten Zinszahlungen zwischen den Datumsparametern.        |
|     Finanzierungsleasing – Finanzieller Cashflow           |     Die Summe der gesamten Kapitalzahlungen aus dem Tilgungsplan zwischen den Datumsparametern.       |
|     Ausführungsleasing – Operativer Cashflow       |     Die Summe aller gebuchten Mietzahlungen und gebuchten variablen Zahlungen zwischen den Datumsparametern.            |

## <a name="lease-balances-forecast"></a>Prognose der Mietvertragssalden
In der Prognose für Mietbestände sind Informationen direkt aus dem Tilgungsplan für Verbindlichkeiten und dem Abschreibungsplan für Vermögenswerte aufgeführt. Der Bericht zeigt die prognostizierten Beträge der prognostizierten Mietverbindlichkeit und der Nutzungsrechte über einen bestimmten Zeitraum, einschließlich aller prognostizierten Kosten für diese Mietverträge. Der Bericht enthält die folgenden Felder.

|     Berichtsfelder                 |     Beschreibung                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Anfangssaldo             |     Der Anfangssaldo im Tilgungsplan des Mietvertrags für den Zeitraum, der das Startdatum des Berichts enthält.            |
|     Anfängliche Erkennung           |     Wenn das Startdatum des Mietvertrags innerhalb des für den Bericht definierten Datumsbereichs liegt, wird in dieser Spalte der Wert des Verbindlichkeitsskontos des Journaleintrags für die erstmalige Erfassung angezeigt.      |
|     Zahlungen                      |     Die Summe der Mietzahlungen, die in den für den Bericht festgelegten Zeitraum fallen.                               |
|     Interesse                      |     Die Summe des Mietzinsaufwands, der in den für den Bericht festgelegten Zeitraum fällt.                    |
|     Endsaldo                |     Der Verbindlichkeitssaldo des Mietvertrags zum **Enddatum**.                                                             |
|     Kurzfristige Verbindlichkeiten          |     Der Betrag der kurzfristige Verbindlichkeiten im Tilgungsplan des Mietvertrags zum **Enddatum**.                           |
|     Langfristige Verbindlichkeit           |     Der Betrag der langfristigen Verbindlichkeiten im Tilgungsplan des Mietvertrags zum **Enddatum**.                            |
|     Anfangs-Nettobuchwert      |     Der „Anfangs-Nettobuchwert“ im Abschreibungsplan des Mietvertrags für den Zeitraum, der das Startdatum des Berichts enthält      |
|     Anfängliche Erkennung           |     Wenn das Startdatum des Mietvertrags zwischen den Datumsparametern des Bericht liegt, wird in dieser Spalte der Wert des Anlagekontos des Journaleintrags für die erstmalige Erfassung angezeigt.            |
|     Abschreibungsausgaben          |     Die Summe des Mietabschreibungsaufwands, der in den für den Bericht festgelegten Zeitraum fällt.                  |
|     Endsaldo                |     Der Anlagesaldo des Mietvertrags zum **Enddatum**.                                                              |
|     Eigenkapitalregulierung             |     Der Anfangssaldo abzüglich des anfänglichen Nettobuchwerts.                                                             |

## <a name="lease-commencements-report"></a>Bericht über Mietbeginn
Der Bericht über den Beginn eines Mietvertrags zeigt alle Mietverträge, die innerhalb eines bestimmten Zeitraums begonnen haben, einschließlich der anfänglichen Verbindlichkeit und der Bilanz der Nutzungsrechte. Der Bericht enthält die folgenden Felder. 

|     Berichtsfelder                 |     Beschreibung                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Anfangsdatum             |     Das Datum des Journaleintrags für die erstmalige Erfassung, der für diese Mietversion gebucht wurde.         |
|     Anfänglicher Betrag der Verbindlichkeit      |     Der Betrag der Verbindlichkeiten aus des Journaleintrags der erstmaligen Erfassung.                                  |
|     Anfangsbetrag der Anlage          |     Der Anlagenbetrag aus des Journaleintrags der erstmaligen Erfassung.                                      |

## <a name="lease-modification-report"></a>Bericht zu Mietänderungen
Der Mietänderungsbericht zeigt alle Mietverträge an, die innerhalb eines bestimmten Datumsbereichs geändert wurden. Der Bericht zeigt auch den Benutzer, der den Mietvertrag angepasst hat, und den Gesamtbetrag der Verbindlichkeiten, der angepasst wurde. Der Bericht enthält die folgenden Felder. 

|     Berichtsfelder                 |     Beschreibung           |
|---------------------------------  |-------------------------  |
|     Angepasst durch                   |     Der Benutzername der Person, die den Mietvertrag geändert hat.                                |
|     Regulierungsdatum               |     Das Datum, an dem der Regulierungsjournaleintrag gebucht wurde.                        |
|     Regulierungen                   |     Der Betrag für einen Regulierungsjournaleintrag, der zwischen den Datumsparametern auf das Konto für Verbindlichkeiten des Mietvertrags gebucht wird. Gutschriften werden positiv angezeigt, während Belastungen negativ sind.       |
|     Gewinn(Verlust)-Betrag            |     Der Betrag für einen Regulierungsjournaleintrag, der zwischen den Datumsparametern auf das Konto für Gewinn/Verlust des Mietvertrags gebucht wird. Gutschriften werden positiv angezeigt, während Belastungen negativ sind.       |
|     Nicht ausgeschüttete Gewinne             |     Der Betrag für einen Regulierungsjournaleintrag, der zwischen den Datumsparametern auf das Konto für Anfangssalden des Mietvertrags gebucht wird.      |
|     Saldo der auslaufenden Verbindlichkeit      |     Der sich daraus ergebende Saldo für Verbindlichkeiten des Mietvertrags zum Datum der Regulierung.           |

## <a name="lease-movement-report"></a>Mietumlagerungsbericht
Der Bericht über die Umlagerung des Mietvertrags dient als fortlaufender Bericht für die Bilanzen der Leasingverbindlichkeit für jeden Mietvertrag. Mit diesem Bericht kann der Benutzer Verbindlichkeitstransaktionen eines Mietvertrags während eines bestimmten Zeitraums anzeigen.

|     Berichtsfelder             |     Beschreibung                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Anfangsdatum         |     Das Startdatum der frühesten Version des Mietvertrags.    |
|     Mietdauer                |     Die Mietdauer der frühesten Version des Mietvertrags.           |
|     Verbleibende Zahlungen        |     Die Anzahl der Zahlungen, die noch nicht für den Mietvertrag gebucht wurden.                       |
|     Anfangssaldo         |     Die Summe aller Transaktionen, die sich auf die Verbindlichkeiten des Mietvertrags auswirken und vor dem Startdatum des Berichts stattgefunden haben.             |
|     Anfängliche Erkennung       |     Der Betrag einer Transaktion für eine erstmalige Erfassung für den Mietvertrag die innerhalb des für den Bericht festgelegten Datumsbereichs gebucht wurde.     |
|     Zahlungen                  |     Die Summe des Mietzahlungstransaktionen, die in dem für den Bericht festgelegten Zeitraum gebucht wurden. Die Werte in dieser Spalte werden als negative Beträge angezeigt, da die Zahlungen den Verbindlichkeitssaldo des Mietvertrags verringern.  |
|     Interesse                  |     Die Summe des Zinsabgrenzungen, die in dem für den Bericht festgelegten Zeitraum bezüglich des Mietvertrags gebucht wurden.            |
|     Regulierungen               |     Die Summe der gebuchten Regulierungstransaktionen des Mietvertrags, die in den für den Bericht festgelegten Zeitraum fallen.                               |
|     Endsaldo            |     Der Saldo aller Verbindlichkeitstransaktionen des Mietvertrags, die zum **Enddatum** des Berichts gebucht wurden.                  |

## <a name="lease-transactions-report"></a>Bericht zu Miettransaktionen
Die Miettransaktionsabfrage zeigt alle Journaleinträge an, die durch Anlagenleasing generiert wurden. Jeder Journaleintrag ist mit der Buch-ID verknüpft, aus der er stammt. Auf diese Weise können Sie den Journaleintrag problemlos mit dem entsprechenden Mietvertrag verknüpfen. Die Miettransaktionsabfrage funktioniert ähnlich wie die **Gutscheintransaktionen**-Seite im Hauptbuch.

## <a name="weighted-average-discount-rate-report"></a>Bericht über den gewichteten durchschnittlichen Diskontsatz
Der Bericht über den gewichteten durchschnittlichen Diskontsatz erfüllt die in ASC 842-20-50-4 (g) (4) angegebene US-GAAP-Offenlegungspflicht für einen gewichteten durchschnittlichen Diskontsatz. Um diesen Bericht anzuzeigen, gehen Sie zu **Anlagen-Leasing > Anfragen und Berichte > Angaben > Gewichteter durchschnittlicher Diskontsatz**. Der Bericht enthält die folgenden Felder. 

|     Berichtsfelder                     |     Beschreibung                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Referenzdatum                        |     Dieser Bericht enthält alle Mietverträge, die am oder vor dem **Ab**-Datumsparameter begonnen haben. Dieser Bericht sollte ab dem letzten Tag des Berichtszeitraums erstellt werden.      |
|     Juristische Person                      |     Die mit dem Mietvertrag verbundene juristische Person.                           |
|     Mietvertragskennung                          |     Die eindeutige Mietvertragskennung.                                                  |
|     Beschreibung des Mietvertrags                 |     Die Beschreibung des Mietvertrags aus dem Header des Mietvertrags.                          |
|     Buch                              |     Der spezifische Buchtyp des angezeigten Mietvertrags.                                                                                                                                            |
|     Buchungsebene                     |     Jedes Buch, das einer Anlage zugeordnet ist, wird für eine bestimmte Buchungsebene eingerichtet, die ein übergeordnetes Abschreibungsziel aufweist.      |
|     Mietvertragsgruppe                       |     Die Gruppe, zu der der Mietvertrag gehört.                                 |
|     Diskontsatz                     |     Der für das Diskontieren von Mietzahlungen verwendete Satz.                             |
|     Währung                          |     Die Abkürzung für die verwendete Transaktionswährung. Alle Berichte konvertieren die Transaktionswährung in die Berichtswährung.  |
|     Verbleibende Mietzahlungen          |     Der Gesamtbetrag der nicht bezahlten Mietzahlungen aus dem Zahlungsplan, der vom **Ab**-Datum verbleibt.            |
|     Verbleibende gewichtete Zahlungen       |     Die verbleibenden Mietraten multipliziert mit dem verwendeten Diskontsatz.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]