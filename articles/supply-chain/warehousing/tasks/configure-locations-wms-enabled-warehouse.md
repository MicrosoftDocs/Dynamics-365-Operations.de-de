--- 
title: "Lagerplätze an einem für WMS aktivierten Lagerort konfigurieren"
description: "Dieses Handbuch zeigt Ihnen an, wie die Lagerplatzeinstellung für einen neuen WMS-aktivierten Lagerort konfiguriert (ein Lagerort, den Verwendung Lagerortverwaltungsprozesse Erweiterter)."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1082c86361180db84bb2b5c0b8158816f76a219e
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Lagerplätze an einem für WMS aktivierten Lagerort konfigurieren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Dieses Handbuch zeigt Ihnen an, wie die Lagerplatzeinstellung für einen neuen WMS-aktivierten Lagerort konfiguriert (ein Lagerort, den Verwendung Lagerortverwaltungsprozesse Erweiterter). Der Prozess wird normalerweise von einer Lagerortverwaltung erfolgt. Sie können diese Prozedur im Demodatenunternehmen USMF oder für Ihre eigenen Daten ausführen. Eine Vorbedingung ist, dass Sie mindestens einen Standort konfiguriert.


## <a name="create-a-new-warehouse"></a>Erstellt einen neuen Lagerort.
1. Gehen Sie zu Lagerorte.
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Lagerort" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Standort" einen Wert ein.
6. Erweitern oder reduzieren Sie den Abschnitt Lagerort.
7. Setzen Sie die Option "Benutzerfehlerprotokoll für Lagerortverwaltungsprozesse verwenden" auf Ja.
    * Bei dieser Einstellung können Sie, um erweiterte Warehousing-Prozesse mithilfe der Lagerort arbeit und -mobiler Geräte auszuführen.  
8. Schließen Sie die Seite.

## <a name="define-a-location-format"></a>Lagerplatzformatdetail erstellen
1. Gehen Sie zu Lagerplatzformate.
    * Lagerplatzformate sind ein Benennungssystem, das verwendet wird, um die eindeutige und konsistenten Namen für die verschiedenen Lagerplatzlagerfachpositionen zu erstellen, die innerhalb eines Lagerorts verwendet werden. Es kann hilfreich sein, Trennzeichen als Teil des Lagerplatzformats zu verwenden, um es zu vereinfachen, Komponenten des Lagerplatzes wie der Gang in zu identifizieren eingegeben werden. In diesem Beispiel erstellen Sie einen Namen mit vier Komponenten. So können diese Gang, Regal, Regalboden und Lagerfach sein.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Format Standort" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Geben Sie im Feld "Beschreibung Segment" einen Wert ein.
    * Diese bezeichnet, was die erste Komponente des Lagerplatznamens darstellt. Beispielsweise kann es Gang sein.  
6. Geben Sie im Feld Länge eine Zahl ein.
    * Dadurch wird festgelegt, wie viele Zeichen der Teil des Lagerplatznamens besitzen muss. Beachten Sie, dass die Summe aller Komponenten im Auftrag, einschließlich Trennzeichen, 10 Zeichen nicht überschreiten.  
7. Geben Sie im Feld Trenner einen Wert ein.
    * Dies bestimmt, welches Zeichen oder Symbol zwischen dem ersten und zweiten Komponente des Namens verwendet wird.  
8. Klicken Sie auf "Neu".
9. Geben Sie im Feld "Beschreibung Segment" einen Wert ein.
10. Geben Sie im Feld Länge eine Zahl ein.
11. Geben Sie im Feld Trenner einen Wert ein.
12. Klicken Sie auf Neu.
13. Geben Sie im Feld "Beschreibung Segment" einen Wert ein.
14. Geben Sie im Feld Länge eine Zahl ein.
15. Geben Sie im Feld Trenner einen Wert ein.
16. Klicken Sie auf Neu.
17. Geben Sie im Feld "Beschreibung Segment" einen Wert ein.
18. Geben Sie im Feld Länge eine Zahl ein.
19. Klicken Sie auf "Speichern".
20. Schließen Sie die Seite.

## <a name="define-location-types"></a>Lagerort-Typen definieren
1. Gehen Sie zu Lagerplatztypen.
    * Lagerplatztypen können als Filteroptionen verwendet werden, die verschiedenen Lagerortverwaltungsprozesse zu steuern. Als Minimum müssen Sie Staging und abschließende Versandorttypen erstellen, um den ausgehenden Lagerortverwaltungsprozess zu definieren.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Typ Standort" einen Wert ein.
4. Geben Sie im Feld "Beschreibung" einen Wert ein.
5. Schließen Sie die Seite.

## <a name="define-location-profile"></a>Lagerortprofile definieren
1. Lagerplatzprofile anzeigen
    * Die Definition von Lagerplatzprofilen ist äußerst wichtig. Die gruppierte Lagerplatzkapazität kann hier gesteuert werden sowie die Richtlinien, die zugeordnet werden, bis zu dem Lager untergebracht abruft und wie Zinsen gespeichert wird. Lagerplatzprofile können als Filteroptionen verwendet werden, die verschiedenen Lagerortverwaltungsprozesse zu steuern. Als Minimum müssen Sie ein Benutzerlagerplatzprofil erstellen, um die Lagerortverwaltungsprozesse zu aktivieren.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.
4. Geben Sie im Feld "Name" einen Wert ein.
5. Klicken Sie im Feld "Format Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld Typ Lagerort auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Aktivieren bzw. deaktivieren Sie das Kontrollkästchen Gemischten Bestandstatus zulassen.
    * Aktivieren Sie diese Option, wenn Sie Mischbestandsstatuswerte an Lagerplätzen zulässig sein soll, die von dieses Lagerplatzprofil gruppiert werden.  
12. Aktivieren bzw. deaktivieren Sie das Kontrollkästen Regeln für Chargentage überschreiben.
    * Aktivieren Sie diese Option, zu überschreiben die Regel für wie viele Tage, die Bestandschargenablaufdaten variieren können, Mixing von Lagerchargen zuzulassen, die diese Schritte Regel nicht, befolgend.  
13. Aktivieren oder deaktivieren Sie das Kontrollkästchen Zykluszählung zulassen
    * Aktivieren Sie diese Option, wenn Verarbeitung von Zykluszählung an allen Lagerplätzen zulässig sein soll, die von dieses Lagerplatzprofil gruppiert werden.  
14. Erweitern oder reduzieren Sie den Abschnitt Dimension.
    * Die Registerkarte "Dimension" ermöglicht es Ihnen, um Parameter und Methoden zu definieren, um genauere Berechnungen der Tragfähigkeit innerhalb jedes der Lagerplätze zu aktivieren.  
15. Schließen Sie die Seite.

## <a name="enable-warehouse-management-parameters"></a>Lagerortverwaltungsparameter importieren ermöglichen
1. Lagerort-Verwaltungsparameter anzeigen
    * Damit Lagerortarbeit zu verarbeiten, müssen Parameter für den Benutzer festgelegt werden, Ort den Staginglagerplatztyp das Profil ein, und die endgültige Versandorttyp Sobald die ausgehenden Prozessenden endgültigen am Versandort eingeben dass Sie definieren, die zugehörigen ausgehenden Buchungen wird "entnommen" aktualisiert.  
2. Erweitern oder reduzieren Sie den Abschnitt Lagerplatzprofile.
3. Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Erweitern oder reduzieren Sie den Abschnitt Lagerplatztypen.
6. Klicken Sie im Feld Typ Lagerort auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld Typ Endkunden-Zustellung auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
10. Schließen Sie die Seite.

## <a name="define-warehouse-zone-groups"></a>Lagerortzonengruppen definieren
1. Lagerortzonengruppen
    * Lagerportzonen können als Filter verwendet werden, die verschiedenen Lagerortverwaltungsprozesse zu steuern. Sie müssen eine Zonengruppe erstellen, bevor Sie eine Zone definieren können.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Zonen-Gruppe-ID" einen Wert ein.
4. Geben Sie im Feld "Zonen-Gruppe-ID" einen Wert ein.
5. Schließen Sie die Seite.

## <a name="define-warehouse-zones"></a>Lagerortzonen definieren
1. Gehe zu Zone
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Zonen-Gruppe-ID" einen Wert ein.
4. Geben Sie im Feld "Zonen-Gruppe-ID" einen Wert ein.
5. Klicken Sie im Feld Zonen-Gruppe-ID auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Schließen Sie die Seite.

## <a name="create-locations-using-the-location-setup-wizard"></a>Erstellen von Lagerplätzen mithilfe des Lagerplatz-Setup-Assistenten
1. Lagerplatz-Setup-Assistent
2. Klicken Sie im Feld "Lagerort" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
3. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
4. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
5. Klicken Sie im Feld Zonen-Gruppe-ID auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
7. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
8. Klicken Sie im Feld "Profilkennung" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
9. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
10. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
11. Markieren Sie in der Liste die ausgewählte Zeile.
12. Geben Sie im Feld "Portnummer" eine Zahl ein.
    * Von der Anzahl und zu den Nummernfeldern definieren Sie, wieviele Lagerplätze erstellt werden. Beispielsweise beim Festlegen von der Anzahl bis 1 und bis 3 für alle vier Positionen im Lagerplatzformat zu nummerieren, 81 Lagerplätze erstellt werden (3x3x3x3).  
13. Geben Sie im Feld "Portnummer" eine Zahl ein.
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
15. Geben Sie im Feld "Portnummer" eine Zahl ein.
16. Geben Sie im Feld "Portnummer" eine Zahl ein.
17. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
18. Geben Sie im Feld "Portnummer" eine Zahl ein.
19. Geben Sie im Feld "Portnummer" eine Zahl ein.
20. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
21. Geben Sie im Feld "Portnummer" eine Zahl ein.
22. Geben Sie im Feld "Portnummer" eine Zahl ein.
23. Klicken Sie auf "Erstellen".

## <a name="create-locations-manually"></a>Lagerort manuell erstellen
1. Zu Lagerplatz gehen
    * Manuell kann Erstellung von Lagerplätzen innerhalb eines Lagerorts leicht ausgeführt werden. Der Lagerplatzname und die Lagerplatzprofil Kennung ist erforderliche Werte.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Lagerort" einen Wert ein.
4. Geben Sie im Feld Standort einen Wert ein.
    * Beachten Sie, dass Sie einen neuen Lagerplatz hier erstellen, müssen Sie einen neuen eindeutigen Namen eingeben, anstatt, ein vorhandenes ausgewählt wird.  
5. Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.
6. Schließen Sie die Seite.

## <a name="define-pack-size-categories"></a>Verpackungsgrößenkategorien definieren
1. Verpackungsgrößenkategorien anzeigen
    * Packmaßkategorien können zu den gesamten verwendet werden, die ähnlichen physischen Komprimierungsgrößen haben. In diesem Beispiel wird die Packmaßkategorie verwendet, um die Kapazität an den Entnahmeorten innerhalb einer bestimmten Zone des Lagerorts zu steuern. Beachten Sie in, dass die Packmaßkategorie Kennung des freigegebenen Produkts zugewiesen werden muss der Entität, um als Teil des Strumpfgrenzenverarbeitens verwendet werden.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Verpackungsgrößenkategorie-ID" einen Wert ein.
4. Geben Sie in Feld "Verpackungs-Namen-Kategorie" einen Wert ein.
5. Schließen Sie die Seite.

## <a name="define-location-stocking-limits"></a>Lagergrenzen für Lagerplatz festlegen
1. Lagerplatzbeschränkungen anzeigen
    * Lagerplatzstrumpfgrenzen unterstützen, zu überprüfen, ob Arbeit nicht erstellt wird, die in einen Lagerplatz angeordnet werden Bestand anzufordern um diesen, der nicht die physische Kapazität hat, Lagerungs- zu übernehmen.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Lagerort" einen Wert ein.
4. Geben Sie im Feld "Lagerort-Profil-ID" einen Wert ein.
5. Geben Sie im Feld "Verpackungsgrößenkategorie-ID" einen Wert ein.
6. Geben Sie im Feld "Menge" eine Zahl ein.
7. Klicken Sie auf "Speichern".
8. Schließen Sie die Seite.

## <a name="define-fixed-picking-locations"></a>detaillierten feste Entnahmeorte definieren
1. Feste Lagerplätze anzeigen
    * Sie können die pro Produkt oder pro Produktvariante verwendet werden Lagerplätze definieren. Es ist möglich, mehrere korrigierte Lagerplätze für das gleiche Produktdimensionsgruppe innerhalb des gleichen Lagerort zu erstellen.  
2. Klicken Sie auf "Neu".
3. Geben Sie im Feld "Artikelnummer" einen Wert ein.
4. Geben Sie im Feld "Lagerort" einen Wert ein.
5. Klicken Sie im Feld "Lagerplatz" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
6. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
7. Schließen Sie die Seite.


