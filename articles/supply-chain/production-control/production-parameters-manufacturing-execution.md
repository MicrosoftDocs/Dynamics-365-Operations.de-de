---
title: Produktionsparameter für Fertigungssteuerung
description: Dieses Thema enthält Informationen zur Einrichtung der Produktionsparameter.
author: johanhoffmann
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ce0dadd353df756a468384e3bf8e68c0ad2033a7042b4986fce41aa0764afdbc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752729"
---
# <a name="production-parameters-in-manufacturing-execution"></a>Produktionsparameter für Fertigungssteuerung

[!include [banner](../includes/banner.md)]

Dieses Thema enthält Informationen zur Einrichtung der Produktionsparameter.

Das Modul **Fertigungssteuerung** ist vorrangig zur Verwendung durch Fertigungsunternehmen bestimmt. Damit können die Zeit und der Artikelverbrauch für Produktions-Einzelvorgänge oder Projekte erfasst werden. Bevor Sie die Fertigungssteuer zum Erfassen von Einzelvorgängen beginnen, müssen Sie verschiedene Produktionsparameter einrichten. Anhand dieser Parameter wird definiert, wie und wann Erfassungen im Produktionsprozess gebucht werden. Die Einstellungen der Produktionsparameter wirken sich auf die Lagerverwaltung, Produktionsverwaltung und Kostenkalkulation aus.

Sie sollten alle Einstellungen im Formular **Produktionsauftragsstandards** sorgfältig prüfen, bevor Arbeitskräfte mit der Erfassung für Produktions-Einzelvorgänge beginnen. Klicken Sie auf **Produktionssteuerung** &gt; **Einstellungen** &gt; **Fertigungssteuerung**&gt; **Produktionsparameterstandard**. Wenn Ihr Unternehmen die Funktion für mehrere Standorte verwendet, kann es ratsam sein, für die einzelnen Standorte unterschiedliche Produktionsparameter einzurichten. Die Parameter für die Integration mit dem **Produktionsmodul**" werden auf den folgenden Registerkarten auf der Seite **Produktionsparameter** eingerichtet:

- **Allgemein** – Allgemeine Paramatereinstellungen für Produktionseinzelvorgänge in der Fertigungssteuerung.
- **Start** – Parameter, die beim Starten von Produktionsarbeitsgängen verwendet werden.
- **Arbeitsgänge** – Parameter, die auf Produktionsarbeitsgänge und Rückmeldungen zu den Arbeitsgängen während des Produktionsprozesses angewendet werden.
- **Als abgeschlossen melden** – Parameter, die verwendet werden, wenn für Artikel im Zuge des letzten Arbeitsgangs eines Produktionsauftrags eine Fertigmeldung erstellt wird.
- **Mengenprüfung** – Parameter, die zur Überprüfung von Rückmeldungsmengen von Produktionsaufträgen verwendet werden.

## <a name="types-of-production-jobs"></a>Arten von Produktions-Einzelvorgängen
Wählen Sie auf der Registerkarte **Arbeitsgänge** die Arten von Produktionseinzelvorgängen aus, die auf der Seite **Einzelvorgangserfassung** erfasst werden müssen.

Üblicherweise findet eine Erfassung durch die Arbeitskräfte bei Einrichtungs- und Verarbeitungs-Einzelvorgängen statt. Wenn jedoch die Feinterminierung angewendet wird, können Sie andere Einzelvorgangstypen auswählen, z. B. Transport-Einzelvorgänge, bei denen Arbeitskräfte ebenfalls Erfassungen dazu vornehmen müssen, wann ein Produktionsauftrag verarbeitet wird. Beispielsweise können Sie die Erfassungen für Transportjobs benötigen.

> [!IMPORTANT]
> Vergewissern Sie sich, dass alle relevanten Einzelvorgangstypen ausgewählt sind. Andernfalls sind ggf. Einzelvorgänge nicht für die Erfassung auf der Seite **Einzelvorgangserfassung** verfügbar. Die Auswahl muss mit der Auswahl in der Spalte **Einzelvorgangsverwaltung** auf der Registerkarte **Einstellungen** der Seite **Arbeitsplangruppen** **Produktionssteuerung** **Einstellungen** &gt; ( **Arbeitspläne** &gt; ) **Arbeitsplangruppen** &gt; übereinstimmen.

Wenn **Einzelvorgangsverwaltung** für einen bestimmten Einzelvorgangstyp der Arbeitsplangruppe ausgewählt istt, wird dieser Einzelvorgangstyp für den Produktionsauftrag als fertig gemeldet, wenn für den Einzelvorgang im Modul "Zeiterfassung/BDE" eine Fertigmeldung erstellt wird. Wenn alle Einzelvorgangstypen, für die **Einzelvorgangsverwaltung** ausgewählt ist, bei einem Arbeitsgang als fertig gemeldet wurden, meldet die "Fertigungssteuerung" den Arbeitsgang ebenfalls als fertig.

> [!NOTE]
> Für einige Einzelvorgangstypen wird mittels Produktionserfassung eine Meldung möglicherweise manuell erstellt. Wählen Sie in diesem Fall die **Einzelvorgangsverwaltung** für den Einzelvorgangstyp aus, aber wählen Sie nicht den Einzelvorgangstyp für die Erfassung auf der Registerkarte **Arbeitsgänge** auf der Seite **Produktionsauftragsstandards** aus.

## <a name="bom-consumption-and-picking-list-journals"></a>Stücklistenverbrauch und Kommissionierlistenerfassungen
Eine konsistenten Einstellung für Stücklisten- (BOM)- Verbrauch ist wichtig, da diese Gewährleistung unterstützt, eine effiziente Lagerverwaltung sicherzustellen. Wenn die Parameter für den Stücklistenverbrauch nicht korrekt eingerichtet sind, kann dies dazu führen, dass Material zweifach oder gar nicht aus dem Bestand abgezogen wird.

Auf der Seite **Produktionsparameter** wird der automatische Stücklistenverbrauchs in drei Stufen eingerichtet:

- Zu Beginn einer Produktion. Richten Sie diesen Schritt in der Registerkarte **Start** ein.
- Während des Produktionsprozesses nach Abschluss eines Arbeitsgangs. Richten Sie diesen Schritt in der Registerkarte **Betrieb** ein.
- Nachdem ein Produktionsauftrag als fertig gemeldet wurde. Richten Sie diesen Schritt in der Registerkarte **Als beendet melden** ein.

Für jede Phase können Sie im Feld **Automatischer BOM-Verbrauch** eine von drei Methoden zum Entnehmen von Artikeln für einen Produktionsauftrag auswählen:

- **Stücklisten-Bezugsprinzip** – Diese Option wird in Kombination mit einer Option verwendet, die in der Stückliste im **Produktionsmodul** definiert wird. Klicken auf **Produktionssteuerung** &gt; **Gemeinsam** &gt; **Produktionsauftrag** &gt; **Alle Produktionsaufträge**. Wählen Sie auf der Seite **Alle Produktionsaufträge** einen Produktionsauftrag aus der Liste aus  und klicken Sie auf **BOM**. Auf der Seite **Stückliste** auf der Registerkarte **Einstellungen**, im Feld **Prinzip für automatischen Artikelverbrauch**, wählen Sie eine der folgenden Optionen aus:

  - **Starten**
  - **Fertig stellen**
  - **Manuell**
  - Leer (keine Option ist aktiviert.)
  - **Am Lagerplatz verfügbar**

    In der Fertigungssteuerung wenn **Prinzip für automatischen Artikelverbrauch** im Feld **Soll=Istrückmeldung Material** auf der Registerkarte **Starten** ausgewählt wird, werden alle Materialien, die in der Stückliste auf **Starten** festgelegt werden, vom Bestand abgezogen, wenn der Arbeitsgang gestartet wird. Die Option **Verfügbar am Lagerplatz** wird für Produkte verwendet, die für erweiterte Lagerortprozesse aktiviert werden. Wenn Sie dieses Prinzip für automatischen Artikelverbrauch aktivieren, wird Material geleert, wenn Lagerortarbeit für Rohmaterialentnahme abgeschlossen wird. Material wird auch geleert, wenn eine Stücklistenposition, die dieses Leerungsprinzip nutzt, für automatischen Artikelverbrauch für den Lagerort freigeben wurde und das Material am Produktionseingangslagerplatz verfügbar ist.

    > [!NOTE]
    > Wenn das Feld **Prinzip für automatischen Artikelverbrauch** auf der Registerkarte **Starten** in der Fertigungssteuerung festgelegt ist, müssen Sie dasselbe Prinzip entweder auf der Registerkarte **Arbeitsgänge** oder der Registerkarte **Fertigmeldung** auswählen. Durch diese Anforderung wird sichergestellt, dass Materialien aus dem Lagerbestand für die Stücklisten abgezogen werden, die **Fertig stellen** als Prinzip für automatischen Artikelverbrauch für den Produktionsauftrag verwenden. Wenn das gleiche Prinzip für automatischen Artikelverbrauch weder auf der Registerkarte **Arbeitsgänge** noch auf der Registerkarte **Fertigmeldung** aktiviert ist, werden Materialien doppelt aus dem Lagerbestand abgezogen werden.

- **Immer** – Wenn Sie in einer Phase diese Option auswählen, werden Materialien für diese Phase immer aus dem Lagerbestand abgezogen. Materialien für die Produktion werden beispielsweise abgezogen, wenn der Produktionsauftrag gestartet wird. Für diese Einstellung muss **Nie** auf den Registerkarten **Arbeitsgänge** und **Fertigmeldung** aktiviert sein. Diese Anforderung verhindert, dass Artikel doppelt aus dem Lagerbestand abgezogen werden.
- **Nie** – Wenn Sie diese Option für eine Phase auswählen, erfolgt kein Stücklistenverbrauch in dieser Phase. Wenn für alle drei Registerkarten beispielsweise **Nie** ausgewählt wurde **Start**, **Betrieb** und **Bericht**, müssen Materialien manuell aus dem Lagerbestand abgezogen werden.

> [!IMPORTANT]
> Berücksichtigen Sie dabei zunächst die Einrichtung der Produktionsparameter und stellen Sie sicher, dass zwischen den Parametern, die auf den verschiedenen Registerkarten der Seite **Produktionsparameter** ausgewählt wurden, keine Konflikte bestehen.

In den folgenden Beispielen werden Parametereinstellungen veranschaulicht, die unterschiedliche Prinzipien des Stücklistenverbrauchs unterstützen. Die Parameter werden auf der Seite **Produktionsparameter** in der Fertigungssteuerung eingerichtet.

### <a name="example-1-backflushing-on-operations"></a>Beispiel 1: – Materialentnahme bei Arbeitsgängen

Verwenden Sie die folgenden Einstellungen, wenn beim Fertigmelden von Artikeln für einen Arbeitsgang Kommmissionierlistenerfassungen und der Stücklistenartikelverbrauch generiert werden sollen.

| Registerkarte                | Feld                          | Einstellung                             |
|--------------------|--------------------------------|-------------------------------------|
| Starten              | Start online aktualisieren           | **Status** oder **Status + Menge** |
| Starten              | Soll=Istrückmeldung Material      | **Nie**                           |
| Operations         | Soll=Istrückmeldung Material      | **Immer**                          |
| Fertigmeldung | Soll=Istrückmeldung Material      | **Nie**                           |
| Fertigmeldung | Fertigmeldungsbericht online aktualisieren | **Status + Menge**               |

### <a name="example-2-backflushing-on-production"></a>Beispiel 2: – Materialentnahme bei der Produktion

Verwenden Sie die folgenden Einstellungen, wenn beim Fertigmelden von Artikeln für den Produktionsauftrag Kommmissionierlistenerfassungen und der Stücklistenartikelverbrauch generiert werden sollen.

| Registerkarte                | Feld                          | Einstellung                             |
|--------------------|--------------------------------|-------------------------------------|
| Starten              | Start online aktualisieren           | **Status** oder **Status + Menge** |
| Starten              | Soll=Istrückmeldung Material      | **Nie**                           |
| Operations         | Soll=Istrückmeldung Material      | **Nie**                           |
| Fertigmeldung | Soll=Istrückmeldung Material      | **Immer**                          |
| Fertigmeldung | Fertigmeldungsbericht online aktualisieren | **Status + Menge**               |

### <a name="example-3-flushing-principle"></a>Beispiel 3: – Prinzip für den automatischen Artikelverbrauch

Verwenden Sie die folgenden Einstellungen, wenn Kommissionierlistenerfassungen und der Stücklistenartikelverbrauch gemäß dem für die Stücklistenartikel festgelegten Prinzip für den automatischen Artikelverbrauch generiert werden sollen.

| Registerkarte                | Feld                          | Einstellung                |
|--------------------|--------------------------------|------------------------|
| Starten              | Start online aktualisieren           | **Status + Menge**  |
| Starten              | Soll=Istrückmeldung Material      | **Stücklisten-Bezugsprinzip** |
| Operations         | Soll=Istrückmeldung Material      | **Stücklisten-Bezugsprinzip** |
| Fertigmeldung | Soll=Istrückmeldung Material      | **Nie**              |
| Fertigmeldung | Fertigmeldungsbericht online aktualisieren | **Status + Menge**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Beispiel 4: – Abziehen von Materialien beim Starten eines Produktionsauftrags

Verwenden Sie die folgenden Einstellungen, wenn beim Starten einer Produktion Kommmissionierlistenerfassungen und der Stücklistenartikelverbrauch generiert werden sollen.

| Registerkarte                | Feld                          | Einstellung                             |
|--------------------|--------------------------------|-------------------------------------|
| Starten              | Start online aktualisieren           | **Status + Menge**               |
| Starten              | Soll=Istrückmeldung Material      | **Immer**                          |
| Operations         | Soll=Istrückmeldung Material      | **Nie**                           |
| Fertigmeldung | Soll=Istrückmeldung Material      | **Nie**                           |
| Fertigmeldung | Fertigmeldungsbericht online aktualisieren | **Status** oder **Status + Menge** |

Basierend auf den weiter oben in diesem Abschnitt beschriebenen Auswahlen werden Kommissionierlistenerfassungen in verschiedenen Stufen des Produktionsauftragsprozesses gebucht:

- Beim Start eines Arbeitsgangs
- Beim Melden der Rückmeldungsmenge für einen Arbeitsgang
- Beim Erstellen einer Fertigmeldung für Artikel des Produktionsauftrags

### <a name="example-5-manual-bom-consumption"></a>Beispiel 5: – Manueller Stücklistenverbrauch

Die folgenden Einstellungen können verwendet werden, wenn Materialien immer manuell aus dem Lagerbestand abgezogen werden sollen. In diesem Fall werden Kommissionierlistenerfassungen nicht gebucht.


|        Registerkarte         |             Feld              |         Einstellung         |
|--------------------|--------------------------------|-------------------------|
|       Starten        |      Start online aktualisieren      | <strong>Status</strong> |
|       Starten        |   Soll=Istrückmeldung Material    | <strong>Nie</strong>  |
|     Operations     |   Soll=Istrückmeldung Material    | <strong>Nie</strong>  |
| Fertigmeldung |   Soll=Istrückmeldung Material    | <strong>Nie</strong>  |
| Fertigmeldung | Fertigmeldungsbericht online aktualisieren | <strong>Status</strong> |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]