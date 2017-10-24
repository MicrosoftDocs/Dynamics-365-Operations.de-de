---
title: "Zahlungsbelegbericht für Europa"
description: "Dieses Thema enthält Informationen zu Zahlungsbelegberichten für Europa."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f82ab348415be3932014a223371412c7ce32cc90
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="payment-slip-report-for-europe"></a><span data-ttu-id="9daa5-103">Zahlungsbelegbericht für Europa</span><span class="sxs-lookup"><span data-stu-id="9daa5-103">Payment slip report for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9daa5-104">Dieses Thema enthält Informationen zu Zahlungsbelegberichten für Europa.</span><span class="sxs-lookup"><span data-stu-id="9daa5-104">This topic provides information about payment slip reports for Europe.</span></span>

<span data-ttu-id="9daa5-105">Die Funktionen für Zahlungsbelegberichte sind für die juristische Personen verfügbar, deren primäre Adresse sich in Dänemark, in Belgien, Norwegen, in der Schweiz oder in Finnland befindet.</span><span class="sxs-lookup"><span data-stu-id="9daa5-105">The functionality for payment slip reports is available for legal entities that have their primary address in Denmark, Belgium, Norway, Switzerland, or Finland.</span></span> <span data-ttu-id="9daa5-106">Unternehmen fügen oft Rechnungen in der Regel gedruckte Zahlungsbelege bei, um Debitoren zu unterstützen und einen Zahlungsnachweis für Buchungen und den Ausgleich von Konten zur Verfügung zu haben.</span><span class="sxs-lookup"><span data-stu-id="9daa5-106">Businesses often attach printed payment slips to invoices to provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="9daa5-107">Der Zahlungsbeleg kann neben Verkaufsrechnungen und Freitextrechnungen auch für Projekt- oder Servicerechnungen, Mahnschreiben, Zinsrechnungen und Kontoauszüge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9daa5-107">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span>

## <a name="set-up-a-creditor-id-number-denmark-only"></a><span data-ttu-id="9daa5-108">Einrichten einer Kreditorenkennung (Nur Dänemark)</span><span class="sxs-lookup"><span data-stu-id="9daa5-108">Set up a creditor ID number (Denmark only)</span></span>
<span data-ttu-id="9daa5-109">Gehen Sie folgendermaßen vor, um Gläubigerkennung (ID)- Nummer des Unternehmens eingeben.</span><span class="sxs-lookup"><span data-stu-id="9daa5-109">Follow these steps to enter your company's creditor identification (ID) number.</span></span> <span data-ttu-id="9daa5-110">Ihr Finanzinstitut stellt diese Nummer bereit.</span><span class="sxs-lookup"><span data-stu-id="9daa5-110">Your financial institution provides this number.</span></span> <span data-ttu-id="9daa5-111">Diese Nummer wird als Referenz verwendet, wenn Debitorenzahlungen über Finanzinstitutionen empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="9daa5-111">It's used as a reference when customer payments are received through financial institutions.</span></span>

1.  <span data-ttu-id="9daa5-112">Klicken Sie auf **Organisationsverwaltung** &gt; **Einrichten**&gt; **Organisationen** &gt; **Juristische Personen**.</span><span class="sxs-lookup"><span data-stu-id="9daa5-112">Click **Organization administration** &gt; **Setup** &gt; **Organization** &gt; **Legal entities**.</span></span>
2.  <span data-ttu-id="9daa5-113">Im Inforegister **Bankkontoinformationen** Wählen Sie das Feld **FI-Gläubiger-Kennung** und geben Sie die eindeutige achtstellige Kreditorenkennung ein.</span><span class="sxs-lookup"><span data-stu-id="9daa5-113">On the **Bank account information** FastTab, in the **FI-Creditor ID** field, enter your unique eight-digit creditor ID number.</span></span>
3.  <span data-ttu-id="9daa5-114">Schließen Sie das Formular, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9daa5-114">Close the form to save your changes.</span></span>

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a><span data-ttu-id="9daa5-115">Einrichten eines Zahlungsbelegformats für Rechnungen, Zinsrechnungen, Inkassoschreiben und Kontoauszüge</span><span class="sxs-lookup"><span data-stu-id="9daa5-115">Set up a payment slip attachment format for invoices, interest notes, collection letters, and account statements</span></span>
<span data-ttu-id="9daa5-116">Folgen Sie diesen Schritten und richten Sie ein Format für einen Zahlungsbeleg ein, der Verkaufsrechnungen, Freitextrechnungen, Zinsrechnungen, Mahnschreiben und Kontoauszügen beigelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9daa5-116">Follow these steps to set up a format for payment slip attachments that accompany sales invoices, free text invoices, interest notes, collection letters, and account statements.</span></span>

1.  <span data-ttu-id="9daa5-117">Klicken Sie auf **Debitoren** &gt; **Einstellungen** &gt; **Formulare** &gt; **Formularnotizen**.</span><span class="sxs-lookup"><span data-stu-id="9daa5-117">Click **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="9daa5-118">In der Registerkarte **Rechnung** wählen Sie das Feld **Zugeordnetr Zahlungsanhang für  Debitorenrechnung** und wählen Sie das Zahlungsbelegformat aus.</span><span class="sxs-lookup"><span data-stu-id="9daa5-118">On the **Invoice** tab, in the **Associated payment attachment on customer invoice** field, select the payment slip attachment format.</span></span>
3.  <span data-ttu-id="9daa5-119">In den Registerkarten **Freitextrechnung,**, **Zinsrechnung**, **Mahnschreiben** und **Bankauszug** wählen Sie ein Format für einen Zahlungsbeleg, der für den Dokumenttyp verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9daa5-119">On the **Free text invoice**, **Interest note**, **Collection letter**, and **Account statement** tabs, select a payment slip attachment format for each document type.</span></span>
4.  <span data-ttu-id="9daa5-120">Schließen Sie das Formular, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9daa5-120">Close the form to save your changes.</span></span>

<span data-ttu-id="9daa5-121">Folgen Sie diesen Schritten und richten Sie ein Format für einen Zahlungsbeleg ein, der Projektrechnungen beigelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9daa5-121">Follow these steps to set up a format for payment slip attachments that accompany project invoices.</span></span>

1.  <span data-ttu-id="9daa5-122">Klicken Sie auf **Projektverwaltung und -buchhaltung**&gt; **Einrichten** &gt; **Formular** &gt; **Formulareinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="9daa5-122">Click **Project management and accounting** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="9daa5-123">Klicken Sie auf die Registerkarte **Zugeordnete Zahlungsbeilagen** und wählen Sie im Feld das Format für den Zahlungsbeleg aus.</span><span class="sxs-lookup"><span data-stu-id="9daa5-123">In the **Associated payment attachment** field, select the payment slip attachment format.</span></span>

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a><span data-ttu-id="9daa5-124">Zuweisen einer Zahlungsbelegsbeilage zu einem Debitorenkonto</span><span class="sxs-lookup"><span data-stu-id="9daa5-124">Assign a payment slip attachment format to a customer account</span></span>
<span data-ttu-id="9daa5-125">Nach dem Einrichten des Zahlungsbelegformats für Verkaufsrechnungen, Freitextrechnungen, Zinsrechnungen, Mahnschreiben, Projektrechnungen, Kontoauszüge und Projektrechnungen können einem ausgewählten Debitor bestimmte Formate zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9daa5-125">After you set up the payment slip attachment format for sales invoices, free text invoices, interest notes, collection letters, account statements, and project invoices, you can assign specific formats for a selected customer.</span></span>

1.  <span data-ttu-id="9daa5-126">Klicken Sie auf **Debitoren** &gt; **Allgemein** &gt; **Kunden** &gt; **Alle Kunden**.</span><span class="sxs-lookup"><span data-stu-id="9daa5-126">Click **Accounts receivable** &gt; **Common** &gt; **Customers** &gt; **All customers**.</span></span>
2.  <span data-ttu-id="9daa5-127">Dient zum Erstellen eines neuen Debitors oder zum Auswählen eines vorhandenen Debitors.</span><span class="sxs-lookup"><span data-stu-id="9daa5-127">Create a new customer, or select an existing customer.</span></span>
3.  <span data-ttu-id="9daa5-128">Im Inforegister in den Feldern **Rechnung und Lieferung** unter **Auf einer Debitorenrechnung**, **Auf einer Freitextrechnung**, **Für eine Zinsrechnung**, **Auf einem Mahnschreiben**, **Auf einer Projektrechnung** und **Auf einem Kontoauszug** wählen Sie das Format für Zahlungsbelegsanhänge aus, die Dokumente jeden Typs begleiten, die an den ausgewählten Debitor gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9daa5-128">On the **Invoice and delivery** FastTab, in the **On a customer invoice**, **On a free text invoice**, **On an interest note**, **On a collection letter**, **On a project invoice**, and **On an account statement** fields, select the format for payment slip attachments that will accompany documents of each type that are sent to the selected customer.</span></span>
4.  <span data-ttu-id="9daa5-129">Schließen Sie das Formular, um Ihre Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9daa5-129">Close the form to save your changes.</span></span>





