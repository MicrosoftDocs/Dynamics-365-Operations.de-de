---
title: Überprüfen der Konfiguration von dualem Schreiben in Finance and Operations-Apps und Dataverse
description: In diesem Thema wird erläutert, wie Sie feststellen können, ob duales Schreiben in Finance and Operations Apps und in Dataverse konfiguriert ist.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748848"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="f510f-103">Überprüfen der Konfiguration von dualem Schreiben in Finance and Operations-Apps und Dataverse</span><span class="sxs-lookup"><span data-stu-id="f510f-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="f510f-104">Dieses Thema enthält Problembehandlungsinformationen zur dualen Schreibintegration zwischen den Apps Finance and Operations und Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f510f-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="f510f-105">In diesem Thema wird speziell erläutert, wie Sie feststellen können, ob Dual-Write in Finance and Operations Apps und in Dataverse konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f510f-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="f510f-106">Überprüfen, ob duales Schreiben in Finance and Operations Apps konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="f510f-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="f510f-107">Um festzustellen, ob die Fehler, die beim Speichern von Zeilen für die Aktualisierung angezeigt werden, auf Dual-Write zurückzuführen sind, überprüfen Sie zunächst, ob Dual-Write konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="f510f-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="f510f-108">Wenn Sie Administratorrechte in der Finance and Operations App haben, gehen Sie zu **Arbeitsbereiche \> Datenmanagement** und wählen Sie die Kachel **Duales Schreiben**.</span><span class="sxs-lookup"><span data-stu-id="f510f-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="f510f-109">Wenn die Details der verknüpften Umgebungen und die Liste der ausgeführten Tabellenzuordnungen angezeigt werden, ist Dual-Write konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f510f-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über Administratorrechte verfügen](media/verify_fin_ops_1.png)

+ <span data-ttu-id="f510f-111">Wenn Sie keine Administratorrechte haben, erhalten Sie eine Fehlermeldung: *Daten können nicht in die Entität geschrieben werden \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="f510f-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="f510f-112">Im Beispiel in der folgenden Abbildung können Sie keine Kundenzeile in der Finance and Operations-App erstellen, da Dual-Write konfiguriert ist, die Referenzdaten für die Kundengruppe und die Zahlungsbedingungen in Dataverse jedoch nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="f510f-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Überprüfen der Finance and Operations App-Verbindung, wenn Sie über keine Administratorrechte verfügen](media/verify_fin_ops_2.png)

<span data-ttu-id="f510f-114">Informationen zum Beheben von Problemen beim Erstellen von Daten in Finance and Operations Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f510f-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="f510f-115">Überprüfen, ob duales Schreiben in Dataverse Apps konfiguriert ist</span><span class="sxs-lookup"><span data-stu-id="f510f-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="f510f-116">Wenn Sie Daten erstellen, sehen Sie die Spalte **Unternehmen** auf Seiten in Dataverse. Duales Schreiben ist konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="f510f-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Überprüfen der Dataverse Verbindung](media/verify_cds.png)

<span data-ttu-id="f510f-118">Informationen zum Beheben von Problemen beim Erstellen von Daten in Dataverse Apps, siehe [Beheben Sie Probleme mit der Live-Synchronisierung](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="f510f-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="f510f-119">Informationen zum Anzeigen von Fehlerdetails, wenn beim Erstellen von Daten Fehler auftreten Dataverse, gehen Sie zu [Aktivieren und Anzeigen der Plug-In-Ablaufverfolgungsanmeldung Dataverse, um Fehlerdetails anzuzeigen](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="f510f-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]