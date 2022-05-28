---
title: Schnellansichtsmodul
description: Dieses Thema enthält Schnellansichtsmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 68808da1ad2b3474852b3544df55db948f8758cd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692699"
---
# <a name="quick-view-module"></a>Schnellansichtsmodul

[!include [banner](includes/banner.md)]

Dieses Thema enthält Schnellansichtsmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Mit dem Schnellansichtsmodul können Benutzer Produktinformationen schnell anzeigen, wenn sie Produkte auf einer Listenseite durchsuchen und ein oder mehrere Produkte über die Listenseite zum Warenkorb hinzufügen, ohne zur Produktdetailseite (PDP) wechseln zu müssen. Das Schnellansichtsmodul bietet einen Überblick über die Produktinformationen, die Benutzer benötigen, um eine Entscheidung zum Hinzufügen zum Warenkorb zu treffen. Es enthält auch einen Link zum PDP, sodass Benutzer zusätzliche Produktdetails und Kaufoptionen anzeigen können.

Das Schnellansichtsmodul wird von den Modulen [Produktkollektion](product-collection-module-overview.md) und [Suchergebnisse](search-result-module.md) unterstützt.

> [!IMPORTANT]
> Das Schnellansichtsmodul ist ab der Version 10.0.17 von Commerce verfügbar.

Das folgende Bild zeigt ein Beispiel eines Schnellansichtsmoduls auf einer Produktlistenseite.

![Beispiel eines Schnellansichtsmoduls auf einer Produktlistenseite.](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a>Moduleigenschaften

Das Schnellansichtsmodul unterstützt einige der gleichen Funktionen wie das Kauffeldmodul. Daher ähneln die Eigenschaften eines Schnellansichtsmoduls den Eigenschaften eines Kauffeldmoduls.

| Eigenschaft | Werte | Beschreibung |
|----------------|--------|-------------|
| Überschriften-Tag | **H1**, **H2**, **H3**, **H4**, **H5** oder **H6** | Diese Eigenschaft definiert das Überschriften-Tag für den Produkttitel. Wenn sich das Schnellansichtsmodul oben auf der Seite befindet, sollte diese Eigenschaft auf **H1** festgelegt werden, um die Zugänglichkeitsstandards zu erfüllen. |
| Benutzerdefinierten Preis zulassen | **True** oder **False** | Wenn diese Eigenschaft auf **Wahr** gesetzt ist, kann der Benutzer einen benutzerdefinierten Preis eingeben. |
| Minimaler Preis | Ganzzahl | Diese Eigenschaft gilt nur, wenn die **Benutzerdefinierten Preis zulassen**-Eigenschaft auf **Wahr** gesetzt ist. Es definiert den Mindestpreis, den der Benutzer eingeben kann (z. B. 1 USD). |
| Maximaler Preis | Ganzzahl | Diese Eigenschaft gilt nur, wenn die **Benutzerdefinierten Preis zulassen**-Eigenschaft auf **Wahr** gesetzt ist. Es definiert den Maximalpreis, den der Benutzer eingeben kann (z. B. 1.000 USD). |

## <a name="commerce-site-builder-settings"></a>Commerce-Website-Generator-Einstellungen

Wie das Kauffeldmodul berücksichtigt auch das Schnellansichtsmodul die Einstellungen unter **Seiteneinstellungen \> Erweiterungen \> Produkt in den Warenkorb legen**. Die **Zur Warenkorbseite navigieren**-Einstellung wird ignoriert, da sie nicht mit dem Zweck des Schnellansichtsmoduls übereinstimmt, mit dem Benutzer mehrere Produkte auf einer Listenseite durchsuchen und in den Warenkorb legen können, ohne sich von der Listenseite zu entfernen.

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a>Hinzufügen eines Schnellansichtsmoduls zu einem Produktsammlungsmodul

Ein Schnellansichtsmodul kann den Modulen Produktkollektion und Suchergebnisse hinzugefügt werden.

Gehen Sie folgendermaßen vor, um ein Schnellansichtsmodul im Commerce-Website-Generator einem Produktsammlungsmodul hinzuzufügen.

1. Rufen Sie **Seiten** auf und wählen Sie dann die Startseite für die Fabrikam-Website aus.
1. Gehen Sie zu einem **Produktsammlungs**-Modul auf der Startseite, wählen Sie die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Schnellansicht** und dann **OK** aus.
1. Im Eigenschaftenbereich des **Schnellansicht**-Moduls wählen Sie **Überschrift**. Im **Überschrift**-Dialogfeld stellen Sie das **Überschriftenebene**-Feld auf **H2** und wählen dann **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Produktsammelmodul](product-collection-module-overview.md)

[Suchergebnismodul](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
