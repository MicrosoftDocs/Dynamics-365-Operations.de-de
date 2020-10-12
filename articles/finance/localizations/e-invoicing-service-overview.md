---
title: Übersicht über das Add-On für die elektronische Rechnungsstellung
description: Dieses Thema enthält Informationen zum Add-On für die elektronische Rechnungsstellung in Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b3445157efce6349b3febafb6c860260052f7d6c
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835958"
---
# <a name="electronic-invoicing-add-on-overview"></a>Übersicht über das Add-On für die elektronische Rechnungsstellung

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Das Add-On für die elektronische Rechnungsstellung für Microsoft Dynamics 365 Finance und Dynamics 365 Supply Chain Management ist ein hyperskalierbarer mandantenfähiger Dienst, der die konfigurierbare Verarbeitung elektronischer Rechnungsdokumente sowie den konfigurierbaren Dokumentenaustausch ermöglicht. Die Verarbeitungs- und Integrationsregeln sind vollständig konfigurierbar und die Logik wird außerhalb von Finance und Supply Chain Management ausgeführt. Der Dienst zielt hauptsächlich auf die Verarbeitung elektronischer Rechnungen in Übermittlungsszenarien zwischen Unternehmen und Behörden ab, kann jedoch auch für andere Zwecke konfiguriert werden.

Mit dem Add-On für die elektronische Rechnungsstellung können Sie die folgenden Ziele erreichen:

- Schnelle und einfache Übernahme landes-/regionsspezifischer Anforderungen
- Standardisierte Implementierungen einer Add-On-Lösung für die elektronische Rechnungsstellung
- Verbesserte Rückverfolgbarkeit des Dokumentverlaufs
- Kürzerer Implementierungszyklus
- Senkung der Gesamtbetriebskosten
- Leicht anpassbare Konfigurationen, für die keine Codeänderungen erforderlich sind
- Vereinfachte Konfigurationsverpackung
- Integrierter Export, Import und Integration sowie einfache Erweiterbarkeit bei der Verarbeitung elektronischer Rechnungsdokumente
- Einfache Wiederverwendung derselben Export-, Import- und Integrationskonfigurationen in allen Unternehmen

Um das Add-On für die elektronische Rechnungsstellung verwenden zu können, müssen Sie es über Ihr Projekt in Microsoft Dynamics Lifecycle Services (LCS) installieren. Befolgen Sie anschließend die Einrichtungsprozedur um die Integration in Finance oder Supply Chain Management zu aktivieren. Weitere Informationen finden Sie unter [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md).

## <a name="availability"></a>Verfügbarkeit

Zunächst steht das Add-On für die elektronische Rechnungsstellung ausgewählten Kunden über ein Vorschauprogramm zur Verfügung. Später wird die Vorschau für weitere Kunden verfügbar gemacht. Schlussendlich wird der Dienst allgemein verfügbar sein. Da Funktionen, die landes-/regionsspezifische Anforderungen berücksichtigen, in verschiedenen Phasen des Release möglicherweise eingeschränkt sind, sollten Sie sich stets anhand der aktuellsten Dokumentation informieren, in der die Abdeckung und der Umfang der unterstützten landes-/regionsspezifischen Lösungen hervorgehoben werden.

Das Add-On für die elektronische Rechnungsstellung wird in den folgenden Azure-Regionen bereitgestellt:

- Vereinigte Staaten
- Europa

> [!NOTE]
> Das Add-On für die elektronische Rechnungsstellung unterstützt keine lokalen Bereitstellungen.

## <a name="extended-configurability"></a>Erweiterte Konfigurierbarkeit

Das Add-On für die elektronische Rechnungsstellung kann in Szenarien verwendet werden, in denen Sie ein elektronisches Dokument erstellen und an die vorgesehenen Parteien senden müssen. Es wurde speziell für die Ausführung eines konfigurierbaren Flows von Verarbeitungsaktionen basierend auf empfangenen Daten entwickelt. Die Konfigurationsoptionen, die in Finance und Supply Chain Management verfügbar sind, beschränken sich auf die Dokumentumwandlung. Der Dienst erweitert diese Optionen um die konfigurierbaren Integrationen, die darin verfügbar sind. Darüber hinaus werden alle zuvor verfügbaren Funktionen für elektronische Rechnungen, z. B. Nota Fiscal Eletrônica (NF-e) für Brasilien, Comprobante Fiscal Digital por Internet (CFDI) für Mexiko oder andere UBL-/PEPPOL-Funktionen (Universal Business Language / Pan-European Public Procurement OnLine) für Westeuropa, Konfigurationen für den Export und Import sowie für die Integration in externe Webdienste verwenden.

## <a name="feature-highlights"></a>Besondere Funktionen

- Vordefinierte Integration in Finance und Supply Chain Management
- Konsistente Benutzererfahrung für die Konfiguration und Überwachung des elektronischen Rechnungsprozesses für alle Länder oder Regionen
- Schnellere, einfachere und kostengünstigere Einführung von Add-On-Lösungen für die elektronische Rechnungsstellung in neuen Ländern oder Regionen
- Konfiguration des Dienstes über die Einrichtung des Regulatory Configuration Service (RCS) und der Globalisierungsfunktion
- Transformation von Geschäftsdaten in mehrere elektronische Rechnungsformate (XML, JavaScript Object Notation \[JSON\], TXT und durch Komma getrennten Werte \[CSV\]) mithilfe von Konfigurationen, die in RCS definiert sind:

    - Elektronische Berichtsformate, die für Länder oder Regionen verfügbar sind, in denen die Konfigurierbarkeit für die Transformation elektronischer Rechnungen nicht verfügbar ist

- Konfigurierbare Übermittlung von elektronischen Rechnungen an externe Webdienste, einschließlich der Bearbeitung von Zertifizierungen durch digitale Signaturen:

    - Integrierte, leicht erweiterbare und konfigurierbare Integration mit zusätzlichen Inhalten für mehrere Länder

    > [!NOTE]
    > Derzeit wird eine begrenzte Anzahl von direkten Übermittlungen unterstützt. Weitere Informationen finden Sie im Abschnitt [Verfügbarkeit](#availability) weiter oben in diesem Thema. Der Support wird in Zukunft erweitert.

- Behandlung von Antworten von Webdiensten, einschließlich konfigurierbarer Behandlung von Ausnahmemeldungen
- Unterstützung für elektronische Signaturen (z. B. mithilfe des XMLDSig-Signaturalgorithmus)
- Stapelverarbeitung von elektronischen Rechnungsnachrichten

## <a name="architecture-and-data-flow"></a>Architektur und Datenfluss

Wenn das Add-On für die elektronische Rechnungsstellung über LCS installiert wird und die erforderliche Einrichtung in allen erforderlichen Anwendungen abgeschlossen ist, wird eine sichere Verbindung hergestellt. Der Dienst befindet sich derzeit in Rechenzentren in den USA und in Europa. Daher kann sich der Standort des Dienstes vom Standort der zugehörigen Instanz von Finance oder Supply Chain Management unterscheiden. Nachdem Sie die Einrichtung des Add-Ons für die elektronische Rechnungsstellung abgeschlossen und die Integration aktiviert haben, werden bei jedem Versand einer elektronischen Rechnung Masterdaten und Transaktionsdaten, die sich auf ein bestimmtes Dokument beziehen, an das Add-On für die elektronische Rechnungsstellung gesendet.

> [!NOTE]
> Wenn Ihre elektronische Rechnung oder ein anderes Dokument persönliche Daten enthält, überprüfen Sie, ob Ihre Verwendung dieser Funktion der Datenschutz-Grundverordnung (DSGVO) und anderen Bestimmungen im Zusammenhang mit der Übermittlung persönlicher Daten entspricht.

### <a name="high-level-description-of-the-data-flow"></a>Übergeordnete Beschreibung des Datenflusses

1. Der Client sendet ein vorschriftsmäßiges Geschäftsdokument an den Dienst.
2. Basierend auf den Kontextinformationen, die vom Client empfangen werden, wählt der Dienst den entsprechenden Verarbeitungs-Flow aus.
3. Der Dienst führt die Verarbeitungsaktionen aus. Diese Aktionen können das Transformieren des Geschäftsdokuments in eine elektronische Rechnung, das Anwenden einer elektronischen Signatur und das Übermitteln des Dokuments an einen externen Webdienst umfassen.
4. Alle empfangenen und verarbeiteten Dokumente werden im Azure Blob-Speicher des Kunden gespeichert.
5. Alle für die Verarbeitung verwendeten Mandantengeheimnisse und -zertifikate werden im Azure-Schlüsseltresor des Kunden gespeichert.
6. Der Dienst stellt dem Kunden bei Bedarf Informationen zum Verarbeitungsstatus des gesendeten Geschäftsdokuments zur Verfügung.
7. Der Client empfängt Informationen über die abgeschlossene Verarbeitung und stellt alle Protokollinformationen zur Verfügung. Außerdem wird das Dokument verfügbar gemacht, das während der Flow-Verarbeitung erstellt oder empfangen wurde.

Die folgende Abbildung zeigt, wie Daten zum und vom Add-On für die elektronische Rechnungsstellung fließen.

![Datenfluss für das Add-On für die elektronische Rechnungsstellung](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>Datenschutzhinweis
Für die Aktivierung und Verwendung der elektronischen Rechnungsstellung müssen möglicherweise nur begrenzte Daten gesendet werden, einschließlich der Steuerregistrierungskennung für die Organisation. Diese Daten werden an von den Steuerbehörden autorisierte Drittagenturen weitergeleitet, um elektronische Rechnungen in den für die Integration in den Webdienst der Behörde erforderlichen Formaten zu senden. Daten, die aus diesen externen Systemen in diesen Dynamics 365-Onlinedienst importiert werden, unterliegen unseren [Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=512132). Weitere Informationen finden Sie in den Abschnitten zum Datenschutz in der landesspezifischen Funktionsdokumentation.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung](e-invoicing-get-started.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Brasilien](e-invoicing-bra-get-started.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Mexiko](e-invoicing-mex-get-started.md)
- [Erste Schritte mit dem Add-On für die elektronische Rechnungsstellung für Italien](e-invoicing-ita-get-started.md)
- [Einrichten des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-setup.md)
