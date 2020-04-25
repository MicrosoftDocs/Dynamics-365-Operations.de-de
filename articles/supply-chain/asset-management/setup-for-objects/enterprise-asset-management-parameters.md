---
title: Anlagenverwaltungsparameter
description: In der Anlageverwaltung müssen allgemeine Parameter in Bezug auf Arbeitsaufträge, Anlagen und Arbeitsauftragsplanung eingerichtet werden.
author: josaw1
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8913fec3e76de0e1f4d10b05804317ada5498e83
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216642"
---
# <a name="asset-management-parameters"></a>Anlagenverwaltungsparameter

[!include [banner](../../includes/banner.md)]

In der Anlageverwaltung müssen allgemeine Parameter in Bezug auf Arbeitsaufträge, Anlagen und Arbeitsauftragsplanung eingerichtet werden. In diesem Thema wird erläutert, wie diese eingerichtet werden. Wählen Sie **Anlagenverwaltung** > **Einrichtung** > **Anlagenverwaltungsparameter**, um die Seite zu öffnen.

> [!NOTE]
> Wenn Sie ein System einrichten möchten, das Demodaten zum Testen von Anlagenverwaltung-Funktionen enthält, finden Sie unter [Demoumgebung bereitstellen](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) Anweisungen.

Link **Anlagen**

- **Funktionaler Lagerplatz Standard** ist der funktionale Lagerplatz Standard, der automatisch auf Anlagen ausgewählt wird, wenn Sie neue Anlagen erstellen.  
- Wählen Sie im Feld **Standardkalender** einen Kalender aus, der für die Berechnung der Anlagen-KPIs verwendet werden soll, wenn keine Ressource auf einer Anlage ausgewählt ist.  
- Wählen Sie im Feld **Ansicht** die Standardansicht, die angezeigt wird, wenn Sie **Anlagenansicht** öffnen (**Anlagenverwaltung** > **Gemeinsam** > **Anlagen** > **Anlagenansicht**).
- **Standardanforderungstyp** ist der Standardwartungsanfragetyp, der automatisch aktiviert wird, wenn Sie einen neuen Einrichtungsantrag erstellen.  
- Wenn Sie Projekte erstellen möchten, die sich auf Anlagen beziehen, werden Projektrelationen bei Auswahl von **Hauptprojekt**, **Projekthierarchie** und die Option **Projekte automatisch erstellen** in **Anlageverwaltungsparameter** eingerichtet.  
- Im Feld **Arbeitsauftragsprojektmaske** können Sie die Anzahl der Unterprojekte definieren die für Arbeitsaufträge und Subventionsanlagen zulässig sind. Eine Arbeitsauftragsmaske wird verwendet, um festzulegen, wie viele Arbeitsaufträge auf einer Anlage erstellt werden und für das zugehörigen Arbeitsauftragseinzelvorgangsprojekt verwendet werden können. Die Arbeitsauftragsmaske wird im Feld **Verwandte Arbeitsauftragsmaske** **Anlageverwaltungsparameter** (**Anlageverwaltung** > **Einstellungen** > **Anlageverwaltungsparameter** > **Arbeitsaufträge**) eingerichtet.  
    >[!NOTE]
    >Das Format für eine zugehörige Arbeitsauftragsmaske ist eine Reihe von Hashvorzeichen (# ), abhängig von der maximalen Anzahl von Arbeitsaufträgen, die Sie für die Anlage erstellen werden. Beispiel: ## ermöglicht es, bis zu 99 Unterprojekte zu erstellen.  
- Planungen auf Einzelvorgangstypen werden auf das Projekt gespeichert, das im Feld **Planungsprojekt** ausgewählt wird. Für jeden Einzelvorgangstyp wird eine neue Aktivität automatisch im Feld Planungsprojekt erstellt. Planungen bezüglich des Stellentyps werden dann im Planungsprojekt gespeichert.  
- Im Feld **Modell** wählen Sie das Planzahlenmodell aus, das auf Einzelvorgangstyp- und Arbeitsauftragsplanungen verwendet wird.  


Link **Arbeitsaufträge**

- **Standardarbeitsauftragstyp** definiert Standardeinstellungen, wenn ein Arbeitsauftrag erstellt wird.  
- **Vorbeugender Arbeitsauftragstyp** definiert den Arbeitsauftragstyp, wenn Arbeitsaufträge von den Wartungsplänen verwendet werden. Wenn dieses Feld leer bleibt, wird der Arbeitsauftrag in dem Feld **Standardarbeitsauftragstyp** verwendet.  
- Im Feld **Verwandte Arbeitsauftragsmaske** definieren die maximale Anzahl von Arbeitsaufträgen, die einem Arbeitsauftrag zugeordnet werden können. Mit ## können Sie zum Beispiel bis zu 99 Arbeitsaufträge miteinander in Beziehung setzen. Wenn Sie eine Maske wie hier beschrieben definieren, werden zugehörige Arbeitsaufträge [Arbeitsauftrag-Kennung des Arbeitsauftrags, auf die sich ein Arbeitsauftrag bezieht] nummeriert mit -01, -02, -03, usw. Wenn Sie keinerlei Maske in diesem Feld definieren, wird ein zugehöriger Arbeitsauftrag die darauf folgende Auftragsnummer die Arbeitsauftrags-Kennung.  
- Wählen Sie **Ja** für **Fehler kopieren**, wenn Sie die auf den Arbeitsaufträgen registrierten Fehler automatisch in die zugehörigen Wartungsanforderungen kopieren möchten. 
- Im Feld **Ebene** definieren Sie die funktionale Lagerplatzebene, die automatisch für einen Arbeitsauftrag eingefügt wird, wenn alle zugehörigen Arbeitsauftragseinzelvorgänge auf den funktionalen gleichen Speicherort verweisen. Wenn nicht alle Arbeitsauftragseinzelvorgänge derselben funktionalen Position auf der definierten Ebene zugeordnet werden, wird das Feld  **Funktionaler Lagerplatz** auf dem Arbeitsauftrag leer gelassen. Wenn Sie z.B. die Zahl „1“ in dieses Feld einfügen, ist das die oberste Ebene in einer funktionalen Standortstruktur. Wenn Sie die Nummer „0“ in diesem Feld einfügen, haben Sie keine bestimmte funktionale Lagerplatzebene definiert, nur dass alle Arbeitsauftragsstellen eines Arbeitsauftrags dem gleichen Standort zugeordnet sein müssen, damit der Lagerplatz dem Arbeitsauftrag funktionale hinzugefügt werden kann.  
- Die Erfassungen, die verwendet werden, wenn der Verbrauch in einem Arbeitsauftrag gebucht wird, kann auf dem Inforegister **Allgemein** in den Feldern **Stunde**, **Artikel** und **Ausgaben** ausgewählt werden.  
- Wählen Sie im Feld **Produktsprachenquelle** die Sprache für die Produktnamen in Anlageverwaltungsberichten aus. Sie können die im Unternehmenskonto oder die für den derzeit angemeldeten Benutzer eingerichtete Sprache auswählen.  
- Wählen Sie **Ja** für **Echtzeitaktualisierung**, wenn Sie Änderungen an den Arbeitsplatzvorgaben, Wartungsplänen und Wartungsrunden automatisch aktualisieren wollen.
  - Wenn Sie **Nein** wählen, werden Änderungen an Arbeitsplatzvorgaben, Wartungsplänen und Wartungsrunden in der Anlagenverwaltung nicht automatisch aktualisiert.
  - Wählen Sie **Nein**, wenn große Datenmengen synchronisiert werden, z.B. viele Anlagen oder funktionalen Standorten, die auf Wartungsplänen oder Wartungsrunden eingerichtet sind, oder eine große Anzahl von Wartungsplänen oder -runden.  
  - Wenn Sie Änderungen an Arbeitsplatzvorgaben oder Wartungsplänen oder -runden vornehmen und **Nein** auf Echtzeit-Aktualisierung eingestellt haben, wird möglicherweise keine Warnung angezeigt, wenn die Änderungen Auswirkungen haben:
    - Einrichtung von funktionalen Standorten auf Wartungsplänen oder -runden  
    - Objekte, die auf Wartungsplänen oder -runden eingerichtet sind  
    - Einrichtung von Wartungsplänen  
    - Einrichtung der Wartungsrunden  
- Auf dem Inforegister **Kategorie** können Standardkategorien in Bezug auf den Verbrauch in Arbeitsaufträgen definiert werden.  


**Arbeitsauftragsterminierung** Link

- **Planungszeitraum planen** definiert den Zeitraum in Tagen, berechnet, nach dem erwarteten Startdatum des Arbeitsauftrags, während dem Arbeitsauftragsvorgänge geplant werden.  
- **Produktprogrammplan** bezeieht sich auf die Ressourcen im Modul **Organisationsverwaltung**. Wenn Sie einen Produktprogrammplan in diesem Feld ausgewählt haben, sind Sie in der Lage, die Kapazitätsreservierungen zu sehen, die den Arbeitsaufträgen **Kapazitätsreservierungen** zugeordnet werden (**Organisationsverwaltung** > **Ressourcen** > **Ressourcen** > Ressource wählen > Registerkarte **Ressource** > Schaltfläche **Kapazitätsreservierungen**). Wenn Sie dieses Feld leer lassen, sehen Sie die Kapazitätsauslastung, die dem Arbeitsauftrag zugeordnet ist unter **Kapazitätsauslastung** (**Organisationsverwaltung** \>**Ressourcen** \> **Ressourcen** \> Ressource auswählen \> Registerkarte **Ressource** \> Schaltfläche **Kapazitätsauslastung**).  

>[!NOTE]
>Die Auswahl hinsichtlich der Verwendung eines Masterplans im Modul **Anlagenmanagement** und die damit verbundene Form, sich einen Überblick über Kapazitätsbuchungen oder Kapazitätsauslastung zu verschaffen, ist die Standardeinstellung. Abhängig von Ihren Einstellungen im Feld **Produktprogrammplan** sind Sie in der Lage, auf Kapazitätsinformationen entweder über **Kapazitätsreservierungen** oder **Kapazitätsauslastung** **Organisationsverwaltung** zuzugreifen. Es ist nicht möglich, eine Einstellung zu erstellen, in der die Kapazitätsreservierungen in beiden Ansichten dargestellt werden.  

Die in der folgenden Liste beschriebenen Felder beziehen sich alle auf errechnete Bewertungskennzahlen, die zur Berechnung der Auftragspriorität bei der Arbeitsauftragsterminierung verwendet werden.

- **Priorität** - Eine Bewertungszahl, die zusammen mit der Bewertungszahl in den Feldern **Kritikalität** und **Starttermin** berechnet wird. Die Zahl in diesem Feld ist abhängig von der Nummer im Feld **Priorität** auf einen Arbeitsauftrag. Wenn beispielsweise der Wert „5,00“ in dieses Feld eingegeben wird und ein Arbeitsauftrag die Priorität „20“ hat, beträgt die Bewertungsnote für die Priorität 0,25.  
- **Kritikalität** - Eine Bewertungsbewertung, die zusammen mit der Bewertungsbewertung in den Feldern **Priorität** und **Beginndatum** berechnet wird. Die Zahl in diesem Feld wird mit der Nummer im Feld **Risiko** auf einen Arbeitsauftrag multipliziert. Wenn beispielsweise der Wert „10,00“ in dieses Feld eingegeben wird und ein Arbeitsauftrag die Kritikalität „5“ hat, beträgt die Bewertungsnote für die Kritikalität 50.  
- **Beginndatum** - Eine Bewertungsbewertung, die zusammen mit der Bewertungsbewertung in den Feldern **Priorität** und **Kritikalität** berechnet wird. Dieses Feld gibt die tägliche Bewertung als negativen Wert an und wird mit dem Feld **Erwarteter Anfang** auf einen Arbeitsauftrag verglichen. Wenn beispielsweise der Wert „10,00“ in dieses Feld eingegeben wird und das erwartete Startdatum eines Arbeitsauftrags in drei Tagen liegt, ist das Rating-Ergebnis minus 30,00. Das Hinzufügen der Ergebnisse von 0,25 und 50 aus den Beispielen **Priorität** und **Risiko**, die oben beschrieben werden, ergeben insgesamt plus-20,25. Diese Zahl wird mit allen anderen Arbeitsauftragsbewertungsnoten während der Arbeitsauftragsplanung verglichen und die höchsten Bewertungsnoten werden dann zuerst geplant.  
- **Verantwortlicher Mitarbeiter** - Ein zusammen mit **Verantwortliche Mitarbeitergruppe**, **Bevorzugter Mitarbeiter**, **Bevorzugte Mitarbeitergruppe**, **Anlagenstandort** und **Startdatum** Ratingscore Werte berechnet. Wenn der Wert „50,00“ auf diesem Feld eingefügt wird und eine zuständige Arbeitskraft in einem Arbeitsauftrag aktiviert wurde, erhält die Arbeitskraft 50 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- **Verantwortliche Mitarbeitergruppe** - Ein Bewertungswert, der zusammen mit **Verantwortlicher Mitarbeiter**, **Bevorzugter Mitarbeiter**, **Bevorzugte Mitarbeitergruppe**, **Asset-Standort** und **Startdatum** Bewertungspunktzahlen berechnet wird. Wenn der Wert „50,00“ auf diesem Feld eingefügt wird und eine zuständige Arbeitskraft in einem Arbeitsauftrag aktiviert wurde, erhält die Arbeitskraft 50 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- **Beschränkung auf Verantwortliche** - Dies begrenzt die Anzahl der für die Arbeitsauftragsplanung verfügbaren Mitarbeiter. Wählen Sie **Nein**, wenn Sie eine Bewertung für alle Mitarbeiter berechnen möchten, unabhängig davon, ob sie als verantwortliche Mitarbeiter oder als Teil einer verantwortlichen Mitarbeitergruppe eingerichtet sind. Wählen Sie **Ja**, wenn Sie eine Punktzahl für Arbeiter berechnen möchten, die als verantwortliche Mitarbeiter auf dem Arbeitsauftrag eingerichtet sind und/oder zu einer auf dem Arbeitsauftrag ausgewählten verantwortlichen Mitarbeitergruppe gehören.  
- **Bevorzugter Mitarbeiter** - Eine Bewertungspunktzahl, die zusammen mit den Werten **Verantwortlicher Mitarbeiter**, **Bevorzugter Mitarbeiter**, **Bevorzugte Mitarbeitergruppe**, **Assetstandort** und **Startdatum** Bewertungspunktzahl berechnet wird. Die vier Bewertungsnoten werden zusammen berechnet und hinzugefügt, um eine Bewertung bereitzustellen, die für die Auswahl verwendet wird, welche der Arbeitskraft während der Arbeitsauftragsplanung zugewiesen wird. Wenn der Wert „10,00“ auf diesem Feld eingefügt wird und eine Arbeitskraft als bevorzugte Arbeitskraft in einem Arbeitsauftrag ausgewählt wurde, erhält die Arbeitskraft 10 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- **Bevorzugte Mitarbeitergruppe** - Ein Rating-Score, der zusammen mit **Verantwortlicher Mitarbeiter**, **Bevorzugter Mitarbeiter**, **Bevorzugte Mitarbeitergruppe**, **Asset-Standort** und **Startdatum** Rating-Scorewerte berechnet wird. Wenn der Wert „10,00“ auf diesem Feld eingefügt wird und eine Arbeitskraft als bevorzugte Arbeitskraft einem Arbeitsauftrag zugewiesen wird, erhält die Arbeitskraft 10 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- **Begrenzung auf bevorzugte Mitarbeiter** - Dies begrenzt die Anzahl der für die Arbeitsauftragsplanung verfügbaren Mitarbeiter. Wählen Sie **Nein**, wenn Sie eine Bewertung für alle Mitarbeiter berechnen möchten, unabhängig davon, ob sie als bevorzugte Mitarbeiter oder als Teil einer bevorzugten Mitarbeitergruppe eingerichtet sind. Wählen Sie **Ja**, wenn Sie nur eine Punktzahl für Arbeiter berechnen möchten, die als bevorzugte Arbeiter eingerichtet sind und/oder zu einer bevorzugten Arbeitergruppe gehören.  
- **Standort** - Ein Rating-Score, der zusammen mit den Werten **Verantwortlicher Mitarbeiter**, **Bevorzugter Mitarbeiter**, **Bevorzugte Mitarbeitergruppe**, **Standort** und **Startdatum** Rating-Scorewerte berechnet wird. Wenn der Wert „3.000,00“ auf diesem Feld eingefügt wird, erhält eine Arbeitskraft 3.000 Punkte in der Berechnung, wenn die Arbeitskraft in derselben Fabrik oder in der selben Einrichtung ist, wie die Anlage, für die der Vorgang geplant ist.  
  - Wenn Ihr Unternehmen funktionale Lagerplätze verwendet, erhalten die Arbeitskräfte die volle Punktzahl, wenn sie sich am selben funktionalen Standort befinden, dem die Anlage zugeordnet ist. Falls der funktionale Standort der Anlage eine übergeordnete Anlage hat, erhalten Arbeitskräfte an diesem funktionalen Standort die Hälfte der Punkte. Wenn dieser Lagerplatz auch einen übergeordneten Platz hat, erhalten die Arbeitskräfte an diesem Standort 1/3 der Punkte. Wenn dieser Lagerplatz auch einen übergeordneten Platz hat, erhalten die Arbeitskräfte an diesem Standort 1/4 der Punkte, und so weiter.  
  - Wenn Ihr Unternehmen einen Anlagestandort verwendet, die von uns nicht empfohlen wird, werden Ort, Bereich und Zone verwendet, um Lagerplatzpunktzahlen zu berechnen. Arbeitskräfte erhalten volle Punkte, wenn sie sich am selben Standort, im selben Bereich und der selben Zone befinden, wie die zugeordnete Anlage. Wenn nur der Arbeitskraftstandort mit dem Standort und dem Bereich übereinstimmt, entspricht die Bewertungsnote für die Arbeitskraft 2/3 der ganzen Punktezahl. Wenn nur der Arbeitskraftstandort mit dem Standort und dem Bereich übereinstimmt, entspricht die Bewertungsnote für die Arbeitskraft 1/3 der ganzen Punktezahl.  
- **Begrenzung auf Standort** - Dies begrenzt die Anzahl der für die Arbeitsauftragsplanung verfügbaren Mitarbeiter. Wählen Sie **Nein**, wenn Sie eine Bewertung für alle Mitarbeiter über alle funktionalen Standorte hinweg berechnen möchten. Wählen Sie **Ja**, wenn Sie nur für die Mitarbeiter, die mit dem Technischen Platz des Arbeitsauftrags verbunden sind, eine Punktzahl berechnen wollen.

>[!NOTE]
>Die drei Felder „Beschränkung auf“ erhöhen die Geschwindigkeit der Arbeitsauftragsplanung, indem sie die Anzahl der für die Arbeiter berechneten Punkte begrenzen.

**Beginndatum des Mitarbeiters** - Eine Bewertungspunktzahl, die zusammen mit **Verantwortlicher Mitarbeiter**, **Bevorzugter Mitarbeiter**, **Bevorzugte Mitarbeitergruppe**, **Asset Location** und **Beginndatum** Bewertungspunktzahlen berechnet wird. Dieses Feld gibt die tägliche Bewertung als negativen Wert an und wird mit dem Feld **Erwarteter Anfang** auf einen Arbeitsauftrag verglichen. Wenn der Wert „10,00“ auf diesem Feld eingefügt wird und das voraussichtliche Startdatum eines Arbeitsauftrags am nächsten Tag ist, ist das Bewertungsergebnis minus 10,00.

  - Angenommen, dass keine zuständige Arbeitskraft und zuständige Arbeitskraftgruppe für einen Arbeitsauftrag eingeplant wird, fügen Sie die Bewertungsnotenwerte in den Beispielen hinzu und ziehen es ab in den Beispielen mit den Felder **Bevorzugte Arbeitskraft**, **Bevorzugte Arbeitskraftgruppe**, **Anlagenstandort** und**Startdatum** und Sie erhalten insgesamt 3.010,00. Das bedeutet eine hohe Bewertung für die Arbeitskraft, die bereits als bevorzugte Arbeitskraft aktiviert ist sowie in der bevorzugten Arbeitskraftgruppe im Feld Arbeitsauftrag einbezogen ist, und die Arbeitskraft sitzt auch am selben Standort wie die Anlage, für die ein Einzelvorgang geplant werden muss. Dies bedeutet, dass eine gute Chance besteht, dass der betreffende Mitarbeiter bei der Arbeitsauftragsplanung für die Ausführung des Auftrags ausgewählt wird.  
  - Wenn der Wert „0,00“ in einem der acht Felder eingefügt wird, wird diese Bewertungsnote nicht innerhalb der Arbeitsauftragsplanung verwendet.  

**Dokumenttypen** Link

Wählen Sie die Dokumenttypen aus, die beim Drucken von Anhängen verfügbar sein sollen, die einem Arbeitsauftragsbericht zugeordnet werden. Dies geschieht durch Auswahl eines Dokumenttyps im Abschnitt **Verfügbar** und Auswahl von ![Vorwärtspfeil](media/15-setup-for-objects.png). Wenn Sie einen ausgewählten Dokumenttyp entfernen möchten, wählen Sie den Dokumenttyp im Abschnitt **Ausgewählt** und wählen Sie ![Pfeil nach hinten](media/16-setup-for-objects.png).

**Nummernkreise** Link

Dient zum Auswählen der erforderlichen Nummernkreise in diesem Bereich. Es gibt zwei Nummernkreise für Anlagen: einen für manuell erstellte Anlagen und einen für Anlagen, die durch ausstehende Anlagen erstellt wurden.
