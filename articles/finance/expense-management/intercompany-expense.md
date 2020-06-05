---
title: Intercompany-Ausgaben
description: Eine Arbeitskraft, die von einer juristischen Personen in einer Organisation beschäftigt wird, kann möglicherweise Arbeit für eine andere juristische Person in derselben Organisation ausführen. In diesem Fall können Sie die Intercompany-Ausgabenfunktion verwenden, um die Ausgaben der Arbeitskraft der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390883"
---
# <a name="intercompany-expenses"></a>Intercompany-Ausgaben

[!include [banner](../includes/banner.md)]

Eine Arbeitskraft, die von einer juristischen Personen in einer Organisation beschäftigt wird, kann möglicherweise Arbeit für eine andere juristische Person in derselben Organisation ausführen. In diesem Fall können Sie die Intercompany-Ausgabenfunktion verwenden, um die Ausgaben der Arbeitskraft der juristischen Person zuzuweisen, für die die Arbeit ausgeführt wurde. Die juristische Person, die die Arbeitskraft verwendet, wird als verleihende juristische Person bezeichnet. Die juristische Person, für die die Arbeitskraft Ausgaben verursacht, wird als ausleihende juristische Person bezeichnet. 

Bevor eine Arbeitskraft Ausgaben für die Arbeit erstellen und übermitteln kann, die für eine andere juristische Person ausgeführt wurde, wählen Sie in der verleihenden juristischen Person auf der Seite **Ausgabenverwaltungsparameter** die Option **Intercompany-Ausgabenpositionen zulassen** aus. 

## <a name="tax-posting-for-intercompany-expenses"></a>Steuerbuchung für Intercompany-Ausgaben

[!include [banner](../includes/banner.md)]

Wenn Sie in Ihrer Spesenabrechnung Steuergruppen verwenden möchten, die der verleihenden juristischen Person (Quelle) anstelle der ausleihenden juristischen Person (Ziel) zugeordnet sind, müssen Sie dies in der eingerichteten Mehrwertsteuer des Hauptbuchs konfigurieren. Wenn der Hauptbuchparameter **Juristische Person für Intercompany-Steuerbuchung** auf **Quelle** und **Mehrwertsteuerregeln anwenden** auf **Nein** festgelegt ist, wird die Steuerkombination für die verleihende juristische Person verwendet. Wenn derselbe Parameter auf **Ziel** festgelegt ist, wird die Steuerkombination für die ausleihende juristische Person verwendet. Für juristische Personen in den USA muss das Feld **Vorsteuer** auch auf der neuen Seite **Sachkontobuchungsgruppen** konfiguriert werden, wenn der Parameter auf **Quelle** festgelegt ist. Die Buchhaltungs-Engine verwendet die Informationen aus diesem Feld für steuerbezogene Buchhaltungseinträge.   
Das Verhalten ist für Ausgabenpositionen, die mit oder ohne Projekt gebucht wurden, konsistent.  
