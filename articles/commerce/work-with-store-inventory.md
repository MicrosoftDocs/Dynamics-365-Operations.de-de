---
title: Bestandsverwaltung im Laden
description: Dieser Artikel beschreibt die Dokumentarten, die Sie zum Verwalten des Bestands verwenden können.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 3f7f228bbf312a2ccdc96d3e95287898bee01de4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022619"
---
# <a name="store-inventory-management"></a>Bestandsverwaltung im Laden

[!include [banner](includes/banner.md)]

Bei der Arbeit mit dem Bestand in Dynamics 365 Commerce und der Verwendung der POS-Anwendung ist zu beachten, dass der POS nur begrenzte Unterstützung für Bestandsdimensionen und bestimmte Bestandsartikelarten bietet.

Die POS-Lösung unterstützt die folgenden Artikelkonfigurationen nicht:

- Stücklistenpositionen (außer Kitprodukten, die einige Komponenten des Stücklistenrahmens verwenden)
- Artikelgewichtsartikel
- Chargengesteuerte Artikel

Die POS-Anwendung unterstützt derzeit die folgenden Tracking-Dimensionen am POS nicht:

- Dimension der Chargenverfolgung
- Eigentümerdimension

Die POS-Lösung bietet begrenzte Unterstützung für die folgenden Dimensionen. Eingeschränkte Unterstützung deutet darauf hin, dass der POS einige dieser Dimensionen automatisch in Bestandstransaktionen einbinden kann, basierend auf der Konfiguration von Lager/Geschäft. POS unterstützt die Dimensionen nicht vollständig in der Art und Weise, wie sie unterstützt werden, wenn ein Verkaufsvorgang manuell in das ERP eingegeben wird. 

- **Lagerortstandort** – Benutzer können den Standort des empfangenden Lagerorts für Artikel nicht verwalten, die für einen Filiallagerort eingehen, wenn die Filiale nicht so konfiguriert wurde, dass der Lagerortverwaltungsprozess verwendet wird. Ein Standardstandort für den Empfang, der im Filiallagerort definiert wird, wird für diese Artikel verwendet. Wenn der Lagerortverwaltungsprozess für die Filiale aktiviert wurde, wird begrenzter Unterstützung ausgelöst, der den Benutzer auffordert, einen Empfangsstandort für den gesamten Eingang auswählen. Artikel, die von der Filiale verkauft werden, werden immer aus dem Standardstandort verkauft, wie bei der Einrichtung des Filiallagerorts definiert. Der Standort zum Verwalten des Rückholbestands kann nach über die Definition des Standardrücklieferungsstandort im Filiallagerort oder auf Grundlage von den in der Rückholstandortrichtlinie definierten Rückholursachencodes gesteuert werden.
- **Ladungsträger** – Ladungsträger gelten nur, wenn **Prozess der Lagerverwaltung verwenden** für den Artikel und den Filiallagerort aktiviert wurde. Im POS: wenn Bestand in einen Filiallagerort eingeht, in dem der Lagerortverwaltungsprozess aktiviert wurde, und der Standort, der für den Empfang der Artikel ausgewählt wurde, mit einen Lagerplatzprofil verknüpft ist, für das Kennzeichensteuerung erforderlich, wendet die POS-Anwendung systematisch ein Kennzeichen für die empfangende Position an. Benutzer im POS können diese Kennzeichendaten nicht ändern oder verwalten. Wenn die vollständige Verwaltung von Kennzeichen erforderlich ist, sollte die Filiale die mobile WMS-Anwendung oder den Backoffice-ERP-Client verwenden, um den Eingang dieser Artikel zu verwalten.
- **Seriennummer** – Die POS-Anwendung hat begrenzte Unterstützung für die Registrierung einzelner Seriennummern in einer Transaktionsverkaufsposition für Aufträge, die in POS mit serialisierten Artikeln erstellt werden. Die Seriennummer wird nicht gegen registrierte Seriennummern geprüft, die bereits im Bestand sind. Wenn ein Auftrag in Callcenterkanal erstellt oder durch das ERP erfüllt wird und während des Erfüllungsprozesses im ERP mehrere Seriennummern für eine einzelne Auftragsverkaufsposition erfasst werden, können diese Seriennummern nicht angewendet oder geprüft werden, wenn eine Rücklieferung im POS für diese Aufträge verarbeitet wird.
- **Bestandstatus** – Für Artikel, die den Lagerortverwaltungsprozess verwenden und einen Bestandsstatus benötigen, kann dieses Statusfeld nicht durch die POS-Anwendung festgelegt oder geändert werden. Der wie in der Filiallagerortkonfiguration definierte Standardbestandsstatus wird verwendet, wenn Artikel im Bestand entgegengenommen werden.

> [!NOTE]
> Alle Unternehmen müssen Artikelkonfigurationen über den POS in Entwicklungs- oder Testumgebungen testen, bevor sie in der Produktion eingesetzt werden können. Testen Sie Ihre Artikel, indem Sie regelmäßige Cash and Carry-Verkaufstransaktionen durchführen und Kundenaufträge (falls vorhanden) über die POS mit Ihren Artikeln erstellen. Das Testen muss die Durchführung eines vollständigen Buchungsprozesses in Ihrer Testumgebung und die Überprüfung, ob es keine Probleme gibt, beinhalten.
>
> Wenn Sie Artikel ohne ordnungsgemäße Tests so konfigurieren, dass sie nicht von der POS-Anwendung unterstützt werden, kann dies dazu führen, dass Ihr Prozess der Rechnungsbuchung in der Produktion fehlschlägt, ohne dass Sie die Probleme einfach beheben können. Partner- oder Kundenanpassungen an die Anwendung können optional in Betracht gezogen werden, damit diese Buchungsprozesse erfolgreich abgeschlossen werden können. Wenn keine Anpassungen erforderlich sind, muss das Unternehmen sicherstellen, dass die Produktkonfiguration Ihrer Produkte in einer Weise erfolgt ist, die vom Standard-POS-Anwendungs-/Auftragserstellungs-/Anlagenbuchungsprozess unterstützt wird.

## <a name="purchase-orders"></a>Bestellungen

Bestellungen werden in der Zentrale erstellt. Wenn ein Lagerort im Bestellkopf enthalten ist, kann der Auftrag im Shop mithilfe von Modern POS (MPOS) oder Cloud POS durch die Operation **Entnahme-/Empfangskennung** empfangen werden. Nachdem die in der Filiale eingehenden Mengen im Feld **Aktuelle Lieferung** im POS für das Bestellungsdokument eingegeben wurden, können sie lokal gespeichert oder zugesagt werden. Das lokale Speichern dieser Daten hat keine Auswirkungen auf den Lagerbestand. Es sollte nur gespeichert werden, wenn der Benutzer nicht bereit ist, den Empfang in der Hauptniederlassung zu buchen und nur eine Möglichkeit benötigt, die zuvor eingegebenen **Aktuelle Lieferung**-Daten vorübergehend zu speichern. Dies speichert die Daten der aktuellen Lieferung lokal auf der Kanaldatenbank des Benutzers. Nachdem das Dokument mit der Option **Zusagen** verarbeitet wurde, werden die **Aktuelle Lieferung**-Daten an die Hauptniederlassung gesendet und der Bestellungszugang wird gebucht. 

## <a name="transfer-orders"></a>Umlagerungsaufträge

Mit einem Umlagerungsauftrag kann angegeben werden, dass eine bestimmte Filiale der Standort ist, von dem Artikel versendet werden können, oder der Standort, an dem der Bestand eingeht. Wenn der POS-Benutzer der Versandlagerort für einen Umlagerungsauftrag ist, kann er **Jetzt liefern**-Mengen aus POS eingeben. Die Daten, die durch die Versandfiliale eingegeben werden, können lokal gespeichert oder zugesagt werden. Bei lokaler Speicherung werden keine Aktualisierungen des Umlagerungsauftragsdokuments in der Hauptniederlassung vorgenommen. Es sollte nur gespeichert werden, wenn der Benutzer nicht bereit ist, die Lieferung in der Hauptniederlassung zu buchen und eine Möglichkeit benötigt, die zuvor eingegebenen **Jetzt liefern**-Daten vorübergehend zu speichern. Nachdem die Filiale bereit ist, die Lieferung zu bestätigen, sollte die Option **Zusagen** ausgewählt werden. Dadurch wird die Lieferung der Umlagerungsauftrags in der Hauptniederlassung gebucht, sodass das empfangenden Lagerort nun für den Empfang bereit ist. 

Wenn der POS-Benutzer der Empfangslagerort für einen Umlagerungsauftrag ist, kann er **Aktuelle Lieferung**-Mengen aus POS eingeben. Die Daten, die durch die Empfangsfiliale eingegeben werden, können lokal gespeichert oder zugesagt werden. Es sollte nur gespeichert werden, wenn der Benutzer nicht bereit ist, den Empfang in der Hauptniederlassung zu buchen und eine Möglichkeit benötigt, die zuvor eingegebenen **Aktuelle Lieferung**-Daten vorübergehend zu speichern. Dies speichert die Daten der aktuellen Lieferung lokal auf der Kanaldatenbank des Benutzers. Nachdem das Dokument mit der Option **Zusagen** verarbeitet wurde, werden die **Aktuelle Lieferung**-Daten an die Hauptniederlassung gesendet und der Umlagerungsauftrag wird gebucht. Beachten Sie unbedingt, dass die empfangende Filiale darauf beschränkt wird, nur Eingangsmengen zuzusagen, die gleich oder kleiner der gelieferten Mengen sind. Ein Versuch, Mengen für einen Umlagerungsauftrag zu empfangen, die zuvor nicht versendet wurden, ergibt Fehler und der Zugang wird in der Hauptniederlassung nicht bestätigt.

## <a name="stock-counts"></a>Bestandsmengen

Bestandsmengen können entweder geplant oder ungeplant sein. Geplante Bestandszählungen werden in der Zentrale veranlasst, die die zu zählenden Artikel vorgibt. Von der Zentrale wird ein Inventurdokument erstellt, das im Shop empfangen werden kann und in dem die tatsächlich verfügbaren Mengen in MPOS oder Cloud POS eingegeben werden. Ungeplante Bestandsmengen werden in einem Shop initiiert, und die Mengen des tatsächlich verfügbaren Lagerbestands werden in MPOS oder Cloud POS aktualisiert. Im Gegensatz zu geplanten Bestandsmengen haben ungeplante Bestandsmengen keine vordefinierte Liste mit Artikeln. Wenn eine Bestandsmenge eines beliebigen Typs abgeschlossen wurde, wird sie kommissioniert und an die Zentrale gesendet. In der Zentrale wird die Anzahl als getrennter Schritt geprüft und gebucht.

## <a name="inventory-lookup"></a>Bestandsuche

Die aktuelle Produktmenge für Mehrfachshops und Lagerorte kann auf der **Bestandssuchen**-Seite angezeigt werden. Neben der aktuellen verfügbaren Menge können auch künftige Verfügbarkeitszusagen-Mengen (ATP) für jede einzelne Filiale angezeigt werden. Klicken Sie hierfür auf die Filiale, für die Sie die VfZ für anzeigen möchten, und klicken Sie auf **Verfügbarkeit in Filiale anzeigen**.
