---
title: Ihren lokalen Kontenplan planen
description: Dieses Thema enthält Informationen, die Ihnen bei der Planung des Kontenplans helfen, wenn Sie Anforderungen an gesetzliche/örtliche Anforderungen für Ihre Organisation haben.
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e224a2e24b4ba293c953c6c883307038128e2f04
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798295"
---
# <a name="plan-your-local-chart-of-accounts"></a>Ihren lokalen Kontenplan planen

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen, die Ihnen bei der Planung des Kontenplans helfen, wenn Ihre Organisation juristische Personen umfasst, die die Anforderungen für bestimmte Standorte erfüllen müssen, an denen sie geschäftlich tätig sind. In diesem Thema werden die folgenden Begriffe verwendet, um Kontenpläne zu beschreiben:

- **Global** – Der Kontenplan, den die Organisation weltweit verwendet. In den meisten Fällen werden Sie auf diesen Kontenplan konsolidieren.
- **Lokal** – Ein Kontenplan, den juristische Personen in einem bestimmten Land oder einer bestimmten Region verwenden.
- **Geteilt** – Ein Kontenplan, den mehr als eine juristische Person verwenden kann. Sowohl der globale Kontenplan als auch der lokale Kontenplan können gemeinsam genutzt werden.

Sie können mehrere Kontenpläne erstellen und freigeben. Ein gemeinsamer Kontenplan kann von mehreren juristischen Personen verwendet werden, jeder juristischen Person kann jedoch nur ein Kontenplan zugeordnet werden. Der Kontenplan, den die juristischen Person verwendet, wird auf der Seite **Sachkonto** definiert.

Viele Organisationen streben bei der Gestaltung des Kontenplans einen globalen Kontenplan an. Die gemeinsame Kontenplanfunktion ermöglicht die Erstellung eines globalen Kontenplans. Die Erstellung und Verwendung eines einzigen Kontenplans hat Vorteile. Beispielsweise sind Governance und Kontrolle, Wartung und Berichterstellung einfacher.

Die meisten Unternehmen bevorzugen einen globalen Kontenplan, der am einfachsten zu implementieren ist. Einige juristische Personen benötigen jedoch aus folgenden Gründen einen lokalen Kontenplan:

- Lokale gesetzliche Anforderungen
- Anforderungen lokaler Rechnungslegungsstandards
- Branchenanforderungen
- Unternehmensspezifische Anforderungen für Berichterstellung und Analyse

Wenn Ihre Organisation erfordert, dass eine juristische Person einen lokalen Kontenplan verwendet, stehen zwei Optionen für die Implementierung zur Verfügung:

- Weisen Sie den globalen Kontenplan zu und definieren Sie andere Möglichkeiten, die lokalen Anforderungen zu erfüllen.
- Weisen Sie der juristischen Person einen lokalen Kontenplan zu und definieren Sie Beziehungen zum globalen Kontenplan.

Die Organisationsstruktur und die Berichtsstruktur bestimmen die genutzte Option.

[![Diagramm, das zeigt, wie die Organisationsstruktur bestimmt, ob ein globaler oder lokaler Kontenplan verwendet wird](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Wenn der juristischen Person der globale Kontenplan zugeordnet ist, stehen folgende Möglichkeiten zur Erfüllung lokaler Berichtspflichten zur Verfügung:

- Lokal konsolidieren.
- Verwenden Sie eine Finanzdimension, um den lokalen Kontenplan zu verfolgen.
- Legen Sie im globalen Kontenplan lokale Hauptkonten an.
- Führen Sie eine externe Zuordnung zum lokalen Kontenplan durch.

Wenn der juristischen Person der lokaler Kontenplan zugeordnet ist, steht derzeit nur die globale Konsolidierung als Möglichkeit zur Erfüllung globaler Berichtspflichten zur Verfügung.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Einer juristischen Person zugeordneter globaler Kontenplan

Wenn Sie den globalen Kontenplan einer juristischen Person zuordnen müssen, stehen Ihnen, wie zuvor beschrieben, vier Möglichkeiten zur Konfiguration des Systems zur Verfügung. Für alle vier Optionen wird ein einzelner Kontenplan konfiguriert und mit jeder juristischen Person auf der Seite **Hauptbuch** verknüpft. Jede Option verwendet dann einen anderen Ansatz, um die Lokalisierungsanforderungen zu erfüllen. In den folgenden Abschnitten werden die allgemeinen Schritte zum Konfigurieren des Systems für die Lokalisierungsanforderungen beschrieben. Sie beschreiben auch die Vor- und Nachteile der einzelnen Optionen.

### <a name="do-local-consolidation"></a>Lokal konsolidieren

Die lokale Konsolidierung ist der empfohlene Ansatz, um lokale Kontenplananforderungen zu erfüllen und die dafür konzipierte Systemfunktionalität zu nutzen.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Konsolidierung für einen lokalen Kontenplan einrichten

1. Erstellen Sie einen einzigen globalen Kontenplan, der alle erforderlichen Hauptkonten enthält.
2. Weisen Sie in jeder juristischen Person den globalen Kontenplan auf der **Hauptbuch**-Seite zu.
3. Erstellen Sie für jede erforderliche Lokalisierung eine juristische Person für die Konsolidierung.
4. Führen Sie einen dieser Schritte aus:

    - Wenn nur eine Lokalisierung erforderlich ist, konfigurieren Sie das Konsolidierungskonto auf der **Hauptkonto**-Seite, oder verwenden Sie die Seiten **Konsolidierungsgruppen** und **Zusätzliche Konsolidierungskonten**.
    - Wenn mehr als eine Lokalisierung erforderlich ist oder sowohl die Kontonummer als auch der Kontoname übersetzt werden müssen, verwenden Sie die Seiten **Konsolidierungsgruppen** und **Zusätzliche Konsolidierungskonten**, um die Lokalisierungsanforderungen darzustellen.

5. Führen Sie den Konsolidierungsprozess aus, um den Wert von der juristischen Quelle der juristischen Person, die den globalen Kontenplan verwendet, in das Konsolidierungsunternehmen umzuwandeln, das den lokalen Kontenplan verwendet.

#### <a name="advantages"></a>Vorteile

- Dieser Ansatz bietet eine einheitliche Arbeitsweise im gesamten Unternehmen.
- Eine Übersetzung der lokalen Position wird durchgeführt.
- Dieser Ansatz unterstützt die Übersetzung sowohl der Hauptkonto-ID als auch des Namens jedes Hauptkontos.
- Es unterstützt mehrere Lokalisierungen.

#### <a name="disadvantages"></a>Nachteile

- Ein zusätzliches Konsolidierungsunternehmen wird angelegt.
- Ein zusätzlicher Konsolidierungsprozess wird abgeschlossen.
- Dieser Ansatz kann erst nach Abschluss des Konsolidierungsprozesses über das lokalisierte Diagramm berichten.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Verwenden Sie eine Finanzdimension, um den lokalen Kontenplan zu verfolgen

Bei diesem Ansatz wird eine Finanzdimension verwendet, bei der die Finanzdimensionswerte die lokalen Hauptkonten darstellen, die für die Lokalisierung erforderlich sind. Es funktioniert gut, wenn nur eine Lokalisierung erforderlich ist. Es wird jedoch weniger nützlich, wenn Sie weitere Lokalisierungen und Finanzdimensionen hinzufügen.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Eine Finanzdimension für einen lokalen Kontenplan einrichten

1. Erstellen Sie einen einzigen globalen Kontenplan, der alle erforderlichen Hauptkonten enthält.
2. Weisen Sie in jeder juristischen Person den globalen Kontenplan auf der **Hauptbuch**-Seite zu.
3. Erstellen Sie eine Finanzdimension, die den lokalen Kontenplan darstellt.
4. Erstellen Sie Finanzdimensionswerte, die die Hauptkonten im lokalen Kontenplan darstellen.
5. Aktualisieren Sie die Kontenstruktur, sodass sie die Finanzdimension „Lokaler Kontenplan“ enthält.
6. Stellen Sie sicher, dass die Finanzdimension „Lokaler Kontenplan“ immer einen Wert hat und keine leeren Werte zulässt. Ziehen Sie in Erwägung, abgeleitete Dimensionen oder feste Dimensionen zu verwenden.
7. Erstellen Sie einen Finanzdimensionssatz, bei dem die Finanzdimension „Lokaler Kontenplan“ die erste ausgewählte Finanzdimension ist. Der Finanzdimensionssatz kann verwendet werden, wenn die Zwischenbilanz generiert wird.

#### <a name="advantages"></a>Vorteile

- Auf Transaktionsebene existieren die Hauptkonten sowohl der globalen als auch der lokalen Kontenpläne. Das Hauptkonto ist global und der Finanzdimensionswert ist lokal.
- Dieser Ansatz bietet Echtzeitberichte und Ansichten sowohl der globalen Finanzposition als auch der lokalen Finanzposition.

#### <a name="disadvantages"></a>Nachteile

- Wenn die **Für das Sammelkonto verwendete Werte**-Feld in den Hauptbuchparametern auf **Buchhaltungsverteilungen** festgelegt ist, werden die Finanzdimensionen, die das Hauptkonto für Aufwand/Anlage/Ertrag darstellen, fälschlicherweise für das Summenkonto Debitoren- und Kreditorenbuchhaltung verwendet. Es wird empfohlen, das Feld stattdessen auf ein Quelldokument festzulegen, um sicherzustellen, dass die richtigen Finanzdimensionswerte verwendet werden.
- Wenn viele lokale Kontenpläne erforderlich sind und für alle eine Finanzdimension verwendet wird, kann die Liste der verwendeten Finanzdimensionswerte lang und schwer zu handhaben sein.
- Wenn viele lokale Kontenpläne erforderlich sind und eine separate Finanzdimension verwendet wird, um jeden einzelnen darzustellen, kann die Benutzerfreundlichkeit und Leistung des Systems beeinträchtigt werden, wenn Finanzdimensionen und Finanzdimensionssätze hinzugefügt werden.
- Es wird empfohlen, die Anzahl der erforderlichen Finanzdimensionen, die Anzahl der Werte in jeder einzelnen und die Anzahl der Finanzdimensionssätze sorgfältig zu berücksichtigen, da all diese Faktoren die Systemleistung beeinträchtigen können.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Im globalen Kontenplan lokale Hauptkonten anlegen

*Was der Lektor fragte:* Bei diesem Ansatz schließen die lokalen Hauptkonten im globalen Kontenplan die Hauptkonten im lokalen Kontenplan in den globalen Kontenplan ein.

*Originalversion:* Die lokalen Hauptkonten innerhalb des globalen CoA-Ansatzes bestehen darin, dass die lokalen CoA-Hauptkonten in den globalen CoA einbezogen werden.

*Soll es das bedeuten:* Bei diesem Ansatz werden die lokalen Hauptkonten des lokalen Kontenplans in den globalen Kontenplan aufgenommen.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Im globalen Kontenplan lokale Hauptkonten einrichten

1. Erstellen Sie einen einzigen Kontenplan, der die Hauptkonten sowohl für den globalen Kontenplan als auch für den lokalen Kontenplan enthält.
2. Weisen Sie in jeder juristischen Person den Kontenplan auf der **Hauptbuch**-Seite zu.
3. Erstellen Sie im Kontenplan Gesamtkonten, um die Hauptkonten zu summieren, die denselben Zweck erfüllen.
4. Erstellen Sie Überschreibungen für juristische Personen für jedes lokale Konto, um Transaktionen von anderen juristischen Personen zu verhindern, für die das lokale Konto nicht konzipiert wurde.
5. Erstellen Sie Überschreibungen für juristische Personen in jedem globalen Konto, um Transaktionen von juristischen Personen der Lokalisierung zu verhindern.

#### <a name="advantages"></a>Vorteile

- Eine Echtzeitansicht sowohl der globalen Finanzposition als auch der lokalen Finanzposition ist in bestimmten Berichten und in bestimmten Ansichten im System, wie beispielsweise einem Bilanzfinanzbericht, verfügbar. Es kann auch über die **Zeitraum**-Schaltfläche auf dem Gesamtkonto darauf zugegriffen werden.
- Sie haben kein zusätzliches Segment im Sachkonto.

#### <a name="disadvantages"></a>Nachteile

- Die Gesamtnutzung des Kontos und die Sichtbarkeit sind begrenzt. Zum Beispiel sind die Gesamtkonten nicht auf der **Zwischenbilanz**-Listenseite sichtbar.
- Die Wartung erfordert zusätzlichen Aufwand.
- Die Erstellung von Finanzberichten erfordert zusätzlichen manuellen Aufwand.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Eine externe Zuordnung zum lokalen Kontenplan durchführen

Die Einführung eines globalen Kontenplans setzt voraus, dass Sie die Zuordnung und Lokalisierungen außerhalb des Systems verwalten. Bei diesem Ansatz erstellen Sie einfach einen einzigen globalen Kontenplan in Microsoft Dynamics 365 Finance und behandeln die Anforderungen außerhalb des Systems.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Eine externe Zuordnung zu einem lokalen Kontenplan einrichten

1. Erstellen Sie einen einzigen globalen Kontenplan, der alle erforderlichen Hauptkonten enthält.
2. Weisen Sie in jeder juristischen Person den globalen Kontenplan auf der **Hauptbuch**-Seite zu.
3. Führen Sie die Zuordnung zum lokalen Kontenplan außerhalb von Finance durch.

#### <a name="advantages"></a>Vorteile

- Dieser Ansatz bietet einheitliche Methoden im gesamten Unternehmen.

#### <a name="disadvantages"></a>Nachteile

- Es ist keine lokale Berichterstellung vom System verfügbar.
- Diese Vorgehensweise ist bei der Erstellung von Finanzberichten fehleranfällig.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Einer juristischen Person zugeordneter lokaler Kontenplan

Wenn Ihre Organisation beschließt, keinen globalen Kontenplan für juristische Personen zu verwenden, wird für jeden eindeutigen lokalen Kontenplan ein separater Kontenplan erstellt. Jede juristische Person wird dann mit dem entsprechenden Kontenplan auf der Seite **Hauptbuch** verknüpft.

### <a name="do-global-consolidation"></a>Global konsolidieren

Bei diesem Ansatz wird ein Konsolidierungsunternehmen verwendet, um die Salden von jedem lokalen Quellunternehmen zusammenzufassen und in den kombinierten globalen Kontenplan in dem Konsolidierungsunternehmen zu kombinieren. Dieser Ansatz erfordert, dass Sie eine Zuordnung jedes lokalen Kontenplans zum globalen Kontenplan in der Konsolidierungsgesellschaft pflegen.

#### <a name="set-up-global-consolidation"></a>Globale Konsolidierung einrichten

1. Erstellen Sie für jede juristische Person mit einem anderen lokalen Kontenplan einen separaten Kontenplan. Wenn juristische Personen denselben lokalen Kontenplan haben, ist nur ein lokaler Kontenplan erforderlich, der gemeinsam genutzt werden kann.
2. Weisen Sie in jeder juristischen Person den geeigneten Kontenplan auf der **Hauptbuch**-Seite zu.
3. Optional: Erstellen Sie einen Kontenplan für den globalen Kontenplan jedes Konsolidierungsunternehmens, das einen anderen globalen Kontenplan hat.
4. Legen Sie für jede erforderliche Konsolidierungsstufe eine juristische Person für die Konsolidierung an und ordnen Sie den entsprechenden Kontenplan auf der **Hauptbuch**-Seite zu.
5. Führen Sie einen dieser Schritte aus:

    - Wenn nur eine Konsolidierung erforderlich ist, konfigurieren Sie das Konsolidierungskonto auf der **Hauptkonto**-Seite.
    - Wenn mehr als eine Konsolidierung erforderlich ist oder sowohl die Kontonummer als auch der Kontoname übersetzt werden müssen, verwenden Sie die Seiten **Konsolidierungsgruppen** und **Zusätzliche Konsolidierungskonten**, um die Anforderungen für den globalen Kontenplan darzustellen.

6. Führen Sie den Konsolidierungsprozess aus, um die Salden von den lokalen juristischen Personen auf die konsolidierte juristische Person zu übertragen. Diese konsolidierte juristische Person verwendet die Konsolidierungskonten, die Sie in Schritt 5 definiert haben.

#### <a name="advantages"></a>Vorteile

- Das Format der lokalen Rechnungslegungsstandards wird nativ angewendet.
- Dieser Ansatz erleichtert dem lokalen Finanzteam die Arbeit.

#### <a name="disadvantages"></a>Nachteile

- Es ist keine Echtzeitansicht der globalen Position verfügbar.
- Der Konsolidierungsprozess kann häufiger ausgeführt werden.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Kontenplan planen](plan-chart-of-accounts.md)
- [Sachkonten konfigurieren](configure-ledger.md)
- [Finanzdimensionen und Veröffentlichungen](Default-dimensions.md#balancing-dimension)
- [Finanzdimensionssätze](financial-dimension-sets.md)
- [Konsolidierungs- und Löschungsüberblick](../budgeting/consolidation-elimination-overview.md)
- [Konsolidierungskontengruppen und zusätzliche Konsolidierungskonten erstellen](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
