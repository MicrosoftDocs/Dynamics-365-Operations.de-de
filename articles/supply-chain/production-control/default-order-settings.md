---
title: Standardauftragseinstellungen für Dimensionen und Produktvarianten
description: Standardauftragseinstellungen definieren den Standort und Lagerort, aus dem Artikel bezogen oder in dem sie gelagert werden, die Mindest-, Höchst-, Mehrfach- und Standardmengen, die für den Handel oder die Lagerverwaltung verwendet werden, die Lieferzeiten, das Beendigungskennzeichen sowie die Auftragszusagemethode.
author: t-benebo
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 13df8eb7873495847d994922be1acd77e57f8f23
ms.sourcegitcommit: dfe5916d982eaa879e2afef7440c30b1d0f4380a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/29/2020
ms.locfileid: "3637755"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Standardmäßige Auftragseinstellungen für Dimensionen und Produktvarianten

[!include [banner](../includes/banner.md)]

Standardauftragseinstellungen in Dynamics 365 Supply Chain Management definieren den Standort und Lagerort, aus dem Artikel bezogen oder an dem sie gelagert werden, die Mindest-, Höchst-, Mehrfach- und Standardmengen, die für den Handel oder die Lagerverwaltung verwendet werden, die Lieferzeiten, das Beendigungskennzeichen sowie die Auftragszusagemethode. Standardauftragseinstellungen werden verwendet, wenn Bestellungen, Aufträge, Umlagerungsaufträge, Bestandsjournale erstellt werden, sowie durch den Produktprogrammplan für die Generierung geplanter Aufträge. Standardauftragseinstellungen können artikelspezifisch, standortpsezifsch, produktvariantenspezfisch oder produktdimensionsspezifisch sein.

Sie können die Standardauftragseinstellungen auf der Seite **Standardauftragseinstellungen** definieren. Um diese Seite zu öffnen, gehen Sie zu **Produktinformationsverwaltung** &gt; **Produkte** &gt; **Freigegebene Produkte** &gt; **Ein freigegebenes Produkt auswählen** &gt; im **Plan**. Sie können auch auf **Bestand verwalten** &gt; **Auftragseinstellungen** &gt; **Standardauftragseinstellungen** gehen.

## <a name="default-order-settings"></a>Standardauftragseinstellungen

Es gibt drei Typen von Standardauftragseinstellungen für Einkäufe, Verkäufe und den Bestand. Die Standardauftragseinstellungen für Einkäufe werden verwendet, wenn Folgendes erstellt wird:

- Bestellpositionen
- Rahmenbestellungspositionen
- Angebotsanforderungspositionen
- Bestellanforderungspositionen
- Lieferungswiederbeschaffungspositionen
- Geplante Einkaufsbestellungen

Die Standardauftragseinstellungen für Verkäufe werden verwendet, wenn Folgendes erstellt wird:

- Auftragspositionen
- Kaufvertragspositionen
- Verkaufsangebotspositionen
- Rücklieferungspositionen und Artikelersetzungspositionen
- Bedarfsplanungspositionen

Die Standardauftragseinstellungen gelten auch beim Erstellen von:

- Projektartikelanforderungen
- Artikelbedarf für Serviceauftrag

Die Standardauftragseinstellungen für den Bestand werden verwendet, wenn Folgendes erstellt wird:

- Lagererfassungen
- Umlagerungsaufträge
- Geplante Umlagerungsaufträge

Die Standardlagerauftragseinstellungen gelten auch beim Erstellen von:

- Quarantäneaufträge
- Qualitätsprüfungsaufträge
- Produktionsaufträge
- Stücklistenpositionen
- Geplante Produktionsaufträge

## <a name="full-definition-of-a-released-product"></a>Vollständige Definition eines freigegebenen Produkts

Wenn Sie eine Buchung erstellen, müssen Sie die vollständige Definition eines veröffentlichten Produkts auf der Position angeben, damit Supply Chain Management versucht, die Standardauftragseinstellungen zu identifizieren. Die vollständige Definition des freigegebenen Produkts bedeutet, dass alle aktiven Artikelnummer und Produktdimensionen, beispielsweise Konfiguration, Größe, Farbe, Stil und für die Buchung angegeben werden. Wenn Sie beispielsweise manuell eine Bestellposition für eine freigegebene Produktvariante erstellen, müssen Sie alle erforderlichen Produktdimensionen angeben, bevor der Standort, Lagerort, die Menge sowie die Lieferzeit standardmäßig in der Auftragsposition angezeigt werden. 

Nicht alle Standardauftrags-Einstellungsparameter werden angewendet, wenn Auftrags- oder Erfassungspositionen erstellt werden. Mengen und Lieferzeiten werden nur standardmäßig angezeigt, sofern zutreffend. Wenn beispielsweise eine Erfassungsposition gezählt wird, werden nur der Standort und der Lagerort standardmäßig angezeigt, wenn die Position erstellt wird. Deshalb wird keine Standardmenge ober Überprüfung auf Mehrfache und Minimums ausgeführt, wenn die Position erstellt oder die Erfassung gebucht wird. 

Das System versucht immer, einen Standardstandort und -lagerort zu finden, wenn eine Auftrags- oder Erfassungsposition erstellt wird Der Standort wird nicht immer standardmäßig von den Auftragseinstellungen angezeigt. Wenn Sie beispielsweise einen Auftrag oder eine Bestellung erstellen, wird der Standort aus dem Auftragskopf automatisch in den Auftragspositionen verwendet. Wird eine Stücklistenposition erstellt, wird der Standort aus dem Stücklistenkopf verwendet. Nachdem der Standort bestimmt wurde, werden mit ihm alle standordspezifischen Auftragseinstellungen gesucht, die dann als Standard für den Lagerort verwendet werden können. 

Der Standardauftragstyp, Einkauf und die Bestandslieferzeiten können von den Dispositionsregeln des Artikels auf die **Artikeldeckung**-Seite überschrieben werden. Zwar werden die Standardauftragseinstellungen nicht für die Unterscheidung zwischen der Produktion und der Übergangslieferzeit zugelassen, aber die Artikeldeckungsregeln lässt sie zu. Allerdings werden die Artikeldeckungseinstellungen nur von der Produktprogrammplanung (MRP) verwendet, wenn geplante Produktions- und geplante Übertragungsaufträge erstellt werden, und sie werden nicht angewendet, wenn Produktions- und Übertragungsaufträge manuell erstellt werden. 

## <a name="default-order-settings-rules"></a>Standardmäßige Auftragseinstellungsregeln

Sie können allgemeine Standardauftragseinstellungen und jede Anzahl von Standardauftragseinstellungsregeln definieren, die nur unter bestimmten Umständen gelten, wie beispielsweise Standort oder eine spezifische Produktdimension oder Produktdimensionskombination. Sie können keine lagerortspezifischen Auftragseinstellungen definieren.

### <a name="rank-in-default-order-settings"></a>Nach standardmäßige Auftragseinstellungen einen Rang zuweisen

Die Standardauftrags-Einstellungsregeln haben Ränge. Je höher der Rang, desto wichtiger ist die Regel. Das bedeutet, dass sie eine höhere Priorität hat und vor den Regeln mit niedrigeren Rängen verwendet wird. Die allgemeinen Standardauftragseinstellungen haben den Rang null, der nicht geändert werden kann. Es kann nur eine Regel mit dem Rang null vorhanden sein. Regeln können denselben Rang haben, vorausgesetzt, dass die Dimensionen, die diese anwenden, um diese zu unterscheiden. Dies ist nützlich für die Modellierung von standordspezifischen Auftragseinstellungen. Wenn eine neue Standardauftrags-Einstellungsregel erstellt wird, werden die Werte für Auftragswerte, Beendigungskennzeichen usw. von der Regel mit Rang null geerbt, können aber überschrieben werden.

### <a name="default-order-settings-for-released-products"></a>Standardmäßige Auftragseinstellungen für freigegebene Produkte

Für eindeutig identifizierbare, freigegebene Produkte können Sie allgemeine Auftragseinstellungen oder standortspezifische Auftragseinstellungen definieren. Die allgemeinen Auftragseinstellungen haben immer den Rang null. Wenn Sie neue Verkaufs-, Einkaufs- und Lagerauftragseinstellungen zur gleichen Zeit einrichten, sollten Sie die **Detailansicht** auf der Seite **Standardauftragseinstellungen** verwenden. Um zur Detailansicht zu wechseln, gehen Sie auf **Optionen** &gt; **Seitenoptionen** &gt; **Ansicht wechseln** &gt; **Detailansicht**.

### <a name="site-specific-order-settings"></a>Standortspezifische Auftragseinstellungen

Um standortspezifische Auftragseinstellungen zu erstellen, wählen Sie **Neu**. Füllen Sie in der **Detailansicht** den Standort im Feld **Standort** unter &gt; **Einstellungen gültig für** aus. Füllen Sie in der **Rasteransicht** den Standort in der Spalte **Standort** aus. Die neue Regel ruft automatisch einen neuen Rangwert ab, der über null liegt. Sie können so viele standortspezifische Regeln wie erforderlich erstellen und allen standortspezifischen Regeln denselben Rang zuweisen, um zu modellieren, dass sie gleich wichtig sind. 

Wenn Sie sich in der **Detailansicht** befinden, können Sie die Übersicht der Regeln nicht erhalten, die für den Artikel erstellt wurden. Benutzen Sie die Schaltfläche **Liste anzeigen/ausblenden**, um Übersichtsinformationen anzuzeigen. Wenn eine Auftragsposition eines beliebigen Typs erstellt wird und für sie kein Standort bereitgestellt ist, sucht Supply Chain Management nach einer Regel, bei der kein Standort angegeben ist. Dies kann dazu beitragen, einen Standardstandort in der Auftragsposition zu verwenden. Dieser Standort wird dann verwendet, um nach einer standortspezifischen Regel zu suchen, bei der möglicherweise ein Standardlagerort festgelegt wurde. Dieser Lagerort wird auf die Auftragsposition angewendet.

### <a name="specific-order-settings-for-product-dimension"></a>Spezifische Auftragseinstellungen für Produktdimension

Sie können Auftragseinstellungsregeln für jede aktive Produktdimension oder Kombination aus aktiven Produktdimensionen definieren. Wenn ein Produktdimensionsfeld leer ist, gilt diese Regel für alle Werte der Produktdimension. 

Berücksichtigen Sie das folgende Beispielprodukt.

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Produktname**                                    | Photoelektrischer Sensor                    |
| **Artikelnummer**                                     | XW56                                    |
| **Konfiguration** (wird verwendet, um den Typ des Lichts zu modellieren) | C1-sichtbares rotes Licht, C2-Infrarotlicht |
| **Stil** (wird zum Modellieren der Techniküberarbeitung verwendet)  | R1, R2, R3                              |

Nehmen Sie für dieses Beispiel an, dass das Produkt beschafft und nicht produziert wird. Nehmen Sie außerdem an, dass die Konfiguration C1 häufiger verwendet wird, sodass es kürzere Lieferzeiten hat. 

Erstellen Sie folgende Standardauftragseinstellungen, um dieses Szenario zu modellieren.

| Rang | Standort | Variante | Formatvorlage | Einkauf – Standardeinstellungen überschreiben | Lieferzeit Einkauf | Einkauf – Angehalten | Vertrieb – Standardeinstellungen überschreiben | Vertrieb – Angehalten |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Wenn eine Bestellposition oder eine geplante Einkaufsbestellung für XW56, Konfiguration C1, erstellt wird, wird die Lieferzeit als 2 behandelt, unabhängig von der Überarbeitung oder dem Standort, wo die Position platziert wird. Nehmen Sie an, dass alle Überarbeitungen, außer R3, angehalten werden.

Sie können die folgenden standardmäßigen Auftragseinstellungsregeln erstellen.

| Rang | Standort | Variante | Formatvorlage | Einkauf – Standardeinstellungen überschreiben | Lieferzeit Einkauf | Einkauf – Angehalten | Vertrieb – Standardeinstellungen überschreiben | Vertrieb – Angehalten |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 20   |      |               | R1    | Ja                                  |                    | Ja                | Ja                               | Ja             |
| 10   |      | C1            |       | Ja                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Die zwei Regeln für die Beendigung der alten Überarbeitungen haben dieselbe Bewertung, was bedeutet, dass sie gleich wichtig sind. Alle beide haben einen höheren Rang als die Regel für Konfiguration C1, was bedeutet, dass sie den Vorrang vor der Regel für Konfiguration C1 haben. 

In diesem Beispiel wird die Anforderung für den Rang erklärt. Wenn eine Bestellung für Konfiguration C1 und Überprüfung R2 erstellt wird, wären bei fehlendem Rang die beiden Regeln, die für R2 und C1 definiert werden, mehrdeutig. Um die Mehrdeutigkeit aufzuheben, durchsucht Supply Chain Management die Regeln in absteigender Rangreihenfolge und wendet die erste anwendbare Regel an. Im aktuellen Beispiel, wenn eine Bestellposition für Konfiguration C1 und Überarbeitung R2 erstellt wird, erhält der Benutzer eine Warnmeldung, dass der Artikel gesperrt ist und dass dies durch den Überarbeitungswert verursacht wird. Wenn die Regel für die Konfiguration größer wäre, als diejenige für die Überarbeitung, dann wäre die Erstellung einer Bestellposition für Konfiguration C1 und Überarbeitung R2 erfolgreich gewesen, und der Benutzer hätte keine Meldung „Artikel gesperrt“ erhalten. 

Berücksichtigen Sie die folgenden standardmäßigen Auftragseinstellungsregeln.

| Rang | Standort | Variante | Formatvorlage | Standardstandort | Standardlagerort | Einkauf – Standardmäßige Lagerdimensionen überschreiben | Lagerort für Einkauf |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ja                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Das System reicht die Sätze von Regeln zweimal weiter, um den Standort und Lagerort zu bestimmen. Wenn eine Bestellposition für Variante C1, Stil R2 konfiguriert wird, wird der Standort basierend auf der Grundlage der Regel mit Rang 10 bestimmt. Dann sucht das System nach einer Regel für Standort 2, um einen Lagerort zu bestimmen. Regel 20 wird gefunden und da sie einen höheren Rang hat, wird der Lagerort in der Bestellposition 22 und nicht 21 sein.

Als allgemeinen Leitfaden erhalten spezifische Regeln und Regeln für Dimensionen, die wichtiger als andere Dimensionen sind, höhere Ränge, während generischere Regeln niedrigere Ränge erhalten. 

Die Regel mit Rang null dient als Sicherheitsnetz. Wenn keine anderen Regeln betroffen sind, dann werden die Standardauftragseinstellungen von Regel null verwendet. 

Da die Rangnummer wichtig ist, befinden sich im Aktionsbereich **Standardauftragseinstellungen** Funktionen, um eine Regel nach oben oder unten zu verschieben und um die Regeln neu zu nummerieren, sodass sie immer in Abstufungen von 10 sind. 

Die Anzahl von Regeln, die für ein freigegebenes Produkt erstellt werden, sind möglicherweise viele. Um besser zu verstehen, was jede Regel überschreibt und warum es notwendig ist, empfehlen wir Ihnen, die **Rasteransicht** auf der Seite **Standardauftragseinstellungen** zu verwenden. Sie können die Rasteransicht aktivieren, indem Sie zu **Optionen** &gt; **Seitenoptionen** &gt; **Ansicht wechseln** &gt; **Rasteransicht** wechseln. Die Anzahl der im Raster angezeigten Spalten könnte ziemlich bedeutsam sein, insbesondere für die Registerkarten "Vertrieb" und "Bestand". Um die Anzahl der im Raster angezeigten Spalten einzuschränken, können Gruppen von Spalten ausgeblendet oder angezeigt werden, indem die Schaltflächen im Menü **Standardauftragseinstellungen** &gt; **Spaltenanzeige** verwendet werden.

### <a name="specific-order-settings-for-released-product-variant"></a>Spezifische Auftragseinstellungen für freigegebene Produktvariante

Wenn das Regelsystem für Standardauftragseinstellungen zu lästig ist, dann gibt es die Option, Standardauftragseinstellungen für jede Produktvariante zu definieren. Im folgenden Beispiel wird gezeigt, wie dies für das Produkt und die oben beschriebenen Fälle aussieht.

| Rang | Standort | Variante | Formatvorlage | Einkauf – Standardeinstellungen überschreiben | Lieferzeit Einkauf | Einkauf – Angehalten | Vertrieb – Standardeinstellungen überschreiben | Vertrieb – Angehalten |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Ja                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C2            | R1    | Ja                                  | 5                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R3    | Ja                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 10   |      | C1            | R1    | Ja                                  | 2                  | Ja                | Ja                               | Ja             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

In diesem Fall ist der Rang tatsächlich unerheblich, sodass Sie ihn ausblenden können. Diese Lösung führt möglicherweise zu einem Wartungsproblem. Möglicherweise empfiehlt es sich jedoch, diese Einstellung zu verwenden, wenn Sie in Erwägung ziehen, eine Integration mit Product-Lifecycle-Management-Systemen (PLM-Systemen) vorzunehmen.

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Verwenden Sie eine strikte oder Standardüberprüfung der Standardbestellmengen

Sie können wählen, wie streng das System bei der Überprüfung der im Feld **Standardauftragseinstellungen** für ein Produkt eingegebenen Mengen sein soll. Wenn Sie die neue strenge Option verwenden, muss die **Standardbestellmenge** immer ein Mehrfaches des angegebenen **Mehrfach**-Wert für Bestellungen, Bestand und Kundenaufträge sein. Wenn Sie eine strikte Überprüfung verwenden, können Sie keine Standardauftragseinstellungen speichern, die diese Anforderung nicht erfüllen (und in der Meldungsleiste wird ein Fehler angezeigt). 

Es gilt eine strikte Überprüfung für Werte der **Standardbestellmenge**, die in den Inforegistern **Bestellung**, **Bestand** und **Auftrag** der Seite **Standardauftragseinstellungen** festgelegt sind. Jedes Inforegister hat seine eigene **Mehrfach**-Einstellung, die zur Überprüfung des Werts der **Standardbestellmenge** für dieses Inforegister verwendet wird.

### <a name="enable-the-strict-validation-option"></a>Strikte Überprüfung aktivieren

Bevor Sie die strikte Überprüfung nutzen können, muss sie auf Ihrem System aktiviert werden. Administratoren können die Seite [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) verwenden, um den Status der Funktion zu überprüfen und sie bei Bedarf zu aktivieren. Hier wird die Funktion als aufgeführt:

- **Modul** - *Produktinformationsverwaltung*
- **Funktionsname** - *Strikte Überprüfung von Standardbestellmengen*

### <a name="set-the-validation-option"></a>Überprüfungsoption festlegen

Um die Überprüfungsoption festzulegen:

1. Gehen Sie zu **Produktinformationsverwaltung \> Einrichten \> Parameter für Produktinformationsverwaltung**.
1. Auf der Registerkarte **Allgemeines** legen Sie unter **Überprüfung von Standardbestellmengen** einen der folgenden Werte fest:
    - **Strikt** – Wählen Sie diese Option, um sicherzustellen, dass alle Werte der **Standardbestellmenge** ein Mehrfaches des Werts **Mehrfach** des jeweiligen Inforegisters (**Bestellung**, **Bestand** und **Auftrag**) sind.
    - **Standard** – Wählen Sie diese Option aus, um die Standardüberprüfung zu verwenden (dies funktioniert genauso, wenn diese Funktion nicht aktiviert ist).
