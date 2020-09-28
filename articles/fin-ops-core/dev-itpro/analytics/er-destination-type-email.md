---
title: E-Mail-ER-Zieltyp
description: Dieses Thema enthält Informationen zum Konfigurieren eines E-Mail-Ziels für jede ORDNER- oder DATEI-Komponente eines ER-Formats (Electronic Reporting), das zum Generieren ausgehender Dokumente konfiguriert ist.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 72f67ad915ba2acc90ecb52bdb97e42504450a03
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745560"
---
# <a name="email-destination"></a><span data-ttu-id="e799d-103">E-Mail-Ziel</span><span class="sxs-lookup"><span data-stu-id="e799d-103">Email destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e799d-104">Sie können ein E-Mail-Ziel für jede ORDNER- oder DATEI-Komponente eines ER-Formats konfigurieren, das zum Generieren ausgehender Dokumente konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="e799d-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="e799d-105">Basierend auf der Zieleinstellung wird ein generiertes Dokument als Anhang einer E-Mail zugestellt.</span><span class="sxs-lookup"><span data-stu-id="e799d-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="e799d-106">Legen Sie **Aktiviert** auf **Ja** fest, um eine Ausgabedatei per E-Mail zu senden.</span><span class="sxs-lookup"><span data-stu-id="e799d-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="e799d-107">Wenn diese Option aktiviert ist, können Sie den E-Mail-Betreff und -Text bearbeiten und die E-Mail-Empfänger angeben.</span><span class="sxs-lookup"><span data-stu-id="e799d-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="e799d-108">Sie können für die E-Mail und den E-Mail-Betreff konstante Texte einrichten, oder Sie können ER-[Formeln](er-formula-language.md) verwenden, um E-Mail-Texte dynamisch zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e799d-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="e799d-109">Sie könnne E-Mail-Adressen für ER auf zwei Arten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e799d-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="e799d-110">Die Konfiguration kann auf dieselbe Weise abgeschlossen werden wie es auch für die Druckverwaltungsfunktion geschieht. Sie können auch eine E-Mail-Adresse auflösen, indem Sie einen direkten Verweis auf die ER-Konfiguration über eine Formel erstellen.</span><span class="sxs-lookup"><span data-stu-id="e799d-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="e799d-111">[![E-Mail-Ziel aktivieren](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="e799d-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="e799d-112">E-Mail-Adressen-Arten</span><span class="sxs-lookup"><span data-stu-id="e799d-112">Email address types</span></span>

<span data-ttu-id="e799d-113">Wenn Sie **Bearbeiten** in den Feldern **An** oder **CC** auswählen, wird das Dialogfeld für **E-Mail an** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e799d-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="e799d-114">Sie können dann den Typ der E-Mail-Adresse auswählen, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="e799d-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="e799d-115">Die E-Mail-Typen **Konfigurations-E-Mail** und **Druckverwaltung** werden derzeit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e799d-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="e799d-116">[![E-Mail-Typ auswählen](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="e799d-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="e799d-117">Druckverwaltung</span><span class="sxs-lookup"><span data-stu-id="e799d-117">Print management</span></span>

<span data-ttu-id="e799d-118">Wenn Sie den E-Mail-Typ **Druckverwaltung** auswählen, können Sie feste E-Mail-Adressen im Feld **An** eingeben.</span><span class="sxs-lookup"><span data-stu-id="e799d-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="e799d-119">[![Feste E-Mail-Adressen konfigurieren](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="e799d-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="e799d-120">Um keine festen E-Mail-Adressen zu verwenden, müssen Sie die E-Mail-Herkunftsart für ein Ziel auswählen.</span><span class="sxs-lookup"><span data-stu-id="e799d-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="e799d-121">Folgende Werte werden unterstützt: **Kunde**, **Lieferant**, **Interessent**, **Kontakt**, **Konkurrent**, **Arbeitskraft**, **Bewerber**, **Künftiger Kreditor** und **Unzulässiger Lieferant**.</span><span class="sxs-lookup"><span data-stu-id="e799d-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="e799d-122">Nachdem Sie einen E-Mail-Quelltyp ausgewählt haben, verwenden Sie die Schaltfläche neben dem Feld **E-Mail-Quellkonto**, um das Formular **Formel-Designer** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e799d-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="e799d-123">Mit diesem Formular können Sie eine Formel anhängen, die zur Laufzeit das **Parteikonto** des ausgewählten Quellentyps vom verarbeiteten Dokument an das E-Mail-Ziel zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e799d-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="e799d-124">[![E-Mail-Quellkonto konfigurieren](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="e799d-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="e799d-125">Formeln sind für die ER-Konfiguration spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="e799d-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="e799d-126">Im Feld **Formel** geben Sie einen dokumentspezifischen Verweis auf einen Debitoren- oder Händlerparteityp ein.</span><span class="sxs-lookup"><span data-stu-id="e799d-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="e799d-127">Anstelle ihn einzugeben, können Sie den Datenquellknoten suchen, der das Debitoren- oder Kreditorenkonto darstellt, und dann auf **Datenquelle hinzufügen** klicken, um die Formel zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="e799d-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="e799d-128">Beispiel: Wenn Sie die Konfiguration **Kreditübertragung (ISO 20022)** verwenden, lautet der Knoten, der ein Debitorenkonto darstellt, `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="e799d-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="e799d-129">Wenn Sie einen Zeichenfolgenwert eingeben, beispielsweise `"DE-001"`, und eine Formel speichern, wird eine E-Mail an die Kontaktperson des Kreditors, **DE-001**, gesendet.</span><span class="sxs-lookup"><span data-stu-id="e799d-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="e799d-130">[![ER-Formel-Designer-Seite](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="e799d-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="e799d-131">[![E-Mail-Quellattributkonto konfigurieren](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="e799d-131">[![Configure email source attributes account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="e799d-132">Konfigurations-E-Mail</span><span class="sxs-lookup"><span data-stu-id="e799d-132">Configuration email</span></span>

<span data-ttu-id="e799d-133">Verwenden Sie diesen E-Mail-Typ, wenn die Konfiguration, die Sie verwenden, einen Knoten in den Datenquellen hat, die eine **E-Mail-Adresse** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e799d-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="e799d-134">Sie können Datenquellen und Funktionen im Formeldesigner verwenden, um eine ordnungsgemäße formatierte E-Mail-Adresse abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e799d-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="e799d-135">Beispiel: Wenn Sie die Konfiguration **Kreditübertragung (ISO 20022)** verwenden, lautet der Knoten, der eine E-Mail-Adresse der Kontaktperson des Kreditors darstellt, `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="e799d-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="e799d-136">[![Quelle der E-Mail-Adresse konfigurieren](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="e799d-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e799d-137">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e799d-137">Additional resources</span></span>

- [<span data-ttu-id="e799d-138">Überblick über die elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="e799d-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e799d-139">Zielorte für elektronische Berichterstellung (ER)</span><span class="sxs-lookup"><span data-stu-id="e799d-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="e799d-140">Formeldesigner in der elektronischen Berichterstellung (EB)</span><span class="sxs-lookup"><span data-stu-id="e799d-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
