---
title: Vorschau auf Dynamics 365 Commerce 10.0.30 (November 2022)
description: Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Microsoft Dynamics 365 Commerce 10.0.30 sind.
author: josaw1
ms.date: 08/31/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 0149c9671e8baeb26965b4f136ed91d09e2d039b
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405565"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Vorschau auf Dynamics 365 Commerce 10.0.30 (November 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Commerce Vorschauversion 10.0.30 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1362 und ist im folgenden Zeitplan verfügbar:

- **Vorschauversion:** September 2022
- **Allgemeine Verfügbarkeit des Release (manuelles Update):** Oktober 2022
- **Allgemeine Verfügbarkeit von Release (automatisches Update):** November 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Artikels, um Funktionen einzubeziehen, die zum Build hinzugefügt wurden, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---------|------------------|----------------|--------------| 
| Kundensupport   | Chatten Sie auf einer E-Commerce-Website mit einem Power Virtual Agents Bot. | Diese Funktion gibt Benutzern von E-Commerce-Sites die Wahl, einen Power Virtual Agents Chatbot für Supportanfragen. | Vom Administrator/Ersteller für Endbenutzer aktiviert |
| Erkenntnisse  |  Betriebseinblicksereignisse von Verkaufsstellen (POS) auf Ihr Application Insights Konto streamen. | [Auf Protokolle in Application Insights zugreifen](../dev-itpro/retail-component-events-diagnostics-troubleshooting.md#enable-diagnostic-events-in-application-insights)   |  Opt-in für IT-Experten/-Entwickler   |
|  Zahlungen  | PayPal-Bestellunterstützung über den 29-tägigen Autorisierungszeitraum hinaus. | Der maximale Autorisierungszeitraum für PayPal beträgt 29 Tage. Danach müssen eine neue Autorisierung und Auftrags-ID generiert werden. Als Alternative bietet PayPal eine Option an, bei der ein PayPal-Auftrag als allgemeiner Auftrag referenziert werden kann, wodurch mehrere Autorisierungen und Erfassungen mit derselben Auftrags-ID möglich sind, statt dess nach 29 Tagen eine neue Autorisierung und Auftrags-ID generiert wird). | Bei der Konfiguration des PayPal-Zahlungsconnectors in Commerce headquarters wurde das Feld **OrderIntent** hinzugefügt und kann zwei Werte haben:<p><p>- **Autorisieren**: Diese Konfiguration ist die Standardeinstellung (wenn das Feld leer gelassen wird, dient **Autorisieren** als Standard). Die Konfiguration von **OrderIntent** auf **Autorisieren** entspricht **processing_instruction** Wert von **NO_INSTRUCTION** von PayPal. Die Bestellung wird mit PayPal autorisiert und die Autorisierung kann nicht geändert werden, wenn dieser Wert verwendet wird.<p>- **Speichern**: Wenn der Wert **OrderIntent** auf **Speichern** festgelegt ist, entspricht dies dem PayPal-Wert **processing_instruction** von **ORDER_SAVED_EXPLICITLY**. Bei Verwendung dieses Wertes werden Auftragsreferenzen im PayPal-Dienst gespeichert.  |
| POS-Anmeldung  | [Self-Service-Diagnosefunktionen für die POS-Anmeldung aktivieren](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Diese Funktion bietet Self-Service-Diagnosefunktionen in der Verkaufsstelle (POS) und in Commerce headquarters, um Filialmitarbeitern und -leitern dabei zu helfen, die Grundursachen von POS-Anmeldeproblemen schnell zu identifizieren und zu beheben.<p><p>- Die auf dem POS-Anmeldebildschirm angezeigten Fehlermeldungen wurden verbessert, um konkrete Informationen zur Grundursache zu liefern, die den Filialmitarbeitern, die den POS verwenden, helfen können, zu verstehen, wo das Problem liegt, damit sie die erforderlichen Gegenmaßnahmen ergreifen können.<p>- Eine Funktion **Anmeldung testen** steht in Commerce headquarters auf der Seite **Arbeitskräfte** zur Verfügung, damit Filialleiter, die POS-Geräte einrichten, die POS-Anmeldung simulieren können. Im Falle eines Anmeldefehlers bietet diese Funktion umsetzbare Anleitungen zur Problembehandlung, damit Filiarlleiter relevante Konfigurationen überprüfen, Probleme beheben und die Korrekturen validieren können.  | Standardmäßig aktiviert |


## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Dynamics 365 Finance 10.0.30 enthält Plattformaktualisierungen. Weitere Informationen finden Sie unter [Plattform-Updates für Version 10.0.30 der Finanz- und Betriebs-Apps](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates der Version 10.0.30 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468) an. 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2022wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-features"></a>Entfernte und veraltete Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beschreibt Funktionen, die für Commerce entfernt oder veraltet sind.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
