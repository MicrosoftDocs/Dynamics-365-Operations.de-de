---
title: Chargendispositionscodes verwenden, um Chargen als verfügbar oder nicht verfügbar zu markieren
description: Dieser Artikel beschreibt, wie Sie Chargendispositionscodes festlegen und verwenden, um Chargen für die Verwendung in der Produktprogrammplanung, der Reservierung, dem Kommissionieren und/oder dem Versand als verfügbar oder nicht verfügbar zu kennzeichnen.
author: t-benebo
ms.date: 09/16/2022
ms.topic: article
ms.search.form: PdsDispositionMaster, InventBatch
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-16
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cfb0743a573550de93d75063df517e0c143f2568
ms.sourcegitcommit: 20ce54cb40290dd116ab8b157c0a02d6757c13f5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/20/2022
ms.locfileid: "9542470"
---
# <a name="use-batch-disposition-codes-to-mark-batches-as-available-or-unavailable"></a>Chargendispositionscodes verwenden, um Chargen als verfügbar oder nicht verfügbar zu markieren

Dieser Artikel beschreibt, wie Sie *Chargendispositionscodes* festlegen und verwenden können. Jeder Chargendispositionscode hat einen Status von entweder *Verfügbar* oder *Nicht verfügbar*. Sie ordnen Chargendispositionscodes Bestandschargen zu, um anzugeben, ob die jeweilige Charge für die Produktprogrammplanung, Reservierung, Kommissionierung und/oder den Versand verfügbar ist.

Um Chargendispositionscodes zu verwenden, müssen Sie die Codes festlegen und sie den Chargen zuordnen, die Sie verwalten möchten.

## <a name="set-up-batch-disposition-codes"></a>Chargendispositionscodes festlegen

Sie müssen jeden Chargendispositionscode, den Sie in Ihrem System verwenden möchten, festlegen. Sie können so viele Codes erstellen, wie Sie möchten. (Sie können z.B. Codes erstellen, um die verschiedenen Gründe zu identifizieren, warum eine Charge verfügbar oder nicht verfügbar sein könnte). Häufig werden Sie jedoch nur zwei Codes haben: einen für *verfügbar* und einen für *nicht verfügbar*. Sie können auch angepasste Codes erstellen, mit denen eine Charge für bestimmte Vorgänge verwendet werden kann, für andere jedoch nicht.

Gehen Sie folgendermaßen vor, um Chargendispositionscodes festzulegen.

1. Gehen Sie zu **Bestandsverwaltung \> Einrichtung \> Charge \> Charge Dispositionsstamm**.
1. Auf der Seite **Chargendispositionsstamm** werden Ihre aktuellen Chargendispositionscodes aufgelistet, und Sie können sie erstellen, löschen und bearbeiten. Führen Sie einen dieser Schritte aus:

    - Um einen vorhandenen Code zu bearbeiten, wählen Sie ihn im Listenbereich aus.
    - Um einen neuen Code zu erstellen, wählen Sie **Neu** im Aktionsbereich.

1. Legen Sie die folgenden Felder in der Kopfzeile des neuen oder ausgewählten Codes fest:

    - **Chargendispositionscode** - Geben Sie den Anzeigenamen für den Code ein.
    - **Beschreibung** - Beschreiben Sie, wie der Code verwendet werden soll.
    - **Status der Chargendisposition** - Wählen Sie den Status, der für die Chargen gilt, denen der Code zugeordnet ist:

        - *Nicht verfügbar* - Die Chargen können nicht für die Produktprogrammplanung, Reservierung, Kommissionierung oder den Versand verwendet werden. Wenn Sie diesen Wert wählen, werden alle **Sperren**-Optionen auf dem Inforegister **Einrichtung** auf *Ja* festgelegt und alle **Dispositionscode einbezogen**-Optionen auf *Nein*. Sie können jedoch einige dieser Einstellungen ändern, um Ausnahmen hinzuzufügen.
        - *Verfügbar* - Die Chargen können für die Produktprogrammplanung, Reservierung, Kommissionierung und/oder den Versand verwendet werden. Wenn Sie diesen Wert wählen, werden alle **Sperren**-Optionen auf der Inforegisterkarte **Einrichtung** auf *Nein* festgelegt und alle **Dispositionscode einbezogen**-Optionen auf *Ja*. Diese Einstellungen sind schreibgeschützt, solange das Feld **Chargendisposition Status** auf *Verfügbar* festgelegt ist.

1. Wenn Sie das Feld **Chargendispositionsstatus** auf *Nicht verfügbar* festlegen, können Sie den Blockstatus jedes Vorgangs (Reservieren, Kommissionieren und Versenden) für jede Art von Auftrag (Verkauf, Umlagerung und Produktion) anpassen. Bei Produktionsaufträgen können Sie wählen, ob Sie die Erfassung der kommissionierten Produktion sperren oder freigeben möchten. Sie können auch wählen, ob Sie die Produktprogrammplanung sperren oder freigeben möchten. Verwenden Sie die Optionen auf dem Inforegister **Einrichtung**, um jeden Vorgang nach Bedarf zu sperren oder freizugeben. Legen Sie die Option **Dispositionscode einbezogen** auf *Ja* fest, um die Produktprogrammplanung zu aktivieren, oder legen Sie sie auf *Nein* fest, um die Produktprogrammplanung zu blockieren.

## <a name="assign-batch-disposition-codes-to-batches"></a>Chargendispositionscodes den Chargen zuweisen

Nachdem Sie die Chargendispositionscodes definiert haben, die Sie benötigen, führen Sie die folgenden Schritte aus, um sie den Chargen zuzuweisen.

1. Gehen Sie zu **Warehouse Management \> Einrichtung \> Bestand \> Chargen**.
1. Wählen Sie eine oder mehrere Chargen aus, denen Sie einen Chargendispositionscode zuweisen möchten.
1. Wählen Sie im Aktionsbereich auf der Registerkarte **Zurücksetzen** die Option **Chargendispositionscode zurücksetzen**.
1. Legen Sie im Dialogfenster **Einschränkungen für den Bestand ändern** im Feld **Neuer Chargendispositionscode** den Namen des Codes fest, den Sie zuweisen möchten.
1. Wählen Sie **OK**, um die neue Einstellung festzulegen und Ihre Änderung zu speichern.

    Auf der Seite **Chargen** werden die Werte in den Spalten **Chargendispositionscode** und **Chargendispositionsstatus** aktualisiert, so dass sie die neuen Einstellungen für die ausgewählten Chargen wiedergeben.

## <a name="master-planning-example"></a>Beispiel für die Produktprogrammplanung

Dieses Beispiel zeigt, wie Chargendispositionscodes die Produktprogrammplanung beeinflussen können.

In diesem Beispiel werden die Chargendispositionscodes wie folgt festgelegt:

- *P-verfügbar:*

    - **Status der Chargendisposition:** *Verfügbar*
    - **Dispositionscode einbezogen:** *Ja*

- *P-Nicht verfügbar:*

    - **Chargendispositionstatus:** *Nicht verfügbar*
    - **Dispositionscode einbezogen:** *Nein*

Es gibt ein Produkt (*Produkt-1*), das zwei Chargen hat: *Charge-A* und *Charge-B*. Diese Chargen sind wie folgt festgelegt:

- *Charge A:*

    - **Chargendispositionscode:** *P-verfügbar*
    - **Bestandsmenge:** 1

- *Charge-B:*

    - **Chargendispositionscode:** *P-Nicht verfügbar*
    - **Im Lagerbestand befindliche Menge:** 1

Es gibt einen Verkaufsauftrag (*SO1*) für eine Menge von 2 des Produkts *Produkt-1*. Das Lieferdatum ist in drei Tagen ab heute.

Sie führen die Produktprogrammplanung aus und legen die folgenden Werte fest, die für dieses Beispiel relevant sind:

- **Geplanter Auftrag:** *Auftrag zum Kauf*
- **Wiederbeschaffungsstrategie:** *Bedarf*
- **Vorlaufzeit:** *0*

Als Ergebnis des Planungslaufs verwendet das System die verfügbare Charge (*Charge-A*), um eine Menge von 1 des Produkts *Produkt-1* für den Verkaufsauftrag *SO1* zu decken. Die Charge *Charge-B* kann jedoch nicht verwendet werden, da diese Charge als nicht verfügbar für die Planung gekennzeichnet ist. Um die verbleibende Menge zu decken, erstellt das System daher einen geplanten Kauf (*PPO1*) für eine neue Charge von Produkt *Produkt-1*.

Die folgende Abbildung zeigt eine Zeitleiste für das Planungsergebnis.

![Beispiel, das zeigt, wie Chargendispositionscodes die Produktprogrammplanung beeinflussen können.](media/batch-codes-planning-example.png "Beispiel, das zeigt, wie Chargendispositionscodes die Produktprogrammplanung beeinflussen können")
