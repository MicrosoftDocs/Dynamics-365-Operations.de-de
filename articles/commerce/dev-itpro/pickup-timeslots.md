---
title: Zeitfenster für die Kundenabholung erstellen und aktualisieren
description: In diesem Thema wird beschrieben, wie Sie Zeitfenster für die Kundenabholung in der Commerce-Zentralverwaltung konfigurieren und aktualisieren.
author: anupamar-ms
manager: AnnBe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: f86eb47ec64dff230223ed0ecbe792373aca649f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681541"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Zeitfenster für die Kundenabholung erstellen und aktualisieren

[!include [banner](../../includes/banner.md)]

In diesem Thema wird beschrieben, wie Sie Zeitfenster für die Kundenabholung in der Commerce-Zentralverwaltung konfigurieren und aktualisieren.

Mit der Zeitfensterfunktion können Einzelhändler ein Zeitfenster für Artikel definieren, für die der Liefertyp Kundenabholung aktiviert ist. Mit Zeitfenstern können Einzelhändler die Tage und Zeiten definieren, an denen Aufträge in einem Geschäft abgeholt werden können. Einzelhändler können auch die Anzahl der Aufträgen definieren, die während eines bestimmten Zeitraums abgeholt werden können. Auf diese Weise können Einzelhändler die Anzahl der Aufträge begrenzen, die an einem bestimmten Tag und zu einer bestimmten Uhrzeit abgeholt werden können. Das Ergebnis ist, dass die Qualität der Erfahrung ihrer Kunden höher ist.

> [!NOTE]
> Die Zeitfensterfunktion ist in Microsoft Dynamics 365 Commerce Version 10.0.15 und höher verfügbar.

Die folgende Abbildung zeigt ein Beispiel für die Auswahl eines Zeitfensters während eines E-Commerce-Auftragsabschlusses.

![Beispiel für die Zeitfensterauswahl während des E-Commerce-Auftragsabschlusses](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Zeitfenstereigenschaften

Ein Zeitfenster ist ein spezifisches Intervall, in dem ein Kunde wählen kann, einen Auftrag in einem bestimmten Geschäft oder an einem bestimmten Standort abzuholen. Die Zeitfensterverwaltungsfunktion ist nur verfügbar, wenn die Kundenabholungslieferart in Dynamics 365 Commerce konfiguriert ist.

Ein Zeitfenster wird mithilfe der folgenden Eigenschaften definiert:

- **Lieferart** – Geben Sie die Abhollieferart an, für den das Zeitfenster gilt.
- **Mindestanzahl von Tagen** und **Höchstanzahl von Tagen** – Geben Sie die frühesten und spätesten Daten an, die für die Abholung ausgewählt werden können, bezogen auf das Datum, an dem der Auftrag erteilt wird. 

    Die Eigenschaft **Mindestanzahl von Tagen** stellt sicher, dass es genug Zeit für den Einzelhändler gibt, um den Auftrag zu verarbeiten, bevor er für die Abholung bereit ist. Die Eigenschaft **Höchstanzahl von Tagen** stellt sicher, dass der Benutzer kein Datum auswählen kann, das zu weit in der Zukunft liegt. Zum Beispiel, wenn der Mindestwert auf **1** festgelegt ist und ein Auftrag am 20. September erteilt wird, ist der früheste Tag, an dem der Auftrag zur Abholung verfügbar ist, der nächste in Frage kommende Tag (21. September). In ähnlicher Weise können Sie durch Festlegen eines Maximalwerts die maximale Anzahl von Tagen definieren, innerhalb derer ein Auftrag abgeholt werden kann. Wenn Mindest- und Höchstwerte definiert werden, können Websitebenutzer während ihrer Auftragsabschlusserfahrung nur eine bestimmte Reihe von Tagen anzeigen und auswählen.

    Sie können den Mindestwert auf einen Dezimalwert festlegen, der kleiner als 1 ist. Wenn die Abholung beispielsweise vier Stunden nach Auftragserteilung verfügbar ist, legen Sie den Mindestwert auf **0,17** fest (= 4 ÷ 24, auf zwei Dezimalstellen aufgerundet). Wenn Sie den Mindestwert jedoch auf einen Dezimalwert von mehr als 1 festlegen, wird er immer auf die nächste ganze Zahl (nach oben oder unten) gerundet.

    Wenn Sie den Höchstwert auf einen Dezimalwert festlegen, wird er immer aufgerundet. Zum Beispiel wird ein Wert von **1,2** auf **2** aufgerundet.

- **Anfangsdatum** und **Endtermin** – Geben Sie das Start- und Enddatum des Zeitfensters an. Jeder Zeitfenstereintrag hat ein Start- und ein Enddatum. Daher haben Sie die Flexibilität, das ganze Jahr über verschiedene Zeitfenster hinzuzufügen (z. B. Abholungen während Ferienzeiten). Wenn das Start- und Enddatum eines Zeitfenster geändert wird, nachdem ein Auftrag erteilt wurde, werden die Änderungen für diesen Auftrag nicht übernommen. Wenn Sie Start- und Enddatum definieren, müssen Sie die Datumsangaben der Tage berücksichtigen, an denen das Geschäft geschlossen ist (z. B. 1. Weihnachtsfeiertag) und sicher stellen, dass keine Zeitfenster für diese Tage definiert werden.
- **Aktive Lieferzeiten** – Geben Sie den Zeitraum an, an dem die Abholung zulässig ist. Beispielsweise können die Abholzeiten täglich zwischen 14:00 Uhr und 17:00 Uhr liegen. Diese Eigenschaft ermöglicht es, dass Abholzeiten unabhängig von Geschäftsöffnungszeiten sind. Daher kann der Einzelhändler Abholzeiten konfigurieren, die seinen spezifischen Geschäftsanforderungen entsprechen. Wenn Sie die aktiven Abholzeiten definieren müssen Sie Geschäftsöffnungszeiten berücksichtigen und sicherstellen, dass keine Abholzeiten für Zeiten definiert werden, zu denen das Geschäft geschlossen ist.

    > [!NOTE]
    > Die Stunden für die Abholung im Geschäft müssen in der Zeitzone des entsprechenden Geschäfts definiert werden.

- **Zeitfensterintervall** – Geben Sie die Dauer an, die jedem Zeitfenster zugewiesen werden kann. Beispielsweise kann die Dauer jedes Zeitfensters in Schritten von 15 Minuten, 30 Minuten oder einer Stunde bestimmt werden.
- **Zeitfenster pro Intervall** – Geben Sie die Anzahl der Kunden oder Aufträge an, die in jedem Zeitfensterintervall zur Abholung bedient werden können. Geben Sie zum Beispiel **1**, **2**, **3** oder irgendeine andere ganze Zahl ein.
- **Aktive Tage** – Geben Sie die Wochentage an, an denen die Abholzeitfenster aktiv sind. Mit dieser Eigenschaft kann der Einzelhändler die Tage definieren, an denen er Abholaufträge unterstützen möchte.
- **Retail Channels** – Geben Sie die Retail Channels an. Jedes Zeitfenster kann einem oder mehreren Einzelhandelsgeschäften zugeordnet werden. Abhängig von den Öffnungszeiten der einzelnen Geschäfte können ein oder mehrere Zeitfenstereinträge erstellt und einem Kanal zugeordnet werden. 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Pro Kanal kann nur eine Zeitschlitzvorlage konfiguriert werden. Zu diesen Kanälen gehören Filialen, Call Center, mobile Geräte und E-Commerce-Sites.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Zeitfensterfunktion in Commerce-Zentralverwaltung konfigurieren

Zeitfenster müssen für jede Abhollieferart in der Commerce-Zentralverwaltung definiert werden, damit Verkaufstellen-(POS)- und E-Commerce-Kanäle auf sie verweisen können.

- Jedem Geschäft oder Kanal kann nur eine Zeitfenstervorlage zugeordnet werden.
- Jedes erstellte Zeitfenster sollte für jede Lieferart in jeder Vorlage eindeutig sein.
- Nachdem die Zeitfensterfunktion konfiguriert wurde, steht der Zeitfensterkalender den ausgewählten Geschäften oder Gruppen von Geschäften zur Verfügung. Er wird auch in der POS als Referenz sichtbar sein.

Um die Zeitfensterfunktion in der Commerce-Zentralverwaltung zu konfigurieren, folgen Sie diesen Schritten.

1. Wechseln Sie zu **Commerce** \> **Kanaleinrichtung** \> **Zeitfenster für Abholung im Geschäft**.
1. Wählen Sie **Neu** aus, um eine neue Zeitfenstervorlage zu erstellen. Um eine vorhandene Vorlage zu verwenden, wählen Sie die Vorlage im linken Bereich aus.
1. Geben Sie in den Feldern **Zeitfenster-ID** und **Beschreibung** Werte ein.
1. Im Inforegister **Auftragsabholung - Zeiteinstellungen** wählen Sie **Hinzufügen** aus.
1. Im Dialogfeld **Auftragsabholung - Zeiteinstellungen** definieren Sie den Datumsbereich, die Lieferart, aktive Lieferstunden, aktive Tage, Zeitfensterintervall, Zeitfenster pro Intervall und andere Einstellungen.

    Wenn die Zeitfenster auf absehbare Zeit statisch sind, lassen Sie das Feld **Enddatum** leer.

    > [!NOTE]
    > Sie können mehrere Vorlagen erstellen, aber nur eine Vorlage kann einem einzelnen Kanal oder Geschäft zugeordnet werden.

    ![Auftragsabholung – Dialogfeld „Zeiteinstellungen“](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Wählen Sie abschließend **OK** aus.
1. Wenn die Zeitfenster an einem Tag variieren, erstellen Sie zusätzliche Einträge im Inforegister **Auftragsabholung – Zeiteinstellungen**, um sicherzustellen, dass sich Datum und Uhrzeit nicht überschneiden.
1. Im Inforegister **Retail Channels** wählen Sie **Hinzufügen** aus, um die Zeitfenstervorlage den Geschäften oder Kanälen zuzuordnen, in denen sie verwendet wird.
1. Verwenden Sei im Dialogfenster **Organisationsknoten auswählen** die Pfeilschaltflächen, um die Geschäfte, Regionen und Organisationen auszuwählen (oder die Auswahl von ihnen aufzuheben), denen Vorlagen zugeordnet werden sollen.

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Wählen Sie abschließend **OK** aus.
1. Führen Sie auf der Seite **Verteilungsplan** die Einzelvorgänge **1070** und **1135** aus, um die Daten mit den Kanälen zu synchronisieren.

## <a name="time-slot-selection-for-pos-orders"></a>Zeitfensterauswahl für POS-Aufträge

Wenn in der POS ein Auftrag oder eine Auftragsposition für die Abholung identifiziert wird, kann der Kassierer das Geschäft oder den Standort für die Abholung sowie ein Datum und Zeitfenster auswählen. Wenn ein Kunde einen Abholauftrag für eine andere Filiale hat, kann der Kassierer einen Termin auswählen, an dem die Abholung in dieser Filiale verfügbar sein wird. Das Store Lookup liefert einen Verweis auf die Daten und Zeiten des Ladens.

Die folgende Abbildung zeigt ein Beispiel für die Auswahl eines Zeitfensters für einen POS-Auftrag.

![Ein Beispiel für die Zeitfensterauswahl für einen POS-Auftrag](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Zeitfensterauswahl für E-Commerce-Aufträge

Informationen zum Bereitstellen der Zeitfensterauswahl für E-Commerce-Aufträge finden Sie unter [Abholinformationsmodul](../pickup-info-module.md).

> [!NOTE]
> Benutzer können Abholzeitfenster auf der Auftragsabschlussseite einer Commerce-Website nur anzeigen und bearbeiten, wenn das Abholinformationsmodul dieser Seite hinzugefügt wurde. Wenn die Auftragsabschlussseite nicht das Abholinformationsmodul enthält, werden Aufträge erteilt, ohne das Benutzer Zeitfensterinformationen angeben oder anzeigen können.

Die folgende Abbildung zeigt ein Beispiel für einen E-Commerce-Auftrag, bei dem ein Abholzeitfenster ausgewählt wurde.

![Beispiel für einen E-Commerce-Auftrag, bei dem ein Abholzeitfenster ausgewählt wurde](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Abholinformationsmodul](../pickup-info-module.md)
