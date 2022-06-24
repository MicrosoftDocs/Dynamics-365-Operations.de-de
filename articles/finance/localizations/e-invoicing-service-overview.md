---
title: Informationen zur elektronischen Rechnungsstellung
description: Dieser Artikel bietet einen Überblick über die Elektronische Rechnungsstellung in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 4ce5776216855fc664b9beba68036d41920ae602
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861295"
---
# <a name="electronic-invoicing-overview"></a>Informationen zur elektronischen Rechnungsstellung

[!include [banner](../includes/banner.md)]

Elektronische Rechnungsstellung für Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management ist ein hyperskalierbarer mandantenfähiger Dienst, der die konfigurierbare Verarbeitung elektronischer Rechnungen und den konfigurierbaren Austausch elektronischer Belege ermöglicht. Die Verarbeitungs- und Integrationsregeln sind vollständig konfigurierbar und die Logik wird außerhalb von Finance und Supply Chain Management ausgeführt. Der Dienst ist hauptsächlich für die Verarbeitung elektronischer Belege in Business-to-Government-Szenarien gedacht. Es kann jedoch für andere Zwecke angepasst werden, z.B. für business-to-business Szenarien für verschiedene Arten von Dokumenten.

Mit der elektronischen Rechnungsstellung können Sie die folgenden Ziele erreichen:

- Schnelle und einfache Übernahme landes-/regionsspezifischer Anforderungen
- Standardisierte Implementierungen einer Lösung für die elektronische Rechnungsstellung
- Verbesserte Rückverfolgbarkeit des Dokumentverlaufs
- Kürzerer Implementierungszyklus
- Senkung der Gesamtbetriebskosten
- Leicht anpassbare Konfigurationen, die keine Codeänderungen erfordern
- Vereinfachte Konfigurationsverpackung
- Integrierter Export, Import und Integration sowie einfache Erweiterbarkeit bei der Verarbeitung elektronischer Belege für Rechnungen
- Einfache Wiederverwendung derselben Export-, Import- und Integrationskonfigurationen in allen Unternehmen

## <a name="service-availability"></a>-Dienstverfügbarkeit

Derzeit ist die Elektronische Rechnungsstellung nur für Kunden aus den Bereichen Finance und Supply Chain Management verfügbar. Weitere Informationen finden Sie in den Lizenzbedingungen für Ihre Anwendung.

Da die Funktionalität, die länder- bzw. regionalspezifische Anforderungen erfüllt, in verschiedenen Phasen der Veröffentlichung eingeschränkt sein kann, sollten Sie immer die aktuellste Dokumentation lesen, die den Umfang der unterstützten länder- bzw. regionalspezifischen Lösungen aufzeigt.

Die elektronische Rechnungsstellung wird in den folgenden Azure-Regionen bereitgestellt:

- USA
- Europa
- Asien

> [!NOTE]
> Die elektronische Rechnungsstellung unterstützt keine lokalen Bereitstellungen.

## <a name="feature-highlights"></a>Besondere Funktionen

- Standardmäßige Integration mit Finance und Supply Chain Management
- Eine einheitliche Benutzererfahrung für die Konfiguration und Überwachung des elektronischen Rechnungsprozesses für alle Länder und Regionen
- Schnellere, einfachere und kostengünstigere Einführung von Lösungen für die elektronische Rechnungsstellung in neuen Ländern oder Regionen
- Konfiguration des Dienstes durch die Einrichtung von Regulatory Configuration Service (RCS) und Globalisierungsfunktionen
- Umwandlung von Geschäftsdaten in mehrere elektronische Rechnungsformate (XML, JavaScript Object Notation \[JSON\], TXT und kommagetrennte Werte \[CSV\]) unter Verwendung von Konfigurationen, die in RCS definiert sind:

    - Elektronische Berichtsformate (ER), die für Länder und Regionen verfügbar sind, in denen die Konfigurierbarkeit für die elektronische Rechnungsumwandlung nicht verfügbar ist

- Konfigurierbare Übermittlung elektronischer Rechnungen an externe Webdienste, einschließlich der Handhabung von Zertifikaten durch digitale Signaturen:

    - Integrierte, leicht erweiterbare und konfigurierbare Integration mit zusätzlichen Inhalten für mehrere Länder und Regionen

- Behandlung von Antworten aus Webdiensten, einschließlich konfigurierbarer Behandlung von Ausnahmenachrichten
- Unterstützung für elektronische Signaturen (z.B. elektronische Signaturen, die den XMLDSig-Signieralgorithmus verwenden)
- Die Funktionalität, Dokumente an E-Mails zu senden und sie in SharePoint zu speichern
- Batch-Verarbeitung von elektronischen Nachrichten über Rechnungen
- Konfigurierbare Umwandlung von eingehenden Belegen und Verarbeitung dieser Belege im Finance und Supply Chain Management
- Die Funktionalitäten für den Empfang eingehender Belege über Kanäle wie E-Mail und SharePoint.

## <a name="privacy-notice"></a>Datenschutzhinweis

Die Aktivierung und Verwendung der Elektronischen Rechnungsstellung kann die Übermittlung begrenzter Daten erfordern. Zu diesen Daten gehört die Steueridentifikationsnummer der Organisation. Diese Daten werden an Drittanbieter übermittelt, die von den Steuerbehörden autorisiert sind, um elektronische Rechnungen in den vordefinierten Formaten zu versenden, die für die Integration mit staatlichen Webdiensten erforderlich sind. Daten, die aus diesen externen Systemen in diesen Dynamics 365-Online-Service importiert werden, unterliegen unserer [Datenschutzerklärung](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie in den Abschnitten zum Datenschutz in der landes-und regionenspezifischen Funktionsdokumentation.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
