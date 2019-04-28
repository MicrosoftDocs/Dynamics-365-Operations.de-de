---
title: Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (24. September 2018)
description: In diesem Thema werden die Funktionen beschrieben, die in Microsoft Dynamics 365 for Talent Core HR entweder neu oder geändert sind.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 24526a5884c6c5d30d1f49077b88a24364aa4365
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "856160"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-24-2018"></a><span data-ttu-id="ecf00-103">Neuerungen oder Änderungen in Dynamics 365 for Talent Core HR (24. September 2018)</span><span class="sxs-lookup"><span data-stu-id="ecf00-103">What's new or changed in Dynamics 365 for Talent Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ecf00-104">**Build 8.1.1015.0**</span><span class="sxs-lookup"><span data-stu-id="ecf00-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="ecf00-105">In diesem Thema werden die Funktionen beschrieben, die in Core HR entweder neu oder geändert sind.</span><span class="sxs-lookup"><span data-stu-id="ecf00-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="ecf00-106">Währung zu den Vergütungen hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="ecf00-106">Currency added to Benefits</span></span>

<span data-ttu-id="ecf00-107">Vorteilspläne wurden aktualisiert, um die Währung des Vorteils einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="ecf00-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="ecf00-108">Dieses neue Feld ist auch für Vergütungen für registrierte Arbeitskräfte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ecf00-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="ecf00-109">Dieses neue Feld ist ein Teil der Liste Vergütungen verwalten und zeigt eine Liste der Vorteile des Sicherheitsrechts an.</span><span class="sxs-lookup"><span data-stu-id="ecf00-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="ecf00-110">Antizipierungen für Urlaub und Abwesenheit aktualisieren</span><span class="sxs-lookup"><span data-stu-id="ecf00-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="ecf00-111">Organisationsprämienfreizeit unterschiedlich auf der Basis, wenn Mitarbeiter das Unternehmen wechseln‌ das Unternehmen eintreten.</span><span class="sxs-lookup"><span data-stu-id="ecf00-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="ecf00-112">Für Mitarbeiter, die die Organisation verlassen, müssen möglicherweise einige die Prämie im Feld Kündigungsdatum beendet werden, während andere erst am letzten Arbeitstag den,  Abgrenzungsprozess beenden.</span><span class="sxs-lookup"><span data-stu-id="ecf00-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="ecf00-113">Diese Änderungen gibt Organisationen die Möglichkeit, auszuwählen, wann die Registrierung für den Kündigungsprozesses beendet wird.</span><span class="sxs-lookup"><span data-stu-id="ecf00-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="ecf00-114">Diese neue Optionen sind Teil der Rechte, um einer Arbeitskraft zu kündigen und eine Arbeitskraft  vom Manager-Self-Service zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="ecf00-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="ecf00-115">Andere Änderungen</span><span class="sxs-lookup"><span data-stu-id="ecf00-115">Other changes</span></span>

<span data-ttu-id="ecf00-116">Diese Version enthält eine Reihe zusätzlicher Fehlerkorrekturen.</span><span class="sxs-lookup"><span data-stu-id="ecf00-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="ecf00-117">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="ecf00-117">Known Issue</span></span>

-   <span data-ttu-id="ecf00-118">**Abgang:**, Wenn einer Arbeitskraft ein neuer Anhang hinzugefügt wird, werden die Schaltflächen **Neu** und **Bearbeiten** abgeblendet. **Problemumgehung:**, Bevor die Anhangsseite geöffnet wird, überprüfen Sie, dass die Infoboxen **Arbeitskraft** geschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ecf00-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="ecf00-119">Wenn die Infoboxen geschlossen werden, wenn die **Arbeitskraft**-Seite geladen wird, werden die Anhangschaltflächen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ecf00-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="ecf00-120">(Dieses Problem wird in der folgenden Plattformaktualisierung korrigiert.)</span><span class="sxs-lookup"><span data-stu-id="ecf00-120">(This issue will be fixed in the next platform update.)</span></span>
