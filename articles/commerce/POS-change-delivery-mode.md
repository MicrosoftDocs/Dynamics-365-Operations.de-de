---
title: Lieferart in POS ändern
description: In diesem Thema wird beschrieben, wie Sie den Änderungsmodus des Zustellvorgangs am POS konfigurieren und verwenden.
author: hhainesms
manager: annbe
ms.date: 03/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2020-02-20
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: d2691ef6b08a44a845857c34fe60072211364f82
ms.sourcegitcommit: 02640a0f63daa9e509146641824ed623c4d69c7f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "3265479"
---
# <a name="change-mode-of-delivery-in-pos"></a>Lieferart in POS ändern

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie die Funktion Liefermodus ändern in Ihrer POS-Umgebung (Point of Sale) einrichten und verwenden. 

In Dynamics 365 Commerce Versionen 10.0.10 und höher, ist der Vorgang (647) **Lieferart ändern** verfügbar, um ihn den POS Bildschirmlayouts hinzufügen.

Mit der Funktion zum Ändern des Zustellungsmodus können Sie den Zustellungsmodus für eine oder mehrere versandkonfigurierte Verkaufslinien in der POS-Transaktion ändern. In früheren Versionen von Commerce mussten Sie die vollständige Version durchlaufen **Versenden Sie alle** oder **Ausgewählte versenden**. Die Konfiguration erfolgt, wenn Sie den Zustellungsmodus für eine vorhandene Linie ändern möchten, die für den Versand konfiguriert wurde. Dieser Vorgang war zeitaufwändig und konnte zu versehentlichen Änderungen des Lieferursprungs oder der Liefertermine für die Linie führen. Die neue Funktionalität bietet eine alternative Methode zur effizienten Aktualisierung der Zustellungsart in diesen Vertriebslinien.

Weitere Informationen zum Hinzufügen einer Operation zu einer Schaltfläche in Ihrem POS-Schaltflächenraster finden Sie unter [Bildschirmlayouts für die Verkaufsstelle](https://docs.microsoft.com/dynamics365/commerce/pos-screen-layouts).

Nachdem diese Funktion in POS konfiguriert wurde, wenn Sie **Lieferart ändern** auswählen, wird eine Listenseite angezeigt, auf der Sie die Zeilen der Transaktion auswählen können, für die Sie den Zustellungsmodus ändern möchten. Sie können einige oder alle Zeilen auswählen oder beenden, ohne Änderungen vorzunehmen. Die Verkaufszeilen, die zuvor für den Versand konfiguriert wurden, sind die einzigen Zeilen in der Liste, die Sie ändern können. Wenn Sie eine Linie ändern möchten, die für die Abholung oder den Transport bestimmt ist, müssen Sie die Vorgänge **Versenden Sie alle** oder **Ausgewählte versenden** auswählen. Wenn Sie dagegen eine als Sendung bezeichnete Position in eine Abholung oder einen Transport ändern möchten, müssen Sie die Vorgänge **Alles abholen**, **Ausgewählte abholen**, **Alles ausführen**, oder **ausgewählte durchführen** verwenden.

Nachdem Sie die Zeilen ausgewählt haben, die Sie ändern möchten, klicken Sie auf **Lieferart ändern**, um aufgefordert zu werden, die Optionen für den Zustellmodus auszuwählen. Wenn Sie mehrere zu ändernde Zeilen ausgewählt haben, zeigt POS nur Zustellungsmodi an, die für alle ausgewählten Produkte als zulässig konfiguriert wurden. Liefermodi können so konfiguriert werden, dass sie bestimmte Produkte und Lieferadressen unterstützen. Wenn es eine Versandart gibt, die für eine Produkt- und Adresskombination akzeptabel ist, für eine andere ausgewählte Produkt- und Adresskombination jedoch nicht akzeptabel ist, ist die Versandart nicht verfügbar. Möglicherweise müssen Sie die Zeilen einzeln auswählen und den Versandmodus für jede Zeile separat ändern, wenn Sie einen Versandmodus für ein Produkt auswählen möchten, das von einem anderen Produkt nicht unterstützt wird.  

Nachdem Sie den neuen Zustellungsmodus ausgewählt haben, wird die Transaktionsseite angezeigt. Wählen Sie die Option aus, um die Auswahl Ihres neuen Zustellmodus zu überprüfen. Wählen Sie die Registerkarte **Lieferung** in der Transaktionsliste.   
