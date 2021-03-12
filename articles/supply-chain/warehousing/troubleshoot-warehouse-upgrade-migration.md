---
title: Fehlerbehebung bei Upgrade und Migration zur erweiterten Lagerortverwaltung
description: In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die beim Upgrade und bei der Migration zur erweiterten Lagerverwaltung auftreten können.
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
ms.openlocfilehash: dc1c487a608c2e165f5f12aed344cb89fe8d41e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993877"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="c1399-103">Fehlerbehebung bei Upgrade und Migration zur erweiterten Lagerortverwaltung</span><span class="sxs-lookup"><span data-stu-id="c1399-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1399-104">In diesem Thema wird beschrieben, wie Sie allgemeine Probleme beheben, die beim Upgrade und bei der Migration zur erweiterten Lagerverwaltung auftreten können.</span><span class="sxs-lookup"><span data-stu-id="c1399-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="c1399-105">Ich erhalte die folgende Fehlermeldung: „java.security.cert.certPathValidatorException: Vertrauensanker für Zertifizierungspfad wurde nicht gefunden.“</span><span class="sxs-lookup"><span data-stu-id="c1399-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c1399-106">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="c1399-106">Issue description</span></span>

<span data-ttu-id="c1399-107">Sie erhalten diese Fehlermeldung in der Lagerort App, da selbstsignierten Zertifikaten auf Android 8+ in lokalen Umgebungen nicht vertraut wird.</span><span class="sxs-lookup"><span data-stu-id="c1399-107">You receive this error message in the warehouse app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c1399-108">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="c1399-108">Issue resolution</span></span>

<span data-ttu-id="c1399-109">Verwenden Sie eine externe (öffentliche) Zertifizierungsstelle (CA).</span><span class="sxs-lookup"><span data-stu-id="c1399-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="c1399-110">Ein Fix für dieses Problem ist in Version 1.9.0.0 der Lagerort App verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c1399-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="c1399-111">Weitere Informationen zu diesem Problem und wie Sie es beheben können, finden Sie unter [Fehlerbehebung bei Verbindungsproblemen der Lagerort App](troubleshoot-warehouse-app-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c1399-111">For more information about this issue and how to fix it, see [Troubleshoot warehouse app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="c1399-112">Was ist der genehmigte Prozess für den Wechsel von Basis-Lagerort zu erweitertem Lagerort?</span><span class="sxs-lookup"><span data-stu-id="c1399-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="c1399-113">Problembeschreibung</span><span class="sxs-lookup"><span data-stu-id="c1399-113">Issue description</span></span>

<span data-ttu-id="c1399-114">Sie arbeiten derzeit mit der Lagerort-/Bestandsverwaltung und nutzen die Basislagerfunktionalität und möchten zur erweiterten Lagerortverwaltung wechseln, um die Vorteile von mobilen Geräten, Wellen und Arbeit zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="c1399-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="c1399-115">Allerdings stoßen Sie auf Probleme, wenn Sie versuchen, diesen Wechsel vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="c1399-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="c1399-116">Sie können z. B. Ihre Produkte nicht so ändern, dass sie Lagerdimensionen (Standort, Lagerort und Lagerplatz) verwenden, weil die Produkte mit Transaktionen belegt sind.</span><span class="sxs-lookup"><span data-stu-id="c1399-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="c1399-117">Daher müssen Sie den genehmigten Prozess für den Umzug von der einfachen Lagerhaltung zur erweiterten Lagerhaltung lernen.</span><span class="sxs-lookup"><span data-stu-id="c1399-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c1399-118">Problemlösung</span><span class="sxs-lookup"><span data-stu-id="c1399-118">Issue resolution</span></span>

<span data-ttu-id="c1399-119">Weitere Informationen über den Prozess für den Wechsel von Basic Warehousing zu Advanced Warehousing finden Sie in den folgenden Blog-Beiträgen und in der Dokumentation:</span><span class="sxs-lookup"><span data-stu-id="c1399-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="c1399-120">Prozess der Lagerortverwaltung für bestehende Elemente und Lagerorte aktivieren</span><span class="sxs-lookup"><span data-stu-id="c1399-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="c1399-121">Migration von Microsoft Dynamics AX WMS auf neue R3-Lager- und Transportfunktionalität</span><span class="sxs-lookup"><span data-stu-id="c1399-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="c1399-122">WMSI/WMS2 Element-Migration</span><span class="sxs-lookup"><span data-stu-id="c1399-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="c1399-123">Upgrade der Lagerortverwaltung von Microsoft Dynamics AX 2012 auf Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="c1399-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)
