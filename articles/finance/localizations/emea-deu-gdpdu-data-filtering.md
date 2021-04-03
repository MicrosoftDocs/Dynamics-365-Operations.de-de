---
title: Hinzufügen von Filtern zu einer Audit-Datei-Konfiguration
description: In diesem Thema wird erklärt, wie Sie einen Datenfilter in der deutschen Audit-Datei hinzufügen können.
author: liza-golub
ms.date: 02/09/2021
ms.topic: article
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Germany
ms.author: elgolu
ms.openlocfilehash: 4adf4e51d1d4b47c06a005f16d13352c52153f0d
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557562"
---
# <a name="add-filters-to-an-audit-file-configuration"></a><span data-ttu-id="8b974-103">Hinzufügen von Filtern zu einer Audit-Datei-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8b974-103">Add filters to an audit file configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b974-104">Dieses Thema erklärt, wie Sie einen Filter für Daten in der deutschen Audit-Datei hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="8b974-104">This topic explains how to add a filter for data in the German audit file.</span></span> <span data-ttu-id="8b974-105">Sie können zum Beispiel einen Filter für das Feld **Buchungsebene** in der Tabelle **Allgemeiner Erfassungseintrag** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8b974-105">For example, you can add a filter for the **Posting layer** field in the **General journal entry** table.</span></span>

<span data-ttu-id="8b974-106">Wie in [Übersicht über die deutsche Prüfdatei (GDPdU/GoBD)](emea-deu-gdpdu-audit-data-export.md#sachkontobuchungen) erläutert, wird das Feld **SPEZIALBUCHUNG** (Buchungsschicht) des **Datensatzes Sachkontobuchungen** aus dem Datenquellenpfad **$GeneralJournalEntry/PostingLayer** für elektronische Meldungen gesammelt.</span><span class="sxs-lookup"><span data-stu-id="8b974-106">As explained in [German audit file (GDPdU/GoBD) overview](emea-deu-gdpdu-audit-data-export.md#sachkontobuchungen), the **SPEZIALBUCHUNG** (Posting layer) field of **Sachkontobuchungen** data set is collected from the **$GeneralJournalEntry/PostingLayer** electronic reporting data source path.</span></span> <span data-ttu-id="8b974-107">Um die Möglichkeit hinzuzufügen, Daten im Bericht nach dem Feld **SPEZIALBUCHUNG** (Buchungsschicht) zu filtern, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8b974-107">To add the possibility of filtering data in the report by the **SPEZIALBUCHUNG** (Posting layer) field, complete the following steps:</span></span>

1. <span data-ttu-id="8b974-108">Gehen Sie zu **Arbeitsbereiche** > **Elektronisches Berichtswesen**, und wählen Sie dann **Berichtskonfigurationen**.</span><span class="sxs-lookup"><span data-stu-id="8b974-108">Go to **Workspaces** > **Electronic reporting**, and then select **Reporting configurations**.</span></span>
2. <span data-ttu-id="8b974-109">Wählen Sie im Konfigurationsbaum die Konfiguration **Datenexportmodell** und leiten Sie sie ab, indem Sie ein Format erstellen, das in Ihrer Firma verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8b974-109">In the configuration tree, select the **Data export model** configuration, and derive it by creating a format that will be used in your company.</span></span>
3. <span data-ttu-id="8b974-110">Wählen Sie die abgeleitete Konfiguration aus und wählen Sie im Aktivitätsbereich **Designer**.</span><span class="sxs-lookup"><span data-stu-id="8b974-110">Select the derived configuration, and on the Action Pane, select **Designer**.</span></span> 
4. <span data-ttu-id="8b974-111">Wählen Sie auf der Seite **Datenmodell** im Aktivitätsbereich **Modell zu Datenquelle zuordnen**.</span><span class="sxs-lookup"><span data-stu-id="8b974-111">On the **Data model** page, on the Action Pane, select **Map model to datasource**.</span></span>
5. <span data-ttu-id="8b974-112">Wählen Sie auf der Seite **Modell zu Datenquelle zuordnen** die Definition **Gruppe**.</span><span class="sxs-lookup"><span data-stu-id="8b974-112">On the **Model to datasource mapping** page, select the **Group** definition.</span></span> <span data-ttu-id="8b974-113">Wählen Sie im Aktivitätsbereich **Designer** und suchen Sie dann auf der Seite **Modell-Mapping-Design** im Abschnitt **Datenquellen** die Datenquelle „$GeneralJournalEntry“.</span><span class="sxs-lookup"><span data-stu-id="8b974-113">On the Action Pane, select **Designer**, and then search for “$GeneralJournalEntry” data source in the **Data sources** section on the **Model mapping design** page.</span></span>

  <span data-ttu-id="8b974-114">Die Datenquelle „$GeneralJournalEntry“ ist eine berechnete Datensatzliste, die Daten aus der Tabelle **GeneralJournalEntry** bezieht (dies können Sie an der Formel für „$GeneralJournalEntry“ erkennen).</span><span class="sxs-lookup"><span data-stu-id="8b974-114">“$GeneralJournalEntry” data source is a calculated record list that sources data from the **GeneralJournalEntry** table (this can be observed from the formula for “$GeneralJournalEntry”).</span></span>
  
6. <span data-ttu-id="8b974-115">Suchen Sie im Bereich **Datenquellen** auf der Seite **Modellzuordnungsdesign** nach **GeneralJournalEntry** und wählen Sie diese Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="8b974-115">In the **Data sources** section on the **Model mapping design** page, search for **GeneralJournalEntry** and select this table.</span></span>
7. <span data-ttu-id="8b974-116">Wählen Sie im Abschnitt **Datenquellen** die Option **Bearbeiten** und aktivieren Sie dann das Kontrollkästchen **Abfrage anfordern** für die Tabelle **GeneralJournalEntry**.</span><span class="sxs-lookup"><span data-stu-id="8b974-116">In the **Data sources** section, select **Edit** and then select the **Ask for query** check box for the **GeneralJournalEntry** table.</span></span> <span data-ttu-id="8b974-117">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b974-117">Select **OK**.</span></span>

![Aktivieren Sie das Kontrollkästchen Abfrage für die Tabelle Allgemeine Hauptbucheinträge](media/ask-for-query-gl-entries.png)

8. <span data-ttu-id="8b974-119">Speichern, schließen und schließen Sie die Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="8b974-119">Save, close, and complete the configuration.</span></span>
9. <span data-ttu-id="8b974-120">Deaktivieren Sie den Parameter **Standard für Modellzuordnung** für die übergeordnete Konfiguration, **Datenexportmodell**, falls er markiert war.</span><span class="sxs-lookup"><span data-stu-id="8b974-120">Unmark the **Default for model mapping** parameter for the parent configuration, **Data export model**, if it was marked.</span></span> <span data-ttu-id="8b974-121">Wählen Sie Ihre abgeleitete Konfiguration als **Standard für die Modellzuordnung**.</span><span class="sxs-lookup"><span data-stu-id="8b974-121">Select your derived configuration as **Default for model mapping**.</span></span> 

<span data-ttu-id="8b974-122">Mit dieser Änderung sehen Sie beim Ausführen von **Datenexport** periodischen Aufgaben **Einzuschließende Datensätze** auf der Inforegister-Registerkarte im Dialogfeld für den Bericht für die Tabelle **Allgemeine Erfassung**.</span><span class="sxs-lookup"><span data-stu-id="8b974-122">With this change, when you run **Data export** periodic tasks, you will see **Records to include** on the FastTab in the dialog box for the report for the **General journal entry** table.</span></span> <span data-ttu-id="8b974-123">Wählen Sie **Filter**, um Bedingungen für das Filtern von Hauptbucheinträgen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8b974-123">Select **Filter** to specify conditions for general ledger entries filtering.</span></span>

![Filterbedingungen für den periodischen Datenexport einrichten](media/filter-setup.png)

<span data-ttu-id="8b974-125">Um nach dem Feld **Buchungsebene** in der Tabelle **Allgemeine Erfassungsbuchung** zu filtern, wählen Sie **Buchungsebene** in der Spalte **Feld** und dann die erforderliche Buchungsebene in der Spalte **Kriterien**.</span><span class="sxs-lookup"><span data-stu-id="8b974-125">To filter by the **Posting layer** field in the **General journal entry** table, select **Posting layer** in the **Field** column, and then select the necessary posting layer in the **Criteria** column.</span></span>
