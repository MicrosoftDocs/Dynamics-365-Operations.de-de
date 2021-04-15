---
title: Transaktions- und Quittungs-E-Mails einen QR-Code oder Barcode hinzufügen
description: In diesem Thema wird erläutert, wie Sie QR-Codes und Barcodes, die Auftrags-IDs darstellen, in Transaktions- und Quittungs-E-Mails in Microsoft Dynamics 365 Commerce einfügen.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: f8d9408090846799c1bb421c4b6e5e248d37fa07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797502"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>Transaktions- und Quittungs-E-Mails einen QR-Code oder Barcode hinzufügen

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In diesem Thema wird erläutert, wie Sie QR-Codes und Barcodes, die Auftrags-IDs darstellen, in Transaktions- und Quittungs-E-Mails in Microsoft Dynamics 365 Commerce einfügen.

Sie können QR-Codes und Barcodes problemlos in Transaktions-E-Mails einfügen, um die Suche nach Bestellungen in einer Einzelhandelsumgebung zu beschleunigen. Um QR-Codes und Barcodes in E-Mails einzufügen, verwenden Sie ein **\<img\>**-HTML-Tag, das ein QR-Code- oder Barcode-Bild von einem Generierungs- und Rendering-Dienst anfordert. Microsoft bietet diesen Dienst nicht an. Es gibt jedoch viele kostenlose oder kostengünstige Dienste, die QR-Codes oder Barcodes bereitstellen können, die dynamisch basierend auf einem Wert generiert werden, der in einer Abfragezeichenfolge übergeben wird.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>Einer Transaktions-E-Mail einen QR-Code oder Barcode hinzufügen

Führen Sie die folgenden Schritte aus, um einen QR-Code oder Barcode in eine Transaktions-E-Mail einzufügen, die im Rahmen eines E-Commerce-Kaufs gesendet wird.

1. Öffnen Sie den Quell-HTML-Code für die Transaktions-E-Mail-Vorlage und fügen Sie ein **\<img\>**-HTML-Tag hinzu, das auf Ihren QR-Code- oder Barcode-Dienst verweist. Hier ist ein Beispiel.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Hier eine Erläuterung des vorherigen Beispiels:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** repräsentiert die Domäne Ihres QR-Codes oder Barcode-Dienstes.
    - **data** stellt den Parameter dar, den der QR-Code- oder Barcode-Dienst verwendet, um den Inhalt zu empfangen, der als QR-Code oder Barcode gerendert werden soll.

        Der Wert **%salesid%** muss diesem Parameter zugewiesen werden. Beachten Sie in diesem Beispiel, dass der Wert auch als Alternativtext für das Bild verwendet wird.

    - **param1** und **param2** stellen zusätzliche optionale Parameter dar.

1. Gehen Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Organisations-E-Mail-Vorlagen** und laden Sie den aktualisierten HTML-Code in die entsprechende Transaktions-E-Mail-Vorlage hoch.

> [!NOTE]
> Die Parameter können zwischen QR-Code- und Barcode-Dienstleistern unterschiedlich sein. Wenden Sie sich daher unbedingt an Ihren Diensteanbieter, um die Parameter zu bestätigen, denen Sie Werte zuweisen müssen.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>Einer Quittungs-E-Mail einen QR-Code oder Barcode hinzufügen 

Führen Sie die folgenden Schritte aus, um einen QR-Code oder Barcode in eine Quittungs-E-Mail einzufügen, die nach dem Kauf am Point of Sale (POS) gesendet werden kann.

1. Öffnen Sie den Quell-HTML-Code für die Quittungs-E-Mail-Vorlage und fügen Sie ein **\<img\>**-HTML-Tag hinzu, das auf Ihren QR-Code- oder Barcode-Dienst verweist. Nachfolgend ein Beispiel.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Hier eine Erläuterung des vorherigen Beispiels:

    - **YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** repräsentiert die Domäne Ihres QR-Codes oder Barcode-Dienstes.
    - **data** stellt den Parameter dar, den der QR-Code- oder Barcode-Dienst verwendet, um den Inhalt zu empfangen, der als QR-Code oder Barcode gerendert werden soll.

        Der Wert **%receiptid%** muss diesem Parameter zugewiesen werden. Beachten Sie in diesem Beispiel, dass der Wert auch als Alternativtext für das Bild verwendet wird.

    - **param1** und **param2** stellen zusätzliche optionale Parameter dar.

1. Gehen Sie zu **Retail und Commerce \> Zentralverwaltungseinrichtung \> Parameter \> Organisations-E-Mail-Vorlagen** und laden Sie den aktualisierten HTML-Code in die E-Mail-Vorlage mit der E-Mail-ID **emailrecpt** hoch.

> [!NOTE]
> Die Parameter können zwischen QR-Code- und Barcode-Dienstleistern unterschiedlich sein. Wenden Sie sich daher unbedingt an Ihren Diensteanbieter, um die Parameter zu bestätigen, denen Sie Werte zuweisen müssen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[E-Mail-Zugänge von Modern POS (MPOS) senden](email-receipts.md)

[Mail-Vorlagen für Transaktionsereignisse erstellen](email-templates-transactions.md)
