---
title: Vorschau auf Dynamics 365 Commerce 10.0.31 (Februar 2023)
description: Dieser Artikel beschreibt Funktionen, die entweder neu oder geändert in Microsoft Dynamics 365 Commerce 10.0.31 sind.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: ed4325095163415d05a56128cb1f0334440fe0e5
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787525"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>Vorschau auf Dynamics 365 Commerce 10.0.31 (Februar 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Commerce Vorschauversion 10.0.31 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1406 und ist im folgenden Zeitplan verfügbar:

- **Vorschau auf Release:** Oktober 2022
- **Allgemeine Verfügbarkeit des Releases (Selbst-Update):** Januar 2023
- **Allgemeine Verfügbarkeit des Releases (Auto-Update):** Februar 2023

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir dieses Artikels, um Funktionen einzubeziehen, die zum Build hinzugefügt wurden, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---|---|---|---|
| Fehlercodes | Commerce hat standardisierte Fehlerreferenzen eingeführt, die in den Fehlermeldungen des Online-Kanals enthalten sind, die den Online-Käufern angezeigt werden.| [Fehlercodes des Checkout-Moduls](../checkout-module-error-codes.md)  | Standardmäßig aktiviert |
| Zahlungen | [Apple Pay mit Dynamics 365 Payment Connector for Adyen aktivieren](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | E-Commerce-Kunden können Apple Pay auf Einkaufswagen- und Kassenseiten nutzen, wenn sie unterstützte Geräte oder Browser verwenden. | Opt-in für Entwickler |
| Zahlungen  |  Commerce hat die Funktionalität hinzugefügt, die Interaktion der Benutzer mit wiederkehrenden Zahlungstoken in der gesamten Benutzeroberfläche Commerce headquarters einzuschränken. Formulare für Zahlungen, wie z.B. die Seite **Call-Center Verkaufsauftrag**, zeigen nicht mehr den zuvor verwendeten Zahlungstoken eines Kunden zur Verwendung in einer neuen Transaktion an. Den Benutzern des Call-Centers oder Commerce headquarters wird bei der Verarbeitung einer Zahlung für eine neue Transaktion nur noch eine bestimmte „Karte in der Datei“ angezeigt, die in den Bildschirm **Kundenzahlungen** von Commerce eingegeben wurde oder mit der ein Kunde bei der Zahlung über einen Verkaufsauftrag einverstanden war. | [Verwendung von Zahlungstoken einschränken](../dev-itpro/limit-token-usage.md)  |  Funktionsverwaltung<p>*Verwendung des Zahlungstoken auf Kontext „Auftrag“ beschränken*  |
| POS | [Erstellen von Bestellungen am POS](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  Der eingehende Bestand-Vorgang in der Point of Sale (POS) App wurde verbessert, um Benutzern das Erstellen, Bearbeiten und Bestätigen von Kaufaufträgen zu erlauben. |  Funktionsverwaltung<p>*Möglichkeit zum Erstellen von Bestellanforderungen am POS*   |
| Zusätzliche Sprachen verfügbar | Es sind vier zusätzliche Sprachen verfügbar | Dem Benutzer stehen in der Liste der bevorzugten Sprachen vier neue Sprachen zur Auswahl: Koreanisch, Portugiesisch (Portugal), Vietnamesisch und Chinesisch (traditionell). Um diese Option auszuwählen, gehen Sie auf **Benutzeroptionen \> Einstellungen \> Einstellung von Sprache und Land/Region**. | Lokalisierte Einstellungen |  



## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattformupdates für Apps für Finanzen und Betrieb

Microsoft Dynamics 365 Commerce 10.0.31 enthält Plattform-Updates. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.31 der Finanz- und Betriebs-Apps (Februar 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>Fehlerkorrekturen

Informationen zu den Fehlerkorrekturen, die in den einzelnen Updates der Version 10.0.31 enthalten sind, erhalten Sie, wenn Sie sich bei den Microsoft Dynamics Lifecycle Services anmelden und den [KB-Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525) lesen.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-2-Plan](/dynamics365-release-plan/2022wave2/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-commerce-features"></a>Entfernte und außer Betrieb genommene Commerce Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beschreibt Funktionen, die für Commerce entfernt oder veraltet sind.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 Monate vor dem Entfernen angezeigt.


Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
