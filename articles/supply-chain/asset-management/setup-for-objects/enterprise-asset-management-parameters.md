---
title: Anlagenverwaltungsparameter
description: In der Anlageverwaltung müssen allgemeine Parameter in Bezug auf Arbeitsaufträge, Anlagen und Arbeitsauftragsplanung eingerichtet werden.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e6a2d428e433256339fff07f3805449a2604213
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783285"
---
# <a name="asset-management-parameters"></a>Anlagenverwaltungsparameter

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In der Anlageverwaltung müssen allgemeine Parameter in Bezug auf Arbeitsaufträge, Anlagen und Arbeitsauftragsplanung eingerichtet werden. In diesem Thema wird erläutert, wie diese eingerichtet werden. Wählen Sie **Anlageverwaltung** > **Einstellungen** > **Anlageverwaltungsparameter** aus, um das Formular zu öffnen.

Die Schaltfläche **Daten-Assistenten erstellen** kann verwendet werden, um in die Einstellungsdaten für Test- oder Demodatenzwecke in einem Unternehmen in Dynamics 365 for Finance and Operations automatisch zu erstellen. Weitere Informationen finden Sie im Whitepaper „Einstellung von Test-Daten im Anlage-Management“, um zu erfahren, wie der Assistent verwendet wird.

Link **Anlagen**

- **Funktionaler Lagerplatz Standard** ist der funktionale Lagerplatz Standard, der automatisch auf Anlagen ausgewählt wird, wenn Sie neue Anlagen erstellen.  
- Im Feld **Standardkalender** wählen Sie einen Kalender, der für die Berechnung der Anlage-KPIs verwendet wird, falls keine Ressource für eine Anlage ausgewählt ist.  
- Im Feld **Ansicht** wählen Sie die Standardansicht aus, die angezeigt wird, wenn Sie das Formular **Anlagenansicht** öffnen (**Anlageverwaltung** > **Gemeinsam** > **Anlagen** > **Anlagenansicht**).
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
- Im Feld **Verwandte Arbeitsauftragsmaske** definieren die maximale Anzahl von Arbeitsaufträgen, die einem Arbeitsauftrag zugeordnet werden können. Beispiel: Beispiel: ## ermöglicht es Ihnen, bis 99 Arbeitsaufträge zuzuordnen. Wenn Sie eine Maske wie hier beschrieben definieren, werden zugehörige Arbeitsaufträge [Arbeitsauftrag-Kennung des Arbeitsauftrags, auf die sich ein Arbeitsauftrag bezieht] nummeriert mit -01, -02, -03, usw. Wenn Sie keinerlei Maske in diesem Feld definieren, wird ein zugehöriger Arbeitsauftrag die darauf folgende Auftragsnummer die Arbeitsauftrags-Kennung.  
- Wählen Sie „Ja“ auf der Umschalttaste **Kopienfehler** aus, wenn Sie die Fehler automatisch kopieren möchten, die auf Arbeitsaufträgen zu zugehörigen Wartungsanforderungen erfasst werden.  
- Im Feld **Ebene** definieren Sie die funktionale Lagerplatzebene, die automatisch für einen Arbeitsauftrag eingefügt wird, wenn alle zugehörigen Arbeitsauftragseinzelvorgänge auf den funktionalen gleichen Speicherort verweisen. Wenn nicht alle Arbeitsauftragseinzelvorgänge derselben funktionalen Position auf der definierten Ebene zugeordnet werden, wird das Feld  **Funktionaler Lagerplatz** auf dem Arbeitsauftrag leer gelassen. Beispiel: Wenn Sie die Nummer „1“ in diesem Feld eingeben, ist dies die höchste Ebene in der funktionalen Lagerplatzstruktur. Wenn Sie die Nummer „0“ in diesem Feld einfügen, haben Sie keine bestimmte funktionale Lagerplatzebene definiert, nur dass alle Arbeitsauftragsstellen eines Arbeitsauftrags dem gleichen Standort zugeordnet sein müssen, damit der Lagerplatz dem Arbeitsauftrag funktionale hinzugefügt werden kann.  
- Die Erfassungen, die verwendet werden, wenn der Verbrauch in einem Arbeitsauftrag gebucht wird, kann auf dem Inforegister **Allgemein** in den Feldern **Stunde**, **Artikel** und **Ausgaben** ausgewählt werden.  
- Wählen Sie im Feld **Produktsprachenquelle** die Sprache für die Produktnamen in Anlageverwaltungsberichten aus. Sie können die Sprache auswählen, die im Unternehmenskonto eingerichtet wird, für das der Benutzer derzeit Dynamics 365 for Finance and Operations angemeldet ist.  
- Wählen Sie „Ja“ auf der Umschalttaste **Echtzeitaktualisierung** aus, wenn Änderungen an den Einzelvorgangstypenstandards, Wartungsplänen und Wartungsdurchgängen automatisch aktualisiert werden sollen.
> - Wenn Sie „Nein“ auswählen, erfolgen keine automatischen Aktualisierungen an Einzelvorgangstyp-Standards, Wartungsplänen und Wartungsdurchgängen in der Anlageverwaltung  
> - Wählen Sie „Nein“ auf der Umschalttaste aus, wenn Sie große Datenmengen haben, die synchronisiert werden, beispielsweise viele Anlagen oder funktionale Standorte in Wartungsanlagen oder Wartungsplänen oder eine große Anzahl von Wartungsplänen oder -aufträgen.  
> - Wenn Sie Änderungen an Einzelvorgangstypstandards oder Wartungsdurchgängen vornehmen, und Sie „Nein“ in der Echtzeitaktualisierung ausgewählt haben, wird keine Warnung angezeigt werden, wenn die Änderung einen Einfluss hat auf:
>   - Funktionale Standorte für Wartungspläne oder Runden einrichten  
>   - Objekte, die für Wartungspläne oder Runden eingerichtet sind.  
>   - Wartungspläne einrichten  
>   - Wartungsdurchgänge inrichten  
- Auf dem Inforegister **Kategorie** können Standardkategorien in Bezug auf den Verbrauch in Arbeitsaufträgen definiert werden.  


**Arbeitsauftragsterminierung** Link

- **Planungszeitraum planen** definiert den Zeitraum in Tagen, berechnet, nach dem erwarteten Startdatum des Arbeitsauftrags, während dem Arbeitsauftragsvorgänge geplant werden.  
- **Produktprogrammplan** bezeieht sich auf die Ressourcen im Modul **Organisationsverwaltung**. Wenn Sie einen Produktprogrammplan in diesem Feld ausgewählt haben, sind Sie in der Lage, die Kapazitätsreservierungen zu sehen, die den Arbeitsaufträgen **Kapazitätsreservierungen** zugeordnet werden (**Organisationsverwaltung** > **Ressourcen** > **Ressourcen** > Ressource wählen > Registerkarte **Ressource** > Schaltfläche **Kapazitätsreservierungen**). Wenn Sie dieses Feld leer lassen, sehen Sie die Kapazitätsauslastung, die dem Arbeitsauftrag zugeordnet ist unter **Kapazitätsauslastung** (**Organisationsverwaltung** \>**Ressourcen** \> **Ressourcen** \> Ressource auswählen \> Registerkarte **Ressource** \> Schaltfläche **Kapazitätsauslastung**).  

>[!NOTE]
>Die Auswahl zur Verwendung eines Produktprogrammplans im Modul **Asset-Management** und das zugehörige Formular, das verwendet wird, um einen Überblick der Kapazitätsreservierungen oder Kapazitätsauslastung abzurufen, ist eine Standard Dynamics 365 for Finance and Operations Einstellung. Abhängig von Ihren Einstellungen im Feld **Produktprogrammplan** sind Sie in der Lage, auf Kapazitätsinformationen entweder über **Kapazitätsreservierungen** oder **Kapazitätsauslastung** **Organisationsverwaltung** zuzugreifen. Es ist nicht möglich, eine Einstellung zu erstellen, in der die Kapazitätsreservierungen in beiden Ansichten dargestellt werden.  

Alle Felder, die in der Aufzählungszeichenliste unter beschrieben werden, beziehen sich alle auf die berechneten Bewertungsnoten, die verwendet werden, um die Arbeitsauftragspriorität während der Arbeitsauftragsplanung zu berechnen.

- **Priorität** eine Bewertungsnote zusammen mit der Bewertungsnote auf den berechneten Feldern **Risiko** und **Startdatum**. Die Zahl in diesem Feld ist abhängig von der Nummer im Feld **Priorität** auf einen Arbeitsauftrag. Beispiel: Wenn der Wert „5,00“ auf diesem Feld eingetragen ist und ein Arbeitsauftrag Priorität „20“ hat, ist die Bewertungsnote für Priorität 0,25.  
- **Risiko** eine Bewertungsnote zusammen mit der Bewertungsnote auf den berechneten Feldern **Priorität** und **Startdatum**. Die Zahl in diesem Feld wird mit der Nummer im Feld **Risiko** auf einen Arbeitsauftrag multipliziert. Beispiel: Wenn der Wert „10,00“ auf diesem Feld eingetragen ist und ein Arbeitsauftrag Priorität „5“ hat, ist die Bewertungsnote für Priorität 50.  
- **Startdatum** eine Bewertungsnote zusammen mit der Bewertungsnote auf den berechneten Feldern **Priorität** und **Risiko**. Dieses Feld gibt die tägliche Bewertung als negativen Wert an und wird mit dem Feld **Erwarteter Anfang** auf einen Arbeitsauftrag verglichen. Beispiel: Wenn der Wert „10,00“ auf diesem Feld eingefügt wird und das voraussichtliche Startdatum eines Arbeitsauftrags drei Tage ab nun ist, ist das Bewertungsergebnis minus 30,00. Das Hinzufügen der Ergebnisse von 0,25 und 50 aus den Beispielen **Priorität** und **Risiko**, die oben beschrieben werden, ergeben insgesamt plus-20,25. Diese Zahl wird mit allen anderen Arbeitsauftragsbewertungsnoten während der Arbeitsauftragsplanung verglichen und die höchsten Bewertungsnoten werden dann zuerst geplant.  
- **Verantwortliche Arbeitskraft** - eine Bewertungsnote, die zusammen mit **Verantwortliche Arbeitskraftgruppe**, **Bevorzugte Arbeitskraft**, **Bevorzugte Arbeitskraftgruppe**, **Anlagenstandort** und **Startdatum** Bewertungsnotenwerten berechnet wird.. Wenn der Wert „50,00“ auf diesem Feld eingefügt wird und eine zuständige Arbeitskraft in einem Arbeitsauftrag aktiviert wurde, erhält die Arbeitskraft 50 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- **Verantwortliche Arbeitskraftgruppe** - eine Bewertungsnote, die zusammen mit **Verantwortliche Arbeitskraft**, **Bevorzugte Arbeitskraft**, **Bevorzugte Arbeitskraftgruppe**, **Anlagenstandort** und **Startdatum** Bewertungsnotenwerten berechnet wird.. Wenn der Wert „50,00“ auf diesem Feld eingefügt wird und eine zuständige Arbeitskraft in einem Arbeitsauftrag aktiviert wurde, erhält die Arbeitskraft 50 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- Die Ja/Nein-Umschalttaste **Limite für Zuständige** schränkt die Anzahl verfügbarer Arbeitskräfte für die Arbeitsauftragsplanung ein. Wählen Sie „Nein“, wenn Sie eine Bewertung für alle Arbeitskräfte berechnen möchten, unabhängig davon, ob sie als zuständige Arbeitskräfte oder als Teil einer Arbeitskraftgruppe eingerichtet werden. Wählen Sie „Ja“ aus wenn Sie eine Bewertung für Arbeitskräfte berechnen möchten, die als zuständige Arbeitskraft im Feld Arbeitsauftrag eingerichtet ist und/oder in einer zuständigen Arbeitskraftgruppe einbezogen wird, die im Arbeitsauftrag aktiviert ist.  
- **Bevorzugte Arbeitskraft** - eine Bewertungsnote, die zusammen mit der **Verantwortlichen Arbeitskraft**, **Bevorzugten Arbeitskraft**, **Bevorzugten Arbeitskraftgruppe**, **Anlagenstandort** und **Startdatum** Bewertungsnotenwerten berechnet wird.. Die vier Bewertungsnoten werden zusammen berechnet und hinzugefügt, um eine Bewertung bereitzustellen, die für die Auswahl verwendet wird, welche der Arbeitskraft während der Arbeitsauftragsplanung zugewiesen wird. Wenn der Wert „10,00“ auf diesem Feld eingefügt wird und eine Arbeitskraft als bevorzugte Arbeitskraft in einem Arbeitsauftrag ausgewählt wurde, erhält die Arbeitskraft 10 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- **Bevorzugte Arbeitskraftgruppe** - eine Bewertungsnote, die zusammen mit der**Verantwortlichen Arbeitskraft**, **Bevorzugten Arbeitskraft**, **Bevorzugten Arbeitskraftgruppe**, **Anlagenstandort** und **Startdatum** Bewertungsnotenwerten berechnet wird.. Wenn der Wert „10,00“ auf diesem Feld eingefügt wird und eine Arbeitskraft als bevorzugte Arbeitskraft einem Arbeitsauftrag zugewiesen wird, erhält die Arbeitskraft 10 Punkte in der Gesamtarbeitskraftberechnung während der Arbeitsauftragsplanung.  
- Die Ja/Nein-Umschalttaste **Limite für bevorzugt** schränkt die Anzahl verfügbarer Arbeitskräfte für die Arbeitsauftragsplanung ein. Wählen Sie „Nein“, wenn Sie eine Bewertung für alle Arbeitskräfte berechnen möchten, unabhängig davon, ob sie als bevorzugte Arbeitskräfte oder als Teil einer bevorzugten Arbeitskraftgruppe eingerichtet werden. Wählen Sie „Ja“, wenn Sie eine Bewertung für alle Arbeitskräfte berechnen möchten, unabhängig davon, ob sie als bevorzugte Arbeitskräfte eingerichtet werden und/oder in einer bevorzugten Arbeitskraftgruppe eingeschlossen werden.  
- **Standort** - eine Bewertungsnote, die zusammen mit der **Verantwortlichen Arbeitskraft**, **Bevorzugten Arbeitskraft**, **Bevorzugten Arbeitskraftgruppe**, **Anlagenstandort** und **Startdatum** Bewertungsnotenwerten berechnet wird. Wenn der Wert „3.000,00“ auf diesem Feld eingefügt wird, erhält eine Arbeitskraft 3.000 Punkte in der Berechnung, wenn die Arbeitskraft in derselben Fabrik oder in der selben Einrichtung ist, wie die Anlage, für die der Vorgang geplant ist.  

  - Wenn Ihr Unternehmen funktionale Lagerplätze verwendet, erhalten die Arbeitskräfte die volle Punktzahl, wenn sie sich am selben funktionalen Standort befinden, dem die Anlage zugeordnet ist. Falls der funktionale Standort der Anlage eine übergeordnete Anlage hat, erhalten Arbeitskräfte an diesem funktionalen Standort die Hälfte der Punkte. Wenn dieser Lagerplatz auch einen übergeordneten Platz hat, erhalten die Arbeitskräfte an diesem Standort 1/3 der Punkte. Wenn dieser Lagerplatz auch einen übergeordneten Platz hat, erhalten die Arbeitskräfte an diesem Standort 1/4 der Punkte, und so weiter.  
  - Wenn Ihr Unternehmen einen Anlagestandort verwendet, die von uns nicht empfohlen wird, werden Ort, Bereich und Zone verwendet, um Lagerplatzpunktzahlen zu berechnen. Arbeitskräfte erhalten volle Punkte, wenn sie sich am selben Standort, im selben Bereich und der selben Zone befinden, wie die zugeordnete Anlage. Wenn nur der Arbeitskraftstandort mit dem Standort und dem Bereich übereinstimmt, entspricht die Bewertungsnote für die Arbeitskraft 2/3 der ganzen Punktezahl. Wenn nur der Arbeitskraftstandort mit dem Standort und dem Bereich übereinstimmt, entspricht die Bewertungsnote für die Arbeitskraft 1/3 der ganzen Punktezahl.  

- Die Ja/Nein-Umschalttaste **Limite für Standort** schränkt die Anzahl verfügbarer Arbeitskräfte für die Arbeitsauftragsplanung ein. Wählen Sie „Nein“ aus wenn Sie eine Bewertung für alle Arbeitskräfte über alle funktionalen Standorte hinweg berechnen möchten. Wählen Sie „Ja“ aus wenn Sie nur eine Bewertung für Arbeitskräfte berechnen möchten, die dem funktionalen Standort des Arbeitsauftrags zugeordnet werden.

>[!NOTE]
>Die drei Umschalttasten „Limite für…“ werden eingeführt, um die Geschwindigkeit der Arbeitsauftragsplanung zu erhöhen, indem die Anzahl von Bewertungen eingeschränkt wird, die für Arbeitskräfte berechnet werden.

**Startdatum Arbeitskraft** - eine Bewertungsnote, die zusammen mit der **Verantwortlichen Arbeitskraft**, **Bevorzugten Arbeitskraft**, **Bevorzugten Arbeitskraftgruppe**, **Anlagenstandort** und **Startdatum** Bewertungsnotenwerten berechnet wird.. Dieses Feld gibt die tägliche Bewertung als negativen Wert an und wird mit dem Feld **Erwarteter Anfang** auf einen Arbeitsauftrag verglichen. Wenn der Wert „10,00“ auf diesem Feld eingefügt wird und das voraussichtliche Startdatum eines Arbeitsauftrags am nächsten Tag ist, ist das Bewertungsergebnis minus 10,00.

  - Angenommen, dass keine zuständige Arbeitskraft und zuständige Arbeitskraftgruppe für einen Arbeitsauftrag eingeplant wird, fügen Sie die Bewertungsnotenwerte in den Beispielen hinzu und ziehen es ab in den Beispielen mit den Felder **Bevorzugte Arbeitskraft**, **Bevorzugte Arbeitskraftgruppe**, **Anlagenstandort** und**Startdatum** und Sie erhalten insgesamt 3.010,00. Das bedeutet eine hohe Bewertung für die Arbeitskraft, die bereits als bevorzugte Arbeitskraft aktiviert ist sowie in der bevorzugten Arbeitskraftgruppe im Feld Arbeitsauftrag einbezogen ist, und die Arbeitskraft sitzt auch am selben Standort wie die Anlage, für die ein Einzelvorgang geplant werden muss. Alles in allem bedeutet dies, dass es eine gute Chance gibt, dass die betreffende Arbeitskraft ausgewählt wurde, um den Einzelvorgang in der Arbeitsauftragsplanung abzuschließen.  
  - Wenn der Wert „0,00“ in einem der acht Felder eingefügt wird, wird diese Bewertungsnote nicht innerhalb der Arbeitsauftragsplanung verwendet.  


**Dokumenttypen** Link

Wählen Sie die Dokumenttypen aus, die beim Drucken von Anhängen verfügbar sein sollen, die einem Arbeitsauftragsbericht zugeordnet werden. Dies erfolgt, indem Sie auf einen Dokumenttyp im Abschnitt **Verfügbar** klicken und auf die Schaltfläche ![Vorwärtspfeil](media/15-setup-for-objects.png) klicken. Wenn Sie einen bestimmten Dokumenttyp entfernen möchten, wählen Sie im Abschnitt **Ausgewählt** den Dokumenttyp aus und klicken auf die Schaltfläche ![Pfeil zurück](media/16-setup-for-objects.png).



**Nummernkreise** Link

Dient zum Auswählen der erforderlichen Nummernkreise in diesem Bereich. Es gibt zwei Nummernkreise für Anlagen: Einen für manuell erstellte Anlagen und einen für die Anlagen betreffed ausstehende Anlagen.
