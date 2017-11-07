---
title: "Terminierungsoptionen für Operations"
description: "In diesem Thema werden die Optionen für die Grobterminierung beschrieben. Diese Grobplanung wird häufig verwendet, wenn eine allgemeine Schätzung der Dauer des Produktionsprozesses benötigt wird."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5a64445b58c3d6b523b766b4e864aeea9f93de2b
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---

# <a name="operations-scheduling-options"></a>Terminierungsoptionen für Operations

[!include[banner](../includes/banner.md)]


In diesem Thema werden die Optionen für die Grobterminierung beschrieben. Diese Grobplanung wird häufig verwendet, wenn eine allgemeine Schätzung der Dauer des Produktionsprozesses benötigt wird.

Die Grobterminierung stellt den voraussichtlichen Zeitplan für einen Produktionsauftrag dar:

-   Start- und Enddatum werden für den Produktionsauftrag und jeden Arbeitsgang festgelegtö.
-   Ressourcen werden den Arbeitsgängen zugewiesen.

Anhand verschiedener Einstellungen kann die Berechnung von Produktionsplänen bestimmt werden. Sie definieren diese Einstellungen auf der Seite **Grobterminierung**. Nachfolgend werden Planungsoptionen erläutert.

## <a name="operations-scheduling"></a>Grobterminierung
### <a name="scheduling-direction"></a>Planungsrichtung

Die Planungsrichtung ist eine Grundlage für den Planungsvorgang. Die Produktion kann je nach Zeit- und Planungsanforderungen ab einem beliebigen Datum vorwärts oder rückwärts geplant werden.

-   **Vorwärts ab Planungsdatum** – Die Produktion wird so geplant, dass sie so früh wie möglich beginnt. Die Produktion kann heute, morgen oder ab einem beliebigen Datum in der Zukunft beginnen. Die Produktion wird so geplant, dass sie am frühestmöglichen Datum beginnt und zum frühestmöglichen Enddatum abgeschlossen werden kann.
-   **Rückwärts ab Planungsdatum** – Die Produktion wird so geplant, dass sie so spät wie möglich beginnt. Dabei ist das Datum maßgeblich, an dem die Produktion abgeschlossen sein muss. Von diesem Datum ausgehend wird bis zum spätestmöglichen Datum zurückgerechnet, an dem die Produktion beginnen kann, ohne die gesetzte Frist zu gefährden.

Die folgenden Optionen sind verfügbar:

-   **Vorwärts ab heute**– Die Terminierung erfolgt vorwärts ab dem aktuellen Datum. (Das aktuelle Datum ist das Systemdatum.)
-   **Vorwärts ab dem geplanten Start** – Die Terminierung erfolgt vorwärts ab einem früheren Startdatum. Wenn keine frühere Terminierung vorliegt, wird das Enddatum auf das aktuelle Datum festgelegt.
-   **Vorwärts ab Planungsdatum**– Die Terminierung erfolgt ab dem Datum, das im Feld **Geplantes Datum** angegebenen ist. Wenn Sie kein Planungsdatum angeben, erfolgt die Terminierung vorwärts ab dem aktuellen Datum.
-   **Rückwärts ab Lieferdatum** – Die Terminierung erfolgt rückwärts ab dem Lieferdatum, das für den Produktionsauftrag angegeben ist. Bei Auswahl dieser Planungsoption ohne Angabe eines Lieferdatums wird das Lieferdatum auf das aktuelle Datum festgelegt.
-   **Rückwärts ab geplantem Ende** – Die Terminierung erfolgt rückwärts ab einem zuvor berechneten Enddatum. Wenn keine frühere Terminierung vorliegt, wird das Enddatum auf das aktuelle Datum festgelegt.
-   **Rückwärts ab Planungsdatum**– Die Terminierung erfolgt rückwärts ab dem Datum, das im Feld **Geplantes Datum** angegebenen ist. Wenn Sie kein Planungsdatum angeben, wird das aktuelle Datum verwendet. Rückwärts ab Aktivitätsdatum wird für den Produktionsauftrag bei der letzten Produktprogrammplanung berechnet. Wenn kein Aktivitätsdatum für den Produktionsauftrag angegeben ist, wird dieses auf das aktuelle Systemdatum festgelegt.
-   **Rückwärts ab Verfügbarkeitsdatum** – Die Terminierung erfolgt rückwärts ab dem Verfügbarkeitsdatum, das für den Produktionsauftrag bei der letzten Produktprogrammplanung berechnet wurde. Wenn kein Datum in der Zukunft für den Produktionsauftrag angegeben ist, wird dieses auf das aktuelle Systemdatum festgelegt.
-   **Laut letzter Planung** – Im Zusammenhang mit der Grobterminierung und der Feinterminierung werden die ausgewählte Planungsrichtung und das Datum gespeichert. Sie können diese Option für nachfolgende Terminierungen auswählen. Liegt keine vorherige Planung des Produktionsauftrags vor, läuft die Planung rückwärts ab dem aktuellen Systemdatum.
-   **Vorwärts ab morgen** – Die Terminierung erfolgt vorwärts ab dem aktuellen Datum plus ein Tag.
-   **Vorwärts ab vorherigem Einzelvorgang** – Diese Funktion ist nur in der Feinterminierung von Bedeutung. Wenn Sie diese Planungsrichtung für die Grobterminierung auswählen, wird der Produktionsauftrag vorwärts ab dem aktuellen Datum geplant. Bei der Feinterminierung wird die Planung für einen Einzelvorgang aufgestellt, und alle anderen Einzelvorgänge für die Produktion werden entsprechend geplant.
-   **Rückwärts ab vorherigem Einzelvorgang** – Diese Funktion ist nur in der Feinterminierung von Bedeutung. Bei Auswahl dieser Planungsrichtung für die Grobterminierung werden Bestellvorschläge rückwärts ab dem aktuellen Datum terminiert. Bei der Feinterminierung wird die Planung für einen Einzelvorgang aufgestellt, und alle anderen Einzelvorgänge für die Produktion werden entsprechend geplant.

### <a name="scheduling-date"></a>Planungsdatum

Das Datum wird für die Planungsrichtung **Vorwärts ab Planungsdatum** und **Rückwärts ab Planungsdatum** verwendet. Die Terminierung erfolgt dann vorwärts oder rückwärts ab diesem Datum. Weitere Informationen finden Sie im vorherigen Abschnitt "Planungsrichtung".

### <a name="recalculate-bom-levels"></a>Stücklistenebenen neu berechnen

Wenn Sie**BOM-Ebenen neue berechnen** wählen, werden die ausgewählten Stücklistenebenen (BOM) neu berechnet, mit deren Hilfe die richtige Planungsreihenfolge sichergestellt wird.

## <a name="limitations"></a>Einschränkungen
### <a name="finite-capacity"></a>Begrenzte Kapazität

Die Planung hängt von der Verfügbarkeit der zum Abschluss der Produktion erforderlichen Ressourcen ab. Wenn die Kapazität nicht ausreicht, können Produktionsaufträge verzögert oder auch angehalten werden. Wenn begrenzte Kapazität auf die Grobplanung angewendet wird, werden vorhandene Kapazitätsreservierungen für die Ressourcen berücksichtigt und die jeweilige Kapazität als nicht verfügbar betrachtet. Der Produktionsauftrag wird gemäß der verfügbaren Kapazität der erforderlichen Ressourcen geplant. Bei der Grobterminierung wird anhand der angegebenen Abfolge der Arbeitsgänge die Reihenfolge der Arbeitsgänge im Produktionsarbeitsplan bestimmt. Die Kapazität für die Ressourcengruppen wird bei der Grobterminierung anhand der Arbeitszeit reserviert, die für den Produktionsarbeitsplan definiert ist. Die Kapazität der Ressourcengruppen ist die Summe der verfügbaren Kapazität aller Ressourcen in den Ressourcengruppen.

### <a name="finite-material"></a>Begrenztes Material

Die Planung hängt auch von der Verfügbarkeit des für die Produktion erforderlichen Materials ab. Nicht ausreichend verfügbare Komponenten können zu Produktionsverzögerungen führen. Die Planung kann auch auf der Materialverwendung basieren. Geben Sie einfach die Materialien an, die anstelle der Materialien für die Produktion verfügbar sein muss, die nicht wichtig sind. Diese Art der Planung wird als Planung mit begrenztem Material bezeichnet. Wenn Sie begrenztes Material angeben, basiert die Produktionsplanung auf der Verfügbarkeit des Materials. **Hinweis:** Wenn Sie Kapazität und Material optimieren, wird die Produktion entsprechend dieser beiden Beschränkungen berechnet. Die Verfügbarkeit von Kapazität und Material wird berücksichtigt, und die Arbeitsgänge des Produktionsauftrags können erst starten, wenn sowohl Kapazität als auch Material in den erforderlichen Mengen verfügbar sind. Aktivieren Sie dieses Kontrollkästchen, um anzugeben, ob das Material bei der Planung als begrenzt betrachtet werden soll. Sind die Materialien begrenzt, wird die Disposition des Materials für diesen Zeitraum berücksichtigt. Das bedeutet, dass bei der Planung die für die Artikel berechneten Verfügbarkeitsdaten berücksichtigt werden. Bei der Planung wird Rohmaterial reserviert, und die aktuelle Produktion wird aufgelöst. Werden mehrfach Planungen durchgeführt, werden nur bei der ersten Planung Aufschlüsselungen und Reservierungen vorgenommen. Wenn Sie Änderungen an der Produktionsstückliste oder am Arbeitsplan vornehmen, findet bei der nächsten Kapazitätsplanung eine Aufschlüsselung statt. Die Auflösung geht davon aus, dass das Material am selben Tag benötigt wird. Da die Produktion nicht zur selben Zeit wie die Produktprogrammplanung geplant wird, ist das aktuelle Datum die beste Schätzung des Zeitpunkts, ab dem die Artikel verfügbar sein werden. Anschließend wird überprüft, ob die Artikel verfügbar sind. Ist dies der Fall, kann der Produktionsbedarf erfüllt werden. Sind die Artikel nicht bis zum aktuellen Datum verfügbar, wird ein Bestellvorschlag generiert, und eine Ausgleichsauswahl für den Bestellvorschlag wird getroffen. Wenn die automatische Umwandlung für den Bestellvorschlag festgelegt wurde, wird der Bestellvorschlag automatisch für Einkauf oder Produktion umgewandelt. Der Produktionsstatus wechselt automatisch auf den Status, der im Feld im Feld **Erforderlicher Produktionsstatus** im Dialogfeld **Dispositionssteuergruppen** angegeben ist. Wenn das Kontrollkästchen deaktiviert ist, wird das Material immer als verfügbar betrachtet. Daher wird bei der Planung nicht berücksichtigt, ob die Materialien zum Zeitpunkt des Bedarfs verfügbar sind.

### <a name="finite-property"></a>Begrenzte Eigenschaft

Aktivieren Sie dieses Kontrollkästchen, damit die Feinterminierung sämtlichen Eigenschaftsbedarf berücksichtigen darf.

### <a name="keep-production-unit"></a>Produktionseinheit beibehalten

Wählen Sie diese Option aus, wenn das Planungsmodul nur Ressourcen planen soll, die bereits für die Produktionseinheit angegeben sind.

### <a name="keep-warehouse-from-resource"></a>Lagerort der Ressource beibehalten

Wählen Sie diese Option aus, wenn das Planungsmodul nur Ressourcen planen soll, die dem für die Ressource angegebenen Eingangslagerort zugeordnet sind.

## <a name="references"></a>Referenzen
### <a name="schedule-references"></a>Referenzen in Planung einbeziehen

Wenn Referenzen von Produktionsaufträgen abhängen, werden sie auch als Unterproduktionen bezeichnet. Unterproduktionen können im Rahmen eines Produktionsauftrags geplant werden. Aktivieren Sie dieses Kontrollkästchen, wenn die Planung von Unterproduktionen auf der Planung der Hauptproduktion basiert. Hinsichtlich der Hauptproduktion werden übergeordnete Produktionen vorwärts terminiert, und untergeordnete Produktionen werden rückwärts terminiert. Sie können Produktionsauftragsreferenzen im Feld **Referenzebenen** auf der Seite **Produktionsaufträge** anzeigen.

### <a name="synchronize-references"></a>Referenzierte Produktionen mitplanen

Sie können Referenzen auch mit dem Produktionsauftrag synchronisieren. Ist die entsprechende Option ausgewählt, wird das Datum der Unterproduktionen verschoben und bei Änderungen am Zeitplan des Produktionsauftrags angepasst. Bei Produktionsaufträgen mit mehreren Unterproduktionen sollten die Unterproduktionen zusammen mit der Hauptproduktion geplant werden. In diesem Fall kann die Hauptproduktion erst gestartet werden, wenn die zugehörigen Unterproduktionen abgeschlossen sind. Aktivieren Sie deshalb dieses Kontrollkästchen, wenn die Planung von Unterproduktionen auf den Start- und Endzeiten der ausgewählten Produktion basiert. Sie können diese Option nur auswählen, wenn die **Zeitplanreferenzoption** ebenfalls aktiviert wird.

## <a name="cancellation"></a>Aufhebung
### <a name="cancel-queue-time"></a>Wartezeiten vernachlässigen

Aktivieren Sie dieses Kontrollkästchen, um eine Position aus der Planung auszuschließen.

### <a name="cancel-setup"></a>Rüstzeiten vernachlässigen

Aktivieren Sie dieses Kontrollkästchen, um eine Zeit aus der Planung auszuschließen.

### <a name="cancel-process"></a>Bearbeitungszeiten vernachlässigen

Aktivieren Sie dieses Kontrollkästchen, um eine Laufzeit aus der Planung auszuschließen.

### <a name="cancel-overlap"></a>Überlappung vernachlässigen

Aktivieren Sie dieses Kontrollkästchen, um eine überschneidende Zeit aus der Planung auszuschließen.

### <a name="cancel-transport"></a>Transport stornieren

Aktivieren Sie dieses Kontrollkästchen, um eine Übergangszeit aus der Planung auszuschließen.

## <a name="set-default"></a>Als Standard festlegen
Sie können die aktuellen Werte als Standardwerte speichern. Es gibt zwei Optionen:

-   Als meinen Standard festlegen
-   Als Standard für jede Person festlegen


<a name="see-also"></a>Siehe auch
--------

[Grobterminierung](operations-scheduling.md)




