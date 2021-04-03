---
title: Aktualisiert die zusammengesetzte Bankerfassungs-Entität
description: Gehen Sie folgendermaßen vor, um das zusätzliche Feld "BankTransactionType" der zusammengesetzten BankJournalEntity hinzuzufügen.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 18137ca8cecc43b4269f14b36df2eb8063192e52
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236346"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="217d0-103">Aktualisiert die zusammengesetzte Bankerfassungs-Entität</span><span class="sxs-lookup"><span data-stu-id="217d0-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="217d0-104">Gehen Sie folgendermaßen vor, um das zusätzliche Feld "BankTransactionType" der zusammengesetzten BankJournalEntity hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="217d0-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="217d0-105">Gehen Sie folgendermaßen vor, um den BankTransactionType-Feld der zusammengesetzten BankJournalEntity hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="217d0-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="217d0-106">Kompilieren und synchronisieren Sie die folgenden zusammengesetzten Bankerfassungsentitäten, Entitäten und Stagingtabellen:</span><span class="sxs-lookup"><span data-stu-id="217d0-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="217d0-107">Zusammengesetzte Entität\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="217d0-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="217d0-108">Entität\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="217d0-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="217d0-109">Entität\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="217d0-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="217d0-110">Tabelle\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="217d0-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="217d0-111">Tabelle\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="217d0-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="217d0-112">Datenverwaltung\\Datenprojekte</span><span class="sxs-lookup"><span data-stu-id="217d0-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="217d0-113">Macht den Typ **Banktransaktion** im Layout **Quelldaten** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="217d0-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="217d0-114">Quelldatenformat = XML-Element</span><span class="sxs-lookup"><span data-stu-id="217d0-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="217d0-115">Entitätsname j= Bankerfassung</span><span class="sxs-lookup"><span data-stu-id="217d0-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="217d0-116">Laden Sie die Datendatei hoch = neue Version SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="217d0-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="217d0-117">Klicken Sie auf **Ja**, um die vorhandene Datei zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="217d0-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="217d0-118">Klicken Sie auf **Ja**, um eine neue Zuordnung von Beginn her zu generieren.</span><span class="sxs-lookup"><span data-stu-id="217d0-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="217d0-119">Überprüfen Sie, dass der Banktransaktionstyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="217d0-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="217d0-120">Klicken Sie auf **Zuordnung anzeigen** auf der Positionsentität.</span><span class="sxs-lookup"><span data-stu-id="217d0-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="217d0-121">Überprüfen Sie, dass der Banktransaktionstyp von der Quelle zum Bereitstellen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="217d0-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="217d0-122">Importieren Sie den neuen Auszug.</span><span class="sxs-lookup"><span data-stu-id="217d0-122">Import the new statement.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]