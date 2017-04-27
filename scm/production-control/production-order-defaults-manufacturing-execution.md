---
title: "Standardwerte zu Produktionsaufträgen in der Fertigungssteuerung"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Standardwerte zu Produktionsaufträgen in der Fertigungssteuerung

[!include[banner](../includes/banner.md)]




Sie sollten alle Einstellungen im Formular **Produktionsauftragsstandards** sorgfältig prüfen, bevor Arbeitskräfte mit der Erfassung für Produktions-Einzelvorgänge beginnen. Wenn Ihr Unternehmen die Funktion für mehrere Standorte verwendet, kann es ratsam sein, für die einzelnen Standorte unterschiedliche Produktionsparameter einzurichten. Die Auftragsstandards für die Integration mit der "Produktionssteuerung" werden auf den folgenden Registerkarten auf der Seite **Produktionsauftragsstandards** eingerichtet:

-   **Allgemein** – Allgemeine Auftragsstandards für Produktionseinzelvorgänge in der Fertigungssteuerung.
-   **Start** – Auftragsstandards, die verwendet werden, wenn Produktionseinzelvorgänge oder Arbeitsgänge gestartet werden.
-   **Vorgänge** –Auftragsstandards, die auf Produktionseinzelvorgänge oder Arbeitsgänge und Rückmeldungen zu den Arbeitsgängen während des Produktionsprozesses angewendet werden.
-   **Fertigmeldung** – Auftragsstandards, die angewendet werden, wenn für Artikel im Zuge des letzten Arbeitsgangs eines Produktionsauftrags eine Fertigmeldung erstellt wird.
-   **Mengenprüfung** – Auftragsstandards zur Überprüfung von Rückmeldungsmengen von Produktionsaufträgen.

## <a name="types-of-production-jobs"></a>Arten von Produktions-Einzelvorgängen
Wählen Sie auf der Registerkarte **Arbeitsgänge** die Arten von Produktionseinzelvorgängen aus, die auf der Seite **Einzelvorgangserfassung** erfasst werden müssen. Üblicherweise findet eine Erfassung durch die Arbeitskräfte bei Einrichtungs- und Verarbeitungs-Einzelvorgängen statt. Wenn jedoch die Feinterminierung angewendet wird, können Sie andere Einzelvorgangstypen auswählen, z. B. Transport-Einzelvorgänge, bei denen Arbeitskräfte ebenfalls Erfassungen dazu vornehmen müssen, wann ein Produktionsauftrag verarbeitet wird. **Wichtig:** Vergewissern Sie sich, dass alle relevanten Einzelvorgangstypen ausgewählt sind. Andernfalls sind ggf. Einzelvorgänge nicht für die Erfassung auf der Seite **Einzelvorgangserfassung** verfügbar. Richten Sie Ihre Auswahlen an den Auswahlen aus, die in der Spalte **Einzelvorgangsverwaltung** auf der Seite **Arbeitsplangruppen** vorgenommen werden. Wenn für die Arbeitsplangruppe die Option **Einzelorgangsverwaltung** ausgewählt, wird der Einzelvorgangstyp für den Produktionsauftrag als fertig gemeldet. Diese Meldung erfolgt, wenn der Einzelvorgang unter "Fertigungssteuerung" als fertig gemeldet wird. Wenn alle Einzelvorgangstypen, für die **Einzelvorgangsverwaltung** ausgewählt ist, bei einem Arbeitsgang als fertig gemeldet wurden, meldet die "Fertigungssteuerung" den Arbeitsgang ebenfalls als fertig. **Hinweis:** Für einige Einzelvorgangstypen kann mittels Produktionserfassungen eine Meldung manuell erstellt werden. Wählen Sie in diesem Fall die **Einzelvorgangsverwaltung** für den Einzelvorgangstyp aus, aber wählen Sie nicht den Einzelvorgangstyp für die Erfassung auf der Registerkarte **Arbeitsgänge** auf der Seite **Produktionsauftragsstandards** aus.

## <a name="bom-consumption-and-picking-list-journals"></a>Stücklistenverbrauch und Kommissionierlistenerfassungen
Materialien können so eingerichtet werden, dass sie entweder automatisch oder manuell während der Produktion verbraucht werden. Die Soll=Istrückmeldung wird durch das Prinzip für automatischen Artikelverbrauch bestimmt, das auf den Stücklistenpositionen eingerichtet wird, sowie durch die Einstellung des Felds **Soll=Istrückmeldung Material** in den Produktionsauftragsstandards. Soll=Istrückmeldung kann so eingerichtet werden, dass sie erfolgt, wenn ein Produktionsauftrag gestartet oder als fertig gemeldet wird. Alternativ kann sie auf der Einzelvorgangebene auftreten, wenn ein Einzelvorgang gestartet oder abgeschlossen wird.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Materialverbrauch steuern, wenn ein Produktionsauftrag gestartet wird

Materialverbrauch während des Starts eines Produktionsauftrags wird durch das Feld **Soll=Istrückmeldung Material** auf der Registerkarte **Start** gesteuert. Folgende Werte sind verfügbar:

-   **Prinzip für automatischen Artikelverbrauch** – Wenn ein Produktionsauftrag gestartet wird, werden Materialmengen gemäß dem Prinzip für automatischen Artikelverbrauch verbraucht, das auf den Produktions-Stücklistenpositionen festgelegt wird. Nur Materialpositionen, bei denen das Prinzip für automatischen Artikelverbrauch auf **Start** festgelegt ist, werden während des Produktionsanfangs verbraucht.
-   **Immer** – Materialmengen, die im Verhältnis zur gestarteten Menge stehen, werden immer verbraucht.
-   **Nie** – Materialmengen werden nie verbraucht.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Materialverbrauch steuern, wenn ein Produktionseinzelvorgang gestartet oder abgeschlossen wird

Materialverbrauch während des Starts oder des Abschlusses eines Produktionseinzelvorgangs wird durch das Feld **Soll=Istrückmeldung Material** auf der Registerkarte **Arbeitsgänge** gesteuert. Folgende Werte sind verfügbar:

-   **Prinzip für automatischen Artikelverbrauch** – Wenn eine Menge in einem Produktionseinzelvorgang gestartet oder abgeschlossen wird, werden Materialmengen gemäß dem Prinzip für automatischen Artikelverbrauch verbraucht, das auf den Produktions-Stücklistenpositionen festgelegt wird. Nur Materialpositionen, bei denen das Prinzip für automatischen Artikelverbrauch auf **Start** oder **Fertig stellen** festgelegt ist, werden verbraucht.
-   **Immer** – Materialmengen, die im Verhältnis zur gestarteten Menge beim Einzelvorgang stehen, werden immer verbraucht.
-   **Nie** – Materialmengen werden nie verbraucht.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Materialverbrauch steuern, wenn ein Produktionsauftrag als fertig gemeldet wird

Materialverbrauch während des Prozesses "Fertigmeldung" für einen Produktionsauftrag wird durch das Feld **Soll=Istrückmeldung Material** auf der Registerkarte **Fertigmeldung** gesteuert. Folgende Werte sind verfügbar:

-   **Prinzip für automatischen Artikelverbrauch** – Wenn ein Produktionsauftrag als fertig gemeldet wird, werden Materialmengen gemäß dem Prinzip für automatischen Artikelverbrauch verbraucht, das auf den Produktions-Stücklistenpositionen festgelegt wird. Nur Materialpositionen, bei denen das Prinzip für automatischen Artikelverbrauch auf **Fertig stellen** festgelegt ist, werden verbraucht.
-   **Immer** – Materialmengen, die im Verhältnis zur Menge stehen, die als fertig gemeldet wird, werden immer verbraucht.
-   **Nie** – Materialmengen werden nie verbraucht.





