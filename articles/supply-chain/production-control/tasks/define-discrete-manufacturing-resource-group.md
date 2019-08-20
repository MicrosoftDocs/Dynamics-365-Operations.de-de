---
title: Ressourcengruppe für einzelne Fertigung definieren
description: Eine Ressourcengruppe ist ein Satz betriebliche Ressourcen, die üblicherweise der physischen Organisation von Arbeitsgruppen entsprechen, definiert durch gelbe Positionen im Fertigungsbereich.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40a0638662cbace147aeb24bd20d3ae34a0c1670
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837662"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="4c9bd-103">Ressourcengruppe für einzelne Fertigung definieren</span><span class="sxs-lookup"><span data-stu-id="4c9bd-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4c9bd-104">Eine Ressourcengruppe ist ein Satz betriebliche Ressourcen, die üblicherweise der physischen Organisation von Arbeitsgruppen entsprechen, definiert durch gelbe Positionen im Fertigungsbereich.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="4c9bd-105">Diese Prozedur zeigt Ihnen, wie eine Ressourcengruppe für die Verwendung in der einzelnen Produktion definiert wird.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="4c9bd-106">Sie können diese Prozedur Schritt für Schritt im Demodatenunternehmen USMF durchführen oder können Ihre eigenen Daten verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="4c9bd-107">Wechseln Sie zu "Ressourcengruppen".</span><span class="sxs-lookup"><span data-stu-id="4c9bd-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="4c9bd-108">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="4c9bd-108">Click New.</span></span>
3. <span data-ttu-id="4c9bd-109">Geben Sie im Feld "Ressourcengruppe" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="4c9bd-110">Geben Sie im Feld "Beschreibung" einen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4c9bd-111">Geben Sie im Feld "Standort" einen Wert ein, oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="4c9bd-112">Geben Sie im Feld "Produktionseinheit" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="4c9bd-113">Definieren von standardmäßigen betriebliche Parametern</span><span class="sxs-lookup"><span data-stu-id="4c9bd-113">Define default operational parameters</span></span>
1. <span data-ttu-id="4c9bd-114">Erweitern Sie den Abschnitt "Arbeitstang".</span><span class="sxs-lookup"><span data-stu-id="4c9bd-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="4c9bd-115">Geben Sie im Feld "Ausschuss" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="4c9bd-116">Geben Sie im Feld "Rüstkostenkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="4c9bd-117">Geben Sie im Feld "Ausführungszeitkategorie" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="4c9bd-118">Geben Sie im Feld "Grobterminierungsprozentsatz" eine Zahl ein.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="4c9bd-119">Definieren von Betriebszeiten</span><span class="sxs-lookup"><span data-stu-id="4c9bd-119">Define operating hours</span></span>
1. <span data-ttu-id="4c9bd-120">Erweitern Sie den Abschnitt "Kalender".</span><span class="sxs-lookup"><span data-stu-id="4c9bd-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="4c9bd-121">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-121">Click Add.</span></span>
3. <span data-ttu-id="4c9bd-122">Geben Sie im Feld "Kalender" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="4c9bd-123">Betriebliche Ressourcen hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4c9bd-123">Add operations resources</span></span>
1. <span data-ttu-id="4c9bd-124">Erweitern Sie den Abschnitt "Ressourcen".</span><span class="sxs-lookup"><span data-stu-id="4c9bd-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="4c9bd-125">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-125">Click Add.</span></span>
3. <span data-ttu-id="4c9bd-126">Geben Sie im Feld "Ressource" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="4c9bd-127">Klicken Sie auf Hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-127">Click Add.</span></span>
5. <span data-ttu-id="4c9bd-128">Geben Sie im Feld "Ressource" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="4c9bd-129">Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4c9bd-130">Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.</span><span class="sxs-lookup"><span data-stu-id="4c9bd-130">In the list, click the link in the selected row.</span></span>

