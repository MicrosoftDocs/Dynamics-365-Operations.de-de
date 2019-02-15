---
title: Debitoren unter Verwendung gemeinsamer Nummernkreise kopieren
description: In diesem Thema wird erläutert, wie Sie gemeinsame Nummernkreise verwenden, um einen Debitor unter Beibehaltung der gleichen Debitorkennung zu einer anderen juristischen Person zu kopieren.
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7a1e6c6e3a995ad745522d58960e850d72c2ee57
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "302303"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Debitoren unter Verwendung gemeinsamer Nummernkreise kopieren

[!include [banner](../includes/banner.md)]

Sie können gemeinsame Nummernkreise verwenden, um Debitorkennungen zuzuweisen. Über gemeinsame Nummernkreise können Sie auch Debitoren von einer juristischen Person zu einer anderen juristischen Person kopieren, während jedoch die gleiche Debitorkennung in beiden juristischen Personen verwendet wird.

## <a name="setup"></a>Setup

Die Funktion wird aktiviert, wenn Sie einen gemeinsamen Nummernkreis verwenden, um Debitorkennungen zuzuweisen. Sie müssen den gleichen Nummernkreis bei jeder juristischen Person verwenden, in die Sie einen Debitor kopieren möchten. Sie ändern den Debitorennummernkreis auf der Seite **Debitorenparameter** für jede juristische Person. Wählen Sie **Debitoren** \> **Parameter** und dann die Registerkarte **Nummernkreise** aus.

Sie können Debitorennummernkreise für jede Debitorengruppe einrichten. Diese Nummernkreise müssen ebenfalls freigegeben sein. Der Nummernkreis für eine Debitorengruppe wird zuerst verwendet. Wenn für eine Debitorengruppe kein Nummernkreis angegeben ist, wird der Nummernkreis verwendet, der auf der Seite **Debitorenparameter** angegeben ist.

Sie können Debitoren auch zwischen juristischen Personen kopieren, wenn Sie manuelle Debitorkennungen verwenden. Wenn Sie jedoch versuchen, einen Debitoren zu einer juristischen Person zu kopieren, in der die Debitorkennung bereits vorhanden ist, wird der Kopiervorgang nicht gestartet.

## <a name="copy-a-customer"></a>Debitor kopieren

Um einen Debitoren zu kopieren, wählen Sie **Neu** auf der Listenseite **Alle Debitoren**, um das Dialogfeld **Debitor erstellen** zu öffnen. Sie sehen, dass die neue Debitorkennung nicht sofort zugewiesen wird. Dieses Verhalten unterscheidet sich vom Verhalten der Vorgängerversionen von Microsoft Dynamics 365 for Finance and Operations. Da Sie die Debitorengruppe noch nicht ausgewählt haben, kann das System nicht den richtigen Nummernkreis ermitteln, der verwendet werden soll. Darüber hinaus kann es nicht feststellen, ob Sie versuchen, einen neuen Debitor zu erstellen oder einen Debitor zu kopieren. Daher wird die Debitorkennung erst zugewiesen, wenn Sie unten im Dialogfeld **Speichern** auswählen.

Wenn Sie einen neuen Debitor erstellen, können Sie alle Felder weiter füllen, wie Sie es gewohnt sind. Wenn Sie fertig sind und **Speichern** auswählen, werden Sie feststellen, dass die Debitorkennung automatisch zugewiesen wurde. Bei manuellen Nummernkreisen sehen Sie, dass Ihre manuelle Debitorkennung verwendet wurde.

Um einen Debitor zu kopieren, geben Sie im Feld **Name** mindestens ein Zeichen für den Debitor ein, den Sie suchen. In einem Suchdialogfeld wird eine Liste der Parteien angezeigt, die möglicherweise den Debitor darstellen, den Sie suchen. Wenn Sie eine der Parteien auswählen, werden auf der rechten Seite des Dialogfelds zusätzliche Informationen angezeigt:

- Die Registerkarte **Allgemein** enthält die Telefonnummer und Adresse der Partei.
- Die Registerkarte **Rollen** enthält die Rollen, die die ausgewählte Partei haben kann, sowie die juristische Person, in der sie die jeweilige Rolle innehat.
- Die Registerkarte **Steuerregistrierungskennung** zeigt die Steuerregistrierungskennungen an, der die Partei zugewiesen sind.

Sie können eine Partei nur kopieren, wenn sie eine Debitorenrolle hat und wenn sie diese Rolle in einer juristischen Person innehat, die nicht die aktuelle juristische Person ist. Wenn Sie eine Partei finden, die diese Kriterien erfüllt, führen Sie die folgenden Schritte aus.

1. Die Option **Debitor kopieren** wird angezeigt. Standardmäßig ist diese Option auf **Nein** festgelegt. Um den Debitor zur aktuellen juristischen Person zu kopieren, legen Sie die Option auf **Ja** fest. 
2. Das Feld **Juristische Person** wird angezeigt. Wählen Sie die juristische Person aus, von der der Debitor kopiert werden soll. Wenn der Debitor in nur einer juristischen Person vorhanden ist, wird das Feld standardmäßig auf diese juristische Person festgelegt.
3. Wählen Sie **Auswählen**. Der neue Debitor wird erstellt.

## <a name="validation"></a>Überprüfung

Wenn Sie einen Debitor kopieren, versucht das System, die neuen Debitordaten zu speichern. Es werden Überprüfungen durchgeführt, um sicherzustellen, dass die kopierten Daten korrekt sind. Sie erhalten für jede Prüfung, die fehlschlägt, eine Fehlermeldung. In den Fehlermeldungen wird erklärt, welche Informationen aktualisiert werden müssen. Die Kopie des Debitors kann erst gespeichert werden, wenn alle Fehler korrigiert wurden.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Debitor unter Verwendung der Umsatzsteuernummer-Suchfunktion kopieren

Sie können Debitoren auch kopieren, indem Sie die Umsatzsteuernummer-Suchfunktion verwenden, die sich in der Gruppe **Registrierung** auf der Registerkarte **Debitor** im Aktivitätsbereich der Seite **Alle Debitoren** befindet. Das Dialogfeld mit der **Umsatzsteuernummernsuche** zeigt die Umsatzsteuernummern, die Debitorkennung, den Debitorennamen und die juristische Person an, in der die Umsatzsteuernummer verwendet wird. Sie können einen Debitoren nur kopieren, wenn er sich in einer juristischen Person befindet, die nicht die aktuelle juristische Person ist. Nachdem Sie einen Debitor ausgewählt haben, der dieses Kriterium erfüllt, führen Sie die folgenden Schritte aus.

1. Die Option **Debitor kopieren** wird angezeigt. Standardmäßig ist diese Option auf **Nein** festgelegt. Um den Debitor zur aktuellen juristischen Person zu kopieren, legen Sie die Option auf **Ja** fest. 
2. Wählen Sie **Auswählen**. Der neue Debitor wird erstellt.
