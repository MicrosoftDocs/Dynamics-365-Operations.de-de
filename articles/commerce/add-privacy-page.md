---
title: Hinzufügen einer Datenschutzrichtlinienseite
description: In diesem Thema wird beschrieben, wie Sie eine Datenschutzrichtlinienseite zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797526"
---
# <a name="add-a-privacy-policy-page"></a>Eine Seite mit Datenschutzrichtlinien hinzufügen

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie eine Datenschutzrichtlinienseite zu Ihrer Site in Microsoft Dynamics 365 Commerce hinzufügen.

Die Einhaltung der Datenschutzbestimmungen umfasst organisatorische Maßnahmen, die die Benutzer der Website darüber informieren, wie ihre Daten erfasst und verarbeitet werden. Benutzer können dann entscheiden, wie sie mit ihren persönlichen Daten umgehen möchten, und entsprechende Maßnahmen ergreifen.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Microsoft-Datenschutzbestimmungen in Dynamics 365 Commerce prüfen

Um die Microsoft-Datenschutzbestimmungen zu prüfen, während Sie bei den Dynamics 365 Commerce Authoring-Tools angemeldet sind, wählen Sie die **Hilfe**-Taste (**?**) in der oberen rechten Ecke und wählen Sie dann **Datenschutz und Cookies** aus. Es wird eine neue Registerkarte geöffnet, die einen Link zur [Microsoft-Datenschutzerklärung](https://privacy.microsoft.com/privacystatement) enthält.

## <a name="build-a-privacy-policy-page-for-your-site"></a>Erstellen Sie eine Datenschutzrichtlinie für Ihre Website

In Dynamics 365 Commerce gibt es verschiedene Möglichkeiten, Benutzern Ihrer Website Zugriff auf Ihre Datenschutzbestimmungen zu gewähren. In diesem Abschnitt wird gezeigt, wie Sie eine Seite mit Datenschutzrichtlinien erstellen und dann mithilfe eines Fußzeilenfragments auf die Seite verweisen.

Die folgende Anleitung ist ein Beispiel zum Erstellen einer allgemeinen Datenschutzrichtlinie für eine Commerce-Site. Sie sind dafür verantwortlich, eine Lösung für Datenschutzrichtlinienseiten zu entwerfen und zu implementieren, die den gesetzlichen Anforderungen Ihres Unternehmens am besten entspricht.

Wechseln Sie zunächst in den Authoring-Tools zu der Site, für die Sie eine Seite mit Datenschutzrichtlinien erstellen möchten.

### <a name="create-a-template"></a>Eine Vorlage erstellen

> [!NOTE]
> Wenn bereits eine Vorlage erstellt wurde, die für die Datenschutzrichtlinie verwendet werden kann, fahren Sie mit dem Abschnitt [Erstellen Sie eine Seite mit Datenschutzrichtlinien](#build-a-privacy-policy-page) fort.

Um eine Vorlage zu erstellen, befolgen Sie diese Schritte.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine Seitenvorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie **Werbebanner-Vorlage** ein und wählen **OK**.
1. Fügen Sie in der Vorlage alle erforderlichen Module zu den erforderlichen Seiten-Slots hinzu. Bewegen Sie den Mauszeiger zur Orientierung über die roten Ausrufezeichen. (Zum Beispiel erfordert der Slot **HTML-Kopf** möglicherweise das Modul **Standardmäßiges externes Skript**.)
1. Fügen Sie im Slot **Text** das Modul **Standardseite** hinzu.
1. Fügen Sie im Modul **Standardseite** im Slot **Haupt** das Modul **Umfangreiches Inhaltsblockmodul** hinzu.
1. Fügen Sie im Modul **Umfangreiches Inhaltsblockmodul** das Modul **Umfangreiches Inhaltsblockelement** hinzu.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

### <a name="build-a-privacy-policy-page"></a>Erstellen einer Datenschutzrichtlinienseite

Gehen Sie folgendermaßen vor, um eine Datenschutzrichtlinienseite zu erstellen.

1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine Seite zu erstellen.
1. Wählen Sie im Dialogfeld **Eine Vorlage auswählen** die Vorlage für die Seite mit den Datenschutzrichtlinien aus.
1. Geben Sie einen Seitennamen und die Seiten-URL ein, und wählen Sie dann **OK** aus. 
1. Fügen Sie im Slot **Haupt** der Seite das Modul **Umfangreiches Inhaltsblockmodul** hinzu.
1. Fügen Sie im Modul **Umfangreiches Inhaltsblockmodul** das Modul **Umfangreiches Inhaltsblockelement** hinzu.
1. Wählen Sie im Eigenschaftenfenster für das Modul **Inhaltsreicher Block** die Option **Datenquelle hinzufügen** und dann **Rich-Text-Inhalt** aus.
1. Geben Sie im Rich-Text-Editor den Inhalt für die Seite mit den Datenschutzrichtlinien ein. Erweitern Sie den Rich-Text-Editor nach Bedarf in den Vollbildmodus.
1. Wenn Sie den Inhalt eingegeben haben, wählen Sie **Vorschau** aus, um eine Vorschau der Seite im Webbrowser anzuzeigen.
1. Vervollständigen Sie alle verbleibenden Ergänzungen der Seiten- und Moduleigenschaften.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.

Um die URL für die Datenschutzrichtlinienseite zu konfigurieren, gehen Sie wie folgt vor.

1. Navigieren Sie zu **URLs**, und wählen Sie die URL für die Datenschutzrichtlinienseite aus.
1. Wählen Sie **Veröffentlichen**, um die ausgewählte URL zu veröffentlichen.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Einen Link zur Datenschutzrichtlinienseite in einer Fußzeile erstellen

Sie können einem Fragment den Link zu einer Datenschutzrichtlinienseite hinzufügen. Auf diese Weise können Sie den Link freigeben und über mehrere Websiteseiten hinweg aktualisieren, indem Sie auf das Fragment verweisen. In diesem Beispiel wird gezeigt, wie einem Fußzeilenfragment ein Link zur Seite mit den Datenschutzrichtlinien hinzugefügt wird.

Gehen Sie folgendermaßen vor, um einem Fußzeilenfragment einen Link hinzuzufügen.

1. Wechseln Sie zu **Fragmente** und wählen Sie dann **Neu** aus, um ein Seitenfragment zu erstellen.
1. Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Fußzeile** aus.
1. Geben Sie unter **Name des Fragment** einen Namen für das Fragment ein und wählen Sie dann **OK** aus.
1. Fügen Sie dem Slot **Fußzeilenkategorie** das Modul **Fußzeilenelement** hinzu.
1. Wählen Sie im Eigenschaftenbereich rechts **Linktext** aus.
1. Geben Sie im Dialogfeld **Linktext** den Linktext und das Linkziel der Datenschutzrichtlinienseite ein, und klicken Sie dann auf **OK**.
1. Um die URL der Datenschutzrichtlinie zu erhalten, gehen Sie zu **Seiten**, dann zur Datenschutzrichtlinienseite, und kopieren Sie die URL aus dem Eigenschaftenbereich.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Zeigen Sie eine Vorschau des Fragments an und testen Sie den Link zur Seite mit den Datenschutzrichtlinien.

Das Fragment kann jetzt in der Vorlage für andere Websiteseiten referenziert werden. Wenn auf dieses Fragment im Modul **Fußzeile** einer Vorlage verwiesen wird, erscheint der Linkverweis auf allen Seiten, die mit dieser Vorlage erstellt wurden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Konformitätsübersicht](compliance-overview.md)

[Funktionen und Leistungsspektrum der Eingabehilfe](accessibility.md)

[Cookie-Compliance](cookie-compliance.md)

[Benutzer-IDs ersetzen, die nachverfolgten Inhalten zugeordnet sind](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
