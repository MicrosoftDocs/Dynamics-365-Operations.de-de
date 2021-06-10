---
title: Talent mit Power Apps und Power Automate erweitern
description: Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Human Resources, die Microsoft Power Apps und Microsoft Power Automate verwenden.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5b1ebe17063d954b52a0607d39e3ea08518adb89
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057597"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="2f738-103">Mit Power Apps und Power Automate erweitern</span><span class="sxs-lookup"><span data-stu-id="2f738-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2f738-104">Dieser Artikel beschreibt einige Beispiele für Erweiterungsszenarien für Microsoft Dynamics 365 Human Resources, die Microsoft Power Apps und Microsoft Power Automate verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f738-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="2f738-105">Sie können das Lösungspaket importieren, das jedem Beispiel in der Power Apps-Umgebung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2f738-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="2f738-106">Sie können entweder die Pakete als Anleitung oder als Startpunkte zu den Werkzeugszenarien verwenden, die der Organisation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2f738-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f738-107">Wenn Sie die Vorlagen und Apps verwenden möchten, die in diesem Thema als „wie vorliegend“ beschrieben sind, müssen Sie diese unbedingt testen, um sicherzustellen, dass sie alle Szenarien beinhalten, die für Ihre Implementierung bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="2f738-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2f738-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="2f738-108">Prerequisites</span></span>

- <span data-ttu-id="2f738-109">Um Pakete zu importieren, müssen Benutzer die Berechtigung **Umgebungs-Hersteller** haben.</span><span class="sxs-lookup"><span data-stu-id="2f738-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="2f738-110">Um Apps zu exportierenden oder zu importieren, müssen Benutzer eine Lizenz für Power Apps Plan 2 oder eine Testlizenz für Power Apps-Plan 2 haben.</span><span class="sxs-lookup"><span data-stu-id="2f738-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="2f738-111">Integration in Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="2f738-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="2f738-112">Die **Integration in Microsoft 365**-App kann verwendet werden, um Teaminformationen für angemeldete Benutzer von Microsoft 365 zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2f738-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="2f738-113">Es verweist auf Arbeitskräfte in Human Resources, um Mitarbeiteridentifikationstypen zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2f738-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="2f738-114">Manager können das Ablaufdatum von Mitarbeiter-ID-Typen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="2f738-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="2f738-115">Sie können auch eine E-Mail-Erinnerung senden, wenn der Typ der Mitarbeiter-ID abläuft.</span><span class="sxs-lookup"><span data-stu-id="2f738-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="2f738-116">Power Automate kann in Power Apps integriert werden, um diese Erinnerung zu senden.</span><span class="sxs-lookup"><span data-stu-id="2f738-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="2f738-117">Power Apps erhält eine Bestätigung von Power Automate, wenn die Erinnerung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f738-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="2f738-118">Zu den Identifikationstypen gehören Führerschein, Reisepass und andere zulässige Ausweispapiere.</span><span class="sxs-lookup"><span data-stu-id="2f738-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="2f738-119">Sie können diese App für andere Szenarien erweitern.</span><span class="sxs-lookup"><span data-stu-id="2f738-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="2f738-120">Sie können sie zum Beispiel verwenden, um Teamferieninformationen, Kalenderereignisse und weitere teamspezifische Ereignisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2f738-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="2f738-121">Um die App **Integration in Microsoft 365, Power Automate**-App herunterzuladen, wechseln Sie zu [Integration in Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) im Microsoft Download Center.</span><span class="sxs-lookup"><span data-stu-id="2f738-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="2f738-122">Power Automate - SQL Verbinden und ausführen</span><span class="sxs-lookup"><span data-stu-id="2f738-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="2f738-123">Die Vorlage **Power Automate - SQL Connect and execute** verbindet sich mit Microsoft SQL Server und ermöglicht die Ausführung von SQL-Abfragen.</span><span class="sxs-lookup"><span data-stu-id="2f738-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="2f738-124">Obwohl diese Vorlage SQL-Tabellen liest und aktualisiert, können Sie sie erweitern und für andere Szenarien verwenden.</span><span class="sxs-lookup"><span data-stu-id="2f738-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="2f738-125">Sie können sie beispielsweise verwenden, um eine Stagingtabelle in Dataverse mit Datensätzen von SQL Server zu füllen und um die Stagingtabelle regelmäßig zu synchronisieren, indem ein inkrementeller Push von SQL Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2f738-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="2f738-126">Die erweiterte Abfrage ist in Flow integriert, um die Datentransformation und die inkrementelle Übertragung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2f738-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="2f738-127">Um die **Power Automate - SQL Connect and execute** Vorlage herunterzuladen, gehen Sie zu [Power Automate - SQL Connect und führen Sie](https://go.microsoft.com/fwlink/?linkid=2081789) im Microsoft Download Center aus.</span><span class="sxs-lookup"><span data-stu-id="2f738-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2f738-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2f738-128">Additional resources</span></span>

[<span data-ttu-id="2f738-129">Das Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="2f738-129">The Microsoft Power Platform</span></span>](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]