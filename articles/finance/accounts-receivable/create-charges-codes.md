---
title: Belastungscodes erstellen
description: In diesem Artikel wird erläutert, wie Belastungscodes sowohl für die Kreditorenbuchhaltung als auch für die Debitorenbuchhaltung konfiguriert werden.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MarkupTable
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d65952cb989672e4eac2dd6101ee9c7c9424daed
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866082"
---
# <a name="create-charges-codes"></a>Belastungscodes erstellen

In diesem Artikel wird erläutert, wie Belastungscodes sowohl für die Kreditorenbuchhaltung als auch für die Debitorenbuchhaltung konfiguriert werden. Wenn Ihre Organisation verlangt, dass Verkaufsbeträge oder Einkaufsbeträge zusätzlich zu Einzelposten in einem Verkaufsauftrag oder einer Bestellung nachverfolgt werden, können Sie für diesen Zweck Belastungscodes verwenden. So können Sie Fracht und Versicherung in einer Bestellung bezahlen, und diese Beträge werden separat in der Bestellung aufgeschlüsselt. In diesem Fall können Sie angeben, ob die Beträge in Ausgabenkonten gebucht oder ob den Kosten der Artikel hinzugefügt werden sollen.

## <a name="set-up-charges-codes-for-accounts-receivable"></a>Einstellen von Belastungscodes für Debitoren

Führen Sie die folgenden Schritte aus, um Belastungscodes für Debitoren zu erstellen.

1. Wechseln Sie zu **Debitoren** &gt; **Belastungseinstellungen** &gt; **Belastungscode**.
2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Belastungscode** einen Code für die Belastung ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung der Belastung ein.
4. Optional: Im Feld **Artikel Umsatzsteuergruppe** wählen Sie eine Artikelumsatzsteuergruppe aus.
5. Geben Sie auf dem Inforegister **Buchung** an, auf welche Weise für die Belastung eine automatische Soll- oder Habenbuchung erfolgen sollte.
6. Wurde **Sachkonto** als Soll-/Habentyp ausgewählt, muss in den Feldern **Buchung** ein Soll-/Haben-Buchungstyp und in den Feldern **Konto** das Soll-/Habenkonto angegeben werden.

### <a name="example"></a>Beispiel

Ihr Kunde zahlt die Belastung. Daher wird sie zur Auftragssumme addiert. Folgende Buchungsinformationen müssen eingerichtet werden:

- Wählen Sie im Feld **Typ** im Abschnitt **Soll** **Debitor/Kreditor** aus, um die Rechnungsbelastung dem Konto des Debitors hinzuzufügen.
- Im **Typ**-Feld im **Haben**-Abschnitt, wählen Sie **Sachkonto** aus. Wählen Sie anschließend im Feld **Konto** das Hauptkonto für Umsatzerlöse für die Rechnungsbelastungen.

> [!NOTE]
> Wenn der Solltyp oder der Habentyp für den ausgewählten Code entweder **Sachkonto** oder **Position** ist, können Sie eine andere Währung für die Belastungstransaktion angeben.

Der Text für Belastungen kann in der Sprache gedruckt werden, die dem Debitor zugewiesen ist. Um den Text für den Belastungscode in anderen Sprachen anzugeben, wählen Sie **Transaktionen**.

## <a name="set-up-charges-codes-for-accounts-payable"></a>Einstellen von Belastungscodes für Kreditorenkonten

Führen Sie die folgenden Schritte aus, um Belastungscodes für Debitorenkonten zu erstellen.

1. Führen Sie einen dieser Schritte aus:

    - Wechseln Sie zu **Debitoren** &gt; **Belastungseinstellungen** &gt; **Belastungscode**.
    - Rufen Sie **Beschaffung** &gt; **Einstellen** &gt; **Belastungen** &gt; **Belastungscode** auf.

2. Wählen Sie **Neu** aus.
3. Geben Sie im Feld **Belastungscode** einen Code für die Belastung ein.
3. Geben Sie im Feld **Beschreibung** eine Beschreibung der Belastung ein.
4. Optional: Im Feld **Artikel Umsatzsteuergruppe** wählen Sie eine Artikelumsatzsteuergruppe aus.
5. Optional: Im **Maximaler Betrag**-Feld geben Sie den maximalen Abschreibungsbetrag ein, der für den Belastungscodes zulässig ist.

    Dieses Feld wird verwendet, um Belastungen für Kreditorenrechnungen zu überprüfen. Um die Belastungsvalidierung zu aktivieren, aktivieren Sie das **Die Überprüfung des Rechnungsabgleichs aktivieren**-Kontrollkästchen auf der **Rechnungsvalidierung**-Registerkarte der **Parameter der Kreditorenbuchhaltung**-Seite.

    > [!IMPORTANT]
    > Um Belastungen für Rechnungen zu prüfen, müssen Sie auch eine Instanz eines Richtlinienregeltyps erstellen, der auf den Belastungen für die jeweilige Kreditorenrechnungsrichtlinie basiert.

6. Geben Sie auf dem Inforegister **Buchung** an, auf welche Weise für die Belastung eine automatische Soll- oder Habenbuchung erfolgen sollte.
7. Wurde **Sachkonto** als Soll-/Habentyp ausgewählt, muss in den Feldern **Sollbuchung** und **Habenbuchung** ein Soll-/Haben-Buchungstyp und in den Feldern **Sollkonto** und **Habenkonto** das Soll-/Habenkonto angegeben werden.
8. Aktivieren Sie das Kontrollkästchen **Bestellung und Rechnungswerte vergleichen**, um einen Vergleich der Belastungswerte für eine Rechnung zu ermöglichen, deren Belastungen im entsprechenden Bestellungskopf oder in den entsprechenden Bestellpositionen enthalten sind.

### <a name="example"></a>Beispiel

Sie können die Belastung als Ausgabe als Teil der Summe für die Bestellung oder Kreditorenrechnung erfassen. Führen Sie diese Schritte aus, um Buchungsinformationen einzurichten. 

- Wählen Sie im Feld **Typ** im Abschnitt **Haben** **Debitor/Kreditor** aus, um die Rechnungsbelastung dem Konto des Kreditors hinzuzufügen.
- Im **Typ**-Feld im **Soll**-Abschnitt, wählen Sie **Sachkonto** aus. Wählen Sie anschließend im Feld **Konto** das Hauptkonto für Ausgaben für die Rechnungsbelastungen.

Befolgen Sie diese Schritte, um Buchungsinformationen einzurichten, sodass die Einheitsbelastung zu den Artikelkosten hinzugefügt wird.

- Wählen Sie im Feld **Typ** im Abschnitt **Haben** **Debitor/Kreditor** aus, um die Rechnungsbelastung dem Konto des Kreditors hinzuzufügen.
- Wählen Sie im Feld **Typ** im Abschnitt **Soll** **Position** aus , um die Belastung zum Artikelpreis zu addieren.

> [!NOTE]
> Sie können eine Währung verwenden, die sich von der Währung unterschiedet, die in der Bestellung oder Rechnung angegeben ist. Sie können eine andere Währung eingeben, wenn der Soll- oder Haben-Typ für den ausgewählten Code entweder **Sachkonto** oder **Position** lautet.

Der Text für Belastungen kann in der Sprache gedruckt werden, die dem Debitor zugewiesen ist. Um den Text für den Belastungscode in anderen Sprachen anzugeben, wählen Sie **Transaktionen**.
