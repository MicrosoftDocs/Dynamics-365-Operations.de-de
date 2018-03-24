---
title: "Finanzberichterstellungs-Data Mart zurücksetzen"
description: "In diesem Thema wird beschrieben, wie der Rechnungslegungs-Damart zurückgesetzt wird."
author: aolson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: aloson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 5b956dcc5a4a93033396ae0ffcf8b7aeba2cf3f2
ms.openlocfilehash: a07e8b5bae2c4f71e9212cd2f8080d2481769818
ms.contentlocale: de-de
ms.lasthandoff: 12/14/2017

---

# <a name="reset-the-financial-reporting-data-mart"></a><span data-ttu-id="66b5b-103">Finanzberichterstellungs-Data Mart zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="66b5b-103">Reset the Financial reporting data mart</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="66b5b-104">In diesem Thema wird erläutert, wie der Rechnungslegungs-Datamart für die folgenden Versionen zurückgesetzt wird:</span><span class="sxs-lookup"><span data-stu-id="66b5b-104">This topic explains how to reset the Financial reporting data mart for the following versions:</span></span>

- <span data-ttu-id="66b5b-105">Microsoft Dynamics 365 for Finance and Operations Financial Reporting Release 7.2.6.0 und später</span><span class="sxs-lookup"><span data-stu-id="66b5b-105">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>
- <span data-ttu-id="66b5b-106">Microsoft Dynamics 365 for Finance and Operations Financial Reporting Release 7.0.10000.4 und später</span><span class="sxs-lookup"><span data-stu-id="66b5b-106">Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>
- <span data-ttu-id="66b5b-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise-Edition (lokal)</span><span class="sxs-lookup"><span data-stu-id="66b5b-107">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises)</span></span>

<span data-ttu-id="66b5b-108">Um Finance and Operations Finanzberichterstellung Version 7.2.6.0 abzurufen, können Sie KB 4052514 von <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514> herunterladen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-108">To get Finance and Operations Financial reporting release 7.2.6.0, you can download KB 4052514 from <https://fix.lcs.dynamics.com/Issue/Resolved?kb=4052514>.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-7260-and-later"></a><span data-ttu-id="66b5b-109">Setzt den Rechnungslegungs-Datamart für Finance and Operations Rechnungslegungsfreigabe 7.2.6.0 und später zurück</span><span class="sxs-lookup"><span data-stu-id="66b5b-109">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.2.6.0 and later</span></span>

### <a name="reset-the-financial-reporting-data-mart-from-report-designer"></a><span data-ttu-id="66b5b-110">Setzt den Rechnungslegungs-Datamart im Berichts-Designer zurück</span><span class="sxs-lookup"><span data-stu-id="66b5b-110">Reset the Financial reporting data mart from Report designer</span></span>

> [!NOTE]
> <span data-ttu-id="66b5b-111">Die Schritte dieses Prozesses werden für Finance and Operations Finanzbericht Release 7.2.6.0 und später unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-111">The steps in this process are supported for Finance and Operations Financial reporting release 7.2.6.0 and later.</span></span> <span data-ttu-id="66b5b-112">Wenn Sie nur eine ältere Version besitzen, wenden Sie sich für Hilfe an das Support-Team.</span><span class="sxs-lookup"><span data-stu-id="66b5b-112">If you have an earlier release, contact the Support team for assistance.</span></span>

<span data-ttu-id="66b5b-113">In bestimmten Szenarien kann es nötig sein, den Datenmarkt für die Finanzberichterstellung zurückzsetzen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-113">In specific scenarios, you might have to reset the data mart for Financial reporting.</span></span> <span data-ttu-id="66b5b-114">Sie können diese Aufgabe im Berichts-Designer Client abschließen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-114">You can complete this task in the Report designer client.</span></span> <span data-ttu-id="66b5b-115">Nachfolgend sind mehrere Szenarios, wo Sie möglicherweise den Data Mart zurücksetzen müssen:</span><span class="sxs-lookup"><span data-stu-id="66b5b-115">Here are some scenarios where you might have to reset the data mart:</span></span>

- <span data-ttu-id="66b5b-116">Die Finance and Operations Datenbank wurde wiederhergestellt, aber die Data Mart-Datenbank wurde nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-116">The Finance and Operations database was restored, but the data mart database wasn't restored.</span></span>
- <span data-ttu-id="66b5b-117">Sie finden falsche Daten für eine Periode.</span><span class="sxs-lookup"><span data-stu-id="66b5b-117">You see incorrect data for a period.</span></span>
- <span data-ttu-id="66b5b-118">Unterstützung weist Sie an, den Data Mart als Teil eines Problembehandlungsschritts zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-118">Support instructs you to reset the data mart as part of a troubleshooting step.</span></span>

<span data-ttu-id="66b5b-119">Die Data Mart-Rücksetzung sollte nur für Zeiten ausgeführt werden, wenn der Betrag des Verarbeitens für die Datenbank klein ist.</span><span class="sxs-lookup"><span data-stu-id="66b5b-119">The data mart reset should be done only during times when the amount of processing on the database is small.</span></span> <span data-ttu-id="66b5b-120">Finanzberichterstellung ist während dem Rücksetzungsprozesses nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="66b5b-120">Financial reporting will be unavailable during the reset process.</span></span>

#### <a name="reset-the-data-mart"></a><span data-ttu-id="66b5b-121">Data Mart zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="66b5b-121">Reset the data mart</span></span>

<span data-ttu-id="66b5b-122">Um den Data Mart im Berichts-Designer im Menü **Extras** zurückzusetzen, wählen Sie **Data Mart zurücksetzen** aus.</span><span class="sxs-lookup"><span data-stu-id="66b5b-122">To reset the data mart, in Report designer, on the **Tools** menu, select **Reset Data Mart**.</span></span> <span data-ttu-id="66b5b-123">Das Dialogfeld, das angezeigt wird, verfügt über zwei Abschnitte: **Statistik** und **Zurücksetzen**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-123">The dialog box that appears has two sections: **Statistics** and **Reset**.</span></span>

<span data-ttu-id="66b5b-124">[![Dialogfeld Data Mart zurücksetzen](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="66b5b-124">[![Reset Data Mart dialog box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

##### <a name="integration-attempts"></a><span data-ttu-id="66b5b-125">Integrationsversuche</span><span class="sxs-lookup"><span data-stu-id="66b5b-125">Integration attempts</span></span>

<span data-ttu-id="66b5b-126">Das Raster **Integrationsversuche** zeigt, wie oft das System versucht hat, Buchungen zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="66b5b-126">The **Integration attempts** grid shows how many times the system has tried to integrate transactions.</span></span> <span data-ttu-id="66b5b-127">Das System versucht weiter, Daten über einen Zeitraum von Tagen zu integrieren, wenn die ersten Versuche nicht erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="66b5b-127">The system continues to try to integrate data over a period of days if the first few attempts aren't successful.</span></span> <span data-ttu-id="66b5b-128">Sie wissen, dass der Data Mart zurückgesetzt werden muss, wenn die Anzahl von Versuchen 8 oder höher ist und wenn es viele Dimensionskombination oder Buchungsdatensätze gibt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-128">You will know that the data mart must be reset is if the number of attempts is 8 or more, and if there are many Dimension combination or Transaction records.</span></span> <span data-ttu-id="66b5b-129">In diesem Fall sind die Daten nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="66b5b-129">In this situation, the data won't be reported on.</span></span>

##### <a name="data-status"></a><span data-ttu-id="66b5b-130">Datenstatus</span><span class="sxs-lookup"><span data-stu-id="66b5b-130">Data status</span></span>

<span data-ttu-id="66b5b-131">Das Raster **Datenenstatus** enthält eine Momentaufnahme der Buchungen, der Wechselkurse und Dimensionswerten im Data Mart.</span><span class="sxs-lookup"><span data-stu-id="66b5b-131">The **Data status** grid provides a snapshot of the transactions, exchange rates, and dimension values in the data mart.</span></span> <span data-ttu-id="66b5b-132">Eine große Anzahl von Datensätzen gibt an, dass verschiedene Aktualisierungen an Datensätzen erfolgt sind.</span><span class="sxs-lookup"><span data-stu-id="66b5b-132">A large number of stale records indicates that numerous updates to the records have occurred.</span></span> <span data-ttu-id="66b5b-133">Diese Situation kann langsamere Berichterstellungszeiten verursachen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-133">This situation might cause slower report generation times.</span></span>

##### <a name="misaligned-main-account-categories"></a><span data-ttu-id="66b5b-134">Falsch ausgerichtete Hauptkontokategorien</span><span class="sxs-lookup"><span data-stu-id="66b5b-134">Misaligned main account categories</span></span>

<span data-ttu-id="66b5b-135">Wenn Sie eine Version verwenden, die früher als Microsoft Dynamics 365 for Finance and Operations Financial Reporting 7.2.1 ist, müssen Sie den Data Mart zurücksetzen, wenn Sie Konten umbenennen und zwischen Kontokategorien Konten verschieben.</span><span class="sxs-lookup"><span data-stu-id="66b5b-135">If you're using a release that is earlier than Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.2.1, you might have to reset the data mart if you rename accounts and move accounts between account categories.</span></span> <span data-ttu-id="66b5b-136">Diese Aktivitäten können dafür verantwortlich sein, dass Hauptkontokategorien nicht korrekt abgestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="66b5b-136">These actions can cause main account categories to become misaligned.</span></span> <span data-ttu-id="66b5b-137">Das Feld **Falsch ausgerichtete Hauptkontokategorien** zeigt an, ob Sie dieses Problem ermitteln.</span><span class="sxs-lookup"><span data-stu-id="66b5b-137">The **Misaligned main account categories** field shows whether you're experiencing that issue.</span></span>

### <a name="reset-the-data-mart-in-finance-and-operations-financial-reporting-release-7260"></a><span data-ttu-id="66b5b-138">Setzt den Data Mart in Finance and Operations Financial Reporting, Release 7.2.6.0 zurück</span><span class="sxs-lookup"><span data-stu-id="66b5b-138">Reset the data mart in Finance and Operations Financial reporting release 7.2.6.0</span></span>

<span data-ttu-id="66b5b-139">Um den Data Mart im Bereich Finance and Operations Financial Reporting, Release 7.2.6.0 und früher zurückzusetzen im Dialogfeld **Data Mart zurücksetzen** wählen Sie **Setzen Sie Data Mart zurück**, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="66b5b-139">To reset the data mart in Finance and Operations Financial reporting release 7.2.6.0 and earlier, in the **Reset Data Mart** dialog box, select the **Reset data mart** check box, and then select **OK**.</span></span> <span data-ttu-id="66b5b-140">Sie sollten den Data Marts nur während einer geplanten Ausfallzeit zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-140">You should reset the data mart only during scheduled downtime.</span></span>

<span data-ttu-id="66b5b-141">[![Dialogfeld Data Mart zurücksetzen](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span><span class="sxs-lookup"><span data-stu-id="66b5b-141">[![Reset data mart check box](./media/Reset-72.jpg)](./media/Reset-72.jpg)</span></span>

### <a name="reset-the-data-mart-and-select-a-reason-in-microsoft-dynamics-365-for-finance-and-operations-financial-reporting-release-730"></a><span data-ttu-id="66b5b-142">Data Mart zurücksetzen und wählen Sie einen Grund in Microsoft Dynamics 365 for Finance and Operations Financial Reporting Release 7.3.0 aus.</span><span class="sxs-lookup"><span data-stu-id="66b5b-142">Reset the data mart and select a reason in Microsoft Dynamics 365 for Finance and Operations Financial reporting release 7.3.0</span></span>

<span data-ttu-id="66b5b-143">Stellt sich heraus, dass eine Data Mart-Rücksetzung erforderlich ist, aktivieren Sie das Kontrollkästchen **Setzen Sie Data Mart zurück**, und wählen Sie dann einen Grund im Feld **Grund** aus.</span><span class="sxs-lookup"><span data-stu-id="66b5b-143">If you determine that a data mart reset is required, select the **Reset data mart** check box, and then select a reason in the **Reason** field.</span></span> <span data-ttu-id="66b5b-144">Die folgenden Optionen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="66b5b-144">The following options are available:</span></span>

- <span data-ttu-id="66b5b-145">**Fehlende oder falsche Daten** – Basierend auf Statistiken haben Sie festgestellt, dass Daten möglicherweise fehlen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-145">**Missing or incorrect data** – Based on the statistics, you've determined that data might be missing.</span></span> <span data-ttu-id="66b5b-146">Bevor Sie fortfahren, wird empfohlen, dass Sie mit Support arbeiten, um festzustellen, was den Fehler verursacht.</span><span class="sxs-lookup"><span data-stu-id="66b5b-146">Before you continue, we recommend that you work with Support to determine the root cause.</span></span>
- <span data-ttu-id="66b5b-147">**Datenbank wiederherstellen** - Die Finance und Operations Datenbank wurde wiederhergestellt, aber die Data Mart-Datenbank wurde nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-147">**Restore database** – The Finance and Operations database was restored, but the database for the Financial reporting data mart wasn't restored.</span></span>
- <span data-ttu-id="66b5b-148">**Sonstiges** – Setzen Sie den Data Mart für einen anderen Grund zurück.</span><span class="sxs-lookup"><span data-stu-id="66b5b-148">**Other** – You're resetting the data mart for another reason.</span></span> <span data-ttu-id="66b5b-149">Wenn Sie göaibem. dass ein Problem besteht, kontaktieren Sie den Support, um das Problem zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="66b5b-149">If you're concerned that there is an issue, contact Support to identify it.</span></span>

<span data-ttu-id="66b5b-150">[![Data Mart zurücksetzen](./media/Integration.png)](./media/Integration.png)</span><span class="sxs-lookup"><span data-stu-id="66b5b-150">[![Reset data mart](./media/Integration.png)](./media/Integration.png)</span></span>

> [!NOTE]
> <span data-ttu-id="66b5b-151">Überprüfen Sie, ob durch alle Data Mart-Zurücksetzungsaufgaben ein erstmaliges Laden abgeschlossen wurde, bevor Sie mit dem Zurücksetzen beginnen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-151">Verify that all data mart reset tasks have completed an initial load before you begin a reset.</span></span> <span data-ttu-id="66b5b-152">Sie können dies bestätigen, indem Sie nach einem Wert in der Spalte „Letzte Laufzeit” suchen, indem Sie **Extras** &gt; **Integrationsstatus** auswählen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-152">You can confirm this by looking for a value in the Last Runtime column by selecting **Tools** &gt; **Integration status**.</span></span>

#### <a name="clear-users-and-companies"></a><span data-ttu-id="66b5b-153">Benutzer und Unternehmen löschen</span><span class="sxs-lookup"><span data-stu-id="66b5b-153">Clear users and companies</span></span>

<span data-ttu-id="66b5b-154">Aktivieren Sie das Kontrollkästchen **Deaktivieren von Benutzern und Unternehmen**, wenn die Datenbank wiederhergestellt wurde, aber Sie dann Änderungen an Benutzern oder an Unternehmen vorgenommenen haben.</span><span class="sxs-lookup"><span data-stu-id="66b5b-154">Select the **Clear users and companies** check box if you restored your database, but you then made changes to users or companies.</span></span> <span data-ttu-id="66b5b-155">Sie sollten dieses Kontrollkästchen nur selten auswählen müssen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-155">You should rarely have to select this check box.</span></span>

<span data-ttu-id="66b5b-156">Wenn Sie bereit sind, den Rücksetzungsprozess zu verwenden, aktivieren Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-156">When you're ready to start the reset process, select **OK**.</span></span> <span data-ttu-id="66b5b-157">Sie werden aufgefordert zu bestätigen, dass, Sie bereit sind, den Prozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="66b5b-157">You're prompted to confirm that you're ready to start the process.</span></span> <span data-ttu-id="66b5b-158">Beachten Sie, dass die Finanzberichterstellung nicht verfügbar ist während der Rücksetzung und der ersten Datenintegration, die dann erfolgt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-158">Note that Financial reporting won't be available during the reset and the initial data integration that occurs afterward.</span></span>

<span data-ttu-id="66b5b-159">Wenn Sie den Status bei der Integration erneut ausführen, wählen Sie **Extras** &gt; **Integrationsstatus**, um das letzte Mal zu sehen, als die Integration ausgeführt wurde und den Status.</span><span class="sxs-lookup"><span data-stu-id="66b5b-159">If you want to review the status of the integration, select **Tools** &gt; **Integration status** to see the last time that the integration was run and the status.</span></span>

<span data-ttu-id="66b5b-160">[![Zeigt den Status der Integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span><span class="sxs-lookup"><span data-stu-id="66b5b-160">[![View the status of the integration](./media/New-integration.PNG)](./media/New-integration.PNG)</span></span>

> [!NOTE]
> <span data-ttu-id="66b5b-161">Die Zurücksetzung ist abgeschlossen, wenn alle Zuordnungen den Status „RanToCompletion” anzeigen und das Fenster „Integrationsstatus” die Meldung „Integration abgeschlossen” in der Ecke unten links wiedergibt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-161">The reset is finished when all mappings show the status of RanToCompletion and the Integration Status window says “Integration complete” in the bottom-left corner.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-financial-reporting-release-70100004-and-later"></a><span data-ttu-id="66b5b-162">Setzt den Rechnungslegungs-Datamart für Finance and Operations Rechnungslegungsfreigabe 7.0.10000.4 und später zurück</span><span class="sxs-lookup"><span data-stu-id="66b5b-162">Reset the Financial reporting data mart for Finance and Operations Financial reporting release 7.0.10000.4 and later</span></span>

<span data-ttu-id="66b5b-163">Wenn Sie ggf. die Finance and Operations-Datenbank aus einer Sicherung wiederherstellen oder die Datenbank aus einer anderen Umgebung kopieren, müssen Sie die Schritte in diesem Thema ausführen, um sicherzustellen, dass der Rechnungslegungs-datamart ordnungsgemäß die zu stornierenden Finance and Operations-Datenbank verwendet.</span><span class="sxs-lookup"><span data-stu-id="66b5b-163">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this section to help guarantee that the Financial reporting data mart correctly uses the restored Finance and Operations database.</span></span>

> [!NOTE]
> <span data-ttu-id="66b5b-164">Beachten Sie, dass die Schritte dieses Prozesses für Microsoft Dynamics AX Anwendungsversion 7.0.1 (Mai 2016 ) (Anwendungs-Build 7.0.1265.23014 und Financial Reporting Build 7.0.10000.4) und später Versionen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="66b5b-164">The steps in this process are supported for Microsoft Dynamics AX application version 7.0.1 (May 2016) (application build 7.0.1265.23014 and Financial reporting build 7.0.10000.4) and later.</span></span> <span data-ttu-id="66b5b-165">Wenn Sie eine frühere Version von Finance and Operations nutzen, wenden Sie sich bitte an unser Support-Team.</span><span class="sxs-lookup"><span data-stu-id="66b5b-165">If you have an earlier version of Finance and Operations, contact Support for assistance.</span></span>

### <a name="export-report-definitions"></a><span data-ttu-id="66b5b-166">Exportieren von Berichtsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="66b5b-166">Export report definitions</span></span>

<span data-ttu-id="66b5b-167">Gehen Sie folgendermaßen vor, um die Berichtsdesigne im Berichts-Designer zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="66b5b-167">First, follow these steps to export the report designs from Report designer.</span></span>

1. <span data-ttu-id="66b5b-168">Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-168">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="66b5b-169">Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-169">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="66b5b-170">Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-170">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="66b5b-171">Wählen Sie die Berichtsdefinition für den Export aus:</span><span class="sxs-lookup"><span data-stu-id="66b5b-171">Select the report definitions to export:</span></span>

    - <span data-ttu-id="66b5b-172">Klicken Sie auf **Alles markieren**, um die Berichtsdefinitionen und die dazugehörigen Bausteine zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="66b5b-172">To export all your report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="66b5b-173">Um bestimmte Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze zu exportieren, klicken Sie auf die entsprechende Registerkarte und wählen die Artikel aus, die exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-173">To export specific reports, rows, columns, trees, or dimension sets, select the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="66b5b-174">Drücken und halten Sie die STRG-Taste gedrückt, um mehrere Elemente auf einer Registerkarte auszuwählen. Wenn Sie Berichte für den Export auswählen, werden die zugeordneten Zeilen, Spalten, Strukturen und Dimensionssätze ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-174">Press and hold the Ctrl key to select multiple items on a tab. When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4. <span data-ttu-id="66b5b-175">Wählen Sie **Exportieren**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-175">Select **Export**.</span></span>
5. <span data-ttu-id="66b5b-176">Geben Sie einen Dateinamen eingeben und einen sicheren Ort aus, an dem Sie die exportierten Berichtsdefinitionen speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="66b5b-176">Enter a file name, and select a secure location where you want to save the exported report definitions.</span></span>
6. <span data-ttu-id="66b5b-177">Wählen Sie **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-177">Select **Save**.</span></span>

<span data-ttu-id="66b5b-178">Anschließend können Sie die Datei an einen sicheren Standort kopieren oder hochladen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-178">You can copy or upload the file to a secure location.</span></span> <span data-ttu-id="66b5b-179">Auf diese Weise kann die Datei in einer anderen Umgebung zu einem späteren Zeitpunkt importiert werden.</span><span class="sxs-lookup"><span data-stu-id="66b5b-179">In this way, the file can be imported into a different environment later.</span></span> <span data-ttu-id="66b5b-180">Informationen zur Verwendung eines Microsoft Azure Storage-Kontos können gefunden werden in [Daten mit dem AzCopy-Kommandozeilenutility übertragen](/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="66b5b-180">For information about how to use a Microsoft Azure storage account, see [Transfer data with the AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy).</span></span>

> [!NOTE]
> <span data-ttu-id="66b5b-181">Microsoft stellt kein Speicherkonto im Rahmen der Finance and Operations Vereinbarung bereit.</span><span class="sxs-lookup"><span data-stu-id="66b5b-181">Microsoft doesn't provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="66b5b-182">Sie müssen entweder ein Speicherkonto kaufen oder ein Speicherkonto von einem separaten Azure-Abonnement verwenden.</span><span class="sxs-lookup"><span data-stu-id="66b5b-182">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span>

> [!WARNING]
> <span data-ttu-id="66b5b-183">Wichtig: Berücksichtigen Sie das Verhalten des D-Laufwerks von Azure Virtual Machines (VMs).</span><span class="sxs-lookup"><span data-stu-id="66b5b-183">Be aware of the behavior of drive D on Azure virtual machines (VMs).</span></span> <span data-ttu-id="66b5b-184">Speichern Sie die exportierten Bausteingruppen auf Laufwerk D nicht permanent. Weitere Informationen zu temporären Laufwerken finden Sie unter [Einverständnis des temporären Laufwerks auf Windows Azure-virtuellen Computern](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="66b5b-184">Don't permanently store your exported building block groups on drive D. For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

### <a name="stop-services"></a><span data-ttu-id="66b5b-185">Services anhalten</span><span class="sxs-lookup"><span data-stu-id="66b5b-185">Stop services</span></span>

<span data-ttu-id="66b5b-186">Die olgenden Microsoft Windows Dienste haben offene Verbindungen zur Finance and Operations-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="66b5b-186">The following Microsoft Windows services will have open connections to the Finance and Operations database.</span></span> <span data-ttu-id="66b5b-187">Verwenden den Microsoft Remotedesktop, um sich mit allen Computern in der Umgebung zu verbinden und die folgenden Windows-Dienste zu beenden, indem Sie services.msc verwenden:</span><span class="sxs-lookup"><span data-stu-id="66b5b-187">Therefore, you must use Microsoft Remote Desktop to connect to all the computers in the environment and then use services.msc to stop these services.</span></span>

- <span data-ttu-id="66b5b-188">Internet-Publishing-Dienst (Anwendungsopbjekt-Server [AOS]-Computer)</span><span class="sxs-lookup"><span data-stu-id="66b5b-188">World wide web publishing service (on all Application Object Servers [AOS] computers)</span></span>
- <span data-ttu-id="66b5b-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)</span><span class="sxs-lookup"><span data-stu-id="66b5b-189">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="66b5b-190">Management Reporter 2012 Process Service (nur Business Intelligence [BI]-Computer)</span><span class="sxs-lookup"><span data-stu-id="66b5b-190">Management Reporter 2012 Process Service (on Business intelligence [BI] computers only)</span></span>

### <a name="reset"></a><span data-ttu-id="66b5b-191">Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="66b5b-191">Reset</span></span>

#### <a name="download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="66b5b-192">Suchen und laden Sie das letzte MinorVersionDataUpgrade.zip-Paket herunter</span><span class="sxs-lookup"><span data-stu-id="66b5b-192">Download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="66b5b-193">Suchen und laden Sie das letzte MinorVersionDataUpgrade.zip-Paket herunter.</span><span class="sxs-lookup"><span data-stu-id="66b5b-193">Download the latest MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="66b5b-194">Anweisungen dazu, wie Sie die korrekte Version des Datenaktualisierungspakets suchen, finden Sie unter und[Das letzte Datenaktualisierungbereitstellungspaket herunterladen](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="66b5b-194">For instructions about how to find and download the correct version of the data upgrade package, see the[Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> 

<span data-ttu-id="66b5b-195">Eine Aktualisierung ist nicht erforderlich, um das MinorVersionDataUpgrade.zip-Paket herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-195">An upgrade isn't required in order to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="66b5b-196">Deshalb müssen Sie derzeit die Schritte ausführen unter "Herunterladen zur Bereitstellung geeigneter Paket der Datenaktualisierung".</span><span class="sxs-lookup"><span data-stu-id="66b5b-196">Therefore, you just have follow the steps in the "Download the latest data upgrade deployable package" section of that topic.</span></span> <span data-ttu-id="66b5b-197">Sie können alle anderen Schritte im Thema überspringen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-197">You can skip all the other steps in the topic.</span></span>

#### <a name="run-scripts-against-the-finance-and-operations-database"></a><span data-ttu-id="66b5b-198">Ausführen von Skripts für die Finance and Operations-Datenbank</span><span class="sxs-lookup"><span data-stu-id="66b5b-198">Run scripts against the Finance and Operations database</span></span>

<span data-ttu-id="66b5b-199">Führen Sie die folgenden Skripts für die Finance and Operations-Datenbank aus (nicht für die Financial-Reporting-Datenbank):</span><span class="sxs-lookup"><span data-stu-id="66b5b-199">Run the following scripts against the Finance and Operations database (not against the Financial reporting database):</span></span>

- <span data-ttu-id="66b5b-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="66b5b-200">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
- <span data-ttu-id="66b5b-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="66b5b-201">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="66b5b-202">Diese Skripts helfen sicherzustellen, dass die Benutzer, die Rollen und die Änderungsnachverfolgungseinstellungen korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="66b5b-202">These scripts help guarantee that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="run-a-windows-powershell-command-to-reset-the-database"></a><span data-ttu-id="66b5b-203">Führen Sie Windows PowerShell-Befehls aus, um Datenbankfeinabstimmungen zurückzusetzen</span><span class="sxs-lookup"><span data-stu-id="66b5b-203">Run a Windows PowerShell command to reset the database</span></span>

<span data-ttu-id="66b5b-204">Starten Sie auf einem Microsoft Windows PowerShell als Administrator und führen Sie die folgenden Schritte aus, um die Integration zwischen Finance and Operations und Financial Reporting zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-204">On the AOS computer, start Microsoft Windows PowerShell as an administrator, and run the following commands to reset the integration between Finance and Operations and Financial reporting.</span></span>

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail "<reason for resetting>"
```

<span data-ttu-id="66b5b-205">Ist eine kurze Erläuterung der im Parameter im Befehl **Zurückgesetzt-DatamartIntegration**:</span><span class="sxs-lookup"><span data-stu-id="66b5b-205">Here is an explanation of the parameters in the **Reset-DatamartIntegration** command:</span></span>

- <span data-ttu-id="66b5b-206">Die gültigen Werte für **Reason** sind **SERVICING**, **BADDATA**, und **OTHER**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-206">The valid values for **-Reason** are **SERVICING**, **BADDATA**, and **OTHER**.</span></span>
- <span data-ttu-id="66b5b-207">Der **ReasonDetail**-Parameter ist Freitext.</span><span class="sxs-lookup"><span data-stu-id="66b5b-207">The **-ReasonDetail** parameter is free text.</span></span>
- <span data-ttu-id="66b5b-208">Grund und Grund-Detail werden in der Telemetrie-/Umgebungsüberwachung erfasst.</span><span class="sxs-lookup"><span data-stu-id="66b5b-208">The reason and reason detail will be recorded in telemetry/environment monitoring.</span></span>

> [!NOTE]
> <span data-ttu-id="66b5b-209">Nachdem Sie die Befehle ausgeführt haben, werden Sie gebeten, **J** einzugeben, um zu bestätigen, dass Sie die Datenbank zurücksetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="66b5b-209">After you run the commands, you will be asked to enter **Y** to confirm that you want to reset the database.</span></span>

#### <a name="restart-services"></a><span data-ttu-id="66b5b-210">Dienste neu starten</span><span class="sxs-lookup"><span data-stu-id="66b5b-210">Restart services</span></span>

<span data-ttu-id="66b5b-211">Verwenden Sie services.msc, um die Services neu zu starten, die Sie eben beendeten:</span><span class="sxs-lookup"><span data-stu-id="66b5b-211">Use services.msc to restart the services that you stopped earlier:</span></span>

- <span data-ttu-id="66b5b-212">Per Internet WWW-Publishing-Dienst (für alle AOS-Computer)</span><span class="sxs-lookup"><span data-stu-id="66b5b-212">World wide web publishing service (on all AOS computers)</span></span>
- <span data-ttu-id="66b5b-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (nur nicht-private AOS-Computern)</span><span class="sxs-lookup"><span data-stu-id="66b5b-213">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
- <span data-ttu-id="66b5b-214">Management Reporter 2012 Process Service (nur BI-Computer)</span><span class="sxs-lookup"><span data-stu-id="66b5b-214">Management Reporter 2012 Process Service (on BI computers only)</span></span>

#### <a name="import-report-definitions"></a><span data-ttu-id="66b5b-215">Imporiteren von Berichtsdefinitionen</span><span class="sxs-lookup"><span data-stu-id="66b5b-215">Import report definitions</span></span>

<span data-ttu-id="66b5b-216">Importieren Sie die Berichtsdesigns im Berichts-Designer, und zwar mithilfe der Datei, die während des Exports erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="66b5b-216">Import your report designs from Report designer by using the file that was created during the export.</span></span>

1. <span data-ttu-id="66b5b-217">Wechseln Sie im Berichts-Designer zu **Unternehmen** &gt; **Bausteingruppen**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-217">In Report designer, select **Company** &gt; **Building Block Groups**.</span></span>
2. <span data-ttu-id="66b5b-218">Wählen Sie die Bausteingruppe aus, die exportiert werden soll, und klicken Sie **Export**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-218">Select the building block group to export, and then select **Export**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="66b5b-219">Für Finance and Operations wird nur eine Bausteingruppe, unterstützt **Standard**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-219">For Finance and Operations, only one building block group is supported, **Default**.</span></span>

3. <span data-ttu-id="66b5b-220">Wählen Sie den **Standard**-Baustein und klicken Sie auf **Importieren**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-220">Select the **Default** building block, and then select **Import**.</span></span>
4. <span data-ttu-id="66b5b-221">Wählen Sie die Datei aus, welche die exportierten Berichtsdefinitionen enthält und klicken Sie auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="66b5b-221">Select the file that contains the exported report definitions, and then select **Open**.</span></span>
5. <span data-ttu-id="66b5b-222">Wählen Sie im Dialogfeld **Importieren** die Berichtsdefinitionen für den Import aus:</span><span class="sxs-lookup"><span data-stu-id="66b5b-222">In the **Import** dialog box, select the report definitions to import:</span></span>

    - <span data-ttu-id="66b5b-223">Klicken Sie auf **Alles markieren**, um die Berichtsdefinitionen und die dazugehörigen Bausteine zu importieren.</span><span class="sxs-lookup"><span data-stu-id="66b5b-223">To import all the report definitions and the associated building blocks, select **Select All**.</span></span>
    - <span data-ttu-id="66b5b-224">Zum Importieren bestimmter Berichte, Zeilen, Spalten, Strukturen oder Dimensionssätze wählen Sie die entsprechenden Berichte, Spalten, Strukturen oder Dimensionssätze aus.</span><span class="sxs-lookup"><span data-stu-id="66b5b-224">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6. <span data-ttu-id="66b5b-225">**Import** auswählen</span><span class="sxs-lookup"><span data-stu-id="66b5b-225">Select **Import**.</span></span>

## <a name="reset-the-financial-reporting-data-mart-for-finance-and-operations-on-premises"></a><span data-ttu-id="66b5b-226">Setzt den Data Mart in Finance and Operations Financial Reporting (lokal) zurück</span><span class="sxs-lookup"><span data-stu-id="66b5b-226">Reset the Financial reporting data mart for Finance and Operations (on-premises)</span></span>

1. <span data-ttu-id="66b5b-227">Weisen Sie alle Benutzer an, den Berichts-Designer und den Rechnungslegungsbereich in Finance and Operations. zu beenden.</span><span class="sxs-lookup"><span data-stu-id="66b5b-227">Instruct all users to exit Report designer and the Financial reporting area of Finance and Operations.</span></span>
2. <span data-ttu-id="66b5b-228">Führen Sie das folgende Skript für die Rechnungslegungsdatenbank aus (MRDB).</span><span class="sxs-lookup"><span data-stu-id="66b5b-228">Run the following script against the Financial reporting database (MRDB).</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ```

3. <span data-ttu-id="66b5b-229">Schneiden oder löschen Sie alle Datensätze aus der FINANCIALREPORTS-Tabelle in der Finance and Operations-Datenbank (AXDB).</span><span class="sxs-lookup"><span data-stu-id="66b5b-229">Truncate or delete all records from the FINANCIALREPORTS table in the Finance and Operations database (AXDB).</span></span>
4. <span data-ttu-id="66b5b-230">Schneiden oder löschen Sie alle Datensätze aus der FINANCIALREPORTS-Tabelle in der Finance and Operations-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="66b5b-230">Truncate or delete all records from the FINANCIALREPORTVERSION table, if this table exists in the Finance and Operations database.</span></span> <span data-ttu-id="66b5b-231">Wenn die Tabelle nicht in der Finance and Operations-Datenbank vorhanden ist, können Sie diesen Schritt überspringen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-231">If the table doesn't exist in the Finance and Operations database, skip this step.</span></span>
5. <span data-ttu-id="66b5b-232">Führen Sie das **ResetDatamart.sql** Skript für die Rechnungslegungsdatenbank aus (MRDB).</span><span class="sxs-lookup"><span data-stu-id="66b5b-232">Run the **ResetDatamart.sql** script against the Financial reporting database.</span></span> <span data-ttu-id="66b5b-233">Dieses Skript deaktiviert die Data Mart-Integration, löscht alle Data Mart-Daten Data und aktiviert anschließend Data Mart erneut.</span><span class="sxs-lookup"><span data-stu-id="66b5b-233">This script disables the data mart integration, deletes all the data mart data, and then reenables the data mart integration.</span></span>

    ```
    DECLARE @triggerIds table(id uniqueidentifier, taskTypeId uniqueidentifier)
    INSERT INTO @triggerIds SELECT tr.[Id], tt.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8') -- 'Maintenance Task', 'Map Task'
    PRINT 'Disable integration tasks'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 0 WHERE [Id] in (SELECT id FROM @triggerIds)
    ------------------------------
    PRINT 'Drop archive tables'
    ------------------------------
    DECLARE @tableId nvarchar(max)
    DECLARE dropCursor CURSOR LOCAL FAST_FORWARD FOR
    SELECT Id FROM [Datamart].Archive
    OPEN dropCursor
    FETCH NEXT FROM dropCursor INTO @tableId
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'FactStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].FactStaging' + @tableId)
        IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationStaging' + @tableId and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationStaging' + @tableId)
        FETCH NEXT FROM dropCursor INTO @tableId
    END
    CLOSE dropCursor
    DEALLOCATE dropCursor
    IF EXISTS (SELECT 1 FROM INFORMATION_SCHEMA.TABLES t WHERE t.TABLE_NAME = 'DimensionCombinationProcessing' and t.TABLE_SCHEMA = 'Datamart')
        EXEC('DROP TABLE [Datamart].DimensionCombinationProcessing')
    ------------------------------
    PRINT 'Begin Truncating tables'
    ------------------------------
    DECLARE @tablename nvarchar(200)
    DECLARE @schemaname nvarchar(200)
    DECLARE clear_tables CURSOR
        FOR SELECT TABLE_NAME, TABLE_SCHEMA FROM INFORMATION_SCHEMA.TABLES WHERE TABLE_SCHEMA = 'Datamart' AND TABLE_TYPE='BASE TABLE'
    PRINT 'remove check constraints'
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename + '] NOCHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'delete data from tables and rebuild indexes'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
            IF(EXISTS (select TOP 1 1 from sys.foreign_keys where referenced_object_id = OBJECT_ID(@schemaname + '.' + @tablename)) OR
            EXISTS(SELECT TOP 1 1 FROM sys.sql_expression_dependencies sed
            INNER JOIN sys.objects o ON sed.referencing_id = o.[object_id]
            WHERE o.[type] = 'V' 
            AND referenced_schema_name = @schemaname
            AND referenced_entity_name = @tablename))
            BEGIN
            PRINT 'deleting from ' + @tablename
            EXEC('DELETE FROM [' + @schemaname + '].[' + @tablename + ']')
            END
            ELSE
            BEGIN
            PRINT 'truncating from ' + @tablename
            EXEC('TRUNCATE TABLE [' + @schemaname + '].[' + @tablename + ']')
            END
        END
        EXEC('ALTER INDEX ALL ON [' + @schemaname + '].[' + @tablename + '] REBUILD')
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    ------------------------------
    PRINT 'reenable check constraints'
    ------------------------------
    OPEN clear_tables
    FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @tablename <> 'VersionHistory'
        BEGIN
        EXEC('ALTER TABLE [' + @schemaname + '].[' + @tablename +'] WITH CHECK CHECK CONSTRAINT ALL')
        END
        FETCH NEXT FROM clear_tables INTO @tablename, @schemaname
    END
    CLOSE clear_tables
    DEALLOCATE clear_tables
    ------------------------------
    PRINT 'Complete Truncating tables'
    ------------------------------
    ------------------------------
    PRINT 'Remove indexes from DimensionCombination'
    ------------------------------
    DECLARE @indexname nvarchar(200)
    DECLARE drop_indexes CURSOR
    FOR SELECT Name FROM sys.indexes WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]') AND is_primary_key = 0
    OPEN drop_indexes
    FETCH NEXT FROM drop_indexes INTO @indexname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('DROP INDEX [' + @indexname + '] on [Datamart].[DimensionCombination]')
        FETCH NEXT FROM drop_indexes INTO @indexname
    END
    CLOSE drop_indexes
    DEALLOCATE drop_indexes
    ------------------------------
    PRINT 'Drop Columns on DimensionCombination'
    ------------------------------
    DECLARE @objectname nvarchar(200)
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombination]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId', 'InactiveDimensions')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombination] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationResolving'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationResolving]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationResolving] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationStaging'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationStaging]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'OrganizationId', 'Description', 'SourceKey', 'OrganizationKey', 'FreshnessDate')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationStaging] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionCombinationUnreferenced'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionCombinationUnreferenced]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('Id', 'Description', 'SourceKey', 'OrganizationId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionCombinationUnreferenced] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on DimensionValueAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[DimensionValueAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('DimensionValueId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[DimensionValueAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Drop Columns on FactAttributeValue'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[FactAttributeValue]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('FactId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[FactAttributeValue] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalance'
    ------------------------------
    DECLARE @name nvarchar(200)
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalance'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalance]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalance] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    ------------------------------
    PRINT 'Remove constraints from TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_constraints CURSOR
    FOR SELECT Name FROM sys.default_constraints WHERE parent_object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_constraints
    FETCH NEXT FROM drop_constraints INTO @name
    WHILE @@FETCH_STATUS = 0
    BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP CONSTRAINT [' + @name + ']')
        FETCH NEXT FROM drop_constraints INTO @name
    END
    CLOSE drop_constraints
    DEALLOCATE drop_constraints
    ------------------------------
    PRINT 'Drop Columns on TranslatedPeriodBalanceChanges'
    ------------------------------
    DECLARE drop_objects CURSOR
    FOR SELECT Name FROM sys.columns WHERE object_id = OBJECT_ID('[Datamart].[TranslatedPeriodBalanceChanges]')
    OPEN drop_objects
    FETCH NEXT FROM drop_objects INTO @objectname
    WHILE @@FETCH_STATUS = 0
    BEGIN
        IF @objectname NOT IN ('PeriodId', 'DimensionsId', 'ScenarioId', 'FactType', 'PostingLayerId')
        BEGIN
        EXEC('ALTER TABLE [Datamart].[TranslatedPeriodBalanceChanges] DROP COLUMN ' + @objectname)
        END
        FETCH NEXT FROM drop_objects INTO @objectname
    END
    CLOSE drop_objects
    DEALLOCATE drop_objects
    -- Rebuild dropped indexes that are dynamic
    EXEC [Datamart].ConfigureIndexesAndConstraints
    ------------------------------------------
    ------------------------------------------
    PRINT 'Reset the map tokens'
    UPDATE [Connector].[Map] SET InitalLoad = 0, ReaderToken=NULL, LastQuerySuccess='1900-01-01' WHERE MapId IN (SELECT t.[Id]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Reset the tasks'
    UPDATE [Scheduling].[TaskState] SET StateType = 0, Progress = 0.0, LastRunTime = NULL, NextRunTime = NULL WHERE TaskId IN (SELECT ts.[TaskId]
    FROM [Scheduling].[Task] t with(nolock)
    JOIN [Scheduling].[Trigger] tr ON t.[TriggerId] = tr.[Id]
    JOIN [Scheduling].[TaskState] ts ON ts.[TaskId] = t.[Id]
    LEFT JOIN [Scheduling].[TaskCategory] tc ON tc.[Id] = t.[CategoryId]
    JOIN [Scheduling].[TaskType] tt ON t.[TypeId] = tt.[Id]
    WHERE tt.[Id] IN ('D81C1197-D486-4FB7-AF8C-078C110893A0', '55D3F71A-2618-4EAE-9AA6-D48767B974D8'))
    PRINT 'Enable integration tasks, RunImmediately'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 1, StartBoundary = '1900-01-01' 
    WHERE Id in (SELECT [id] from @triggerIds WHERE taskTypeId = '55D3F71A-2618-4EAE-9AA6-D48767B974D8')
    PRINT 'Enable the Maintenance Task'
    UPDATE [Scheduling].[Trigger] SET IsEnabled = 1, RunImmediately = 0, StartBoundary = GETDATE() WHERE Id in
    (SELECT [id] from @triggerIds WHERE taskTypeId = 'D81C1197-D486-4FB7-AF8C-078C110893A0')
    ------------------------------------------
    ------------------------------------------
    ```

6. <span data-ttu-id="66b5b-234">Nach dem Zurücksetzen können Sie das Neuladen der Daten manuell prüfen, indem Sie in der Abfrage für die Rechnungslegungsdatenbank ausführen.</span><span class="sxs-lookup"><span data-stu-id="66b5b-234">After the reset, you can manually verify the data reload by running the following query against the Financial reporting database.</span></span>

    ```
    select ReaderObjectName, WriterObjectName, LastRunTime, StateType from Connector.MapsWithDetail with (nolock)
    ```

    <span data-ttu-id="66b5b-235">Bestätigen Sie, ob alle Zeilen **LastRunTime** einen Wert angeben und dass **StateType** auf **5** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="66b5b-235">Confirm that all rows have a **LastRunTime** value, and that **StateType** is set to **5**.</span></span> <span data-ttu-id="66b5b-236">Ein **StateType**-Wert **5** gibt an, dass die Daten erfolgreich erneut geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="66b5b-236">A **StateType** value of **5** indicates that the data was successfully reloaded.</span></span> <span data-ttu-id="66b5b-237">Ein Wert von **7** wird ein falsches Bundesland angezeigt.</span><span class="sxs-lookup"><span data-stu-id="66b5b-237">A value of **7** indicates a faulted state.</span></span> <span data-ttu-id="66b5b-238">Manchmal hat die Organisationshierarchiezuordnung dieses Status das erste Mal, wenn sie ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66b5b-238">Sometimes, the Organization Hierarchy map has this state the first time that it runs.</span></span> <span data-ttu-id="66b5b-239">Allerdings sollte das bemängelte Bundesland jedoch automatisch gelöst werden.</span><span class="sxs-lookup"><span data-stu-id="66b5b-239">However, the faulted state but should be automatically resolved.</span></span>
