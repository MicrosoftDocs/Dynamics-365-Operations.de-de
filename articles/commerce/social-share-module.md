---
title: Social-Share-Modul
description: Dieses Thema enthält Social-Share-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022075"
---
# <a name="social-share-module"></a>Social-Share-Modul

[!include [banner](includes/banner.md)]

Dieses Thema enthält Social-Share-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

## <a name="overview"></a>Übersicht

Mithilfe von Social-Share-Modulen können Benutzer URLs von E-Commerce-Websiteseiten in sozialen Medien wie z. B. Facebook, Twitter, Pinterest und LinkedIn verwenden. Webite-Seiten-URLs können auch per E-Mail freigegeben werden. Social-Share-Module werden häufig auf Produktdetailseiten (PDPs) verwendet, um Benutzern den Austausch von Produktinformationen zu erleichtern.

Jedes Social-Share-Modul ist ein Container für Social-Share-Artieklmodule. Jedes Social-Share-Artikelmodul kann so konfiguriert werden, dass es auf eine bestimmte Social-Media-Website verweist. Integration in Facebook, Twitter, Pinterest, LinkedIn und E-Mail wird sofort unterstützt. Wenn ein Website-Benutzer ein Social-Media-Symbol auswählt, wird ein HTML-IFrame für die jeweilige Social-Media-Website gestartet. Innerhalb des IFrames kann sich der Benutzer anmelden und den angezeigten Seiteninhalt veröffentlichen.

Jede Social-Media-Plattform kann Cookies verfolgen. Daher müssen Benutzer der Website für dieses Modul die Benachrichtigung über die Zustimmung zur Cookie-Zustimmung akzeptieren. Wenn die Zustimmung zum Cookie nicht akzeptiert wird, wird das Modul auf der Seite ausgeblendet. Weitere Informationen finden Sie unter [Cookie-Compliance](cookie-compliance.md).

Die folgende Abbildung zeigt ein Beispiel für ein Social-Share-Modul, das auf einer Produktdetailseite verwendet wird.

![Beispiel eines Social-Share-Moduls](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Social-Share-Moduleigenschaften

| Eigenschaftenname             | Wert                 | Beschreibung |
|---------------------------|-----------------------|-------------|
| Beschriftung                  | Text | Diese Eigenschaft gibt eine Beschriftung für das Modul an. |
| Ausrichtung | **Horizontal** oder **vertikal**  | Diese Eigenschaft definiert die Layoutausrichtung für die Social-Media-Elemente. |

## <a name="social-share-item-module-properties"></a>Social-Share-Artikelmoduleigenschaften
| Eigenschaftenname             | Wert                 | Beschreibung |
|---------------------------|-----------------------|-------------|
| Soziale Medien              | **Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **E-Mail** | Ein Dropdown-Menü mit einer Liste von Social-Media-Plattformen. |
| Symbol |Bild    | Dies ist das Bild, das für die jeweiligen sozialen Medien angezeigt wird. Als eine bewährte Methode, finden Sie das empfohlene Bild für jede Plattform im SDK der Social-Media-Plattform. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Hinzufügen eines Social-Share-Moduls zu einem Kauffeldmodul

Um ein Social-Share-Modul einem Kauffeldmodul hinzuzufügen, befolgen Sie diese Schritte.

1. Wählen Sie auf der Fabrikam-Website **Seiten** und dann die Seite **DefaultPDP** aus, um die Produktdetailseite zu öffnen. 
1. Wählen Sie im Slot **Kauffeld (erforderlich)** die Ellipsen-Schaltfläche ( **...** ) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Social-Share** und dann **OK** aus.
1. Wählen Sie im Slot **Social-Share** die Ellipsen-Schaltfläche ( **...** ) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **SocialShare** und dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich des Moduls **SocialShare** unter **Ausrichtung** **Horizontal**. Fügen Sie nach Bedarf eine Beschriftung hinzu.
1. Wählen Sie im Slot **SocialShare** die Ellipsen-Schaltfläche ( **...** ) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **SocialShareItem** und dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich des Moduls **SocialShareItem** unter **Soziale Medien** **Facebook**.
1. Wählen Sie im Eigenschaftenbereich des Moduls **SocialShareItem** unter **Symbol** **+ Ein Bild hinzufügen**.
1. Wählen Sie im Dialogfeld **Medienauswahl** das Facebook-Logobild und dann **OK** aus. Wenn kein Facebook-Logobild vorhanden ist, wählen Sie **Neues Medienelement hochladen** aus, um eins hochladen.
1. Fügen Sie nach Bedarf zusätzliche **SocialShareItem** -Module hinzu und konfigurieren Sie diese.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Auf der Seite wird das Social-Share-Modul angezeigt.
1. Wählen **Bearbeiten beenden** , um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen** , um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Kauffeldmodul](add-buy-box.md)

[Cookie-Compliance](cookie-compliance.md)
