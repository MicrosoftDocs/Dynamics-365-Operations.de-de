---
title: Neuerungen und Änderungen in Dynamics 365 Human Resources 12. Juli 2021
description: Dieses Thema beschreibt Funktionen, die in Microsoft Dynamics 365 Human Resources für den 12. Juli 2021 neu sind oder geändert wurden.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c01d00e7ede44c20e64fc4a8cd8646201caa3992
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686798"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Neuerungen und Änderungen in Dynamics 365 Human Resources 12. Juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In diesem Thema werden die Funktionen beschrieben, die in Dynamics 365 Human Resources neu oder geändert wurden oder demnächst verfügbar sind.

Weitere Informationen zu unserem Aktualisierungsprozess und Zeitplan finden Sie unter [Aktualisierungsprozess](hr-admin-setup-update-process.md).

Weitere Informationen zu neuen Funktionen und den voraussichtlichen allgemeinen Verfügbarkeitsterminen finden Sie unter [Überblick Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>In dieser Version

Diese Version enthält die folgenden neuen Funktionen und Fehlerbehebungen. Änderungen gelten für Build-Nummer 8.1.4353.

### <a name="new-features"></a>Neue Features

Die folgenden Funktionen sind in dieser Version allgemein verfügbar.

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
|  Umschalten der Anzeige von Betriebsjahren | |Diese Funktion bietet die Möglichkeit, unterschiedliche Daten zur Berechnung der Dienstjahre zu verwenden, die auf der Seite **Bereinigte Mitarbeiterentität** und im Formular **Personen** angezeigt werden.  Dies wird in den [Human Resources-Parametern](/dynamics365/human-resources/hr-setup-parameters) verfügbar sein. |


### <a name="bug-fixes"></a>Fehlerkorrekturen

Die folgenden Fehlerkorrekturen sind in diesem Release enthalten.

> [!NOTE]
> Unser Ziel ist es, Ihnen diese Informationen so schnell wie möglich zukommen zu lassen. Wir können dieses Thema aktualisieren, um Fehlerbehebungen aufzunehmen, die es nach der Erstveröffentlichung dieses Themas in den Build geschafft haben.

| Problemnummer | Problem |  Beschreibung |
| --- | --- | --- |
| 595871 | Der Infobereich in der Personalabteilung hat eine falsche Dataverse Terminologie | Mit der Umbenennung von Common Data Service zu Dataverse wurde die Terminologie im Microsoft Dynamics 365 Human Resources Informationsbereich aktualisiert (**Hilfe & Support > Über**). |
| 598676 | Ein optimiertes Mitarbeitereingabeformular überschreibt die Aufgabe und kann bei Verwendung mit der gespeicherten Ansicht zu einem Fehler führen| Auf der **Arbeitskraft** Seite, wenn die Funktion optimierte Mitarbeitereingabe aktiviert ist, kann die Anwendung fehlschlagen, wenn **Immer zum Bearbeiten geöffnet** in der gespeicherten Ansicht eingestellt ist. |
| 592344 |Der Abschnitt Arbeitskraftkompensation zur Position sollte nur gelesen werden, wenn die Leistungsverwaltung aktiviert ist | Die Vergütungs-Information für Mitarbeiter wird mit der alten Leistungsfunktionalität erstellt.  Wenn die Leistungsverwaltung aktiviert ist, sind die Felder schreibgeschützt. Wenn die Leistungsverwaltung aktiviert ist und **Veraltete Leistungsformulare ausblenden** auf **Ja** in den gemeinsamen HR-Parametern eingestellt ist, wird die Registerkarte **Arbeitskraftvergütung** ausgeblendet. |
| 598617 | **HcmDiskussion** Formularaktivierungsregisterkarte verursacht eine Endlosschleife, wenn Personalisierungen angewendet werden | Wenn sowohl die Raster als auch die Detailansicht **Immer zum Bearbeiten geöffnet** aktiviert ist, kollidiert der Code, der die Registerkarte in der überschriebenen Aufgabenmethode aktiviert, mit der Personalisierung, welches Steuerelement den Fokus haben soll, und erstellt eine Endlosschleife. |
| 593553 | Das Feld Erfassungsdatum in der Leistungserfassung wird in UTC angezeigt | Das Feld **Erfassungsdatum** für Leistungserfassungen wird in der UTC-Zeitzone und nicht in der in der Systemdatumseinrichtung definierten Zeitzone angezeigt, was dazu führt, dass das Datum für einige Zeitzonen falsch ist. |
| 586930 | Das Öffnen von Aktivitäten für Leistungsziele öffnet einen ganz anderen Datensatz | Wenn die Funktion Erweiterte Berichtsansicht für Leistungserfassungen in der Funktionsverwaltung aktiviert ist, können Sie die Leistungsziele für erweiterte Berichte auf der Registerkarte **Mein Team** auswählen und in **Mitarbeiter Selbstservice** werden die Ziele für einen Mitarbeiter anstelle des ausgewählten Mitarbeiters geöffnet. |
| 569959 |  Die Hcm-Position ArbeiteitskraftzuweisungV2-Entität weist einer Position keine Arbeitskraft zu | Benutzer haben einen Fehler erhalten, wenn sie einen Stellenzuweisungsdatensatz über die Entität hinzufügen und die Veröffentlichung fehlgeschlagen ist. |
| 582259 | Der VETS 4212-Bericht verwendet das Formular 2017 anstelle des Formulars 2020 | Auf das Format 2020 aktualisiert.  Um das neue Format zu laden, gehen Sie zu **Berichtskonfigurationen** und löschen Sie den VETS-4212-Bericht in der linken Spalte. Gehen Sie zu **Elektronische Berichterstattung – Repositorys – HR-Ressourcen** und wählen Sie **Offen**.  Wählen Sie **VETS-4212 PDF-Ausdruck** und dann **Importieren**.|


## <a name="in-preview"></a>Vorschau

Die folgenden neuen Funktionen stehen in der Vorschau zur Verfügung. Weitere Informationen zur Aktivierung oder Deaktivierung von Vorschaufunktionen finden Sie unter [Funktionen verwalten](hr-admin-manage-features.md).

| Funktion | Freigabeplan | Dokumentation |
| --- | --- | --- |
| Arbeitsbereich für Vorteilsverwaltung | [Arbeitsbereich für die Verwaltung von Zusatzleistungen (Vorschau)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeitsbereich „Vorteilsverwaltung“](hr-benefits-management-workspace.md) |
| Ermöglicht eine vereinfachte Integration der Gehaltsabrechnung (APIs zur Integration der Gehaltsabrechnung) | [Ermöglichen Sie eine vereinfachte Integration mit Gehaltsabrechnungsanbietern](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lohnintegrations-API](hr-admin-integration-payroll-api-introduction.md)|
|  Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten | [Aktivieren Sie einen Abwesenheitsmanager, um den Urlaub zu verwalten](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Rolle des Abwesenheitsmanagers konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Anhangsanforderung pro Urlaubsart konfigurieren | [Anhangsanforderung pro Urlaubsart konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Urlaubseinheiten pro Urlaubstyp konfigurieren | [Urlaubseinheiten pro Urlaubstyp konfigurieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Urlaubs- und Abwesenheitstypen konfigurieren](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Aktivieren, dass Mitarbeiter als zahlungsbereit markiert werden | [Mitarbeiter als zahlungsbereit markieren](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Für Zahlung bereit](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Demnächst

| Funktion | Informationen |
| --- | --- |
| Plattformupdate 10.0.20 (44) | Das Plattform-Update 10.0.20 wird voraussichtlich mit dem Service-Release am 26. Juli 2021 ausgerollt. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.20 der Apps für Finanzen und Betrieb (August 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Eine vollständige Liste der geplanten Funktionen und ihrer geplanten Versionen finden Sie unter [Überblick über Dynamics 365 Human Resources 2021 Veröffentlichungszyklus 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Siehe auch

[Neuerungen oder Änderungen in Human Resources](hr-admin-whats-new.md)</br>
[Übersicht zu Dynamics 365 Human Resources 2021 Versionswelle 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualisierungsprozess](hr-admin-setup-update-process.md)</br>
[Funktionen verwalten](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
