---
title: Häufig gestellt Fragen zur elektronischen Rechnungsstellung
description: Dieses Thema enthält Informationen zu häufig gestellten Fragen zur elektronischen Rechnungsstellung.
author: gionoder
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 41cddcdad5043ec314a94dda67f4f2e9de406cac
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840171"
---
# <a name="electronic-invoicing-faq"></a>Häufig gestellt Fragen zur elektronischen Rechnungsstellung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Antworten auf häufig gestellte Fragen zur elektronischen Rechnungsstellung. Die elektronische Rechnungsstellung erweitert die Funktionen der elektronischen Rechnungsstellung, die in Dynamics 365 Finance, Dynamics 365 Supply Chain Management und Dynamics 365 Project Operations vorhanden sind. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Was ist an der elektronischen Rechnungsstellung wichtig und warum sollte es für mein Unternehmen von Bedeutung sein?

Die betriebliche Komplexität und das Risiko nehmen weiter zu, da Unternehmen global wachsen und ihre Präsenz in verschiedenen Regionen ausbauen. Die Einhaltung der Vorschriften und die Anpassung an sich häufig ändernde Vorschriften stellen eine wachsende Herausforderung dar und sind für die Rechnungsstellung von besonderer Bedeutung. Die Rechnungsstellung war traditionell teuer und fehleranfällig, da Unternehmen auf Papierdokumente und manuell intensive Prozesse angewiesen sind.  

Unternehmen haben begonnen, sich von Papierrechnungen zu entfernen, um Kosten zu senken und den End-to-End-Prozess zu beschleunigen. Die Regierungen wenden sich zunehmend der elektronischen Rechnungsstellung als Schlüsselkomponente der Steuerdigitalisierung zu. Durch die Verpflichtung von Organisationen, Steuerinformationen in Echtzeit digital an Steuerbehörden zu übermitteln, können Regierungen Steuerhinterziehung und -manipulation minimieren und Betrug reduzieren. 

Die Welt verlagert sich auf die papierlose Dokumentenverarbeitung. Ohne die Implementierung einer elektronischen Rechnungsstellung können Kunden Compliance-Probleme, unnötige Kosten und einen Rückstand gegenüber Wettbewerbern riskieren. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Enthalten Finance, Supply Chain Management und Project Operations nicht bereits Funktionen für die elektronische Rechnungsstellung? Welchen Wert bietet mir das als Kunde? 

Die elektronische Rechnungsstellung erweitert die Funktionen für die elektronische Rechnungsstellung, die in Finance, Supply Chain Management und Project Operations enthalten sind. Die Funktionalität vereinfacht auch die Einhaltung der neuesten Standards für die elektronische Rechnungsstellung und bietet kohärente Erfahrungen für verschiedene Regionen bei der Verarbeitung und dem Austausch elektronischer Rechnungen. Die Funktionen der elektronischen Rechnungsstellung bieten eine Reihe von Vorteilen, darunter: 

   - Schnellere und einfachere Übernahme landes-/regionsspezifischer Anforderungen.
   - Standardisierung der Implementierung von E-Invoicing-Lösungen. 
   - Verbesserte Rückverfolgbarkeit der Verarbeitung elektronischer Rechnungen.  
   - Einfachere Wartung zur Anpassung an sich ändernde gesetzliche Anforderungen und lokale Geschäftspraktiken. 
   - Vereinfachte Lösungsverpackung.
   - Skalierungsfunktionen für eine große Menge übermittelter Dokumente, die zu einer schnelleren Abwicklung führen.
   - Möglichkeit, Ihre Lösungen mit anderen Unternehmen zu teilen.

## <a name="does-electronic-invoicing-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Unterstützt die elektronische Rechnungsstellung die lokalen Installationen von Finance, Supply Chain Management und Project Operations? 

Die aktuelle Plattform erlaubt die Verwendung der lokalen Version nicht und es gibt keine Pläne, sie in Zukunft zu unterstützen.

## <a name="does-electronic-invoicing-interface-with-the-vendor-import-automation-feature"></a>Ist die elektronische Rechnungsstellung mit der Importautomatisierungsfunktion des Anbieters verbunden?

Nein. Es gibt Pläne für diese Schnittstelle, aber es gibt keine geplante Zeitskala. Wenn geplant, werden die Termine in [Release-Pläne](https://docs.microsoft.com/dynamics365/release-plans/) bekannt gegeben.

## <a name="how-does-electronic-invoicing-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Wie behandelt die elektronische Rechnungsstellung Dateianhänge in der elektronischen Rechnung? Wird ein SharePoint-Server benötigt beim Einbetten von PDF-Dateien in die XML-Datei?

Die an die elektronische Rechnung angehängten Dateien werden als eingebettete Binärdaten in einem XML-Element behandelt. Ein SharePoint-Server wird nicht zum Einbetten von PDF-Dateien benötigt, der Anhang muss jedoch im Dokumentenverwaltungssystem von Finance, Supply Chain Management und Project Operations gespeichert werden.

## <a name="is-electronic-invoicing-available-according-to-the-regulations-of-my-countryregion"></a>Ist die elektronische Rechnungsstellung gemäß den Bestimmungen meines Landes/meiner Region verfügbar?

Die elektronische Rechnungsstellung ist eine Microservice-Plattform, die weltweit verfügbar sein wird.

Microsoft plant, die elektronischen Rechnungsformate und -integrationen für die von Microsoft funktional lokalisierten Länder zu veröffentlichen. Weitere Informationen finden Sie unter [Verfügbarkeit von Funktionen für die elektronische Rechnungsstellung](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Wenn das elektronische Rechnungsstellungsformat für Ihr Land/Ihre Region nicht aufgeführt ist, soll die Plattform dieses Szenario in Zukunft unterstützen. Sie können weiterhin von den Konfigurationsfunktionen der elektronischen Rechnungsstellung profitieren und das elektronische Rechnungsstellungsformat selbst konfigurieren, oder Sie können mit einem Partner/ISV zusammenarbeiten, um diese für Ihre Organisation zu konfigurieren.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Ist Dynamics 365 for Regulatory Services ein neues Modul wie Human Resources oder Project Operations, das mit Finance oder Supply Chain Management verbunden ist? Gibt es dafür zusätzliche Kosten?

Der Dynamics 365 for Regulatory Services (RCS) ist ein Clouddienst zum Konfigurieren von Globalisierungsressourcen. RCS ist für alle Lizenzinhaber aus den Bereichen Finance, Supply Chain Management und Project Operations kostenlos.

Für die RCS-Anmeldung gehen Sie zu <https://marketing.configure.global.dynamics.com/>.

Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing--or-just-turn-it-on-in-feature-management"></a>Muss ich mich anmelden, um die elektronische Rechnungsstellung zu erhalten, oder muss ich sie nur in der Funktionsverwaltung aktivieren?

Wenn Sie über eine Lizenz für Finance, Supply Chain Management und Project Operations verfügen, lesen Sie [Erste Schritte mit der Dienstverwaltung des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md), um sich für die elektronische Rechnungsstellung anzumelden.

## <a name="does-electronic-invoicing-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Funktioniert die elektronische Rechnungsstellung mit virtuellen Maschinen der Ebene 1? Was ist die minimal erforderliche Umgebung?

Für die Integration in die elektronische Rechnungsstellung ist mindestens eine virtuelle Maschine der Ebene 2 erforderlich, um Finance oder Supply Chain Management zu hosten. Weitere Informationen zur Umgebungsplanung finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-have-a-test-mode-for-testing-invoice-submission"></a>Verfügt die elektronische Rechnungsstellung über einen Testmodus zum Testen der Rechnungsübermittlung?

Dies kann durch Konfiguration erreicht werden. Um die Rechnungsübermittlung zu testen, können Sie über eine UAT-Umgebung (Benutzerakzeptanztest) eine Verbindung zu Finance oder Supply Chain Management herstellen und die Testrechnungen übermitteln. Die elektronische Rechnungsstellung unterstützt die Konfiguration digitaler Testzertifikate und bei E-Rechnungen, für die eine digitale Genehmigung erforderlich ist, die Einrichtung einer URL aus Testwebdiensten, die von den Steuerbehörden veröffentlicht wurden.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Gibt es eine Dokumentation zu den vorgefertigten länderspezifischen Funktionen für die elektronische Rechnungsstellung?

Ja. Informationen zur Verfügbarkeit der Funktionen für die elektronische Rechnungsstellung und den von ihnen unterstützten Formaten finden Sie unter [Verfügbarkeit von Funktionen für die elektronische Rechnungsstellung](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Wenn Sie die gesuchte Antwort nicht gefunden haben, senden Sie Ihre Frage per E-Mail an das Produktentwicklungsteam unter <D365EInvoicePreview@microsoft.com>. Wir werden uns entweder mit Ihnen in Verbindung setzen oder die Abdeckung dieser FAQ verbessern.
