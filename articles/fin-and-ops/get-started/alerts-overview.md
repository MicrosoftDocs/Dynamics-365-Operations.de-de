---
title: Warnungen
description: Dieses Thema enthält allgemeine Informationen zu Warnungen in Microsoft Dynamics 365 for Finance and Operations. Sie können Warnungen verwenden, um über Ereignisse informiert zu bleiben, die Sie während des Arbeitstags nachverfolgen möchten.
author: tjvass
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 28ee34cd9133c634af98a50168e22efd0f74abce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546938"
---
# <a name="alerts"></a>Warnungen

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Info über Warnungen
Warnungen bilden ein Benachrichtigungssystem für wichtige Ereignisse in Microsoft Dynamics 365 for Finance and Operations. Sie können Warnungen verwenden, um über Ereignisse informiert zu bleiben, die Sie während des Arbeitstags nachverfolgen möchten. Sie können eigene Warnregelsätze einfach erstellen, sodass Sie gewarnt werden, wenn Lieferungen überfällig sind, wenn Aufträge gelöscht werden, wenn Preise sich ändern oder wenn ein beliebiges anderes Ereignis eintritt, auf das Sie reagieren müssen.

In der Enterprise Resource Planning (ERP) gibt es mehrere typische Szenarien, in der die Warnfunktionen im Bereich Finance and Operations verwendet werden kann. Nachfolgend finden Sie einige Beispiele.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Szenario 1: Erstellen einer Warnregel für neue Aufträge

1. Die Seite **Alle Bestellungen** wird angezeigt.
2. Klicken Sie alternativ im Aktivitätsbereich auf der Registerkarte **Optionen** in der Gruppe **Freigeben** auf **Benutzerdefinierte Warnung** erstellen.
3. Im Dialogfeld **Warnregel erstellen** auf dem Inforegister **Warnen wenn**, auf dem Feld **Ereignis**, wählen Sie **Datensatz wurde erstellt** aus.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Szenario 2: Erstellen einer Warnregel für die Verschiebung eines Liefertermins

1. Die Seite **Bestellungen** wird angezeigt.
2. Wählen Sie eine Bestellungs-ID aus, um auf die Bestellungsdetails zuzugreifen.
3. Erweitern Sie das Inforegister **Bestellkopf**.
4. Klicken Sie alternativ im Aktivitätsbereich auf der Registerkarte **Optionen** in der Gruppe **Freigeben** auf **Benutzerdefinierte Warnung** erstellen.
5. Im Dialogfeld **Warnregel erstellen** auf dem Inforegister **Warnen wenn**, auf dem Feld **Ereignis**, wählen Sie **Lieferungsdatum** aus.
6. Wählen Sie im Feld **Ereignis** **wurde verschoben** aus.
    
Nachdem Sie das Dialogfeld **Warnregel erstellen** schließen, erscheint die Regel auf der Seite **Warnregeln verwalten**. Sie können die Seite **Warnregeln verwalten** verwenden, um Ihre vorhandenen Warnregeln zu aktualisieren. So können Sie Ereignistrigger ändern, Ereignisbenachrichtigungen aktualisieren und Ablaufdatum aktualisieren. Um die Seite **Warnregeln verwalten** zu öffnen, klicken Sie auf die Schaltfläche **" Warnen** auf der Registerkarte **Optionen** im Aktivitätsbereich.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Was passiert, wenn eine Warnregel erstellt wird?

Beim Erstellen von Warnregeln können Sie ein vordefiniertes Ereignis einem spezifischen Feld zuordnen. Wenn beispielsweise das Datum eintritt, das im Feld angegeben ist, oder wenn die Inhalte eines Felds sich ändern. Alternativ können Sie ein Ereignis den Datensätzen auf einer bestimmten Seite zuordnen. Wenn beispielsweise der Datensatz erstellt oder gelöscht wird.

Wenn das ausgewählte Ereignis für das Feld oder für einen Datensatz auf der Seite eintritt, wird eine Warnung an Sie gesendet. Sie erstellen beispielsweise eine Regel, in der Sie das Feld **Lieferdatum** in einer bestimmten Bestellposition mit dem Ereignis verknüpfen **ist seit dieser Zeitdauer fällig**. Sie legen den Zeitrahmen auf fünf Tage fest. In diesem Beispiel wird eine Warnung fünf Tage nach dem Lieferdatum dieser Bestellposition ausgelöst.

Darüber hinaus können Sie die Warnregeln verfeinern, indem Sie Bedingungen festlegen. So können Sie bei neuen Bestellungen gewarnt werden, die für bestimmte Kreditorenkonten erstellt werden.

## <a name="preparing-for-an-alert"></a>Vorbereiten auf ein Warnung

Vor dem Einrichten einer Warnregel müssen Sie entscheiden, wann oder in welchen Situationen Sie Warnungen erhalten möchten. Wenn Sie wissen, über welches Ereignis Sie informiert werden möchten, suchen Sie in Finance and Operations die Seite, wo die Daten angezeigt werden, die dieses Ereignis verursachen. Das Ereignis kann ein eintretendes Datum oder eine spezifische Änderung sein. Daher müssen Sie die Seite finden, auf der das Datum angegeben ist, oder auf der das Feld, das sich ändert oder der neue Datensatz, der erstellt wird, angezeigt wird. Auf Basis dieser Informationen können Sie nun die Warnregel erstellen.

## <a name="components-of-an-alert-rule"></a>Komponenten einer Warnungsregel

Eine Warnregel besitzt fünf Komponenten:

- **Ereignis** – Das Ereignis, das eine Warnregel auslöst, kann ein eintretendes Datum oder eine bestimmte Änderung sein, die eintritt. Sie definieren Ereignisse im Inforegister **E-Mail-Warnungen für Änderungen des Einzelvorgangsstatus senden** des Dialogfelds **Warnregel erstellen**.
- **Bedingung** – Klicken Sie auf dem Inforegister **Warnen für** des Dialogfelds **Warnregel erstellen**, Sie können den Bereich für die Bedingung auswählen, um zu steuern, wann Sie über Ereignisse informiert werden. Sie können die Regel entweder nur auf den aktuellen Datensatz anwenden oder auf alle sichtbaren Datensätze auf der Seite. Wenn die Regel für juristischen Personen gilt, können Sie die Option **Organisationsweit** auf **Ja** festlegen.
- **Ablauf einer Regel** – Klicken Sie auf dem Inforegister **Warnen bis** des Dialogfelds **Warnregel erstellen** ad. Dort können Sie angeben, wie lange die Warnregel aktiv sein soll.
- **Inhalt** – Klicken Sie auf dem Inforegister **Warnen mit** des Dialogfelds **Warnregel erstellen**, geben Sie den Text und den abhängigen Meldungstext ein, die die Warnungen verwendet werden sollen.
- **Benutzer** – Klicken Sie auf dem Inforegister **Warnregel erstellen** des Dialogfelds **Warnregel erstellen**. Dort können Sie angeben, welcher Benutzer die Warnmeldungen erhalten soll. Standardmäßig wird Ihre Benutzerkennung ausgewählt.

    > [!NOTE]
    > Diese Option ist auf Organisationsadministratoren beschränkt.

## <a name="email-notifications-from-alerts"></a>E-Mail-Benachrichtigungen von Warnungen

E-Mail-Benachrichtigungen von Warnungen sind noch nicht aktiviert. Diese werden in einer späteren Aktualisierung aktiviert.
