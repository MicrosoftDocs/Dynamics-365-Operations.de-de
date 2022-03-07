---
title: Mediengaleriemodul
description: Dieses Thema befasst sich mit Mediengaleriemodulen und beschreibt, wie diese Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 045568797722a621ea4e6c82d10dbb266b9e8162
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982465"
---
# <a name="media-gallery-module"></a>Mediengaleriemodul

[!include [banner](includes/banner.md)]

Dieses Thema befasst sich mit Mediengaleriemodulen und beschreibt, wie diese Seiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Mediengaleriemodule zeigen ein oder mehrere Bilder in einer Katalogansicht. Mediengaleriemodule unterstützen Miniaturansichten, die horizontal (als Zeile unter dem Bild) oder vertikal angeordnet werden (als Spalte neben dem Bild). Mediengaleriemodule bieten auch Funktionen, mit denen Bilder gezoomt (vergrößert) oder im Vollbildmodus angezeigt werden können. Um in einem Mediengaleriemodul gerendert zu werden, muss ein Bild in der Medienbibliothek des Commerce Site Builder verfügbar sein. Derzeit unterstützen Mediengaleriemodule nur Bilder.

Im Standardmodus verwendet ein Mediengaleriemodul zum Rendern der entsprechenden Produktbilder die Produkt-ID, die im Seitenkontext einer Produktdetailseite (PDP) verfügbar ist. Im Commerce Headquarters muss für alle Produkte ein Mediendateipfad festgelegt werden. Die Bilder sollten dann gemäß dem Dateipfad, der für die Produkte im Commerce Headquarters festgelegt wurde, in die Site-Builder-Medienbibliothek hochgeladen werden. Zu diesen Bildern gehören Bilder für Produkte und alle Produktvarianten. Weitere Informationen zum Hochladen von Bildern in die Site-Builder-Medienbibliothek finden Sie unter [Bilder hochladen](dam-upload-images.md).

Alternativ kann ein Mediengaleriemodul einen vollständig kuratierten Bildersatz auf einer Bildergalerieseite hosten. In diesem Fall bestehen keine Abhängigkeiten von der Produkt-ID oder dem Seitenkontext. In diesem Fall müssen Bilder in die Medienbibliothek des Site Builders hochgeladen und dort spezifiziert werden.

Hier sind einige Anwendungsbeispiele für Mediengaleriemodule:

- Rendern von Produktbildern auf einer PDP
- Rendern von Produktbildern auf einer Produktmarketingseite
- Anzeigen eines kuratierten Bildersatzes auf einer Marketingseite, z. B. einer Galerieseite

In dem Beispiel der folgenden Abbildung werden in einem Kauffeld auf einer PDP Produktbilder mithilfe eines Mediengaleriemoduls gehostet.

![Beispiel für ein Kauffeld auf einer Produktdetailseite, auf der Produktbilder mithilfe eines Mediengaleriemoduls gehostet werden](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Eigenschaften der Mediengalerie

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Bildquelle | **Seitenkontext** oder **Produkt ID** | Der Standardwert ist **Seitenkontext**. Wenn **Seitenkontext** ausgewählt ist, erwartet das Modul, dass die Seite die Produkt-ID bereitstellt. Wenn **Produkt ID** ausgewählt ist, muss die Produkt-ID für ein Bild als Wert für die **Produkt ID**-Eigenschaft angegeben werden. Diese Funktion steht in der Commerce-Version 10.0.12 zur Verfügung. |
| Produktkennung | Produkt-ID | Diese Eigenschaft gilt nur, wenn der Wert der Eigenschaft **Bildquelle** ist **Produkt-ID**. |
| Bildvergrößerung | **Inline** oder **Container** | Mit dieser Eigenschaft kann der Benutzer Bilder im Mediengaleriemodul zoomen. Ein Bild kann entweder inline oder in einem separaten Container neben dem Bild gezoomt werden. Diese Funktion ist in Version 10.0.12 verfügbar |
| Zoommaßstab | Eine Dezimalzahl | Diese Eigenschaft gibt den Skalierungsfaktor für das Zoomen von Bildern an. Wenn zum Beispiel der Wert auf **2,5** gesetzt ist, werden Bilder um das 2,5-Fache vergrößert.|
| Vollbild | **True** oder **False** | Diese Eigenschaft gibt an, ob Bilder im Vollbildmodus angezeigt werden können. Im Vollbildmodus können Bilder auch weiter vergrößert werden, wenn die Zoomfunktion aktiviert ist. Diese Funktion steht in der Commerce-Version 10.0.13 zur Verfügung. |
| Bilder | Bilder, die aus der Site-Builder-Medienbibliothek ausgewählt wurden | Bilder können nicht nur aus einem Produkt gerendert, sondern auch für ein Mediengaleriemodul kuratiert werden. Diese Bilder werden an alle verfügbaren Produktbilder angehängt. Diese Funktion steht in der Commerce-Version 10.0.12 zur Verfügung. |
| Ausrichtung der Miniaturansicht | **Vertikal** oder **horizontal** | Diese Eigenschaft gibt an, ob Miniaturansichten in einem vertikalen oder horizontalen Streifen angezeigt werden sollen. |

Die folgende Abbildung zeigt ein Beispiel eines Mediengaleriemoduls, in dem die Vollbild- und Zoomoptionen verfügbar sind.

![Beispiel eines Mediengaleriemoduls, in dem die Vollbild- und Zoomoptionen verfügbar sind](./media/ecommerce-media-zoom.png)

Die folgende Abbildung zeigt ein Beispiel eines Mediengaleriemoduls mit kuratierten Bildern (d. h. die angegebenen Bilder hängen nicht von der Produkt-ID oder dem Seitenkontext ab).

![Beispiel eines Mediengaleriemoduls mit kuratierten Bildern](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unit-Interaktion

Wenn die Bildquelle aus dem Seitenkontext abgeleitet wird, wird die Produkt-ID von der PDP zum Abrufen der Bilder verwendet. Das Mediengaleriemodul ruft Bilddateipfade für Produkte mithilfe der Commerce Scale Unit-Anwendungsprogrammschnittstellen (APIs) ab. Die Bilder werden dann aus der Medienbibliothek abgerufen, damit sie im Modul gerendert werden können.

## <a name="add-a-media-gallery-module-to-a-page"></a>Hinzufügen eines Mediengaleriemoduls zu einer Seite

Gehen Sie folgendermaßen vor, um ein Mediengaleriemodul einer Marketingseite hinzuzufügen.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** geben Sie unter **Vorlagenname** **Containervorlage** ein und wählen Sie **OK**.
1. Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.
1. Auf der Standardseite wählen Sie **Haupt**-Slot und dann die Ellipsen (**...**) und **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Marketingvorlage** aus. Unter **Seitenname** geben Sie **Mediengalerieseite** ein und wählen dann **OK**.
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Mediengallerie** und dann **OK** aus.
1. Im Eigenschaftenbereich für das Mediengaleriemodul wählen Sie unter **Bildquelle** **Produkt ID**. Geben Sie dann in das Feld **Produkt-ID** eine Produkt-ID ein.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Sie sollten die Bilder für das Produkt in einer Galerieansicht sehen können.
1. Um nur kuratierte Bilder im Eigenschaftenbereich zu verwenden, wählen Sie unter **Bildquelle** **Produkt ID**. Dann wählen Sie unter **Bilder** so oft wie nötig **Ein Bild hinzufügen**, um Bilder aus der Medienbibliothek hinzuzufügen.
1. Legen Sie alle zusätzlichen Eigenschaften fest, die Sie festlegen möchten, z. B. **Bildzoom**, **Zoomfaktor** und **Ausrichtung der Miniaturansichten**.
1. Wenn Sie fertig sind, wählen Sie **Speichern** und dann **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Containermodul](add-container-module.md)

[Bilder hochladen](dam-upload-images.md)
