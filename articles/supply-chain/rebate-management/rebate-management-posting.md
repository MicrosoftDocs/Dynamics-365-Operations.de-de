---
title: Einrichtung von Rückvergütungsverwaltungsbuchungen
description: Dieses Thema beschreibt, wie Sie die Daten für Buchungsprofile festlegen. Buchungsprofile werden verwendet, um Buchungseinträge für Berechnungspositionen für die Rückvergütungsverwaltung zu ermitteln.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 808080d9e84c4af1b061d5a4ce76d5fa309e66f7
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216742"
---
# <a name="rebate-management-posting-setup"></a>Einrichtung von Rückvergütungsverwaltungsbuchungen

[!include [banner](../includes/banner.md)]

Buchungsprofile für die Rückvergütungsverwaltung werden verwendet, um Buchungseinträge für Berechnungspositionen für die Rückvergütungsverwaltung zu ermitteln. Wenn in der Deal-Kopfzeile ein Buchungsprofil ausgewählt ist, gilt dies für alle Deal-Positionen.

Diese Funktion funktioniert unternehmensübergreifend (juristische Personen). Sie können das Unternehmen angeben, für das Rückstellungen gebildet werden und von dem Ansprüche bezahlt werden. Sie können auch verschiedene Rückstellungssollkonten und Abschreibungshabenkonten pro Quellenbuchungsunternehmen festlegen.

Um Buchungsprofile für die Rückvergütungsverwaltung für Debitoren und Kreditoren einzurichten, gehen Sie zu **Rückvergütungsverwaltung \> Einrichtung von Rückvergütungsverwaltungsbuchungen \> Buchungsprofile für die Rückvergütungsverwaltung**. Die Seite **Buchungsprofile für die Rückvergütungsverwaltung** einen Listenbereich, in dem alle vorhandenen Profile angezeigt werden. Sie können die Schaltflächen im Aktivitätsbereich verwenden, um der Profile zur Liste hinzuzufügen oder daraus zu entfernen.

In den verbleibenden Abschnitten dieses Themas wird beschrieben, wie Sie die verfügbaren Felder beim Erstellen oder Bearbeiten eines Profils verwenden.

## <a name="posting-profile-header"></a>Buchungsprofilkopfzeile

In der folgenden Tabelle werden die Einstellungen beschrieben, die im Kopfbereich jedes Buchungsprofile für die Rückvergütungsverwaltung verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Buchungsprofil | Geben Sie einen eindeutigen Namen für das Profil ein. |
| Beschreibung | Geben Sie eine Beschreibung des Profils ein. |
| Modul | Wählen Sie die Art der Rückvergütungen und Lizenzgebühren aus, mit denen das Profil verknüpft ist (*Debitor* oder *Kreditor*). |
| Typ | Wählen Sie den Profiltyp (*Rückvergütung* oder *Lizenzgebühr*). |
| Zahlungstyp | <p>Dieses Feld bestimmt das Format der gebuchten Rückvergütungsausgabe.<p><p>Wenn das Feld **Typ** auf *Rückvergütung* gesetzt ist, stehen folgende Werte zur Verfügung:</p><ul><li>*Bezahlen mit Kreditorenkonten* – Wenn Sie eine Rückvergütung für einen Kunden buchen, wird eine Kreditorenrechnung für den Remissekreditor erstellt, die für den Rückvergütungsdebitor eingerichtet wurde. Wenn Sie eine Rückvergütung für einen Lieferanten buchen, wird eine Kreditorenrechnung für das Rückvergütungsdebitorkonto eingerichtet erstellt.</li><li>*Debitorabzüge* – Wenn Sie die Rückvergütung buchen, wird eine Debitorabzugserfassung für den Rückvergütungsdebitor erstellt.</li><li>*Steuerrechnung-Debitorabzüge* – Wenn Sie die Rückvergütung buchen, wird eine Freitextrechnung für den Rückvergütungsdebitor erstellt.</li><li>*Handelsausgaben* – Wenn Sie die Rückvergütung buchen, wird eine Debitorabzugserfassung für den Rückvergütungsdebitor erstellt.</li><li>*Berichterstellung* – Wenn Sie die Rückvergütung buchen, wird eine Debitorabzugserfassung für den Rückvergütungsdebitor erstellt.</li></ul><p>Wenn das Feld **Typ** auf *Lizenzgebühr* gesetzt ist, stehen folgende Werte zur Verfügung:</p><ul><li>*Bezahlen mit Kreditorenkonten* – Wenn Sie die Rückvergütung buchen, wird eine Kreditorenrechnung für das Rückvergütungsdebitorkonto eingerichtet erstellt.</li><li>*Berichterstellung* – Wenn Sie die Rückvergütung buchen, wird eine Kreditorenrechnung für das Rückvergütungsdebitorkonto eingerichtet erstellt.</li></ul><p>Weitere Informationen finden Sie im folgenden Abschnitt zu [Zahlungstypen](#payment-types). |
| Firma | Wählen Sie das Unternehmen (juristische Person) aus, für das Rückstellungen gebildet werden und von dem Ansprüche bezahlt werden. |

### <a name="payment-types"></a>Zahlungstypen

Die folgende Tabelle fasst zusammen, wie die verschiedenen Einstellungen des Felds **Zahlungstyp** beeinflussen, wo Zahlungen gebucht werden. Zahlungen können abhängig von der Zieltransaktion und dem Rückvergütungstyp auf ein Debitorenkonto, ein Kreditorenkonto oder ein Remissekonto gebucht werden.

| Zahlungstyp | Zieltransaktionstyp | Rückvergütungstyp | Zahlung an (Rechnungskonto) |
|---|---|---|---|
| Bezahlen mit Kreditorenkonten | Kreditorenrechnungserfassung | Debitorenrückvergütung | Remissekreditorenkonto des Debitors |
| Bezahlen mit Kreditorenkonten | Kreditorenrechnungserfassung | Debitorenlizenzgebühr | Kreditorenkonto |
| Bezahlen mit Kreditorenkonten | Kreditorenrechnungserfassung | Händlerrückvergütung | Kreditorenkonto |
| Debitorenabzüge | Tägliche Erfassung | Debitorenrückvergütung | Debitorenkonto |
| Steuerrechnungs-Debitorabzüge | Freitextrechnung | Debitorenrückvergütung | Debitorenkonto |
| Handelsausgaben | Tägliche Erfassung | Debitorenrückvergütung | Debitorenkonto |
| Bericht | Tägliche Erfassung | Debitorenrückvergütung | Debitorenkonto |
| Bericht | Kreditorenrechnungserfassung | Debitorenlizenzgebühr | Kreditorenkonto |
| Bericht | Kreditorenrechnungserfassung | Händlerrückvergütung | Kreditorenkonto |

> [!NOTE]
> Berücksichtigen Sie beim Einrichten von [Rückvergütungsverwaltungsdeals](rebate-management-deals.md) die folgenden Punkte:
>
> - Für Deals, bei denen das Feld **Abstimmen nach** auf *Deal* gesetzt ist, können Sie das dynamische Dealkonto während der Buchung nicht verwenden. Sie müssen ein bestimmtes Debitoren- oder Kreditorenkonto verwenden.
> - Für Deals, bei denen das Feld **Abstimmen nach** auf *Position* gesetzt ist, können Sie ein Buchungsprofil verwenden, das mit einem dynamischen Dealkonto in der Deal-Position verrechnet wird, da der Debitor pro Deal-Position festgelegt ist.

## <a name="posting-fasttab"></a>Buchungs-Inforegister

In der folgenden Tabelle werden die Felder beschrieben, die im Inforegister **Buchung** für die Rückvergütungsverwaltung verfügbar sind.

| Feld | Beschreibung |
|---|---|
| Gutschrifttyp | Wählen Sie aus, ob die Gutschrift an ein Sachkonto oder einen Debitor oder Kreditor gehen soll. |
| Habenkonto | Das Konto, auf das die Gutschriften gebucht werden, wenn Rückstellungen für Rückvergütungen gebildet werden. Dieses Konto wird auch als Sollkonto verwendet, wenn die Rückvergütung zur Gutschrift an den Debitor gebucht wird. |
| Name der Erfassung<br>(Im Abschnitt **Rückstellung**) | Wählen Sie den Namen der Erfassung aus, in der die gebuchte Rückstellung aufgezeichnet werden soll. |
| Typ | Wählen Sie aus, ob die Rückvergütung an ein Sachkonto oder einen Debitor oder Kreditor gebucht werden soll. Wenn das Feld **Zahlungstyp** in der Kopfzeile auf *Steuerrechnungs-Debitorabzüge* gesetzt ist, steht dieses Feld auf *Debitor/Kreditor*. |
| Kontoquelle verwenden | <p>Wählen Sie einen der folgenden Werte aus:</p><ul><li>*Keiner* – Wenn Sie diesen Wert auswählen, müssen Sie im Feld **Rückvergütungskonto** ein Konto angeben.</li><li>*Dealkonto* – Verwenden Sie das Debitor- oder Kreditorenkonto, das in der Rückvergütungsposition angegeben ist. Sie können diesen Wert nur für Deals auswählen, bei denen das Feld **Abstimmen nach** auf *Position* und das Feld **Kontocode** auf *Tabelle* gesetzt ist. Dies gilt nicht für Debitorenbuchungsprofile für Lizenzgebühren.</li></ul> |
| Rückvergütungskonto | Das Konto, auf das tatsächliche Rückvergütungsausgaben gebucht werden. |
| Name der Erfassung<br>(Im Abschnitt **Rückvergütungsverwaltung**) | Wählen Sie den Namen der Erfassung aus, mit der eine Gutschrift für den Rückvergütungsbetrag an den Debitor gebucht werden soll. Dieses Feld steht nicht zur Verfügung, wenn das Feld **Zahlungstyp** in der Kopfzeile auf *Steuerrechnungs-Debitorabzüge* gesetzt ist. |
| Artikel-Mehrwertsteuergruppe | Geben Sie an, ob die Rückvergütung steuerpflichtig ist. |
| Name der Erfassung<br>(Im Abschnitt **Abschreibung**) | Wenn die gebuchte Rückvergütung nicht der Rückstellung entspricht, kann die Differenz abgeschrieben werden. Wählen Sie den Namen der Erfassung aus, in der die gebuchte Abschreibung aufgezeichnet werden soll. |

## <a name="posting-by-company-fasttab"></a>Inforegister „Buchung nach Unternehmen“

Im Inforegister **Buchung nach Unternehmen** können Sie für jedes Buchungsprofil für die Rückvergütungsverwaltung das Buchungskonto angeben, das von jedem Unternehmen (juristische Person) im Raster verwendet wird.

Verwenden Sie die Schaltflächen in der Symbolleiste, um dem Raster Unternehmen hinzuzufügen und sie daraus zu entfernen. Verwenden Sie jedes Mal, wenn Sie dem Raster eine Zeile hinzufügen, das Feld **Unternehmen**, um die juristische Person für diese Zeile anzugeben. Das Feld **Name** wird dann automatisch ausgefüllt.

Wählen Sie die Zeile für jedes Unternehmen aus und geben Sie die folgenden Informationen in die Felder unter dem Raster ein:

- **Solltyp** – Wählen Sie aus, ob die Lastschrift an ein Sachkonto oder einen Debitor oder Kreditor gehen soll.
- **Sollkonto** – Geben Sie das Konto ein, auf das der Lastschriftbetrag gebucht wird, wenn Rückstellungen für Rückvergütungen gebildet werden.
- **Hauptkonto** – Wählen Sie das Hauptkonto für Abschreibungen aus.
