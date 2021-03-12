---
title: Ein neues Produkt in Commerce erstellen
description: In diesem Thema wird beschrieben, wie Sie ein neues Produkt in Microsoft Dynamics 365 Commerce erstellen.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b578c1bdfe1c6b4bf66cc85cc09ed906fb812a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965310"
---
# <a name="create-a-new-product-in-commerce"></a>Ein neues Produkt in Commerce erstellen


[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie ein neues Produkt in Microsoft Dynamics 365 Commerce erstellen.

## <a name="overview"></a>Übersicht

Ein Produkt wird hauptsächlich durch eine Produktnummer, einen Namen und eine Beschreibung definiert. Es sind jedoch auch andere Daten erforderlich, ein Produkt oder einen Service zu beschreiben:

## <a name="create-a-new-product"></a>Neues Produkt erstellen

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Freigegebene Produkte nach Kategorie**.
1. Wählen Sie im Aktivitätsbereich **Neu** aus.
1. Wählen Sie in der Dropdownliste **Produktart** entweder **Artikel** oder **Dienstleistung** aus.
1. Wählen Sie in der Dropdownliste **Produktuntertyp** entweder **Produkt** (wenn das Produkt keine Varianten hat) oder **Produktmaster** (wenn das Produktvarianten haben wird) aus.
1. Geben Sie in das Feld **Produktnummer** eine Produktnummer ein, falls diese noch nicht vorbelegt ist.
1. Geben Sie in das Feld **Produktname** einen Produktnamen ein.
1. Geben Sie in das Feld **Suchbegriff** einen Suchbegriff ein.
1. Wählen Sie in der Dropdownliste **Einzelhandelskategorie** eine entsprechende Kategorie aus.
1. Wenn das Produkt ein Set ist, wählen Sie **Ja** für **Produktset**.
1. Wenn der Produktuntertyp Produktmaster ist, legen Sie die **Produktdimensionsgruppe** fest, um die unterstützten Varianten einzuschließen. Zu den Optionen zählen **Farbe**, **Größe**, **Stil** und **Konfiguration**. Bei Bedarf müssen Sie möglicherweise zusätzliche Produktdimensionsgruppen erstellen.
1. Wählen Sie in der Dropdownliste **Konfigurationstechnologie** eine entsprechende Option aus.
1. Wählen Sie **OK**.

Das folgende Bild zeigt das Beispiel eines hinzugefügten Produkts.

![Ein Produkt erstellen](media/create-new-product.png)

Sobald ein Produkt hinzugefügt wurde, können zusätzliche Daten dafür festgelegt werden, zum Beispiel **Produktbeschreibung**, **Variantengruppen**, **Dimensionsgruppen**, **Produkteigenschaften** und **Verwandte Produkte**.

Das folgende Bild zeigt die zusätzlichen Details eines Produkts.

![Produktdetails](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Produktvarianten erstellen

Wenn der Produktuntertyp **Produktmaster** ist, müssen bestimmte Varianten angelegt werden. 

Gehen Sie folgendermaßen vor, um ein Produktvarianten zu erstellen.

1. Wählen Sie im Aktivitätsbereich **Produktvarianten**.
1. Wenn im Aktionsbereich Variantengruppen ausgewählt wurden, wählen Sie **Variantenvorschläge*.
1. Wählen Sie die Varianten aus, die Sie für das Produkt unterstützen möchten.
1. Wählen Sie **Erstellen** aus.

## <a name="release-a-product"></a>Freigeben eines Produkts

Um ein Produkt zu verkaufen, muss es zunächst an eine juristische Person freigegeben werden.

1. Wählen Sie auf der Produktseite **Produkte freigeben**.

    ![Produkt freigeben](media/create-new-product-3.png)

1. Wählen Sie das freizugebende Produkt und anschließend **Nächste** aus.

    ![Freizugebendes Produkt auswählen](media/create-new-product-4.png)

1. Wählen Sie die freizugebende Produktsatzvarianten und anschließend **Nächste** aus.

    ![Freizugebende Varianten auswählen](media/create-new-product-5.png)

1. Wählen Sie die juristische Person und dann **Nächste** aus.

    ![Juristische Person auswählen](media/create-new-product-6.png)

1. Wählen Sie **Fertig stellen** aus.

    ![Produktfreigabe abschließen](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Ein freigegebenes Produkt konfigurieren

Sobald ein Produkt freigegeben ist, ist eine weitere Konfiguration erforderlich, die das Hinzufügen eines Preises zum Produkt umfasst.

1. Gehen Sie im Navigationsbereich zu **Module \> Einzelhandel und Handel \> Produkte und Kategorien \> Freigegebene Produkte nach Kategorie**.
1. Wählen Sie den Produktkategorieknoten für das freigegebene Produkt aus und wählen Sie das Produkt aus der Produktliste aus.
1. Wählen Sie im Aktionsbereich **Bearbeiten** aus.
1. Konfigurieren Sie im Abschnitt **Kauf** alle erforderlichen Eigenschaften, einschließlich **Einheit**, **Preis** und **Menge**.
1. Wählen Sie im Aktionsbereich **Bestätigen**, um sicherzustellen, dass für fehlende Felder keine Fehler gemeldet werden.
1. Wählen Sie im Aktionsbereich **Speichern** aus.

Das folgende Bild zeigt eine Beispielkonfiguration für ein freigegebenes Produkt.

![Freigegebenes Produkt konfigurieren](media/create-new-product-8.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Erstellen juristischer Personen](channels-legal-entities.md)

[Eine Variantengruppe erstellen](create-variant-group.md) 
