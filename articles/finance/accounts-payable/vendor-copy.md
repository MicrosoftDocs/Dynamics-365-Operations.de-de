---
title: Kreditoren unter Verwendung gemeinsamer Nummernkreise kopieren
description: In diesem Artikel wird erläutert, wie Sie gemeinsame Nummernkreise verwenden, um einen Kreditor unter Beibehaltung der gleichen Kreditorenkennung zu einer anderen juristischen Person zu kopieren.
author: sunfzam
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7b7285cdf454955656c4fb20c3abf68f3f9c39dc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904900"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Kreditoren unter Verwendung gemeinsamer Nummernkreise kopieren

[!include [banner](../includes/banner.md)]

Sie können gemeinsame Nummernkreise verwenden, um Kreditorenkennungen zuzuweisen. Über gemeinsame Nummernkreise können Sie auch Kreditoren von einer juristischen Person zu einer anderen juristischen Person kopieren, während jedoch die gleiche Kreditorenkennung in beiden juristischen Personen verwendet wird.

## <a name="setup"></a>Setup

Die Funktion wird aktiviert, wenn Sie einen gemeinsamen Nummernkreis verwenden, um Kreditorenkennungen zuzuweisen. Sie müssen den gleichen Nummernkreis bei jeder juristischen Person verwenden, in die Sie einen Kreditoren kopieren möchten. Sie ändern den Kreditorennummernkreis auf der Seite **Kreditorenparameter** für jede juristische Person. Wählen Sie **Kreditorenkonten** \> **Setup** \> **Kreditorenkontenparameter** und dann die Registerkarte **Nummernkreise** aus.

Sie können Kreditorennummernkreise auch für jede Kreditorengruppe einrichten. Diese Nummernkreise müssen ebenfalls freigegeben sein. Der Nummernkreis für eine Kreditorengruppe wird zuerst verwendet. Wenn für eine Kreditorengruppe kein Nummernkreis angegeben ist, wird der Nummernkreis verwendet, der auf der Seite **Kreditorenparameter** angegeben ist.

Sie können Kreditoren auch zwischen juristischen Personen kopieren, wenn Sie manuelle Kreditorenkennungen verwenden. Wenn Sie jedoch versuchen, einen Kreditor in eine juristische Person zu kopieren, in der die Kreditorenkennung bereits vorhanden ist, wird der Kopiervorgang nicht gestartet.

## <a name="copy-a-vendor"></a>Kopieren von Kreditoren

Um einen Kreditor zu kopieren, wählen Sie auf der Listenseite **Alle Kreditoren** die Option **Neu** aus. Die Seite **Alle Kreditoren, neuer Datensatz** wird angezeigt. Die neue Kreditorenkennung wird nicht sofort zugewiesen. Dieses Verhalten unterscheidet sich vom Verhalten der Vorgängerversionen. Da Sie die Kreditorengruppe noch nicht ausgewählt haben, kann der zu verwendende Nummernkreis nicht ermittelt werden. Darüber hinaus kann es nicht feststellen, ob Sie versuchen, einen neuen Kreditor zu erstellen oder einen Kreditor zu kopieren. Daher wird die Kreditorkennung erst zugewiesen, wenn Sie unten auf der Seite **Speichern** auswählen.

Wenn Sie einen neuen Kreditor erstellen, können Sie alle Felder weiter füllen, wie Sie es gewohnt sind. Wenn Sie fertig sind und **Speichern** auswählen, wird die Kreditorenkennung automatisch zugewiesen. Bei manuellen Nummernkreisen sehen Sie, dass Ihre manuelle Kreditorenkennung verwendet wurde.

Um einen Kreditor zu kopieren, geben Sie im Feld **Name** mindestens ein Zeichen für den Kreditor ein, den Sie suchen. In einem Suchdialogfeld wird eine Liste der Parteien angezeigt, die möglicherweise den Kreditor darstellen, den Sie suchen. Wenn Sie eine der Parteien auswählen, werden auf der rechten Seite des Dialogfelds zusätzliche Informationen angezeigt:

- Die Registerkarte **Allgemein** enthält die Telefonnummer und Adresse der Partei.
- Die Registerkarte **Rollen** enthält die Rollen, die die ausgewählte Partei haben kann, sowie die juristische Person, in der sie die jeweilige Rolle innehat.
- Die Registerkarte **Steuerregistrierungskennung** zeigt die Steuerregistrierungskennungen an, der die Partei zugewiesen sind.

Sie können eine Partei nur kopieren, wenn sie eine Kreditorenrolle hat und wenn sie diese Rolle in einer juristischen Person innehat, die nicht die aktuelle juristische Person ist. Wenn Sie eine Partei finden, die diese Kriterien erfüllt, führen Sie die folgenden Schritte aus.

1. Die Option **Kreditor kopieren** wird angezeigt. Standardmäßig ist diese Option auf **Nein** festgelegt. Um den Kreditor zur aktuellen juristischen Person zu kopieren, legen Sie die Option auf **Ja** fest. 
2. Das Feld **Juristische Person** wird angezeigt. Wählen Sie die juristische Person aus, von der der Kreditor kopiert werden soll. Wenn der Kreditor in nur einer juristischen Person vorhanden ist, wird das Feld standardmäßig auf diese juristische Person festgelegt.
3. Wählen Sie **Auswählen**. Der neue Kreditor wird erstellt.

## <a name="validation"></a>Prüfung

Wenn Sie einen Kreditor kopieren, wird versucht, die neuen Kreditordaten zu speichern. Es werden Überprüfungen durchgeführt, um sicherzustellen, dass die kopierten Daten korrekt sind. Sie erhalten für jede Prüfung, die fehlschlägt, eine Fehlermeldung. In den Fehlermeldungen wird erklärt, welche Informationen aktualisiert werden müssen. Die Kopie des Kreditors kann erst gespeichert werden, wenn alle Fehler korrigiert wurden.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Kreditor unter Verwendung der Umsatzsteuernummer-Suchfunktion kopieren

Sie können Kreditoren auch kopieren, indem Sie die Suchfunktion der **Umsatzsteuernummer** verwenden, die sich in der Gruppe **Registrierung** auf der Registerkarte **Kreditor** im Aktivitätsbereich der Seite **Alle Kreditoren** befindet. Das Dialogfeld mit der **Umsatzsteuernummernsuche** zeigt die Umsatzsteuernummern, die Kreditorenkennung, den Kreditorennamen und die juristische Person an, in der die Umsatzsteuernummer verwendet wird. Sie können einen Kreditoren nur kopieren, wenn er sich in einer juristischen Person befindet, die nicht die aktuelle juristische Person ist. Nachdem Sie einen Kreditor ausgewählt haben, der dieses Kriterium erfüllt, führen Sie die folgenden Schritte aus.

1. Die Option **Kreditor kopieren** wird angezeigt. Standardmäßig ist diese Option auf **Nein** festgelegt. Um den Kreditor zur aktuellen juristischen Person zu kopieren, legen Sie die Option auf **Ja** fest.
2. Wählen Sie **Auswählen**. Der neue Kreditor wird erstellt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
