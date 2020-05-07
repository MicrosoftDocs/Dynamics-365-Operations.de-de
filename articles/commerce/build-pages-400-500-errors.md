---
title: Erstellen von benutzerdefinierte Antwortseiten für Fehler mit 4xx/5xx-Statuscodes
description: In diesem Thema wird beschrieben, wie benutzerdefinierte Antwortseiten für 4xx und 5xx Statuscodefehler mithilfe von Erstellungstools in Microsoft Dynamics 365 Commerce erstellt werden.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269543"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="713a6-103">Erstellen von benutzerdefinierte Antwortseiten für Fehler mit 4xx/5xx-Statuscodes</span><span class="sxs-lookup"><span data-stu-id="713a6-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="713a6-104">In diesem Thema wird beschrieben, wie benutzerdefinierte Antwortseiten für 4xx und 5xx Statuscodefehler mithilfe von Erstellungstools in Microsoft Dynamics 365 Commerce erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="713a6-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="713a6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="713a6-105">Overview</span></span>

<span data-ttu-id="713a6-106">Wenn eine Anforderung nicht erfolgreich ist, gibt der Server HTTP-Statuscode-Fehlerantworten aus.</span><span class="sxs-lookup"><span data-stu-id="713a6-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="713a6-107">Der Statuscode 404 wird erfasst und zurückgegeben, wenn eine Seite nicht gefunden wurde, und der Statuscode 500 wird aufgezeichnet wird zurückgegeben, wenn ein Serverfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="713a6-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="713a6-108">In Dynamics 365 Commerce können Anwendungsbenutzer benutzerdefinierte Statuscodefehlerantwortseiten erstellen die den Benutzern für diese Statuscode-Fehlerantworten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="713a6-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="713a6-109">Erstellen Sie eine Statuscodefehlerantwortseite</span><span class="sxs-lookup"><span data-stu-id="713a6-109">Build a status code error response page</span></span>

<span data-ttu-id="713a6-110">Um eine Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="713a6-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="713a6-111">In Ihrem bevorzugten Webbrowser melden Sie sich an in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="713a6-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="713a6-112">Wählen Sie die Site aus, für die eine Fehlerantwortseite des zugeordneten Statuscodes 4xx/5xx erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="713a6-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="713a6-113">Erstellen Sie die Vorlage</span><span class="sxs-lookup"><span data-stu-id="713a6-113">Build the template</span></span>

<span data-ttu-id="713a6-114">Um die Vorlage für eine Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="713a6-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="713a6-115">Gehen Sie zu **Vorlagen**.</span><span class="sxs-lookup"><span data-stu-id="713a6-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="713a6-116">Wählen Sie **Neu** aus, um eine Seitenvorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="713a6-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="713a6-117">Im Dialogfeld **Neue Vorlage** unter **Vorlagenname** geben Sie einen Namen für die neue Vorlage ein und wählen **OK**.</span><span class="sxs-lookup"><span data-stu-id="713a6-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="713a6-118">Erstellen Sie die Vorlage auf der Struktur, die Sie für die Statuscodefehlerantwortseite möchten.</span><span class="sxs-lookup"><span data-stu-id="713a6-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="713a6-119">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="713a6-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="713a6-120">Erstellen Sie die Statuscodefehlerantwortseite</span><span class="sxs-lookup"><span data-stu-id="713a6-120">Build the status code error response page</span></span>

<span data-ttu-id="713a6-121">Um die Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="713a6-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="713a6-122">Wechseln Sie zu **Seiten**.</span><span class="sxs-lookup"><span data-stu-id="713a6-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="713a6-123">Wählen Sie **Neu** aus, um eine Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="713a6-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="713a6-124">Wählen Sie im Dialogfeld **Eine Vorlage auswählen** eine Vorlage aus und geben Sie dann unter **Seitenname** einen Namen für die Statuscode-Fehlerantwortseite ein.</span><span class="sxs-lookup"><span data-stu-id="713a6-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="713a6-125">Lassen Sie das Feld **Seiten-URL** leer.</span><span class="sxs-lookup"><span data-stu-id="713a6-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="713a6-126">Erstellen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="713a6-126">Build the page.</span></span>
1. <span data-ttu-id="713a6-127">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="713a6-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="713a6-128">Sie können separate Statuscodefehlerantwortseiten für Fehler für 4xx und 5xx Statuscodes erstellen.</span><span class="sxs-lookup"><span data-stu-id="713a6-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="713a6-129">Alternativ können Sie die gleichen allgemeinen Statuscodefehlerantwortseite für beide Fehlerkategorien verwenden.</span><span class="sxs-lookup"><span data-stu-id="713a6-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="713a6-130">Einrichten einer Umleitung für die Statuscodefehlerantwortseite</span><span class="sxs-lookup"><span data-stu-id="713a6-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="713a6-131">Um eine Umleitung für die Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="713a6-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="713a6-132">Gehen Sie zu **URLs \> Neu \> Neuer Alias** und wählen Sie die Statuscodefehlerantwortseite aus, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="713a6-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="713a6-133">Im Feld **Aliasname** geben Sie entweder **default-4xx** oder **default-5xx** ein, je nach Statuscodefehlerantwortseite, für die Sie eine Umleitung einrichten.</span><span class="sxs-lookup"><span data-stu-id="713a6-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="713a6-134">Dieser Alias muss veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="713a6-134">These aliases must be published.</span></span> <span data-ttu-id="713a6-135">Sonst funktioniert die Umleitung nicht.</span><span class="sxs-lookup"><span data-stu-id="713a6-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="713a6-136">Schließen Sie die Seite mit **OK**, um die Verknüpfung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="713a6-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="713a6-137">Falls Sie eine einzelne Statuscodefehlerantwortseite für beide Fehlerkategorien verwenden, wiederholen Sie dieses Verfahren, um einem Alias für die andere Fehlerkategorie der gleichen Seite herzustellen.</span><span class="sxs-lookup"><span data-stu-id="713a6-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="713a6-138">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="713a6-138">Additional resources</span></span>

[<span data-ttu-id="713a6-139">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="713a6-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="713a6-140">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="713a6-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="713a6-141">Erstellen einer Seiten-URL</span><span class="sxs-lookup"><span data-stu-id="713a6-141">Create a page URL</span></span>](create-page-url.md)
