---
title: Leasinggenehmigungs-Workflows verwenden
description: In diesem Thema wird erläutert, wie Sie mithilfe von Workflows Analgenleasings genehmigen und den Status und den Verlauf der Workflows verfolgen.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0b35dfa599895cb39cdd6a0a95fdcdcc54c45044
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724924"
---
# <a name="use-lease-approval-workflows"></a>Leasinggenehmigungs-Workflows verwenden

[!include [banner](../includes/banner.md)]

In diesem Thema wird erläutert, wie Sie mithilfe von Workflows Analgenleasings genehmigen und den Status und den Verlauf der Workflows verfolgen. Workflows tragen zur Konsistenz der Verwaltung von Leasinggenehmigungen bei, indem sie einen Standardsatz von Genehmigungsschritten bereitstellen und bestimmte Benutzer zuweisen, die jeden Schritt des Prozesses genehmigen. Eine genehmigende Person kann einen Mietvertrag genehmigen, ablehnen, eine Änderung anfordern oder ihn einem anderen Benutzer zur Genehmigung zuweisen. Workflows können auch mehr Transparenz in den Genehmigungsprozess bringen, indem Sie deren Status und Verlauf verfolgen können. Darüber hinaus können Sie eine zentrale Arbeitsliste anzeigen, in der die Aufgaben und Genehmigungen aufgeführt sind, die bestimmten genehmigenden Personen zugewiesen sind.

Stellen Sie vor Verwendung dieses Verfahrens sicher, dass mindestens ein Workflow für die Genehmigung von Mietverträgen erstellt wurde. Wenn kein Workflow vorhanden ist, erstellen Sie einen. Informationen zum Einrichten eines Workflows finden Sie unter [Einrichten von Workflows für die Leasinggenehmigung](set-up-lease-wrkflw.md).

1. Übermitteln Sie einen Mietvertrag zur Genehmigung. Wählen Sie auf der **Buchdetails**-Seite für den Mietvertrag **Workflow** und dann **Senden** aus.
2. Im angezeigten Dialogfeld können Sie einen Kommentar hinzufügen. Die benannte genehmigende Person sieht diesen Kommentar zusammen mit dem Mietvertrag. Wenn Sie den Kommentar eingegeben haben, wählen Sie **Senden**. Der Mietvertrag wird an das Workflow-System gesendet und vom die genehmigende Person erhält ihn zur Genehmigung.
3. Um die Mietverträge anzuzeigen, für deren Genehmigung sie bestimmt sind, gehen Sie zu **Module \> Allgemein \> Arbeitsaufgaben \> Mir zugewiesene Arbeitsaufgaben**.
4. Auf der **Mir zugewiesene Arbeitsaufgaben**-Seite wählen Sie den **Leasing-ID**-Link für den Mietvertrag, den Sie anzeigen möchten. Die angezeigte Seite hängt von den Leasingbüchern und Details zum Mietvertrag ab, auf die Sie Zugriff haben.
5. Wenn Sie den Mietvertrag angezeigt haben, wählen Sie **Workflow** und entscheiden Sie, welche Maßnahmen ergriffen werden sollen. Die Optionen umfassen **Genehmigen**, **Abgelehnt**, **Änderung anfordern**, **Delegieren** und **Abgebrochen**. Sie können auch **Verlauf anzeigen** auswählen, um den Genehmigungsverlauf für den ausgewählten Mietvertrag anzuzeigen.
6. Nachdem Sie eine Aktion ausgewählt haben, geben Sie einen Kommentar ein, um die Aktion zu beschreiben. Wenn Sie den Kommentar eingegeben haben, wählen Sie die **Genehmigt**-Aktion in der Liste.
7. Um die Genehmigungsaktionen anzuzeigen, kehren Sie zur **Details zum Mietvertrag**-Seite von der **Mietvertragsübersicht**-Seite zurück und wählen Sie dann **Workflow \> Verlauf anzeigen** aus.

    Sie können die Workflow-Aktivitäten auf der **Workflow-Verlauf**-Seite anzeigen. Diese Seite zeigt die Workflow-Schritte, die für den jeweiligen Mietvertrag ausgeführt wurden. Sie können auch das **Arbeitsaufgaben**-Feld verwenden, um den Status der zugewiesenen Arbeitsaufgaben anzuzeigen.

8. Um einen Workflow zu stoppen, klicken Sie auf der **Workflow-Verlauf**-Seite auf **Zurückrufen**. Wählen Sie im Dialogfeld, das angezeigt wird, einen Kommentar ein wählen Sie dann **OK**.
9. Um die Aktivierung eines Workflows aufzuheben oder einen zuvor erstellten Workflow zu aktivieren, gehen Sie zu **Anlagenleasing \> Einrichtung \> Leasing-Workflow**. Dann auf der **Leasing-Workflow**-Seite wählen Sie **Workflow \> Versionen** aus. Um einen aktuellen Workflow inaktiv zu machen, wählen Sie den aktiven Mietvertrag im Dialogfeld Mietvertragsversion aus und wählen Sie dann **Inaktiv machen** aus. Um einen vorhandenen Workflow zu aktivieren, wählen Sie den Workflow aus und wählen Sie dann **Aktivieren**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
