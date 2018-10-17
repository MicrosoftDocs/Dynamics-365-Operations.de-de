--- 
title: "Formular \"Einrichtung der elektronischen Steuererklärung\" für Deutschland"
description: "Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxElectronicDeclarationSetup, TaxElectronicCertificates, TaxElectronicHTTPServer
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Germany
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: fbff209963828ab85bdc5ccf800a97ddaf864c0d
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2018

---
# <a name="setup-electronic-tax-declaration-for-germany"></a><span data-ttu-id="f1712-103">Formular "Einrichtung der elektronischen Steuererklärung" für Deutschland</span><span class="sxs-lookup"><span data-stu-id="f1712-103">Setup electronic Tax declaration for Germany</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1712-104">Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch.</span><span class="sxs-lookup"><span data-stu-id="f1712-104">This procedure walks you through setting electronic tax declaration.</span></span>

<span data-ttu-id="f1712-105">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="f1712-105">This procedure was created using the demo data company DEMF.</span></span> 

<span data-ttu-id="f1712-106">Diese Funktion ist für juristische Personen verfügbar, deren primäre Adresse sich in Deutschland befindet.</span><span class="sxs-lookup"><span data-stu-id="f1712-106">This functionality is available for legal entities whose primary address is in Germany.</span></span>

<span data-ttu-id="f1712-107">Sie sollten ein gültiges Zertifikat (wie test-soft-pse.pfx) und eine Steuerbehördenbescheinigung (Coala2019.pem.cer) verwenden bevor Sie dieses Verfahren ausführen können.</span><span class="sxs-lookup"><span data-stu-id="f1712-107">You should have a valid user certificate (like test-soft-pse.pfx) and a Tax authority certificate (Coala2019.pem.cer) before you can complete this procedure.</span></span>



1. <span data-ttu-id="f1712-108">Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "Einrichtung der elektronischen Steuererklärung".</span><span class="sxs-lookup"><span data-stu-id="f1712-108">Go to Tax > Setup > Sales tax > Electronic tax declaration setup.</span></span>
2. <span data-ttu-id="f1712-109">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="f1712-109">Click Edit.</span></span>
3. <span data-ttu-id="f1712-110">Wählen Sie "Ja" im Feld "Authentifizierung".</span><span class="sxs-lookup"><span data-stu-id="f1712-110">Select Yes in the Authentication field.</span></span>
4. <span data-ttu-id="f1712-111">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f1712-111">In the Format mapping field, enter or select a value.</span></span>
    * <span data-ttu-id="f1712-112">Wie eine Komponente, die Sie von Konfiguration Kreditbriefen Elster (Modell und Stil) für generische elektronische Berichterstellung hochladen sollen.</span><span class="sxs-lookup"><span data-stu-id="f1712-112">As a prerequisite you should upload from LCS Elster configuration (model and format) for Generic electronic reporting.</span></span>  
5. <span data-ttu-id="f1712-113">Elektronische Steuerzertifikate anklicken</span><span class="sxs-lookup"><span data-stu-id="f1712-113">Click Electronic tax certificates.</span></span>
6. <span data-ttu-id="f1712-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="f1712-114">Click New.</span></span>
7. <span data-ttu-id="f1712-115">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="f1712-115">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="f1712-116">Sie sollten Bescheinigungen nach Microsoft Management Console zunächst einrichten und Anzeigenamen zuweisen, die in diesen Schritten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1712-116">You should first install certificates through Microsoft Management Console and assign friendly names that will be used in these steps.</span></span>  <span data-ttu-id="f1712-117">In MMC für private Bescheinigung "in den Bescheinigungen/zu persönliche /Certificates", fahren rechten Mausklick.</span><span class="sxs-lookup"><span data-stu-id="f1712-117">In MMC for private certificate go to “Certificates / Personal /Certificates”, right mouse click.</span></span>  <span data-ttu-id="f1712-118">Im Kontextmenü klicken Sie auf Alle Aufgaben > auf Importieren…. Gewähren Sie Leseberechtigungen der Bescheinigung für den Benutzer, der die Übermittlung ausführt.</span><span class="sxs-lookup"><span data-stu-id="f1712-118">In the context menu click All Tasks > Import....  Grant read permissions to the certificate for the user who is doing the submission.</span></span>  <span data-ttu-id="f1712-119">In MMC klicken Sie auf der Bescheinigung mit der rechten Maustaste, und verwenden Sie alle Aufgaben/Verwalten von private Schlüssel - Wählen Sie den Benutzer aus und fügen Sie Leseberechtigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="f1712-119">In MMC Right click on the certificate and use All Tasks/Manage Private Keys – select the user and add read permission.</span></span>  <span data-ttu-id="f1712-120">Für Steuerbehördenbescheinigung MMC-Rechtsklick "vertraute im Stammzertifikats-" Import " Coala2019.pem.cer".</span><span class="sxs-lookup"><span data-stu-id="f1712-120">For Tax authority certificate in MMC right-click “Trusted Root Certificate Authorities”  Import "Coala2019.pem.cer".</span></span>  
8. <span data-ttu-id="f1712-121">Geben Sie im Feld Wert einen Referenztyp ein.</span><span class="sxs-lookup"><span data-stu-id="f1712-121">In the Certificates reference field, type a value.</span></span>
9. <span data-ttu-id="f1712-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f1712-122">Click Save.</span></span>
10. <span data-ttu-id="f1712-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1712-123">Close the page.</span></span>
11. <span data-ttu-id="f1712-124">Klicken Sie auf HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="f1712-124">Click HTTP servers.</span></span>
    * <span data-ttu-id="f1712-125">HTTP-URL-Adressen werden aus der Behörde bereitgestellt und können von der Behörde geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f1712-125">HTTP url addresses are provided by the authority and can be changed by the authority.</span></span> <span data-ttu-id="f1712-126">Microsoft stellt Standardadressen, die vom System zufällig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f1712-126">Microsoft provides default addresses that are used by the system randomly.</span></span>  
12. <span data-ttu-id="f1712-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f1712-127">Click Save.</span></span>
13. <span data-ttu-id="f1712-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="f1712-128">Close the page.</span></span>
14. <span data-ttu-id="f1712-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="f1712-129">Click Save.</span></span>


