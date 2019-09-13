---
title: Überblick über die Finanzberichterstellung
description: In diesem Thema wird beschrieben, wo Sie in Microsoft Dynamics 365 for Finance and Operations auf Finanzberichte zugreifen und wie Sie Finanzberichtfunktionen verwenden. Es umfasst eine Beschreibung der Standardfinanzberichte, die zur Verfügung stehen.
author: aprilolson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3727907c2ff5f51ef3e5132a78836b5e699221b
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865752"
---
# <a name="financial-reporting-overview"></a>Überblick über die Finanzberichterstellung

[!include [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wo Sie in Microsoft Dynamics 365 for Finance and Operations auf Finanzberichte zugreifen und wie Sie Finanzberichtfunktionen verwenden. Es umfasst eine Beschreibung der Standardfinanzberichte, die zur Verfügung stehen.

<a name="accessing-financial-reporting"></a>Finanzberichterstellung nutzen
-----------------------------

Sie können das Menü **Finanzberichterstellung** an den folgenden Stellen in Finance and Operations nutzen:

-   **Hauptbuch** &gt; **Abfragen und Berichte**
-   **Planung** &gt; **Anfragen und Berichte** &gt; **Grundlegende Planung**
-   **Planung** &gt; **Anfragen und Berichte** &gt; **Grundlegende Planung**
-   **Planung** &gt; **Anfragen und Berichte** &gt; **Grundlegende Steuerung**
-   Konsolidierungen

Um Finanzberichte für eine juristische Person zu erstellen und zu generieren, müssen Sie die folgenden Informationen für diese juristische Person einrichten:

-   Steuerkalender
-   Unternehmen
-   Kontenplan
-   Währung

Die Finanzberichtsfunktionen stehen Benutzern zur Verfügung, denen die entsprechenden Rechte und die Aufgaben über ihre Sicherheitsrollen zugewiesen werden. Die folgenden Abschnitten führen diese Rechte und Aufgaben und die zugeordneten Rollen auf.

### <a name="duties"></a>Aufgaben

| Aufgabenbezeichnung                            | Beschreibung                                                             | AOT-Name                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Finanzberichtssicherheit verwalten | Finanzberichtssicherheit verwalten und Verwaltungsaufgaben ausführen. | FinancialReportsSecurityMaintain |
| Finanzberichte verwalten            | Finanzberichte entwerfen und verwalten.                                  | FinancialReportsMaintain         |
| Finanzberichte generieren            | Finanzberichte generieren und aktualisieren.                                 | FinancialReportsGenerate         |
| Die Finanzen des Unternehmens überprüfen          | Die Finanzen des Unternehmens überprüfen und analysieren.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Berechtigungen

| Rechtebezeichnung                       | Beschreibung                                                             | AOT-Name                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Finanzberichtssicherheit verwalten | Finanzberichtssicherheit verwalten und Verwaltungsaufgaben ausführen. | FinancialReportsSecuritySystemMaintain |
| Finanzberichte verwalten            | Finanzberichte entwerfen und verwalten.                                  | FinancialReportsMaintainReports  |
| Finanzberichte generieren            | Finanzberichte generieren und aktualisieren.                                 | FinancialReportsGenerateReports  |
| Finanzberichte anzeigen                | Finanzberichte anzeigen.                                                 | FinancialReportsView             |

### <a name="roles"></a>Rollen

| Rechtebezeichnung                       | Berechtigungen                                  | Rollen                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Finanzberichtssicherheit verwalten | Finanzberichtssicherheit verwalten | Sicherheitsadministrator                                                          |
| Finanzberichte verwalten            | Finanzberichte verwalten            | Buchhaltungsmanager, Buchhaltungsvorgesetzter, Finanzcontroller, Planungsmanager |
| Finanzberichte generieren            | Finanzberichte generieren            | CEO, CFO, Buchhalter                                                            |
| Finanzberichte anzeigen                | Die Finanzen des Unternehmens überprüfen          | Nicht zugewiesen                                                                   |

Nachdem Sie ein Benutzer hinzugefügt haben, oder eine Rolle geändert wurde, sollte der Benutzer in der Lage sein, innerhalb weniger Minuten auf die Finanzberichterstellung zuzugreifen. **Hinweis** Die Rolle sysadmin wird allen Rollen in der Finanzberichterstellung hinzugefügt.

## <a name="default-reports"></a>Standardberichte
Die Finanzberichterstellung enthält 22 standardmäßige Finanzberichte. Jeder Bericht verwendet die standardmäßigen Hauptkontokategorien in Finance and Operations. Sie können diese Berichte verwenden oder sie als Ausgangspunkt für Ihre Finanzberichte nutzen. Zusätzlich zu herkömmlichen Finanzaufstellungen (z. B. Einkommensaufstellung und Bilanz) enthalten diese Standardberichte Berichte, die die unterschiedlichen Arten von Finanzberichten aufzeigen, die Sie erstellen können. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Standardbericht                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 Monatiges Rollen-Einspalteneinkommensaufstellung - Standard | Hier wird die Rentabilität einer Organisation für den letzten 12 Monate in einer Spalte angezeigt.                                                                                                                                                                                                                                      |
| 12 Monatige Einnahmentrendaufstellung - Standard                 | Hier wird die Rentabilität einer Organisation für jeden der letzten 12 Monate angezeigt. Die 12 Monate können mehr als ein Geschäftsjahr umfassen.                                                                                                                                                                                             |
| Projekt vs. Budget – Standard                                | Anzeigen ausführlicher Saldoinformationen für alle Konten für das ursprüngliche Budget und Vergleich des überarbeiteten Budgets mit den tatsächlichen Zahlen mit einer Abweichung.                                                                                                                                                                          |
| Überwachungsdetails – Standard                                  | Detaillierte Ansicht der Saldoinformationen für alle Konten. In diesem Bericht werden Soll- und Guthabensalden in der Berichtswährung und in der lokalen Währung angezeigt, zusammen mit zusätzlichen Buchungsinformationen, wie der Benutzerkennung, dem Benutzer, der zuletzt die Daten bearbeitet hat, dem Datum der letzten Änderung und der Erfassungskennung. |
| Saldenliste – Standard                                   | Detaillierte Ansicht der Saldoinformationen für alle Konten. In diesem Bericht werden Anfangs- und Abschlusssalden sowie Soll- und Guthaben für die aktuelle Periode bis zum aktuellen Jahr zusammen mit zusätzlichen Buchungsinformationen, wie dem Beleg angezeigt.                                                                    |
| Bilanz – Standard                                   | Enthält eine Ansicht der Finanzposition der Organisation für das Jahr.                                                                                                                                                                                                                                                             |
| Konsolidierte Bilanz und Einkommensaufstellung parallel – Standard | Hier werden der finanzielle Stand und die Rentabilität der Organisation für das Jahr nebeneinander angezeigt.                                                                                                                                                                                                                              |
| Cashflow – Standard                                       | Informationen zum Bargeld, das ein- und ausgeht.                                                                                                                                                                                                                                   |
| Detaillierter JE- und TB-Review - Standard                      | Hier werden Anfangssaldo und Aktivitätsinformationen für alle Konten angezeigt.                                                                                                                                                                                                                                                      |
| Ausführliche Zwischenbilanz – Standard                         | Enthält Saldoinformationen für alle Konten und schließt Soll- und Habensalden und deren Nettowert zusammen mit dem Transaktionsdatum, dem Beleg und der Erfassungsbeschreibung ein.                                                                                                                                  |
| Vierteljährlicher Ausgabentrend über drei Jahre – Standard             | Information zu Ausgaben während der letzten 12 Quartale in den vorherigen drei Jahren.                                                                                                                                                                                                                                   |
| Finanztitel JE- und TB-Review – Standard            | Ein Überblicks der Salden und der Aktivität für die Anlage, die Fälligkeit, das Eigenkapitalkonto, Umsatzerlöse, Ausgaben, Gewinn oder Verlust Finanztitel.                                                                                                                                                                           |
| Einkommensaufstellung – Standard                                | Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.                                                                                                                                                                                                                                   |
| Sachkontobuchungsliste – Standard                        | Detaillierte Ansicht der Saldoinformationen für alle Konten. Dieser Bericht zeigt die Soll- und Habensaldos, zusammen mit zusätzlichen Buchungsinformationen, wie Buchungsdatum, der Erfassungsnummer, dem Beleg, dem Buchungstyp und der Tracenummer an.                                                                            |
| Kennzahlen – Standard                                          | Hier werden die Solvenz, die Rentabilität und die Effizienzrate für die Organisation für das Jahr angezeigt.                                                                                                                                                                                                                           |
| Umlaufende Ausgaben über 12 Monate – Standard                       | Informationen zu Ausgaben für die letzten 12 Monate. Die 12 Monate können mehr als ein Geschäftsjahr umfassen.                                                                                                                                                                                                       |
| Umlaufende vierteljährliche Einkommensaufstellung – Standard               | Hier wird die Rentabilität der Organisation vierteljährlich für das letzte Jahr und für das laufende Jahr angezeigt.                                                                                                                                                                                                                   |
| Parallele Bilanz – Standard                      | Enthält eine Ansicht der Finanzposition der Organisation für das Jahr. Dieser Bericht zeigt die Aktiva und die Verbindlichkeiten und das Eigenkapital der Anteilseigner parallel an.                                                                                                                                                                                |
| Zusammengefasste Zwischenbilanz – Standard                          | Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied ein.                                                                                                                                                                  |
| Jährlich zusammengefasste Zwischenbilanz – Standard           | Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied für das aktuelle Jahr und das vergangene Jahr ein.                                                                                                                           |
| Wochenumsatz und Rabatte – Standard                     | Informationen zum in Verkauf und zu Rabatten für jeder Woche in einem Monat. Dieser Bericht umfasst eine Summe für vier Wochen.                                                                                                                                                                                                              |
| Die verfügbaren Budgetmittel - Standard                         | Hier wird ein detaillierter Vergleich des überarbeiteten Budgets, die tatsächliche Aufwendungen, Budgetreservierungen und der Budgetmittel, die für alle Konten verfügbar sind, angezeigt                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Öffnen von Finanzberichten
Wenn Sie auf das Menü **Finanzberichterstellung** klicken, wird die Liste der standardmäßigen Finanzberichte für das Unternehmen angezeigt. Sie können einen Bericht öffnen oder ändern. Um einen der Standardberichte zu öffnen, wählen Sie den Berichtsname aus. Wenn ein Bericht zum ersten Mal geöffnet wird, wird er automatisch für den vorherigen Monat generiert. Wenn Sie beispielsweise einen Bericht zum ersten Mal im August 2016 öffnen, wird der Bericht zum 31. Juli 2016 generiert. Nach dem Öffnen eines Berichts können Sie ihn durchsuchen, indem Sie Detailinformationen bestimmter Daten anzeigen und Berichtsoptionen ändern.

## <a name="creating-and-modifying-financial-reports"></a>Finanzberichte erstellen und ändern
Über die Finanzberichte Liste können Sie einen neuen Bericht erstellen oder einen vorhandenen Bericht ändern. Wenn Sie die erforderlichen Berechtigungen besitzen, können Sie einen neuen Finanzbericht erstellen, indem Sie **Neu** anklicken im Aktivitätsbereich. Ein Berichts-Designer-Programm wird auf Ihr Gerät heruntergeladen. Nachdem der Berichts-Designer startete, können Sie den neuen Bericht erstellen. Nachdem Sie den neuen Bericht gespeichert haben, erscheint er in der Finanzberichtsliste. Die Liste enthält nur Berichte, die für das Unternehmen erstellt wurden, das Sie in Finance and Operations verwenden. 

> [!NOTE] 
> Der Computer, auf dem Sie den Berichts-Designer-Client herunterladen, muss Version 4.6.2 von Microsoft .NET Framework installiert haben. Diese Version von Microsoft .NET Framework kann heruntergeladen und eingerichtet werden vom [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53345). Wenn Sie Chrome verwenden, müssen Sie eine ClickOnce-Erweiterung installieren, um den Berichtsdesigner-Client herunterzuladen. Wenn Sie den privaten Browser verwenden, sollten Sie sicherstellen, dass die ClickOnce-Erweiterung auch für den privaten Modus aktiviert ist. Sie können auch einen Bericht ändern, der in der Finanzberichtsliste erscheint. Wenn der Bereich um den Berichtsnamen aktiviert ist, klicken Sie im Aktivitätsbereich auf **Bearbeiten**. Das Berichtsdesigner-Programm startet.

## <a name="additional-resources"></a>Zusätzliche Ressourcen
- [Finanzberichte anzeigen](view-financial-reports.md)



