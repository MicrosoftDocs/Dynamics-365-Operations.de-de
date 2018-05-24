---
title: Lagerortverwaltung von Microsoft Dynamics AX 2012 auf Finance and Operations aktualisieren
description: "Dieses Thema bietet eine Übersicht über Optionen für die Produkt- und Lagerverwaltungsmigration."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0ff3a22b89ce22096198d2e1dd1ea9ed10239a9
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-finance-and-operations"></a>Lagerortverwaltung von Microsoft Dynamics AX 2012 auf Finance and Operations aktualisieren

[!include [banner](../includes/banner.md)]

Dieses Thema gibt einen Überblick über den Prozess des Upgrades von Microsoft Dynamics AX 2012 R3 mit dem WMSII-Modul auf Microsoft Dynamics 365 for Finance and Operations.

Finance and Operations unterstützt nicht mehr bestehende **WMSII**-Modul von Microsoft Dynamics AX 2012. Stattdessen können Sie das Modul **Lagerortverwaltung** verwenden. Im WMSII-Modul konnten die Bestandsdimensionen Standort und Paletten-ID für die Finanzbestandsaufnahme ausgewählt werden, jedoch kann die Bestandsdimension Paletten-ID nicht für die Finanzbestandsaufnahme im Bereich Finanzen und Betrieb verwendet werden.

Bei einem Upgrade werden alle Produkte, die einer Lagerdimensionsgruppe zugeordnet sind, die die Bestandsdimension Paletten-ID verwendet, identifiziert, als gesperrt gekennzeichnet und nicht zum Upgrade verarbeitet.

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>Aktualisierung auf Finance and Operations, wenn AX 2012 R3 WMSII verwendet wird
Nach dem Upgrade können Sie eine Reihe von Optionen in der Gruppe **Lagerdimension ändern für Positionen** Formular verwenden, um Produkte, die während des Upgrades gesperrt wurden, zu entsperren und dann Transaktionen für diese Produkte zu bearbeiten.

### <a name="enabling-items-in-finance-and-operations"></a>Artikel in Finance and Operations aktivieren
Diese Änderung ist erforderlich, da die Artikelverfolgung im Bereich Finanzen und Betrieb Teil der Lagerverwaltungsprozesse ist. Für diesen Prozess müssen alle Lagerorte und die Lagerplätze einem Lagerplatzprofil zugeordnet werden. Wenn Sie Lagerverwaltungsprozesse verwenden möchten, müssen Sie Folgendes konfigurieren:
-   Alle bestehenden Lagerorte müssen für Lagerortverwaltungsprozesse aktiviert werden 
-   Vorhandene freigegebene Produkte müssen einer Lagerdimensionsgruppe zugeordnet werden, die Lagerortverwaltungsprozesse verwendet. 

Wenn die Quelllagerdimensionsgruppen die Palettennummerlagerungsdimension verwenden, müssen die vorhandenen Standorte des verfügbaren Lagerbestands, die die Palettennummerlagerungsdimension verwenden, einem Lagerplatzprofil zugeordnet sein, in dem der Parameter **Nutzungslizenzplattennachverfolgung** ausgewählt wird. Wenn vorhandene Lagerorte nicht aktiviert werden, um Lagerortverwaltungsprozesse zu verwenden, können Sie Lagerdimensionsgruppen für verfügbaren Lagerbestand der vorhandenen Gruppen ändern, die nur die Standort-, Lagerort und Lagerplatz-Lagerungsdimensionen behandeln. 

> [!NOTE] 
>  Beachten Sie, dass Sie die Lagerdimensionsgruppe ändern können, auch wenn offenen Lagerbuchungen vorhanden sind.

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>Produkte finden, die wegen der Paletten-ID blockiert wurden
Um die Liste von freigegebenen Produkten anzuzeigen, die für die Aktualisierung nicht gesperrt wurden und verarbeitet werden können klicken Sie auf, &gt; **Lagerverwaltung** **Einstellungen** &gt; **Lager** &gt; **Artikel für Bestandsaktualisierungen gesperrt**.

## <a name="change-storage-dimension-group-for-blocked-products"></a>Lagerdimensionsgruppe für gesperrte Produkte ändern 
 
Um als Teil eines Lagerverwaltungsprozesses verwendet werden zu können, muss ein Artikel einer Lagerdimensionsgruppe zugeordnet sein, in der die Dimension Ortsinventur aktiv ist und der Parameter **Lagerverwaltungsprozesse verwenden** ausgewählt ist. Wenn diese Einstellungen aktiviert ist, werden der Standort, Lagerort, die Abfrage, Standort und Kennzeichnungsbestanddimension aktiv.

Um für Produkte die Sperrung aufzuheben die bei einer Aktualisierung möglicherweise gesperrt wurden, müssen Sie eine neue Lagerdimensionsgruppe für die Produkte auswählen. Beachten Sie, dass Sie die Lagerdimensionsgruppe ändern können, auch wenn offenen Lagerbuchungen vorhanden sind. Um Artikel zu verwenden, die bei einer Aktualisierung möglicherweise gesperrt wurden, haben Sie zwei Möglichkeiten:

-   Ändern Sie die Lagerdimensionsgruppe für den Artikel in eine Lagerdimensionsgruppe, die nur die Lagerort-, Standort-, und Standortbestanddimensionen verwendet. Infolge dieser Änderung wird die Palettennummerlagerungsdimension nicht mehr verwendet.
-   Ändern Sie die Lagerdimensionsgruppe für den Artikel in eine Lagerdimensionsgruppe, die nur die Lagerort-, Standort-, und Standortbestanddimensionen verwendet. Infolge dieser Änderung wird jetzt die Palettennummerlagerungsdimension verwendet.

## <a name="configure-warehouse-management-processes"></a>Lagerortverwaltungsprozesse konfigurieren
Bevor Sie freigegebene Produkte im Modul **Lagerortverwaltung** verwenden können, müssen die Produkte eine Lagerdimensionsgruppe verwenden, wobei **Verwendungslagerortverwaltungsprozesse** der Parameter ausgewählt wird.

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>Alle bestehenden Lagerorte müssen für Lagerortverwaltungsprozesse aktiviert werden.

1.  Erstellen Sie mindestens ein neues Lagerplatzprofil.
2.  Klicken Sie auf **Lagerortverwaltung** &gt; **Einstellungen** &gt; **Aktivieren Sie Lagerortverwaltungsprozesse** &gt; **Aktivieren Sie Lagerorteinstellungen**.
3.  Auf der Seite **Aktivieren Sie Lagerorteinstellungen** können Sie die Lagerorte hinzufügen, die aktiviert werden sollen. Sie können dieses Schritts entweder direkt auf der Seite ausführen oder indem Sie die Microsoft Office-Integration verwenden.
4.  Zuweisen eines Lagerplatzprofil an sämtliche Standorte. Sie können dieses Schritts entweder direkt auf der Seite ausführen oder indem Sie die Microsoft Office-Integration verwenden. Sie können entweder die Daten exportieren und importieren, oder verwenden Sie die Datenentität, die die unter [Datenverwaltung](../../dev-itpro/data-entities/data-entities.md) ausgeführt wird.
5.  Überprüfen Sie die vorgeschlagenen Änderungen. Als Teil des Validierungsprozesses treten verschiedene Prüfungen der Datenintegrität auf. Als Teil eines längeren Aktualisierungsprozesses können möglicherweise Probleme auftreten, die auf der Quellimplementierung angepasst werden müssen. In diesem Fall ist eine zusätzliche Datenaktualisierung erforderlich.
6.  Änderung verarbeiten.

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>Der Artikel ist einer Lagerdimensionsgruppe zugeordnet, die Lagerortverwaltungsprozesse verwendet

1.  Erstellen Sie einen neuen Wert **Lagerstatus**, und weisen Sie diesen als der Wert **Kennung Standardbestandsstatus** in den Formularen **Lagerverwaltungsparameter** Einstellungen zu.
2.  Erstellen Sie eine neue Lagerdimensionsgruppe, in der der Parameter ausgewählt wurde. **Verwenden Sie Lagerortverwaltungsprozesse**.
3.  Auf der Seite **Reservierungshierarchie** können Sie eine neue Reservierungshierarchie entsprechend der Rückverfolgungsangabengruppe des Artikels definieren.
4.  Erstellen Sie eine oder mehrere Einheitsnummernkreisgruppen, die mindestens die gleichen Einheiten enthalten, für die die Lagereinheiten der Artikel verwendet werden.
5.  Klicken Sie auf **Lagerortverwaltung** &gt; **Einstellungen** &gt; **Aktivieren Sie Lagerortverwaltungsprozesse** &gt; **Ändern Sie Lagerdimensionsgruppe für Artikel**.
6.  Auf der Seite **Ändern Sie Lagerdimensionsgruppe für Artikel** können Sie die die Artikelnummern, Lagerdimensionsgruppen und die Einheitnummernkreisgruppen hinzufügen. Sie können dieses Schritts direkt auf der Seite ausführen, indem Sie die Microsoft Office-Integration verwenden oder indem Sie in den Datenentitätsprozess [Datenverwaltung](../../dev-itpro/data-entities/data-entities.md) verwenden.
7.  Überprüfen Sie die vorgeschlagenen Änderungen. Als Teil des Validierungsprozesses treten verschiedene Prüfungen der Datenintegrität auf. Als Teil eines längeren Aktualisierungsprozesses können möglicherweise Probleme auftreten, die auf der Quellimplementierung angepasst werden müssen. In diesem Fall ist eine zusätzliche Datenaktualisierung erforderlich.
8.  Änderung verarbeiten. Eine Aktualisierung aller Lagerungsdimensionen kann einige Zeit in Anspruch nehmen. Sie können den Fortschritt überwachen, indem Sie die Stapelverarbeitungsauftragaufgaben verwenden.

