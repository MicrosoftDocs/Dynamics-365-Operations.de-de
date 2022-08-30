---
title: Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.26 (Mai 2022)
description: Dieser Artikel beschreibt Funktionen, die in Microsoft Dynamics 365 Supply Chain Management 10.0.26 neu oder geändert wurden.
author: kamaybac
ms.date: 03/01/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: dd98b22a2dfcd8cad62bdef2d31ac2880b3422f8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334714"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-10026-may-2022"></a>Neuerungen oder Änderungen in Dynamics 365 Supply Chain Management 10.0.26 (Mai 2022)

[!include [banner](../includes/banner.md)]

In diesem Artikel werden die Funktionen aufgeführt, die in Microsoft Dynamics 365 Supply Chain Management Version 10.0.26 entweder neu oder geändert sind. Diese Version hat die Build-Nummer 10.0.1192 und ist wie folgt verfügbar:

- **Vorschau auf die Veröffentlichung:** März 2022
- **Allgemeine Verfügbarkeit der Version (Selbst-Update):** April 2022
- **Allgemeine Verfügbarkeit des Releases (Auto-Update):** Mai 2022

## <a name="features-included-in-this-release"></a>In dieser Version enthaltene Funktionen

Die folgende Tabelle listet die Funktionen auf, die in dieser Version enthalten sind. Möglicherweise aktualisieren wir diesen Artikel, um Funktionen einzubeziehen, die es in den Build geschafft haben, nachdem dieser Artikel ursprünglich veröffentlicht wurde.

| Funktionsbereich | Funktion | Mehr erfahren | Aktiviert von |
|---|---|---|---|
| Bestand und Logistik | [Inventory Visibility Abfrage des Lagerbestands zur Unterstützung von Elementen der erweiterten Lagerortverwaltung](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/inventory-visibility-support-advanced-warehouse-management) | [Inventory Visibility-Unterstützung für WMS-Artikel](../inventory/inventory-visibility-whs-support.md) | Funktionsverwaltung:<br>*Lagerortartikel in Bestandsanzeige aktivieren* |
| Bestand und Logistik | [Für das Bestandssichtbarkeits-Add-In verfügbar](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/available-to-promise-inventory-visibility-add-in) | [Inventory Visibility - Lagerbestände ändern und zusagen](../inventory/inventory-visibility-available-to-promise.md) | Aktiviert durch Servicekonfiguration |
| Fertigung | [Elemente mit Artikelgewicht für die Produktionsausführungsoberfläche](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/catch-weight-items-production-floor-execution-interface) | [Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte](../production-control/production-floor-execution-use.md) | Funktionsverwaltung:<br>*Bericht über Artikel mit Artikelgewicht über die Produktionsausführungsoberfläche* |
| Fertigung | Registerkarte Meine Einzelvorgänge auf der Produktionsausführungsoberfläche <!-- KFM: Add link to release plan when available --> | [Verwendung der Produktionsausführungsoberfläche durch Arbeitskräfte](../production-control/production-floor-execution-use.md) | Funktionsverwaltung:<br>*Registerkarte Meine Einzelvorgänge auf der Produktionsausführungsoberfläche* |

## <a name="feature-enhancements-included-in-this-release"></a>Funktionsverbesserungen In dieser Version enthalten

Die folgende Tabelle listet die Funktionsverbesserungen auf, die in dieser Version enthalten sind. Jede dieser Funktionen bietet Verbesserungen einer vorhandenen Funktion. Da es sich nur um Verbesserungen handelt, sind sie nicht in der Liste [Releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features) aufgeführt. Um jedoch sicherzustellen, dass diese Verbesserungen nicht mit Ihren vorhandenen Anpassungen oder Einstellungen in Konflikt stehen, ist jede standardmäßig deaktiviert (sofern nicht anders angegeben).

Wenn Sie eine dieser Funktionen ein‑ oder ausschalten möchten, müssen Sie dies in der [Funktionsverwaltung](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tun.

| Modul | Funktion Name in FunktionVerwaltung | Mehr erfahren |
|---|---|---|
| Beschaffung | Registrierte Mengen von gelagerten Produkten und Restmengen von nicht gelagerten Produkten für Eingänge und Kreditorenrechnungen buchen | Diese Funktion ändert die Art und Weise, wie Mengen von nicht vorrätigen Produkten (wie z.B. Dienstleistungen) bei der Verarbeitung von Einkaufsrechnungen und eingehenden Lieferungen gegen Bestellungen gebucht werden. Die Funktion ändert das Verhalten der Mengenoption *Registrierte Menge und Services* für das Buchen von Quittungen und Lieferantenrechnungen, indem sie es an das Verhalten der Option *Registrierte Menge und nicht gelagerte Produkte* anpasst, die bereits beim Buchen von Mengen für Verkaufslieferscheine zur Verfügung steht.<br><br>Wenn Sie einen Produktzugang oder eine Lieferantenrechnung mit der Mengenoption *Registrierte Menge und Services* buchen, bucht das System die registrierte Menge der gelagerten Produkte und die Restmenge der nicht gelagerten Produkte (einschließlich Services und Nicht-Services). Ohne diese Funktion bucht das System immer noch die registrierte Menge an vorrätigen Produkten (einschließlich Services, die als vorrätige Artikel konfiguriert sind), bucht aber immer die volle bestellte Menge an nicht vorrätigen Serviceprodukten (und ignoriert nicht vorrätige Produkte, die nicht vom Typ *Service* sind). |
| Beschaffung | Rückverfolgungsangaben für Intercompany-Auftrags- und -Bestellzeilen synchronisieren | Mit dieser Funktion können Sie steuern, ob die Dimensionen der Seriennummer und der Batch-Nummern bei Intercompany-Verkaufsaufträgen und Kaufaufträgen synchronisiert werden sollen. Es fügt neue Einstellungen auf den Registerkarten **Richtlinien für Bestellungen** und **Richtlinien für Verkaufsaufträge** der Einrichtungsseite **Intercompany** für Kunden und Lieferanten hinzu. Außerdem werden die Namen einiger verwandter, nahe gelegener Einstellungen aktualisiert, um mehr Klarheit zu schaffen.<br><br>Wenn Sie Lagerverwaltungsprozesse (WMS) verwenden, beachten Sie, dass diese Funktion Batch- und Seriennummern nur dann synchronisiert, wenn diese Dimensionen in der Reservierungshierarchie des Zielortes über dem Ort stehen. |
| Produktinformationsverwaltung | Produktattributwerte bereinigen | Diese Funktion fügt eine periodische Aufgabe namens **Produktattributwerte bereinigen** hinzu, die Datensätze von Produktattributwerten bereinigt, die nicht mehr mit einem Produkt über eine Produktkategorie verbunden sind. |
| Lager- und Lagerortverwaltung | (Russland) Verhinderung von Diskrepanzen bei der Ausstellung von GTDs für Bestellungen, die WMS-aktivierte Artikel enthalten | Diese Funktion ist nur für die russische Lokalisierung vorgesehen. Er verhindert Diskrepanzen, die bei der Ausgabe russischer Zollanmeldungsnummern (GTDs) für Importbestellungen auftreten, die Artikel enthalten, die für Lagerverwaltungsprozesse (WMS) aktiviert sind. Der GTD-Ausgabeprozess ändert einige Werte der Bestandsdimensionen in den zugehörigen Bestandstransaktionen für Rechnungen, die in das angepasste Zoll-Journal aufgenommen wurden, was zu Diskrepanzen zwischen den Datensätzen für den Arbeitsauftrag und den Transaktionen für den Kauf führt. Wenn diese Funktion aktiviert ist, erzeugt der GTD-Ausgabeprozess Anpassungsarbeit, die solche Diskrepanzen beseitigt. |
| Lagerortverwaltung | Erweiterter Parser für GS1-Barcodes | Diese Funktion fügt einen verbesserten Parser für GS1 Symboldaten hinzu. Der neue Parser implementiert den Algorithmus der GS1 Allgemeinen Spezifikation zum Parsen von GS1 Symbolen und bietet eine stärkere Datenvalidierung. Weitere Informationen finden Sie unter [GS1-Barcodes scannen](../warehousing/gs1-barcodes.md). |
| Lagerortverwaltung | Warehouse Management-Anwendung – leere GTD | Diese Funktion ist nur für die russische Lokalisierung vorgesehen. Es lässt zu, dass Arbeitskräfte, die die Warehouse Management-Mobile-App verwenden, bei Bedarf russische Zollanmeldungsnummern (GTDs) leer lassen. Wenn die Dimension für die GTD-Verfolgung so festgelegt ist, dass Leerwerte zugelassen werden, akzeptiert das System Leerwerte für GTD für Vorgänge im Bestand, sofern ein Lagerbestand vorhanden ist. |

## <a name="new-and-updated-documentation-resources"></a>Neue und aktualisierte Dokumentationsressourcen

Wir haben die folgenden Hilfeartikel kürzlich hinzugefügt oder erheblich aktualisiert. Diese Artikel stehen nicht unbedingt im Zusammenhang mit den neuen Funktionen, die für diese Version hinzugefügt wurden, wie in den vorherigen Abschnitten aufgeführt. Sie können Ihnen jedoch helfen, mehr aus vorhandenen Funktionen herauszuholen.

| Funktionsbereich | Neue oder aktualisierte Artikel |
|---|---|
| Kostenverwaltung | Zu jedem der folgenden Artikeln wurden aktualisierte Beispiele und Diagramme hinzugefügt:<ul><li>[FIFO mit physischem Wert und Markierung](../cost-management/fifo-physical-value-marking.md)</li><li>[LIFO mit physischem Wert und Markierung](../cost-management/lifo-physical-value-marking.md)</li><li>[LIFO-Datum (LIFO, last in first out, zuletzt eingetroffenen, zuerst versendet) mit physischem Wert und Markierung](../cost-management/lifo-date-physical-value-marking.md)</li><li>[Laufender Durchschnittseinstandspreis](../cost-management/running-average-cost-price.md)</li><li>[Gewichteter Durchschnitt mit physischem Wert und Markierung](../cost-management/weighted-average-physical-value-marking.md)</li></ul> |

## <a name="additional-resources"></a>Zusätzliche Ressourcen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Plattform-Updates für Finanz- und Betriebs-Apps

Microsoft Dynamics 365 Supply Chain Management 10.0.26 enthält das Plattform-Update. Weitere Informationen finden Sie unter [Plattform-Updates für die Version 10.0.26 der Finanz- und Betriebs-Apps (Mai 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-26.md).

### <a name="bug-fixes"></a>Fehlerkorrekturen

Melden Sie sich bei Lifecycle Services (LCS) an, um Informationen zu den Fehlerbehebungen zu erhalten, die in den einzelnen Updates von 10.0.26 enthalten sind und zeigen Sie die [KB Artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) an.

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan

Sie möchten Informationen über zukünftige und vor Kurzem veröffentlichte Funktionen unserer Unternehmens-Apps oder -Plattformen erhalten?

Informieren Sie sich über den [Dynamics 365 und industrielle Clouds: 2022 Veröffentlichungszyklus-1-Plan](/dynamics365-release-plan/2022wave1/). Hier finden Sie zentral und übersichtlich in einem Dokument alle Informationen, die Sie für Ihre Planung benötigen.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Entfernte und veraltete Supply Chain Management-Funktionen

Der Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beschreibt Funktionen, die für das Supply Chain Management entfernt oder veraltet waren oder werden sollen.

- Eine Funktion *entfernt* ist nicht mehr im Produkt verfügbar.
- Eine Funktion *veraltet* wird nicht aktiv entwickelt und könnte bei einem zukünftigen Update entfernt werden.

Bevor eine Funktion aus dem Produkt entfernt wird, wird der Verfallshinweis im Artikel [Entfernte oder veraltete Funktionen in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 Monate vor dem Entfernen angezeigt.

Bei Änderungen, die sich nur auf die Kompilierungszeit auswirken, aber binär mit Sandbox- und Produktionsumgebungen kompatibel sind, beträgt die Entfernungszeit weniger als 12 Monate. In der Regel handelt es sich hierbei um Funktionsaktualisierungen, die am Compiler vorgenommen werden müssen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

