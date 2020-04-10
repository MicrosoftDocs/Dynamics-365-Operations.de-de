---
title: Überprüfen, ob duales Schreiben in Finance and Operations-Apps und Common Data Service konfiguriert ist
description: In diesem Thema wird erläutert, wie Sie feststellen können, ob duales Schreiben in Finance and Operations Apps und in Common Data Service konfiguriert ist.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172644"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="02bee-103">Überprüfen, ob duales Schreiben in Finance and Operations-Apps und Common Data Service konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="02bee-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="02bee-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="02bee-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="02bee-105">In diesem Thema wird speziell erläutert, wie Sie feststellen können, ob Dual-Write in Finance and Operations Apps und in Common Data Service konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="02bee-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="02bee-106">Überprüfen, ob duales Schreiben in Finance and Operations Apps konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="02bee-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="02bee-107">Um festzustellen, ob die Fehler, die beim Speichern von Datensätzen für die Aktualisierung angezeigt werden, auf Dual-Write zurückzuführen sind, überprüfen Sie zunächst, ob Dual-Write konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="02bee-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="02bee-108">Wenn Sie Administratorrechte in der Finance and Operations App haben, gehen Sie zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**.</span><span class="sxs-lookup"><span data-stu-id="02bee-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="02bee-109">Wenn die Details der verknüpften Umgebungen und die Liste der ausgeführten Entitätszuordnungen angezeigt werden, ist Dual-Write konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="02bee-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über Administratorrechte verfügen](media/verify_fin_ops_1.png)

+ <span data-ttu-id="02bee-111">Wenn Sie keine Administratorrechte haben, erhalten Sie eine Fehlermeldung: *Daten können nicht in die Entität geschrieben werden \<Entitätsname\>*.</span><span class="sxs-lookup"><span data-stu-id="02bee-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="02bee-112">Im Beispiel in der folgenden Abbildung können Sie keinen Kundendatensatz in der Finance and Operations App erstellen, da Dual-Write konfiguriert ist, die Referenzdaten für Kundengruppe und Zahlungsbedingungen jedoch nicht vorhanden sind in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="02bee-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über keine Administratorrechte verfügen](media/verify_fin_ops_2.png)

<span data-ttu-id="02bee-114">Informationen zum Beheben von Problemen beim Erstellen von Daten in Finance and Operations Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="02bee-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="02bee-115">Überprüfen, ob duales Schreiben in Common Data Service Apps konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="02bee-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="02bee-116">Wenn Sie Daten erstellen, sehen Sie das Feld **Unternehmen** auf Seiten in Common Data Service. Dual-Write ist konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="02bee-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Überprüfen der Common Data Service Verbindung](media/verify_cds.png)

<span data-ttu-id="02bee-118">Informationen zum Beheben von Problemen beim Erstellen von Daten in Common Data Service Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="02bee-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="02bee-119">Informationen zum Anzeigen von Fehlerdetails, wenn beim Erstellen von Daten Fehler auftreten Common Data Service, gehen Sie zu [Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Common Data Service, um Fehlerdetails anzuzeigen](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="02bee-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
