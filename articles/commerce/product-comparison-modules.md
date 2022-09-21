---
title: Produktvergleichsmodule
description: Dieser Artikel beschreibt Produktvergleichsmodule und wie sie implementiert werden, damit Kunden Produktvergleiche auf Microsoft Dynamics 365 Commerce E-Commerce-Websites durchführen können.
author: ashishmsft
ms.date: 08/09/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 6fd851ce6b32d0772c3fe23c4d7bd4dae2616fdc
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474125"
---
# <a name="product-comparison-modules"></a>Produktvergleichsmodule

[!include [banner](../includes/banner.md)]

Dieser Artikel beschreibt Produktvergleichsmodule und wie sie implementiert werden, damit Kunden Produktvergleiche auf Microsoft Dynamics 365 Commerce E-Commerce-Websites durchführen können.

> [!NOTE]
> Das Module Produktvergleich und Produktvergleichs-Schaltfläche stehen ab der Dynamics 365 Commerce-Version 10.0.29 zur Verfügung. Sie können sowohl für Business-to-Consumer (B2C)- als auch für Business-to-Business (B2B)-Websites verwendet werden.

Mit der Produktvergleichsfunktion können Käufer Produktdetails auf einer Produktvergleichsseite vergleichen, um bessere Kaufentscheidungen zu treffen. Diese Funktionalität wird im Commerce Site Builder mithilfe des Produktvergleichsmoduls konfiguriert. Auf Produktlistenseiten (PLPs), wie z. B. Kategorieergebnissen, Suchergebnissen und Produktkollektionsseiten, können Sie eine Schaltfläche für den Produktvergleich konfigurieren, mit der Käufer Produkte zu einem Vergleichsfeld hinzufügen können. Diese Funktionalität wird im Site Builder mithilfe des Produktvergleichs-Schaltflächenmoduls konfiguriert, das wie [Schnellansichtsmodul](quick-view-module.md) funktioniert.

Wenn Websitebenutzer Produkte zum Vergleich hinzufügen, indem sie sie auf Produktkacheln auswählen, wird unten auf der Seite eine Vergleichsleiste angezeigt. Die Vergleichsleiste zeigt die Produkte, die der Käufer gerade vergleicht, zusammen mit einer kurzen Vorschau der Produkte. Site-Benutzer können auch Produkte von Produktdetailseiten (PDPs) hinzufügen, und sie können bestimmte Produktvarianten hinzufügen, um sie mit Produktmastern zu vergleichen.

Nachdem Kunden dem Vergleichsfach einige Produkte hinzugefügt haben, können sie **Vergleichen** auswählen, um auf eine Produktvergleichsseite umgeleitet werden. Die Produktvergleichsseite zeigt Produktdetails für jedes ausgewählte Produkt, sodass Kunden Bilder, Preise, Produktabmessungen (Größe, Stil und Farbe), aggregierte Bewertungsinformationen und andere Produktattribute vergleichen können.

Die folgende Abbildung zeigt Beispiele für die Schaltfläche „Produkt vergleichen“, die Schaltfläche „Aus Vergleich entfernen“, die Vergleichsleiste und die Produktvergleichsseite.

![Die Produktvergleichsübersicht zeigt die Schaltfläche „Produkt vergleichen“, die Schaltfläche „Aus Vergleich entfernen“, die Vergleichsleiste und die Produktvergleichsseite.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Die Produktvergleichsseite vergleicht einen Standardsatz von Produkteigenschaften und alle Attribute, die auf einem PDP für ein bestimmtes Produkt angezeigt werden können.
> - Eigenschaften wie Liefermodus, verfügbarer Lagerbestand und Maßeinheit können auf einer Produktvergleichsseite nicht angezeigt werden.
> - Kunden können dem Vergleichskorb Produkte aus verschiedenen Kategorien hinzufügen, sofern die Produkte aus demselben Katalog stammen.
> - Die Produktvergleichsfunktion ist derzeit auf den Vergleich von Produkten in einem einzelnen Katalog beschränkt. Websitebenutzer können keine katalogübergreifenden Vergleiche durchführen.
> - Sie sollten sicherstellen, dass die Eigenschaft **Modul clientseitig rendern** für alle Produktvergleichsmodule gelöscht wird.
> - Sie sollten sicherstellen, dass das Caching auf Seitenebene für alle Seiten deaktiviert ist, auf denen das Produktvergleichsmodul verwendet wird. Diese Seiten umfassen PDPs, PLPs und Produktvergleichsseiten. Weitere Informationen finden Sie unter [Konfigurieren des Seitencachings](e-commerce-extensibility/page-caching.md).

Die folgende Abbildung zeigt das Beispiel einer Produktvergleichsseite.

![Produktvergleichsseite.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Fügen Sie das Produktvergleichsmodul zu einer neuen Produktvergleichsseite hinzu

Sie können eine dedizierte Produktvergleichsseite erstellen, indem Sie dem Hauptteil einer Seite ein Produktvergleichsmodul hinzufügen. Neben der Möglichkeit für Kunden, Produktdetails verschiedener Produkte zu vergleichen, können Sie das Produktvergleichsmodul so konfigurieren, dass Kunden die Möglichkeit haben, ihren Kauf schnell abzuschließen, nachdem sie Produkte verglichen haben. Das Produktvergleichsmodul enthält auch einen Slot **Leerer Vergleich**, wo Sie ein Inhaltsblockmodul hinzufügen können, das den leeren Zustand beschreibt (z. B. „Ihr Produktvergleich ist leer“).

Um ein Produktvergleichsmodul einer neuen Produktvergleichsseite hinzuzufügen, führen Sie die folgenden Schritte aus.

1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. Geben Sie im Dialogfeld **Eine neue Seite erstellen** unter **Seitenname** einen passenden Seitennamen ein (z. B. **Produktvergleich**) und wählen dann **Weiter**.
1. Wählen Sie unter **Wählen Sie eine Vorlage** eine passende Vorlage aus (z. B. die auch von Ihrer Standard-Kategorieseite verwendet wird), und wählen Sie dann **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** ein Seitenlayout (z.B. **Flexibles Layout**) und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**.
1. Markieren Sie im Feld **Zuteilung von Zeitfenstern** die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Produktvergleich** und wählen Sie dann **OK**.
1. Im Slot **Schaltfläche „Schnellansicht“** wählen Sie die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Produktschnellansicht** und wählen Sie dann **OK**.
1. Legen Sie im Eigenschaftsfenster rechts die Eigenschaften für das **Produktschnellansicht**-Modul fest:
1. Wählen Sie im Slot **Leerer Vergleich** die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Inhaltsblock** und dann **OK** aus.
1. Legen Sie im Eigenschaftsfenster rechts die Eigenschaften für das **Inhaltsblockmodul** fest: 
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

Die folgende Abbildung zeigt ein Beispiel für eine leere Vergleichsseite im Site Builder.

![Produktvergleichsmodul.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Fügen Sie Produktkacheln auf Such- und Kategorieergebnisseiten eine Produktvergleichsschaltfläche hinzu

Mit der Produktvergleichsschaltfläche können Benutzer schnell ein Produkt zur Vergleichsleiste hinzufügen, wenn sie Produkte auf einer Listenseite durchsuchen. Sie können ein oder mehrere Produkte von einer Listenseite zum Vergleichsfach hinzufügen, ohne zu einem PDP gehen zu müssen.

Die Schaltfläche "Produktvergleich" von den Modulen Produktkollektion, Suchergebnisse und PDP-Kauffeld unterstützt.

Fügen Sie Produktkacheln auf Such- und Kategorieergebnisseiten eine Produktvergleichsschaltfläche hinzu, indem Sie folgende Schritte befolgen.

1. Gehen Sie im Site Builder zu **Seiten** und öffnen Sie die Kategorieseite, der Sie eine Produktvergleichsschaltfläche hinzufügen möchten.
1. Markieren Sie im Feld **Zuteilung von Zeitfenstern** die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Suchergebnisse** und wählen Sie dann **OK**.
1. Wählen Sie im Slot **Produktvergleichsschaltfläche** des Moduls **Suchergebnisse** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Produktvergleichsschaltfläche** und wählen Sie dann **OK**.
1. Legen Sie im Eigenschaftsfenster rechts die Eigenschaften für das **Produktvergleichsschaltfläche**-Modul fest:
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Geben Sie die maximale Anzahl von Produkten an, die in der Vergleichsleiste angezeigt werden sollen

Sie können die maximale Anzahl von Produkten angeben, die in der Vergleichsleiste angezeigt werden, indem Sie zu **Seiteneinstellungen \> Erweiterungen** im Site-Builder gehen. Sie können separate Höchstgrenzen für Desktop- und Mobil-/Tablet-Ansichten konfigurieren. Standardmäßig wird kein Limit erzwungen, wenn kein Höchstlimit definiert ist.

> [!NOTE]
> Für ein optimales Surferlebnis empfehlen wir Ihnen, die maximale Anzahl von Produkten in der Vergleichsleiste auf **2** für das mobile Ansichtsfenster und **4** für das Desktop-Ansichtsfenster, um das erforderliche horizontale Scrollen zu reduzieren.

So geben Sie die maximale Anzahl von Produkten an, die in der Vergleichsleiste angezeigt werden sollen.

1. Gehen Sie in Side Builder auf **Site-Einstellungen \> Erweiterungen**.
1. Für die Eigenschaft **Produkte im Vergleichslimit – Desktop-Geräte** geben Sie die maximale Anzahl von Produkten ein, die in der Vergleichsleiste für Desktop-Ansichtsfenster angezeigt werden sollen.
1. Für die Eigenschaft **Produkte im Vergleichslimit – mobile und Tablet-Geräte** geben Sie die maximale Anzahl von Produkten ein, die in der Vergleichsleiste für mobile und Tablet-Geräte-Ansichtsfenster angezeigt werden sollen.
1. Wählen Sie in der Befehlsleiste **Speichern und veröffentlichen** aus.

![Website-Einstellungen, um Produkte in der Vergleichsleiste einzuschränken.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
