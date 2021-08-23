---
title: Hinzufügen einer Begrüßungsnachricht
description: In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce-Website hinzugefügt wird.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d6c4f1746dc0e5f3e6525f36979e33a4ebd0180fa1e52ec011a8c1cfa69565c3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725361"
---
# <a name="add-a-welcome-message"></a>Hinzufügen einer Begrüßungsnachricht

[!include [banner](includes/banner.md)]

In diesem Thema wird beschrieben, wie eine Begrüßungsmeldung Ihrer Microsoft Dynamics 365 Commerce-Website hinzugefügt wird.

Eine Begrüßungsmeldung auf der E-Commerce-Website kann Besucher über laufende Verkäufe, Siteaktualisierungen oder verfügbaren saisonale Sammlungen informieren. Die Begrüßungsmeldung wird festgelegt, indem das Warnungsmodul verwendet wird.

Das allgemeine Modul muss den **Fehler-/Informationensnachrichten** Slots des Kopffragments hinzugefügt werden. Mit dem Warnungsmodul können Sie den Text definieren, der angezeigt wird, die Textfarbe und die Ausrichtung. Es kann auch angeben, ob Besucher der Site die Nachricht ablehnen können.

Wenn eine Begrüßungsmeldung einem freigegebenen Kopffragment hinzugefügt wird, wir dieses für jede Seite angezeigt, die die Vorlage verwendet, in dem das freigegebene Kopffragment verwendet wird.

Um eine Begrüßungsmeldung der Site hinzufügen, führen Sie die folgenden Schritte aus.

1. Navigieren Sie im Commerce Site Builder zu Ihrer Site.
1. Wählen Sie **Fragmente**.
1. Wählen Sie das Kopffragment aus, um die Nachricht hinzuzufügen.
1. In der Gliederungsstruktur erweitern Sie **Fehler-/Informationensnachrichten**
1. Wählen Sie das Warnungsmodul aus und wählen Sie dann **OK** aus. Wenn ein Warnungsmodul noch nicht vorhanden ist, wählen Sie zunächst die Ellipsen-Schaltfläche (**...**) neben der **Fehler-/Informationensnachricht** aus, und wählen Sie dann **Fügen Sie Modul hinzu** aus.
1. Im Eigenschaftenbereich auf der rechten Seite auf der Registerkarte **Daten** wählen Sie **Fügen Sie Datenquelle hinzu** und **Inhalt** aus.
1. Im Feld **Geben Sie Text ein** geben Sie den Text der Begrüßungsmeldung ein.
1. Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Kopffragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen. 

Die Begrüßungsmeldung wird nun oben auf jeder Standortsseite angezeigt, das das ausgewählte Kopffragment verwendet.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Hinzufügen eines Logos](add-logo.md)

[Auswählen eines Sitedesigns](select-site-theme.md)

[Arbeiten mit CSS-Überschreibungsdateien](css-override-files.md)

[Hinzufügen eines Favicons](add-favicon.md)

[Hinzufügen eines Urheberrechtshinweises](add-copyright-notice.md)

[Hinzufügen von Sprachen zu Ihrer Website](add-languages-to-site.md)

[Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
