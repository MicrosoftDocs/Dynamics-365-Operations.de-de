---
title: Direktimport/-export verwenden
description: "Zweck des Direktimports/-exports ist der Import und Export über weniger Schritte."
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4bb5bf73210abfc3fc06f7f291ae60fdf4298b71
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="run-the-test-data-transfer-tool-beta-for-dynamics-ax-ax-2012"></a><span data-ttu-id="9f543-103">Führen Test Data Transfer Tool (Beta) für Dynamics AX (AX 2012) aus</span><span class="sxs-lookup"><span data-stu-id="9f543-103">Run the Test Data Transfer Tool (beta) for Dynamics AX (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9f543-104">Zweck des Direktimports/-exports ist der Import und Export über weniger Schritte.</span><span class="sxs-lookup"><span data-stu-id="9f543-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="9f543-105">Wir haben eine Funktion für den Direktimport/-export hinzugefügt, um den Benutzer den schnellen Import oder Export von einfachen Einzelaufträgen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9f543-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="9f543-106">Die Funktion wird im Idealfall in Szenarien genutzt, in denen eine Datei automatisch zum System zugeordnet wird und der Benutzer keine erweiterte Zuordnung durchführen oder wiederholt Import- oder Exportvorgänge erstellen muss.</span><span class="sxs-lookup"><span data-stu-id="9f543-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="9f543-107">Diese Funktion unterstützt die Arbeit mit standardmäßigen und angepassten Entitäten.</span><span class="sxs-lookup"><span data-stu-id="9f543-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="9f543-108">Sie können aus Dateien importieren. Wenn Sie eine ODBC-Datenquelle verwenden, können Sie eine Abfrage zum Definieren des Imports auswählen.</span><span class="sxs-lookup"><span data-stu-id="9f543-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="9f543-109">Sie müssen zuvor Quelldatenformate für "AX" oder "Datei" definiert haben und deren Speicherort kennen.</span><span class="sxs-lookup"><span data-stu-id="9f543-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="9f543-110">Sie müssen keine Verarbeitungsgruppe für den Direktimport/-export erstellen. Das System erstellt bei der Ausführung automatisch eine Verarbeitungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9f543-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="9f543-111">Sie können außerdem den Verlauf der importieren/exportieren Daten speichern.</span><span class="sxs-lookup"><span data-stu-id="9f543-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="9f543-112">Beachten Sie, dass der Direktimport/-export davon ausgeht, dass Sie mit den DIXF-Konzepten vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="9f543-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>




