---
title: Dateien für positive Zahlungen mithilfe der elektronischen Berichterstellung einrichten und generieren
description: In diesem Thema wird beschrieben, wie positive Zahlungen mit der elektronischen Berichterstellung eingerichtet werden.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: bc2f17d62b429b599d5ac5f2a521819275d36b64
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770246"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Dateien für positive Zahlungen mithilfe der elektronischen Berichterstellung einrichten

In diesem Thema wird erklärt, wie Sie mit Hilfe des elektronischen Berichtswesens positive Zahlungen festlegen und positive Zahlungsdateien erstellen können.

> [!NOTE] 
> Bevor Sie die Funktion **Bankpositive Lohndatei generieren** verwenden, müssen Sie zunächst die Liste der Entitäten aktualisieren.
> Gehen Sie zu **Datenverwaltung > Import / Export > Framework-Parameter** 
> **Entitätseinstellungen** Inforegister, wählen Sie **Entitätsliste aktualisieren**.


Sie können positiven Lohn verwenden, um eine elektronische Liste mit Schecks zu generieren, die für die Bank bereitgestellt wird. Wenn ein Scheck bei der Bank vorgelegt wird, vergleicht die Bank ihn mit der Liste der Schecks. Wenn der Originalscheck mit einem Scheck in der Liste übereinstimmt, löscht die Bank den Scheck. Wenn der Scheck mit keinem Scheck iin der Liste übereinstimmt, hält die Bank den Scheck zur Prüfung zurück.

## <a name="security-for-positive-pay-files"></a>Sicherheit für Dateien für positive Zahlungen
Positive Lohndateien können vertrauliche Informationen zu Zahlungsempfänger und Scheckbeträgen enthalten. Daher stellen Sie sicher, dass Sie entsprechende Sicherheitspraktiken ab dem Zeitpunkt verwenden, an dem die Dateien generiert werden, bis sie von der Bank empfangen werden. Positive Lohndateien werden an den Speicherort heruntergeladen, der von Ihrem Webbrowser angegeben wurde. Da positive Lohndateien vertrauliche Informationen enthalten können, ist es wichtig, dass nur autorisierte Benutzer diese Informationen in Microsoft Microsoft Dynamics 365 Finance generieren und anzeigen können. Nutzen Sie die folgende Tabelle, um die Rechte zu bestimmen, die erforderlich sind.

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

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfiguration der elektronischen Berichterstellung einrichten

1. Wechseln Sie zu **Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Auf der Kachel für den Konfigurationsanbieter **Microsoft** wählen Sie **Repositorys** aus.
3. Wählen Sie **Global** und dann **Öffnen** aus.
4. Wenn eine Verbindung zum Repository hergestellt werden muss, wählen Sie den blauen Link im Dialogfeld aus.
5. Suchen Sie in der Konfigurationsliste **Modell für positive Zahlungen \> Format für positive Zahlungen**, und wählen Sie die Optionen aus.
6. Wählen Sie im Inforegister **Versionen** die neueste Version, und wählen Sie dann **Importieren** aus.

## <a name="set-up-a-positive-pay-format"></a>Einrichten eines Formats für positive Zahlungen

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> Formate für positive Zahlungen**.
2. Wählen Sie **Neu** aus.
3. Legen Sie die Felder **Zahlungsformat** und **Beschreibung** fest.
4. Aktivieren Sie das Kontrollkästchen **Allgemeines elektronisches Exportformat**.
5. Legen Sie das Feld **Formatkonfiguration exportieren** auf das **Format für positive Zahlungen** fest.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Zuweisen eines Formats für positive Zahlungen zu einem Bankkonto
Jedem Bankkonto, für das Sie positive Erfassung von Lohndaten generieren möchten, müssen Sie das positive Lohnformat zuweisen, das im vorherigen Abschnitt angegeben wurde. Wählen Sie auf der Bankkonten-Seite das positive Lohnformat aus, das dem Bankkonto entspricht. Geben Sie im Feld **Startdatum für positive Zahlungen** das erste Datum ein, an dem positive Lohndateien generiert werden sollen. 

>[!Important]
> Geben Sie ein Datum in das Feld **Startdatum der Zahlung** ein. Wenn Sie dieses Feld leer lassen, enthält die erste positive Zahlungsdatei, die erstellt wird, alle Schecks, die für dieses Bankkonto erstellt wurden.

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Öffnen Sie das Bankkonto.
3. Legen Sie im Inforegister **Allgemein** das Feld **Format für positive Zahlungen** auf das zuvor erstellte Format fest.
4. Legen Sie das **Startdatum für positive Zahlungen** auf das aktuelle Datum fest.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Zuweisen eines Nummernkreises für positive Lohndateien
Jede positive Lohndatei muss eine eindeutige Nummer haben. Erstellen Sie auf der Seite **Kassen- und Bankverwaltungsparameter** auf der Registerkarte **Nummernkreise** eine Sequenz für positive Lohndateien.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Generieren Sie eine positive Lohndatei für ein einzelnes Bankkonto
Sie können eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto generieren. Weitere Informationen zur Generierung positiver Lohndateien für mehrere juristische Personen und Bankkonten finden Sie im nächsten Abschnitt. Um eine positive Lohndatei für eine einzelne juristische Person und ein einzelnes Bankkonto zu generieren, öffnen Sie das Dialogfeld **Datei für positive Zahlungen generieren** über die Seite **Bankkonten**. Wählen Sie im Feld **Stichtag** das letzte Scheckdatum, um es in der positiven Lohndatei einzubeziehen. Alle Schecks, die nicht in einer positiven Lohndatei bis zu diesem Scheckdatum einbezogen wurden, sind in der Datei enthalten.

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Öffnen Sie ein Bankkonto, für das positive Zahlungen eingerichtet sind.
3. Wählen Sie **Zahlungen verwalten \> Positive Zahlung \> Datei für positive Zahlungen** aus.
4. Legen Sie das Feld **Stichtag** fest. Prüfungen, die vor diesem Datum erstellt wurden, werden berücksichtigt.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Generieren Sie eine positive Lohndatei für ein mehrere Bankkonten
Um eine positive Lohndatei für mehrere Bankkonten zu erstellen, verwenden Sie die periodische Aufgabe **Positive Lohndatei**. Wählen Sie das positive Lohnformat für die Datei aus, und legen Sie fest, ob die Datei für alle juristischen Personen oder für eine ausgewählte juristische Person generiert wird. Sie können außerdem wählen, ob der positive Lohn für alle Bankkonten generiert wird, die das angegebenen positive Format verwenden, oder nur für ein ausgewähltes Bankkonto. Wählen Sie im Feld **Stichtag** das letzte Scheckdatum, um es in der positiven Lohndatei einzubeziehen. Alle Schecks, die nicht in einer positiven Lohndatei bis zu diesem Scheckdatum einbezogen wurden, sind in der Datei enthalten.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Anzeigen der Ergebnisse der positiven Lohndateierstellung
Nachdem die positive Lohndatei generiert wurde, können Sie die Ergebnisse auf der Seite **Zusammenfassung der Datei für positive Zahlungen** anzeigen. Um die Details der einzelnen Schecks anzuzeigen, gehen Sie auf die Seite **Details der Abrechnungsdatei**.

## <a name="confirm-a-positive-pay-file"></a>Dient zum Bestätigen einer Datei für positive Zahlungen.
Nachdem die Schecks, die in einer positiven Lohndatei aufgeführt sind, bezahlt wurden, erhalten Sie eine Bestätigungsnummer von der Bank. Anschließend können Sie die positive Lohndatei bestätigen. Wählen Sie auf der **Zusammenfassung der Datei für positive Zahlungen**-Seite eine positive Lohndatei deren Status **Erstellt** ist aus, und wählen Sie dann die Aktivität **Bestätigung eingeben** aus. Wenn Sie eine positive Lohndatei bestätigend, wird die Bestätigungsnummer, die Sie von der Bank erhalten haben, erfasst.

## <a name="recall-a-positive-pay-file"></a>Datei für eine positive Zahlung zurückrufen
Wenn Sie eine Datei für positive Zahlungen ändern müssen, können Sie diese erneut aufrufen. Wählen Sie auf der **Zusammenfassung der Datei für positive Zahlungen**-Seite eine positive Lohndatei deren Status **Erstellt** ist aus, und wählen Sie dann die Aktivität **Zurückziehen** aus. Für jeden Scheck in der positiven Lohndatei zeigt das Feld an, ob der Scheck in einer positiven Lohndatei zurückgesetzt wurde. Sie können dann eine neue positive Lohndatei erstellen, die dem Scheck umfasst, der erneut aufgerufen wurde.


Die resultierende XML-Datei wird heruntergeladen.
