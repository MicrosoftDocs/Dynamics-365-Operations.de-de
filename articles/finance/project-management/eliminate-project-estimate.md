---
title: Beseitigen Sie eine Projektschätzung
description: Dieses Thema enthält Informationen zum Entfernen einer Projektschätzung nach deren Abschluss.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410222"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="612df-103">Beseitigen Sie eine Projektschätzung</span><span class="sxs-lookup"><span data-stu-id="612df-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="612df-104">Projektschätzungen liefern die Finanzansicht für Arbeiten, die für ein Projekt geschätzt und geplant werden.</span><span class="sxs-lookup"><span data-stu-id="612df-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="612df-105">Wenn Sie mit Vorkalkulationen für ein Projekt arbeiten möchten, müssen Sie das Projekt einem Vorkalkulationsprojekt zuordnen.</span><span class="sxs-lookup"><span data-stu-id="612df-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="612df-106">Ein Vorkalkulationsprojekt basiert stets auf einem vorhandenen Projekt, aber mehrere Projekte können sich auf ein einzelnes Vorkalkulationsprojekt beziehen.</span><span class="sxs-lookup"><span data-stu-id="612df-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="612df-107">Nur Festpreis- und Investitionsprojekte können Vorkalkulationsprojekten angehängt werden, und diese Projekte müssen zur gleichen Projektgruppe gehören wie das Vorkalkulationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="612df-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="612df-108">Ein Vorkalkulationsprojekt kann nur gelöscht werden, wenn es vollständig abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="612df-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="612df-109">In den folgenden Schritten wird erläutert, wie Sie eine Schätzung entfernen.</span><span class="sxs-lookup"><span data-stu-id="612df-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="612df-110">Wechseln Sie zu **Projektverwaltung und -verrechnung** > **Alle Projekte** und öffnen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="612df-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="612df-111">Auf der Registerkarte **Verwalten** wählen Sie **Schätzungen** und auf der Seite **Schätzung** wählen Sie **Beseitigen**.</span><span class="sxs-lookup"><span data-stu-id="612df-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="612df-112">Auf der **Schätzung eliminieren** Seite auf der Registerkarte **Allgemein** legen Sie die folgenden Optionen fest:</span><span class="sxs-lookup"><span data-stu-id="612df-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="612df-113">**Periodencode**: Wählen Sie den Periodencode zum Auswählen der entsprechenden Vorkalkulationsprojekte aus.</span><span class="sxs-lookup"><span data-stu-id="612df-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="612df-114">**Geschätztes Datum**: Wählen Sie das entsprechende Vorkalkulationsdatum für den Löschvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="612df-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="612df-115">**Beseitigen mit WIP-Warnungen**: Aktivieren Sie diese Option, um eine Benachrichtigung bereitzustellen, wenn ein Kostenvoranschlag, der mit einer laufenden Arbeit (WIP) verknüpft ist, entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="612df-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="612df-116">Ist das Kontrollkästchen deaktiviert, kann der Löschvorgang nicht fortgesetzt werden, wenn Buchungen ohne Vorkalkulation vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="612df-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="612df-117">Diese Option steht nur zur Verfügung, wenn die Löschung auf ein Vorkalkulationsprojekt angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="612df-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="612df-118">Bei Verwendung periodischer Buchungen ist es nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="612df-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="612df-119">Diese Einstellung funktioniert mit den Einstellungen auf der **Schätzen** Registerkarte auf der **Projektparameter** Seite, in der Feldgruppe **Ermöglichen Sie die Eliminierung, wenn nicht geschätzte Transaktionen vorhanden sind**.</span><span class="sxs-lookup"><span data-stu-id="612df-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="612df-120">**Phase auf Beendet stellen**: Aktivieren Sie diese Option, um die Phase des Vorkalkulationsprojektes auf **Beendet** festzusetzen, nachdem Sie die Eliminierung ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="612df-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="612df-121">**Vorkalkulationsliste drucken**: Wählen Sie die Informationen aus, die beim Drucken der Vorkalkulationsprojektliste eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="612df-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="612df-122">**Infolog anzeigen**: Aktivieren Sie diese Option, um den Infolog anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="612df-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="612df-123">**Buchungsdatum** : Wählen Sie das Buchungsdatum des Kostenvoranschlags.</span><span class="sxs-lookup"><span data-stu-id="612df-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="612df-124">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="612df-124">Select **OK**.</span></span>
5. <span data-ttu-id="612df-125">Nach Abschluss des Eliminierungsprozesses wird das eliminierte Schätzprojekt mit einem negativen Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="612df-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="612df-126">Wenn Sie nicht vorhatten, eine Schätzung zu entfernen, können Sie die eliminierte Schätzung **Schätzung wiederherstellen** wählen.</span><span class="sxs-lookup"><span data-stu-id="612df-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
