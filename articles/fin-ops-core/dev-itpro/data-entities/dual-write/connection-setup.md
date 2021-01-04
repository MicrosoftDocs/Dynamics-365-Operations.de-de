---
title: Anleitung zum Einrichten des dualen Schreibens
description: In diesem Thema werden die Szenarien beschrieben, die für die Dual-Write-Einrichtung unterstützt werden.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 47c07dd0e2f311b61297340a48a5a31cb1de3903
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685664"
---
# <a name="guidance-for-dual-write-setup"></a><span data-ttu-id="af098-103">Anleitung zum Einrichten des dualen Schreibens</span><span class="sxs-lookup"><span data-stu-id="af098-103">Guidance for dual-write setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="af098-104">Sie können eine Dual-Write-Verbindung zwischen einer Finance and Operations-Umgebung und einer Dataverse-Umgebung einrichten.</span><span class="sxs-lookup"><span data-stu-id="af098-104">You can set up a dual-write connection between a Finance and Operations environment and a Dataverse environment.</span></span>

+ <span data-ttu-id="af098-105">Eine **Finance and Operations-Umgebung** bietet die zugrunde liegende Plattform für **Finance and Operations-Anwendungen** (z.B. Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce und Dynamics 365 Human Resources).</span><span class="sxs-lookup"><span data-stu-id="af098-105">A **Finance and Operations environment** provides the underlying platform for **Finance and Operations apps** (for example, Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce, and Dynamics 365 Human Resources).</span></span>
+ <span data-ttu-id="af098-106">Eine **Dataverse-Umgebung** bietet die zugrunde liegende Plattform für **Kundenbindungs-Apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing und Dynamics 365 Project Service Automation).</span><span class="sxs-lookup"><span data-stu-id="af098-106">A **Dataverse environment** provides the underlying platform for **customer engagement apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing, and Dynamics 365 Project Service Automation).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af098-107">Das Modul „Personalressourcen“ in Dynamics 365 Finance unterstützt Verbindungen für duales Schreiben, die Dynamics 365 Human Resources-App jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="af098-107">The Human Resources module in Dynamics 365 Finance supports dual-write connections, but the Dynamics 365 Human Resources app doesn't.</span></span>

<span data-ttu-id="af098-108">Der Einrichtungsmechanismus variiert je nach Ihrem Abonnement und der Umgebung:</span><span class="sxs-lookup"><span data-stu-id="af098-108">The setup mechanism varies, depending on your subscription and the environment:</span></span>

+ <span data-ttu-id="af098-109">Bei neuen Instanzen von Finance and Operations Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="af098-109">For new instances of Finance and Operations apps, the setup of a dual-write connection begins in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="af098-110">Wenn Sie eine Lizenz für Microsoft Power Platform haben, erhalten Sie eine neue Dataverse-Umgebung, wenn Ihr Mandant keine hat.</span><span class="sxs-lookup"><span data-stu-id="af098-110">If you have a license for Microsoft Power Platform, you will get a new Dataverse environment if your tenant doesn't have one.</span></span>
+ <span data-ttu-id="af098-111">Für bestehende Instanzen von Finance and Operations-Anwendungen beginnt die Einrichtung einer Dual-Write-Verbindung in der Finance and Operations-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="af098-111">For existing instances Finance and Operations apps, the setup of a dual-write connection begins in the Finance and Operations environment.</span></span>

<span data-ttu-id="af098-112">Bevor Sie mit dem dualen Schreiben für eine Entität beginnen, können Sie eine erste Synchronisierung ausführen, um vorhandene Daten auf beiden Seiten, also auf der Seite der Finance and Operations-Apps und der Seite der Customer Engagement-Apps, zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="af098-112">Before you start dual-write on an entity, you can run an initial synchronization to handle existing data on both sides: Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="af098-113">Sie können diese erste Synchronisierung überspringen, wenn Sie keine Daten zwischen den beiden Umgebungen synchronisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="af098-113">You can skip the initial synchronization if you don't have to sync data between the two environments.</span></span>

<span data-ttu-id="af098-114">Bei einer ersten Synchronisierung können Sie vorhandene Daten bidirektional von einer App in eine andere kopieren.</span><span class="sxs-lookup"><span data-stu-id="af098-114">An initial synchronization lets you copy existing data from one app to another bidirectionally.</span></span> <span data-ttu-id="af098-115">Es gibt verschiedene Einrichtungsszenarien, je nachdem, welche Umgebungen Sie bereits verwenden und welche Art von Daten sich in den Umgebungen befinden.</span><span class="sxs-lookup"><span data-stu-id="af098-115">There are several setup scenarios, depending on the environments that you already have and the type of data in them.</span></span>

<span data-ttu-id="af098-116">Die folgenden Einrichtungsszenarien werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="af098-116">The following setup scenarios are supported:</span></span>

+ [<span data-ttu-id="af098-117">Eine neue Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-117">A new Finance and Operations app instance and a new customer engagement app instance</span></span>](#new-new)
+ [<span data-ttu-id="af098-118">Eine neue Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-118">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>](#new-existing)
+ [<span data-ttu-id="af098-119">Eine neue Finance and Operations-Anwendungsinstanz, die über Demodaten und eine neue Customer Engagement Anwendungsinstanz verfügt</span><span class="sxs-lookup"><span data-stu-id="af098-119">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>](#new-data-new)
+ [<span data-ttu-id="af098-120">Eine neue Finance and Operations App-Instanz, die über Demodaten verfügt, und eine bestehende Customer Engagement App-Instanz</span><span class="sxs-lookup"><span data-stu-id="af098-120">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>](#new-data-existing)
+ [<span data-ttu-id="af098-121">Eine bestehende Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-121">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>](#existing-new)
+ [<span data-ttu-id="af098-122">Eine bestehende Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-122">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a><span data-ttu-id="af098-123">Eine neue Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-123">A new Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="af098-124">Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer neuen Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten in [Duales Schreiben einrichten von Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="af098-124">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and a new instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="af098-125">Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="af098-125">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="af098-126">Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="af098-126">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="af098-127">Es wird eine neue, leere Instanz einer Customer Engagement Anwendung bereitgestellt, in der die CRM-Prime-Lösung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="af098-127">A new, empty instance of a customer engagement app is provisioned, where the CRM prime solution is installed.</span></span>
- <span data-ttu-id="af098-128">Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.</span><span class="sxs-lookup"><span data-stu-id="af098-128">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="af098-129">Tabellenzuordnungen werden für die Live-Synchronisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af098-129">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="af098-130">Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="af098-130">Both environments are then ready for live data synchronization.</span></span>

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a><span data-ttu-id="af098-131">Eine neue Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-131">A new Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="af098-132">Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die keine Daten hat, und einer bestehenden Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten in [Duales Schreiben einrichten von Lifecycle Services](lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="af098-132">To set up a dual-write connection between a new instance of a Finance and Operations app that has no data and an existing instance of a customer engagement app, follow the steps in [Dual-write setup from Lifecycle Services](lcs-setup.md).</span></span> <span data-ttu-id="af098-133">Wenn der Verbindungsaufbau abgeschlossen ist, werden die folgenden Aktionen automatisch ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="af098-133">When the connection setup is completed, the following actions automatically occur:</span></span>

- <span data-ttu-id="af098-134">Eine neue, leere Finance and Operations-Umgebung wird bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="af098-134">A new, empty Finance and Operations environment is provisioned.</span></span>
- <span data-ttu-id="af098-135">Eine Dual-Write-Verbindung wird für DAT-Firmendaten hergestellt.</span><span class="sxs-lookup"><span data-stu-id="af098-135">A dual-write connection is established for DAT company data.</span></span>
- <span data-ttu-id="af098-136">Tabellenzuordnungen werden für die Live-Synchronisierung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af098-136">Table maps are enabled for live synchronization.</span></span>

<span data-ttu-id="af098-137">Beide Umgebungen sind dann für die Live-Datensynchronisierung bereit.</span><span class="sxs-lookup"><span data-stu-id="af098-137">Both environments are then ready for live data synchronization.</span></span>

<span data-ttu-id="af098-138">Um die vorhandenen Dataverse-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="af098-138">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="af098-139">Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="af098-139">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="af098-140">Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.</span><span class="sxs-lookup"><span data-stu-id="af098-140">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="af098-141">[Bootstrap](bootstrap-company-data.md) die Dataverse-Daten unter Verwendung eines aus drei Buchstaben bestehenden Buchungscodees der International Organization for Standardization (ISO).</span><span class="sxs-lookup"><span data-stu-id="af098-141">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter International Organization for Standardization (ISO) company code.</span></span>
4. <span data-ttu-id="af098-142">Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="af098-142">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="af098-143">Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example) später in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="af098-143">For links to an example and an alternative approach, see the [Example](#example) section later in this topic.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a><span data-ttu-id="af098-144">Eine neue Finance and Operations Anwendungsinstanz, die über Demodaten und eine neue Customer Engagement Anwendungsinstanz verfügt</span><span class="sxs-lookup"><span data-stu-id="af098-144">A new Finance and Operations app instance that has data and a new customer engagement app instance</span></span>

<span data-ttu-id="af098-145">Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer neuen Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz](#new-new) weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="af098-145">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and a new instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and a new customer engagement app instance](#new-new) section earlier in this topic.</span></span> <span data-ttu-id="af098-146">Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der Customer Engagement Anwendung synchronisieren möchten, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="af098-146">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="af098-147">Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.</span><span class="sxs-lookup"><span data-stu-id="af098-147">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="af098-148">Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="af098-148">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="af098-149">Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).</span><span class="sxs-lookup"><span data-stu-id="af098-149">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a><span data-ttu-id="af098-150">Eine neue Finance and Operations App-Instanz, die über Demodaten verfügt, und eine bestehende Customer Engagement App-Instanz</span><span class="sxs-lookup"><span data-stu-id="af098-150">A new Finance and Operations app instance that has data and an existing customer engagement app instance</span></span>

<span data-ttu-id="af098-151">Um eine Verbindung duales Schreiben zwischen einer neuen Instanz einer Finance and Operations-Anwendung, die über Demodaten verfügt, und einer bestehenden Instanz einer Customer Engagement Anwendung einzurichten, folgen Sie den Schritten im Abschnitt [Eine neue Finance and Operations-Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz](#new-existing) weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="af098-151">To set up a dual-write connection between a new instance of a Finance and Operations app that has data and an existing instance of a customer engagement app, follow the steps in the [A new Finance and Operations app instance and an existing customer engagement app instance](#new-existing) section earlier in this topic.</span></span> <span data-ttu-id="af098-152">Wenn der Verbindungsaufbau abgeschlossen ist und Sie die Demodaten mit der Customer Engagement Anwendung synchronisieren möchten, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="af098-152">When the connection setup is completed, if you want to sync the data to the customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="af098-153">Öffnen Sie die Anwendung Finance and Operations von der LCS-Seite, melden Sie sich an und gehen Sie dann zu **Datenverwaltung \> Dual-write**.</span><span class="sxs-lookup"><span data-stu-id="af098-153">Open the Finance and Operations app from the LCS page, sign in, and then go to **Data Management \> Dual-write**.</span></span>
2. <span data-ttu-id="af098-154">Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="af098-154">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="af098-155">Um die vorhandenen Dataverse-Daten mit der Finance and Operations-Anwendung zu synchronisieren, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="af098-155">To sync the existing Dataverse data to the Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="af098-156">Erstellen Sie ein neues Unternehmen in der Finance and Operations-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="af098-156">Create a new company in the Finance and Operations app.</span></span>
2. <span data-ttu-id="af098-157">Fügen Sie das Unternehmen zum Dual-Write-Verbindungsaufbau hinzu.</span><span class="sxs-lookup"><span data-stu-id="af098-157">Add the company to the dual-write connection setup.</span></span>
3. <span data-ttu-id="af098-158">[Bootstrap](bootstrap-company-data.md) der Dataverse-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungscodees.</span><span class="sxs-lookup"><span data-stu-id="af098-158">[Bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
4. <span data-ttu-id="af098-159">Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="af098-159">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="af098-160">Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).</span><span class="sxs-lookup"><span data-stu-id="af098-160">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a><span data-ttu-id="af098-161">Eine bestehende Finance and Operations Anwendungsinstanz und eine neue Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-161">An existing Finance and Operations app instance and a new customer engagement app instance</span></span>

<span data-ttu-id="af098-162">Die Einrichtung einer Verbindung duales Schreiben zwischen einer bestehenden Instanz einer Finance and Operations-Anwendung und einer neuen Instanz einer Customer Engagement Anwendung erfolgt in der Finance and Operation-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="af098-162">The setup of a dual-write connection between an existing instance of a Finance and Operations app and a new instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="af098-163">[Richten Sie die Verbindung von der Finance and Operations-Anwendung aus ein](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="af098-163">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="af098-164">Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="af098-164">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="af098-165">Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).</span><span class="sxs-lookup"><span data-stu-id="af098-165">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a><span data-ttu-id="af098-166">Eine bestehende Finance and Operations Anwendungsinstanz und eine bestehende Customer Engagement Anwendungsinstanz</span><span class="sxs-lookup"><span data-stu-id="af098-166">An existing Finance and Operations app instance and an existing customer engagement app instance</span></span>

<span data-ttu-id="af098-167">Die Einrichtung einer Verbindung für duales Schreiben zwischen einer bestehenden Instanz einer Finance and Operations-App und einer bestehenden Instanz einer Customer Engagement-App erfolgt in der Finance and Operation-Umgebung.</span><span class="sxs-lookup"><span data-stu-id="af098-167">The setup of a dual-write connection between an existing instance of a Finance and Operations app and an existing instance of a customer engagement app occurs in the Finance and Operation environment.</span></span>

1. <span data-ttu-id="af098-168">[Richten Sie die Verbindung von der Finance and Operations-Anwendung aus ein](enable-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="af098-168">[Set up the connection from the Finance and Operations app](enable-dual-write.md).</span></span>
2. <span data-ttu-id="af098-169">Um die vorhandenen Dataverse-Daten mit der Finance and Operations-Anwendung zu synchronisieren, [Bootstrap](bootstrap-company-data.md) die Dataverse-Daten unter Verwendung eines dreibuchstabigen ISO-Buchungskreises.</span><span class="sxs-lookup"><span data-stu-id="af098-169">To sync the existing Dataverse data to the Finance and Operations app, [bootstrap](bootstrap-company-data.md) the Dataverse data by using a three-letter ISO company code.</span></span>
3. <span data-ttu-id="af098-170">Führen Sie die Funktion **Erstsynchronisierung** für die Tabellen aus, für die Sie Daten synchronisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="af098-170">Run the **Initial sync** functionality for the tables that you want to sync data for.</span></span>

<span data-ttu-id="af098-171">Links zu einem Beispiel und einem alternativen Ansatz finden Sie im Abschnitt [Beispiel](#example).</span><span class="sxs-lookup"><span data-stu-id="af098-171">For links to an example and an alternative approach, see the [Example](#example) section.</span></span>

## <a name="example"></a><span data-ttu-id="af098-172">Beispiel</span><span class="sxs-lookup"><span data-stu-id="af098-172">Example</span></span>

<span data-ttu-id="af098-173">Ein Beispiel finden Sie unter [Aktivieren der Tabellenzuordnung für Kunden V3 – Kontakte](enable-entity-map.md#enable-table-map).</span><span class="sxs-lookup"><span data-stu-id="af098-173">For an example, see [Enabling the Customers V3—Contacts table map](enable-entity-map.md#enable-table-map)</span></span>

<span data-ttu-id="af098-174">Einen alternativen Ansatz basierend auf den Datenmengen in jeder Entität, für die eine Erstsynchronisierung ausgeführt werden muss, finden Sie unter [Überlegungen zur Erstsynchronisierung](initial-sync-guidance.md).</span><span class="sxs-lookup"><span data-stu-id="af098-174">For an alternative approach that is based on data volumes in each entity that must run an initial synchronization, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>
