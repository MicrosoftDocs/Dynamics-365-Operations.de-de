---
title: Erstellen von benutzerdefinierte Antwortseiten für Fehler mit 4xx/5xx-Statuscodes
description: In diesem Thema wird beschrieben, wie benutzerdefinierte Antwortseiten für 4xx und 5xx Statuscodefehler mithilfe von Erstellungstools in Microsoft Dynamics 365 Commerce erstellt werden.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001125"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="86cdd-103">Erstellen von benutzerdefinierte Antwortseiten für Fehler mit 4xx/5xx-Statuscodes</span><span class="sxs-lookup"><span data-stu-id="86cdd-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="86cdd-104">In diesem Thema wird beschrieben, wie benutzerdefinierte Antwortseiten für 4xx und 5xx Statuscodefehler mithilfe von Erstellungstools in Microsoft Dynamics 365 Commerce erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="86cdd-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="86cdd-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="86cdd-105">Overview</span></span>

<span data-ttu-id="86cdd-106">Wenn eine Anforderung nicht erfolgreich ist, gibt der Server HTTP-Statuscode-Fehlerantworten aus.</span><span class="sxs-lookup"><span data-stu-id="86cdd-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="86cdd-107">Der Statuscode 404 wird erfasst und zurückgegeben, wenn eine Seite nicht gefunden wurde, und der Statuscode 500 wird aufgezeichnet wird zurückgegeben, wenn ein Serverfehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="86cdd-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="86cdd-108">In Dynamics 365 Commerce können Anwendungsbenutzer benutzerdefinierte Statuscodefehlerantwortseiten erstellen die den Benutzern für diese Statuscode-Fehlerantworten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="86cdd-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="86cdd-109">Erstellen Sie eine Statuscodefehlerantwortseite</span><span class="sxs-lookup"><span data-stu-id="86cdd-109">Build a status code error response page</span></span>

<span data-ttu-id="86cdd-110">Um eine Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="86cdd-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="86cdd-111">In Ihrem bevorzugten Webbrowser melden Sie sich an in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="86cdd-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="86cdd-112">Wählen Sie die Site aus, für die eine Fehlerantwortseite des zugeordneten Statuscodes 4xx/5xx erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="86cdd-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="86cdd-113">Erstellen Sie die Vorlage</span><span class="sxs-lookup"><span data-stu-id="86cdd-113">Build the template</span></span>

<span data-ttu-id="86cdd-114">Um die Vorlage für eine Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="86cdd-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="86cdd-115">Gehen Sie zu **Vorlagen \> Neue Vorlage**.</span><span class="sxs-lookup"><span data-stu-id="86cdd-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="86cdd-116">Neuen der neuen Vorlage.</span><span class="sxs-lookup"><span data-stu-id="86cdd-116">Name the new template.</span></span>
1. <span data-ttu-id="86cdd-117">Erstellen Sie die Vorlage auf der Struktur, die Sie für die Statuscodefehlerantwortseite möchten.</span><span class="sxs-lookup"><span data-stu-id="86cdd-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="86cdd-118">Laden Sie die Vorlage hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="86cdd-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="86cdd-119">Erstellen Sie die Statuscodefehlerantwortseite</span><span class="sxs-lookup"><span data-stu-id="86cdd-119">Build the status code error response page</span></span>

<span data-ttu-id="86cdd-120">Um die Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="86cdd-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="86cdd-121">Gehen Sie zu **Seiten \> Neue Seite**</span><span class="sxs-lookup"><span data-stu-id="86cdd-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="86cdd-122">Benennen Sie die Statuscodefehlerantwortseite, aber legen Sie das Feld **nicht** auf die **URL** fest.</span><span class="sxs-lookup"><span data-stu-id="86cdd-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="86cdd-123">Erstellen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="86cdd-123">Build the page.</span></span>
1. <span data-ttu-id="86cdd-124">Laden Sie die Seite hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="86cdd-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="86cdd-125">Sie können separate Statuscodefehlerantwortseiten für Fehler für 4xx und 5xx Statuscodes erstellen.</span><span class="sxs-lookup"><span data-stu-id="86cdd-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="86cdd-126">Alternativ können Sie die gleichen allgemeinen Statuscodefehlerantwortseite für beide Fehlerkategorien verwenden.</span><span class="sxs-lookup"><span data-stu-id="86cdd-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="86cdd-127">Einrichten einer Umleitung für die Statuscodefehlerantwortseite</span><span class="sxs-lookup"><span data-stu-id="86cdd-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="86cdd-128">Um eine Umleitung für die Statuscodefehlerantwortseite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="86cdd-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="86cdd-129">Gehen Sie zu **URLs \> Neu \> Neuer Alias** und wählen Sie die Statuscodefehlerantwortseite aus, die Sie eben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="86cdd-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="86cdd-130">Im Feld **Aliasname** geben Sie entweder **default-4xx** oder **default-5xx** ein, je nach Statuscodefehlerantwortseite, für die Sie eine Umleitung einrichten.</span><span class="sxs-lookup"><span data-stu-id="86cdd-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="86cdd-131">Dieser Alias muss veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="86cdd-131">These aliases must be published.</span></span> <span data-ttu-id="86cdd-132">Sonst funktioniert die Umleitung nicht.</span><span class="sxs-lookup"><span data-stu-id="86cdd-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="86cdd-133">Schließen Sie die Seite mit **OK**, um die Verknüpfung zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="86cdd-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="86cdd-134">Falls Sie eine einzelne Statuscodefehlerantwortseite für beide Fehlerkategorien verwenden, wiederholen Sie dieses Verfahren, um einem Alias für die andere Fehlerkategorie der gleichen Seite herzustellen.</span><span class="sxs-lookup"><span data-stu-id="86cdd-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86cdd-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="86cdd-135">Additional resources</span></span>

[<span data-ttu-id="86cdd-136">Arbeiten mit Vorlagen</span><span class="sxs-lookup"><span data-stu-id="86cdd-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="86cdd-137">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="86cdd-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="86cdd-138">Erstellen einer Seiten-URL</span><span class="sxs-lookup"><span data-stu-id="86cdd-138">Create a page URL</span></span>](create-page-url.md)
