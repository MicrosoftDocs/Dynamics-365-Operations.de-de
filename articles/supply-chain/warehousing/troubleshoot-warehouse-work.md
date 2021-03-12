---
title: Fehlerbehebung im Lagerort
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerortarbeit in Microsoft Dynamics 365 Supply Chain Management auftreten können.
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
ms.openlocfilehash: 3015ec777953cedb5a5d8eea873ed1043cac04cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970233"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="5a9e8-103">Fehlerbehebung bei der Lagerortarbeit</span><span class="sxs-lookup"><span data-stu-id="5a9e8-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a9e8-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben können, die bei der Arbeit mit Lagerortarbeit in Microsoft Dynamics 365 Supply Chain Management auftreten können.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="5a9e8-105">Ich kann keine Ladungsträger mit Seriennummern-Elementen verschieben, wenn Blanko-Ausgabe und Blanko-Empfang in der Dimensionsgruppe für die Nachverfolgung erlaubt sind.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5a9e8-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5a9e8-106">Issue description</span></span>

<span data-ttu-id="5a9e8-107">Sie können einen Ladungsträger nicht mit dem Menüelement **Verschieben** verschieben, wenn die Seriennummer die Einstellungen *Leerzeichenausgabe erlaubt* und *Leerzeichenquittung erlaubt* auf der Tracking-Dimensionsgruppe hat und wenn sich mehrere Ladungsträger auf demselben Lagerplatz befinden, von denen einige Seriennummern haben und einige nicht.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5a9e8-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="5a9e8-108">Issue resolution</span></span>

<span data-ttu-id="5a9e8-109">Dieses Problem wird durch Änderungen behoben, die in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="5a9e8-110">Diese Änderungen werden das Feld **Seriennummer** optional machen, wenn leere Quittungen und leere Ausgaben erlaubt sind.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="5a9e8-111">Ich erhalte in der Lagerort App folgende Fehlermeldung, wenn ich Bewegungen verarbeite: „Der Besitzer des Bestandes %1 ist in diesem Prozess nicht erlaubt.“</span><span class="sxs-lookup"><span data-stu-id="5a9e8-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5a9e8-112">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="5a9e8-112">Issue description</span></span>

<span data-ttu-id="5a9e8-113">Die Dimension **Besitzer** für die Nachverfolgung fehlt, wenn die Lagerort App verwendet wird, um Bewegungen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="5a9e8-114">Eine reguläre Bestandsumlagerungserfassung aus dem Supply Chain Management Client scheint wie vorgesehen zu funktionieren und kann nur gebucht werden, wenn die Dimension **Besitzer** ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5a9e8-115">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="5a9e8-115">Issue resolution</span></span>

<span data-ttu-id="5a9e8-116">Microsoft hat dieses Problem untersucht und festgestellt, dass es sich um eine Einschränkung der Funktion handelt.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="5a9e8-117">Derzeit unterstützen die Prozesse der Lagerortverwaltung nur Bestände, die im Besitz der juristischen Entität sind.</span><span class="sxs-lookup"><span data-stu-id="5a9e8-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
