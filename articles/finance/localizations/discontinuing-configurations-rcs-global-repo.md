---
title: Konfigurationen im RCS Global-Repository einstellen
description: In diesem Thema wird beschrieben, wie Sie Konfigurationen im RCS Global-Repository beenden.
author: JaneA07
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 35d0af91161d898b09557a83913019609c71e836
ms.sourcegitcommit: e9d19f25e64cf4d1c1d07c8031a7081454a6f79e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2021
ms.locfileid: "5474247"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="3c216-103">Konfigurationen im RCS Global-Repository einstellen</span><span class="sxs-lookup"><span data-stu-id="3c216-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c216-104">In diesem Thema wird beschrieben, wie Sie eine Konfiguration im RCS Global-Repository beenden.</span><span class="sxs-lookup"><span data-stu-id="3c216-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="3c216-105">Bisher konnten nur nicht mehr benötigte Konfigurationen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3c216-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="3c216-106">Jetzt können Sie jedoch eine freigegebene Konfiguration im RCS Global-Repository als **Eingestellt** markieren.</span><span class="sxs-lookup"><span data-stu-id="3c216-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="3c216-107">Darüber hinaus können Sie mit dieser Funktion auch Folgendes durchführen:</span><span class="sxs-lookup"><span data-stu-id="3c216-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="3c216-108">Stellen Sie im Voraus Benachrichtigungen bereit, wenn die Einstellung einer Konfiguration geplant ist.</span><span class="sxs-lookup"><span data-stu-id="3c216-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="3c216-109">Geben Sie die entsprechenden Details zur Ersatzkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="3c216-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="3c216-110">Legen Sie ein **Unterstützt bis**-Datum für die spezifische Konfiguration fest, um den Benutzer darüber zu informieren, wann sie eingestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c216-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="3c216-111">Wenn Sie eine Konfigurationsversion beenden, können Sie die folgenden optionalen Informationen angeben:</span><span class="sxs-lookup"><span data-stu-id="3c216-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="3c216-112">**Ersatzkonfiguration**</span><span class="sxs-lookup"><span data-stu-id="3c216-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="3c216-113">**Ersatzkonfigurationsversion**</span><span class="sxs-lookup"><span data-stu-id="3c216-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="3c216-114">**Freitextnotiz**: Verwenden Sie dieses Feld, um Dokumentationslinks oder Referenzen bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="3c216-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="3c216-115">**Unterstützt bis**: Dieses Feld enthält das vorgeschlagene Datum, bis zu dem die aktuelle Konfiguration/Version unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="3c216-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="3c216-116">Dieses Datum muss manuell aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c216-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="3c216-117">Führen Sie die folgenden Schritte aus, um die Konfiguration einzustellen.</span><span class="sxs-lookup"><span data-stu-id="3c216-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="3c216-118">Wählen Sie aus, ob Sie eine einzelne Version oder alle Versionen mit denselben Einstellungen in einem Vorgang beenden möchten, indem Sie **Alle Versionen** auf **Ja** festlegen.</span><span class="sxs-lookup"><span data-stu-id="3c216-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="3c216-119">Stellen Sie den Parameter **Nicht fortsetzen** auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3c216-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="3c216-120">Wählen Sie **OK** aus, um die Konfigurationen abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="3c216-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="3c216-121">Das Feld **Aufgabedatum** wird ausgefüllt, wenn Sie die Änderungen speichern.</span><span class="sxs-lookup"><span data-stu-id="3c216-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Konfigurationsinformationen beenden](media/Discontinue-details-2.png)
  
<span data-ttu-id="3c216-123">Sie können die Konfiguration auf **Freigegeben** zurücksetzen oder die Abbruchinformationen jederzeit anpassen.</span><span class="sxs-lookup"><span data-stu-id="3c216-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="3c216-124">Wenn Sie eine Konfiguration freigeben, geben Sie das Datum **Unterstützt bis** und alle anderen Informationen im Zusammenhang mit der Einstellung an, um Ihre Pläne für eine zukünftige Einstellung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3c216-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="3c216-125">Wenn Sie Informationen über eine geplante Einstellung teilen möchten, bevor Sie die Konfiguration tatsächlich einstellen, kann der Benutzer alle Felder im Zusammenhang mit dem Ersetzen vorab ausfüllen, aber den Parameter **Nicht fortsetzen** auf **Nein** belassen.</span><span class="sxs-lookup"><span data-stu-id="3c216-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="3c216-126">Die Einstellung schränkt Vorgänge mit Konfigurationen nicht ein.</span><span class="sxs-lookup"><span data-stu-id="3c216-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="3c216-127">Sie können die Konfigurationen weiterhin importieren, ausführen oder ableiten. Diese Felder dienen nur zur Information.</span><span class="sxs-lookup"><span data-stu-id="3c216-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="3c216-128">Finance unterstützt die Anzeige dieser Informationen ab Version 10.0.14</span><span class="sxs-lookup"><span data-stu-id="3c216-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="3c216-129">Dynamics 365 Finance unterstützt die Anzeige von Einstellungsinformationen ab Version 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="3c216-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="3c216-130">Auf der Seite **Globales Repository** können Sie aktuelle Informationen zur Einstellung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3c216-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="3c216-131">Standardmäßig werden nicht mehr verfügbare Konfigurationen herausgefiltert.</span><span class="sxs-lookup"><span data-stu-id="3c216-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="3c216-132">Auf der Seite **Importierte Konfigurationen** (ERSolutionTable) werden Konfigurationen angezeigt, die beim Import bereits eingestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="3c216-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="3c216-133">Für die Konfigurationen, die nach dem Import eingestellt wurden, können die Abbruchinformationen durch Ausführen von **Konfigurationsaktualisierungen importieren** synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="3c216-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


