---
title: Breadcrumb-Modul
description: Dieses Thema behandelt Breadcrumb-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.openlocfilehash: 050ba58073d6e7e7710ab768e7ce3ea628440f4d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346947"
---
# <a name="breadcrumb-module"></a>Breadcrumb-Modul

[!include [banner](includes/banner.md)]

Dieses Thema behandelt Breadcrumb-Module und es wird beschrieben, wie diese Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Breadcrumb-Module werden verwendet, um eine sekundäre Navigation auf Websiteseiten bereitzustellen. Sie werden normalerweise oben auf einer Seite unterhalb der Kopfzeile angezeigt. Obwohl Breadcrumb-Module zu jeder Seite hinzugefügt werden können, werden sie am häufigsten auf Produktdetailseiten (PDPs) verwendet, um die Produktkategoriehierarchie anzuzeigen und eine schnelle Möglichkeit zum Bewegen auf einer Site bereitzustellen. Ein Breadcrumb-Modul kann auch verwendet werden, um einen Link Zurück zu Ergebnissen anzuzeigen, wenn Benutzer einen PDP über eine Such- oder Listenseite öffnen. Auf diese Weise können Benutzer schnell zu ihrer gefilterten Listenseite zurückkehren, um mit dem Einkaufen fortzufahren.

Auf Seiten mit Produktkategoriekontext, wie z. B. PDPs und Kategorieseiten, zeigen Breadcrumb-Module die Kategoriehierarchie. Auf Seiten ohne Kategoriekontext werden Breadcrumb-Module standardmäßig **&lt;Site-Root&gt; / &lt;Aktuelle Seite&gt;** angezeigt. Breadcrumb-Module können auch manuell auf anderen Arten von Websiteseiten konfiguriert werden, um Links zu bestimmten Seiten auf der Website anzuzeigen.

> [!NOTE]
> Das Breadcrumb-Modul ist in Dynamics 365 Commerce 10.0.12 verfügbar.

Das folgende Bild zeigt ein Beispiel eines Breadcrumb-Moduls, das die Kategoriehierarchie auf einem PDP zeigt.

![Beispiel eines Breadcrumb-Moduls.](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Einstellungen des Breadcrumb-Moduls

Das Breadcrumb-Modul basiert auf der **Breadcrumb-Anzeigetyp auf PDP** Einstellung, die unter **Seiteneinstellungen \> Erweiterungen** im Site Builder definiert wird. Diese Einstellung hat drei mögliche Werte:

- **Kategoriehierarchie anzeigen** – Wenn dieser Wert ausgewählt ist, zeigt das Breadcrumb-Modul die vollständige Kategoriehierarchie des Produkts an, das auf dem PDP angezeigt wird.
- **Zeigen Sie zurück zu den Ergebnissen** – Wenn dieser Wert ausgewählt ist, zeigt das Breadcrumb-Modul einen Link Zurück zu Ergebnissen auf einem PDP an, wenn der Benutzer den PDP über ein Modul geöffnet hat, das einen Link Zurück zu Ergebnissen ermöglicht. Diese Funktion ist verfügbar, wenn Benutzer von Seiten mit Kategorien, Such-, Listen- und Empfehlungslisten navigieren. Um diese Funktionalität zu unterstützen, verfügen die Module für Produktsammlung und Suchergebnisse über eine Eigenschaft mit dem Namen **Lassen Sie die Ergebnisse auf PDP zurück**. Mit dieser Eigenschaft können Sie flexibel definieren, welche Module die Linkfunktionalität Zurück zu den Ergebnissen auf dem PDP unterstützen sollen. Zum Beispiel wenn **Zeigen Sie zurück zu den Ergebnissen** für den **Breadcrumb-Anzeigetyp auf PDP** Einstellung des Breadcrumb-Moduls ausgewählt ist und **Lassen Sie die Ergebnisse auf PDP zurück** ausgewählt ist für das Suchergebnismodul der Suchseite, wird ein Link Zurück zu den Ergebnissen angezeigt, wenn Benutzer von der Suchseite zu einem PDP navigieren.
- **Kategoriehierarchie anzeigen und zurück zu den Ergebnissen** – Dieser Wert ist eine Kombination der beiden vorherigen. Wenn dieser Wert ausgewählt ist, zeigt das Breadcrumb-Modul sowohl die vollständige Kategoriehierarchie als auch einen Link Zurück zu den Ergebnissen (falls konfiguriert) auf einem PDP an.

> [!IMPORTANT]
> Diese Einstellungen sind in Dynamics 365 Commerce 10.0.12 verfügbar. Wenn Sie eine Aktualisierung von einer älteren Version von Dynamics 365 Commerce durchführen, müssen Sie die Datei appsettings.json manuell aktualisieren. Anweisungen zum Aktualisieren der Datei appsettings.json finden Sie unter [SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="breadcrumb-module-properties"></a>Eigenschaften des Breadcrumb-Moduls

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Stamm | Text oder Verknüpfung| Diese optionale Eigenschaft gibt den Linktext und ein Linkziel für das Breadcrumb-Site-Stammverzeichnis an. Wenn diese Eigenschaft nicht konfiguriert ist, wird kein Stamm definiert. |
| Breadcrumb-Verknüpfung | Verknüpfen | Diese optionale Eigenschaft gibt Verknüpfungen für einen manuell konfigurierten Breadcrumb an, wenn diese Verknüpfungen erforderlich sind. Links werden in der Reihenfolge angezeigt, in der sie aufgeführt sind. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Ein Breadcrumb-Modul einer neuen Seite hinzufügen

Um ein Breadcrumb-Modul einem PDP hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie zu **Website-Einstellungen \> Erweiterungen** und wählen dann für die Einstellung **Breadcrumb-Anzeigetyp auf PDP** die Option **Kategoriehierarchie anzeigen** aus.
1. Gehen Sie zu **Vorlagen** und wählen Sie die PDP-Vorlage aus.
1. Im Slot **Container**, der das Kauffeldmodul enthält, wählen Sie die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Breadcrumb** und dann **OK** aus.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehe Sie zu **Seiten** und öffnen Sie einen PDP, der die PDP-Vorlage verwendet. Wenn noch kein PDP vorhanden ist, erstellen Sie einen.
1. Im Slot **Container**, der das Kauffeldmodul enthält, wählen Sie die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Breadcrumb** und dann **OK** aus.
1. Im Eigenschaftenbereich des Slots **Breadcrumb** wählen Sie unter **Root** den **Link Text**.
1. In dem **Link Text** Dialogfeld geben Sie **Startseite** ein und wählen dann unter **Linkziel** **Fügen Sie einen Link hinzu**.
1. Im Dialogfeld **Fügen Sie einen Link hinzu** wählen Sie den Link für die Breadcrumb-Ursprung und wählen Sie **OK**.
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Navigationsmenümodul](nav-menu-module.md)

[Siteauswahlmodul](site-selector.md)

[Übersicht der Standard-Kategorie-Landingpage und Suchergebnisseite](category-search-page-overview.md)

[Produktsammelmodule](product-collection-module-overview.md)

[Kauffeldmodul](add-buy-box.md)

[SDK- und Modulbibliothekupdates](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]