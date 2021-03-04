---
title: Erstellen von Warnregeln
description: Dieses Thema enthält Informationen zu Warnungen und erläutert, wie eine Warnregel erstellt wird, damit Sie über Ereignisse benachrichtigt werden, wie ein Datum, das eintritt, oder eine spezifische Änderung, die auftritt.
author: tjvass
manager: AnnBe
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 4fe97ca8e1eecdc064ad4d21d5acdeade9f33d9c
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694494"
---
# <a name="create-alert-rules"></a>Erstellen von Warnregeln

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Erste Schritte

Vor dem Einrichten einer Warnregel müssen Sie entscheiden, wann oder in welchen Situationen Sie Warnungen erhalten möchten. Wenn Sie wissen, über welches Ereignis Sie informiert werden möchten, suchen Sie nach der Seite, auf der die Daten angezeigt werden, die dieses Ereignis verursachen. Das Ereignis kann ein eintretendes Datum oder eine spezifische Änderung sein. Daher müssen Sie die Seite finden, auf der das Datum angegeben ist, oder auf der das Feld, das sich ändert oder der neue Datensatz, der erstellt wird, angezeigt wird. Auf Basis dieser Informationen können Sie nun die Warnregel erstellen.

Wenn Sie eine Warnregel erstellen, legen Sie die Kriterien fest, die erfüllt werden müssen, bevor eine Warnung ausgegeben wird. Kriterien ist grundsätzlich die Übereinstimmung zwischen dem Auftreten eines Ereignisses und der Erfüllung bestimmter Bedingungen. Wenn ein Ereignis auftritt, beginnt das System mit der Überprüfung anhand der Bedingungen, die eingerichtet wurden.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Sicherstellen, dass die Batch-Jobs für die Alarme ausgeführt werden.

Die Batch-Jobs für Datenänderungs- und Fälligkeitswarnungen müssen ausgeführt werden, damit die Warnbedingungen verarbeitet und die Benachrichtigungen gesendet werden können. Um Batch-Jobs auszuführen, gehen Sie zu **Systemadministration** > **Periodische Aufgaben** > **Alarme** und fügen Sie einen neuen Batch-Job für **Änderungsbasierte Warnungen** und/oder **Fälligkeits-Warnungen** hinzu. Wenn ein langer und häufig laufender Batch-Job benötigt wird, wählen Sie **Wiederholung** und setzen **Kein Enddatum** mit einem **Wiederholungsmuster** von **Minuten** und einem **Zahl** von **1**.

## <a name="events"></a>Ereignisse

Das Ereignis, das eine Warnregel auslöst, kann ein eintretendes Datum oder eine bestimmte Änderung sein, die eintritt. Auslöser für Ereignisse werden auf dem Inforegister **" Warnen wenn** des Dialogfelds **Warnregel erstellen** definiert. Welche Ereignisse für ein bestimmtes Feld verfügbar sind, hängt vom ausgewählten Auslöser ab.

Wenn Sie beispielsweise eine Warnregel für das Feld **Startdatum** einrichten möchten, sind Fälligkeitsereignisse geeignet. Daher ist der Ereignistyp **ist fällig in** für dieses Feld verfügbar. Für ein Feld wie **Kostenstelle** ist ein Fälligkeitsdatum dieses Ereignisses nicht angebracht. Daher ist der Ereignistyp **ist fällig in** für dieses Feld nicht verfügbar. Stattdessen ist der Ereignistyp **wurde geändert** verfügbar.

## <a name="event-types"></a>Ereignistypen

Drei Arten von Ereignisse können eintreten:

- **Ereignisse vom Typ " Erstellen und Löschen** – Diese Ereignisse lösen eine Warnung aus, wenn ein Datensatz erstellt oder gelöscht wird.
- **Aktualisierung von Typereignissen** – Dieser Ereignisse lösen eine Warnung aus, wenn die Daten in einem bestimmten Feld geändert werden.
- **Fälligkeitsdatum für Typereignisse** – Diese Ereignisse lösen eine Warnung aus, wenn ein Datum eintritt.
    
Auftretende Änderungen können von einem Benutzer initiiert werden. Beispielsweise ändert der Benutzer das Lieferdatum einer Bestellung. Alternativ können Änderungen als Teil eines Prozesses eintreten. Beispielsweise ändert sich das Feld **Status** eines Formulars, um den Lebenszyklus unterschiedlicher Prozesse im System widerzuspiegeln.

## <a name="conditions"></a>Bedingungen

Auf dem Dialogfenster **Warnung für mich** im **Alarmregel erstellen** können Sie mit Bedingungen steuern, wann Sie über Ereignisse alarmiert werden.

Beispielsweise können Sie angeben, dass das System Sie warnen soll, wenn der Status von Bestellungen sich ändert, jedoch nur, wenn eine Bestellung bestimmten Bedingungen entspricht. Konkret möchten Sie gewarnt werden, wenn der Status einer Bestellung auf **Eingegangen** festgelegt ist. Diese Statusänderung ist das Ereignis, das die Warnung auslöst.

Weiter muss entschieden werden, bei welchen Bestellungen Sie gewarnt werden möchten. Sie können zum Beispiel eine der folgenden Optionen auswählen. Diese Optionen definieren die Bedingungen für die Warnregel.

- **Aktuell ausgewählter Datensatz** – Sie erhalten eine Warnung, wenn der Status einer spezifischen Bestellung sich in **Eingegangen** ändert.
- **Alle Datensätze** – Sie erhalten eine Warnung, wenn sich der Status einer Bestellung für einen Artikel in der aktiven Seitenvorschau ändert. Sie können die erweiterte Filterung verwenden, die auf der Seite verfügbar ist, um Regeln für einen bestimmten Satz von Datensätzen zu erstellen. Sie können beispielsweise eine Warnung erstellen, die für alle Bestellungen für die Debitoren aus einer bestimmten Debitorengruppe ausgelöst wird.
    
## <a name="expiry-of-rule"></a>Ablaufdatum der Regel

Klicken Sie auf dem Inforegister **Warnen bis** des Dialogfelds **Warnregel erstellen**. Dort können Sie angeben, wie lange die Warnregel aktiv sein soll.

## <a name="alert-contents"></a>Warnungsinhalte

Klicken Sie auf dem Inforegister **Warnen mit** des Dialogfelds **Warnregel erstellen**, geben Sie den Text und den abhängigen Meldungstext ein, die für die Warnungen verwendet werden sollen.

## <a name="user-id"></a>Benutzer-ID

Auf der Registerkarte **Warnung durch** im Dialogfeld **Warnungsregel erstellen** können Sie definieren, welcher Benutzer die Warnmeldungen erhalten soll. Standardmäßig wird Ihre Benutzerkennung ausgewählt. Die Möglichkeit, den Benutzer, der die Warnung erhält, zu ändern, ist auf Administratoren der Organisation beschränkt.

## <a name="alerts-as-business-events"></a>Warnungen als Geschäftsereignisse

Warnungen können über das Event-Framework extern gesendet werden. Setzen Sie beim Anlegen eines Warnung **Organisationsweit** auf **Nein** und **Extern senden** auf **Ja**. Nachdem der Alert das Ereignis ausgelöst hat, können Sie einen in Power Automate eingebauten Ablauf über **Wenn ein Ereignis eintritt** auf dem Konnektor Finance and Operations auslösen oder das Ereignis über **Ereigniskatalog** explizit an einen Veranstaltungs-Endpunkt senden.

## <a name="create-an-alert-rule"></a>Erstellen Sie eine Warnregel.

0. Stellen Sie sicher, dass die Warnungen-Batch-Jobs ausgeführt werden (siehe oben).
1. Öffnen Sie das Formular, das die zu überwachenden Daten enthält.
2. Klicken Sie alternativ im Aktivitätsbereich auf der Registerkarte **Optionen** in der Gruppe **Freigeben** auf **Benutzerdefinierte Warnungsregek** erstellen.
3. Aktivieren Sie im Formular **Warnregel erstellen** in der Liste **Feld** das Feld, das überwacht werden soll.
4. Wählen Sie im Feld **Ereignis** den Typ des Berechtigungsereignisses aus.
5. Wählen Sie auf der Registerkarte **Warnen für** die gewünschte Option. Wenn Sie die Warnung als Geschäftsereignis senden möchten, stellen Sie sicher, dass **Organisationsweit** auf **Nein** gesetzt ist.
6. Wenn die Warnregel an einem bestimmten Datum deaktiviert werden soll, wählen Sie im Abschnitt **Warnung bis** ein Enddatum aus.
7. Auf der Registerkarte **Warnung mit** im Feld **Betreff** akzeptieren Sieie Standardbetreffzeile für die E-Mail-Nachricht, oder geben Sie einen neuen Betreff ein. Der Text wird als Betreffzeile für die E-Mail-Nachricht verwendet, die Sie empfangen, wenn eine Warnung ausgegeben wird. Wenn Sie die Warnung als Veranstaltung senden möchten, setzen Sie **Externes Senden** auf **Ja**.
8. Geben Sie im Feld **Nachricht** einen optionalen Meldungstext ein. Der Text wird als die Meldung verwendet, die Sie bei Auslösung einer Warnung erhalten.
9. Wählen Sie **OK** aus, um die Einstellungen zu speichern und die Warnregel zu erstellen.

## <a name="limitations-and-workarounds"></a>Einschränkungen und Problemumgehungen

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Problemumgehung zum Erstellen von Warnungen für die sekundären Datenquellen eines Formulars
Für einige sekundäre Datenquellen in Formularen können keine Warnungen erstellt werden. Wenn Sie beispielsweise Warnungen im Formular für Kunden- oder Kreditorenbuchungsprofile erstellen, sind nur die Felder in der Kopfzeile (CustLedger oder VendLedger) verfügbar und nicht die Dimensionskonten. Diese Einschränkung kann durch die Verwendung von **SysTableBrowser**, um diese Tabelle als primäre Datenquelle zu verwenden, umgangen werden. 
1. Öffnen Sie die Tabelle im Formular **SysTableBrowser**.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Erstellen Sie eine Warnung aus dem SysTableBrowser-Formular.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]