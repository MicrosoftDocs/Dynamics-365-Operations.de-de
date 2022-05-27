---
title: Ein Projektbuget erstellen und übermitteln – Workflow
description: Diese Prozedur zeigt Ihnen, wie Sie das Budget für ein Projekt erstellen und übermitteln.
author: GalynaFedorova
ms.date: 11/22/2021
ms.topic: article
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e554fb578371f52f665ef348d6fa81fd27196a9e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671027"
---
# <a name="create-and-submit-a-project-budget-workflow"></a>Ein Projektbuget erstellen und übermitteln – Workflow

[!include [banner](../../includes/banner.md)]

Wenn Sie ein Projektbudget erstellen, können Sie die vorkalkulierten Umsatzerlöse und Kosten für ein Projekt eingegeben und diese Werte anschließend zum Steuern der tatsächlichen Projektbuchungen verwenden. Bei der Projektbudgetierung müssen alle ursprünglichen Budgets und Überarbeitungen an den Projektworkflow zur Genehmigung gesendet werden. Der Workflow verbessert die Steuerung der Budegetierung, und der Änderungsverlauf wird aufgezeichnet. Nachdem Sie ein [Projekt erstellen](/dynamicsax-2012/appuser-itpro/create-a-project), verwenden Sie die Prozedur, um das Budget zu erstellen und zu übermitteln.

1. Wechseln Sie zu **Module** > **Projektverwaltung und -verrechnung** > **Projekte** > **Alle Projekte**.
1. Wählen Sie in der Projektliste ein Projekt aus.
1. Wählen Sie auf der Detailseite des Projekts die Registerkarte **Planen** aus.
1. Wählen Sie in der Gruppe **Budget** **Projektbudget** aus.
1. Geben Sie auf dem Inforegister **Allgemein** die folgenden Informationen ein:
   - Geben Sie im Feld **Beschreibung** einen Wert ein.
   - Option auswählen für **Ursprüngliches Budget**.
   - Option auswählen für **Verbleibendes Budget**.
1. Erweitern Sie das Inforegister **Kosten** und wählen Sie **Neu**. Legen Sie dann die folgenden Einstellungen fest:
   - Wählen Sie für **Transaktionsart** eine Option aus.
   - Wählen Sie eine geeignete **Kategorie**.
   - Geben Sie einen Wert in **Ursprüngliches Budget** ein.
1. Erweitern Sie das Inforegister **Erlöse** und wählen Sie **Neu**. Legen Sie dann die folgenden Einstellungen fest:
   - Wählen Sie für **Transaktionsart** eine Option aus.
   - **Kategorie** auswählen.
   - Geben Sie einen Wert für **Ursprüngliches Budget** ein.
1. Wählen Sie **Speichern** aus.
1. Wählen Sie **Workflow \> Absenden** aus.
1. Geben Sie auf der **Workflow des ursprünglichen Budgets überprüfen – Absenden**-Seite einen **Kommentar** ein und wählen Sie **Absenden** aus.
