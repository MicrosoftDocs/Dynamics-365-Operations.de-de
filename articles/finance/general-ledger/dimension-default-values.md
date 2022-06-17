---
title: Standardfinanzdimensionen für Finanzerfassungen
description: In diesem Artikel werden die Regeln beschrieben, die definieren, wie Finanzdimensionswerte für Transaktionen festgelegt werden, die über Finanzerfassungen eingegeben werden. Es enthält auch Details für Szenarien, in denen feste Dimensionen verwendet werden.
author: kweekley
ms.date: 09/04/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransDaily, LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d0fcf836e22207baae562801fb082d735df0f96
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907921"
---
# <a name="default-financial-dimensions-on-financial-journals"></a>Standardfinanzdimensionen für Finanzerfassungen

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Regeln beschrieben, die definieren, wie Finanzdimensionswerte für Transaktionen festgelegt werden, die über Finanzerfassungen (jedoch nicht über Lagererfassungen oder Projekterfassungen) eingegeben werden. Es enthält auch Details für Szenarien, in denen feste Dimensionen verwendet werden.

## <a name="symptom"></a>Symptom

Die Finanzdimensionswerte werden nicht wie erwartet für das Konto oder das Gegenkonto in einer Finanzerfassung festgelegt. Die folgenden Szenarien bieten zwei Beispiele:

Ein Beleg wird in eine Erfassung oder allgemeine Erfassung eingegeben. Das Konto ist ein Kreditorenkonto und das Gegenkonto ist ein Bankkonto. Die Finanzdimensionen des Kreditors werden standardmäßig im Konto eingegeben, die Finanzdimensionen der Bank werden jedoch nicht standardmäßig im Gegenkonto eingegeben. Stattdessen werden die Dimensionswerte aus dem Konto standardmäßig in das Gegenkonto eingegeben.

Einem Debitor sind standardmäßige Finanzdimensionswerte zugewiesen, und einem Umsatzhauptkonto ist ein fester Dimensionswert für die Finanzdimension „Abteilung“ zugewiesen. Ein Beleg wird in eine allgemeine Erfassung eingegeben.  Das Konto ist der Debitor und das Gegenkonto ist ein Sachkonto, insbesondere das Umsatzkonto mit dem festen Dimensionswert. Die feste Dimension ist nicht auf das Gegenkonto für das Umsatzhauptkonto festgelegt. Stattdessen wird es auf den Dimensionswert „Abteilung“ des Kontos festgelegt, das vom Debitor stammt.  Nach dem Buchen des Belegs wird der feste Dimensionswert für den gebuchten Buchhaltungseintrag verwendet, aber der Beleg zeigt weiterhin den Abteilungswert des Debitors auf dem Umsatzkonto an. 

Welche Regeln gelten für Finanzdimensionswerte, die auf Belegen innerhalb einer Erfassung festgelegt werden?

## <a name="resolution"></a>Lösung

Die folgenden Regeln werden umgesetzt, um Finanzdimensionswerte standardmäßig in die Positionen eines Belegs in Finanzerfassungen einzugeben, z. B. die allgemeine Erfassung oder die Kreditorenrechnungserfassung. 

1. **Erfassungskopf**

   - Die Erfassungskopfdimensionen für Erfassungen werden standardmäßig aus den Dimensionen des Erfassungsnamens entnommen.

2. **Erfassungspositionskonto**

   - Die Erfassungspositions-Kontodimensionen werden standardmäßig aus den Dimensionen des Erfassungskopfes entnommen.
   - Wenn Finanzdimensionen leer sind, werden ihre Werte standardmäßig aus Debitoren-, Kreditoren-, Bank-, Anlage-, Projekt- oder Sachkontodimensionen eingegeben.

     - Wenn der Kontotyp **Sachkonto** ist, wird eine feste Dimension eines Sachkontos bei der Transaktionserfassung wie eine Standarddimension behandelt.
     - Wenn der Kontotyp **Debitor**, **Kreditor**, **Bank**, **Anlage** oder **Projekt** ist, kann das Hauptkonto noch nicht ermittelt werden. Daher wird standardmäßig nie eine feste Dimension für das Konto eingegeben.

3. **Erfassungspositions-Gegenkonto**

 - Die Erfassungspositions-Gegenkontodimensionen werden standardmäßig aus den Dimensionen des Erfassungspositionskontos entnommen.

 - Wenn Finanzdimensionen leer sind, wird der nächste Standardeintrag aus den Standarddimensionen der Debitoren-, Kreditoren-, Bank-, Anlage-, Projekt- oder Sachkontodimensionen entnommen.
   1. Wenn der Gegenkontotyp **Sachkonto** ist, wird eine feste Dimension eines Sachkontos bei der Transaktionserfassung wie eine Standarddimension behandelt. Wenn bereits standardmäßig ein Dimensionswert aus dem Konto übernommen wurde, überschreibt der Standardwert oder der feste Dimensionswert des Hauptkontos nicht den vorhandenen Wert.
   2. Wenn der Gegenkontotyp **Debitor**, **Kreditor**, **Bank**, **Anlage** oder **Projekt** ist, ist das Hauptkonto noch nicht bekannt, daher wird für das Gegenkonto nie standardmäßig eine feste Dimension verwendet.

4. **Buchung**

    1. Beim Buchen wird das Hauptkonto für jede Zeile des Buchhaltungspostens (sowohl für das Konto als auch für das Gegenkonto) ausgewertet, um festzustellen, ob es einen festen Dimensionswert gibt. Wenn eine feste Dimension definiert ist, werden alle vorhandenen oder leeren Werte durch diese feste Dimension ersetzt.

        Der feste Dimensionswert wird nach der Buchung **nicht** in den Erfassungspositionen angezeigt. Stattdessen wird er auf dem Buchhaltungseintrag angezeigt, wenn Sie den Beleg nach der Buchung anzeigen.

    2. Beim Buchen werden standardmäßig keine anderen Dimensionswerte eingegeben, einschließlich zusätzlicher Sachkonten, die während des Buchens hinzugefügt werden könnten, z. B. Centrundungskonten und Intercompany-Konten des Typ „Fällig bis“ oder „Fällig von“. Die Standarddimensionseinträge für zusätzliche Sachkonten werden aus dem Konto oder den Gegenkonten übernommen.

Für die standardmäßige Eingabe von Dimensionswerten kann der Erfassungsstandardprozess nicht feststellen, ob ein leerer Dimensionswert absichtlich leer gelassen wurde oder ob der Standardeintrag nicht vorgenommen wurde. Wenn ein Dimensionswert absichtlich leer gelassen wird, kann ein Wert dennoch standardmäßig in der zuvor beschriebenen Standardreihenfolge eingegeben werden. Wenn Sie für eine Dimension einen leeren Wert benötigen, müssen Sie möglicherweise eine Dimension mit einem Wert von **0** (null) oder **Leer** erstellen, sodass dies anstelle einer leeren Dimension verwendet werden kann.

Sehen Sie sich die folgenden Szenarien an, um Beispiele für die Standardreihenfolge der Finanzdimension zu erhalten.

### <a name="scenario-1"></a>Szenario 1

Wechseln Sie zu **Hauptbuch \> Erfassungseinstellungen \> Journale**, und wählen Sie den Erfassungsnamen **GenJrn** aus. Definieren Sie dann auf dem Inforegister **Finanzdimensionen** die folgenden Werte für die Standardfinanzdimensionen:

- **BUSINESSUNIT:** 001
- **DEPARTMENT:** 024

[![Seite „Journale“](./media/financial-dimension-defaulting-jrnl-names-01.png)](./media/financial-dimension-defaulting-jrnl-names-01.png)

Wechseln Sie zu **Hauptbuch \> Erfassungseinträge \> Allgemeine Erfassung**, und erstellen Sie eine neue allgemeine Erfassung mit dem Erfassungsnamen **GenJrn**. Die Dimensionen werden standardmäßig vom Erfassungsnamen (LedgerJournalName-Tabelle) bis zum Erfassungskopf (LedgerJournalTable-Tabelle) eingegeben, wie auf der Registerkarte **Finanzdimensionen** dargestellt.

[![Registerkarte „Finanzdimensionen“ auf der Seite „Allgemeine Erfassungen“](./media/financial-dimension-defaulting-genrl-jrnl-02.png)](./media/financial-dimension-defaulting-genrl-jrnl-02.png)

Wechseln Sie zu den **Positionen**. Wählen Sie im Feld **Kontotyp** die Option **Sachkonto** aus, und geben Sie dann im Feld **Konto** den Wert **170150** ein. Drücken Sie dann die **TAB-TASTE**, um das Feld zu verlassen. Die Dimensionen werden standardmäßig aus dem Erfassungskopf entnommen. Daher wird der Wert **Konto** als **170150-001-024** angezeigt.

[![Erfassungspositionen für eine allgemeine Erfassung auf der Seite „Erfassungsbeleg“](./media/financial-dimension-defaulting-jrnl-vchr-03.png)](./media/financial-dimension-defaulting-jrnl-vchr-03.png)

Ändern Sie den Wert für **Konto** in **170150-001-023**. Geben Sie entweder einen Soll- oder einen Habenbetrag ein. Wählen Sie im Feld **Gegenkontotyp** die Option **Sachkonto** aus, und geben Sie dann im Feld **Gegenkonto** den Wert **600150** ein. Die Dimensionswerte werden standardmäßig aus dem Konto entnommen. Daher wird der Wert **Gegenkonto** als **600150-001-023** angezeigt.

### <a name="scenario-2"></a>Szenario 2

Verwenden Sie dieselben Finanzdimensionen, die Sie in Szenario 1 für den Erfassungsnamen definiert haben. Im nächsten Schritt wechseln Sie zu **Debitorenkonten \> Debitoren \> Alle Debitoren** und definieren Standardwerte für die Finanzdimension für den Debitor „US-001“. Wählen Sie den Debitor aus, um die Debitorendetails zu öffnen. Behalten Sie auf der Registerkarte **Finanzdimensionen** den Standardwert für die Dimension **BUSINESSUNIT** (**001**) bei. Ergänzen Sie die Dimension **COSTCENTER**, und geben Sie den Wert **007** ein.

Erstellen Sie eine neue allgemeine Erfassung mit dem Erfassungsnamen **GenJrn**. Ändern Sie auf der Registerkarte **Finanzdimensionen** den Standardwert für **BUSINESSUNIT** von **001** in **002**.

Wechseln Sie zu den **Positionen**. Wählen Sie im Feld **Kontotyp** die Option **Debitor** aus, und geben Sie dann im Feld **Konto** den Wert **US-001** ein. Wählen Sie **Finanzdimensionen \> Konto** aus, um die Finanzdimensionen für Nicht-Sachkontotypen anzuzeigen. Die folgenden Standardeinträge für die Finanzdimensionswerte werden eingegeben:

- **BUSINESSUNIT:** 002 – Der Standardeintrag wird aus dem Erfassungskopf entnommen. Der Wert **001** wird in der Standardeinstellung nicht aus dem Debitor „US-001“ übernommen, da bereits ein Standardwert eingegeben wurde.
- **COSTCENTER:** 007 – Der Standardeintrag wird aus der Konfiguration des Debitors „US-001“ übernommen.
- **DEPARTMENT:** 024 – Der Standardeintrag wird aus dem Erfassungskopf entnommen.

Wählen Sie dann wieder in der Position **Gegenkontotyp** und **Sachkonto** aus, und geben Sie dann im Feld **Gegenkonto** den Wert **600150** ein. Die folgenden Standardeinträge für die Finanzdimensionswerte werden in der Position eingegeben:

- **BUSINESSUNIT:** 002 – Der Standardeintrag wird aus den Finanzdimensionen des Kontos übernommen. (Er wurde ursprünglich standardmäßig aus dem Erfassungskopf übernommen.)
- **DEPARTMENT:** 024 – Der Standardeintrag wird aus den Finanzdimensionen des Kontos übernommen. (Er wurde ursprünglich standardmäßig aus dem Erfassungskopf übernommen.)
- **COSTCENTER:** 007 – Der Standardeintrag wird aus den Finanzdimensionen des Kontos übernommen. (Er wurde ursprünglich standardmäßig aus dem Debitor übernommen.)

### <a name="scenario-3"></a>Szenario 3

Fügen Sie in derselben Erfassung, die Sie für Szenario 2 verwendet haben, eine neue Position hinzu. Wählen Sie im Feld **Kontotyp** die Option **Sachkonto** aus, und geben Sie dann im Feld **Konto** den Wert **170150** ein. Löschen Sie die Standarddimensionswerte, sodass nur das Hauptkonto 170150 übrig bleibt. Wählen Sie im Feld **Gegenkontotyp** die Option **Debitor** aus, und geben Sie dann im Feld **Gegenkonto** den Wert **US-001** ein. Die folgenden Standardeinträge für die Finanzdimensionswerte werden eingegeben:

- **BUSINESSUNIT:** 002 – Der Standardeintrag wird aus dem Erfassungskopf übernommen, da der Kontodimensionswert leer ist. Der Wert **001** wird in der Standardeinstellung nicht aus dem Debitor „US-001“ übernommen, da bereits ein Standardwert aus dem Erfassungskopf übernommen wurde. Wenn der Wert **BUSINESSUNIT** absichtlich leer gelassen wurde, müssen Sie auch die Finanzdimension aus dem Gegenkonto entfernen.
- **COSTCENTER:** 007 – Der Standardeintrag wird dem Debitor „US-001“ entnommen, da der Kontodimensionswert und der Dimensionswert des Erfassungskopfes leer sind. Wenn der Wert **COSTCENTER** absichtlich leer gelassen wurde, müssen Sie auch die Finanzdimension aus dem Gegenkonto entfernen.
- **DEPARTMENT:** 024 – Der Standardeintrag wird aus dem Erfassungskopf übernommen, da der Kontodimensionswert leer ist. Wenn der Wert **DEPARTMENT** absichtlich leer gelassen wurde, müssen Sie auch die Finanzdimension aus dem Gegenkonto entfernen.

### <a name="scenario-4"></a>Szenario 4

Verwenden Sie dieselben Standardwerte für Finanzdimension, die Sie in den Szenarien 1 und 2 für den Erfassungsnamen und den Debitor definiert haben. Als Nächstes definieren Sie einen festen Dimensionswert für die Dimension **BUSINESSUNIT** im Hauptkonto 170150. Wechseln Sie zu **Hauptbuch \> Kontenplan \> Konten \> Hauptkonten**. Wählen Sie im Feld **Hauptkonten** den Wert **170150** und dann auf Registerkarte **Juristische Person überschreibt** die Option **Hinzufügen** aus. Wählen Sie **USMF** als juristische Person und dann **Hinzufügen** aus. Wählen Sie diesen Datensatz und dann **Standarddimensionen** aus. Ändern Sie die Dimension **BUSINESSUNIT** in **Fester Wert**, und geben Sie **003** als Wert ein.

Erstellen Sie eine neue allgemeine Erfassung mit dem Erfassungsnamen **GenJrn**. Entfernen Sie auf der Registerkarte **Finanzdimensionen** alle Standarddimensionswerte.

Wechseln Sie zu den **Positionen**. Wählen Sie im Feld **Kontotyp** die Option **Sachkonto** aus, und geben Sie dann im Feld **Konto** den Wert **170150** ein. Drücken Sie dann die **TAB-TASTE**, um das Feld zu verlassen. Die Dimensionswerte werden standardmäßig aus der Hauptkontokonfiguration des Kontos 170150 übernommen. Daher wird der Wert **Konto** als **170150-003-** angezeigt.

Ändern Sie den Wert für **Konto** in **170150-004-**. **Die Erfassungsfunktion verhindert nicht, dass ein fester Dimensionswert geändert wird.** Geben Sie entweder einen Soll- oder einen Habenbetrag ein. Wählen Sie im Feld **Gegenkontotyp** die Option **Sachkonto** aus, und geben Sie dann im Feld **Gegenkonto** den Wert **170250** ein. Der Finanzdimensionswert 004 wird als Standardwert aus dem Konto übernommen. Anschließend buchen Sie das Dokument. Wählen Sie in der Erfassung **Beleg** aus. Beachten Sie, dass der Wert **BUSINESSUNIT** während der Buchung auf den festen Dimensionswert **003** zurückgesetzt wurde.

Wenn Sie zu dem Beleg in der Erfassung zurückkehren, gibt die Dimension **BUSINESSUNIT** **nicht** den festen Dimensionswert wieder. Sie hat immer den Wert, der vor der Buchung angezeigt wurde. Der Buchungsprozess ändert keine Werte, die auf dem Beleg eingetragen wurden. Beim Buchen wird nur der Buchhaltungseintrag geändert.

## <a name="developer-notes"></a>Entwicklerhinweise

Wenn Sie sich als Entwickler den Code für den Standardprozess ansehen möchten, überprüfen Sie die folgenden Methoden:

- **LedgerJournalEngine.accountModified()** – Diese Methode ist der Haupteinstiegspunkt für den Standardprozess der primären Kontodimension, der für alle Erfassungen standardmäßig gilt (und von einigen Erfassungstypen überschrieben wird).
- **LedgerJournalEngine.offsetAccountModified()** – Diese Methode ist der Haupteinstiegspunkt für den Standardprozess der Gegenkontodimension.
