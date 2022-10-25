---
title: Invoice Capture-Lösungübersicht
description: Dieser Artikel enthält Informationen zur Invoice Capture-Lösung.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691160"
---
# <a name="invoice-capture-solution"></a>Invoice Capture-Lösung

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dieser Artikel enthält Informationen zur Invoice Capture-Lösung, die Kreditorenrechnungen automatisch aus digitalen Rechnungsbildern erstellt.

Die Abteilung Kreditorenkonten (AP) verwaltet und verarbeitet Rechnungen für erhaltene Waren und Dienstleistungen. Der Kreditorenbuchhalter überprüft Daten auf Kreditorenrechnungen aus folgenden Gründen:

- Um zusätzlichen Aufwand zu vermeiden, wenn während des Periodenabschlusses Anpassungen oder Korrekturen erforderlich sind
- Um Lieferantenrechnungen rechtzeitig zu bezahlen und finanzielle Verluste aufgrund von Fehlern oder Betrug zu vermeiden

Die optische Zeichenerkennung (OCR) ist in den letzten Jahren in verschiedenen Branchen weit verbreitet. Mittlerweile ist es üblich, gedruckte Texte zu digitalisieren, damit sie elektronisch bearbeitet, durchsucht, kompakter gespeichert und online angezeigt werden können. Der digitale Text kann in maschinellen Prozessen wie Cognitive Computing, maschineller Übersetzung, Text-to-Speech, Schlüsseldaten und Text Mining verwendet werden.

Die Entwicklung der Technologie der künstlichen Intelligenz (KI) hat es modernen OCR-Lösungen ermöglicht, verschiedene Rechnungsformate von verschiedenen Anbietern zu lesen, ohne dass viel menschliches Eingreifen erforderlich ist. Immer mehr Unternehmen erkennen, dass sie Aufwand sparen und die Genauigkeit verbessern können, indem sie Rechnungen automatisiert statt manuell verarbeiten.

## <a name="system-landscape"></a>Systemlandschaft

Die folgende Abbildung zeigt die Hauptkomponenten und Schritte der Invoice Capture-Lösung.

[![Komponenten und Schritte in der Invoice Capture-Lösung.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Erforderliche Rollen

Die folgende Tabelle zeigt die Rollen, die zum Einrichten und Verwenden der Invoice Capture-Lösung erforderlich sind.

| Rolle          | Aktionen | Systeme | Rollennamen |
|---------------|---------|---------|-----------|
| Administrator | <ul><li>Umgebungen in Microsoft Power Platform einrichten.</li><li>Lösungen in Microsoft Power Platform bereitstellen.</li><li>Richten Sie Verbindungen zwischen Dynamics 365 und AI Builder ein.</li><li>Azure Data Lake Storage Standorte einrichten.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Dynamics 365-Administrator</li><li>Power Platform-Administrator</li><li>Datenbesitzer des Speicher-Blobs</li></ul> |
| KI-Hersteller      | <ul><li>Flows aufrechterhalten.</li><li>Benutzerdefinierte KI-Modelle erstellen.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Bürger Macher</li></ul> |
| AP-Angestellter      | <ul><li>Überprüfen und ergreifen Sie Maßnahmen im Bereitstellungsbereich für Kreditorenrechnungen.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Neue Rolle als Kreditorenbuchhalter in Power Platform</li></ul> |
| AP-Angestellter      | <ul><li>Führen Sie den täglichen Betrieb als Kreditorenbuchhalter durch.</li><li>Navigieren Sie zum Bereitstellungsbereich für Kreditorenrechnungen.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Sachbearbeiter Kreditorenkonten</li></ul> |
  
Weitere Informationen zum Installieren der Rechnungserfassung finden Sie unter [Invoice Capture installieren](../accounts-payable/install-invoice-capture.md).  
