---
title: Abonnierenmodul
description: Dieser Artikel behandelt Abonnierenmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 23b74f5853ffb7f191ea7ee3da0d3238db339d34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852692"
---
# <a name="subscribe-module"></a>Abonnierenmodul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt Abonnierenmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.

Abonnierenmodule können auf WebsiteSeiten verwendet werden, um Kundeninformationen für Newsletter oder Aktionen zu erfassen.

Die folgende Abbildung zeigt ein Beispiel für ein Abonnierenmodul in der Fußzeile auf einer Adventure Works-Websiteseite.

![Beispiel für ein Abonnierenmodul in der Fußzeile auf einer Adventure Works-Websiteseite](./media/Subscribe.PNG)

> [!IMPORTANT]
> - Das Abonnierenmodul ist in der Commerce-Modulbibliothek ab der Dynamics 365 Commerce-Version 10.0.20 verfügbar.
> - Das Abonnierenmodul wird im Adventure Works-Design vorgestellt.
> - Das Abonnierenmodul erfordert eine Datenaktivitätserweiterung, um mit einigen Marketing-E-Mail-Anbietern zusammenzuarbeiten, damit nach dem Erfassen von Kundeninformationen Newsletter oder Werbe-E-Mails gesendet werden können.

## <a name="subscribe-module-properties"></a>Eigenschaften Abonnierenmodul

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Überschrift       | Überschriftentext und Überschriftsmarkierung (**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**) | Eine Textüberschrift für das Abonnierenmodul, wie z. B. **Abonnieren Sie den Newsletter** oder **Melden Sie sich für 10 % Rabatt an**. |
| Absatz     | Absatztext | Das Abonnierenmodul unterstützt Absatztext im Rich-Text-Format, um zusätzliche Details für den Handlungsaufruf in der Überschrift bereitzustellen. |

## <a name="add-a-subscribe-module-to-a-new-page"></a>Ein Abonnierenmodul einer neuen Seite hinzufügen

Um ein Abonnierenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften im Commerce-Website-Generator festzulegen, führen Sie die folgenden Schritte aus.

1. Gehen Sie auf **Vorlagen** und öffnen Sie die Marketingvorlage für die Homepage Ihrer Site (oder erstellen Sie eine neue Marketingvorlage).
1. Auf der Standardseite wählen Sie **Haupt**-Slot und dann die Ellipsen (**...**) und **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Abonnement** und wählen Sie dann **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zu **Seiten** und öffnen Sie die Homepage der Site (oder erstellen Sie eine neue Homepage mithilfe der Marketingvorlage).
1. Auf dem Seitenüberblick wählen Sie den Slot **Haupt** und wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Abonnement** und wählen Sie dann **OK**.
1. Fügen Sie im Eigenschaftenbereich des Abonnierenmoduls eine Überschrift hinzu, wie z. B. **Abonnieren**.
1. Fügen Sie einen Absatztext hinzu, z. B **Neueste Trends, Styles und Aktionen. Sind Sie schon auf der Liste? Melden Sie sich zu einem Abonnement an und sichern Sie sich die neuesten heißen Angebote!**
1. Wählen **Speichern** und dann **Vorschau** aus, um eine Vorschau der Seite anzuzeigen.
1. Wählen **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Adventure Works-Design](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
