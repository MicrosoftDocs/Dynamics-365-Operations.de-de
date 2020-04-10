---
title: ISO20022-Direktbelastungskonfiguration importieren
description: Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Debitorenzahlung importieren.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e5d4256b155d3e06d63e425fab63b4025ef2577f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140017"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="a12ca-103">ISO20022-Direktbelastungskonfiguration importieren</span><span class="sxs-lookup"><span data-stu-id="a12ca-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a12ca-104">Dieses Verfahren zeigt, wie Sie eine Berichterstellungskonfiguration der elektronische Debitorenzahlung importieren.</span><span class="sxs-lookup"><span data-stu-id="a12ca-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="a12ca-105">Diese Verfahren verwendet das ISO 20022-Direktbelastungsformat als Beispiel.</span><span class="sxs-lookup"><span data-stu-id="a12ca-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="a12ca-106">Dieses Verfahren wurde mithilfe des Demodatunternehmens DEMF erstellt, doch es kann ein beliebiges Demodatunternehmen verwenden, um diese Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a12ca-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="a12ca-107">Dies ist die erste von sechs Aufgaben, die das Verfahren für Debitorenzahlungen über elektronischen Berichterstellungskonfigurationen zeigen.</span><span class="sxs-lookup"><span data-stu-id="a12ca-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="a12ca-108">Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.</span><span class="sxs-lookup"><span data-stu-id="a12ca-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a12ca-109">Wählen Sie als Konfigurationsanbieter "Microsoft".</span><span class="sxs-lookup"><span data-stu-id="a12ca-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="a12ca-110">Klicken Sie auf "Als aktiv festlegen"</span><span class="sxs-lookup"><span data-stu-id="a12ca-110">Click Set active.</span></span>
4. <span data-ttu-id="a12ca-111">Klicken Sie auf Repositorys.</span><span class="sxs-lookup"><span data-stu-id="a12ca-111">Click Repositories.</span></span>
5. <span data-ttu-id="a12ca-112">Klicken Sie auf "Öffnen".</span><span class="sxs-lookup"><span data-stu-id="a12ca-112">Click Open.</span></span>
6. <span data-ttu-id="a12ca-113">Klicken Sie auf "Filter anzeigen".</span><span class="sxs-lookup"><span data-stu-id="a12ca-113">Click Show filters.</span></span>
7. <span data-ttu-id="a12ca-114">Wenden Sie die nachfolgenden Filter an: Geben Sie einen Filterwert für "ISO20022 Direktbelastung (DE)" im Feld " Konfigurationsname" unter Verwendung des "begins with"-Filteroperators ein</span><span class="sxs-lookup"><span data-stu-id="a12ca-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="a12ca-115">Optional können Sie die Konfiguration in der Liste aufrufen, sie auswählen und diesen Schritt übergehen.</span><span class="sxs-lookup"><span data-stu-id="a12ca-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="a12ca-116">Klicken Sie auf Import.</span><span class="sxs-lookup"><span data-stu-id="a12ca-116">Click Import.</span></span>
    * <span data-ttu-id="a12ca-117">Wenn die Importschaltfläche nicht verfügbar ist, bedeutet dies, dass die Konfiguration bereits importiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a12ca-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="a12ca-118">Klicken Sie auf "Ja".</span><span class="sxs-lookup"><span data-stu-id="a12ca-118">Click Yes.</span></span>

