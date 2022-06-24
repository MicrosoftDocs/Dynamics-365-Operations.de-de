---
title: Customer Voice in E-Commerce-Websites einbinden
description: In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 Customer Voice in Dynamics 365 Commerce-E-Commerce-Website-Seiten integrieren.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850329"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>Customer Voice in E-Commerce-Websites einbinden

[!include [banner](../includes/banner.md)]

In diesem Artikel wird beschrieben, wie Sie Microsoft Dynamics 365 Customer Voice in Dynamics 365 Commerce-E-Commerce-Website-Seiten integrieren.

Sie können [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/) in Ihre E-Commerce-Website integrieren, um Kunden-Feedback in Echtzeit zu sammeln, zu analysieren und zu verfolgen. Um mit der Integration zu beginnen, müssen Sie ein Konto erstellen und eine Customer Voice-Projektvorlage für die Art von Feedback auswählen, das Sie sammeln möchten.

## <a name="integrate-the-customer-voice-service"></a>Integrieren des Customer Voice-Diensts

Um ein Customer Voice-Konto zu erstellen, gehen Sie zu [Customer Voice](https://dynamics.microsoft.com/customer-voice/overview/), und folgen Sie den Anweisungen.

Nachdem Sie ein Customer Voice-Konto erstellt haben und sich angemeldet haben, besteht der nächste Schritt darin, eine Projektvorlage für die Art von Feedback auszuwählen, das Sie sammeln möchten.

Führen Sie die folgenden Schritte aus, um eine Customer Voice-Projektvorlage auszuwählen.

1. Gehen Sie zur [Customer Voice-Projektvorlagenseite](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Wählen Sie **Beginnen**.
1. Wählen Sie die Projektvorlage für den Feedbacktyp aus, den Sie sammeln möchten, und wählen Sie dann **Weiter**.
1. Wählen Sie auf der **Senden**-Registerkarte unter **Einbettungsformat auswählen** ein Einbettungsformat aus. Das **Eingebetteter Code**-Feld zeigt den Code, der in Commerce Site Builder eingebettet werden muss.

Die Beispiele in diesem Artikel verwenden die **Periodische Kundenbefragung**-Projektvorlage und das eingebettete Format **Schaltfläche**.

Die folgende Beispielabbildung zeigt die **Periodische Kundenbefragung**-Projektvorlagenseite, wo die Option für das eingebettete Format **Schaltfläche** ausgewählt ist, und der Einbettungscode für diese Option im Feld **Eingebetteter Code** angezeigt wird. Drei separate Aktionen sind erforderlich, um den bereitgestellten Code wie in den folgenden Abschnitten beschrieben in Ihre Website-Seiten einzubetten.

![Die Seite für die periodische Kundenumfrage von Customer Voice mit ausgewählter Schalfläche-Option.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Die externe Skript-URL einbetten

Auf allen Website-Seiten, die eine Customer Voice-Umfrage enthalten sollen, müssen Sie die externe Skript-URL einbetten, die Customer Voice im Einbettungscode bereitgestellt hat. Die beste Methode zum Einbetten des Skripts in mehrere Website-Seiten besteht darin, im Site Builder ein Fragment zu erstellen, das die externe Skript-URL enthält, und das Fragment dann den entsprechenden Seitenvorlagen hinzuzufügen. Nachdem Sie eine aktualisierte Vorlage veröffentlicht haben, sieht der eingebettete externe Skriptcode auf den Seiten der betroffenen Website wie im folgenden Beispiel aus.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Weitere Informationen zu Fragmenten erhalten Sie unter [Arbeiten mit Fragmenten](work-with-fragments.md).

> [!NOTE]
> Sie müssen dem Fragment nur die URL hinzufügen. Das externe Skriptmodul fügt den anderen Skriptcode hinzu.

Führen Sie die folgenden Schritte aus, um die externe Skript-URL in ein Fragment einzubetten.

1. Erstellen Sie im Site Builder ein Fragment, das auf dem [Externes Skript-Modul](script-module.md) basiert.
1. Wählen Sie im neuen Fragment den Platz **Externes Standardskript** aus.
1. Geben Sie in dem **Externes Standardskript**-Eigenschaftenbereich im Feld **Skriptquelle** wie in der folgenden Beispielabbildung gezeigt die URL des externen Skripts ein.

    ![Externe Skript-URL im Skriptquelle-Feld für das neue Fragment.](media/customer-voice-integration-2.png)

1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen**, um das Fragment zu veröffentlichen.

Das neue Fragment, das den eingebetteten externen Skriptblock enthält, kann jetzt der entsprechenden Seitenvorlage hinzugefügt werden.

### <a name="embed-the-external-style-sheet-code"></a>Den externen Stylesheet-Code einbetten

Auf allen Website-Seiten, die eine Customer Voice-Umfrage enthalten sollen, müssen Sie als Nächstes den externen Stylesheet-Code einbetten, den Customer Voice im Einbettungscode bereitgestellt hat. Wie im vorherigen Abschnitt besteht die beste Methode zum Einbetten des externen Stylesheet-Codes darin, im Site Builder ein Fragment zu erstellen, das den Stylesheet-Code enthält, und das Fragment dann den entsprechenden Seitenvorlagen hinzuzufügen. Der eingebettete externe Stylesheet-Code ähnelt dem folgenden Beispielcode.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Führen Sie die folgenden Schritte aus, um den externen Stylesheet-Code in ein Fragment einzubetten.

1. Erstellen Sie im Site Builder ein Fragment, das auf dem [Metatags-Modul](metatags-module.md) basiert.
1. Wählen Sie im Fragment den Platz **Standard-Metatags** aus.
1. Geben Sie in dem **Standard-Metatags**-Eigenschaftenbereich im Feld **Metatags** wie in der folgenden Beispielabbildung gezeigt den Stylesheet-Code ein.

    ![Externer Stylesheet-Code im Metatags-Feld für das neue Fragment.](media/customer-voice-integration-3.png)

1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen**, um das Fragment zu veröffentlichen.

Das neue Fragment, das den eingebetteten externen Stylesheet-Code enthält, kann jetzt der entsprechenden Seitenvorlage hinzugefügt werden.

### <a name="embed-the-inline-script-code"></a>Den Inline-Skriptcode einbetten 

Auf allen Website-Seiten, die eine Customer Voice-Umfrage enthalten sollen, müssen Sie als Nächstes den Inline-Skriptcode einbetten, den Customer Voice im Einbettungscode bereitgestellt hat. Wie in den vorherigen Abschnitten, besteht die beste Methode zum Einbetten des Inline-Skriptcodes darin, im Site Builder ein Fragment zu erstellen, das den Inline-Skriptcode enthält, und das Fragment dann den entsprechenden Seitenvorlagen hinzuzufügen.

Im folgenden Beispiel für Inline-Skriptcode ist **SURVEY\_KEY** ein Platzhalter. Der Wert für **SURVEY\_KEY** sollte mit dem tatsächlichen Umfrageschlüssel übereinstimmen, den Customer Voice im Einbettungscode bereitgestellt hat. Die letzte Zeile ruft den Code zum Rendern der Umfrageschaltfläche nach einer Sekunde auf, um sicherzustellen, dass die Skripte genügend Zeit zum Laden haben. Je nach ausgewählter Umfrage müssen Sie möglicherweise auch andere Metadaten hinzufügen oder aktualisieren, z. B. den Firmennamen.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Führen Sie die folgenden Schritte aus, um den Inline-Skriptcode in ein Fragment einzubetten.

1. Erstellen Sie im Site Builder ein Fragment, das auf dem [Inline-Skript-Modul](script-module.md) basiert.
1. Wählen Sie im neuen Fragment den Platz **Standard-Inline-Skript** aus.
1. Geben Sie in dem **Standard-Inline-Skript**-Eigenschaftenbereich im Feld **Inline-Skript** wie in der folgenden Beispielabbildung gezeigt die URL des Inline-Skriptcodes ein.

    ![Inline-Skriptcode im Inline-Skript-Feld für das neue Fragment.](media/customer-voice-integration-4.png)

1. Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.
1. Wählen Sie **Veröffentlichen**, um das Fragment zu veröffentlichen.

Das neue Fragment, das den eingebetteten Inline-Skriptcode enthält, kann jetzt der entsprechenden Seitenvorlage hinzugefügt werden.

## <a name="add-fragments-to-a-template"></a>Einer Vorlage ein Fragment hinzufügen

Wenn Sie mit dem Erstellen der Fragmente fertig sind, die den eingebetteten Code von Customer Voice enthalten, müssen Sie sie zu den Seitenvorlagen hinzufügen, die den Website-Seiten zugeordnet sind, auf denen Sie sie verwenden möchten. In der folgenden Beispielabbildung wurden die drei Beispielfragmente einer Vorlage für Produktdetailseiten (PDP) hinzugefügt.

![Beispielfragmente, die einer PDP-Vorlage hinzugefügt wurden.](media/customer-voice-integration-5.png)

Nachdem die aktualisierte Vorlage veröffentlicht wurde, wird die Customer Voice-Umfrage auf allen Seiten angezeigt, die von der Vorlage gesteuert werden.

Informationen zu Vorlagen erhalten Sie unter [Arbeiten mit Vorlagen](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Inhaltssicherheitsrichtlinie konfigurieren

Standardmäßig lässt die Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) keine Aufrufe anderer Dienste zu, es sei denn, es wird eine zusätzliche Konfiguration vorgenommen. Daher ist es nach dem Veröffentlichen der aktualisierten Vorlagen wahrscheinlich, dass die Umfrage nicht auf den entsprechenden Seiten der Website geladen werden kann. Um die CSP-bezogenen Fehler anzuzeigen, öffnen Sie die Entwicklertools Ihres Webbrowsers (F12), und gehen Sie dann zu einer Seite mit der Umfrage. Die CSP-bezogenen Fehler werden in der Konsolenausgabe angezeigt.

Führen Sie die folgenden Schritte aus, um CSP im Website-Generator zu konfigurieren, damit die Fehler behoben werden.

1. Gehen Sie zu **Site-Einstellungen \> Erweiterungen**.
1. Fügen Sie auf der **Inhaltssicherheitsrichtlinie**-Registerkarte `https://customervoice.microsoft.com/` der **child-src**-Richtlinie hinzu.
1. Fügen Sie `https://customervoice.microsoft.com/` zur **frame-src**-Richtlinie hinzu.
1. Fügen Sie `https://mfpembedcdnmsit.azureedge.net` und **.azureedge.net** der **img-src**-Richtlinie hinzu.

Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie](manage-csp.md).

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Externes Skript-Modul](script-module.md)

[Metatags-Modul](metatags-module.md)

[Inline-Skript-Modul](script-module.md)

[Inhaltssicherheitsrichtlinie](manage-csp.md)

[Arbeiten mit Fragmenten](work-with-fragments.md)

[Arbeiten mit Vorlagen](work-with-templates.md)
