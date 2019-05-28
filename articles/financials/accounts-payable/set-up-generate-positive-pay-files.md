---
title: Einrichten und Generieren von Dateien für positive Zahlungen
description: In diesem Thema wird beschrieben, wie positive Lohnzahlungen eingerichtet und positive Lohndateien generiert werden.
author: abruer
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a5579eae5117a7a3ca517bbcc235c2ed2d925d7f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512360"
---
# <a name="set-up-and-generate-positive-pay-files"></a>Einrichten und Generieren von Dateien für positive Zahlungen

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wie positive Lohnzahlungen eingerichtet und positive Lohndateien generiert werden. 

Sie können positiven Lohn verwenden, um eine elektronische Liste mit Schecks zu generieren, die für die Bank bereitgestellt wird. Wenn der Scheck der Bank präsentiert wird, vergleicht die Bank den Scheck mit der Liste der Schecks. Wenn der Originalscheck mit einem Scheck in der Liste übereinstimmt, löscht die Bank den Scheck. Wenn der Scheck mit keinem Scheck iin der Liste übereinstimmt, hält die Bank den Scheck zur Prüfung zurück.

## <a name="security-for-positive-pay-files"></a>Sicherheit für Dateien für positive Zahlungen
Positive Lohndateien können vertrauliche Informationen zu Zahlungsempfänger und Scheckbeträgen enthalten. Daher stellen Sie sicher, dass Sie entsprechende Sicherheitspraktiken ab dem Zeitpunkt verwenden, an dem die Dateien generiert werden, bis sie von der Bank empfangen werden. Positive Lohndateien werden an den Speicherort heruntergeladen, der von Ihrem Webbrowser angegeben wurde. Da positive Lohndateien vertrauliche Informationen enthalten können, ist es wichtig, dass nur autorisierte Benutzer diese Informationen in Microsoft Dynamics 365 for Finance and Operations generieren und anzeigen können. Nutzen Sie die folgende Tabelle, um die Rechte zu bestimmen, die erforderlich sind.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Aufgabe</th>
<th>Recht</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Generieren Sie positive Lohndateien über die Listenseite <strong>Bankkonten</strong> oder der Seite <strong>Bankkonten</strong>.</td>
<td><ul>
<li><strong>Informationen zu positiven Bankzahlungen verwalten</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Generieren positiver Lohndateien für mehrere juristische Personen und Bankkonten im Formular auf der Seite <strong>Datei für positive Zahlungen generieren</strong>.</td>
<td><ul>
<li><strong>Informationen zu positiven Bankzahlungen verwalten</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Positive Lohndateien auf der Seite <strong>Zusammenfassung der Datei für positive Zahlungen</strong>.</td>
<td><strong>Bankinformationen zu positiven Zahlungen für mehrere juristische Personen anzeigen</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Bestätigen Sie eine Datei für positive Bankzahlungen auf der Seite <strong>Zusammenfassung der Datei für positive Zahlungen</strong>.</td>
<td><strong>Datei für positive Zahlungen bestätigen</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Ziehen Sie eine Datei für positive Bankzahlungen auf der Seite <strong>Zusammenfassung der Datei für positive Zahlungen</strong> zurück.</td>
<td><strong>Datei für positive Zahlungen zurückrufen</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Einrichten eines Formats für positive Zahlungen
Dateien für positive Zahlungen werden über Datenentitäten erstellt. Bevor Sie eine positive Lohndatei generieren können, müssen Sie ein Transformationseingabeformat einrichten, das verwendet wird, um die Schecks in ein Format zu übersetzen, das mit der Bank kommunizieren kann. Auf der **Format für positive Zahlungen**-Seite können Sie eine Dateiformatkennung und eine Beschreibung erstellen. Das Umwandlungseingabeformat muss ein XML-Dateiformat sein. Das Format hängt von der Transformationsdatei ab, die Sie verwenden. Die Beispieldatei-XSLT-Datei (Extensible Stylesheet Language Transformations) verwendet beispielsweise das **XML-Element**-Format. Verwenden Sie die **Upload-Datei für Umwandlung**-Aktivität, um den Speicherort der Transformdatei für das Format anzugeben, das Ihre Bank erfordert.

## <a name="example-xslt-file-for-positive-pay-file"></a>Beispiel: XSLT-Datei für positive Lohndatei
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
          <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Zuweisen eines eines Formats für positive Zahlungen zu einem Bankkonto
Jedem Bankkonto, für das Sie positive Erfassung von Lohndaten generieren möchten, müssen Sie das positive Lohnformat zuweisen, das im vorherigen Abschnitt angegeben wurde. Wählen Sie auf der **Bankkonten**-Seite das positive Lohnformat aus, das dem Bankkonto entspricht. Geben Sie im Feld **Startdatum für positive Zahlungen** das erste Datum ein, an dem positive Lohndateien generiert werden sollen. Es ist wichtig, dass Sie in diesem Feld ein Datum eingeben. Andernfalls umfasst die erste positive Lohndatei, die generiert wird, alle Prüfungen, die jemals für dieses Bankkonto erstellt wurden.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Zuweisen eines Nummernkreises für positive Lohndateien
Jede positive Lohndatei muss eine eindeutige Nummer haben. Nutzen Sie die Registerkarte **Nummernkreise** auf der **Bargeld- und Bankverwaltungsparameter**-Seite, um einen Nummernkreis für positive Lohndateien zu erstellen.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generieren Sie eine positive Lohndatei für ein einzelnes Bankkonto
Sie können eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto generieren. Weitere Informationen zur Generierung positiver Lohndateien für mehrere juristische Personen und Bankkonten finden Sie im nächsten Abschnitt. Um eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto zu generieren, öffnen Sie das Dialogfeld **Datei für positive Zahlungen generieren** über die Seite **Bankkonten**. Wählen Sie im Feld **Stichtag** das letzte Scheckdatum, um es in der positiven Lohndatei einzubeziehen. Alle Schecks, die nicht in einer positiven Lohndatei bis zu diesem Scheckdatum einbezogen wurden, sind in der Datei enthalten.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generieren Sie eine positive Lohndatei für ein mehrere Bankkonten
Um eine positive Lohndatei für mehrere juristische Personen und Bankkonten zu generieren, nutzen Sie die periodische Aufgabe **Datei für positive Zahlungen generieren**. Wählen Sie das positive Lohnformat für die Datei aus, und legen Sie fest, ob die Datei für alle juristischen Personen oder für eine ausgewählte juristische Person generiert wird. Sie können außerdem wählen, ob der positive Lohn für alle Bankkonten generiert wird, die das angegebenen positive Format verwenden, oder nur für ein ausgewähltes Bankkonto. Wählen Sie im Feld **Stichtag** das letzte Scheckdatum, um es in der positiven Lohndatei einzubeziehen. Alle Schecks, die nicht in einer positiven Lohndatei bis zu diesem Scheckdatum einbezogen wurden, sind in der Datei enthalten.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Anzeigen der Ergebnisse der positiven Lohndateierstellung
Nachdem die positive Lohndatei generiert wurde, können Sie die Ergebnisse auf der Seite **Zusammenfassung der Datei für positive Zahlungen** anzeigen. Um die Details der einzelnen Schecks anzuzeigen, nutzen Sie die Detailseite **Positive Lohndatei**.

## <a name="confirm-a-positive-pay-file"></a>Dient zum Bestätigen einer Datei für positive Zahlungen.
Nachdem die Schecks, die in einer positiven Lohndatei aufgeführt sind, bezahlt wurden, erhalten Sie eine Bestätigungsnummer von der Bank. Anschließend können Sie die positive Lohndatei bestätigen. Wählen Sie auf der **Zusammenfassung der Datei für positive Zahlungen**-Seite eine positive Lohndatei deren Status **Erstellt** ist aus, und wählen Sie dann die Aktivität **Bestätigung eingeben** aus. Wenn Sie eine positive Lohndatei bestätigend, wird die Bestätigungsnummer, die Sie von der Bank erhalten haben, erfasst.

## <a name="recall-a-positive-pay-file"></a>Datei für eine positive Zahlung zurückrufen
Wenn Sie eine Datei für positive Zahlungen ändern müssen, können Sie diese erneut aufrufen. Wählen Sie auf der **Zusammenfassung der Datei für positive Zahlungen**-Seite eine positive Lohndatei deren Status **Erstellt** ist aus, und wählen Sie dann die Aktivität **Zurückziehen** aus. Für jeden Scheck in der positiven Lohndatei zeigt das Feld an, ob der Scheck in einer positiven Lohndatei zurückgesetzt wurde. Sie können dann eine neue positive Lohndatei erstellen, die dem Scheck umfasst, der erneut aufgerufen wurde.



