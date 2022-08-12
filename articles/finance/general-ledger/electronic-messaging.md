---
title: Elektronisches Messaging
description: Dieser Artikel enthält eine Übersicht und Einrichtungsinformationen für elektronisches Messaging in Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4e765c6d56e0ab6d209c27a70fd4b7e52273c103
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069879"
---
# <a name="electronic-messaging"></a>Elektronisches Messaging

[!include [banner](../includes/banner.md)]

In diesem Artikel erhalten Sie einen Überblick über die Funktionalität **Elektronische Nachrichten** (EN).

Vor kurzem haben die Behörden und die gesetzgebenden Instanzen aus verschiedenen Ländern und Regionen der Welt Meldeanforderungen für Unternehmen implementiert, die in diesen Ländern oder Regionen registriert sind. Anhand dieser Anforderungen sollen Daten von diesen Unternehmen in elektronischem Format bezogen werden, direkt aus den Systemen, in denen sie kalkuliert, gespeichert und verarbeitet werden.

Die EN-Funktionalität in Microsoft Dynamics 365 Finance unterstützt verschiedene Prozesse zum elektronischen dialogfähigen Betrieb zwischen Finance und den Systemen, die Regierungen und gesetzgebende Instanzen zur Berichterstellung, Übermittlung und dem Empfang von amtlichen Informationen anbieten.

Die EN-Funktionalität ist in das Modul **Elektronische Berichterstellung** (EB) integriert. Sie können die EB-Formate für elektronische Nachrichten einrichten. Weitere Informationen finden Sie unter [Elektronische Berichterstellung (EB)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>Grundlegende Konzepte der EN-Funktionalität

Die EN-Funktionalität basiert auf den folgenden Entitäten:

- **Elektronische Nachricht** – Eine Bericht oder eine Erklärung, der intern gemacht bzw. die intern übermittelt werden soll, z. B. eine Meldung an ein Finanzamt.
- **Elektronische Nachrichtenelemente** – Datensätze, die in die Nachricht eingeschlossen werden sollen, die gemeldet wird.
- **Verarbeiten der elektronischen Nachricht** – Eine Kette von Aktivitäten, die ausgeführt werden sollte, um die erforderlichen Daten zu sammeln, Berichte zu generieren, Daten in Azure Blob Storage zu speichern, Berichte außerhalb des Systems zu übermitteln, Antworten von außerhalb des Systems zu empfangen und die Datenbank anhand empfangener Informationen zu aktualisieren. Die Aktivitäten in der Kette können entweder verknüpft oder unverknüpft sein.

Die folgende Abbildung zeigt den EN-Datenfluss.

![Datenfluss elektronischer Nachrichten.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>Von der EN-Funktionalität unterstützte Szenarien

Die EN-Funktionalität unterstützt die folgenden Szenarien:

- Manuelles Erstellen von Nachrichten und Generieren von Berichten, die auf zugeordneten EB-Formaten verschiedener Typen für das Exportieren basieren. Zu diesen Typen gehören Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, Text und Microsoft Word.
- Automatisches Erstellen und Verarbeiten von Nachrichten, die auf Informationen basieren, die von einer Behörde mithilfe eines zugeordneten EB-Formats für den Import angefordert und empfangen wurden.
- Sammeln und Verarbeiten von Informationen aus einer Datenquelle als Nachrichtenelemente. Die Datenquelle für eine Finance-Tabelle.
- Zusätzliche Informationen speichern und verschiedene Werte auswerten, indem speziell definierte ausführbare Klassen in Relation zu Nachrichten und Nachrichtenelementen aufgerufen werden.
- Aggregieren von Informationen, die in Nachrichtenelementen gesammelt werden, Aufteilung dieser Informationen nach Nachricht und Generieren von Berichten, die in zugeordneten Export-EB-Formaten sind.
- Übermitteln der Berichte, die für einen Webdienst mithilfe von Sicherheitsinformationen generiert werden, die im Azure Key Vault gespeichert sind.
- Empfangen einer Antwort über einen Webdienst, Interpretieren der Antwort und Aktualisieren der Daten in Finance je nach Bedarf.
- Speichern und Überprüfen aller Berichte, die generiert werden.
- Speichern und Überprüfen aller Protokollinformationen, die Aktivitäten zugeordnet sind, die für die eine Nachricht oder ein Nachrichtenelement ausgeführt werden.
- Steuern der Verarbeitung durch verschiedene Nachrichtenstatus und Nachrichtenelementstatus.

## <a name="security-privileges"></a>Sicherheitsrechte

Die folgenden Sicherheitsrechte sind für elektronische Nachrichten verfügbar.

| Sicherheitsrecht           | Zugriffsebene | Zuordnung |
|------------------------------|--------------|-------------|
| Elektronische Nachrichten verwalten | Dieses Recht gewährt vollen Zugriff auf die EM-Funktionalität. Wenn Sie über dieser Recht verfügen, können Sie die elektronische Nachrichtenübermittlung einrichten und die gesamte Verarbeitung ausführen. | Dieses Recht ist in der Sicherheitspflicht **Mehrwertsteuerbuchungen verwalten** enthalten. Diese Pflicht wiederum ist in der Sicherheitsrolle **Buchhalter** enthalten. |
| Elektronische Nachrichten anzeigen     | Dieses Recht gewährt Lesezugriff auf die EM-Funktionalität. Wenn Sie über dieser Recht verfügen, können Sie die Einstellungen für elektronische Nachrichten sowie die Nachrichten selbst anzeigen. Sie können jedoch nichts einrichten oder ausführen. | Dieses Recht ist in der Sicherheitspflicht **Status von Mehrwertsteuerbuchungen abfragen** enthalten. Diese Pflicht wiederum ist in den folgenden Sicherheitsrollen enthalten:<ul><li>Leiter Inkasso</li><li>Sachbearbeiter Debitorenkonten</li><li>Leiter Debitorenkonten</li><li>Steuerberater</li><li>Sachbearbeiter Buchhaltung</li><li>Leiter Buchhaltung</li><li>Supervisor Buchhaltung</li><li>Verkaufsleiter</li><li>Sachbearbeiter Kreditorenkonten</li></ul> |
| Elektronische Nachrichten verarbeiten  | Dieses Recht gewährt nur Zugriff auf die Seiten **Elektronische Nachrichten** und **Elektronische Nachrichtenelemente**. Wenn Sie über dieses Recht verfügen, können Sie die gesamte Verarbeitung ausführen, die über diese Seiten aufgerufen wird. | Dieses Recht ist in der Sicherheitspflicht **Elektronische Nachrichten betreiben** enthalten. Diese Pflicht wiederum ist in der Sicherheitsrolle **Operator elektronische Nachrichten** enthalten. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Länderspezifische rechtliche Funktionen, die von der EN-Funktionalität unterstützt werden

Die folgende Tabelle enthält Informationen zu einigen länderspezifischen rechtlichen Funktionen, die von der EN-Funktionalität unterstützt werden.

| Land     | Funktionsname | Funktionsdemoaufzeichnung |
|-------------|--------------|------------------------|
| Spanien       | [Sofortige Bereitstellung von Informationen zur MwSt. (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungarn     | [Online-Fakturierungssystem](../localizations/emea-hun-online-invoicing.md) | |
| Vereinigtes Königreich | [Digitale Steuer (MTD) – Abgabe der Mehrwertsteuerklärung](../localizations/emea-gbr-mtd-vat-integration.md) | [Finanzen und Betrieb: UK Digital Tax – MwSt.-Erklärung in Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litauen   | [i.SAF-Berichterstattung](../localizations/emea-ltu-isaf.md) | |
| Polen      | [Mehrwertsteuererklärung mit Registern (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK-Umsatzsteuerprüfungsregister](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Niederlande | [MwSt.-Erklärung für die Niederlande](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tschechische Republik | [MwSt.-Erklärung](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasilien      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Russische Föderation      | [MwSt.-Erklärung](../localizations/rus-vat-declaration.md) | |
| Russische Föderation      | [Buchhaltungsberichte im elektronischen Format](../localizations/rus-accounting-reporting.md) | |
| Russische Föderation      | [Gewinnsteuererklärung](../localizations/rus-profit-tax-declaration.md) | |
| Russische Föderation      | [Veranschlagte Steuererklärung](../localizations/rus-assessed-tax-declaration.md) | |
| Russland      | [Transportsteuererklärung](../localizations/rus-transport-tax-declaration.md) | |
| Russland      | [Grundsteuererklärung](../localizations/rus-land-tax-declaration.md) | |
| Norwegen      | [MwSt.-Erklärung mit direkter Übermittlung an Altinn](../localizations/emea-nor-vat-return.md) | [Neue Umsatzsteuererklärung mit direkter Übermittlung an Altinn in Dynamics 365 Finance](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Frankreich      | [Mehrwertsteuererklärung (Frankreich)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Österreich     | [Mehrwertsteuererklärung (Österreich)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Deutschland     | [Umsatzsteuererklärung (Deutschland)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Niederlande | [MwSt.-Erklärung für die Niederlande](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Schweden      | [Mehrwertsteuererklärung (Schweden)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Schweiz | [Mehrwertsteuererklärung (Schweiz)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


