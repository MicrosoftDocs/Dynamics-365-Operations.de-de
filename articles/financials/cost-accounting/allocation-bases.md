---
title: Zuteilungsbasen
description: "Dieses Thema enthält Informationen zu Zuteilungsbasen. Zuteilungsbasen sind Schlüsselkomponenten bei der Kostenrechnung und werden größtenteils verwendet, um Gemeinkosten zuzuteilen."
author: AndersGirke
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63f39a6c06a0c6b5df901f7aa4235aab3c4ac06e
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="allocation-bases"></a>Zuteilungsbasen 

[!include [banner](../includes/banner.md)]

Eine Zuteilungsbasis ist die Basis, auf der die Kostenrechnung Gemeinkosten zuteilt. Eine Zuteilungsbasis kann eine Menge, wie Maschinenstunden, die verwendet werden, Kilowattstunden (kWh), die verbraucht werden, oder Grundfläche sein, die beansprucht wird. Zuteilungsbasen werden meistens verwendet, um Gemeinkosten dem Bestand zuzuweisen, der erstellt wird. Beispielsweise weist eine IT-Abteilung die Ausgaben gemäß der Anzahl von Computern zu, die jede Abteilung verwendet.

Es gibt drei Typen von Zuteilungsbasen bei der Kostenrechnung:

- Vordefinierte Dimensionselement-Zuteilungsbasen
- Hierarchiezuteilungsbasen
- Formelzuteilungsbasen

## <a name="predefined-dimension-member-allocation-bases"></a>Vordefinierte Dimensionselement-Zuteilungsbasen

Die vordefinierten Dimensionselement-Zuteilungsbasen werden automatisch erstellt, wenn ein Dimensionselement für einen der folgenden Typen erstellt wird:

- Mitglieder der statistischen Dimension
- Kostenelement-Dimensionsmitglieder

> [!NOTE]
> Die Vordefinierten Dimensionselement-Zuteilungsbasen, die auf einem Kostenelement-Dimensionsmitglied basieren, berücksichtigen nur die Werte aus dem Datenquellenanbieter, wie dem Hauptbuch oder dem Budget.

### <a name="example-1-use-a-cost-element-dimension-member-as-the-allocation-base"></a>Beispiel 1: Verwenden eines Kostenelement-Dimensionsmitglieds als die Zuteilungsbasis
Dieses Beispiel zeigt, wie eine Kostenzuteilungsregel erstellt wird, um Kostenelement 10002 (Mitarbeiterversicherung) dem Saldo zuzuweisen, das auf Kostenelement 10001 (Ausgaben) eingetragen ist. Die Zuordnungsregel wird auf dem Verhältnis der Gehälter jeder Abteilung zu allen Gehältern definiert. (Prüfung erforderlich!)

Im Hauptbuch wird der Kontenplan wie folgt definiert.

| Kontenplan | Hauptkonto | Beschreibung        | Hauptkontotyp |
|------------------|--------------|--------------------|-------------------|
| Gemeinsam           | 10001        | Löhne           | Spesen           |
| Gemeinsam           | 10002        | Mitarbeiterversicherung | Spesen           |

Definieren Sie eine Kostenelementdimension und konfigurieren Sie den Datenkonnektor. Nachdem die Daten importiert wurden, werden die folgenden Einträge in der Kostenrechnung erstellt.

**Kostenelement-Dimensionsmitglieder**

| Name für Kostenelementdimension | Kostenelement |  Beschreibung       | Typ    |
|-----------------------------|--------------|--------------------|---------|
| Kostenelemente               | 10001        | Löhne           | Primär |
| Kostenelemente               | 10002        | Mitarbeiterversicherung | Primär |

**Vordefinierte Dimensionselement-Zuteilungsbasen** 

| Name  | Beschreibung        | Kostenelementdimension |
|-------|--------------------|------------------------|
| 10001 | Löhne           | Kostenelemente          |
| 10002 | Mitarbeiterversicherung | Kostenelemente          |

Im Hauptbuch wurden die folgenden Einträge gebucht:

- Die Einträge, die das Gehaltshauptkonto anzeigen, stammen aus dem Lohnabrechnungssystem und werden in den Kostenstellen gebucht.
- Die Ausgaben für Mitarbeiterversicherung werden manuell in eine standardmäßige Kostenstelle gebucht.

| Abschlussstichtag | Kostenstelle |  Beschreibung        | Hauptkonto |  Beschreibung       | Betrag in Buchhaltungswährung |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 03-01-2017      | CC001       | Personalverwaltung                  | 10001        | Löhne           | 2.000,00                      |
| 03-01-2017      | CC002       | FI                  | 10001        | Löhne           | 5.000,00                      |
| 03-01-2017      | CC003       | LU                  | 10001        | Löhne           | 3.000,00                      |
| 03-01-2017      | CC099       | Standardmäßige Kostenstelle | 10002        | Mitarbeiterversicherung | 1.000,00                      |

Nachdem die Daten importiert wurden, werden die folgenden Einträge in der Kostenrechnung erstellt.

**Kosteneinträge**

| Kostenobjekt |  Beschreibung        | Kostenelement  |  Beschreibung       | Kostenverhalten   |Betrag|Abschlussstichtag|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | Personalverwaltung                  | 10001         | Löhne           | Nicht klassifiziert    |2.000,00|  03-01-2017    |
| CC002       | FI                  | 10001         | Löhne           | Nicht klassifiziert    |5.000,00|     03-01-2017         |
| CC003       | LU                  | 10001         | Löhne           | Nicht klassifiziert    |3.000,00|      03-01-2017        |
| CC099       | Standardmäßige Kostenstelle | 10002         | Mitarbeiterversicherung | Nicht klassifiziert    |1.000,00|      03-01-2017       |

Dieses vereinfachte Beispiel zeigt, wie eine Kostenzuteilungsregel erstellt wird, um Kostenelement 10002 (Mitarbeiterversicherung) dem Saldo zuzuweisen, das auf Kostenelement 10001 (Ausgaben) eingetragen ist.

**Kostenverteilungsregel**

| Kostenobjekt-Dimensionshierarchieknoten | Kostenelement-Dimensionshierarchieknoten | Kostenverhalten | Verteilschlüssel |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Nicht klassifiziert  | 10001           |

**Gemeinkostenberechnung durchführen**

Nachdem das Kostenelement 10001 (Gehälter) als die Zuteilungsbasis angewendet wurde, lautet das Ergebnis der Gemeinkostenberechnung wie folgt.

| Kostenobjekt | Beschreibung | Größe |   Zuweisungsfaktor         | Betrag |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | Personalverwaltung          | 2.000     | (2.000 ÷ 10.000) × 1.000,00 | 200,00 |
| CC002       | FI          | 5.000     | (5.000 ÷ 10.000) × 1.000,00 | 500,00 |
| CC003       | LU          | 3.000     | (3.000 ÷ 10.000) × 1.000,00 | 300,00 |

**Erfassung**

| Erfassung | Journaltyp                          | Steuerkalenderperiode | Jahr | Periode   | Version                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Berechnung der Kostenverteilung | Steuerlich                 | 2017 | Periode 1 | Gemeinkostenberechnung / 01-02-2017 11:51:00 PM / Sachkonto /2017 / Periode 1 |

**Kostenobjektsaldo-Erfassungseinträge**

| Abschlussstichtag | Kostenobjekt | Beschreibung         | Kostenelement | Beschreibung        | Kostenverhalten |  Betrag  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31-01-2017      | CC099       | Standardmäßige Kostenstelle | 10002        | Mitarbeiterversicherung | Nicht klassifiziert  | 1.000,00 |

**Kosteneinträge**

| Kostenobjekt |  Beschreibung        | Kostenelement |    Beschreibung     | Kostenverhalten | Betrag    | Abschlussstichtag |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Standardmäßige Kostenstelle | 10002        | Mitarbeiterversicherung | Nicht klassifiziert  | -1.000,00 | 31-01-2017      |
| CC001       | Personalverwaltung                  | 10002        | Mitarbeiterversicherung | Nicht klassifiziert  | 200,00    | 31-01-2017      |
| CC002       | FI                  | 10002        | Mitarbeiterversicherung | Nicht klassifiziert  | 500,00    | 31-01-2017      |
| CC099       | LU                  | 10002        | Mitarbeiterversicherung | Nicht klassifiziert  | 300,00    | 31-01-2017      |

### <a name="example-2-use-a-statistical-dimension-member-as-the-allocation-base"></a>Beispiel 2: Verwenden eines Kostenelement-Dimensionsmitglieds als die Zuteilungsbasis

Statistische Dimensionsmitglieder können als Zuteilungsbasen verwendet werden, um Richtlinien zu definieren oder nicht-monetären Verbrauch durch Kostenobjekten zu melden. Sie können statistische Dimensionsmitglieder manuell erstellen oder sie aus einer Datei importieren, indem Sie das Datenverwaltungsimport-/-export-Tool verwenden.

**Mitglieder der statistischen Dimension**

| Name der statistischen Dimension | Statistisches Element | Beschreibung               | Einheit |
|----------------------------|---------------------|---------------------------|------|
| Statistische Elemente       | FTE                 | Vollzeitmitarbeiter       | St.   |
| Statistische Elemente       | Elektrizität         | Stromverbrauch   | kWh  |

Wenn ein statistisches Dimensionsmitglied gespeichert wird, wird ein entsprechender Datensatz in den vordefinierten Dimensionselement-Zuteilungsbasen erstellt.

**Vordefinierte Dimensionselement-Zuteilungsbasen**

| Name        | Beschreibung             | Statistische Elementdimension |
|-------------|-------------------------|-------------------------------|
| FTE         | Vollzeitmitarbeiter     | Statistische Elemente          |
| Elektrizität | Stromverbrauch | Statistische Elemente          |

Statistische Maßnahmen können aus verschiedenen Quellen stammen:

- Stromverbrauch kann mit Messgeräten gemessen werden, die in verschiedenen Bereichen des Unternehmens eingerichtet werden.
- In Tabellen werden statistische Messwerte angezeigt. Beispielsweise beinhaltet die HcmEmployment-Tabelle eine Liste aller Mitarbeiter und der Kostenstellen, für die sie arbeiten.

| Name       | Kostenstelle |  Beschreibung  | Arbeitskrafttyp |
|------------|-------------|----|-------------|
| Mitarbeiter A | CC001       | Personalverwaltung | Mitarbeiter    |
| Mitarbeiter B | CC002       | FI | Mitarbeiter    |
| Mitarbeiter C | CC002       | FI | Mitarbeiter    |
| Mitarbeiter D | CC003       | LU | Mitarbeiter    |
| Mitarbeiter F | CC003       | LU | Mitarbeiter    |

> [!NOTE]
> Alle Tabellen, die Finanzdimensionen enthalten, können als Quellen für statistische Maßnahmen verwendet werden.

Kostenrechnung unterstützt eine Sammlung von statistischen Maßnahmen, indem die folgenden Datenverbindungen verwendet werden:

- Tool für den Datenverwaltungsimport/-export
- Statistische Maßnahmen

Um statistischen Maßnahmen vom System abzurufen, ist eine Anbietervorlage für statistischen Maßnahmen erforderlich. Weitere Informationen finden Sie unter "Anbietervorlagen für statistische Maßnahmen". (Füge einen Link hinzu, sobald dieses Thema geschrieben ist.)

**Anbietervorlagen für statistische Maßnahmen**

| Name  | Funktion | Quelltabelle  | Summenfeld      | Datumsfeld     |
|-------|----------|---------------|----------------|----------------|
| FTES | Anzahl    | HcmEmployment | Nicht zutreffend | Nicht zutreffend |

Nachdem die Quelldaten für statistische Maßnahmen verarbeitet wurden, werden die folgenden Einträge in der Kostenrechnung erstellt.

**Statistische Einträge**

| Kostenobjekt | Beschreibung      | Abschlussstichtag | Statistisches Dimensionselement | Beschreibung         | Größe |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personalverwaltung               | 31-01-2017      | FTES                        | Vollzeitmitarbeiter | 1,00      |
| CC002       | FI               | 31-01-2017      | FTES                        | Vollzeitmitarbeiter | 2.00      |
| CC003       | LU               | 31-01-2017      | FTES                        | Vollzeitmitarbeiter | 2.00      |

Dies ist das Beispiel einer Kostenaufteilungsregel, wenn die vordefinierte Dimensionsmitglieds-Zuteilungsbasis der FTES als die Zuteilungsbasis darin zugewiesen wird.

| Kostenobjekt | Beschreibung  | Größe | Zuweisungsfaktor |
|-------------|------|-----------|-------------------|
| CC001       | Personalverwaltung   | 1,00      | (1/5) × Betrag    |
| CC002       | FI   | 2.00      | (2/5) × Betrag    |
| CC003       | LU   | 2.00      | (2/5) × Betrag    |

Sie können die Datenentität für die importierten statistischen Maßnahmen verwenden, um statistische Maßnahmen in die Kostenrechnung zu importieren. Sie können auch das Tool für den Datenverwaltungsimport/-export verwenden. In Excel wird der Stromverbrauch wie folgt erfasst.

| Abschlussstichtag | Dimensionsmitglied | Größe | Quellenbezeichner |
|-----------------|------------------|-----------|-------------------|
| 31-01-2017      | CC001            | 2,450.00  | Elektrizität       |
| 31-01-2017      | CC002            | 4,100.00  | Elektrizität       |
| 31-01-2017      | CC003            | 15.000,00 | Elektrizität       |

Nachdem die Quelldaten für statistische Maßnahmen verarbeitet wurden, werden die folgenden Einträge in der Kostenrechnung erstellt.

**Statistische Einträge**

| Kostenobjekt |    | Abschlussstichtag | Statistisches Dimensionselement |    Beschreibung          | Größe |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personalverwaltung | 31-01-2017      | Elektrizität                  | Stromverbrauch | 2,450.00  |
| CC002       | FI | 31-01-2017      | Elektrizität                  | Stromverbrauch | 4,100.00  |
| CC003       | LU | 31-01-2017      | Elektrizität                  | Stromverbrauch | 15.000,00 |

Dies ist das Beispiel einer Kostenaufteilungsregel, wenn die vordefinierte Dimensionsmitglieds-Zuordnungsbasis für Elektrizität als Zuordnungsbasis darin zugewiesen ist.

| Kostenobjekt | Beschreibung  | Größe | Zuweisungsfaktor          |
|-------------|------|-----------|----------------------------|
| CC001       | Personalverwaltung   | 2,450.00  | (2.450 ÷ 21.550) × Betrag  |
| CC002       | FI   | 4,100.00  | (4.100 ÷ 21.550) × Betrag  |
| CC003       | LU   | 15.000,00 | (15.000 ÷ 21.550) × Betrag |

## <a name="hierarchy-allocation-bases"></a>Hierarchiezuteilungsbasen

Kostenbuchalter können die Hierarchiezuordnungsbasen manuell erstellen, indem sie einen Kostenobjektdimensionshierarchieknoten in einer vorhandenen Zuordnungsbasis übernehmen. Auf diese Weise kann der Bereich der ursprünglichen vordefinierten Dimensionsmitglieds-Zuordnungsbasis eingeschränkt werden. Eine vordefinierter Dimensionsmitglieds-Zuordnungsbasis kann verwendet werden, um mehrere Hierarchiezuordnungsbasen zu erstellen. Bereiche können in der Kostenobjektdimensionshierarchie verwaltet werden, die den Hierarchiezuordnungsbasen zugeordnet ist.

### <a name="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization"></a>Beispiel: Hierarchiezuweisungsbasen, die auf Vollzeitmitarbeiter in der Organisation basieren
Dies ist das Beispiel einer Kostenobjektdimensionshierarchie, die erstellt werden kann, um einer vereinfachte Organisation zu beschreiben.

| Hierarchiename | Knotenebene 0 | Knotenebene 1 | Knotenebene 2 | Dimensionsmitglieder |
|----------------|--------------|--------------|--------------|-------------------|
| Organisation   | Geschäftsführer          | Leiter der Finanzabteilung          | FICO         | CC001             |
| Organisation   | Geschäftsführer          | Leiter der Finanzabteilung          | Personalverwaltung           | CC002             |
| Organisation   | Geschäftsführer          | PR-Leitung          | LU           | CC003             |

Die vordefinierte Dimensionsmitglieds-Zuordnungsbasis der FTES, die im vorherigen Abschnitt erstellt wurde, enthält die folgenden Einträge.

**Statistische Einträge**

| Kostenobjekt | Beschreibung  | Abschlussstichtag | Statistisches Dimensionselement | Beschreibung | Größe |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personalverwaltung   | 31-01-2017      | FTES                        | Vollzeitmitarbeiter | 1,00      |
| CC002       | FI   | 31-01-2017      | FTES                        | Vollzeitmitarbeiter | 2.00      |
| CC003       | LU   | 31-01-2017      | FTES                        | Vollzeitmitarbeiter | 2.00      |

Kosten müssen zwischen Kostenstellen verteilt werden, die dem Leiter der Finanzabteilung (CFO) der Organisation gemeldet werden. Es ist anerkannt, dass das korrekte Zuweisungsverhältnis die Anzahl der Vollzeitmitarbeiter (FTEs) nach Kostenstelle ist.

**Hierarchiezuteilungsbasen**

| Name                  | Verteilschlüssel | Kostenobjekt-Dimensionshierarchie | Kostenobjekt-Dimensionshierarchieknoten |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| Zahl der Vollzeitbeschäftigten unter dem Leiter der Finanzabteilung | FTES           | Organisation                    | Leiter der Finanzabteilung                                  |

Mit einer Vorschaufunktion kann die Hierarchiezuordnungsbasis, die auf Grundlage der statistischen Einträge im System erstellt wird, überprüft werden.

**Zuordnungsbasisdetails**

| Kostenobjekt | Beschreibung  |  Größe |
|-------------|------|------------|
| CC001       | Personalverwaltung   | 1,00       |
| CC002       | FI   | 2.00       |

Dies ist das Beispiel einer Kostenaufteilungsregel, wenn die Anzahl der FTES in der CFO-Hierarchie-Zuordungsbasis als Zuordungsbasis darin zugeordnet ist.

| Kostenobjekt | Beschreibung  | Größe | Zuweisungsfaktor |
|-------------|------|-----------|-------------------|
| CC001       | Personalverwaltung   | 1,00      | (1/3) × Betrag    |
| CC002       | FI   | 2.00      | (2/3) × Betrag    |

## <a name="formula-allocation-bases"></a>Formelzuteilungsbasen

Mit Formelzuordnungsbasen können Sie erweiterte Formeln definieren, um die korrekte Zuordnungsbasis zu erreichen. Sie können Formelzuordnungsbasen manuell erstellen.

Wenn Sie eine Formelzuordnungsbasis erstellen, wählen Sie aus, welche statistische Dimension und Kostenelement-Dimension die Grundlage für die Formel sein sollen. Alle Zuordnungsbasen, die aus der zuvor ausgewählten Dimensionen stammen, können in einer Formelzuordnungsbasis verwendet werden.

> [!NOTE]
> Zuvor definierte Formelzuordnungsbasen können verwendet werden, um eine neue Formelzuordnungsbasis zu definieren.

In den Faktoren der Formelzuteilungsbasen erstellen Sie ein Alias und ordnen es entweder einer Zuordnungsbasis oder einer Konstanten zu. Die Alias werden dann verwendet, um die Formel zu definieren.

Sie können die folgenden Operatoren verwenden, um die Formel zu definieren.

| Symbole | Text           |
|---------|----------------|
| ( )     | Klammern    |
| \<      | Kleiner als   |
| \>      | Größer als    |
| +       | Hinzufügung       |
| –       | Subtrahieren    |
| \*      | Multiplikation |

Traditionelle **IF**-Anweisungen werden nicht unterstützt. Allerdings können Sie Anweisungen erstellen und überprüfen, ob sie erfüllt sind.

| Aufstellung | Prüfung | Ergebnis |
|-----------|------------|--------|
| a \> b    | TRUE       | 1      |
| a \> b    | FALSE      | 0      |

### <a name="example-1-a-simple-formula"></a>Beispiel 1: Eine einfache Formel

Stromrechnungen bestehen oft aus zwei Teilen:

- Eine feste Gebühr für den Anschluss ans Netz
- Kosten, die dem Verbrauch pro kWh zugeordnet werden

Die vordefinierte Dimensionsmitglieds-Zuordnungsbasis für Strom ist bereits definiert und enthält diese Werte.

**Statistische Einträge**

| Kostenobjekt | Name | Abschlussstichtag | Statistisches Dimensionselement | Beschreibung             | Größe |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personalverwaltung   | 31-01-2017      | Elektrizität                  | Stromverbrauch | 2,450.00  |
| CC002       | FI   | 31-01-2017      | Elektrizität                  | Stromverbrauch | 4,100.00  |
| CC003       | LU   | 31-01-2017      | Elektrizität                  | Stromverbrauch | 15.000,00 |

Wenn die feste Gebühr jetzt gleichmäßig über Kostenobjekte verteilt werden muss, die Strom verbrauchen, haben Sie zwei Möglichkeiten für die Zuordnung der Kosten:

- Erstellen Sie die neue vordefinierte Zuordnungsbasis " Strom fix" und wenden Sie dann eine statistische Maßnahme von 1,00 für jedes Kostenobjekt an, das Strom verbraucht hat.
- Erstellen Sie die Formelzuordnungsbasis "Strom fix", die die vordefinierte Zuordnungsbasis für Strom nutzt, die bereits im System definiert wurde. Der Vorteil dieser Option ist, dass Daten nur für ein statistisches Dimensionsmitglied für Strom in die Kostenrechnung geladen werden muss.

**Formelzuordnungsbasis** 

| Name              | Kostenelementdimension | Statistische Dimension | Berechnungsgrundlage |
|-------------------|------------------------|-----------------------|---------|
| Strom fix |                        | Statistische Elemente  |         |

Bevor das Feld **Formel** ausgefüllt werden kann, müssen Sie den Alias angeben, der in der Formel verwendet werden soll.

**Faktoren der Formelzuordnungsbasis**

| Alias | Konstante | Verteilschlüssel |
|-------|----------|-----------------|
| a     |          | Elektrizität     |
| b     | 0,01     |                 |

Beachten Sie, dass 0 (null) nicht als Konstante unterstützt wird.

**Formelzordnungsbasis**

| Name              | Kostenelementdimension | Statistische Dimension | Berechnungsgrundlage |
|-------------------|------------------------|-----------------------|---------|
| Strom fix |                        | Statistische Elemente  | a \> b  |

Mit einer Vorschaufunktion kann die Formelzuordnungsbasis, die auf Grundlage der statistischen Einträge im System erstellt wird, überprüft werden.

**Zuordnungsbasisdetails**

| Kostenobjekt | Beschreibung  | Berechnungsgrundlage           | Größe |
|-------------|------|-------------------|-----------|
| CC001       | Personalverwaltung   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4.100,00 \> 0,01  | 1,00      |
| CC003       | LU   | 15.000,00 \> 0,01 | 1,00      |

Dies ist das Beispiel einer Kostenaufteilungsregel, wenn die vordefinierte Fomelzuordnungsbasis für Strom als die darin verwendete Zuordnungsbasis zugeordnet wird.

**Kostenobjektgrößen-Zuodnungfaktor**

| Kostenobjekt | Name | Größe |  Zuweisungsfaktor |
|-------------|------|-----------|--------------------|
| CC001       | Personalverwaltung   | 1,00      | (1/3) × Betrag     |
| CC002       | FI   | 1,00      | (1/3) × Betrag     |
| CC003       | LU   | 1,00      | (1/3) × Betrag     |

### <a name="example-2-an-advanced-formula"></a>Beispiel 2: Eine erweiterte Formel
Bei diesem Beispiel sollten die Kosten für Strom nicht nur dem tatsächlichen Stromverbrauch in kWH folgen. Verwaltung möchte einen Anreiz geschaffen, die Stromverwendung zu verringern. 

| Regel              | Satz | 
|-------------------|------|
| a <= 10000.00 kWh | 0.75 |
| a > 10000.00 kWh  | 1.15 |

Die neue Formelzuordnungsbasis "Stromverwendung" wird erstellt.

**Formelzuordnungsbasis**

| Name              | Kostenelementdimension | Statistische Dimension | Berechnungsgrundlage |
|-------------------|------------------------|-----------------------|---------|
| Stromnutzung |                        | Statistische Elemente  |         |

Bevor das Feld **Formel** ausgefüllt werden kann, müssen Sie den Alias angeben, der in der Formel verwendet werden soll.

**Faktoren der Formelzuordnungsbasis**

| Alias | Konstante  | Verteilschlüssel |
|-------|-----------|-----------------|
| a     |           | Elektrizität     |
| b     | 10.000,00 |                 |
| c     | 0.75      |                 |
| d     | 1.15      |                 |

**Formelzuordnungsbasis**

| Name              | Kostenelementdimension | Statistische Dimension | Berechnungsgrundlage                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Strom fix |                        | Statistische Elemente  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

Mit einer Vorschaufunktion kann die Formelzuordnungsbasis, die auf Grundlage der statistischen Einträge im System erstellt wird, überprüft werden.

**Zuordnungsbasisdetails**

| Kostenobjekt |    | Berechnungsgrundlage                                                                                                                             | Größe |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | Personalverwaltung | ((2.450.00 \> 10.000,00) × ((10.000,00 × 0,75) + (2.450.00 – 10.000,00) × 1,15)) + ((2.450.00 \<= 10.000,00) × 2.450.00 × 0,75)     | 1,837.50  |
| CC002       | FI | ((4.100.00 \> 10.000,00) × ((10.000,00 × 0,75) + (4.100.00 – 10.000,00) × 1,15)) + ((4.100.00 \<= 10.000,00) × 4.100.00 × 0,75)     | 3,075.00  |
| CC003       | LU | ((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) | 1,3250.00 |

Hier wird die Formel für CC003 (IT) genauer betrachtet:

((15.000,00 \> 10.000,00) × ((10.000,00 × 0,75) + (15.000,00 – 10.000,00) × 1,15)) + ((15.000,00 \<= 10.000,00) × 15.000,00 × 0,75) = 13.250,00

(1 × (7.500,00 + 5.000,00 × 1,15)) + (0 × 15.000,00 × 0,75)            

1 × 7.500,00 + 5.750,00 + 0 

Dies ist das Beispiel einer Kostenaufteilungsregel, wenn die vordefinierte Fomelzuordnungsbasis für "Strom fix" als die darin verwendete Zuordnungsbasis zugewiesen wird.


| Kostenobjekt | Beschreibung | Größe |        Zuweisungsfaktor         |
|-------------|-------------|-----------|----------------------------------|
|    CC001    |     Personalverwaltung      | 1,837.50  | (1.837,50 ÷ 18.162,50) × Betrag  |
|    CC002    |     FI      | 3,075.00  | (3.075,00 ÷ 18.162,50) × Betrag  |
|    CC003    |     LU      | 13,250.00 | (13.250,00 ÷ 18.162,50) × Betrag |


