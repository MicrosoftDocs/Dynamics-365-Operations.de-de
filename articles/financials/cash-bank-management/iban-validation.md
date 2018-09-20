---
title: "Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer"
description: "Dieses Thema erklärt, wie Sie die internationale Bankkontonummer (IBAN) prüfen."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: de-de
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>Verwalten Sie die Kontoprüfung (IBAN) der internationalen Bankkontonummer

[!include [banner](../includes/banner.md)]

Internationale Bankkontonummer (IBAN) Kontoüberprüfung erhöht den Betrag der Prüfung, die  ausgeführt wird, wenn Sie eine IBAN einem Bankkonto hinzufügen.

Die Struktur der IBAN wird in Microsoft Dynamics 365 for Finance and Operations gespeichert und automatisch beim Verwenden der IBAN auf Bankkonten geladen. Die Kontonummer ist Teil der Struktur, die für eine IBAN-Nummer definiert wird. Basierend auf dieser Struktur wenn die Position und die Länge der Kontonummer der IBAN nicht mit der Position übereinstimmen, die in der Struktur für jedes Land oder jede Region definiert wird, werden Warnungsnachrichten angezeigt.

## <a name="set-up-iban-structures"></a>Einrichten der IBAN-Struktur

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> IBAN-Struktur**.
2. Beachten Sie, dass die IBAN-Strukturen für jedes Land oder jede Region automatisch installiert wurden.
3. Wenn Sie Strukturen für ein bestimmtes Land oder eine Region anpassen möchten, können Sie sie bearbeiten.
4. Die Strukturdefinitionen sind Teil einer neuen Version. Sie können das Menü **Rücksetzungsstrukturen** verwenden, um die neuesten Definitionen nach jeder Aktualisierung zu laden.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>Überprüfen Sie die IBAN-Struktur auf einem Bankkonto

1. Gehen Sie zu**Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Bankkonto erstellen.
3. Auf dem Inforegister **Zusätzliche Informationen** können Sie eine IBAN-Nummer eingeben.

    Basierend auf dieser Struktur wenn die Position und die Länge der Kontonummer der IBAN nicht mit der Position übereinstimmen, die in der Struktur für jedes Land oder jede Region definiert wird, werden Warnungsnachrichten angezeigt. Sie können nicht fortfahren, wenn die Länge der IBAN nicht der Länge in der IBAN-Struktur entspricht.

    Es wird auch geprüft, ob die Bankkontonummer mit dem Teil der IBAN übereinstimmt, die die Bankkontonummer darstellt. Wenn die Kontonummer nicht übereinstimmt, erhalten Sie eine Warnmeldung. Eine Warnmeldung wird angezeigt. Sie können fortfahren, selbst wenn die Kontonummer nicht übereinstimmt.

