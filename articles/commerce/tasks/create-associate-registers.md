---
title: " Register erstellen und zuordnen"
description: Diese Prozedur zeigt, wie ein Verkaufsstellen-(POS)-Register erstellt wird.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 001bdd61f9266798dadae2ac7c96a4f4c19dbb94
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141452"
---
# <a name="create-and-associate-registers"></a> Register erstellen und zuordnen

[!include [banner](../includes/banner.md)]

Diese Prozedur zeigt, wie ein Verkaufsstellen-(POS)-Register erstellt wird. Für diese Prozedur wird das Demo-Datenunternehmen USRT verwendet.

1. Wechseln Sie zu Retail und Commerce > Kanaleinstellungen > POS-Einstellungen > Register.
2. Klicken Sie auf Neu.
3. Geben Sie im Feld "Registernummer" eine Kennung für ein neues Register ein.
    * Die Registerkennung umfasst gewöhnlich Codes, die helfen, das Register dem Lager zuzuordnen, zu dem es gehört, sowie zum Lagerplatz innerhalb des Lagers.  
4. Geben Sie im Feld "Name" einen aussagekräftigen Namen für das Register ein.
5. Geben Sie im Feld "Lagernummer" einen Wert ein oder wählen Sie einen Wert aus.
6. Geben Sie im Feld "Hardwareprofil" einen Wert ein, oder wählen Sie einen Wert aus.
    * Hardwareprofile werden zur Angabe der Peripheriegeräte verwendet, die an die Registrierkasse angeschlossen werden, wie z.B. Kassenlade und Bondrucker.  
7. Geben Sie im Feld "Visuelles Profil" einen Wert ein oder wählen Sie einen Wert aus.
    * Visuelle Profile werden verwendet, um die Bilder anzugeben, die im POS-Hintergrund und auf der Anmeldeseite sowie als Themen für das POS verwendet werden.  
8. Geben Sie im Feld "POS-Registernummer für elektronische Überweisung" einen Wert ein.
    * Die POS-Registernummer für elektronische Überweisungen wird verwendet, um den Zahlungsprozessor darüber zu informieren, welches Zahlungsterminal Autorisierungsanforderungen sendet. Dieser Wert wird häufig als „Terminalkennung“ oder „TID“ bezeichnet. Die TID kann allgemein auf einem Aufkleber auf dem Zahlungsgerät gefunden werden.  
9. Klicken Sie auf "Speichern".
