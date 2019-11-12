---
title: Strichcodes mithilfe einer Kamera in Dynamics 365 for Finance and Operations – Warehousing-App
description: In diesem Thema wird erläutert, wie Sie die Dynamics 365 for Finance and Operations – Warehousing-App einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 58cf27a250778d68bdffa1eefa5e939276e467fc
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578148"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a>Strichcodes mithilfe einer Kamera in Dynamics 365 Supply Chain Management – Warehousing-App

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie die Dynamics 365 for Finance and Operations – Warehousing-App einrichten, um Strichcodes mithilfe einer Kamera auf einem mobilen Gerät zu scannen. 

## <a name="prerequisites"></a>Voraussetzungen
Damit Sie diese Funktion verwenden können, müssen Sie 1.2.0.0 Version der Warehousing-App eingerichtet haben, und Ihr Gerät muss eine Kamera haben. Wenn Sie die App nach der Aktualisierung öffnen, werden Sie aufgefordert, der App zu erlauben, die Kamera zu verwenden. Wenn Ihr Gerät keine Kamera hat, wird keine entsprechende Meldung angezeigt, und Sie können die Kamera nicht als Scanner verwenden. 

## <a name="setup"></a>Einrichten
In der Anzeige der Warehousing-Anwendung können Sie auswählen, ob die Kamera für Scannen von Strichcodes verwendet wird. Wenn Sie **Verwenden Sie die Kamera als Scanner** aktivieren, können Sie die Kamera auf jedem Eingabefeld verwenden, bei dem der bevorzugte Eingabemodus auf **Scannen** festgelegt ist. 

Um zu steuern, ob ein Eingabefeld gescannt werden soll, legen Sie auf der Seite **Feldnamen in Lagerortanwendung** **Bevorzugter Eingabemodus** auf **Scannen** fest. Wenn diese Option aktiviert ist, kann eine Kamera für das Scannen in der Warehousing-App verwendet werden. Informationen darüber, wie Sie App-Feldnamen im Warehousing konfigurieren, finden Sie unter [Konfigurieren Sie App-Feldnamen in der Warehousing-App](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Unterstützte Strichcodeformate
Die Formate der allgemeinsten Strichcodes einschließlich Code 128 Code 39, Codes 93, EAN-8, EAN-13, UPC-A und QR unterstützt. 

## <a name="navigation"></a>Navigieren
Die Kameraseite wird auf jeder Seite verwendet, die im Eingabefeld einen bevorzugten Eingabemodus hat, auf der dem Vorgang festgelegt ist, wenn Sie auf der Kameraseitenverwendung zu den folgenden Optionen navigieren:
- Klicken Sie auf die Schaltfläche "Zurück", um wieder zu den Aufgaben und die Detailseite zu wechseln. 
- Klicken Sie auf den Stift für die Aufgabe und die Detailseite, um zur Seite zu wechseln, in der Sie die Eingabe manuell eingeben können.
- Klicken Sie auf die Kamera der Aufgabe und auf die Detailseite, um zur Kameraseite zu wechseln. 

| Aufgabe und Detailseite | Kameraseite | 
| :---------------------: | :--------------------: |
| ![Aufgabe und Detailseite für Beispiel zum Scannen mit der Kamera](./media/camera-scanning-example-task-detail-page50.png)          | ![Aufgabe und Detailseite für Beispiel zum Scannen mit der Kamera – kleiner](./media/camera-scanning-example-camera-page50.png)          |

Auf der Kameraseite, wenn Sie auf die Kameraschaltfläche klicken, wird sie abgeblendet angezeigt, wenn Sie versuchen, einen Strichcode zu identifizieren. Wenn ein Strichcode nicht innerhalb von 5 Sekunden gekennzeichnet wird, wird der Prozess unterbrochen und die Kameraschaltfläche wird wieder verfügbar. Sie können dann versuchen, den Strichcode erneut zu scannen.

Wenn Sie die Kamera auf einen Strichcode richten, halten Sie den Strichcode auf die Klammern ausgerichtet, um das beste Ergebnis zu erzielen. Wenn ein Strichcode erfolgreich gescannt wird, wird das Ergebnis verarbeitet, und Sie werden auf die nächste Stufe übernommen. Wenn im nächsten Schritt ein anderes Eingabefeld den bevorzugten Eingabemodus enthält, der im Vorgang festgelegt wird, wird die Kameraseite erneut angezeigt. Wenn der nächste Schritt kein Scan-Feld ist, wird die Kameraseite nicht gestartet.

