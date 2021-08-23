---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Finance
description: In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Finance.
author: roschlom
ms.date: 04/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7ce7353de5795fd82e53bb1b7919c95dae4fe0ab6b8f536361613a7bcae19101
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781200"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

In diesem Thema werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Finance.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

> [!NOTE]
> Detaillierte Informationen über Objekte in Finance and Operations Apps finden Sie in den [Technischen Referenzberichten](/dynamics/s-e/global/axtechrefrep_61). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die sich in jeder Version von Finance and Operations-Anwendungen geändert haben oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.20

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>Konfiguration des Formats der elektronischen Berichterstellung (ER) „RTIR-Abfrage von Rechnungsdatenanforderungen (HU)“

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ausgenommen von der Verarbeitung elektronischer Nachrichten für die Zusammenarbeit mit dem ungarischen Online-Abrechnungssystem |
| **Ersetzt durch eine andere Funktion?**   | Nr. |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 15. April 2022 planen wir, die Konfiguration des Formats „RTIR-Abfrage von Rechnungsdatenanforderungen (HU)“ nicht mehr zu unterstützen. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>Format der elektronischen Berichterstellung (ER) „Französische FEC-Protokolldatei“ für Frankreich im Format „Deutsche Ausgabeprotokolldatei“

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch neues Format „FEC-Protokolldatei (FR)“ |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 1. Mai 2022 planen wir, das Format zur elektronischen Berichtserstellung „Französische FEC-Protokolldatei“ für Frankreich im Format „Deutsche Ausgabeprotokolldatei“ nicht mehr zu unterstützen. Das neue Format der FEC-Auditdatei (FR) wird stattdessen unter dem „Datenexportmodell“ eingeführt. |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.17

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-Repository als Speicheroption für Konfigurationen zur elektronischen Berichterstellung

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch das neue globale Repository des Regulatory Configuration Service (RCS) |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Dynamics 365 Finance-, Supply Chain Management- und Project Operations-Produkte|
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Wir planen, das Microsoft Dynamics Lifecycle Services (LCS)-Repository ab dem 01. April 2022 nicht länger als Speicheroption für EB-Konfigurationen (elektronische Berichterstellung) zu unterstützen. Neue Microsoft-EB-Konfigurationen werden exklusiv im globalen Repository zum Download veröffentlicht. Auf das globale Repository kann über die Dynamics 365-Produkte und RCS zugegriffen werden. Weitere Informationen finden Sie unter [Importieren von ER-Konfigurationen aus RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) und [Regulatory Configuration Service – Lifecycle Services (LCS)-Speichereinstellung](../localizations/rcs-lcs-repo-dep-faq.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.16

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Elektronische Berichtsformate „Mehrwertsteuererklärung (CZ)“ und „Steueranweisungsexport (CZ)“ für die Tschechische Republik

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Durch neue Formate ersetzt |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 22. Januar 2022 planen wir, die Formate „Umsatzsteuererklärung (CZ)“ und „Steueranweisungsexport (CZ)“ für elektronische Berichterstattung (ER) nicht mehr zu unterstützen. Stattdessen werden im Model „Steuererklärung“ die neuen Formate „Umsatzsteuererklärung XML (CZ)“ Umsatzsteuererklärung XML Excel (CZ) und Umsatzsteueranweisung XML (CZ) eingeführt. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>Das elektronisches Berichtsformat „Ledger Transaction Export Format (BE)“ und das entsprechende „Ledger Transaction Export (BE)“-Modell für Belgien

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch das neue ER-Format unter dem Modell „Standard Audit File (SAF-T)“.  |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 1. Dezember 2021 planen wir, das elektronische Berichtsformat „Ledger Transaction Export Format (BE)“ und das entsprechende Modell „Ledger Transaction Export (BE)“ nicht mehr zu unterstützen. Stattdessen wird im Modell „Standard Audit File (SAF-T)“ ein neues Format „General Ledger Data Export (BE)“ zusammen mit „General Ledger Data Model Mapping“ eingeführt. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>„VAT 100“-Bericht für Großbritannien im SSRS-Format

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch neues ER-Format – „VAT Declaration Excel (UK)“-Format im „Tax Declaration Model“.  |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 1. Dezember 2021 planen wir, den „VAT 100-Bericht“ im SSRS-Format nicht mehr zu unterstützen. Ein neues „VAT Declaration Excel (UK)“-Format im „Tax Declaration Model“ wurde in der EU in der [MTD-Mehrwertsteuerfunktion](../localizations/emea-gbr-mtd-vat-integration.md) eingeführt. |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11-Unterstützung für Dynamics 365 ist veraltet

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ab Dezember 2020 wird die Unterstützung von Microsoft Internet Explorer 11 für alle Dynamics 365-Produkte veraltet sein und Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt werden.<br><br>Dies wirkt sich auf Kunden aus, die Dynamics 365-Produkte verwenden, die für die Verwendung über eine Internet Explorer 11-Schnittstelle entworfen wurden. Nach August 2021 wird Internet Explorer 11 für solche Dynamics 365-Produkte nicht mehr unterstützt. |
| **Ersetzt durch eine andere Funktion?**   | Wir empfehlen den Kunden den Übergang zu Microsoft Edge.|
| **Betroffene Produktbereiche**         | Alle Dynamics 365-Produkte |
| **Bereitstellungsoption**              | Alle|
| **Status**                         | Veraltet. Internet Explorer 11 wird nach August 2021 nicht mehr unterstützt.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.12

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Nicht außer Betrieb genommen: Polnische SSRS-Berichte: Umsatzsteuerkartei, Kaufsteuerkartei, EU-Summensteuerkartei – Funktion Referenz PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Nicht rechtlich obligatorisch.  |
| **Ersetzt durch eine andere Funktion?**   | Ja (Excel-Format für Standard-Auditdatei mit Umsatzsteuererklärung – JPK_VDEK) |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Nicht außer Betrieb genommen: Ab dem 27. April 2021 ist geplant, die SSRS-Berichte weiterhin zu unterstützen: **Verkaufs-Mehrwertsteuerregister, Kauf-Mehrwertsteuerregister, EU-Summen-Mehrwertsteuerregister – Funktionsreferenz PL-00014**. Ein Beispiel für ein Excel-Format für eine Standard-Prüfungsdatei mit Mehrwertsteuererklärung (JPK_VDEK) wurde ebenfalls eingeführt. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.11

### <a name="norwegian-standard-main-accounts"></a>Norwegische Standard-Hauptkonten

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Neugestaltung  |
| **Ersetzt durch eine andere Funktion?**   | Ja (ersetzt durch anwendungsspezifische Parameter im ER-Format) |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Bis zum 1. April 2021 planen wir, Funktionen für Standardhauptkonten nicht mehr zu unterstützen: Referenzfeld, zugehörige Tabelle, Datenentität. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.7

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Das Dialogfeld für die Änderung von Workflow-Anforderungen enthält nicht mehr die Dropdown-Liste für die Benutzerauswahl.

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Geändert in die Funktion mit Kontogruppenauswahl.  |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Workflow |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Wir planen, die chinesischen Belegtypen-Einstellungen ohne Kontogruppenauswahl bis zum 1. Dezember 2020 nicht mehr zu unterstützen. Zusätzliche Details für das neue Design in [Was ist neu in 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Frühere Ankündigungen über entfernte oder veraltete Funktionen
Um mehr über Funktionen zu erfahren, die in früheren Versionen entfernt oder veraltet sind, siehe [Entfernte oder veraltete Funktionen in früheren Versionen](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
