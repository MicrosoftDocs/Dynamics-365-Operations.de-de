---
title: DE-00003 Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)
description: Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxElectronicDeclarationSetup, TaxElectronicCertificates, TaxElectronicHTTPServer
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7e5857fcbd4aeedca6e195c80b2391ba206184e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822629"
---
# <a name="de-00003-electronic-transmission-of-vat-declaration-elster"></a><span data-ttu-id="876e7-103">DE-00003 Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)</span><span class="sxs-lookup"><span data-stu-id="876e7-103">DE-00003 Electronic transmission of VAT declaration (ELSTER)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="876e7-104">Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch.</span><span class="sxs-lookup"><span data-stu-id="876e7-104">This procedure walks you through setting electronic tax declaration.</span></span>

<span data-ttu-id="876e7-105">Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt.</span><span class="sxs-lookup"><span data-stu-id="876e7-105">This procedure was created using the demo data company DEMF.</span></span> 

<span data-ttu-id="876e7-106">Diese Funktion ist für juristische Personen verfügbar, deren primäre Adresse sich in Deutschland befindet.</span><span class="sxs-lookup"><span data-stu-id="876e7-106">This functionality is available for legal entities whose primary address is in Germany.</span></span>

<span data-ttu-id="876e7-107">Sie sollten ein gültiges Zertifikat (wie test-soft-pse.pfx) und eine Steuerbehördenbescheinigung (Coala2019.pem.cer) verwenden bevor Sie dieses Verfahren ausführen können.</span><span class="sxs-lookup"><span data-stu-id="876e7-107">You should have a valid user certificate (like test-soft-pse.pfx) and a Tax authority certificate (Coala2019.pem.cer) before you can complete this procedure.</span></span>



1. <span data-ttu-id="876e7-108">Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "Einrichtung der elektronischen Steuererklärung".</span><span class="sxs-lookup"><span data-stu-id="876e7-108">Go to Tax > Setup > Sales tax > Electronic tax declaration setup.</span></span>
2. <span data-ttu-id="876e7-109">Klicken Sie auf "Bearbeiten".</span><span class="sxs-lookup"><span data-stu-id="876e7-109">Click Edit.</span></span>
3. <span data-ttu-id="876e7-110">Wählen Sie "Ja" im Feld "Authentifizierung".</span><span class="sxs-lookup"><span data-stu-id="876e7-110">Select Yes in the Authentication field.</span></span>
4. <span data-ttu-id="876e7-111">Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="876e7-111">In the Format mapping field, enter or select a value.</span></span>
    * <span data-ttu-id="876e7-112">Wie eine Komponente, die Sie von Konfiguration Kreditbriefen Elster (Modell und Stil) für generische elektronische Berichterstellung hochladen sollen.</span><span class="sxs-lookup"><span data-stu-id="876e7-112">As a prerequisite you should upload from LCS Elster configuration (model and format) for Generic electronic reporting.</span></span>  
5. <span data-ttu-id="876e7-113">Elektronische Steuerzertifikate anklicken</span><span class="sxs-lookup"><span data-stu-id="876e7-113">Click Electronic tax certificates.</span></span>
6. <span data-ttu-id="876e7-114">Klicken Sie auf "Neu".</span><span class="sxs-lookup"><span data-stu-id="876e7-114">Click New.</span></span>
7. <span data-ttu-id="876e7-115">Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="876e7-115">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="876e7-116">Sie sollten Bescheinigungen nach Microsoft Management Console zunächst einrichten und Anzeigenamen zuweisen, die in diesen Schritten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="876e7-116">You should first install certificates through Microsoft Management Console and assign friendly names that will be used in these steps.</span></span>  <span data-ttu-id="876e7-117">In MMC für private Bescheinigung gehen Sie mit einem rechten Mausklcik zu Zertifikate / Personal/ Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="876e7-117">In MMC for private certificate go to "Certificates / Personal /Certificates", right mouse click.</span></span>  <span data-ttu-id="876e7-118">Im Kontextmenü klicken Sie auf Alle Aufgaben > auf Importieren…. Gewähren Sie Leseberechtigungen der Bescheinigung für den Benutzer, der die Übermittlung ausführt.</span><span class="sxs-lookup"><span data-stu-id="876e7-118">In the context menu click All Tasks > Import....  Grant read permissions to the certificate for the user who is doing the submission.</span></span>  <span data-ttu-id="876e7-119">In MMC klicken Sie auf der Bescheinigung mit der rechten Maustaste, und verwenden Sie alle Aufgaben/Verwalten von private Schlüssel - Wählen Sie den Benutzer aus und fügen Sie Leseberechtigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="876e7-119">In MMC Right click on the certificate and use All Tasks/Manage Private Keys – select the user and add read permission.</span></span>  <span data-ttu-id="876e7-120">Für Steuerbehördenbescheinigung klicken Sie in MMC mit der rechten Maustaste auf „Vertrauenswürdige Stammzertifizierungsstelle“ und importieren Sie „Coala2019.pem.cer“.</span><span class="sxs-lookup"><span data-stu-id="876e7-120">For Tax authority certificate in MMC right-click "Trusted Root Certificate Authorities"  Import "Coala2019.pem.cer".</span></span>  
8. <span data-ttu-id="876e7-121">Geben Sie im Feld Wert einen Referenztyp ein.</span><span class="sxs-lookup"><span data-stu-id="876e7-121">In the Certificates reference field, type a value.</span></span>
9. <span data-ttu-id="876e7-122">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="876e7-122">Click Save.</span></span>
10. <span data-ttu-id="876e7-123">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="876e7-123">Close the page.</span></span>
11. <span data-ttu-id="876e7-124">Klicken Sie auf HTTP-Server.</span><span class="sxs-lookup"><span data-stu-id="876e7-124">Click HTTP servers.</span></span>
    * <span data-ttu-id="876e7-125">HTTP-URL-Adressen werden aus der Behörde bereitgestellt und können von der Behörde geändert werden.</span><span class="sxs-lookup"><span data-stu-id="876e7-125">HTTP url addresses are provided by the authority and can be changed by the authority.</span></span> <span data-ttu-id="876e7-126">Microsoft stellt Standardadressen, die vom System zufällig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="876e7-126">Microsoft provides default addresses that are used by the system randomly.</span></span>  
12. <span data-ttu-id="876e7-127">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="876e7-127">Click Save.</span></span>
13. <span data-ttu-id="876e7-128">Schließen Sie die Seite.</span><span class="sxs-lookup"><span data-stu-id="876e7-128">Close the page.</span></span>
14. <span data-ttu-id="876e7-129">Klicken Sie auf "Speichern".</span><span class="sxs-lookup"><span data-stu-id="876e7-129">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]