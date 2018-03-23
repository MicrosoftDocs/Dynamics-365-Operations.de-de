---
title: "Erweitern Sie die Funktionalität von Microsoft Dynamics 365 for Talent"
description: "Wenn Sie Microsoft PowerApps erstellt haben, können Sie diese Anwendungen von Links innerhalb von Microsoft Dynamics 365 for Talent starten."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: de-de
ms.lasthandoff: 03/07/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="b1282-103">Erweitern Sie die Funktionalität von Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="b1282-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!include[banner](includes/banner.md)]

<span data-ttu-id="b1282-104">Wenn Sie Microsoft PowerApps erstellt haben, können Sie diese Anwendungen von Links innerhalb von Microsoft Dynamics 365 for Talent starten.</span><span class="sxs-lookup"><span data-stu-id="b1282-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="b1282-105">Um Zugriff auf Ihre Bewerbungen einzurichten, müssen Sie einige Informationen im Talent auf einer Konfigurationsseite eirichten die Sie aus dem Arbeitsbereich **Systemverwaltung** öffnen können.</span><span class="sxs-lookup"><span data-stu-id="b1282-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="b1282-106">Konfigurieren von eingebetteten PowerApps innerhalb von Talent</span><span class="sxs-lookup"><span data-stu-id="b1282-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="b1282-107">Verwenden Sie die Seite **Satz eingebettetes Microsoft PowerApps**, um Talent Seiten zu konfigurieren, um PowerApps-Bewerbungen zu starten.</span><span class="sxs-lookup"><span data-stu-id="b1282-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="b1282-108">Um die Seite **Legen Sie eingebettetes Microsoft PowerApps fest** zu öffnen, öffnen Sie die Verknüpfung **Systemverwaltung** und anschließend **Links** auswählen Registerkarte **Microsoft PowerApps** in der Gruppe **Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="b1282-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="b1282-109">Die folgenden Informationen werden auf dieser Seite eingegeben oder festgelegt:</span><span class="sxs-lookup"><span data-stu-id="b1282-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="b1282-110">Ein beschreibender Name oder eine Kennung für die PowerApps-Bewerbung.</span><span class="sxs-lookup"><span data-stu-id="b1282-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="b1282-111">Eine eindeutige Kennung (GUID) für jede Anwendung, die Sie einer Talent Seite hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b1282-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="b1282-112">Anwendungs-ID ist im Feld PowerApps-Standort, [powerapps.com](http://powerapps.com/) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1282-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="b1282-113">Die Seite, von der Benutzer eine Anwendung oder öffnen kann</span><span class="sxs-lookup"><span data-stu-id="b1282-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="b1282-114">Nicht alle Talent Seiten unterstützen eingebettete PowerApps und Power BI-Berichte.</span><span class="sxs-lookup"><span data-stu-id="b1282-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="b1282-115">Geben Sie hier den internen Namen der Seite ein, anstatt den Anzeigenamen, der am oberen Seitenrand erscheint.</span><span class="sxs-lookup"><span data-stu-id="b1282-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="b1282-116">Um den internen Namen zu suchen, öffnen Sie die Seite für den internen Namen und klicken Sie irgendwo auf der Seite mit der rechten Maustaste.</span><span class="sxs-lookup"><span data-stu-id="b1282-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="b1282-117">Wenn das Menü sich öffnet, zeigen Sie im **Formularinformationen** auf Artikel.</span><span class="sxs-lookup"><span data-stu-id="b1282-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="b1282-118">Der interne Formularname wird neben dem Menü **Formularinformationen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b1282-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="b1282-119">Definieren Sie das Formularsteuerelement, aus dem die Bewerbung Kontextdaten erwerben kann.</span><span class="sxs-lookup"><span data-stu-id="b1282-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="b1282-120">So kann beispielsweise eine Anwendung Daten zu einer Arbeitskraft nutzen.</span><span class="sxs-lookup"><span data-stu-id="b1282-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="b1282-121">Wenn Sie die Seite **Arbeitskraft** im Feld **Kontext** eingeben, wird die Seite **Arbeitskraft** geöffnet, wenn Sie die Bewerbung starten.</span><span class="sxs-lookup"><span data-stu-id="b1282-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="b1282-122">Ein Eintrag ist im **Kontextfeld** optional.</span><span class="sxs-lookup"><span data-stu-id="b1282-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="b1282-123">Legen Sie die Größe des Dialogfelds fest, an dem die PowerApps-Bewerbung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1282-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="b1282-124">Die Dialogfelder werden als "klein"oder "groß" festgelegt, um die Benutzeroberfläche zu optimieren, wenn Sie Ihre Bewerbung auf einem Telefon oder einem größeren Gerät laufen lassen.</span><span class="sxs-lookup"><span data-stu-id="b1282-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="b1282-125">Sie können auch angeben, für welche juristische Personen eine Bewerbung verfügbar ist, oder Sie können Produktbeziehungen Katalogs für alle juristischen Personen vefügbar machen.</span><span class="sxs-lookup"><span data-stu-id="b1282-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="b1282-126">Standardmäßig sind die PowerApps-Bewerbungen für alle juristischen Personen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1282-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="b1282-127">Öffnen Sie eine Bewerbung</span><span class="sxs-lookup"><span data-stu-id="b1282-127">Opening an application</span></span>
<span data-ttu-id="b1282-128">Wenn Sie eingebettete PowerApps-Bewerbungen konfigurieren, werden Links für Anwendungen, die Sie zuvor definiert haben, zu Seiten innerhalb von Talent hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b1282-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="b1282-129">Klicken Sie auf einen Link, um eine Bewerbung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b1282-129">Click a link to open an application.</span></span> 



