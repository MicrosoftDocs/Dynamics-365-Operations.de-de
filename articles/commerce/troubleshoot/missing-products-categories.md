---
title: Nach dem Kopieren der Umgebung fehlende Produkte und Kategorien
description: Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Kopieren einer Website zwischen Umgebungen oder innerhalb derselben Umgebung fehlen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801722"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="f96e8-103">Nach dem Kopieren der Umgebung fehlende Produkte und Kategorien</span><span class="sxs-lookup"><span data-stu-id="f96e8-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f96e8-104">Dieses Thema enthält Anleitungen zur Fehlerbehebung, die hilfreich sein können, wenn Produkte und Kategorien nach dem Kopieren einer Website zwischen Umgebungen oder innerhalb derselben Umgebung fehlen.</span><span class="sxs-lookup"><span data-stu-id="f96e8-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="f96e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f96e8-105">Description</span></span>

<span data-ttu-id="f96e8-106">Nachdem eine Website von einer Umgebung in eine andere oder innerhalb derselben Umgebung kopiert wurde, fehlen die Produkte und Kategorien auf der Website.</span><span class="sxs-lookup"><span data-stu-id="f96e8-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="f96e8-107">Die Produkte und Kategorien fehlen in der E-Commerce-Storefront und in der Registerkarte **Produkte** im Commerce-Website-Generator.</span><span class="sxs-lookup"><span data-stu-id="f96e8-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="f96e8-108">Lösung</span><span class="sxs-lookup"><span data-stu-id="f96e8-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="f96e8-109">Die Kanalvorgangseinheitsnummer einer neu kopierten Website im Commerce-Website-Generator zuordnen</span><span class="sxs-lookup"><span data-stu-id="f96e8-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="f96e8-110">Befolgen Sie diese Schritte, um die Kanalvorgangseinheitsnummer (Operating Unit Number, OUN)einer neu kopierten Website im Commerce-Website-Generator zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f96e8-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f96e8-111">Wählen Sie die neu kopierte Website aus.</span><span class="sxs-lookup"><span data-stu-id="f96e8-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="f96e8-112">Wählen Sie in den **Websiteeinstellungen** die Option **Kanäle** aus.</span><span class="sxs-lookup"><span data-stu-id="f96e8-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="f96e8-113">Wählen Sie neben dem Kanalnamen die Auslassungspunkte (**...**) und anschließend **Onlineshop-Kanal ändern** aus.</span><span class="sxs-lookup"><span data-stu-id="f96e8-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="f96e8-114">Wählen Sie im Dialogfeld **Onlineshop-Kanal ändern** den Kanal aus, der der neu kopierten Website zugeordnet werden soll, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="f96e8-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="f96e8-115">Wählen Sie **Speichern und veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="f96e8-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f96e8-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f96e8-116">Additional resources</span></span>

[<span data-ttu-id="f96e8-117">Zuordnen einer Dynamics 365 Commerce-Website zu einem Onlinekanal</span><span class="sxs-lookup"><span data-stu-id="f96e8-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
