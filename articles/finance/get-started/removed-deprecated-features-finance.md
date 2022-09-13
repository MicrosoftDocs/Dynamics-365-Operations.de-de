---
title: Entfernte oder veraltete Funktionen in Dynamics 365 Finance
description: In diesem Artikel werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Finance.
author: kfend
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 83fa9d0a08d4d9ec171aeee685d39bba46e5687d
ms.sourcegitcommit: 6fd44fc6e9a7bad197cab58c36ec25a555724cf1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410449"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Entfernte oder veraltete Funktionen in Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen beschrieben, die entfernt wurden oder entfernt werden sollen von Dynamics 365 Finance.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Diese Liste soll ihnen dabei helfen, diese entfernten und veralteten Funktionen bei Ihrer eigenen Planung zu berücksichtigen. 

> [!NOTE]
> Ausführliche Informationen über Objekte in Apps für Finanzen und Betrieb finden Sie in den [Technischen Referenzberichten](/dynamics/s-e/global/axtechrefrep_61). Sie können die verschiedenen Versionen dieser Berichte vergleichen, um sich über Objekte zu informieren, die in den einzelnen Versionen der Apps für Finanzen und Betrieb geändert oder entfernt wurden.

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.30

### <a name="revenue-recognition"></a>Umsatzerlöserkennung

[Umsatzerlöserkennung](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Grund für veralteten Zustand/Entfernung** |Ersetzt durch verbesserte Funktionalität, [Abonnementabrechnung](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche** | Anwendung |
| **Bereitstellungsoption** | Alle |
| **Status** | Veraltet: Nach April 2023 wird die Umsatzrealisierungsfunktion in Dynamics 365 Finance nicht mehr mit Fehlerbehebungen unterstützt. Kunden werden gebeten, die verbesserte Funktionalität [Abonnementabrechnung](../../finance/accounts-receivable/subscription-billing-summary.md) zu nutzen. Ab Oktober 2023 ist die Funktion „Umsatzrealisierung“ nicht mehr verfügbar. Kunden werden gebeten, auf die verbesserte Funktionalität „Abonnementabrechnung“ umzustellen.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.29

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Umlagerungsaufträge mit Steuer auf den Verrechnungspreis

[Umlagerungsaufträge mit Steuer auf den Verrechnungspreis](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch verbesserte Funktionalität, [Umlagerungsaufträge für Indien](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche** | Anwendung |
| **Bereitstellungsoption** | Alle |
| **Status** | Veraltet: Nach April 2023 wird die Funktion **Umlagerungsaufträge, die Steuern auf den Transferpreis enthalten** nicht mehr mit Fehlerkorrekturen und Sicherheitskorrekturen unterstützt. Kunden werden gebeten, die verbesserte Funktionalität [Umlagerungsaufträge für Indien](../../finance/localizations/apac-ind-stock-transfer.md) zu nutzen. Nach Oktober 2023 wird die Funktion **Umlagerungsaufträge, die Steuern auf den Transferpreis enthalten** nicht mehr verfügbar sein, und die Kunden werden gebeten, auf die verbesserte Funktionalität umzusteigen. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Bankauszug importieren und Dateien für positive Zahlungen exportieren

| &nbsp;  | &nbsp;  |
|---|---|
| **Grund für veralteten Zustand/Entfernung** |Durch die verbesserte Funktionalität ersetzt, Bankauszüge importieren und Dateien für positive Zahlungen exportieren.| 
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Anwendung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Die XSLT-Funktionalität zum Importieren und Exportieren von Dateien wird nicht mehr mit Fehlerkorrekturen und Sicherheitskorrekturen unterstützt. Kunden werden gebeten, die verbesserte Funktion zu verwenden: [Dateien für positive Zahlungen mithilfe der elektronischen Berichterstellung einrichten](../../finance/accounts-payable/set-up-positive-pay-er.md) und [Erweiterten Bankabstimmungsimport mithilfe der elektronischen Berichterstellung einrichten](../../finance/accounts-payable/import-bai2-er.md). Nach September 2022 wird die XSLT-Funktionalität nicht mehr verfügbar sein und Kunden werden gebeten, auf die verbesserte Funktionalität umzusteigen.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.26

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Mehrwertsteuer-Bericht für Finnland (Entwurf auf der Grundlage von Meldecodes)

[Mehrwertsteuererklärung für Finnland](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch ein neues Design für die Mehrwertsteuererklärung, [Mehrwertsteuererklärung für Finnland](../localizations/emea-fin-vat-declaration.md). |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Anwendung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Außer Betrieb genommen: Ab dem 1. März 2023 werden wir den Mehrwertsteuer-Bericht für Finnland (finnisches Berichtslayout) nicht mehr unterstützen. Neue **Mehrwertsteuererklärung TXT (FI**) und **Mehrwertsteuererklärung Excel (FI)** Elektronische Berichterstattung (ER) werden unter dem **Steuererklärung**-Modell eingeführt. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.24

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Mehrwertsteuererklärung für Schweden (Design basierend auf Erklärungscodes)

[Mehrwertsteuererklärung für Schweden](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch ein neues MwSt.-Erklärungsdesign, [Umsatzsteuererklärung für Schweden](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab dem 1. Dezember 2022 wird die Mehrwertsteuererklärung für Schweden (schwedisches Berichtslayout) nicht mehr unterstützt. Stattdessen werden im Modell **Steuererklärung** die neuen elektronischen Berichterstellungs(EB)-Formate **Umsatzsteuererklärung XML (SE)** und **Umsatzsteuererklärung Excel (SE)** eingeführt. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>MwSt.-Abrechnung für Österreich (Design basierend auf Erklärungscodes)

[MwSt-Berichtdetails für Österreich](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch ein neues MwSt.-Erklärungsdesign, [Umsatzsteuererklärung für Österreich](../localizations/emea-aut-vat-declaration-austria.md) |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab dem 1. Dezember 2022 planen wir, das elektronische Berichtsformat (EB) **MwSt.-Erklärung (AT)** unter **Mehrwertsteuererklärungsmodell** nicht mehr zu unterstützen. Stattdessen werden im Modell **Steuererklärung** die neuen Formate **Umsatzsteuererklärung XML (AT)** und **Umsatzsteuererklärung Excel (AT)** eingeführt. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ELSTER-Erklärung für Deutschland (Design basierend auf Erklärungscodes)

[MwSt.-Abrechnung](../localizations/emea-de-vat-declaration.md)</br>
[Einrichtung der elektronischen Steuererklärung für Deutschland](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[Elektronische Übermittlung der Umsatzsteuererklärung (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch ein neues MwSt.-Erklärungsdesign, [Umsatzsteuererklärung für Deutschland](../localizations/emea-deu-vat-declaration-germany.md) |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab dem 1. Dezember 2022 planen wir, die elektronischen Berichtsformate (EB) **Elster (DE)** und **Elster-Modell** nicht mehr zu unterstützen. Stattdessen werden im Modell **Steuererklärung** die neuen Formate **Umsatzsteuererklärung XML (DE)** und **Umsatzsteuererklärung Excel (DE)** eingeführt. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>OB-Meldung für die Niederlande (Design basierend auf Erklärungscodes)

[OB-Meldung](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ersetzt durch ein neues MwSt.-Erklärungsdesign, [Umsatzsteuererklärung für die Niederlande](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Ersetzt durch eine andere Funktion?**   | Ja |
| **Betroffene Produktbereiche**         | Bewerbung |
| **Bereitstellungsoption**              | Alle |
| **Status**                         | Veraltet: Ab dem 1. Dezember 2022 planen wir, die elektronischen Berichtsformate (EB) **OB-Meldung (NL)** und **OB-Meldungsmodell** nicht mehr zu unterstützen. Stattdessen werden im Modell **Steuererklärung** die neuen Formate **Umsatzsteuererklärung XML (NL)** und **Umsatzsteuererklärung Excel (NL)** eingeführt. |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Entfernte oder veraltete Funktionen in Finance Release 10.0.20

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>Konfiguration des Formats der elektronischen Berichterstellung (ER) „RTIR-Abfrage von Rechnungsdatenanforderungen (HU)“

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Grund für veralteten Zustand/Entfernung** | Ausgenommen von der Verarbeitung elektronischer Nachrichten für die Zusammenarbeit mit dem ungarischen Online-Abrechnungssystem |
| **Ersetzt durch eine andere Funktion?**   | Nein |
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

