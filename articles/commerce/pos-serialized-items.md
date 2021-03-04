---
title: Arbeiten mit serialisierten Artikeln in der POS
description: In diesem Thema wird erläutert, wie Sie serialisierte Artikel in der Verkaufsstellen-(POS)-Anwendung verwalten.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412678"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Arbeiten mit serialisierten Artikeln in der POS

[!include [banner](includes/banner.md)]

Viele Einzelhändler verkaufen Produkte, die eine serielle Kontrolle erfordern. Diese Produkte werden als *serialisierte Artikel* bezeichnet. Einige Einzelhändler möchten möglicherweise Seriennummern im Shop- oder Lagerortbestand für Nachverfolgungszwecke beibehalten. Andere Einzelhändler möchten möglicherweise während des Verkaufsprozesses Seriennummern für Service- und Garantiezwecke erfassen. In diesem Thema wird erläutert, wie Sie serialisierte Artikel in der Microsoft Dynamics 365 Commerce-Verkaufsstellen-(POS)-Anwendung verwalten können.

## <a name="serial-number-configurations"></a>Seriennummernkonfigurationen

Ein Artikel wird als serialisierter Artikel betrachtet, wenn ihm eine Rückverfolgungsangaben-Gruppe zugewiesen ist, der eingerichtet ist, um Seriennummern zu ermöglichen. Wählen Sie in der Commerce-Zentralverwaltung auf der **Verfolgen von Dimensionsgruppen**-Seite die **Aktiv**-Option, um Seriennummern für den Inventarisierungsprozess zu aktivieren, oder wählen Sie die **Aktiv im Verkaufsprozess**-Option zum Aktivieren von Seriennummern für den Verkaufsprozess.

Schalten Sie im Inforegister **Rückverfolgungsangaben** die Parameter **Leerer Zugang zulässig** ein, um zuzulassen, dass die Seriennummer eine optionale Eingabe während des Bestandszugangsprozesses ist. Durch das Deaktivieren dieses Parameters wird die Seriennummer als erforderliche Eingabe erzwungen. Ebenso steuert der **Leerer Abgang zulässig** -Parameter, ob während des Bestandsversandvorgangs eine Seriennummer erforderlich ist.

> [!NOTE]
> Um die POS-Vorgänge **Eingehender Bestand** oder **Ausgehender Bestand** zu verwenden, um Seriennummern gegenüber einem serialisierten Artikel zu registrieren oder zu validieren, müssen Sie diesen Artikel so konfigurieren, dass er einer Rückverfolgungsangaben-Gruppe zugewiesen wird, die so eingerichtet ist, dass Seriennummern für die Option **Aktiv**, nicht für die Option **Aktiv im Verkaufsprozess** zulässig sind.

## <a name="serial-number-management-page"></a>Seite zur Verwaltung der Seriennummer

Wenn es sich bei dem ausgewählten, empfangenen oder versendeten Artikel in den **Eingangsbestand**- und **Ausgangsbestand**-POS-Vorgängen um einen serialisierten Artikel handelt, enthält der **Einzelheiten**-Bereich eine **Seriennummer verwalten**-Option, die auf die **Seriennummernverwaltung**-Seite verweist, auf der Sie Seriennummern für den Artikel registrieren oder validieren können. Alternativ können Sie die Seite **Seriennummernverwaltung** öffnen, entweder durch die Auswahl der **Seriennummer**-Aktion in der App-Leiste der Auftragsdetailansicht oder durch Auswahl von **Seriennummer verwalten** im Dialogfeld, das Sie während des Empfangs- oder Lieferprozesses auffordert. 

Die Seite **Seriennummernverwaltung** listet alle offenen Seriennummernpositionen auf, deren Registrierung oder Überprüfung aussteht. Auf dieser Seite befinden sich möglicherweise zwei Registerkarten: eine für den aktuellen Artikel und eine andere für alle serialisierten Artikel im Auftrag.

Das Feld **Status** auf der Seite **Seriennummernverwaltung** bietet Informationen über die aktuelle Phase, in der sich jede Seriennummer befindet:

- **Nicht registriert** – Die Seriennummer wurde nicht angegeben oder die vorregistrierte Seriennummer wurde noch nicht überprüft (im Empfangsprozess).
- **Wird registriert** – Die Seriennummer wurde registriert und lokal in der Kanaldatenbank der Filiale gespeichert, oder die vorregistrierte Seriennummer wurde überprüft. Nur Seriennummern mit dem Status **Wird registriert** werden zur Commerce-Zentrale übermittelt, wenn Sie Ihrem Empfang oder Ihre Erfüllung abschließen.

## <a name="receive-serialized-items"></a>Serialisierte Artikel empfangen

Der POS-Vorgang **Eingehender Bestand** ermöglicht es Benutzern, die folgenden Aufgaben für serialisierte Elemente auszuführen:

- Registrieren Sie Seriennummern für serialisierte Artikel, wenn diese Artikel über eine Bestellung in der Filiale eingehen.
- Überprüfen Sie vorregistriere Seriennummern für serialisierte Artikel, wenn diese Artikel über eine Bestellung oder ein Umlagerungsauftrag in der Filiale eingehen.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrieren Sie Seriennummern für serialisierte Artikel

Für eine Bestellung werden Sie von einem Dialogfeld mit der Option **Seriennummer verwalten** während des Empfangsprozesses eines serialisierten Artikels aufgefordert. Sie können diese Option auswählen, um die Seite **Seriennummernverwaltung** zu öffnen und mit der Registrierung von Seriennummern zu beginnen. Sie können diesen Schritt auch während des Empfangsprozesses überspringen und die Eingabe später bereitstellen, bevor der Beleg gebucht wird.

Standardmäßig wird die Registerkarte für den aktuellen Artikel angezeigt. Alle Seriennummernpositionen haben einen leeren Seriennummernwert und den Status **Nicht registriert**. Sie können Seriennummern-Strichcodes scannen oder **Seriennummer** in der App-Leiste auswählen, um fortlaufend Seriennummern einzugeben. Die von Ihnen eingegebenen Seriennummern werden in der Liste angezeigt, und ihr Status wird in **Wird registriert** geändert. Die maximale Anzahl von Seriennummern, die Sie in der Liste registrieren können, entspricht der Empfangsmenge. Wenn Sie einen Fehler machen, können Sie **Bearbeiten** oder **Löschen** im Bereich **Details** auswählen, um Änderungen an den von Ihnen eingegebenen Seriennummern vorzunehmen.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern registrieren möchten.

### <a name="validate-serial-numbers-on-serialized-items"></a>Seriennummern für serialisierte Artikel überprüfen

Bei einem Umlagerungsauftrag muss die ausgehende Seite während des Versandvorgangs Seriennummern für die serialisierten Artikeln vorregistrieren. Bei einer Bestellung kann der Lieferant Informationen zur Seriennummer über einen Versand-Avis (ASN) bereitstellen, und Sie können die Nummern der zu versendenden Artikel vorregistrieren. In beiden Fällen sind die Seriennummern vor dem Empfang bekannt. Auf der eingehenden Seite müssen Sie daher nur überprüfen, ob Sie das erhalten haben, was Sie erhalten sollten.

Um Seriennummern zu überprüfen, können Sie die Seite **Seriennummernverwaltung** öffnen, entweder während des Empfangsprozesses oder zu einem beliebigen Zeitpunkt, bevor der Empfang verbucht wird. Für jeden serialisierten Artikel mit vorregistrierten Seriennummern werden alle Seriennummern automatisch auf den Anfangsstatus **Nicht registriert** auf dieser Seite festgelegt. Um Seriennummern zu validieren, können Sie diese scannen oder eingeben. Bei der Eingabe der Seriennummer überprüft die Anwendung, ob sie mit vorregistrierten Seriennummern übereinstimmen. Wenn sie übereinstimmen, wird ihr Status in **Wird registriert** geändert. Anderenfalls wird eine Fehlermeldung angezeigt. Alternativ können Sie direkt eine Seriennummer und dann die **Seriennummer überprüfen**-Option im **Einzelheiten**-Bereich auswählen, um diese Seriennummer schnell als validiert zu markieren. Die maximale Anzahl von Seriennummern, die Sie in der Liste überprüfen können, entspricht der Empfangsmenge.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern überprüfen möchten.

## <a name="ship-serialized-items"></a>Versenden serialisierter Artikel

Sie können den **Ausgangsbestand**-POS-Vorgang zum Registrieren von Seriennummern für serialisierte Artikel verwenden, wenn diese über einen Transportauftrag aus dem aktuellen Shop versendet werden.

### <a name="register-serial-numbers-against-serialized-items"></a>Registrieren Sie Seriennummern für serialisierte Artikel

Für einen Transfer werden Sie von einem Dialogfeld mit der Option **Seriennummer verwalten** während des Versandprozesses eines serialisierten Artikels aufgefordert. Sie können die Option auswählen, um die Seite **Seriennummernverwaltung** zu öffnen und mit der Registrierung von Seriennummern zu beginnen. Sie können diesen Schritt auch während des Versandprozesses überspringen und den Versand später bereitstellen, bevor der Beleg gebucht wird.

Standardmäßig wird die Registerkarte für den aktuellen Artikel angezeigt. Alle Seriennummernpositionen haben einen leeren Seriennummernwert und den Status **Nicht registriert**. Sie können Seriennummern-Strichcodes scannen oder **Seriennummer** in der App-Leiste auswählen, um fortlaufend Seriennummern einzugeben. Die von Ihnen eingegebenen Seriennummern werden in der Liste angezeigt, und ihr Status wird in **Wird registriert** geändert. Die maximale Anzahl von Seriennummern, die Sie in der Liste registrieren können, entspricht der Versandmenge. Wenn Sie einen Fehler machen, können Sie **Bearbeiten** oder **Löschen** im Bereich **Details** auswählen, um Änderungen an den von Ihnen eingegebenen Seriennummern vorzunehmen.

Sie können auch Seriennummern auf der Registerkarte **Alle serialisierten Artikel** der Seite **Seriennummernverwaltung** registrieren. Wählen Sie in der Liste den Artikel aus, für den Sie Seriennummern registrieren möchten.

Optional können Sie die Überprüfung der Verfügbarkeit von Seriennummern während der Registrierung der Seriennummer für einen ausgehenden Überweisungsauftrag aktivieren. Wenn Sie bei dieser Validierung versuchen, eine Seriennummer zu versenden, die nicht im Bestand des Versandgeschäfts verfügbar ist, erhalten Sie eine Fehlermeldung und müssen eine andere Nummer angeben.

Um eine solche Validierung als Voraussetzung zu aktivieren, müssen Sie die folgenden Einzelvorgänge so planen, dass sie regelmäßig ausgeführt werden:

- **Retail und Commerce** > **Retail und Commerce IT** > **Produkte und Bestand** > **Produktverfügbarkeit mit Rückverfolgungsangaben**
- **Retail und Commerce** > **Verteilungspläne** > **1130** (**Produktverfügbarkeit**)

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Eingehender Bestandsvorgang in POS](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Ausgehender Bestandsvorgang in POS](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]