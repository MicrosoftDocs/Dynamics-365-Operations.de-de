---
title: Strichcodes mit einer Kamera in die Warehouse Management Mobile App scannen
description: In diesem Thema wird erläutert, wie Sie die Warehouse Management Mobile App einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen.
author: Mirzaab
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: cc58d88865fea17e0e27463b25e2ba815ee1a5b1
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901971"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Strichcodes mit einer Kamera in die Warehouse Management Mobile App scannen

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Warehouse Management Mobile App einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen.

## <a name="setup"></a>Einstellung

In der Anzeige der Warehouse Management Mobile App können Sie auswählen, ob die Kamera für Scannen von Strichcodes verwendet wird. Wenn Sie **Verwenden Sie die Kamera als Scanner** aktivieren, können Sie die Kamera auf jedem Eingabefeld verwenden, bei dem der bevorzugte Eingabemodus auf **Scannen** festgelegt ist.

Um zu steuern, ob ein Eingabefeld gescannt werden soll, legen Sie auf der Seite **Feldnamen in Lagerortanwendung** **Bevorzugter Eingabemodus** auf **Scannen** fest. Wenn diese Option aktiviert ist, kann eine Kamera für das Scannen in der Warehouse Management Mobile App verwendet werden. Weitere Informationen finden Sie unter [Felder für die Warehouse Management Mobile App konfigurieren](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Unterstützte Strichcodeformate

Die Formate der allgemeinsten Strichcodes einschließlich Code 128 Code 39, Codes 93, EAN-8, EAN-13, UPC-A und QR unterstützt.

## <a name="navigation"></a>Navigieren

Die Kameraseite wird auf jeder Seite verwendet, die im Eingabefeld einen **Bevorzugten Eingabemodus** hat, auf dem der Vorgang auf *Scannen* festgelegt ist, wenn Sie auf der Kameraseiten zu den folgenden Optionen navigieren:

- Wählen Sie auf die Schaltfläche „Zurück“, um wieder zur Seite **Aufgaben und Details** zu wechseln.
- Wählen Sie den Stift auf der Seite **Aufgabe und Details** aus, um zur Seite zu wechseln, in der Sie die Eingabe manuell eingeben können.
- Wählen Sie auf der Seite **Aufgabe und Details** die Kamera aus, um zur Kameraseite zu wechseln.

Auf der Kameraseite, wenn Sie die Kameraschaltfläche auswählen, wird sie abgeblendet angezeigt, wenn Sie versuchen, einen Strichcode zu identifizieren. Wenn ein Strichcode nicht innerhalb von 5 Sekunden gekennzeichnet wird, wird der Prozess unterbrochen und die Kameraschaltfläche wird wieder verfügbar. Sie können dann versuchen, den Strichcode erneut zu scannen.

Wenn Sie die Kamera auf einen Strichcode richten, halten Sie den Strichcode auf die Klammern ausgerichtet, um das beste Ergebnis zu erzielen. Wenn ein Strichcode erfolgreich gescannt wird, wird das Ergebnis verarbeitet, und Sie werden auf die nächste Stufe übernommen. Wenn im nächsten Schritt ein anderes Eingabefeld den bevorzugten Eingabemodus enthält, der im Vorgang festgelegt wird, wird die Kameraseite erneut angezeigt. Wenn der nächste Schritt kein Scan-Feld ist, wird die Kameraseite nicht gestartet.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]