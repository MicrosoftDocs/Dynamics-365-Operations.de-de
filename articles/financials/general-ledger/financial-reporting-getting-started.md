---
title: Finanzberichterstellung
description: "In diesem Thema wird beschrieben, wo Sie in Microsoft Dynamics 365 for Finance and Operations auf Finanzberichte zugreifen und wie Sie Finanzberichtfähigkeiten verwenden. Es umfasst eine Beschreibung der Standardfinanzberichte, die zur Verfügung stehen."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 5de1f5b40af076173dd0b38c6f6110f83c04528a
ms.contentlocale: de-de
ms.lasthandoff: 03/26/2018

---

# <a name="financial-reporting"></a>Finanzberichterstellung

[!INCLUDE [banner](../includes/banner.md)]

In diesem Thema wird beschrieben, wo Sie in Microsoft Dynamics 365 for Finance and Operations auf Finanzberichte zugreifen und wie Sie Finanzberichtfähigkeiten verwenden. Es umfasst eine Beschreibung der Standardfinanzberichte, die zur Verfügung stehen.

<a name="accessing-financial-reporting"></a>Finanzberichterstellung nutzen
-----------------------------

Sie können das Menü **Finanzberichterstellung** an den folgenden Stellen in Finance and Operations nutzen:

-   **Hauptbuch** &gt; **Abfragen und Berichte**
-   **Planung** &gt; **Anfragen und Berichte**  &gt; **Grundlegende Planung**
-   **Planung** &gt; **Anfragen und Berichte**  &gt; **Grundlegende Planung**
-   **Planung** &gt; **Anfragen und Berichte**  &gt; **Grundlegende Steuerung**
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
| Finanzberichtssicherheit verwalten | Finanzberichtssicherheit verwalten und Verwaltungsaufgaben ausführen. | FinancialReportsSecurityMaintain |
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
Die Finanzberichterstellung enthält 22 standardmäßige Finanzberichte. Jeder Bericht verwendet die standardmäßigen Hauptkontokategorien in Finance and Operations. Sie können diese Berichte verwenden oder sie als Ausgangspunkt für Ihre Finanzberichte nutzen. Zusätzlich zu herkömmlichen Finanzaufstellungen (z. B. Einkommensaufstellung und Bilanz) enthalten diese Standardberichte Berichte, die die unterschiedlichen Arten von Finanzberichten aufzeigen, die Sie erstellen können. Jeder Bericht in den folgenden Tabelle ist mit einer Office-Mischungspräsentation über den Bericht verknüpft.

| Standardbericht                                                                                         | Beschreibung                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Monatiges laufende Einkommensaufstellung in einzelnen Spalten - Standard](https://mix.office.com/watch/76kc7bm3wnt1) | Hier wird die Rentabilität einer Organisation für den letzten 12 Monate in einer Spalte angezeigt.                                                                                                                                                                                                                                      |
| [12 Monatige Trend-Einkommensaufstellung - Standard](https://mix.office.com/watch/12brmfge5p8r)                 | Hier wird die Rentabilität einer Organisation für jeden der letzten 12 Monate angezeigt. Die 12 Monate können mehr als ein Geschäftsjahr umfassen.                                                                                                                                                                                             |
| [Projekt vs. Budget – Standard](https://mix.office.com/watch/fi439lkwr0no)                                | Anzeigen ausführlicher Saldoinformationen für alle Konten für das ursprüngliche Budget und Vergleich des überarbeiteten Budgets mit den tatsächlichen Zahlen mit einer Abweichung.                                                                                                                                                                          |
| [Überwachungsdetails – Standard](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Detaillierte Ansicht der Saldoinformationen für alle Konten. In diesem Bericht werden Soll- und Guthabensalden in der Berichtswährung und in der lokalen Währung angezeigt, zusammen mit zusätzlichen Buchungsinformationen, wie der Benutzerkennung, dem Benutzer, der zuletzt die Daten bearbeitet hat, dem Datum der letzten Änderung und der Erfassungskennung. |
| [Saldenliste – Standard](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Detaillierte Ansicht der Saldoinformationen für alle Konten. In diesem Bericht werden Anfangs- und Abschlusssalden sowie Soll- und Guthaben für die aktuelle Periode bis zum aktuellen Jahr zusammen mit zusätzlichen Buchungsinformationen, wie dem Beleg angezeigt.                                                                    |
| [Bilanz – Standard](https://mix.office.com/watch/zkgq0u7visw9)                                   | Enthält eine Ansicht der Finanzposition der Organisation für das Jahr.                                                                                                                                                                                                                                                             |
| [Konsolidierte Bilanz und Einkommensaufstellung parallel – Standard](https://mix.office.com/watch/zkgq0u7visw9) | Hier werden der finanzielle Stand und die Rentabilität der Organisation für das Jahr nebeneinander angezeigt.                                                                                                                                                                                                                              |
| [Cashflow – Standard](https://mix.office.com/watch/jd3go9pz6390)                                       | Informationen zum Bargeld, das ein- und ausgeht.                                                                                                                                                                                                                                   |
| [Detaillierter JE- und TB-Review - Standard](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Hier werden Anfangssaldo und Aktivitätsinformationen für alle Konten angezeigt.                                                                                                                                                                                                                                                      |
| [Ausführliche Zwischenbilanz – Standard](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Enthält Saldoinformationen für alle Konten und schließt Soll- und Habensalden und deren Nettowert zusammen mit dem Transaktionsdatum, dem Beleg und der Erfassungsbeschreibung ein.                                                                                                                                  |
| [Vierteljährlicher Ausgabentrend über drei Jahre – Standard](https://mix.office.com/watch/gwm4zu7tmtj8)             | Information zu Ausgaben während der letzten 12 Quartale in den vorherigen drei Jahren.                                                                                                                                                                                                                                   |
| [Finanztitel JE- und TB-Review – Standard](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Ein Überblicks der Salden und der Aktivität für die Anlage, die Fälligkeit, das Eigenkapitalkonto, Umsatzerlöse, Ausgaben, Gewinn oder Verlust Finanztitel.                                                                                                                                                                           |
| [Einkommensaufstellung – Standard](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Enthält eine Ansicht der Rentabilität der Organisation für die aktuelle Periode und seit Jahresbeginn.                                                                                                                                                                                                                                   |
| [Sachkontobuchungsliste – Standard](https://mix.office.com/watch/19h9v2rmh48vy)                        | Detaillierte Ansicht der Saldoinformationen für alle Konten. Dieser Bericht zeigt die Soll- und Habensaldos, zusammen mit zusätzlichen Buchungsinformationen, wie Buchungsdatum, der Erfassungsnummer, dem Beleg, dem Buchungstyp und der Tracenummer an.                                                                            |
| [Kennzahlen – Standard](https://mix.office.com/watch/b08hfc5h92me)                                          | Hier werden die Solvenz, die Rentabilität und die Effizienzrate für die Organisation für das Jahr angezeigt.                                                                                                                                                                                                                           |
| [Umlaufende Ausgaben über 12 Monate – Standard](https://mix.office.com/watch/iywod5qmqhz7)                       | Informationen zu Ausgaben für die letzten 12 Monate. Die 12 Monate können mehr als ein Geschäftsjahr umfassen.                                                                                                                                                                                                       |
| [Umlaufende vierteljährliche Einkommensaufstellung – Standard](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Hier wird die Rentabilität der Organisation vierteljährlich für das letzte Jahr und für das laufende Jahr angezeigt.                                                                                                                                                                                                                   |
| [Parallele Bilanz – Standard](https://mix.office.com/watch/zkgq0u7visw9)                      | Enthält eine Ansicht der Finanzposition der Organisation für das Jahr. Dieser Bericht zeigt die Aktiva und die Verbindlichkeiten und das Eigenkapital der Anteilseigner parallel an.                                                                                                                                                                                |
| [Zusammengefasste Zwischenbilanz – Standard](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied ein.                                                                                                                                                                  |
| [Jährlich zusammengefasste Zwischenbilanz – Standard](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Enthält Saldoinformationen für alle Konten und schließt Eröffnungs- und Abschlusssalden sowie Soll- und Habensalden, zusammen mit ihrem Nettounterschied für das aktuelle Jahr und das vergangene Jahr ein.                                                                                                                           |
| [Wochenumsatz und Rabatte – Standard](https://mix.office.com/watch/112ng0hy5de0j)                     | Informationen zum in Verkauf und zu Rabatten für jeder Woche in einem Monat. Dieser Bericht umfasst eine Summe für vier Wochen.                                                                                                                                                                                                              |
| [Die verfügbaren Budgetmittel - Standard](https://mix.office.com/watch/15hcpezcbx7tv)                         | Hier wird ein detaillierter Vergleich des überarbeiteten Budgets, die tatsächliche Aufwendungen, Budgetreservierungen und der Budgetmittel, die für alle Konten verfügbar sind, angezeigt                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Öffnen von Finanzberichten
Wenn Sie auf das Menü **Finanzberichterstellung** klicken, wird die Liste der standardmäßigen Finanzberichte für das Unternehmen angezeigt. Sie können einen Bericht öffnen oder ändern. Um einen der Standardberichte zu öffnen, wählen Sie den Berichtsname aus. Wenn ein Bericht zum ersten Mal geöffnet wird, wird er automatisch für den vorherigen Monat generiert. Wenn Sie beispielsweise einen Bericht zum ersten Mal im August 2016 öffnen, wird der Bericht zum 31. Juli 2016 generiert. Nach dem Öffnen eines Berichts können Sie ihn durchsuchen, indem Sie Detailinformationen bestimmter Daten anzeigen und Berichtsoptionen ändern.

## <a name="creating-and-modifying-financial-reports"></a>Finanzberichte erstellen und ändern
Über die Finanzberichte Liste können Sie einen neuen Bericht erstellen oder einen vorhandenen Bericht ändern. Wenn Sie die erforderlichen Berechtigungen besitzen, können Sie einen neuen Finanzbericht erstellen, indem Sie **Neu** anklicken im Aktivitätsbereich. Ein Berichts-Designer-Programm wird auf Ihr Gerät heruntergeladen. Nachdem der Berichts-Designer startete, können Sie den neuen Bericht erstellen. Nachdem Sie den neuen Bericht gespeichert haben, erscheint er in der Finanzberichtsliste. Die Liste enthält nur Berichte, die für das Unternehmen erstellt wurden, das Sie in Finance and Operations verwenden. Weitere Informationen über den Prozess zum Erstellen und Bearbeiten von Finanzberichten in Finance and Operations finden Sie unter [Blogbeiträge](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) im Blog Dynamics Finanzberichterstellung. **Hinweis:** Der Computer, auf den Sie den Berichts-Designer-Client herunterladen, muss Version 4.6.2 vom Microsoft .NET Frameworks installiert haben. Diese Version von Microsoft .NET Frameworks kann heruntergeladen und eingerichtet werden [von](https://www.microsoft.com/en-us/download/details.aspx?id=53345) Wenn Sie Chrome verwenden, müssen Sie eine ClickOnce-Erweiterung installieren, um den Berichtsdesigner-Client herunterzuladen. Wenn Sie den privaten Browser verwenden, sollten Sie sicherstellen, dass die ClickOnce-Erweiterung auch für den privaten Modus aktiviert ist. Sie können auch einen Bericht ändern, der in der Finanzberichtsliste erscheint. Wenn der Bereich um den Berichtsnamen aktiviert ist, klicken Sie im Aktivitätsbereich auf **Bearbeiten**. Das Berichtsdesigner-Programm startet.

<a name="see-also"></a>Siehe auch
--------

[Finanzberichte anzeigen](view-financial-reports.md)

[Dynamics Financial Reporting-Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)




