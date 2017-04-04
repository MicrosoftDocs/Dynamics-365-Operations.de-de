---
title: Budget planning justification documents
description: "Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Budget planning justification documents

Begründungsdokumente ermöglichen eine Erläuterung für diese Anfordern eines Budgets, um zu erläutern bereit, warum ein bestimmtes Budget erforderlich ist. 

Eine Budgetplanvorlage wird vom Budget-Manager in Microsoft Word erstellen und zum aktuellen Budgetplanungsprozess. Budgeteigentümer können die Vorlage und öffnen dann die Daten haben, die automatisch in Word auf der Grundlage ihrer Budgetanforderung ausgefüllt werden. Sie können zusätzliche Text oder Daten vor dem Anfügen Speichervorgangs und ihrer Begründungsdokuments personalisierten ihrem Budgetplan hinzufügen.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Einstellungs-MicrosoftDynamicss Add-In für Microsoft Office Word

1.  Öffnet ein neues Microsoft Word-Dokument).
2.  ** Einfügen auf ** auf dem Menüband auf Shop ** **.
3.  Suchen Add-In Microsoft Dynamics und auf Office ** Hinzufügen **.
4.  In Word im rechten Bereich, auf ** fügen Sie Serverinformationen ** hinzu.
5.  Dient zum Eingeben oder fügen Sie die URL ein Server und klicken Sie auf OK ** **.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Definieren Sie die Begründungsvorlage in Microsoft Word

1.  ** Auf Entwurf ** Add-In im Microsoft Dynamics Public-Vorlage Office, nachdem Sie angemeldet haben.
2.  Für Kopfdaten verwenden Sie die Felder hinzu ** fügen Sie ** Schaltfläche.
3.  Wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf Weiter ** **. ** Hinweis: ** Diese Entität ist für alle Begründungsdokument erforderlich. Andere Entitäten können verwendet werden, aber der Upload zurück an Microsoft Dynamics 365 für Arbeitsgänge schlägt fehl, wenn diese Entität nicht einbezogen wird.
4.  Fügen Sie das BudgetPlanName, das BudgetPlanPreparer, das ResponsibilityCenter und Bezeichnungen und die Werte im DocumentNumber Word-Dokument hinzu. ** Hinweis: ** Sie können eigene benutzerdefinierten Beschriftungen, anstatt die Standardetiketts verwenden, falls erforderlich.
5.  ** Auf erfolgt ** um das Kopfbereichs abzuschließen.
6.  Für Positionsebenedetail von Budgetplanbeträgen, auf ** fügen Sie Tabelle hinzufügen **.
7.  Wieder wählen Sie die Entitätsdatenquelle von BudgetPlanJustification aus, und klicken Sie auf Weiter ** **.
8.  Hinzufügen von Feldern für EffectiveDate, ScenarioName, AccountDisplayValue und AccountingCurrencyExpenseAmount hinzu. ** Hinweis: ** Wenn Kommentare sind verfügbar, innerhalb der einzelnen Budgetplanpositionen hinzuzufügen, können die in Tabelle hier hinzugefügt werden.
9.  Fügen Sie alle zusätzliche Anweisungen hinzu, z Endbenutzer bereitzustellen, und führen Sie eine erforderliche Formatierung oder das Formatieren dem Dokument aus.
10. Speichern Sie das Dokument an den lokalen Computer und schließen Sie die Datei, bevor Sie fortfahren.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Installieren des Budgetplanungsprozess, um die Begründungsvorlage zu verwenden

1.  In Microsoft Dynamics 365 für Arbeitsgänge, fahren ** Planung ** &gt; ** Einstellungen ** &gt; ** Budgetplanung ** ** &gt; Begründungsdokumentvorlagen **.
2.  ** Der auf neu ** und durchsuchen dem neu erstellten oder ein Microsoft Word-Dokument).
3.  Geben Sie einen Vorlagenanzeigenamen und eine Beschreibung ein. Click **OK**.
4.  Wechseln ** Planung ** &gt; ** Einstellungen ** &gt; ** Budget ** ** Planung ** &gt; ** Budgetplanungsprozess **.
5.  Wählen Sie den Prozess, in dem die Begründungsvorlage verwendet werden soll, und klicken Sie auf ** Bearbeiten **.
6.  Wählen Sie im Begründungsdokumentvorlage ** ** Feld die geeignete Vorlage aus und speichern Sie.

##### <a name="edit-and-save-personalized-justification-documents"></a>Bearbeiten und speichern Sie personalisierte Begründungsdokumente

1.  In Dynamics 365 für Arbeitsgänge, erstellen Sie einen neuen Budgetplan oder öffnen Sie einen vorhandenen Budgetplan.
2.  Im ** Begründung ** Dropdownmenü auswählen ** erstellen Sie neue Begründung **.
3.  Nachdem Sie in ausgefüllt haben, wählen Sie aus, um das Dokument aus dem personalisierte ** Begründung ** Dropdownmenü hochzuladen.



