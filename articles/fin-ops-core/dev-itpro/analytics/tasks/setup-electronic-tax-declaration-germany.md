---
title: Einrichtung der elektronischen Steuererklärung für Deutschland
description: Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxElectronicDeclarationSetup, TaxElectronicCertificates, TaxElectronicHTTPServer
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Germany
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a125d0e138824b74388a27d0011c3e23f6b092a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143143"
---
# <a name="set-up-electronic-tax-declaration-for-germany"></a><span data-ttu-id="c03e6-103">Einrichtung der elektronischen Steuererklärung für Deutschland</span><span class="sxs-lookup"><span data-stu-id="c03e6-103">Set up electronic Tax declaration for Germany</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c03e6-104">Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch.</span><span class="sxs-lookup"><span data-stu-id="c03e6-104">This procedure walks you through setting electronic tax declaration.</span></span>

<span data-ttu-id="c03e6-105">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="c03e6-105">This procedure was created using the demo data company DEMF.</span></span> 

<span data-ttu-id="c03e6-106">Diese Funktion ist für juristische Personen verfügbar, deren primäre Adresse sich in Deutschland befindet.</span><span class="sxs-lookup"><span data-stu-id="c03e6-106">This functionality is available for legal entities whose primary address is in Germany.</span></span>

<span data-ttu-id="c03e6-107">Sie sollten ein gültiges Zertifikat (wie test-soft-pse.pfx) und eine Steuerbehördenbescheinigung (Coala2019.pem.cer) verwenden bevor Sie dieses Verfahren ausführen können.</span><span class="sxs-lookup"><span data-stu-id="c03e6-107">You should have a valid user certificate (like test-soft-pse.pfx) and a Tax authority certificate (Coala2019.pem.cer) before you can complete this procedure.</span></span>


1. <span data-ttu-id="c03e6-108">Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "Einrichtung der elektronischen Steuererklärung".</span><span class="sxs-lookup"><span data-stu-id="c03e6-108">Go to Tax > Setup > Sales tax > Electronic tax declaration setup.</span></span>
2. <span data-ttu-id="c03e6-109">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="c03e6-109">Click Edit.</span></span>
3. <span data-ttu-id="c03e6-110">Wählen Sie "Ja" im Feld "Authentifizierung".</span><span class="sxs-lookup"><span data-stu-id="c03e6-110">Select Yes in the Authentication field.</span></span>
4. <span data-ttu-id="c03e6-111">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c03e6-111">In the Format mapping field, enter or select a value.</span></span>
    * <span data-ttu-id="c03e6-112">Wie eine Komponente, die Sie von Konfiguration Kreditbriefen Elster (Modell und Stil) für generische elektronische Berichterstellung hochladen sollen.</span><span class="sxs-lookup"><span data-stu-id="c03e6-112">As a prerequisite you should upload from LCS Elster configuration (model and format) for Generic electronic reporting.</span></span>  
5. <span data-ttu-id="c03e6-113">Elektronische Steuerzertifikate anklicken</span><span class="sxs-lookup"><span data-stu-id="c03e6-113">Click Electronic tax certificates.</span></span>
6. <span data-ttu-id="c03e6-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="c03e6-114">Click New.</span></span>
7. <span data-ttu-id="c03e6-115">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c03e6-115">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="c03e6-116">Sie sollten Bescheinigungen nach Microsoft Management Console zunächst einrichten und Anzeigenamen zuweisen, die in diesen Schritten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c03e6-116">You should first install certificates through Microsoft Management Console and assign friendly names that will be used in these steps.</span></span>  
    * <span data-ttu-id="c03e6-117">In MMC für private Bescheinigung gehen Sie mit einem rechten Mausklcik zu Zertifikate / Personal/ Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="c03e6-117">In MMC for private certificate go to "Certificates / Personal /Certificates", right mouse click.</span></span> 
    * <span data-ttu-id="c03e6-118">Klicken Sie im Kontextmenü auf „Alle Aufgaben > Import“.</span><span class="sxs-lookup"><span data-stu-id="c03e6-118">In the context menu, click All Tasks > Import.</span></span> <span data-ttu-id="c03e6-119">Gewähren Sie Leseberechtigungen der Bescheinigung für den Benutzer, der die Übermittlung an.</span><span class="sxs-lookup"><span data-stu-id="c03e6-119">Grant read permissions to the certificate for the user who is doing the submission.</span></span>     <span data-ttu-id="c03e6-120">\* Klicken Sie in der MMC mit der rechten Maustaste auf das Zertifikat und verwenden Sie „Alle Aufgaben/Private Schlüssel verwalten“.</span><span class="sxs-lookup"><span data-stu-id="c03e6-120">\* In MMC, right click the certificate and use All Tasks/Manage Private Keys.</span></span> 
    * <span data-ttu-id="c03e6-121">Wählen Sie den Benutzer aus und fügen Sie eine Leseberechtigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="c03e6-121">Select the user and add read permission.</span></span>  
    * <span data-ttu-id="c03e6-122">Bei einem Steuerbehördenzertifikat klicken Sie in MMC mit der rechten Maustaste auf „Vertrauenswürdige Stammzertifizierungsstelle“</span><span class="sxs-lookup"><span data-stu-id="c03e6-122">For Tax authority certificate in MMC, right-click "Trusted Root Certificate Authorities"</span></span>  
    * <span data-ttu-id="c03e6-123">Importieren Sie „Coala2019.pem.cer“.</span><span class="sxs-lookup"><span data-stu-id="c03e6-123">Import "Coala2019.pem.cer".</span></span>  
8. <span data-ttu-id="c03e6-124">Geben Sie im Feld Wert einen Referenztyp ein.</span><span class="sxs-lookup"><span data-stu-id="c03e6-124">In the Certificates reference field, type a value.</span></span>
9. <span data-ttu-id="c03e6-125">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c03e6-125">Click Save.</span></span>
10. <span data-ttu-id="c03e6-126">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c03e6-126">Close the page.</span></span>
11. <span data-ttu-id="c03e6-127">Klicken Sie auf HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="c03e6-127">Click HTTP servers.</span></span>
    * <span data-ttu-id="c03e6-128">HTTP-URL-Adressen werden aus der Behörde bereitgestellt und können von der Behörde geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c03e6-128">HTTP url addresses are provided by the authority and can be changed by the authority.</span></span> <span data-ttu-id="c03e6-129">Microsoft stellt Standardadressen, die vom System zufällig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c03e6-129">Microsoft provides default addresses that are used by the system randomly.</span></span>  
12. <span data-ttu-id="c03e6-130">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c03e6-130">Click Save.</span></span>
13. <span data-ttu-id="c03e6-131">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="c03e6-131">Close the page.</span></span>
14. <span data-ttu-id="c03e6-132">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="c03e6-132">Click Save.</span></span>

