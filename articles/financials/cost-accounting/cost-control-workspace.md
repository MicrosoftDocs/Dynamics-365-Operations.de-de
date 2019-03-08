---
title: Kostensteuerungs-Arbeitsbereich
description: Dieses Thema enthält Informationen zum Kostensteuerung-Arbeitsbereich. Dieser Arbeitsbereich ist ein zentraler Punkt, in dem Vorgesetze, die für die Steuerung eines Kostenobjekts oder für das Festlegen eines Satzes von Kostenobjekten in einer Dimension oder über Dimensionen hinweg zuständig sind, auf Berichte zugreifen können.
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspaceConfiguration, CAMCostControlWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6a196c677ed27666efec8a180f1d3b7e7ee931c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "363751"
---
# <a name="cost-control-overview"></a>Überblick der Kostensteuerung 

[!include [banner](../includes/banner.md)]

Der Arbeitsbereich **Kostensteuerung** ist ein zentraler Punkt, in dem Manager, die zum Steuern des Kostenträgers des Satzes oder Kostenträger in eine Dimension oder zu Dimensionen (zum Beispiel Kostenstellen und Produktgruppen) zuständig sind, Berichte zugreifen können. Die Berichte im Arbeitsbereich werden vollständig von den Kostenbuchhaltern verwaltet, damit das Layout und die Daten, die für die Berichtserstattung verwendet werden, in der gesamten Organisation konsistent sein können.

## <a name="cost-control-workspace-configuration"></a>Arbeitsbereichskonfiguration für Kostensteuerung

Kostenbuchhalter können so viele Berichtskonfigurationen definieren, wie für die gewünschte Datenanordnung oder das Layout erforderlich. Eine Berichtskonfiguration besteht aus sechs Abschnitten, und jede davon trägt entweder zur Auswahl der Zieldatenanordnung oder dem Layout bei.

Um einen Arbeitsbereich für Kostensteuerung zu konfigurieren, klicken Sie auf **Kostenrechnung** \> **Einstellungen** \> **Arbeitsbereichskonfiguration für Kostensteuerung**

### <a name="general"></a>Allgemein

Auf dem Inforegister **Allgemeines** können Sie ein eindeutiges Berichtslayout erstellen. Der Name des Berichts ist ein eindeutiger Bezeichner, den Benutzer im **Kostensteuerung**-Arbeitsbereich erkennen können. Sie können auch angeben, ob der Bericht für Kostenbuchhalter freigegeben oder intern bleiben soll.

| Feld       | Beschreibung |
|-------------|-------------|
| Name        | Geben Sie einen eindeutigen Namen für das Layout ein. |
| Beschreibung | Geben Sie eine detailierte Beschreibung ein. |
| Publiziert   | Wenn Sie das Feld auf **Ja** festlegen, kann ein Benutzer, dem eine der folgenden Rollen zugewiesen wird, den Bericht im Arbeitsbereich **Kostensteuerung** anzeigen:<ul><li>Kostenrechnungs-Manager</li><li>Kostenbuchhalter</li><li>Sachbearbeiter Kostenbuchhaltung</li><li>Kostenobjekt-Controller</li></ul>Wenn Sie das Feld auf **Nein** festlegen, können nur Benutzer, denen eine der folgenden Rollen zugewiesen werden, den Bericht im Arbeitsbereich **Kostensteuerung** anzeigen:<ul><li>Kostenrechnungs-Manager</li><li>Kostenbuchhalter</li><li>Sachbearbeiter Kostenbuchhaltung</li></ul> |

### <a name="data-filtering"></a>Datenfilterung

Auf dem Inforegister **Datenenfilterung** können Sie die Datenengrundlage für den Bericht definieren. Benutzer dieses Berichts werden Werte im Bericht angezeigt, nachdem Daten verarbeitet wurden.

| Feld                                                             | Beschreibung |
|-------------------------------------------------------------------|-------------|
| Kostenrechnungssachkonto                                            | Das **Kostenrechnungssachkonto**, auf dem der Bericht basiert. Der Wert wird aus dem Feld **Kostenkontrolleinheit** abgeleitet. |
| Kostensteuerungseinheit                                                 | Der Wert, den Sie auswählen, bestimmt das Kostenrechnungs-Sachkonto und die Kostenobjekte, auf denen dieser Bericht basiert. |
| Statistische Dimensionshierarchie, Kostenelementdimensionshierarchie | Ein Konfigurationssatz des **Kostensteuerung**-Arbeitsbereichs kann entweder nicht-monetäre oder monetäre Werte melden, aber nicht im gleichen Layout. Wählen Sie einen Wert im Feld **Kostenelement-Dimensionshierarchie** aus, um monetäre Werte zu melden. Wählen Sie einen Wert im Feld **Statistische Dimensionshierarchie** aus, um nicht monetäre Werte zu melden. Der Dimensionshierarchiedatensatz, den Sie auswählen, bestimmt die Struktur die Ebenen der Berichtserstellung und Aggregation.<blockquote>[!NOTE]<br>Um nicht-monetäre und monetäre Werte nebeneinander anzuzeigen, können Sie die Daten nach Microsoft Excel für das Microsoft Power BI-Inhaltspaket exportieren.</blockquote> |
| Kostenobjekt-Dimensionshierarchie                                   | Wählen Sie die Dimensionshierarchie der Kostenelementdimension aus, die dem Zweck der Berichterstellung, die Sie definieren, entspricht. |
| Ursprüngliche Budgetversion                                           | Wählen Sie die Budgetversion-ID aus, die als ursprüngliches Budget im Rahmen dieses Berichts dient. |
| Überarbeitete Budgetversion                                            | Wählen Sie die Budgetversion-ID aus, die als überarbeitetes Budget im Rahmen dieses Berichts dient. |

### <a name="assign-calculation-records"></a>Berechnungsdatensätze zuweisen

Die Gemeinkostenberechnung führt mehrere Berechnungsschritte mit den Quelldaten aus, z. B. Kostenverhaltensklassifizierung, Kostenaufteilung und Kostenzuweisung. Mehrere Gemeinkostenberechnungen können für den gleichen Finanzzeitraum durchgeführt werden, falls fehlende Quelldaten ermittelt werden, oder Regeln aktualisiert werden müssen. Jede Gemeinkostenberechnung wird mit einer eindeutigen Kennung gespeichert. Der Kostenbuchhalter kann eine bestimmte Gemeinkostenberechnungskennung auswählen. Benutzer des Berichts, z. B. Manager, finden die Ergebnisse der obenliegenden Berechnung im **Kostensteuerung**- Arbeitsbereich.

| Feld                  | Beschreibung |
|------------------------|-------------|
| Steuerkalenderperiode | Wählen Sie die Steuerkalenderperiode aus, der eine Gemeinkostenberechnungskennung zugewiesen werden soll.<blockquote>[!NOTE]<br>Die Finanzzeiträume, die im Feld aufgeführt sind, stammen aus dem Steuerkalender, der dem Kostenrechnungs-Sachkonto zugeordnet ist.</blockquote> |
| Tatsächliche Version         | Wählen Sie die entsprechende Gemeinkostenberechnungskennnung. |
| Budgetversion         | Wählen Sie die entsprechende Gemeinkostenberechnungskennnung. |
| Überarbeitete Budgetversion | Wählen Sie die entsprechende Gemeinkostenberechnungskennnung. |

### <a name="fiscal-periods-per-column"></a>Finanzzeiträume pro Spalte

Im Inforegister **Finanzzeiträume pro Spalte** entscheidet der Kostenbuchhalter, welche Steuerperiode im Berichtslayout angezeigt werden soll.

Die Werte in den ausgewählten Spalten werden mit den ausgewählten Werten im Inforegister **Finanzzeiträume pro Spalte** multipliziert.

| Feld                | Beschreibung |
|----------------------|-------------|
| Aktuelle Periode       | Der Saldo des aktuellen Finanzzeitraums wird angezeigt.<blockquote>[!NOTE]<br>Standardmäßig wird die aktuelle Periode vom Sitzungsdatum bestimmt. Im Arbeitsbereich **Kostensteuerung** kann ein bestimmter Finanzzeitraum ausgewählt werden. Der ausgewählte Wert stellt dann die aktuelle Periode dar.</blockquote> |
| Vorherige Periode      | Der Saldo des vorherigen Finanzzeitraums wird angezeigt. Verwendete Formel:<br>Laufender Finanzzeitraum – 1<blockquote>[!NOTE]<br>Standardmäßig wird die vorherige Periode vom Sitzungsdatum abgeleitet. Im Arbeitsbereich **Kostensteuerung** kann ein bestimmter Finanzzeitraum als aktueller Zeitraum ausgewählt werden. **Vorheriger Zeitraum** wird anschließend entsprechend neu berechnet.</blockquote> |
| Seit Jahresbeginn         | Der Wert seit Jahresbeginn wird angezeigt. Verwendete Formel:<br>YearToDate (Laufender Finanzzeitraum)<blockquote>[!NOTE]<br>Standardmäßig wird die aktuelle Periode vom Sitzungsdatum bestimmt. Im Arbeitsbereich **Kostensteuerung** kann ein bestimmter Finanzzeitraum ausgewählt werden. Der ausgewählte Wert stellt dann den aktuelle Zeitraum dar, und der Wert **Seit Jahresbeginn** wird entsprechend aktualisiert.</blockquote> |
| Durchschnitt seit Jahresbeginn | Der Durchschnitt seit Jahresbeginn wird angezeigt. Verwendete Formel:<br>(YearToDate [Laufender Finanzzeitraum]) ÷ (Anzahl [Laufender Finanzzeitraum])<p><strong>Beispiel</strong></p><ul><li>**Statistisches Dimensionsmitglied:** Vollzeitmitarbeiter</li><li>**Aktuelles Datum:** 3-21-2017</li><li>**Zeitraum:** Finanzzeitraum 1, Finanzzeitraum 2, Finanzzeitraum 3</li><li>**Größe:** 10, 10, 12</li></ul>In diesem Fall **Durchschnitt seit Jahresbeginn** = (10 + 10 + 12) = 3 ÷ 10,67<p>Der Wert **Durchschnitt seit Jahresbeginn** kann für Kostenelementdimensionsmitglieder und statistische Dimensionsmitglieder berechnet werden.</p><blockquote>[!NOTE]<br>Standardmäßig wird die aktuelle Periode vom Sitzungsdatum bestimmt. Im Arbeitsbereich **Kostensteuerung** kann ein bestimmter Finanzzeitraum ausgewählt werden. Der ausgewählte Wert stellt dann den aktuellen Zeitraum dar, und die Werte **Seit Jahresbeginn** und **Durchschnitt seit Jahresbeginn** werden entsprechend aktualisiert.</blockquote> |

### <a name="columns-to-display-for-costs"></a>Anzuzeigende Spalten für Kosten

Im Inforegister **Anzuzeigende Spalten für Kosten** entscheidet der Kostenbuchhalter, welche Spalten der Berichtslayouts enthalten sollen. Es gibt drei Kategorien: Fixkosten, variable Kosten und nicht klassifizierte Kosten.

| Feld                 | Beschreibung |
|-----------------------|-------------|
| Fixkosten            | Dieser Spaltentyp zeigt die Fixkosten auf Grundlage der ausgewählten Gemeinkostenberechnungskennnung.<blockquote>[!NOTE]<br>Dieser Spaltentyp zeigt nur dann einen Saldo, wenn Gemeinkostenberechnungskennnung für den Finanzzeitraum ausgewählt ist.</blockquote> |
| Variable Kosten         | Dieser Spaltentyp zeigt die variblen Kosten auf Grundlage der ausgewählten Gemeinkostenberechnungskennnung.<blockquote>[!NOTE]<br>Dieser Spaltentyp zeigt nur dann einen Saldo, wenn Gemeinkostenberechnungskennnung für den Finanzzeitraum ausgewählt ist.</blockquote> |
| Fixkosten und variable Kosten | Dieser Spaltentyp zeigt die Fixkosten auf Grundlage der ausgewählten Gemeinkostenberechnungskennnung.<blockquote>[!NOTE]<br>Dieser Spaltentyp zeigt nur dann einen Saldo, wenn Gemeinkostenberechnungskennnung für den Finanzzeitraum ausgewählt ist.</blockquote> |
| Gesamtkosten            | Dieser Spaltentyp zeigt die Gesamtkosten (nicht klassifizierte Kosten, Fixkosten und variable Kosten).<blockquote>[!NOTE]<br>Der Spaltentyp zeigt jederzeit den Saldo.</blockquote> |
| Nicht klassifizierte Kosten     | Dieser Spaltentyp zeigt die nicht klassifizierten Kosten.<blockquote>[!NOTE]<br>Diese Spalte kann verwendet werden, um zu überprüfen, ob alle Kosten von der Gemeinkostenberechnung richtig klassifiziert wurden, oder ob die Kostenverhaltensregeln angepasst werden müssen.</blockquote> |

### <a name="columns-to-display-for-budgeted-costs"></a>Anzuzeigende Spalten für budgetierte Kosten

Im Inforegister **Anzuzeigende Spalten für budgetierte Kosten** entscheidet der Kostenbuchhalter, welche Spalten für die ausgewählten Budgetversionen angezeigt werden sollen. Eine individuelle Auswahl kann für das ursprüngliche und das überarbeitete Budgets vorgenommen werden.

> [!NOTE]
> Da die sich folgenden Felder für das ursprüngliche Budget und das überarbeitete Budget auf die gleiche Art verhalten, werden sie nur einmal erklärt.

| Feld                     | Beschreibung |
|---------------------------|-------------|
| Budget                    | Budgetsalden werden entsprechend der ausgewählten Spalten angezeigt.<blockquote>[!NOTE]<br>Die Salden basieren auf den Budgetversionen, die auf dem Inforegister **Datenenfilterung** ausgewählt werden.</blockquote> |
| Budgetabweichung           | Berechnen Sie die Differenz zwischen Budget und Istkosten und zeigen Sie sie an. Verwendete Formel:<br>Budgetsaldo – Tatsächliches Saldo |
| Budgetabweichung in %      | Berechnen Sie die Differenz zwischen Budget und Istkosten in Prozent und zeigen Sie sie an. Verwendete Formel:<br>(Budgetsaldo – tatsächliches Saldo) ÷ Budgetsaldo |
| Abweichungsperiodenschwellenwert | Legen Sie einen Schwellenwert für die Abweichung des Geldbetrags für den aktuellen Zeitraum fest. Wenn der Schwellenwert überschritten wird, wird die entsprechende Position rot im Arbeitsbereich **Kostensteuerung** hervorgehoben.<blockquote>[!NOTE]<br>Dieses Feld gilt nur für die Kostenelemente, die Aufwendungen darstellen.</blockquote> |
| Abweichungsjahresschwellenwert   | Legen Sie einen Schwellenwert für die Abweichung des Geldbetrags für das Jahr fest. Wenn der Schwellenwert überschritten wird, wird die entsprechende Position rot im Arbeitsbereich **Kostensteuerung** hervorgehoben. |
| Abweichungsschwellenwert %      | Legen Sie einen Schwellenwert für die Abweichung in Prozent fest. Wenn der Schwellenwert überschritten wird, wird die entsprechende Position rot im Arbeitsbereich **Kostensteuerung** hervorgehoben.<blockquote>[!NOTE]<br>Der gleiche Prozentsatzschwellenwert gilt für den aktuellen Zeitraum und das Jahr.</blockquote> |

## <a name="cost-control-workspace"></a>Kostensteuerungs-Arbeitsbereich

Der Arbeitsbereich **Kostensteuerung** ist als Internet-Bericht vorgesehen. Daher kann allen Managern, die für einen Kostenobjekt zuständig sind, wie unter [Zugriffsrechte für Kostenobjekt-Controller definieren](access-rights-cost-object-controller.md) beschrieben, Zugriff erteilt werden.

Die Liste der Berichte, die für Benutzer, z. B. Manager, verfügbar sind, wird von der Einstellung der Option **Veröffentlicht** auf der Seite **Konfigurationen des Kostensteuerungs-Arbeitsbereichs** gesteuert.

![Ein Bericht, den Benutzer im Kostensteuerungs-Arbeitsbereichs finden können](./media/report-cost-control.png)

Ein Manager kann die anzuzeigende Steuerkalenderperiode auswählen. Das Sitzungsdatum wird verwendet, um die standardmäßige aktuelle Periode zu bestimmen.

Die Werte in der Steuerkalenderperiode werden durch den Berichtsnamen und den Steuerkalender bestimmt, der für das Kostenrechnungssachkonto ausgewählt wurde, das dem Berichtsnamen auf der Seite **Konfigurationen des Kostensteuerungs-Arbeitsbereichs** zugeordnet ist.

In der Kostenobjektdimensionshierarchie können Benutzer die Aggregationsebene auswählen, auf der Salden angezeigt werden sollen. Wenn Sie Sicherheit auf Zugriffsebene aktivieren, steuern Sie die Berechtigungen, damit Benutzer nur die Hierarchieebenen auswählen können, für die ihnen Zugriff erteilt wurde. Daher können sie nur die zusammengefassten Salden anzeigen, für die Ihnen Zugriff erteilt wurde.

### <a name="add-or-remove-columns"></a>Spalten hinzufügen oder entfernen

Benutzer können die Spalten in einem Bericht entsprechend Ihrer Anforderungen anpassen.

### <a name="view-details"></a>Details anzeigen

Benutzer können die Details zu den Salden anzeigen, die im Arbeitsbereich angezeigt werden. Wenn Benutzer einen Kostenelement-Dimensionshierarchieknoten auswählen und dann auf **Details anzeigen** klicken, zeigt das Dialogfeld **Kostenelementdetails** Informationen für den Knoten an.

Das Raster zeigt jedes Kostenelement, das dem Kostenelement-Dimensionshierarchieknoten zugeordnet ist, sowie dessen Werte. Die Spalten, die in der Rasterabgleichung die Arbeitsbereichseinstellungen aufgeführt sind.

Zwei Diagramme zeigen eine Zusammenfassung der Istwerte im vgl. zu Budget und Budgetabweichung nach Zeitraum.

![Diagramme, die eine Zusammenfassung der Istwerte im vgl. zu Budget und Budgetabweichung nach Zeitraum anzeigen](./media/cost-element-details-operations.png)

Benutzer können auf **Kosteneinträge** klicken, um bei Bedarf die Detailinformationen zu den Eintragsdetails anzuzeigen.

![Kosteneinträge](./media/cost-entries.png)

Beispielsweise ist Miete eine Aufwendung, die zu Kostenstellen verteilt wird. Ein Benutzer, der die Mietkosten verstehen möchte, die in der Kostenstelle enthalten sind, kann Detailinformationen anzeigen, um zu sehen, wie die Miete berechnet wurde.

Wenn Benutzer auf **Verteilschlüssel** auf der Seite **Kosteneinträge** klicken, wird ein Dialogfeld angezeigt. Benutzer können der Regel den Verteilschlüssel zuweisen und dann die entsprechenden statistischen Kennzahlen angezeigen, die für den Zeitraum erfasst werden.

Im folgenden Beispiel hat der Verteilschlüssel den Typ **Formelzuteilungsbasis**, und die Formel wird angezeigt. Die Faktoren, die die Formel definieren, werden aufgelistet. Darüber hinaus zeigt ein Raster die Berechnung an, die pro Kostenobjekt durchgeführt wird.

![Berechnungen pro Kostenobjekt](./media/cost-entries-allocation-base.png)

Zusätzliche Ressourcen 

[Zugriffsrechte für Kostenobjekt-Controller definieren](access-rights-cost-object-controller.md)


