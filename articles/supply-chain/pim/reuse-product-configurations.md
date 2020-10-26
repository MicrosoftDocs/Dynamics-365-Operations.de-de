---
title: Produktkonfigurationen wiederverwenden
description: Sie können angeben, dass Sie eine Variante für ein Produkt automatisch recyceln möchten. Wenn der Benutzer eine Konfigurationssitzung beendet hat, prüft das System, ob eine Konfiguration, die mit der Auswahl des Benutzers übereinstimmt, bereits vorhanden ist. Wenn eine übereinstimmende Variante gefunden wird, werden die Konfigurationskennung, die korrekte Stückliste (BOM) und der Arbeitsplan recycelt.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd6d730528522f4074b6e2a3ce6059cc12ff5a0f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984752"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="be3ee-105">Produktkonfigurationen wiederverwenden</span><span class="sxs-lookup"><span data-stu-id="be3ee-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be3ee-106">Sie können angeben, dass Sie eine Variante für ein Produkt automatisch recyceln möchten.</span><span class="sxs-lookup"><span data-stu-id="be3ee-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="be3ee-107">Wenn der Benutzer eine Konfigurationssitzung beendet hat, prüft das System, ob eine Konfiguration, die mit der Auswahl des Benutzers übereinstimmt, bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="be3ee-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="be3ee-108">Wenn eine übereinstimmende Variante gefunden wird, werden die Konfigurationskennung, die korrekte Stückliste (BOM) und der Arbeitsplan recycelt.</span><span class="sxs-lookup"><span data-stu-id="be3ee-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="be3ee-109">Anforderungen für die Wiederverwendung von Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="be3ee-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="be3ee-110">Damit Konfigurationen wieder verwendet werden können, müssen Sie die folgenden Informationen für die Komponenten und Attribute auf der Seite **Produktkonfigurationsmodelldetails** angeben:</span><span class="sxs-lookup"><span data-stu-id="be3ee-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="be3ee-111">**Komponenten und Unterkomponenten** – Wählen Sie im Inforegister**Allgemein** im Feld **Konfiguration wiederverwenden** **Ja**.</span><span class="sxs-lookup"><span data-stu-id="be3ee-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="be3ee-112">**Attribute** – Auf dem Inforegister **Attribute** wählen Sie die Option **In Wiederverwendung einbeziehen** aus.</span><span class="sxs-lookup"><span data-stu-id="be3ee-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="be3ee-113">Diese Option wird nur angezeigt, wenn die zugehörige Komponente zur Wiederverwendung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="be3ee-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="be3ee-114">Wenn Sie keine Attribute zur Wiederverwendung auswählen, wird die Konfiguration immer recycelt, unabhängig von der Auswahl des Benutzers für eine Konfigurationssitzung.</span><span class="sxs-lookup"><span data-stu-id="be3ee-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="be3ee-115">Die Attributwerte in der vorhandenen Konfiguration müssen der Auswahl des Benutzers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="be3ee-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="be3ee-116">Wenn der Benutzer zum Beispiel die Farbe **Blau** für eine Farbe während der Konfigurationssitzung auswählt, prüft das System, ob eine Variante der Komponente ein Attribut für die Farbe Blau hat.</span><span class="sxs-lookup"><span data-stu-id="be3ee-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="be3ee-117">Wiederverwendung der Konfiguration zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="be3ee-117">Resetting configuration reuse</span></span>
<span data-ttu-id="be3ee-118">Wenn Sie die Konfigurationswiederverwendung zurücksetzen, werden zuvor erstellte Konfigurationen nicht mehr berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="be3ee-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="be3ee-119">Sie wollen möglicherweise die Konfigurationswiederverwendung zurücksetzen, wenn die Stückliste oder der Arbeitsplan geändert aber keine entsprechenden Attribute geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="be3ee-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="be3ee-120">Sie können die Konfiguration auf dem Inforegister **Allgemeines** für die Komponente wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="be3ee-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>



