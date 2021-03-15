---
title: Erste Schritte mit dem Anlagen-Leasing
description: In diesem Thema wird die Anlagenleasing-Funktion beschrieben und Sie werden durch die Schritte zum Erstellen eines Anlagenleasings sowie zum Anzeigen von Informationen zu diesen Leasingverträgen geführt.
author: moaamer
manager: Ann Beebe
ms.date: 10/16/2020
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
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 97fcaeb091d91c3b214451b0b156382e450e60f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971502"
---
# <a name="asset-leasing-get-started"></a>Erste Schritte mit dem Anlagen-Leasing

[!include [banner](../includes/banner.md)]

In diesem Thema wird die Anlagenleasing-Funktion beschrieben und Sie werden durch die Schritte zum Erstellen eines Anlagenleasings sowie zum Anzeigen von Informationen zu diesen Leasingverträgen geführt. Das Thema definiert außerdem die in der Benutzeroberfläche und der Dokumentation verwendete Terminologie. Anlagenleasing ist eine erweiterte Funktion zur Verwaltung, Verfolgung und Automatisierung von Finanzbuchungen für Leasingobjekte in Microsoft Dynamics 365 Finance. Anlagenleasing entspricht den internationalen Rechnungslegungsstandards (IFRS 16) und den US-GAAP-Standards (ASC 842). Anlagenleasing erfasst und verarbeitet Informationen zu den Leasingverträgen und unterstützt das Generieren von Journaleinträgen über den gesamten Lebenszyklus des Leasingtvertrags hinweg, von der erstmaligen Erfassung über monatliche Journaleinträge bis hin zur dauerhaften Wertminderung und zur Beendigung des Leasingvertrags. Anlagenleasing lässt sich nahtlos in andere Komponenten von Dynamics 365 Finance integrieren, inklusive „Anlagen“, „Kreditorenkonten“ und „Hauptbuch“.

Weitere Informationen zu Rechnungslegungsstandards finden Sie in der Standarddokumentation für IFRS 16 und US GAAP ASC 842.

## <a name="asset-leasing-elements"></a>Analgen-Leasing-Elemente
Das folgende Diagramm zeigt die Hauptelemente des Geschäftsprozesses für Leasingverhältnisse.

[![Analgen-Leasing-Elemente](./media/overview-01.png)](./media/overview-01.png)

Ein Leasingobjekt enthält folgende Hauptkomponenten:

- **Leasingvertrag**: Der Leasinggeber ist Eigentümer der Anlage und vereinbart mit dem Leasingnehmer das Leasing einer Anlage für einen bestimmten Zeitraum gegen regelmäßige Leasingzahlungen. Neben dem rechtsgültigen Vertrag zwischen dem Leasinggeber und dem Leasingnehmer erfasst der Leasingvertrag Managemententscheidungen wie die Wahrscheinlichkeit des Gebrauchmachens von einer Verlängerungsoption und die Übertragung des Eigentums.

- **Leasingberechnung und -klassifizierung nach Rechnungslegungsstandard**: Die Berechnung und Klassifizierung des Leasingverhältnisses geben den Rechnungslegungsstandard an, der bei der anfänglichen und nachfolgenden Bewertung angewendet wird, sowie den Klassifizierungstest, der die Art des Leasingverhältnisses bestimmt. Ein Leasingverhältnis kann ein Finanzierungsleasing, ein Ausrüstungs-Leasingvertrag, ein Kurzzeitleasing oder ein Leasing von geringem Wert sein. Das System berechnet auch den Barwert zukünftiger Mindestleasingzahlungen zum Zwecke der Bewertung und Klassifizierung.

- **Leasingbuchungen**: Das Anlagenleasing unterstützt die erstmalige Erfassung des Nutzungsrechts am Leasingobjekt für in der Bilanz enthaltene Leasingverhältnisse sowie die anschließende Bewertung entweder für bilanzielle oder für außerbilanzielle Leasingverhältnisse. Die erstmalige Erfassungbuchung bemisst den Barwert zukünftiger Mindestleasingzahlungen. Diese Daten werden verwendet, um den Wert des ursprünglichen Nutzungsrechts am Leasingobjekt und der Leasingverbindlichkeiten zu bestimmen, der sich auf die Bilanz des Unternehmens auswirkt. Die anschließende Bewertung der monatlichen Leasingbuchungen umfasst die Aufzinsung auf die Leasingverbindlichkeit, wodurch sich die Leasingverbindlichkeit erhöht. Außerdem wird die Rückstellung von Leasingzahlungen bewertet, die die Leasingverbindlichkeit verringern und anschließend an den Leasinggeber gezahlt werden. Die Bewertung umfasst auch die Amortisierung des Nutzungsrechts am Leasingobjekt.

  Bei außerbilanziellen Leasingverhältnissen berechnet das System die linearen Leasingaufwendungen für den niedrigeren der folgenden Werte: die wirtschaftliche Lebensdauer der Anlage oder die Leasingdauer. Leasinganpassungen bewerten Vertragsänderungen, wie eine Verlängerung oder Erweiterung des Leasingverhältnisses, sowie die Wertminderungsbuchung, bei der das Nutzungsrecht am Leasingobjekt für nicht erstattungsfähige Kosten verwendet wird.

  Anlagenleasing wird in Hauptbuch integriert, um sicherzustellen, dass alle gebuchten Leasingbuchungen Ihren Kontenplan aktualisieren. Assetleasing wird in Kreditorenkonten integriert, um Leasinggeberrechnungen in den Kreditorenkonten zu verfolgen und zukünftige Zahlungen von dort zu übernehmen. Durch die Integration in Anlage können Sie Leasingverhältnisse im Anlagenregister verfolgen und Buchungen mit Nutzungsrechten am Leasingobjekt, einschließlich der erstmaligen Erfassung, der Abschreibung und der dauerhaften Wertminderung der Anlage, innerhalb von Anlage buchen.   

## <a name="asset-leasing-components"></a>Assetleasing-Komponenten 
Assetleasing ordnet Leasinginformationen, Zahlungspläne, Start- und Enddaten sowie die Zahlungshäufigkeit zu. Außerdem werden Berechnungen für den Barwert, die monatlichen Leasingzahlungen, die Zinsen und die Leasingamortisierung automatisiert. Das System führt je nach Konfiguration Klassifizierungstests für das Leasingverhältnis durch. Das System erstellt und bucht auch die entsprechenden Leasingbuchungen, die auf dem Framework basieren, das durch den von Ihnen befolgten Rechnungslegungsstandard definiert ist.

Das folgende Diagramm zeigt das Leasingbuch, das Leasingverhältnis, den berechneten Zahlungsplan, die Klassifizierungstests für Leasingverhältnisse und -bücher sowie die entsprechenden Buchhaltungsbuchungen.

[![Leasing, Leasingbuch und Zahlungsplan](./media/overview-02.png)](./media/overview-02.png)

- **Leasingbuch**: Das Leasingbuch enthält alle Informationen zum Leasingvertrag wie Leasingbestimmungen, Zeitwert und Leasingzahlungen. Es enthält auch den Rechnungslegungsstandard, den Sie befolgen, die Leasingart und die Schwellenwerte, die im Klassifizierungstest für das Leasingverhältnis berücksichtigt werden. Das Leasingbuch enthält auch die Leasingbuchungen, die im Hauptbuch gebucht wurden. 
  
- **Leasingvertrag**: Der Leasingvertrag enthält die Informationen zum Anlagenleasing, die die Grundlage für selbiges darstellen. Die Informationsquelle für Leasingverträge sind Leasingverträge und Managemententscheidungen, die beide außerhalb von Dynamics 365 Finance getroffen werden. Der Zeitwert der Anlage ist der Preis, der zum Bewertungsstichtag für eine Anlage in einer Buchung gezahlt würde. Dieser Wert kann von der Anlagenart, den Marktbedingungen und anderen Kriterien abhängen, die bei der Bewertung berücksichtigt werden können. Der Zeitwert der Anlage wird in der Gleichung für den Klassifizierungstest berücksichtigt.

- **Nutzungsdauer der Anlage**: Dies sind die verbleibenden Zeiträume der Nutzungsdauer einer Anlage ab dem Datum des Leasingbeginns. Die Nutzungsdauer einer Anlage wird in der Gleichung für den Klassifizierungstest berücksichtigt. Sie unterscheidet sich von der in den Anlagen definierten Nutzungsdauer.

- **Zinssatz für Neukredit**: Dies ist der Zinssatz, der zur Berechnung des Barwerts verwendet wird. Das System verwendet den impliziten Satz, wenn er in den Leasingdaten definiert ist, um den Barwert der Leasingzahlungen zu berechnen. Wenn der implizite Satz nicht definiert ist, verwendet das System den Zinssatz für Neukredite.

- **Annuitätstyp**: Die Leasingzahlung, die entweder zu Beginn des Zahlungszeitraums oder am Ende des Zeitraums fällig ist. Dies kann eine Vorauszahlung oder eine fällige Annuität (zu Beginn des Zeitraums der Leasingzahlung) oder eine normale Annuität (am Ende des Zeitraums der Leasingzahlung) sein.

  Der erste Monat gilt als Zeitraum mi der Nummer Null für die Vorauszahlung. Der erste Monat gilt als erster Zeitraum für Zahlungsrückstände.

- **Aufzinsungsintervall**: Dies entspricht der Anzahl der Zeiträume, die der Zins pro Jahr aufgezinst wird. Diese Aufzinsung kann monatlich (12 Zeiträume pro Jahr), vierteljährlich (4 Zeiträume pro Jahr), halbjährlich (2 Zeiträume pro Jahr) oder jährlich (1 Zeitraum pro Jahr) erfolgen. Die Anzahl der Zeiträume wird bei der Barwertberechnung berücksichtigt.

- **Datum des Leasingbeginns**: Das Datum, an dem der Leasinggeber dem Leasingnehmer die Anlage zur Nutzung zur Verfügung stellt. Alle Leasingberechnungen und -buchungen basieren auf dem Datum des Leasingbeginns. Das Datum des Leasingbeginns sollte am Anfang eines Zeitraums (1. des Monats) liegen, um die Genauigkeit nachfolgender Berechnungen sicherzustellen. Sie können das Feld **Datum der Vertragsunterzeichnung** zur Eingabe des tatsächlichen Datums der Vertragsunterzeichnung verwenden.

- **Leasingdauer**: Die Länge des Leasingzeitraums in Monaten.

> [!NOTE] 
> Die Definition der Leasingdauer basiert auf der Anzahl der Zeiträume oder Intervalle in den Zahlungsplanpositionen. Die definierte Anzahl von Intervallen wird in Monate umgerechnet.

- **Zahlungsplanposition**: Erfasst die Leasingzahlungen pro Zeitraum. Außerdem legt sie fest, ob ein Verlängerungszeitraum ausgeübt und in die erstmalige Bewertung des Nutzungsrechts am Leasingobjekt und der Leasingverbindlichkeit einbezogen wird. Sie können das Startdatum der fälligen Leasingzahlungen und die Zeitraumintervalle definieren, die die Dauer des Leasingverhältnisses darstellen. Dies können Tage, Monate oder Jahre sein.

- **Zahlungshäufigkeit**: Gibt an, ob die Zahlung monatlich, vierteljährlich, halbjährlich oder jährlich erfolgt. Das Enddatum wird automatisch anhand des Startdatums und der Anzahl der eingegebenen Zeiträume berechnet.

- **Zahlungsplan**: Der berechnete Barwert, basierend auf der von den Leasingzahlungen abgedeckten Zeitspanne, der Höhe der Zahlungen, den Aufzinsungsintervallen und dem Annuitätstyp.

- **Zeiträume**: Die Leasingzeiträume, die das Aufzinsungsintervall und den Annuitätstyp widerspiegeln. Das Aufzinsungsintervall bestimmt, wie Zeiträume aufgeteilt werden. Sie können folgende Aufzinsungsintervalle festlegen:

  - Monatlich, 12 Zeiträume pro Jahr
  - Vierteljährlich, 4 Zeiträume pro Jahr
  - Halbjährlich, 2 Zeiträume pro Jahr
  - Jährlich, 1 Zeitraum pro Jahr

Der erste Zeitraum beginnt mit dem Zeitraum Null, wenn der Annuitätstyp „Annuität fällig“ ist. Andernfalls beginnt der erste Zeitraum mit Eins, wenn der Annuitätstyp „Zahlungsrückstände“ ist.

- **Monate**: Gibt die Anzahl der Kalendermonate über die Laufzeit des Leasingverhältnisses an. Der Zahlungsbetrag ist der fällige Betrag, wie in der Zahlungshäufigkeit definiert. Der berechnete Barwert ist die auf dem Barwert basierende Leasingzahlung pro Zeitraum, die Aufzinsungsintervalle und der Zinssatz für Neukredite.

> [!NOTE] 
> Der Barwert wird basierend auf der Gleichung des diskontierten Cashflows berechnet.

- **Bücher**: Das vorkonfigurierte Setup, das jedem Leasingverhältnis zugeordnet wird. Das Buch definiert den angewandten Rechnungslegungsstandard, die Leasingarten und den Schwellenwert, der als Grundlage für die Klassifizierungstests verwendet wird. Klassifizierungstests werden verwendet, um die Leasingart automatisch festzulegen.

- **Rechnungslegungsrahmen**: Zeigt den ausgewählten Rechnungslegungsstandard (entweder IFRS 16 oder ASC 842) an, den Sie befolgen. Der Rechnungslegungsstandard ist in dem Buch angegeben, das dem Leasingverhältnis zugeordnet ist. Der Rechnungslegungsstandard bestimmt die Sachkonten, die im Buchungsprofil angegeben sind.

- **Leasingarten**: Gibt an, welche der beiden Arten von Leasingverhältnissen verwendet wird, entweder ein Finanzierungsleasing oder ein Ausrüstungs-Leasingvertrag. Im Rahmen eines Finanzierungsleasings werden Risiken und Chancen, die mit dem Leasingobjekt zusammenhängen, auf den Leasingnehmer übertragen. Bei einem Ausrüstungs-Leasingvertrag verbleiben die Risiken und Chancen, die sich auf das Leasingobjekt beziehen, beim Leasinggeber. Eine dritte Option ist eine automatisierte Identifizierung der Leasingart (Finanzierungsleasing oder Ausrüstungs-Leasingvertrag) basierend auf den im Buch definierten Schwellenwerten. Diese automatische Identifizierung wird während dem Reklassifizierungstests für das Leasingverhältnis durchgeführt.

- **Schwellenwerte**: Werden in den Klassifizierungstests für Leasingverhältnisse verwendet, um festzustellen, ob die Anlage als eine der folgenden klassifiziert ist:

  - **Leasingdauer**: Der Prozentsatz der Nutzungsdauer, der für den Klassifizierungstest verwendet werden soll. Das System klassifiziert das Leasingverhältnis als Finanzierungsleasing, wenn die Leasingart auf automatisch eingestellt ist und das Verhältnis der Leasingdauer zur Nutzungsdauer der Anlage größer oder gleich dem hier definierten Prozentsatz ist.

  - **Barwert**: Der Prozentsatz des Zeitwerts der Anlage, der für den Klassifizierungstest verwendet werden soll. Das System klassifiziert das Leasingverhältnis als Finanzierungsleasing, wenn die Leasingart auf automatisch eingestellt ist und das Verhältnis des Barwerts künftiger Leasingzahlungen zum Zeitwert der Anlage größer oder gleich dem hier definierten Prozentsatz ist.

  - **Kurzzeitleasing**: Wenn die Leasingdauer kürzer oder gleich dem hierfür definierten Wert ist, wird das Leasingverhältnis als Kurzzeitleasing eingestuft.

  - **Leasingobjekt von geringem Wert**: Wenn der Zeitwert der Anlage kleiner oder gleich dem hierfür definierten Wert ist, wird das Leasingverhältnis als Leasingobjekt von geringem Wert eingestuft.

  - **Leasingklassifizierung und -buchungen**: Die Leasingklassifizierung ist ein automatisierter Prozess zur Klassifizierung der Leasingverhältnisse anhand der in Büchern definierten Schwellenwerte sowie anderer Kriterien für Klassifizierungstests, um festzustellen, ob es sich bei dem Leasingverhältnis um ein Finanzierungsleasing, einen Ausrüstungs-Leasingvertrag, ein Kurzzeitleasing oder ein Leasingobjekt von geringem Wert handelt. Dies wird auch verwendet, um festzustellen, ob der Prozess für den zurückgestellten Mietaufwand eingehalten wird.

Zu den Klassifizierungstests gehören Eigentumsübertragung, Kaufoption, Leasingdauer, Barwert und Einmalige Anlage. Das folgende Diagramm zeigt die Klassifizierungstests für Leasingverhältnisse.

[![Klassifizierungstests für Leasingverhältnisse](./media/overview-03.png)](./media/overview-03.png)

Jede Leasingart geht bei der Buchhaltung für unterschiedliche Leasingbuchungen anders vor. Die Buchungen umfassen erstmalige Erfassung, Zinsaufwand, fällige Leasingzahlungen und Leasingabschreibungen und basieren auf den von Ihnen befolgten Rechnungslegungsstandards (IFRS 16 oder ASC 842). Sachkonten werden unter dem Buchungsprofil des Leasingverhältnisses für jede Buchungsart und jeden Rechnungslegungsrahmen definiert.

## <a name="asset-leasing-transactions"></a>Transaktionen beim Anlagenleasing

#### <a name="initial-recognition"></a>Anfängliche Erkennung 
Für die erstmalige Erfassung eines Leasingobjekts wird der berechnete Barwert verwendet, damit er in der Bilanz ausgewiesen werden kann. Der Buchhaltungseintrag hierfür wird automatisch generiert. Diese Transaktion belastet das Konto des Nutzungsrechts am Leasingobjekt und führt für das Konto der Ausrüstungs-Leasingverbindlichkeit wie folgt eine Gutschrift durch. Wenn dem Leasingverhältnis eine Anlage zugeordnet ist, wird der erste Erfassungseintrag als eine Anlagenanschaffung ausgewiesen. In diesem Szenario müssen Sie ein Buchungsprofil für Anlagen definieren, um die Buchung auf das Konto des Nutzungsrechts am Leasingobjekt durchzuführen. 

> [!NOTE]
> Ausrüstungs-Leasingverträge werden nur von US GAAP ASC 842 unterstützt.

|     Typ                                          |     Belastung                     |     Gutschrift                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operating-Leasingvertrag nach US GAAP              |     Nutzungsrecht am Leasingobjekt      |     Ausrüstungs-Leasingverbindlichkeit       |
|     Finanzierungsleasing nach IFRS und US GAAP        |     Nutzungsrecht am Leasingobjekt      |     Ausrüstungs-Leasingverbindlichkeit       |

#### <a name="lease-liability-amortization-interest-expense"></a>Amortisierung von Leasingverbindlichkeiten (Zinsaufwand) 
Die Zinsen für ein Leasingverhältnis werden durch Berechnung der Zinsen für den Anfangssaldo des Leasingverhältnisses, die Leasingzahlung pro Zeitraum, den Sollzinssatz und die Aufzinsungsintervalle pro Jahr erfasst. Der Zinsbetrag erhöht das Konto der Ausrüstungs-Leasingverbindlichkeit durch eine Gutschrift, die in der Bilanz des Unternehmens ausgewiesen wird. Die Transaktion beinhaltet auch eine Belastung des Zinsaufwandkontos, die für ein Finanzierungsleasing in der Gewinn- und Verlustrechnung ausgewiesen wird, sowie des Leasingaufwandkontos für Ausrüstungs-Leasingverträge.

|     Typ                                          |     Belastung                     |     Gutschrift                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Eintrag der Ausrüstungs-Leasingverbindlichkeit nach US GAAP ASC 842    |     Zinsausgaben          |     Verbindlichkeit für Ausrüstungs-Leasingvertrag         |
|     Eintragung der Finanzierungsleasingverbindlichkeit nach IFRS und US GAAP      |     Zinsausgaben          |     Verbindlichkeit durch Finanzierungsleasing           |

#### <a name="accrued-lease-payment"></a>Aufgelaufene Leasingzahlung
Eine aufgelaufene Leasingzahlung wird als zukünftige Leasingzahlung erfasst, die als Zahlungstransaktion vom Bank- oder vom Geldkonto verarbeitet werden soll. Die fällige Leasingzahlung verringert die Leasingverbindlichkeit, indem das Leasingverbindlichkeitskonto belastet wird. Hierbei kommt es darauf an, ob ein untergeordnetes Sachkonto des Kreditors im Falle des Leasinggebers als Kreditor definiert ist, oder ob die Habenseite auf das Sachkonto einer Wechselverbindlichkeit gebucht wird. Anschließend wird die Zahlung entweder für den Kreditor oder die Wechselverbindlichkeit ausgeführt.

|     Typ                                          |     Belastung                     |     Gutschrift                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operating-Leasingvertrag nach US GAAP              |  Verbindlichkeit für Ausrüstungs-Leasingvertrag    |   Kreditorenverbindlichkeit (untergeordnetes Sachkonto) / Wechselverbindlichkeit  |
|     Finanzierungsleasing nach IFRS und US GAAP        |  Verbindlichkeit durch Finanzierungsleasing      |   Kreditorenverbindlichkeit (untergeordnetes Sachkonto) / Wechselverbindlichkeit  |

#### <a name="asset-depreciation"></a>Anlagenabschreibung
Das Nutzungsrecht am Leasingobjekt wird entweder über die Nutzungsdauer der Anlage oder die Leasingdauer abgeschrieben, je nachdem, welcher Wert kleiner ist. Die Methode zur Berechnung der Abschreibung nach US GAAP (ASC 842) basiert auf der Differenz zwischen den linearen Leasingaufwendungen und dem Zinsbetrag. Die Zinsen für ein Finanzierungsleasing werden linear berechnet. Die Leasingabschreibung wirkt sich durch die Zinsaufwendungen auf die Gewinn- und Verlustrechnung aus. Bei Finanzierungsleasings wird die Bilanz durch kumulierte Gutschriften auf das Konto des Nutzungsrechts am Leasingobjekt beeinflusst. Bei Ausrüstungs-Leasingverträgen wird die Abschreibung dem Leasingaufwandskonto gutgeschrieben. Wenn das Leasingverhältnis mit einer Anlage verknüpft ist, werden die Abschreibungstransaktionen nur über das Anlagenmodul ausgeführt. 

|     Typ                                          |     Belastung                     |     Gutschrift                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Operating-Leasingvertrag nach US GAAP              |  Mietvertragsausgaben                |   Kumulierte Abschreibungen für das Nutzungsrecht am Leasingobjekt     |
|     Finanzierungsleasing nach IFRS und US GAAP        |   Abschreibung der Ausgaben für das Nutzungsrecht am Leasingobjekt   |   Kumulierte Abschreibungen für das Nutzungsrecht am Leasingobjekt    |

#### <a name="short-term-lease"></a>Kurzfristiger Mietvertrag
Ein Kurzzeitleasing wird als Ausgabe erfasst, die sich auf die Gewinn- und Verlustrechnung eines Unternehmens auswirkt. Die generierte fällige Leasingzahlung belastet das Leasingaufwandskonto und führt eine Gutschrift für das Konto der Wechselverbindlichkeit oder das untergeordnete Sachkonto des Kreditors durch.

|     Typ                                          |     Belastung                     |     Gutschrift                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Eintragung des Kurzzeitleasings nach IFRS und US GAAP     |  Mietvertragsausgaben                |   Kreditorenverbindlichkeit (untergeordnetes Sachkonto) / Wechselverbindlichkeit  |

#### <a name="low-value-lease"></a>Leasingobjekt von geringem Wert
Ein Leasingobjekt von geringem Wert wird als Ausgabe erfasst, die sich auf die Gewinn- und Verlustrechnung Ihres Unternehmens auswirkt. Die generierte fällige Leasingzahlung belastet das Leasingaufwandskonto und führt eine Gutschrift für das Konto der Wechselverbindlichkeit oder das untergeordnete Sachkonto des Kreditors durch.

|     Typ                                          |     Belastung                     |     Gutschrift                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Eintragung des Leasingobjekts von geringem Wert nach IFRS und US GAAP      |  Mietvertragsausgaben                |   Kreditorenverbindlichkeit (untergeordnetes Sachkonto) / Wechselverbindlichkeit  |


#### <a name="index-revaluation"></a>Index-Neubewertung
Das Anlagenleasingkonto für variable Leasingzahlungen, gemessen anhand einer Indexrate. Änderungen der Leasingzahlungen aufgrund von Schwankungen der Indexrate stellen eine Leasinganpassung nach IFRS 16 dar. Die Leasingverbindlichkeit und das Nutzungsrecht am Leasingobjekt werden angepasst, um die neuen Zahlungen zu berücksichtigen. 

|     Typ                                          |     Belastung                             |     Gutschrift                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Eintragung zur Neubewertung des Index nach IFRS im Falle einer Erhöhung  |  Nutzungsrecht am Leasingobjekt       |   Verbindlichkeit für Ausrüstungs-Leasingvertrag |
|   Eintragung zur Neubewertung des Index nach IFRS im Falle einer Senkung  |  Verbindlichkeit für Ausrüstungs-Leasingvertrag  |   Nutzungsrecht am Leasingobjekt      |

Wenn sich Zahlungen aufgrund einer Änderung der Indexrate ändern, ändern sich nur die variablen Zahlungen, es sei denn, es gibt zusätzliche Änderungen des Cashflows, z. B. eine Änderung der Leasingdauer in Bezug auf die Zinssätze nach US GAAP ASC 842.

#### <a name="lease-adjustment"></a>Mietvertragsregulierung
Mit Anlagenleasing können Leasingverhältnisse angepasst werden, wenn die Leasingdauer geändert, das Leasingverhältnis verlängert oder zusätzliche Umstände vorliegen, unter denen ein Leasingverhältnis eine Anpassung erfordert. Leasinganpassungen werden gebucht, um das Nutzungsrecht am Leasingobjekt und die Leasingverbindlichkeit zu erhöhen oder zu verringern. Der Anpassungsprozess übernimmt zum Zeitpunkt der Anpassung Endsalden der Amortisierung von Verbindlichkeiten sowie Anlagensalden. Wenn ein Leasingverhältnis mit der Anlage verbunden ist, wird die Anpassung des Nutzungsrechts unter Verwendung der in der Anlage zugewiesenen ID gebucht. 

|     Typ                                          |     Belastung                             |     Gutschrift                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Eintragung der Leasinganpassung nach IFRS und US-GAAP im Falle einer Erhöhung     |  Nutzungsrecht am Leasingobjekt       |   Verbindlichkeit für Ausrüstungs-Leasingvertrag |
|   Eintragung der Leasinganpassung nach IFRS und US-GAAP im Falle einer Senkung     |  Verbindlichkeit für Ausrüstungs-Leasingvertrag  |   Nutzungsrecht am Leasingobjekt      |


#### <a name="lease-impairment"></a>Leasingminderung
Dies entspricht der übertragenen Saldosenkung des Nutzungsrechts am Leasingobjekt. Ermitteln Sie den Wertminderungsbetrag, das Transaktionsdatum und die verbleibenden Zeiträume. Das verbleibende Nutzungsrecht am Leasingobjekt wird linear abgeschrieben. Die Logik der Leasingminderung berücksichtigt den Übertragswert der Anlage, die im Abschreibungsplan für die Anlage enthalten ist.  

|     Typ                                          |     Belastung                             |     Gutschrift                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Eintragung der Wertminderung nach IFRS und US GAAP           |  Aufwand der dauerhaften Wertminderung                   |    Nutzungsrecht am Leasingobjekt     |

>[!NOTE]
> Wenn das Leasingverhältnis mit einer Anlage verknüpft ist, sollte die Leasingminderung aus der Anlage gebucht werden, da die Abschreibung der Anlage über das Anlagenmodul erfolgt.

**Doppelte Währung**: Leasingtransaktionen können in einer anderen Währung als der Buchhaltungs- und Berichtswährung gebucht werden. Der Wechselkurs wird am Datum des Leasingbeginns im Hauptbuch definiert. Sie können die Wechselkurse ändern, indem Sie das Feld **Fester Wechselkurs** auf **Ja** festlegen, wenn Sie das Leasingverhältnis erstellen. Wenn Sie Leasingtransaktionen eingeben, wird für die erstmalige Erfassung und die anschließenden Abschreibungstransaktionen der Wechselkurs vom Datum des Leasingbeginns verwendet. Für die nachfolgenden Zahlungen und Zinsbuchungen wird der aktuelle Wechselkurs verwendet. 

## <a name="create-an-asset-lease"></a>Erstellen eines Anlagenleasings
Führen Sie die folgenden Schritte aus, um ein neues Leasing zu erstellen. 

1. Um die Funktion **Anlagenleasing** zu verwenden, müssen Sie sie im Arbeitsbereich **Funktionsverwaltung** aktivieren. Wählen Sie im Arbeitsbereich **Funktionsverwaltung** die Option **Alle** aus, damit alle Funktionen auf der Seite aufgelistet werden. Wählen Sie **Anlagenleasing** aus und wählen Sie dann **Jetzt aktivieren** aus.
2. Wechseln Sie zu **Anlagenleasing > Allgemein > Leasingübersicht**. Füllen Sie die erforderlichen Felder auf dem Inforegister **Allgemein** aus. 
   - **Details zum Mietvertrag**
   - **Nutzungsdauer für Anlagen (Monate)**
   - **Mietvertragsgruppe**
   - **Zinssatz für Neukredit (%)**
   - **Aufzinsungsintervall**
   - **Annuitätstyp**
   - **Währung**
   - **Anfangsdatum**

3. Wechseln Sie zum Inforegister **Zahlungsplanpositionen** und geben Sie eine Zahlungsposition ein. Wählen Sie dann **Zeitpläne erstellen** aus.

4. Wählen Sie **Bücher**. 

5. Wechseln Sie zum Inforegister **Allgemein**. Das **anfängliche Nutzungsrecht am Leasingobjekt** und die **Leasingverbindlichkeit** werden berechnet. 

6. Wechseln Sie zum Inforegister **Klassifizierungstest für das Leasingverhältnis**, um den Wert im Feld **Leasingart** zu überprüfen. 

   Die **Leasingart** wird automatisch anhand der Kriterien klassifiziert, die auf der Seite **Bücher** definiert sind.

7.  Wechseln Sie zu **Zahlungsplan** im Bereich **Funktion**.  

   Die Seite **Zahlungsplan** listet zukünftige Zahlungspläne für eine Leasing-ID auf. Wählen Sie **Zeitplan bestätigen** aus, um die Transaktionen **Erstmalige Erfassung** buchen zu können. 

[![Funktion „Erstmalige Erfassung“](./media/overview-13.png)](./media/overview-13.png)

8. Wählen Sie **Erstmalige Erfassung** aus, um die erste Erfassung zu erstellen. 

9. Wählen Sie **Erfassungen für das Anlagenleasing** aus, um die erste Erfassungstransaktion zu buchen. 

   Über den Zahlungsplan können Sie eine detaillierte Seite öffnen, auf der die Transaktionen für das Nutzungsrecht am Leasingobjekt aufgeführt sind. 
 
   Der **Zeitplan zur Amortisierung von Leasingverbindlichkeiten** zeigt den Zinsbetrag an, der für jeden Zeitraum berechnet wird.
   
10. Erstellen Sie die Erfassung und wechseln Sie dann zu **Erfassungen für das Anlagenleasing**. Der **Zeitplan zur Amortisierung von Leasingverbindlichkeiten** wird auch in den Zinstransaktionen angezeigt.

   Die Seite **Abschreibungsplan für die Anlage** zeigt die Abschreibungstransaktionen für die ausgewählte Leasing-ID an. 

   [![Seite „Transaktionen für das Nutzungsrecht am Leasingobjekt“](./media/overview-20.png)](./media/overview-20.png)

   Die Seite **Transaktionen für das Nutzungsrecht am Leasingobjekt** zeigt die erstmalige Erfassung, die kumulierten Abschreibungen und das Anlagensaldo an. 

   Dei Seite **Leasingverbindlichkeitstransaktionen** zeigt die erstmalige Erfassung, die Leasingzinszahlung, die Leasingzahlung und den Saldo der Leasingverbindlichkeit an. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]