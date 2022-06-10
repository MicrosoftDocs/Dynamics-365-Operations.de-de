---
title: Akkordeon Modul
description: Dieses Thema behandelt Akkordeonmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e17476d745da6f498b4f3ed90d55b0d13a0264b6
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780688"
---
# <a name="accordion-module"></a>Akkordeonmodul

[!include [banner](includes/banner.md)]

Dieses Thema behandelt Akkordeonmodule und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Akkordeonmodule sind containerähnliche Module, mit denen die Informationen oder Module auf einer Seite organisiert werden, indem eine zusammenklappbare schubladenähnliche Funktion bereitgestellt wird. Ein Akkordeonmodul kann auf jeder Seite verwendet werden.

In jedem Akkordeonmodul können ein oder mehrere Akkordeongegenstandsmodule hinzugefügt werden. Jedes Akkordeonelementsmodul repräsentiert eine reduzierbare Schublade. edem Akkordeonmodul können ein oder mehrere Akkordeonartikelmodule hinzugefügt werden. Es gibt keine Einschränkungen hinsichtlich der Modultypen, die einem Akkordeonartikeltmodul hinzugefügt werden können.

Das folgende Bild zeigt ein Beispiel eines Akkordeonmoduls, mit dem Informationen auf der Seite mit häufig gestellten Fragen (FAQ) eines Geschäfts organisiert werden.

![Beispiel eines Akkordeonmoduls.](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a>Eigenschaften des Akkordeonmoduls

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift | Text | Diese Eigenschaft gibt eine optionale Textüberschrift für das Akkordeonmodul an. |
| Alle Ebenen erweitern | **True** oder **False** | Wenn der Wert auf **Wahr** eingestellt ist, ist die Funktion zum Erweitern/Reduzieren aktiviert, sodass alle Elemente im Akkordeonmodul erweitert und reduziert werden können. |
| Interaktionsstil | **Unabhängig** oder **Nur ein Artikel erweitern** | Diese Eigenschaft definiert den Interaktionsstil für Akkordeonelemente. Wenn der Wert auf **Unabhängig** eingestellt ist, kann jeder Akkordeonartikel unabhängig erweitert oder reduziert werden. Wenn der Wert auf **Erweitern Sie nur einen Artikel** eingestellt ist, kann jeweils nur ein Artikel erweitert werden. Wenn Elemente erweitert werden, werden zuvor erweiterte Artikel reduziert. |

## <a name="accordion-item-module-properties"></a>Eigenschaften des Akkordeonartikelmoduls

| Eigenschaftenname | Werte | Beschreibung |
|----------------|--------|-------------|
| Titel | Text | Diese Eigenschaft gibt die Textüberschrift für das Akkordeonelementmodul an. Durch Auswahl des Titelbereichs können Benutzer den Abschnitt erweitern oder reduzieren. |
| Standardmäßig erweitern | **True** oder **False** | Wenn der Wert auf **Wahr** eingestellt ist, wird das Akkordeonelement beim Laden der Seite standardmäßig erweitert. |

## <a name="add-an-accordion-module-to-a-faq-page"></a>Ein Akkordeonmodul einer FAQ-Seite hinzufügen

Um ein Akkordeonmodul einer FAQ-Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Seiten** und verwenden Sie die Fabrikam-Marketingvorlage (oder eine Vorlage ohne Einschränkungen), um eine neue Seite mit dem Namen **FAQ speichern** zu erstellen.
1. Auf der **Standardseite** wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Akkordeon** und dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich des Akkordeonmoduls die Option **Überschrift** neben dem Stiftsymbol.
1. In dem **Überschrift** Dialogfeld unter **Überschriftstex** geben Sie **Häufig gestellte Fragen** ein. Wählen Sie dann **OK** aus.
1. Wählen Sie im Eigenschaftenbereich des Akkordeonmoduls das Kontrollkästchen **alle erweitern anzeigen** und dann im Feld **Interaktionsstil** **Unabhängig**.
1. Wählen Sie im Slot **Akkordeon** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Akkordeonelement** und dann **OK** aus.
1. Im Eigenschaftenbereich des Akkordeonelementmoduls unter **Titel** geben Sie den Titeltext ein (z. B. **Wie funktionieren Retouren?**).
1. Wählen Sie im Slot **Akkordeonelement** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Textblock** und dann **OK** aus.
1. Geben Sie im Eigenschaftenbereich des Textblockmoduls einen Textabsatz ein (z. B. **Rücksendungen müssen über das Call Center bearbeitet werden. Wenden Sie sich für Rücksendungen an 1-800-FABRIKAM. Produkte haben ein 30-tägiges Rückgaberecht. Rückgaben müssen innerhalb dieses Zeitraums eingeleitet werden.**).
1. In dem **Akkordeon** Slot fügen Sie ein paar weitere Akkordeonelementmodule hinzu. Fügen Sie in jedem Akkordeonelementmodul ein Textblockmodul mit Inhalt hinzu.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen. Auf der Seite wird ein Akkordeonmodul angezeigt, das den von Ihnen hinzugefügten Inhalt enthält.
1. Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Registerkartenmodul](add-tab.md)

[Textblockmodul](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
