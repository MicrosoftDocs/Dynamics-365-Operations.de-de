---
title: IFrame-Modul
description: Dieses Thema behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665395"
---
# <a name="iframe-module"></a>IFrame-Modul

[!include [banner](includes/banner.md)]

Dieses Thema behandelt das iFrame-Modul und beschreibt, wie es Webseiten in Microsoft Dynamics 365 Commerce hinzugefügt wird.

## <a name="overview"></a>Übersicht

Ein iFrame-Modul stellt einen iFrame (Inlineframe) bereit, der externe Inhalte auf einer Website hostet. Zum Beispiel kann es verwendet werden, um auf einer Webseite ein YouTube-Video oder einen PDF-Datei-Viewer zu hosten. 

Ein iFrame-Modul benötigt eine Ziel-URL. Anschließend wird der Inhalt der Zielseite in einem HTML-**iFrame**-Element gehostet. Externe URLs müssen auf der Zulassungsliste gemäß der Inhaltssicherheitsrichtlinie (CPS) der Website stehen. Für iFrame-Inhalte sollten URLs mithilfe der **frame-ancester**-Richtlinie zugelassen werden. Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie (CSP) verwalten](manage-csp.md).

> [!NOTE]
> Das iFrame-Modul ist in der Dynamics 365 Commerce-Version 10.0.13 verfügbar.

Das folgende Bild zeigt Beispiele für iFrame-Module, die externe Videos auf Webseiten zeigen.

![Beispiel für iFrame-Module, die externe Videos zeigen](./media/ecommerce-iframe.PNG)

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
1. In dem Dialogfeld **Wählen Sie eine Vorlage** wählen Sie die Vorlage **Marketingvorlage** aus. Gehen Sie unter **Seitenname** **Marketingseite** ein und wählen Sie dann **OK**.
1. Auf der neuen Seite wählen Sie **Haupt**-Slot und wählen dann die Ellipsen (**...**) und wählen **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.
1. Legen Sie im Eigenschaftsbereich des Moduls den **Breite**-Wert auf **Container füllen** fest.
1. Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.
1. Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **iFrame** und dann **OK** aus.
1. Legen Sie im Eigenschaftenbereich des Moduls den Wert der **Ziel-URL** auf eine externe URL für ein Video fest.
1. Legen Sie weitere benötigte Eigenschaften fest, wie **Überschrift** und **Höhe**.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.
1. Gehen Sie zur Marketingseite Ihrer Website. Sie sollten sehen, dass das Video im iFrame-Modul gerendert wird.
 
## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Übersicht über die Modulbibliothek](starter-kit-overview.md)

[Inhaltssicherheitsrichtlinie (Content Security Policy, CSP) verwalten](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]