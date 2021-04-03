---
title: Kunden-FAQs
description: Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Finance and Operations-Client.
author: jasongre
manager: AnnBe
ms.date: 09/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 12334
ms.assetid: a9a57f0e-a67c-46b1-83c9-5d6350fb3b86
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a7d311bfcd65e23e4062f105435d05cb1ceda6b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567039"
---
# <a name="client-faq"></a>Kunden-FAQ

[!include [banner](../includes/banner.md)]

Dieser Artikel enthält Antworten auf häufig gestellte Fragen zum Finance and Operations-Client.

## <a name="why-arent-symbols-loaded"></a>Warum werden keine Symbole geladen?

Die Sicherheitseinstellungen in Ihrem Browser verhinderten möglicherweise, das die Symbole ordnungsgemäß geladen werden. Zur Behebung dieses Problems wird Folgendes empfohlen:

- Falls dieses Problem in Internet Explorer auftritt, klicken Sie auf **Tools**, und klicken Sie dann auf **Internetoptionen**. Im Internetoptionsdialogfeld **Datenschutz** auf der Registerkarte, klicken Sie **Benutzerdefinierte  Ebene** an, und vergewissern Sie sich, dass die **Schriftartdownload** Option ausgewählt wird.
- Andernfalls müssen Sie möglicherweise die App-Website der Liste der vertrauenswürdigen Standorte hinzufügen.

## <a name="i-miss-the-ribbon-from-dynamics-ax-2012-can-i-keep-action-pane-tabs-open-all-the-time"></a>Ich vermisse das Menüband von Dynamics AX 2012. Kann ich Registerkarten ständig offen anhalten?

Wir planen, diese Funktion bald zu implementieren. Die Benutzer können dann angeben, ob die Registerkarten im Aktivitätsbereichen ständig offen sein soll. Andernfalls werden die Registerkarten reduziert wenn sie nicht verwendet werden, um mehr Platz für die Seite zu erhalten.

## <a name="why-do-i-sometimes-see-different-shortcut-menus-when-i-right-click"></a>Warum sehe ich manchmal andere Kontextmenüs, wenn mit rechts klicke?

Wenn Sie mit rechts auf ein bearbeitbares Feld klicken, oder wenn Text markiert ist, wird das Kontextmenü des Browsers angezeigt. Dieses Menü ermöglicht das **Ausschneiden**, **Kopieren** und **Einfügen**. Wir können diese Befehle aus Sicherheitsgründen nicht in die Kontextmenüs einbetten, da die Browser den programmgesteuerten Zugriff auf die Systemzwischenablage nicht gestatten.

Wenn Sie mit der rechten Maustaste auf eine Feldbezeichnung oder auf den Wert eines schreibgeschützten Steuerelements klicken, erhalten Sie das Kontextmenü.

Um den Tastaturzugriff zu vereinfachen, planen wir, eine Tastenkombination zu implementieren, die das Kontextmenü öffnet.

## <a name="where-is-the-view-details-functionality"></a>Wo ist die Funktion „Details anzeigen”?

Die **Details anzeigen**-Option ist auf mehrere Arten verfügbar:

- Wenn ein Steuerelemente die Funktionen **Details anzeigen** hat, und wenn das Steuerelement einen Wert enthält, dann wird der Wert als Link angezeigt. Sie können auf die Verknüpfung klicken, um die Seite zu öffnen, die zusätzliche Details enthält.
- **Details anzeigen** ist außerdem eine Option in den Kontextmenüs. Weitere Informationen zur Anzeige von Kontextmenüs, die beim Rechtsklick angezeigt werden, finden Sie im vorherigen Abschnitt.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]