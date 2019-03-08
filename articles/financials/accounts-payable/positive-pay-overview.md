---
title: Überblick über die positive Zahlung
description: In diesem Artikel finden Sie Informationen über positive Zahlungen, die zur Generierung einer elektronischen Liste mit Schecks verwendet werden, die für die Bank bereitgestellt wird.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a7af2fc0e2c9915c4267f60e27dbddac320af6a5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "315175"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="1bfe4-103">Überblick über die positive Zahlung</span><span class="sxs-lookup"><span data-stu-id="1bfe4-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1bfe4-104">In diesem Artikel finden Sie Informationen über positive Zahlungen, die zur Generierung einer elektronischen Liste mit Schecks verwendet werden, die für die Bank bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="1bfe4-105">Positive Zahlungen werden zur Generierung einer elektronischen Liste mit Schecks verwendet, die für die Bank bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="1bfe4-106">Positive Lohndateien können Scheckbetrug verhindern.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="1bfe4-107">Sie richten positiven Zahlungen ein, um eine elektronische Liste mit Schecks zu generieren, wenn Schecks gedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="1bfe4-108">Wenn der Scheck der Bank präsentiert wird, vergleicht die Bank den Scheck mit der Liste der Schecks, die zuvor eingereicht gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="1bfe4-109">Wenn der Originalscheck mit einem Scheck in der Liste übereinstimmt, löscht die Bank den Scheck.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="1bfe4-110">Wenn der Scheck mit keinem Scheck iin der Liste übereinstimmt, hält die Bank den Scheck zur Prüfung zurück.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="1bfe4-111">Positiver Lohn wird auch als SafePay bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="1bfe4-112">Positive Lohndateien können vertrauliche Informationen zu Zahlungsempfänger und Scheckbeträgen enthalten.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="1bfe4-113">Daher stellen Sie sicher, dass Sie entsprechende Sicherheitspraktiken ab dem Zeitpunkt verwenden, an dem die Dateien generiert werden, bis sie von der Bank empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="1bfe4-114">Dateien für positive Zahlungen werden gemäß den Downloadanweisungen für den Webbrowser heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="1bfe4-115">Dateien für positive Zahlungen werden über Datenentitäten erstellt.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="1bfe4-116">Bevor Sie eine Datei für positive Zahlungen generieren, müssen Sie die Transformationsformate für das XML einrichten, das die Daten in ein Format übersetzt, das die Bank verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="1bfe4-117">Jedem Bankkonto, für das Sie positive Erfassung von Lohndaten generieren möchten, müssen Sie das positive Lohnformat zuweisen.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="1bfe4-118">Nach der Generierung der Zahlungen können Sie eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto generieren.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="1bfe4-119">Alternativ können Sie Dateien für positive Zahlungen für mehrere juristische Personen und Bankkonten gleichzeitig generieren.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="1bfe4-120">Nachdem die Schecks, die in einer positiven Lohndatei aufgeführt sind, bezahlt wurden, erhalten Sie eine Bestätigungsnummer von der Bank.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="1bfe4-121">Anschließend können Sie die positive Lohndatei in Microsoft Dynamics 365 for Finance and Operations bestätigen.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="1bfe4-122">Wenn Sie eine Datei für positive Zahlungen ändern müssen, können Sie diese erneut aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="1bfe4-123">Für jeden Scheck in der positiven Lohndatei zeigt das Feld an, ob der Scheck in einer positiven Lohndatei zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="1bfe4-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="1bfe4-124">Weitere Informationen finden Sie unter [Einrichten und Generieren von Dateien für positive Zahlungen](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="1bfe4-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>



