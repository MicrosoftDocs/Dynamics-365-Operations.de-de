---
title: "Finance and Operations-Client – FAQ"
description: "Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Microsoft Dynamics 365 for Finance and Operations-Client."
author: jasongre
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 658d5a1a031f2292dbd445fa7fb345be01c61947
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="finance-and-operations-client-faq"></a>Finance and Operations-Client – FAQ

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Microsoft Dynamics 365 for Finance and Operations-Client.

<a name="why-arent-symbols-loaded-when-i-use-finance-and-operations"></a>Warum werden Symbole nicht geladen, wenn ich Dynamics 365 for Finance and Operations verwende?
-----------------------------------------------------------------

Die Sicherheitseinstellungen in Ihrem Browser verhinderten möglicherweise, das die Symbole ordnungsgemäß geladen werden. Zur Behebung dieses Problems wird Folgendes empfohlen:

-   Falls dieses Problem in Internet Explorer ermitteln, klicken Sie **Tools**, und klicken Sie dann **Internetoptione**.  Im Internetoptionsdialogfeld **Datenschutz** auf der Registerkarte, klicken Sie **Benutzerdefinierte  Ebene** an, und vergewissern Sie sich, dass die **Schriftartdownload** Option ausgewählt wird.
-   Andernfalls müssen Sie möglicherweise die Finance and Operations-Website der Liste der vertrauenswürdigen Standorte hinzufügen.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Ich vermisse das Menüband von Microsoft Dynamics AX 2012. Kann ich Registerkarten ständig offen anhalten?
Wir planen, diese Funktion bald zu implementieren. Die Benutzer können dann angeben, ob die Registerkarten im Aktivitätsbereichen ständig offen sein soll. Andernfalls werden die Registerkarten reduziert wenn sie nicht verwendet werden, um mehr Platz für die Seite zu erhalten.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Warum sehe ich manchmal andere Kontextmenüs, wenn mit rechts klicke?
Wenn Sie mit rechts auf ein bearbeitbares Feld klicken, oder wenn Text markiert ist, wird das Kontextmenü des Browsers angezeigt. Dieses Menü ermöglicht das **Ausschneiden**, **Kopieren** und **Einfügen**. Wir können diese Befehle nicht in die Kontextmenüs von Finance and Operations einbetten, da Browser aus Sicherheitsgründen den programmgesteuerten Zugriff auf die Systemzwischenablage nicht gestatten.

Wenn Sie mit rechts auf eine Feldbezeichnung oder auf den Wert eines schreibgeschützten Steuerelements klicken, erhalten Sie das Finance and Operations-Kontextmenü.

Um den Tastaturzugriff zu vereinfachen, planen wir eine Tastenkombination zu implementieren, die das Kontextmenü von Finance and Operations öffnet.

## <a name="where-is-the-view-details-functionality-in-finance-and-operations"></a>Wo ist in Finance and Operations die "Details anzeigen"-Funktion?
Die **Details anzeigen**-Option ist auf mehrere Arten verfügbar:

-   Wenn ein Steuerelemente die Funktionen **Details anzeigen** hat, und wenn das Steuerelement einen Wert enthält, dann wird der Wert als Link angezeigt. Sie können auf die Verknüpfung klicken, um die Seite zu öffnen, die zusätzliche Details enthält.
-   **Details anzeigen** ist außerdem eine Option in den Kontextmenüs von Finance and Operations. Weitere Informationen zur Anzeige von Finance and Operations-Kontextmenü beim Rechtsklick finden Sie im vorherigen Abschnitt.





