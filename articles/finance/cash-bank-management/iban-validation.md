---
title: Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer
description: Dieses Thema erklärt, wie Sie die internationale Bankkontonummer (IBAN) prüfen.
author: twheeloc
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 89d6c38088e43f0f24fa41accecaa262a64006cf
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462763"
---
# <a name="manage-international-bank-account-number-iban-account-validation"></a>Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer

[!include [banner](../includes/banner.md)]

Internationale Bankkontonummer (IBAN) Kontoüberprüfung erhöht den Betrag der Prüfung, die  ausgeführt wird, wenn Sie eine IBAN einem Bankkonto hinzufügen.

Informationen über die Struktur der IBAN sind in Microsoft Dynamics 365 Finance gespeichert und werden automatisch geladen, wenn Sie die IBAN zum ersten Mal auf Bankkonten verwenden. Sie enthält die Länge der IBAN, die Anfangspositionen der Bankkontonummer und die Routingnummer und die Länge der Kontonummer und die Routingnummer.

## <a name="set-up-iban-structures"></a>Einrichten der IBAN-Struktur

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> IBAN-Struktur**.
2. Beachten Sie, dass die IBAN-Strukturen für jedes Land oder jede Region automatisch installiert wurden.
3. Wählen Sie die Schaltfläche **Bearbeiten**, wenn die Struktur für ein bestimmtes Land oder eine bestimmte Region aktualisiert werden muss.
4. Die Strukturdefinitionen sind Teil einer neuen Version. Sie können das Menü **Rücksetzungsstrukturen** verwenden, um die neuesten Definitionen nach jeder Aktualisierung zu laden.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Überprüfen Sie die IBAN-Struktur auf einem Bankkonto

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Bankkonto erstellen.
3. Auf dem Inforegister **Zusätzliche Informationen** können Sie eine IBAN-Nummer eingeben.

    Wenn die Länge der IBAN nicht mit der Länge übereinstimmt, die für jedes Land oder jede Region definiert ist, erhalten Sie eine Warnmeldung. Sie können nicht fortfahren, wenn die Länge der IBAN nicht der Länge in der definierten IBAN-Struktur entspricht.

    Es wird auch geprüft, ob die Bankkontonummer mit dem Teil der IBAN übereinstimmt, die die Bankkontonummer darstellt. Wenn die Kontonummer nicht übereinstimmt, erhalten Sie eine Warnmeldung. Eine Warnmeldung wird angezeigt. Sie können fortfahren, selbst wenn die Kontonummer nicht übereinstimmt.

    Es wird auch geprüft, ob die Bankkontonummer mit dem Teil der IBAN übereinstimmt, die die Bankroutingnummer darstellt. Die Routingnummer enthält eine Banknummer und häufig eine zusätzliche Bankfiliale. Wenn die Bankroutingnummer nicht übereinstimmt, erhalten Sie eine Warnmeldung. Eine Warnmeldung wird angezeigt. Sie können fortfahren, selbst wenn die Bankroutingnummer nicht übereinstimmt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
