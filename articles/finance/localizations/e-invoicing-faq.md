---
title: Häufig gestellt Fragen zur elektronischen Rechnungsstellung
description: Dieser Artikel enthält Informationen zu häufig gestellten Fragen zur elektronischen Rechnungsstellung.
author: gionoder
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: fbb43438a9da567460eb744afb64dae5274f04a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904353"
---
# <a name="electronic-invoicing-faq"></a>Häufig gestellte Fragen zur elektronischen Rechnungsstellung

[!include [banner](../includes/banner.md)]

In diesem Artikel finden Sie Antworten auf häufig gestellte Fragen zum Dienst für die elektronische Rechnungsstellung. Die elektronische Rechnungsstellung erweitert die Funktionen der elektronischen Rechnungsstellung, die in Dynamics 365 Finance, Dynamics 365 Supply Chain Management und Dynamics 365 Project Operations vorhanden sind. 

## <a name="what-is-important-about-electronic-invoicing-and-why-should-it-matter-to-my-organization"></a>Was ist an der elektronischen Rechnungsstellung wichtig und warum sollte es für mein Unternehmen von Bedeutung sein?

Die betriebliche Komplexität und das Risiko nehmen weiter zu, da Unternehmen global wachsen und ihre Präsenz in verschiedenen Regionen ausbauen. Die Einhaltung der Vorschriften und die Anpassung an sich häufig ändernde Vorschriften stellen eine wachsende Herausforderung dar und sind für die Rechnungsstellung von besonderer Bedeutung. Die Rechnungsstellung war traditionell teuer und fehleranfällig, da Unternehmen auf Papierdokumente und manuell intensive Prozesse angewiesen sind.  

Unternehmen haben begonnen, sich von Papierrechnungen zu entfernen, um Kosten zu senken und den End-to-End-Prozess zu beschleunigen. Die Regierungen wenden sich zunehmend der elektronischen Rechnungsstellung als Schlüsselkomponente der Steuerdigitalisierung zu. Durch die Verpflichtung von Organisationen, Steuerinformationen in Echtzeit digital an Steuerbehörden zu übermitteln, können Regierungen Steuerhinterziehung und -manipulation minimieren und Betrug reduzieren. 

Die Welt verlagert sich auf die papierlose Dokumentenverarbeitung. Ohne die Implementierung einer elektronischen Rechnungsstellung können Kunden Compliance-Probleme, unnötige Kosten und einen Rückstand gegenüber Wettbewerbern riskieren. 

## <a name="doesnt-finance-supply-chain-management-and-project-operations-already-include-electronic-invoicing-functionality-what-value-does-this-provide-to-me-as-a-customer"></a>Enthalten Finance, Supply Chain Management und Project Operations nicht bereits Funktionen für die elektronische Rechnungsstellung? Welchen Wert bietet mir das als Kunde? 

Elektronische Rechnungsstellung erweitert die Funktionalitäten der elektronischen Rechnungsstellung, die in Finance, Supply Chain Management und Project Operations vorhanden sind. Die Funktionalität vereinfacht auch die Einhaltung der neuesten Standards für die elektronische Rechnungsstellung und bietet kohärente Erfahrungen für verschiedene Regionen bei der Verarbeitung und dem Austausch elektronischer Rechnungen. Die Funktionen der elektronischen Rechnungsstellung bieten eine Reihe von Vorteilen, darunter: 

   - Schnellere und einfachere Übernahme landes-/regionsspezifischer Anforderungen.
   - Standardisierung der Implementierung von E-Invoicing-Lösungen. 
   - Verbesserte Rückverfolgbarkeit der Verarbeitung elektronischer Rechnungen.  
   - Einfachere Wartung zur Anpassung an sich ändernde gesetzliche Anforderungen und lokale Geschäftspraktiken. 
   - Vereinfachte Lösungsverpackung.
   - Skalierungsfunktionen für eine große Menge übermittelter Dokumente, die zu einer schnelleren Abwicklung führen.
   - Möglichkeit, Ihre Lösungen mit anderen Unternehmen zu teilen.

## <a name="does-electronic-invoicing-service-support-the-on-premises-installations-of-finance-supply-chain-management-and-project-operations"></a>Unterstützt der Dienst für die elektronische Rechnungsstellung die lokalen Installationen von Finance, Supply Chain Management und Project Operations? 

Die aktuelle Plattform erlaubt die Verwendung der lokalen Version nicht und es gibt keine Pläne, sie in Zukunft zu unterstützen.

## <a name="does-electronic-invoicing-service-interface-with-the-vendor-import-automation-feature"></a>Verfügt der Dienst für die elektronische Rechnungsstellung über eine Schnittstelle mit der Funktion zur Automatisierung des Kreditor-Imports?

Nein. Es gibt Pläne für diese Schnittstelle, aber es gibt keine geplante Zeitskala. Wenn geplant, werden die Termine in [Release-Pläne](/dynamics365/release-plans/) bekannt gegeben.

## <a name="how-does-electronic-invoicing-service-handle-file-attachments-into-the-electronic-invoice-is-a-sharepoint-server-needed-when-embedding-pdf-files-into-the-xml-file"></a>Wie behandelt der Dienst für die elektronische Rechnungsstellung Dateianhänge in der elektronischen Rechnung? Wird ein SharePoint-Server benötigt beim Einbetten von PDF-Dateien in die XML-Datei?

Die an die elektronische Rechnung angehängten Dateien werden als eingebettete Binärdaten in einem XML-Element behandelt. Ein SharePoint-Server wird nicht zum Einbetten von PDF-Dateien benötigt, der Anhang muss jedoch im Dokumentenverwaltungssystem von Finance, Supply Chain Management und Project Operations gespeichert werden.

## <a name="is-electronic-invoicing-service-available-according-to-the-regulations-of-my-countryregion"></a>Ist der Dienst für die elektronische Rechnungsstellung gemäß den Vorschriften meines Landes/ meiner Region verfügbar?

Der Dienst für die elektronische Rechnungsstellung ist eine Microservice-Plattform, die weltweit verfügbar sein wird.

Microsoft plant, die elektronischen Rechnungsformate und -integrationen für die von Microsoft funktional lokalisierten Länder zu veröffentlichen. Weitere Informationen finden Sie unter [Verfügbarkeit von Funktionen für die elektronische Rechnungsstellung](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

Wenn das elektronische Rechnungsstellungsformat für Ihr Land/Ihre Region nicht aufgeführt ist, soll die Plattform dieses Szenario in Zukunft unterstützen. Sie können weiterhin von den Konfigurationsfunktionen der elektronischen Rechnungsstellung profitieren und das elektronische Rechnungsstellungsformat selbst konfigurieren, oder Sie können mit einem Partner/ISV zusammenarbeiten, um diese für Ihre Organisation zu konfigurieren.

## <a name="is-dynamics-365-for-regulatory-services-a-new-module-like-human-resources-or-project-operations-that-is-linked-to-finance-or-supply-chain-management-are-there-extra-costs-for-that"></a>Ist Dynamics 365 for Regulatory Services ein neues Modul wie Human Resources oder Project Operations, das mit Finance oder Supply Chain Management verbunden ist? Gibt es dafür zusätzliche Kosten?

Der Dynamics 365 for Regulatory Services (RCS) ist ein Clouddienst zum Konfigurieren von Globalisierungsressourcen. RCS ist für alle Lizenzinhaber aus den Bereichen Finance, Supply Chain Management und Project Operations kostenlos.

Für die RCS-Anmeldung gehen Sie zu <https://marketing.configure.global.dynamics.com/>.

Weitere Informationen finden Sie unter [Regulatory Configuration Services (RCS) – Globalisierungsfunktionen](rcs-globalization-feature.md).

## <a name="do-i-need-to-sign-up-to-get-electronic-invoicing-service-or-just-turn-it-on-in-feature-management"></a>Muss ich mich anmelden, um den Dienst für die elektronische Rechnungsstellung zu erhalten, oder kann ich ihn einfach in der Funktionsverwaltung einschalten?

Wenn Sie über eine Lizenz für Finance, Supply Chain Management und Project Operations verfügen, lesen Sie [Erste Schritte mit der Dienstverwaltung des Add-Ons für die elektronische Rechnungsstellung](e-invoicing-get-started-service-administration.md), um sich für die elektronische Rechnungsstellung anzumelden.

## <a name="does-electronic-invoicing-service-work-with-tier-1-virtual-machines-what-is-the-minimal-required-environment"></a>Arbeitet der Dienst für die elektronische Rechnungsstellung mit virtuellen Tier-1-Maschinen? Was ist die minimal erforderliche Umgebung?

Die Integration mit dem Dienst für die elektronische Rechnungsstellung erfordert mindestens eine virtuelle Maschine der Stufe 2, um Finance oder Supply Chain Management zu hosten. Weitere Informationen zur Umgebungsplanung finden Sie unter [Umgebungsplanung](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).

## <a name="does-electronic-invoicing-service-have-a-test-mode-for-testing-invoice-submission"></a>Verfügt der Dienst für die elektronische Rechnungsstellung über einen Testmodus zum Testen der Rechnungsübermittlung?

Dies kann durch Konfiguration erreicht werden. Um die Rechnungsübermittlung zu testen, können Sie über eine UAT-Umgebung (Benutzerakzeptanztest) eine Verbindung zu Finance oder Supply Chain Management herstellen und die Testrechnungen übermitteln. Die elektronische Rechnungsstellung unterstützt die Konfiguration digitaler Testzertifikate und bei E-Rechnungen, für die eine digitale Genehmigung erforderlich ist, die Einrichtung einer URL aus Testwebdiensten, die von den Steuerbehörden veröffentlicht wurden.

## <a name="is-there-any-documentation-about-the-out-of-box-country-specific-electronic-invoicing-features"></a>Gibt es eine Dokumentation zu den standardmäßigen länderspezifischen Funktionen der Elektronischen Rechnungsstellung?

Ja. Informationen über die Verfügbarkeit der Funktionen für die Elektronische Rechnungsstellung und die unterstützten Formate finden Sie unter [Verfügbarkeit der Funktionen für die Elektronische Rechnungsstellung](e-invoicing-configuration-rcs.md#availability-of-electronic-invoicing-features).

## <a name="does-the-electronic-invoicing-service-allow-a-legal-entity-in-finance-or-supply-chain-management-that-is-configured-for-a-specific-country-to-consume-electronic-invoicing-features-from-different-countryregions"></a>Lässt der Dienst für die elektronische Rechnungsstellung zu, dass eine juristische Entität in Finance oder Supply Chain Management, die für ein bestimmtes Land konfiguriert ist, Funktionen für die elektronische Rechnungsstellung aus anderen Ländern/Regionen nutzen kann?

Ja. Die Funktionen der Elektronischen Rechnungsstellung können genutzt werden, um Geschäftsdokumente unabhängig vom Land der juristischen Entität zu verarbeiten, wenn Folgendes zutrifft:

   - Das erzeugte Geschäftsdokument verwendet die entsprechende Zuordnung des Dokumentenmodells.
   - Es gibt eine Übereinstimmung zwischen dem Geschäftsdokument und den Anwendbarkeitsregeln, die in der Funktion für die elektronische Rechnungsstellung konfiguriert sind.

## <a name="does-the-electronic-invoicing-service-use-the-same-configuration-and-design-experience-provided-by-the-electronic-reporting-module-in-finance-and-supply-chain-management"></a>Verwendet der Dienst für die elektronische Rechnungsstellung die gleichen Konfigurations- und Designmöglichkeiten, die das Modul für das elektronische Reporting in Finance und Supply Chain Management bietet? 

Ja. Die gleichen Designer-Tools, die im Modul „Elektronisches Reporting (ER)“ in Finance und Supply Chain Management verwendet werden, werden zum Erstellen und Konfigurieren der Zuordnung von Datenmodellen und Dateiformaten verwendet. Diese Designer Tools werden auch in Regulatory Configuration Services (RCS) verwendet, um Zuordnungen von Datenmodellen und Dateiformaten zu erstellen und zu konfigurieren, die bei der Konfiguration der Funktionen für die elektronische Rechnungsstellung verwendet werden.

## <a name="can-the-applicability-rules-be-extended-and-configured-so-that-they-arent-tied-to-any-specific-parameter-such-as-a-legal-entity"></a>Können die Anwendbarkeitsregeln so erweitert und konfiguriert werden, dass sie nicht an einen bestimmten Parameter gebunden sind, z.B. an eine juristische Entität?

Ja. Die Anwendbarkeitsregeln sind vollständig konfigurierbar. Sie können Klauseln und logische Vorgänge hinzufügen oder entfernen sowie Klauseln gruppieren und ihre Gruppierung aufheben. Weitere Informationen finden Sie unter [Anwendbarkeitsregeln](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#applicability-rules).

## <a name="does-the-electronic-invoicing-service-support-adding-other-er-format-configurations-to-generate-other-types-of-documents-does-it-support-sending-the-documents-electronically-to-customers-such-as-a-delivery-note"></a>Unterstützt der Dienst für die elektronische Rechnungsstellung das Hinzufügen anderer ER-Format-Konfigurationen, um andere Arten von Dokumenten zu erzeugen? Unterstützt er den elektronischen Versand der Dokumente an den Debitor, z.B. eines Lieferscheins?

Sie können andere ER-Format-Konfigurationen verwenden, um die gewünschten Ausgabedateien zu erzeugen. Die ER-Format-Konfiguration muss jedoch von derselben ER-Rechnungsmodell-Zuordnung abgeleitet werden, die in Finance oder Supply Chain Management konfiguriert ist, um Geschäftsdokumente zu erzeugen. Das Senden der Ausgabedatei direkt an den Debitor als EDI-Transaktion wird von der Elektronischen Rechnungsstellung nicht out-of-the-box unterstützt.

## <a name="does-the-electronic-invoicing-service-support-exchanging-electronic-invoices-with-customers-does-it-support-configuring-different-invoice-formats-for-the-same-invoice"></a>Unterstützt der Dienst für die elektronische Rechnungsstellung den Austausch von elektronischen Rechnungen mit Debitor? Unterstützt er die Konfiguration verschiedener Rechnungsformate für dieselbe Rechnung?

Die Funktionalität, elektronische Rechnungen von Kreditor zu empfangen und zu importieren, ist auf der Roadmap, aber der automatische Versand der elektronischen Rechnungen an den Debitor wird derzeit nicht unterstützt.

## <a name="does-the-electronic-invoicing-service-extend-to-support-exchanging-edi-messages-with-other-companies"></a>Unterstützt der Dienst für die elektronische Rechnungsstellung auch den Austausch von EDI-Nachrichten mit anderen Firmen?

Der Schwerpunkt des Dienstes für die elektronische Rechnungsstellung liegt auf dem Austausch von elektronischen Rechnungsnachrichten, die durch die Einhaltung gesetzlicher Vorschriften bedingt sind. Das Empfangen und Importieren von elektronischen Rechnungen von Kreditor ist auf der Roadmap, aber das Senden von elektronischen Rechnungsdateien an die Debitor ist derzeit nicht out-of-the-box unterstützt, außer in Szenarien, in denen das Senden der elektronischen Rechnung an den Debitor eine gesetzliche Vorschrift ist.

## <a name="does-the-electronic-invoicing-service-support-importing-or-merging-customizations-made-in-the-er-format-configurations-from-the-legacy-electronic-invoicing-feature"></a>Unterstützt der Dienst für die elektronische Rechnungsstellung das Importieren oder Zusammenführen von angepassten ER-Format-Konfigurationen aus der veralteten Funktion für die elektronische Rechnungsstellung?

Sie können Konfigurationen des ER-Formats im Dienst für die elektronische Rechnungsstellung wiederverwenden. Die ER-Format-Konfiguration muss jedoch von derselben ER-Rechnungsmodell-Zuordnung abgeleitet werden, für die die Funktion „Elektronische Rechnungsstellung“ entwickelt wurde und die in Finance oder Supply Chain Management konfiguriert ist, um die Geschäftsdokumente zu generieren.

## <a name="does-the-electronic-invoicing-service-support-issuing-electronic-invoices-from-custom-made-tables-if-so-how-do-you-create-the-er-data-model-configurations-for-these-new-tables-and-entities"></a>Unterstützt der Dienst für die elektronische Rechnungsstellung das Ausstellen von elektronischen Rechnungen aus angepassten Tabellen? Wenn ja, wie erstellen Sie die ER-Datenmodell-Konfigurationen für diese neuen Tabellen und Entitäten?

Ja. Es erfordert jedoch eine Anpassung der Zuordnung des Rechnungsmodells und das Hinzufügen der notwendigen Referenzen zu den benutzerdefinierten Tabellen, oder je nach Komplexität das Erstellen einer neuen Zuordnung des Rechnungsmodells.

## <a name="does-the-electronic-invoicing-service-support-different-web-service-endpoints"></a>Unterstützt der Dienst für die elektronische Rechnungsstellung verschiedene Web-Service-Endpunkte?

Der Dienst für die elektronische Rechnungsstellung unterstützt verschiedene Web-Services-Endpunkte. Sie können eine konfigurierbare Integration mit REST-Webservices oder eine Reihe von parametrisierten länderspezifischen Webservice-Integrationen verwenden. Verschiedene Endpunkte können für dieselben Web-Services und APIs mit unterschiedlichen Konfigurationsversionen konfiguriert werden. Weitere Informationen finden Sie unter [Liste der Parameter nach Aktion](e-invoicing-setup.md#list-of-parameters-by-action).

## <a name="is-electronic-invoicing-integrated-with-the-various-invoice-operators-apis-from-the-nordic-countries-or-should-that-be-handled-on-a-case-by-case-basis"></a>Ist die Elektronische Rechnungsstellung mit den APIs der verschiedenen Rechnungssteller aus den nordischen Ländern integriert, oder soll das von Fall zu Fall gehandhabt werden?

Microsoft erweitert kontinuierlich den Funktionsumfang, um Out-of-the-Box-Integrationen mit den Funktionen zur Elektronischen Rechnungsstellung zu ermöglichen. Weitere Informationen zu den unterstützten Formaten und Integrationen finden Sie unter [Verfügbarkeit von Funktionen für die Elektronische Rechnungsstellung](e-invoicing-configuration-rcs.md?toc=/dynamics365/finance/toc.json#availability-of-electronic-invoicing-features).

> [!NOTE] 
> Wenn Sie die gesuchte Antwort nicht gefunden haben, senden Sie Ihre Frage per E-Mail an das Produktentwicklungsteam unter <D365EInvoicePreview@microsoft.com>. Wir werden uns entweder mit Ihnen in Verbindung setzen oder die Abdeckung dieser FAQ verbessern.
