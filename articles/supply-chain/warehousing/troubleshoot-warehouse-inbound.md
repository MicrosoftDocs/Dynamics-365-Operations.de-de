---
title: Fehlerbehebung bei eingehenden Lagerort-Vorgängen
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit eingehenden Lagerort-Operationen in Microsoft Dynamics 365 Supply Chain Management auftreten können.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6875c3c644b9993a384ba4d8623640536d7307e1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250881"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="ee6f8-103">Fehlerbehebung bei eingehenden Lagerort-Vorgängen</span><span class="sxs-lookup"><span data-stu-id="ee6f8-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee6f8-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit eingehenden Lagerort-Operationen in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="ee6f8-105">Ich erhalte die folgende Fehlermeldung: „Qualitätsauftrag %1 wurde erzeugt.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="ee6f8-106">Clusterprofil konnte nicht gefunden werden, bitte überprüfen Sie Ihre Konfiguration.“</span><span class="sxs-lookup"><span data-stu-id="ee6f8-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ee6f8-107">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="ee6f8-107">Issue description</span></span>

<span data-ttu-id="ee6f8-108">Diese Fehlermeldung bezieht sich auf einen Eingangsvorgang, bei dem das Qualitätsmanagement (QMS) eingeschaltet ist.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="ee6f8-109">Abhängig von den Konfigurationen in Ihrer Umgebung können zusätzliche Details über die Transaktion, die die Fehlermeldung erzeugt, helfen, das Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ee6f8-110">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="ee6f8-110">Issue resolution</span></span>

<span data-ttu-id="ee6f8-111">Überprüfen Sie zunächst die [Clusterkommissionierung](set-up-cluster-picking.md) und stellen Sie sicher, dass Ihre Cluster-Profile richtig festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="ee6f8-112">Sie können kein Menüelement für die Cluster-Kommissionierung auf einem mobilen Gerät verwenden, wenn keine Cluster-Profile festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="ee6f8-113">Abhängig von Ihrer Umgebung müssen Sie möglicherweise auch andere zugehörige Konfigurationen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="ee6f8-114">Der Empfang von gemischten Ladungsträgern funktioniert nicht für alle Dispositionscodes außer Guthaben.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ee6f8-115">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="ee6f8-115">Issue description</span></span>

<span data-ttu-id="ee6f8-116">Wenn das Feld **Aktion** für einen Dispositionscode auf *Kredit* oder *Schrott* festgelegt ist, können Sie nur den Menüpunkt [Mischkennzeichen-Empfang](mixed-license-plate-receiving.md) verwenden, um zurückgegebene Elemente zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ee6f8-117">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="ee6f8-117">Issue resolution</span></span>

<span data-ttu-id="ee6f8-118">Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="ee6f8-119">Derzeit werden für den gemischten Ladungsträger-Empfang nur [Positionscodes](../service-management/set-up-disposition-codes.md) unterstützt, bei denen das Feld **Aktion** auf *Gutschrift* oder *Ausschuss* festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="ee6f8-120">Wenn ich die Aufgabe „Periodische Wareneingänge aktualisieren“ ausführe, werden unbestätigte Einkaufsbestellungen bestätigt.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ee6f8-121">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="ee6f8-121">Issue description</span></span>

<span data-ttu-id="ee6f8-122">Nachdem Sie die periodische Aufgabe *Produkteingänge aktualisieren* ausgeführt haben, bestätigt das System automatisch unbestätigte Einkaufsbestellungen, die einen Bestandstransaktionsstatus von *Registriert* haben.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ee6f8-123">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="ee6f8-123">Issue resolution</span></span>

<span data-ttu-id="ee6f8-124">Eine neue Funktion zur Behandlung eingehender Ladungen, *Übernahme von Ladungsmengen*, behebt dieses Problem.</span><span class="sxs-lookup"><span data-stu-id="ee6f8-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="ee6f8-125">Um diese Funktion zu aktivieren, gehen Sie zu [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) und schalten Sie die folgenden Funktionen ein (in der Reihenfolge, in der sie aufgelistet sind):</span><span class="sxs-lookup"><span data-stu-id="ee6f8-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="ee6f8-126">Zuordnung von Bestellbestandsbuchungen zur Ladung</span><span class="sxs-lookup"><span data-stu-id="ee6f8-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="ee6f8-127">Zu hoher Zugang bei Auslastungsmengen</span><span class="sxs-lookup"><span data-stu-id="ee6f8-127">Over receipt of load quantities</span></span>

<span data-ttu-id="ee6f8-128">Weitere Informationen finden Sie unter [Registrierte Produktmengen gegen Einkaufsbestellungen verbuchen](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="ee6f8-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]