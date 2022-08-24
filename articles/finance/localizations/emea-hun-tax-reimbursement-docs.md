---
title: Steuerrückerstattungsdokumente für Ungarn
description: In diesem Artikel wird erläutert, wie Steuerrückerstattungsdokumente für Ungarn eingerichtet und erstellt werden.
author: AdamTrukawka
ms.date: 03/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria
ms.author: atrukawk
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 55218172a3eb7e445b26795a4d4b936ecc2fce8a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283023"
---
# <a name="tax-reimbursement-documents-for-hungary"></a>Steuerrückerstattungsdokumente für Ungarn

[!include [banner](../includes/banner.md)]

## <a name="set-up-parameters-for-tax-reimbursement-documents"></a>Parameter für Steuerrückerstattungsdokumente einrichten

Ein Debitor ist ggf. eine Person, die in einem Land oder in einer Region wohnt, die kein Mitglied der Europäischen Union (EU) ist. Debitoren dieses Typs beantragen möglicherweise die Rückerstattung von Mehrwertsteuer (MwSt.), die sie bei Einkäufen bezahlt, die sie in Ungarn vorgenommen haben. Diese Debitoren bitten Sie möglicherweise auch darum, den Betrag der MwSt. zu dokumentieren, den sie Ihnen gezahlt haben. In diesem Fall können Sie ein Steuerrückerstattungsdokument aus der Debitorenrechnung erstellen.

### <a name="set-up-a-default-exchange-rate"></a>Standardwechselkurs einrichten

Verwenden Sie diese Prozedur, um einen Wechselkurs einzurichten, der automatisch in Steuerrückerstattungsdokumenten aktiviert ist.

1. Wählen Sie **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter** aus.
2. Auf der Seite **Debitorenparameter** auf der Registerkarte **Updates** im Inforegister **Sonstiges** im Feld **Steuerrückerstattungsbeleg** wählen Sie den Wechselkurstyp aus, der für Steuerrückerstattungsdokumente standardmäßig verwendet werden soll.

### <a name="set-up-a-number-sequence"></a>Einrichten eines Nummernkreises

Verwenden Sie diese Prozedur, um einen Nummernkreis einzurichten, der automatisch den Steuerrückerstattungsdokumenten zugewiesen wird.

1. Wählen Sie **Debitoren** &gt; **Einstellungen** &gt; **Debitorenparameter** aus.
2. Auf der Seite **Debitorenparameter** auf der Registerkarte **Nummernkreise**, im Feld **Referenz**, wählen Sie **Steuerrückerstattungsdokument** aus.
3. Wählen Sie im Feld **Nummernkreiscode** einen Nummernkreis für Steuerrückerstattungsdokumente aus.
4. Füllen Sie die verbleibenden optionalen Felder aus.

## <a name="create-and-print-a-tax-reimbursement-document"></a>Erstellen und Drucken eines Steuerrückerstattungsdokuments

Sie können ein Steuerrückerstattungsdokument für Debitoren bereitstellen, die Ihnen MwSt. gezahlt haben. Debitoren können das Steuerrückerstattungsdokument verwenden, um eine Mehrwertsteuererrückerstattung von der Steuerbehörde zu beanspruchen.

Das Steuerrückerstattungsdokument ist nur verfügbar, wenn der Debitor als Person auf der Seite **Debitoren** eingerichtet ist. Auf der Seite **Debitoren** auf dem Inforegister **Allgemein** bestätigen Sie, dass das Feld **Datensatztyp** auf **Person** festgelegt ist.

### <a name="set-up-print-management-for-a-tax-reimbursement-document"></a>Einrichten der Druckverwaltung für ein Steuerrückerstattungsdokument

1. Wählen Sie **Debitoren** &gt; **Einstellungen** &gt; **Formulare** &gt; **Formulareinstellungen** aus.
2. Auf der Seite **Formulareinstellungen** auf der Registerkarte **Allgemein** wählen Sie **Druckverwaltung** aus.
3. Auf der Seite **Druckverwaltungseinstellungen** unter **Modul – Debitoren** wählen Sie **Steuerrückerstattungsbeleg** aus.
4. Unter **Modul – Lagerverwaltung** &gt; **Kommissionierliste** wählen Sie entweder **Original** oder **Kopie** aus.
5. Geben Sie im rechten Fensterbereich Informationen darüber ein, was gedruckt werden soll.
6. Optional: Geben Sie im Feld **Fußzeilentext** den Text ein, der unten im Steuerrückerstattungsdokument gedruckt werden soll.

### <a name="select-invoice-lines-for-a-tax-reimbursement-document"></a>Rechnungspositionen für ein Steuerrückerstattungsdokument auswählen

1. Wählen Sie **Debitoren** &gt; **Abfragen und Berichte** &gt; **Erfassungen** &gt; **Rechnungserfassung** aus.
2. Auf der Seite **Rechnungserfassung** auf der Registerkarte **Übersicht** wählen Sie die Debitorenrechnung aus, für die der Debitor eine Steuerrückerstattung anfordert.
3. Aktivieren Sie das Kontrollkästchen **Steuerrückerstattung** für die ausgewählte Rechnung.
4. Standardmäßig sind auf der Registerkarte **Positionen**, im Feld **Steuerrückerstattungspositionen** alle Rechnungspositionen ausgewählt. Deaktivieren Sie das Kontrollkästchen für jede Rechnungsposition, die vom Steuerrückerstattungsdokument ausgeschlossen werden soll.
5. Auf der Registerkarte **Übersicht** wählen Sie **Steuerrückerstattung** &gt; **Vorschau des Originals** aus, um das Dokument anzuzeigen, bevor Sie es drucken.
6. Optional: Wählen Sie **Steuerrückerstattung** &gt; **Druckverwaltung verwenden** aus, um die Druckeinstellungen zu ändern, beispielsweise die Anzahl der zu druckenden Kopien.
7. Überprüfen Sie auf der Seite **Original anzeigen** die Informationen, und drucken Sie dann das Steuerrückerstattungsdokument.

Wenn Sie ein Steuerrückerstattungsdokument drucken, wird die Dokumentnummer, die dem Dokument zugewiesen ist, im Feld **Steuerrückerstattungsdokument** auf der Seite **Rechnungserfassung** angezeigt. Das Kontrollkästchen **Steuerrückerstattung** ist für die Positionen, die Sie in das Steuerrückerstattungsdokument einbezogen haben, nicht verfügbar.

### <a name="settle-a-tax-reimbursement"></a>Eine Steuerrückerstattung ausgleichen

Wenn Ihre Organisation einem Debitor für Mehrwertsteuer Erstattung bietet, müssen Sie die Rückerstattung in der Rechnungserfassung angeben. Andernfalls könnte der Debitor dieselbe Rückerstattung doppelt erhalten. Gehen Sie folgendermaßen vor, um Rechnungspositionen auszugleichen, für die ein Debitor eine MwSt.-Rückerstattung empfangen hat.

1. Wählen Sie **Debitoren** &gt; **Abfragen und Berichte** &gt; **Erfassungen** &gt; **Rechnungserfassung** aus.
2. Auf der Seite **Rechnungserfassung** auf der Registerkarte **Übersicht** wählen Sie die Debitorenrechnung aus, für die der Debitor eine Mehrwertsteuerrückerstattung empfangen hat.
3. Wählen Sie **Steuerrückerstattung** &gt; **MwSt. ausgeglichen.** aus.

Das Kontrollkästchen **MwSt. ausgeglichen.** ist für die Rechnung und die Rechnungspositionen aktiviert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
