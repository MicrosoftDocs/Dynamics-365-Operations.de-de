---
title: Websiteauswahlmodul
description: Dieses Thema befasst sich mit dem Websiteauswahlmodul und es wird beschrieben, wie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a1954f6b2fea35d5138218e6a2a23ab1fd04c8fc
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710302"
---
# <a name="site-picker-module"></a>Websiteauswahlmodul

[!include [banner](includes/banner.md)]

Dieses Thema befasst sich mit dem Websiteauswahlmodul und es wird beschrieben, wie Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Wenn ein Unternehmen unterschiedliche Websites in verschiedenen Märkten, Regionen und Gebiete hat, benötigen Websitebenutzer eine einfache Möglichkeit, zwischen Websites zu wechseln und ihre bevorzugte Einkaufsseite auszuwählen. Um diesem Szenario gerecht zu werden, können Benutzer mit dem Websiteauswahlmodul mehrere Sites durchsuchen. Eine Websiteauswahl wird auch empfohlen, wenn die [Geo-Erkennung und -Umleitung](geo-detection-redirection.md) für Ihre E-Commerce-Website implementiert wurden, sodass Kund\*innen die von ihnen angegebene Website-Präferenz überschreiben können, indem sie das Modul [Länder-/Regionsauswahl](country-region-picker-module.md) verwenden. 

Das Websiteaswahlmodul muss mit der Liste der Sites (Märkte, Regionen oder Gebietsschemas) konfiguriert sein, die Site-Benutzer durchsuchen können. Die folgende Abbildung zeigt ein Beispiel für ein Websiteauswahlmodul, das in der Kopfzeile einer Seite enthalten ist.

![Beispiel eines Websiteauswahlmoduls in der Kopfzeile einer Seite.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Eigenschaften des Websiteauswahlmoduls

| Eigenschaftenname | Wert                 | Description |
|---------------|-----------------------|-------------|
| Überschrift       | Text                  | Die Überschrift für das Modul. |
| Websiteoptionen  | Name, Bild, URL      | Diese Eigenschaft gibt einen Namen, einen Link zur Homepage der Site und ein optionales Bild für jede Site an, die im Modul enthalten ist. Das Bild kann eine Flagge oder eine Darstellung eines Marktes, einer Region oder eines Gebietsschemas sein. |

## <a name="add-a-site-picker-module-to-a-page"></a>Hinzufügen eines Websiteauswahlmoduls zu einer Seite

Das Websiteauswahlmodul kann dem **Websiteauswahl**-Slot des [Kopfzielenmoduls](author-header-module.md) hinzugefügt werden. Nach dem Hinzufügen eines Websiteauswahlmoduls können Sie die Modulüberschrift und die Site-Optionen definieren. Im Allgemeinen ist ein Kopfzeilenmodul in einem Kopfzeilenfragment enthalten, das über E-Commerce-Seiten für eine Website gemeinsam genutzt werden kann. 

Gehen Sie folgendermaßen vor, um das Websiteauswahlmodul einem Kopfzeilenmodul hinzuzufügen.

1. Wählen Sie im Slot **Websiteauswahl** das Kopfzeilenmodul des Kopfzeilenfragments, die Auslassungspunkte (**...**) und dann **Modul hinzufügen** aus.
1. Fügen Sie im Dialogfeld **Module auswählen** ein Modul **Websiteauswahl** hinzu und wählen Sie dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich **Websiteauswahl** die Option **Website-Optionsliste hinzufügen** aus. Eine bearbeitbare Option **Website-Optionsliste** erscheint.
1. Wählen Sie **Website-Optionsliste** aus. Das Dialogfeld **Website-Optionsliste** erscheint.
1. Unter **Websitename** geben Sie den Text des Websitenamens ein, der in der Dropdown-Liste der Websiteauswahl angezeigt wird.
1. Wählen Sie unter **Website-Umleitungs-URL** die Option **Link hinzufügen** aus. Der Flyout-Bereich **Link hinzufügen** wird angezeigt.
1. Wählen Sie im Flyout-Bereich **Link hinzufügen** die Option **Benutzerdefinierte Seite** und dann **Weiter** aus.
1. Wählen Sie aus der Website-URL-Liste die URL mit dem Pfad aus, den Sie beim Hinzufügen des Kanals zur Website erstellt haben (z. B. `www.adventure-works.com/fr-ca`), und wählen Sie dann **Anwenden** aus.
1. Wählen Sie **OK** aus.
1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen** aus, um die Seite zu veröffentlichen.

Im folgenden Beispiel wurde das Websiteauswahlmodul zum **Websiteauswahl**-Slot eines Kopfzeilenmoduls hinzugefügt, das in einem Kopfzeilenfragment namens **HeaderContainer** enthalten ist.

![Beispiel eines Websiteauswahlmoduls in einem Kopfzeilenfragment.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Kopfzeilenmodul](author-header-module.md)

[Breadcrumb-Modul](add-breadcrumb.md)

[Navigationsmenümodul](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
