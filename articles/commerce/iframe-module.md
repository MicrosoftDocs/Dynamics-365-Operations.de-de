---
title: Iframe-Modul
description: Dieser Artikel behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e9f1804cde1010c585d53d63bc0a487bc5407552
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858936"
---
# <a name="iframe-module"></a>Iframe-Modul

[!include [banner](includes/banner.md)]

Dieser Artikel behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.

Ein iFrame-Modul stellt einen iFrame (Inlineframe) bereit, der externe Inhalte auf einer Website hostet. Zum Beispiel kann es verwendet werden, um auf einer Webseite ein YouTube-Video oder einen PDF-Datei-Viewer zu hosten. 

Ein iFrame-Modul benötigt eine Ziel-URL. Anschließend wird der Inhalt der Zielseite in einem HTML-**iFrame**-Element gehostet. Externe URLs müssen auf der Zulassungsliste gemäß der Inhaltssicherheitsrichtlinie (CPS) der Website stehen. Für iFrame-Inhalte sollten URLs mithilfe der **frame-ancester**-Richtlinie zugelassen werden. Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie (CSP) verwalten](manage-csp.md).

> [!NOTE]
> Das iFrame-Modul ist in der Dynamics 365 Commerce-Version 10.0.13 verfügbar.

Das folgende Bild zeigt Beispiele für iFrame-Module, die externe Videos auf Webseiten zeigen.

![Beispiel für iFrame-Module, die externe Videos zeigen.](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Hinzufügen von iFrame-Eigenschaften

| Eigenschaftenname             | Wert                 | Beschreibung |
|---------------------------|-----------------------|-------------|
| Überschrift | Text | Die Überschrift für das Modul. |
| Ziel-URL | URL | Die URL, die im Modul gehostet wird. |
| Höhe | Anzahl oder Prozentsatz | Die Höhe des Moduls, in Pixeln oder Prozent. Zum Beispiel wird der Wert **100** als Anzahl von Pixeln und der Wert **100 %** als Prozentsatz behandelt. |
| Aria-Label | Text | Aus Gründen der Barrierefreiheit kann ein Label von „Accessible Rich Internet Applications“ (ARIA) festgelegt werden. |

## <a name="add-an-iframe-module-to-a-page"></a>Ein iFrame-Modul einer Seite hinzufügen

Gehen Sie wie folgt vor, um einer Seite ein iFrame-Modul hinzuzufügen und ein externes Video anzuzeigen.

1. Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.
1. Im Dialogfeld **Neue Vorlage** geben Sie unter **Vorlagenname** **Containervorlage** ein und wählen Sie **OK**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.
1. Im Dialogfeld **Neue Seite erstellen** unter **Seitenname** geben Sie **Marketing-Seite** ein und wählen **Weiter**.
1. Unter **Vorlage auswählen** wähle Sie die **Marketing-Vorlage** aus, die Sie erstellt haben, und Sie wählen dann **Weiter**.
1. Wählen Sie unter **Wählen Sie ein Layout** ein Seitenlayout (z.B. **Flexibles Layout**) und wählen Sie dann **Weiter**.
1. Unter **Prüfen und beenden** überprüfen Sie die Konfiguration der Seite. Wenn Sie die Seiteninformationen bearbeiten müssen, wählen Sie **Zurück**. Wenn die Seiteninformationen korrekt sind, wählen Sie **Seite erstellen**. 
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **Container** und dann **OK** aus.
1. Legen Sie im Eigenschaftsbereich des Moduls den **Breite**-Wert auf **Container füllen** fest.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Module auswählen** das Modul **iframe** und dann **OK** aus.
1. Legen Sie im Eigenschaftenbereich des Moduls den Wert der **Ziel-URL** auf eine externe URL für ein Video fest.
1. Legen Sie weitere benötigte Eigenschaften fest, wie **Überschrift** und **Höhe**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zur Marketingseite Ihrer Website. Sie sollten sehen, dass das Video im iFrame-Modul gerendert wird.

> [!NOTE]
> Da das iFrame-Modul externe Inhalte hostet, müssen Site-Autoren sicherstellen, dass die in einem iFrame-Modul gehosteten Inhalte nicht gegen die Richtlinien zur Inhaltseinschränkung des jeweiligen Marktes verstoßen. Wenn auf einer Seite, die das iFrame-Modul verwendet, eine Verletzung der Inhaltsrichtlinien vorliegt, kann der Site-Autor das iFrame-Modul entfernen, indem er die Seite im Site-Builder öffnet und **Modul entfernen** im iFrame-Modulsteckplatz auswählt, speichern Sie die Seite und veröffentlichen Sie sie erneut.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Informationen zur Modulbibliothek](starter-kit-overview.md)

[Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) verwalten](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
