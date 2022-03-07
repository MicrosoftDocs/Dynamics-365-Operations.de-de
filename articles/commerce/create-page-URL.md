---
title: Erstellen einer Seiten-URL
description: In diesem Thema werden grundlegende Konzepte und Verfahren zum Erstellen einer Seiten-URL auf Ihrer Site behandelt.
author: bicyclingfool
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 923723ce6e3f92c5186cd8a562a6e3fee3fdf70dfe8db29c86192cb1db515b1a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717722"
---
# <a name="create-a-page-url"></a>Erstellen einer Seiten-URL

[!include [banner](includes/banner.md)]

In diesem Thema werden grundlegende Konzepte und Verfahren zum Erstellen einer Seiten-URL auf Ihrer Site behandelt.

Der vollständige oder absolute URL die auf eine Seite auf Ihrer Site verweist, besteht aus eindeutigen Teilen. Zum Beispiel verfügt die URL `https://www.contoso.com/en-us/contactus` über folgende Bereiche:

- `https://www.contoso.com` – Das HTTP-Protokoll und die Domäne des Standorts.
- `/en-us` – Der Sprachenpfad der Site.
- `/contactus` – Die relative URL für die Seite **Kontaktieren Sie uns**. Eine relative URL ist auch als ein URL *Titel* bekannt.

Sie richten die Domäne Ihrer Site und den optionalen Sprachenpfad ein, wenn Sie die Site einrichten. Sie können mehrere Domänen und Sprachenpfade Ihrer Site über die Onlineshopseite in den Einstellungen der Site hinzufügen.

Der URL-Titel für eine Seite ist als eigenständige Entität in der Siteerstellungsumgebung vorhanden. Eine Seiten-URL besteht aus zwei Teilen: ein Name, der den URL-Titel darstellt und eine Verknüpfung zu einer Seite, entweder zu Ihrer Site oder einer externen Site. Eine Seiten-URL kann auch so konfiguriert werden, dass sie als Umleitung zu einer anderen Seite entweder auf Ihre Site oder eine externe Site zu dienen.

## <a name="create-a-page-url"></a>Erstellen einer Seiten-URL

Es gibt zwei Möglichkeiten, Seiten-URLs zu erstellen:

- Automatisch wenn Sie eine Seite erstellen
- Manuell von den Seiten-**URLs**

### <a name="create-a-page-url-when-you-create-a-page"></a>Hier können Sie eine Seiten-URL erstellen, wenn Sie eine Seite erstellen

Wenn Sie einen Namen im Feld **URL** angeben, wenn Sie eine neue Seite erstellen, wird eine Seiten-URL, die auf diese Seite verweist, automatisch auf den Seiten **URLs** erstellt. Nachdem Sie die URL und die Seite veröffentlicht haben, auf die verwiesen wird, können Site-Benutzer (Ihre Debitoren) auf die Seite zugreifen, die mit der URL verknüpft ist.

> [!NOTE]
> Wenn Sie eine URL veröffentlichen, ohne die Seite zu veröffentlichen, auf die verwiesen wird, erhalten Sitebenutzer einen Fehlercode 404, wenn Sie versuchen, die Seite zu öffnen. Wenn Sie eine Seite veröffentlichen, ohne die URL zu veröffentlichen, die darauf verweist, kann nicht auf die Seite nicht mithilfe der URL zugegriffen werden.

### <a name="manually-create-a-page-url"></a>Manuell eine Seiten-URL erstellen

Wenn Sie neue Seiten erstellen, müssen Sie keine Seiten-URL definieren. Wenn Sie das URL Feld leer lassen, wird die Seite in einem nicht verknüpften Status erstellt. In diesem Fall sind Debitoren nicht in der Lage, auf die Seite zuzugreifen, selbst wenn sie veröffentlicht wurde. Um die Seite verfügbar zu machen, müssen Sie die URL manuell erstellen und diese mit der Seite verknüpfen.

Um die Seiten-URL manuell für eine Seite zu erstellen, führen Sie die folgenden Schritte aus.

1. Wählen Sie auf der Seite **URL** die Option **Neu** aus.
1. Wählen Sie die Siteseite, die mit der URL verknüpft werden soll.
1. Geben Sie den URL-Titel ein und wählen Sie dann **OK** aus.

An diesem Punkt ist die URL in einem Entwurfzustand. Sie muss veröffentlicht werden, bevor der Sitebenutzer auf die verknüpfte Seite zugreifen kann.

## <a name="update-a-page-url"></a>Seiten-URL aktualisieren

Um die Zielseite einer Seiten-URL zu aktualisieren, führen Sie die folgenden Schritte aus.

1. Wählen Sie auf der Seite **URLs** die URL aus, um sie zu aktualisieren.
1. Im Eigenschaftenbereich auf der rechten Seite klicken Sie auf die Ellipsen.Schaltfläche (**…**) neben dem Zielseitenfeld.
1. Wählen Sie im Dialogfeld eine andere Seite wählen dann **OK**.
1. URL speichern und veröffentlichen.

## <a name="redirect-a-page-url"></a>Seiten-URL umleiten

Manchmal möchten Sie, dass Ihre Debitoren eine andere Seite angezeigt erhalten, wenn sie eine bestimmte URL anfordern. In diesen Fällen ist der beste und einfachste Ansatz häufig, die Seite zu ändern, auf die die Seiten-URL verweist. Aber möglicherweise haben Sie bereichtigte Gründe, HTTP 301 oder 3023 zu verwenden, um die Anfrage für eine URL auf eine andere URL weiterzuleiten.

Um eine URL zu einer anderen URL weiterzuleiten, folgen Sie diesen Schritten.

1. Wählen Sie auf der Seite **URLs** die URL aus, um sie zu aktualisieren.
1. Wählen Sie im Eigenschaftenbereich rechts die Eigenschaft **Umleitung** aus.
1. Wählen Sie ein Ziel für die Umleitung aus

    - Um auf eine andere Seite auf Ihrer Site zu verweisen, wählen Sie **Interne URL**, wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie anschließend die URL für die Umleitung.
    - Um auf eine Seite auf einer externen Site zu verweisen, wählen Sie **Externe URL** und geben Sie dann die vollständige URL für diese Seite ein. Achten Sie darauf, dass das Protokoll miteinbezogen wird. Geben Sie beispielsweise `https://domain.com/new/page` ein. Wenn die URL bereits auf eine interne URL umleitet, müssen Sie **Auswahl löschen** auswählen, bevor Sie eine externe URL eingeben können.

1. Wählen Sie einen Umleitungstyp aus.

    - **Permanente Umleitung (301)** – Wählen Sie diese Option aus, wenn Sie wissen, dass Ihr Inhalt dauerhaft verschoben wird und nicht zur vorherigen URL zurückkommt. Suchmodule weisen den Suchmaschinen-Optimierungs (SEO)- Wert der umleitenden URL zu der URL zu, die umgeleitet wird und aktualisiert den Datensatz, um die neue URL anzuzeigen. 
    - **Temporäre Umleitung (302)** – Wählen Sie diese Option aus, um den Verkehr umzuleiten, ohne die Suchmodule zu aktualisieren. Dieser Ansatz wird normalerweise verwendet, wenn der Inhalt bald zur vorherigen URL zurückkehrt.

1. Wenn Sie bereit sind, die Umleitung zu implementieren, speichern und veröffentlichen Sie die URL.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Anpassen der Sitenavigation](customize-site-navigation.md)

[Neue Seite hinzufügen](add-new-page.md)

[Konfigurieren Ihres Domänennamens](configure-your-domain-name.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
