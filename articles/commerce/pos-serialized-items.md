---
title: Arbeiten mit serialisierten Artikeln in der POS
description: In diesem Thema wird erläutert, wie Sie serialisierte Artikel in der Verkaufsstellen-(POS)-Anwendung verwalten.
author: boycezhu
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 1e0d6aa7cd5576578378e70c6ee808833314aff3
ms.sourcegitcommit: 919620b4aca425e6a1248ee12f50a622d2531e58
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/27/2020
ms.locfileid: "3290769"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbeiten mit serialisierten Artikeln in der POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Viele Einzelhändler verkaufen Produkte, die eine serielle Kontrolle erfordern. Diese Artikel werden als *serialisierte Artikel* bezeichnet. Einige Einzelhändler möchten möglicherweise Seriennummern für Nachverfolgungszwecke beibehalten. Andere Einzelhändler möchten möglicherweise während des Verkaufsprozesses Seriennummern für Service- und Garantiezwecke erfassen. In diesem Thema wird erläutert, wie Sie serialisierte Artikel in der Microsoft Dynamics 365 Commerce-Verkaufsstellen-(POS)-Anwendung verwalten können.

## <a name="serial-number-configurations"></a>Seriennummernkonfigurationen

Ein Artikel wird als serialisierter Artikel betrachtet, wenn ihm eine Rückverfolgungsangaben-Gruppe zugewiesen ist, der eingerichtet ist, um Seriennummern zu ermöglichen. In Commerce-Zentrale auf der Seite **Rückverfolgungsangaben-Gruppen** wählen Sie die Option **Aktiv** aus, um Seriennummern für den Bestandsprozess zu aktivieren. Um Seriennummern für den Vertriebsprozess zu aktivieren, wählen Sie die Option **Aktiv im Vertriebssprozess** aus.

Im Inforegister **Rückverfolgungsangaben**, wenn die Option **Leerer Zugang zulässig** aktiviert ist, ist die Seriennummer eine optionale Eingabe während des Bestandszugangsprozesses. Wenn die Option deaktiviert ist, ist die Seriennummer erforderlich.

Im Inforegister **Seriennummern**, wenn die Option **Seriennummernkontrolle** aktiviert ist, muss die Seriennummer pro Einheit eindeutig sein. Mit anderen Worten, doppelte Seriennummern sind nicht zulässig.

## <a name="serialized-items-in-the-receiving-process"></a>Serialisierte Artikel im Empfangsprozess

Der Vorgang **Eingehender Bestand** in der POS-Anwendung ermöglicht es Benutzern, die folgenden Aufgaben für serialisierte Elemente auszuführen:

- Registrieren Sie Seriennummern für serialisierte Artikel, wenn diese Artikel über eine Bestellung in der Filiale eingehen.
- Überprüfen Sie vorregistriere Seriennummern für serialisierte Artikel, wenn diese Artikel über eine Bestellung oder ein Umlagerungsauftrag in der Filiale eingehen.

> [!NOTE]
> Um den Vorgang **Eingehender Bestand** zum Registrieren oder Überprüfen serialisierter Artikel zu verwenden, muss dem Artikel eine Rückverfolgungsangaben-Gruppe zugewiesen werden, die so eingerichtet ist, dass Seriennummern für die Option **Aktiv**, nicht für die Option **Aktiv im Verkaufsprozess** zulässig sind.

Um den Empfangsprozess zu starten, können Sie im Vorgang **Eingehender Bestand** in der Ansicht **Jetzt empfangen** beginnen, indem Sie den Strichcode des Artikels scannen oder die Artikel-ID eingeben. Alternativ können Sie in der Ansicht **Vollständige Auftragsliste** beginne, indem Sie den Artikel manuell auswählen.

Wenn es sich bei dem ausgewählten oder empfangenen Artikel um einen serialisierten Artikel handelt, enthält der Bereich **Details** für den Artikel einen Link **Seriennummer verwalten**, der die Seite **Seriennummernverwaltung** öffnet. Alternativ können Sie die Seite **Seriennummernverwaltung** öffnen, entweder durch die Auswahl **Seriennummer** in der App-Leiste der Auftragsdetailansicht oder durch Auswahl von **Seriennummer verwalten** im Dialogfeld, das Sie während des Empfangsprozesses auffordert. Die Seite **Seriennummernverwaltung** listet alle offenen Seriennummernpositionen auf, deren Registrierung oder Überprüfung aussteht. Auf dieser Seite befinden sich möglicherweise zwei Registerkarten: eine für den aktuellen Artikel und eine für alle serialisierten Artikel im Auftrag.

Das Feld **Status** auf der Seite **Seriennummernverwaltung** bietet Informationen über die aktuelle Phase, in der sich jede Seriennummer befindet:

- **Nicht registriert** – Die Seriennummer wurde nicht angegeben oder die vorregistrierte Seriennummer wurde noch nicht überprüft.
- **Wird registriert** – Die Seriennummer wurde registriert und lokal in der Kanaldatenbank der Filiale gespeichert, oder die vorregistrierte Seriennummer wurde überprüft. Nur Seriennummern mit dem Status **Wird registriert** werden zur Commerce-Zentrale übermittelt, wenn Sie Ihrem Empfang abschließen.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrieren Sie Seriennummern für serialisierte Artikel

Für eine Bestellung bietet ein Dialogfeld, das Sie während des Empfangsprozesses eines serialisierten Artikels auffordert, die Option **Seriennummer verwalten**. Sie können diese Option auswählen, um die Seite **Seriennummernverwaltung** zu öffnen und mit der Registrierung von Seriennummern zu beginnen. Sie können diesen Schritt auch während des Empfangsprozesses überspringen und die Eingabe später bereitstellen, bevor der Beleg gebucht wird.

Standardmäßig wird die Registerkarte für den aktuellen Artikel angezeigt. Alle Seriennummernpositionen haben einen leeren Seriennummernwert und den Status **Nicht registriert**. Sie können Seriennummern-Strichcodes scannen oder **Seriennummer** in der App-Leiste auswählen, um fortlaufend Seriennummern in das Dialogfeld einzugeben. Die von Ihnen eingegebenen Seriennummern werden in der Liste angezeigt, und der Status der Seriennummernpositionen wird in **Wird registriert** geändert. Die maximale Anzahl von Seriennummern, die Sie in der Liste registrieren können, entspricht der Empfangsmenge. Wenn Sie einen Fehler machen, können Sie **Bearbeiten** oder **Löschen** im Bereich **Details** auswählen, um Änderungen an den von Ihnen eingegebenen Seriennummern vorzunehmen.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern registrieren möchten.

Während der Registrierung der Seriennummer auf dieser Seite erfolgt eine Überprüfung der Duplizierung. Wenn Sie versuchen, eine doppelte Seriennummer für einen Artikel einzugeben, für das die Seriennummernsteuerung aktiviert ist, erhalten Sie eine Fehlermeldung und müssen eine andere Nummer angeben.

### <a name="validate-serial-numbers-on-serialized-items"></a>Seriennummern für serialisierte Artikel überprüfen

Bei einem Umlagerungsauftrag muss die ausgehende Seite während des Versandvorgangs Seriennummern für die serialisierten Artikeln vorregistrieren. Bei einer Bestellung kann der Lieferant Informationen zur Seriennummer über einen Versand-Avis (ASN) bereitstellen, und Sie können die Nummern der zu versendenden Artikel vorregistrieren. In beiden Fällen sind die Seriennummern vor dem Empfang bekannt. Auf der eingehenden Seite müssen Sie daher nur überprüfen, ob Sie das erhalten haben, was Sie erhalten sollten.

Um Seriennummern zu überprüfen, können Sie die Seite **Seriennummernverwaltung** öffnen, entweder während des Empfangsprozesses oder zu einem beliebigen Zeitpunkt, bevor der Empfang verbucht wird. Für jeden serialisierten Artikel mit vorregistrierten Seriennummern werden alle Seriennummern automatisch auf den Anfangsstatus **Nicht registriert** auf dieser Seite festgelegt. Um Seriennummern zu validieren, können Sie diese scannen oder eingeben. Bei der Eingabe der Seriennummer überprüft die Anwendung, ob sie mit vorregistrierten Seriennummern übereinstimmen. Wenn sie übereinstimmen, wird ihr Status in **Wird registriert** geändert. Anderenfalls wird eine Fehlermeldung angezeigt. Die maximale Anzahl von Seriennummern, die Sie in der Liste überprüfen können, entspricht der Empfangsmenge.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern überprüfen möchten.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eingehender Bestandsvorgang in POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
