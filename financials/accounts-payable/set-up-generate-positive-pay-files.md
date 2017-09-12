---
title: "Einrichten und Generieren von Dateien für positive Zahlungen"
description: In diesem Artikel wird beschrieben, wie positiven Lohndateien eingerichtet und positive Lohndateien generiert werden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8294eb2861f48402c8489b84cc5f139408a22262
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="224a0-103">Einrichten und Generieren von Dateien für positive Zahlungen</span><span class="sxs-lookup"><span data-stu-id="224a0-103">Set up and generate positive pay files</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="224a0-104">In diesem Artikel wird beschrieben, wie positiven Lohndateien eingerichtet und positive Lohndateien generiert werden.</span><span class="sxs-lookup"><span data-stu-id="224a0-104">This article explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="224a0-105">Sie können positiven Lohn verwenden, um eine elektronische Liste mit Schecks zu generieren, die für die Bank bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="224a0-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="224a0-106">Wenn der Scheck der Bank präsentiert wird, vergleicht die Bank den Scheck mit der Liste der Schecks.</span><span class="sxs-lookup"><span data-stu-id="224a0-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="224a0-107">Wenn der Originalscheck mit einem Scheck in der Liste übereinstimmt, löscht die Bank den Scheck.</span><span class="sxs-lookup"><span data-stu-id="224a0-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="224a0-108">Wenn der Scheck mit keinem Scheck iin der Liste übereinstimmt, hält die Bank den Scheck zur Prüfung zurück.</span><span class="sxs-lookup"><span data-stu-id="224a0-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="224a0-109">Sicherheit für Dateien für positive Zahlungen</span><span class="sxs-lookup"><span data-stu-id="224a0-109">Security for positive pay files</span></span>
<span data-ttu-id="224a0-110">Positive Lohndateien können vertrauliche Informationen zu Zahlungsempfänger und Scheckbeträgen enthalten.</span><span class="sxs-lookup"><span data-stu-id="224a0-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="224a0-111">Daher stellen Sie sicher, dass Sie entsprechende Sicherheitspraktiken ab dem Zeitpunkt verwenden, an dem die Dateien generiert werden, bis sie von der Bank empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="224a0-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="224a0-112">Positive Lohndateien werden an den Speicherort heruntergeladen, der von Ihrem Webbrowser angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="224a0-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="224a0-113">Da positive Lohndateien vertrauliche Informationen enthalten können, ist es wichtig, dass nur autorisierte Benutzer diese Informationen in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, generieren und anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="224a0-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="224a0-114">Nutzen Sie die folgende Tabelle, um die Rechte zu bestimmen, die erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="224a0-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="224a0-115">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="224a0-115">Task</span></span></th>
<th><span data-ttu-id="224a0-116">Recht</span><span class="sxs-lookup"><span data-stu-id="224a0-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="224a0-117">Generieren Sie positive Lohndateien über die Listenseite <strong>Bankkonten</strong> oder der Seite <strong>Bankkonten</strong>.</span><span class="sxs-lookup"><span data-stu-id="224a0-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="224a0-118"><strong>Informationen zu positiven Bankzahlungen verwalten</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="224a0-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="224a0-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="224a0-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="224a0-120">Generieren positiver Lohndateien für mehrere juristische Personen und Bankkonten im Formular auf der Seite <strong>Datei für positive Zahlungen generieren</strong>.</span><span class="sxs-lookup"><span data-stu-id="224a0-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="224a0-121"><strong>Informationen zu positiven Bankzahlungen verwalten</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="224a0-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="224a0-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="224a0-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="224a0-123">Positive Lohndateien auf der Seite <strong>Zusammenfassung der Datei für positive Zahlungen</strong>.</span><span class="sxs-lookup"><span data-stu-id="224a0-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="224a0-124"><strong>Bankinformationen zu positiven Zahlungen für mehrere juristische Personen anzeigen</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="224a0-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="224a0-125">Bestätigen Sie eine Datei für positive Bankzahlungen auf der Seite <strong>Zusammenfassung der Datei für positive Zahlungen</strong>.</span><span class="sxs-lookup"><span data-stu-id="224a0-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="224a0-126"><strong>Datei für positive Zahlungen bestätigen</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="224a0-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="224a0-127">Ziehen Sie eine Datei für positive Bankzahlungen auf der Seite <strong>Zusammenfassung der Datei für positive Zahlungen</strong> zurück.</span><span class="sxs-lookup"><span data-stu-id="224a0-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="224a0-128"><strong>Datei für positive Zahlungen zurückrufen</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="224a0-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="224a0-129">Einrichten eines Formats für positive Zahlungen</span><span class="sxs-lookup"><span data-stu-id="224a0-129">Set up a positive pay format</span></span>
<span data-ttu-id="224a0-130">Dateien für positive Zahlungen werden über Datenentitäten erstellt.</span><span class="sxs-lookup"><span data-stu-id="224a0-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="224a0-131">Bevor Sie eine positive Lohndatei generieren können, müssen Sie ein Transformationseingabeformat einrichten, das verwendet wird, um die Schecks in ein Format zu übersetzen, das mit der Bank kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="224a0-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="224a0-132">Auf der **Format für positive Zahlungen**-Seite können Sie eine Dateiformatkennung und eine Beschreibung erstellen.</span><span class="sxs-lookup"><span data-stu-id="224a0-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="224a0-133">Das Umwandlungseingabeformat muss ein XML-Dateiformat sein.</span><span class="sxs-lookup"><span data-stu-id="224a0-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="224a0-134">Das Format hängt von der Transformationsdatei ab, die Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="224a0-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="224a0-135">Die Beispieldatei-XSLT-Datei (Extensible Stylesheet Language Transformations) verwendet beispielsweise das **XML-Element**-Format.</span><span class="sxs-lookup"><span data-stu-id="224a0-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="224a0-136">Verwenden Sie die **Upload-Datei für Umwandlung**-Aktivität, um den Speicherort der Transformdatei für das Format anzugeben, das Ihre Bank erfordert.</span><span class="sxs-lookup"><span data-stu-id="224a0-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="224a0-137">Beispiel: XSLT-Datei für positive Lohndatei</span><span class="sxs-lookup"><span data-stu-id="224a0-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BankPositivePayExportEntity">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="224a0-138">Zuweisen eines eines Formats für positive Zahlungen zu einem Bankkonto</span><span class="sxs-lookup"><span data-stu-id="224a0-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="224a0-139">Jedem Bankkonto, für das Sie positive Erfassung von Lohndaten generieren möchten, müssen Sie das positive Lohnformat zuweisen, das im vorherigen Abschnitt angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="224a0-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="224a0-140">Wählen Sie auf der **Bankkonten**-Seite das positive Lohnformat aus, das dem Bankkonto entspricht.</span><span class="sxs-lookup"><span data-stu-id="224a0-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="224a0-141">Geben Sie im Feld **Startdatum für positive Zahlungen** das erste Datum ein, an dem positive Lohndateien generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="224a0-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="224a0-142">Es ist wichtig, dass Sie in diesem Feld ein Datum eingeben.</span><span class="sxs-lookup"><span data-stu-id="224a0-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="224a0-143">Andernfalls umfasst die erste positive Lohndatei, die generiert wird, alle Prüfungen, die jemals für dieses Bankkonto erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="224a0-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="224a0-144">Zuweisen eines Nummernkreises für positive Lohndateien</span><span class="sxs-lookup"><span data-stu-id="224a0-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="224a0-145">Jede positive Lohndatei muss eine eindeutige Nummer haben.</span><span class="sxs-lookup"><span data-stu-id="224a0-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="224a0-146">Nutzen Sie die Registerkarte **Nummernkreise** auf der **Bargeld- und Bankverwaltungsparameter**-Seite, um einen Nummernkreis für positive Lohndateien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="224a0-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="224a0-147">Generieren Sie eine positive Lohndatei für ein einzelnes Bankkonto</span><span class="sxs-lookup"><span data-stu-id="224a0-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="224a0-148">Sie können eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto generieren.</span><span class="sxs-lookup"><span data-stu-id="224a0-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="224a0-149">Weitere Informationen zur Generierung positiver Lohndateien für mehrere juristische Personen und Bankkonten finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="224a0-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="224a0-150">Um eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto zu generieren, öffnen Sie das Dialogfeld **Datei für positive Zahlungen generieren** über die Seite **Bankkonten**.</span><span class="sxs-lookup"><span data-stu-id="224a0-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="224a0-151">Wählen Sie im Feld **Stichtag** das letzte Scheckdatum, um es in der positiven Lohndatei einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="224a0-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="224a0-152">Alle Schecks, die nicht in einer positiven Lohndatei bis zu diesem Scheckdatum einbezogen wurden, sind in der Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="224a0-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="224a0-153">Generieren Sie eine positive Lohndatei für ein mehrere Bankkonten</span><span class="sxs-lookup"><span data-stu-id="224a0-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="224a0-154">Um eine positive Lohndatei für mehrere juristische Personen und Bankkonten zu generieren, nutzen Sie die periodische Aufgabe **Datei für positive Zahlungen generieren**.</span><span class="sxs-lookup"><span data-stu-id="224a0-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="224a0-155">Wählen Sie das positive Lohnformat für die Datei aus, und legen Sie fest, ob die Datei für alle juristischen Personen oder für eine ausgewählte juristische Person generiert wird.</span><span class="sxs-lookup"><span data-stu-id="224a0-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="224a0-156">Sie können außerdem wählen, ob der positive Lohn für alle Bankkonten generiert wird, die das angegebenen positive Format verwenden, oder nur für ein ausgewähltes Bankkonto.</span><span class="sxs-lookup"><span data-stu-id="224a0-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="224a0-157">Wählen Sie im Feld **Stichtag** das letzte Scheckdatum, um es in der positiven Lohndatei einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="224a0-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="224a0-158">Alle Schecks, die nicht in einer positiven Lohndatei bis zu diesem Scheckdatum einbezogen wurden, sind in der Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="224a0-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="224a0-159">Anzeigen der Ergebnisse der positiven Lohndateierstellung</span><span class="sxs-lookup"><span data-stu-id="224a0-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="224a0-160">Nachdem die positive Lohndatei generiert wurde, können Sie die Ergebnisse auf der Seite **Zusammenfassung der Datei für positive Zahlungen** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="224a0-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="224a0-161">Um die Details der einzelnen Schecks anzuzeigen, nutzen Sie die Detailseite **Positive Lohndatei**.</span><span class="sxs-lookup"><span data-stu-id="224a0-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="224a0-162">Dient zum Bestätigen einer Datei für positive Zahlungen.</span><span class="sxs-lookup"><span data-stu-id="224a0-162">Confirm a positive pay file</span></span>
<span data-ttu-id="224a0-163">Nachdem die Schecks, die in einer positiven Lohndatei aufgeführt sind, bezahlt wurden, erhalten Sie eine Bestätigungsnummer von der Bank.</span><span class="sxs-lookup"><span data-stu-id="224a0-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="224a0-164">Anschließend können Sie die positive Lohndatei bestätigen.</span><span class="sxs-lookup"><span data-stu-id="224a0-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="224a0-165">Wählen Sie auf der **Zusammenfassung der Datei für positive Zahlungen**-Seite eine positive Lohndatei deren Status **Erstellt** ist aus, und wählen Sie dann die Aktivität **Bestätigung eingeben** aus.</span><span class="sxs-lookup"><span data-stu-id="224a0-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="224a0-166">Wenn Sie eine positive Lohndatei bestätigend, wird die Bestätigungsnummer, die Sie von der Bank erhalten haben, erfasst.</span><span class="sxs-lookup"><span data-stu-id="224a0-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="224a0-167">Datei für eine positive Zahlung zurückrufen</span><span class="sxs-lookup"><span data-stu-id="224a0-167">Recall a positive pay file</span></span>
<span data-ttu-id="224a0-168">Wenn Sie eine Datei für positive Zahlungen ändern müssen, können Sie diese erneut aufrufen.</span><span class="sxs-lookup"><span data-stu-id="224a0-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="224a0-169">Wählen Sie auf der **Zusammenfassung der Datei für positive Zahlungen**-Seite eine positive Lohndatei deren Status **Erstellt** ist aus, und wählen Sie dann die Aktivität **Zurückziehen** aus.</span><span class="sxs-lookup"><span data-stu-id="224a0-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="224a0-170">Für jeden Scheck in der positiven Lohndatei zeigt das Feld an, ob der Scheck in einer positiven Lohndatei zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="224a0-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="224a0-171">Sie können dann eine neue positive Lohndatei erstellen, die dem Scheck umfasst, der erneut aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="224a0-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>




