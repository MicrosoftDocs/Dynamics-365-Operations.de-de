---
title: Daten einer Tochtergesellschaft in Dateien exportieren
description: In diesem Thema wird erläutert, wie Sie den Export von Daten aus Microsoft Dynamics 365 Finance vorbereiten, und sie anschließend in eine konsolidierte juristische Person importieren.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 33c17cc2c1dcaa57244bf0bfaa661b11b221e2f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205498"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="f62c1-103">Daten einer Tochtergesellschaft in Dateien exportieren</span><span class="sxs-lookup"><span data-stu-id="f62c1-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f62c1-104">Verwenden Sie die **Exportieren**-Seite (**Systemverwaltung \> Arbeitsbereiche \> Importieren/Exportieren**) zur Vorbereitung des Exports von Daten einer Tochtergesellschaft in Dateien, die dann in eine konsolidierte juristische Person importiert werden können.</span><span class="sxs-lookup"><span data-stu-id="f62c1-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="f62c1-105">Weitere Informationen über die Import- und Exportprozesse finden Sie unter [Übersicht über Einzelvorgänge für Datenimport und ‑export](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="f62c1-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="f62c1-106">Erstellen Sie eine juristische Person für den Konsolidierungsprozess.</span><span class="sxs-lookup"><span data-stu-id="f62c1-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="f62c1-107">Informationen zum Erstellen juristischer Personen finden Sie unter [Eine juristische Person erstellen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="f62c1-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="f62c1-108">Weitere Informationen finden Sie unter [Eine juristische Person für den Konsolidierungsprozess vorbereiten](prepare-company-for-consolidation.md) und [Eine juristische Person vom Typ Tochtergesellschaft zur Konsolidierung einrichten](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="f62c1-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="f62c1-109">Rufen Sie **Konsolidierungen \> Unternehmenssalden exportieren** auf.</span><span class="sxs-lookup"><span data-stu-id="f62c1-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="f62c1-110">Geben Sie auf der Registerkarte **Kriterien** der Seite **Unternehmenssalden exportieren** die Details der Konsolidierung an, indem Sie die folgenden Felder festlegen.</span><span class="sxs-lookup"><span data-stu-id="f62c1-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="f62c1-111">Feld</span><span class="sxs-lookup"><span data-stu-id="f62c1-111">Field</span></span>                             | <span data-ttu-id="f62c1-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f62c1-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="f62c1-113">Hauptkonto</span><span class="sxs-lookup"><span data-stu-id="f62c1-113">Main account</span></span>                      | <span data-ttu-id="f62c1-114">Geben Sie die zu konsolidierenden Konten an.</span><span class="sxs-lookup"><span data-stu-id="f62c1-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="f62c1-115">Lassen Sie dieses Feld leer, um alle Konten einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f62c1-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="f62c1-116">Konsolidierungskonto verwenden</span><span class="sxs-lookup"><span data-stu-id="f62c1-116">Use consolidation account</span></span>         | <span data-ttu-id="f62c1-117">Wenn Sie Konsolidierungskonten angegeben haben, setzen Sie diese Option auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f62c1-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="f62c1-118">Konsolidierungskonto auswählen aus</span><span class="sxs-lookup"><span data-stu-id="f62c1-118">Select consolidation account from</span></span> | <span data-ttu-id="f62c1-119">Wählen Sie entweder **Hauptkonto** oder **Konsolidierungskontengruppe** aus.</span><span class="sxs-lookup"><span data-stu-id="f62c1-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="f62c1-120">Konsolidierungskontogruppe</span><span class="sxs-lookup"><span data-stu-id="f62c1-120">Consolidation account group</span></span>       | <span data-ttu-id="f62c1-121">Wählen Sie eine Konsolidierungskontengruppe für das ausgewählte Konsolidierungskonto aus.</span><span class="sxs-lookup"><span data-stu-id="f62c1-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="f62c1-122">Konsolidierungsperiode</span><span class="sxs-lookup"><span data-stu-id="f62c1-122">Consolidation period</span></span>              | <span data-ttu-id="f62c1-123">Geben Sie einen „Von – Bis“–Datumsbereich für die Konsolidierung an.</span><span class="sxs-lookup"><span data-stu-id="f62c1-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="f62c1-124">Istbeträge einbeziehen</span><span class="sxs-lookup"><span data-stu-id="f62c1-124">Include actual amounts</span></span>            | <span data-ttu-id="f62c1-125">Setzen Sie diese Option auf **Ja**, um tatsächliche Beträge einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f62c1-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="f62c1-126">Budgetbeträge einbeziehen</span><span class="sxs-lookup"><span data-stu-id="f62c1-126">Include budget amounts</span></span>            | <span data-ttu-id="f62c1-127">Setzen Sie diese Option auf **Ja**, um Budgetbeträge in Konsolidierungen einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="f62c1-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="f62c1-128">Budgetmodelle</span><span class="sxs-lookup"><span data-stu-id="f62c1-128">Budget models</span></span>                     | <span data-ttu-id="f62c1-129">Geben Sie das einzuschließende Budgetmodell an.</span><span class="sxs-lookup"><span data-stu-id="f62c1-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="f62c1-130">Geben Sie auf der Registerkarte **Finanzdimensionen** die Details der Konsolidierung an:</span><span class="sxs-lookup"><span data-stu-id="f62c1-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="f62c1-131">Geben Sie die Informationen zu den Finanzdimensionen an, die aus den Buchungen in den Konten der Tochtergesellschaften in die Buchungen der konsolidierten juristischen Person übertragen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f62c1-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="f62c1-132">Wählen Sie die Finanzdimensionen in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="f62c1-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="f62c1-133">Identifizieren Sie die richtige Spezifikation für jede konsolidierte Finanzdimension.</span><span class="sxs-lookup"><span data-stu-id="f62c1-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="f62c1-134">Die verfügbaren Optionen umfassen **Dimension**, **Gruppendimension**, **Unternehmenskonten** und **Konto**.</span><span class="sxs-lookup"><span data-stu-id="f62c1-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="f62c1-135">Mithilfe der Option **Gruppendimension** können Sie den Dimensionswert definieren, der von der Unternehmensgruppe verwendet wird, die konsolidiert wird.</span><span class="sxs-lookup"><span data-stu-id="f62c1-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="f62c1-136">Geben Sie die Segmentreihenfolge an, in der konsolidiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f62c1-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="f62c1-137">Führen Sie die folgenden Schritte auf der Registerkarte **Juristische Personen** aus, um die zu exportierende juristische Person anzugeben:</span><span class="sxs-lookup"><span data-stu-id="f62c1-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="f62c1-138">Wählen Sie **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f62c1-138">Select **New**.</span></span>
    2. <span data-ttu-id="f62c1-139">Geben Sie im Feld **Juristische Person der Quelle** die juristische Person ein.</span><span class="sxs-lookup"><span data-stu-id="f62c1-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="f62c1-140">Gelten für mehrere Tochtergesellschaften, die sich in derselben Datenbank befinden, die gleichen Kriterien, können Sie die Daten dieser Tochtergesellschaften in einem einzigen Schritt in verschiedene Exportdateien übertragen:</span><span class="sxs-lookup"><span data-stu-id="f62c1-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="f62c1-141">Erstellen Sie für jede Tochtergesellschaft, deren Konten in Dateien exportiert werden sollen, eine Position.</span><span class="sxs-lookup"><span data-stu-id="f62c1-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="f62c1-142">Diese Dateien werden später in die konsolidierte juristische Person importiert.</span><span class="sxs-lookup"><span data-stu-id="f62c1-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="f62c1-143">Geben Sie für jede Tochtergesellschaft den Namen der Tochtergesellschaft sowie den Namen der Exportdatei ein, die im Zuge des Exportvorgangs erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f62c1-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="f62c1-144">Wählen Sie im Feld **Kontenart für Konvertierungsdifferenzen** die Option **Gewinn und Verlust** oder **Bilanz** aus.</span><span class="sxs-lookup"><span data-stu-id="f62c1-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="f62c1-145">Geben Sie einen Dateinamen für die zu erstellende Exportdatei ein.</span><span class="sxs-lookup"><span data-stu-id="f62c1-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="f62c1-146">Wählen Sie zum Ausführen des Exports **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f62c1-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="f62c1-147">Nach Abschluss des Exports erhalten Sie eine Meldung mit der Anzahl der in den einzelnen Dateien gespeicherten Datensätze.</span><span class="sxs-lookup"><span data-stu-id="f62c1-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="f62c1-148">Sie können die Dateien dann in die konsolidierte juristische Person importieren.</span><span class="sxs-lookup"><span data-stu-id="f62c1-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]