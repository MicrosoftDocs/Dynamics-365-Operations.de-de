---
title: Kostenkonfiguration für die verteilte Auftragsverwaltung (DOM)
description: Dieses Thema behandelt die Kostenkonfiguration für die Funktion zur verteilten Auftragsverwaltung (DOM) in Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4459051"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Kostenkonfiguration für die verteilte Auftragsverwaltung (DOM)

[!include [banner](../includes/banner.md)]

Um den optimalen Standort zur Erledigung von Aufträgen zu ermitteln, berücksichtigen Organisationen mehrere Kostenkomponenten. Dazu gehören unter anderem Kosten für Versand, Bearbeitung und Verpackung. Anhand einer berechneten Kombination dieser Kosten wird der Erfüllungslagerplatz bestimmt.

Bei der Verbesserung der Zuweisung von Aufträgen zu Erfüllungslagerplätzen durch die erste Iteration der verteilten Auftragsverwaltung (DOM) in Dynamics 365 Commerce wurde nur die Entfernung als Faktor berücksichtigt. Auch wenn diese ggf. mit Kosten korreliert, ist sie nicht mit Kosten identisch. So kann ein Übernachtversand über dieselbe Entfernung mehr als ein Drei- oder Sieben-Tage-Versand kosten.

Mit der Funktion zur Kostenkonfiguration können Einzelhändler zusätzliche Kostenkomponenten anlegen und konfigurieren, die zur Ermittlung des besten Standortes zur Erfüllung von Auftragspositionen berechnet und berücksichtigt werden.

Sind Kostenkomponenten konfiguriert, verwendet der DOM-Solver bei der Ermittlung des besten Erfüllungslagerplatzes nur diese Kostendefinitionen. Die Entfernungskomponente wird nicht als Kosten berücksichtigt. Sind keine Kostenkomponenten konfiguriert, verwendet der DOM-Solver bei der Ermittlung des besten Erfüllungslagerplatzes die Entfernungskomponente als Kosten.

## <a name="set-up-cost-components"></a>Kostenkomponenten einrichten

In System können zwei maßgebliche Kostenkomponenten festgelegt werden: **Versand** und **Sonstiges**.

Wie in der folgenden Tabelle dargestellt, unterstützen beide Typen von Kostenkomponenten mehrere Berechnungsgrundlagen.

<table>
<thead>
<tr>
<th>Typ der Kostenkomponente</th>
<th>Berechnungsbasis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Versand</td>
<td>
<ul>
<li>Einfach</li>
<li>Mehrstufig</li>
</ul>
</td>
</tr>
<tr>
<td>Sonstiges</td>
<td>
<ul>
<li>Auftrag</li>
<li>Verkaufsposition</li>
<li>Ort</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Kostenkomponententyp „Versand“

In diesem Abschnitt wird beschrieben, wie die einzelnen Kombinationen des Kostenkomponententyps **Versand** und eine Berechnungsgrundlage für Versandkosten eingerichtet werden. Ferner wird erläutert, wie der DOM-Solver die einzelnen Kombinationen verwendet.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Kostenkomponententyp = Versand und Berechnungsgrundlage = Einfach

Wird eine Kombination aus dem Kostenkomponententyp **Versand** und der Berechnungsgrundlage **Einfach** verwendet, beruhen die Versandkosten einer Lieferart entweder auf einer Kostenpauschale oder auf der Entfernung.

Für diese Kombination müssen die folgenden Felder eingerichtet werden:

- **Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.
- **Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.
- **Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken. Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.
- **Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist. Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.
- **Unternehmen**: Geben Sie die juristische Person an, für die Kostenfaktor konfiguriert wird. Alle Positionen der Berechnungskriterien müssen sich auf dieselbe juristische Person beziehen.
- **Lieferarten**: Geben Sie die Lieferarten an, für die die Kosten konfiguriert werden.
- **Berechnungstyp**: Geben Sie an, wie die Kosten für die einzelnen Lieferarten berechnet werden sollen. Es werden zwei Berechnungsarten unterstützt:

    - **Fest**: Für die Lieferart wird eine Pauschale verwendet. Bei Auswahl dieser Berechnungsart bestimmt das Feld **Kosten** die Kostenpauschale.
    - **Pro Entfernungseinheit**: Die Kosten für die Lieferart werden berechnet, indem der im Feld **Kosten** angegebene Wert mit der Entfernung zwischen Lieferadresse und Standorten multipliziert wird.

- **Kosten**: Geben Sie den Wert an, der im Zusammenhang mit dem Feld **Berechnungstyp** verwendet wird, um die Kosten für eine Lieferart zu berechnen.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Kostenkomponententyp = Versand und Berechnungsgrundlage = Mehrstufig

Wird eine Kombination aus dem Kostenkomponententyp **Versand** und der Berechnungsgrundlage **Mehrstufig** verwendet, beruhen die Versandkosten einer Lieferart entweder auf einer Kostenpauschale oder auf der Entfernung. Allerdings beruht die Entfernung bei dieser Kombination auf einer mehrstufigen Entfernungsskala.

Für diese Kombination müssen die folgenden Felder eingerichtet werden:

- **Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.
- **Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.
- **Standardkosten**: Geben Sie die Kosten an, die für eine Lieferart verwendet werden sollen, wenn die Entfernung zwischen der Lieferadresse und dem Standort nicht in eine der mehrstufigen Entfernungen der Lieferart fällt.
- **Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken. Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.
- **Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist. Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.
- **Unternehmen**: Geben Sie die juristische Person an, für die Kostenfaktor konfiguriert wird. Alle Positionen der Berechnungskriterien müssen sich auf dieselbe juristische Person beziehen.
- **Lieferarten**: Geben Sie die Lieferarten an, für die die Kosten konfiguriert werden.
- **Entfernungstyp**: Geben Sie an, ob die mehrstufige Entfernungsdefinition Luftlinie oder Straßenentfernung ist.
- **Entfernungseinheiten**: Geben Sie die Einheit an, in der die Entfernung gemessen wird.
- **Entfernung von**: Geben Sie den Startpunkt der mehrstufigen Entfernung an.
- **Entfernung bis**: Geben Sie den Zielpunkt der mehrstufigen Entfernung an.
- **Berechnungstyp**: Geben Sie an, wie die Kosten für die einzelnen Lieferarten und die mehrstufige Entfernung berechnet werden sollen. Es werden zwei Berechnungsarten unterstützt:

    - **Fest**: Für die Lieferart wird eine Pauschale verwendet. Bei Auswahl dieser Berechnungsart bestimmt das Feld **Kosten** die Kostenpauschale.
    - **Pro Entfernungseinheit**: Die Kosten für die Lieferart und die mehrstufige Entfernung werden berechnet, indem der im Feld **Kosten** angegebene Wert mit der Entfernung zwischen Lieferadresse und Standorten multipliziert wird.

- **Kosten**: Geben Sie den Wert an, der im Zusammenhang mit dem Feld **Berechnungstyp** verwendet wird, um die Kosten für eine Lieferart zu berechnen.

> [!NOTE]
> - Bei Angaben mehrstufiger Entfernungen prüft das System, ob Entfernungen fehlen oder überlappen.
> - Der für eine Lieferart verwendete Entfernungstyp muss für alle mehrstufigen Entfernungen identisch sein.

### <a name="other-cost-component-type"></a>Kostenkomponententyp „Sonstiges“

In diesem Abschnitt wird beschrieben, wie die einzelnen Kombinationen des Kostenkomponententyps **Sonstiges** und eines weiteren Kostentyps bei nicht versandbezogenen Kosten berechnet werden. Ferner wird erläutert, wie der DOM-Solver die einzelnen Kombinationen verwendet.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Kostenkomponententyp = Sonstiges und anderer Kostentyp = Auftrag

Eine Kombination aus dem Kostenkomponententyp **Sonstiges** und dem anderen Kostentyp **Auftrag** wird verwendet, um auf Auftragsebene Kosten ohne Versandbezug zu definieren.

Für diese Kombination müssen die folgenden Felder eingerichtet werden:

- **Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.
- **Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.
- **Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken. Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.
- **Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist. Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.
- **Kosten**: Geben Sie den Wert für nichtversandbezogene Kosten auf Auftragsebene ein.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Kostenkomponententyp = Sonstiges und anderer Kostentyp = Auftragsposition

Eine Kombination aus dem Kostenkomponententyp **Sonstiges** und dem anderen Kostentyp **Auftragsposition** wird verwendet, um auf Auftragspositionsebene Kosten ohne Versandbezug zu definieren.

Für diese Kombination müssen die folgenden Felder eingerichtet werden:

- **Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.
- **Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.
- **Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken. Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.
- **Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist. Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.
- **Kosten**: Geben Sie den Wert für nichtversandbezogene Kosten auf Auftragspositionsebene ein.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Kostenkomponententyp = Sonstiges und anderer Kostentyp = Standort

Eine Kombination aus dem Kostenkomponententyp **Sonstiges** und dem anderen Kostentyp **Standort** wird verwendet, um für eine Gruppe von Standorten oder für einen einzelnen Standort nichtversandbezogene Kosten zu berechnet.

Für diese Kombination müssen die folgenden Felder eingerichtet werden:

- **Kostenfaktor**: Geben Sie einen eindeutigen Bezeichner für den Kostenfaktor ein.
- **Beschreibung**: Geben Sie Name und Beschreibung des Kostenfaktors ein.
- **Startdatum** und **Enddatum**: Mithilfe dieser Felder können Sie den Kostenfaktor auf einen bestimmten Zeitraum beschränken. Werden diese Felder leer gelassen, gilt der Kostenfaktor unendlich lang.
- **Aktiv**: Gibt an, ob der Kostenfaktor aktiv ist. Bei der DOM werden nur aktive Kostenfaktoren berücksichtigt, die dem Erfüllungsprofil zugewiesen sind.
- **Erfüllungsgruppe**: Geben Sie die Gruppe der Standorte an, für die die Kosten ohne Versandbezug definiert werden.
- **Erfüllungslagerplatz**: Geben Sie den Ort an, für den die Kosten ohne Versandbezug definiert werden.

    > [!NOTE]
    > Bei standortbasierten Berechnungskriterien können keine Erfüllungsgruppe und kein Erfüllungslagerplatz angegeben werden.

- **Kosten**: Geben Sie den Wert für die Kosten ohne Versandbezug auf Ebene der Erfüllungsgruppe oder auf Ebene des Erfüllungslagerplatzes an.

> [!IMPORTANT]
> Damit diese Kosten bei der DOM berücksichtigt werden, muss der Kostenfaktor im jeweiligen Erfüllungsprofil ergänzt werden.
