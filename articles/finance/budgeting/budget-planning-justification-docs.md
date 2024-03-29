---
title: Budgetplanungs-Begründungsdokumente
description: Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03780b36cb3a6a609350c61792f0c98f2c08244d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711770"
---
# <a name="budget-planning-justification-documents"></a>Budgetplanungs-Begründungsdokumente

[!include [banner](../includes/banner.md)]

Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist. 

Eine Budgetplanvorlage wird vom Budget-Manager in Microsoft Word erstellt und zum aktuellen Budgetplanungsprozess hinzugefügt. Budgeteigentümer können die Vorlage öffnen und dann die Daten automatisch in Word auf der Grundlage ihrer Budgetanforderung ausfüllen. Sie können zusätzliche Text oder Daten vor dem Speichern anfügen und Ihre personalisierten  Begründungsdokument im Budgetplan hinzufügen.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Dynamics Office-Add-In für Microsoft Word einrichten

1.  Öffnen Sie ein neues Microsoft Word-Dokument.
2.  Klicken Sie auf **Einfügen** auf dem Menüband und dann auf **Shop**.
3.  Suchen Sie nach Microsoft Dynamics Office Add-in, und klicken Sie auf **Hinzufügen**.
4.  In Word im rechten Bereich, klicken  Sie auf **Serverinformationen hinzufügen.**
5.  Geben Sie die URL des Server ein und klicken Sie auf **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definieren der Begründungsvorlage in Microsoft Word

1.  Klicken Sie auf **Entwurf** im Microsoft Dynamics Office-Add-In, nachdem Sie sich angemeldet haben.
2.  Für Kopfdaten verwenden Sie die Schaltfläche **Felder hinzufügen**.
3.  Wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf **Weiter**. **Hinweis:** Diese Entität ist für alle Begründungsdokumente erforderlich. Andere Entitäten können verwendet werden, aber der Upload zurück an Microsoft Dynamics 365 Finance schlägt fehl, wenn diese Entität nicht einbezogen wird.
4.  Fügen Sie BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter und DocumentNumber Bezeichnungen und Werte im Word-Dokument hinzu. **Hinweis**: Sie können eigene benutzerdefinierten Beschriftungen verwenden, statt die Standardetiketts, sofern erforderlich.
5.  Klicken Sie **Fertig**, um den Kopfbereich abzuschließen.
6.  Für Positionsebenedetail von Budgetplanbeträgen, klicken Sie auf **Tabelle hinzufügen**
7.  Wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf **Weiter**.
8.  Hinzufügen von Feldern für EffectiveDate, ScenarioName, AccountDisplayValue und AccountingCurrencyExpenseAmount. **Hinweis:** Wenn Kommentare verfügbar sind und innerhalb der einzelnen Budgetplanpositionen hinzugefügt werden, können diese in Tabelle hier hinzugefügt werden.
9.  Fügen Sie alle zusätzlichen Anweisungen hinzu, wie Endbenutzer bereitzustellen, und führen Sie eine erforderliche Formatierung oder das Formatieren des Dokuments aus.
10. Speichern Sie das Dokument lokal auf Ihrem Computer und schließen Sie die Datei, bevor Sie fortfahren.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Richten Sie den Budgetplanungsprozess ein, den Sie mit der Begründungsvorlage verwenden möchten.

1.  Gehen Sie zu **Planung** &gt; **Einstellungen** &gt; **Budgetplanung** &gt; **Begründungsdokumentvorlagen**.
2.  Klicken Sie auf **Neu**, und navigieren Sie zu Ihrem neu erstellten Microsoft Word-Dokument.
3.  Vorlagenname und Beschreibung eingeben. Klicken Sie auf **OK**.
4.  Navigieren Sie zu **Budgetierung** &gt; **Einrichtung** &gt; **Budget** **Planung** &gt; **Butgetplanungsprozess**.
5.  Wählen Sie den Prozess aus, in dem die Begründungsvorlage verwendet werden soll, und klicken Sie auf **Bearbeiten**.
6.  Wählen Sie im Feld **Begründungsdokumentvorlage** die geeignete Vorlage aus und speichern Sie diese.

##### <a name="edit-and-save-personalized-justification-documents"></a>Bearbeiten und speichern Sie personalisierte Begründungsdokumente

1.  Erstellen Sie einen neuen Budgetplan oder öffnen Sie einen vorhandenen Budgetplan.
2.  Im Dropdownmenü **Begründung** wählen Sie **Neue Begründung erstellen**.
3.  Nachdem Sie die Details ausgefüllt haben, laden Sie das personalisierte Dokument aus dem Dropdownmenü **Begründung** hoch.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
