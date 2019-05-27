---
title: ISO20022-Banküberweisungskonfiguration importieren
description: Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Kreditorenzahlung importieren.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fbd2e39f488696ebe8db5579ed88595e246ce97
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573116"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="76638-103">ISO20022-Banküberweisungskonfiguration importieren</span><span class="sxs-lookup"><span data-stu-id="76638-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76638-104">Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Kreditorenzahlung importieren.</span><span class="sxs-lookup"><span data-stu-id="76638-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="76638-105">Das deutsche ISO 20022-Banküberweisungsformat wird als Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="76638-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="76638-106">Diese Prozedur kann für andere verfügbare elektronisches Berichterstellungsformat verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="76638-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="76638-107">Diese Aufgabe wurde mithilfe des Demodatunternehmens DEMF erstellt, doch es kann ein beliebiges Demodatunternehmen verwenden, um diese Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="76638-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="76638-108">Dies ist der erste von fünf Aufgaben, die das Verfahren für Kreditorenzahlung über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="76638-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="76638-109">Diese Prozedur ist eine Funktion, für die in Dynamics 365 for Operations Version 1611 hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="76638-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="76638-110">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="76638-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="76638-111">Wählen Sie als Konfigurationsanbieter "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="76638-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="76638-112">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="76638-112">Click Set active.</span></span>
4. <span data-ttu-id="76638-113">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="76638-113">Click Repositories.</span></span>
5. <span data-ttu-id="76638-114">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="76638-114">Click Open.</span></span>
6. <span data-ttu-id="76638-115">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="76638-115">Click Show filters.</span></span>
7. <span data-ttu-id="76638-116">Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert für "ISO20022 Kreditübertragung (DE)" im Feld " Konfigurationsname" unter Verwendung des "begins with"-Filteroperators ein</span><span class="sxs-lookup"><span data-stu-id="76638-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="76638-117">Oder Sie suchen die Konfiguration in der Liste, wählen diese aus und verschieben sie zur Importaufgabe.</span><span class="sxs-lookup"><span data-stu-id="76638-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="76638-118">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="76638-118">Click Import.</span></span>
    * <span data-ttu-id="76638-119">Wenn die Importschaltfläche nicht verfügbar ist, bedeutet dies, dass die Konfiguration bereits importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="76638-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="76638-120">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="76638-120">Click Yes.</span></span>

