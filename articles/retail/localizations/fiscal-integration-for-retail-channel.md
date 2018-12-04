---
title: "Steuerintegration für Einzelhandelskanal"
description: "In diesem Thema erhalten Sie einen Überblick über für die steuerliche Integration für Retail POS."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: de-de
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a>Steuerintegration für Einzelhandelskanal

[!include [banner](../includes/banner.md)]

Dieses Thema enthält einen Überblick der steuerlichen Integrationsfunktionen, die in Microsoft Dynamics 365 for Retail verfügbar sind. Die steuerliche Integrationsfunktionen sind ein Framework, das entwickelt wurde, um die lokalen Steuerrechte zu unterstützen, um im Einzelhandel Betrug zu verhindern. Typische Szenarien, die erfasst werden können, indem steuerliche Integration verwendet wird, umfassen Folgendes:

- Das Drucken des Steuerbelegs und die Übergabe an den Debitor.
- Die Übermittlung der Informationen von Verkäufen und die Rücklieferungen, die am POS für eine Fremddienstleistung erfolgt, die von der Behörde bereitgestellt wird.
- Verwenden des Datenschutzes mit einer digitalen Signatur, autorisiert von der Behörde.

Dieses Thema erstellt Richtlinien zum Einrichten der steuerlichen Integration, sodass Benutzer die folgenden Aufgaben ausführen. 

- Konfigurieren Sie steuerliche Verbindungen, welche steuerlichen Geräte oder Dienste sind, die für  Erfassungszwecke wie Speichern, digitale Signaturen und gesicherter Übermittlung von Steuerdaten verwendet werden.
- Konfigurieren Sie den Dokumentanbieter, der eine Ausgabemethode und ein Algorithmus für steuerliche Dokumentgenerierung definiert.
- Konfigurieren vom steuerlichen Registrierungsprozess, der eine Folge von Schritten und eine Gruppe von Verbindungen definiert, die in jedem Schritt verwendet werden.
- Weisen Sie steuerliche Anmeldeprozesse zu POS-Funktionsprofilen hinzu.
- Weisen Sie Verbindungen technischen Profilen zu, entweder den Hardwareprofilen (für die lokalen steuerlichen Verbindungen) oder den POS-Funktionsprofilen (für andere steuerliche Konnektortypen).

## <a name="fiscal-integration-execution-flow"></a>Steuerlicher Integrationsausführungsfluss
Im folgenden Szenario wird der allgemeine steuerliche Integrationsausführungsfluss angezeigt.

1. Initialisierung des Steuerregistrierungsprozesses.
  
   Nach dem einige Aktivitäten ausgeführt wurden, bei denen die Steuererfassung erforderlich ist, wie nach einer Einzelhandelstransaktion, wird der Steuerreferenz Registrierungsprozess dem Funktionsprofil des laufenden POS zugeordnet.

1. Dient zum Suchen eines steuerlichen Konnektors.
   
   Für jeden steuerlichen Erfassungsschritt, der im steuerlichen Registrierungsprozess einbezogen wird, wird vom System die Liste von steuerlichen Verbindungen abgeglichen. Diese Verbindungen haben ein funktionales Profil, das in der angegebenen Konnektorgruppe enthalten ist, mit einer Liste von Verbindungen, die ein technisches Profil mit dem aktuellen Hardwareprofil enthalten (für einen Verbindungstyp, der nur **Lokal** ist) oder mit dem aktuellen POS_Funktionalitätsprofil (für andere Verbindungstypen).
   
1. Führen Sie die steuerliche Integration aus.

   Das System führt alle erforderlichen Aktivitäten aus, die für eine Assembly definiert werden, die mit dem gefundenen Konnektor verknüpft ist. Dieses wird entsprechend den Einstellungen des funktionalen und des technischen Profils gemacht, das im vorhergehenden Schritt für diesen Konnektor gefunden wurde.

## <a name="setup-needed-before-using-fiscal-integration"></a>Einstellung vor der Verwendung für steuerliche Integration erforderlich
Vor der Verwendung für steuerliche Integrationsfunktionen müssen Sie die folgenden Einstellungen  definieren:

- Definieren Sie die Reihenfolge auf der Seite **Einzelhandelsparameter** für die steuerliche funktionale Profilnummer.
  
- Dient zum Definieren der Nummernkreise **Freigegebene Einzelhandelsparameter**Seite für die  folgenden Referenzen:
  
  - Nummer des technischen Steuerprofils
  - Nummer der Steuerconnectorgruppe
  - Registrierungsprozessnummer

- Erstellen Sie **Steuerlicher Konnektor** in **Retail > Kanal einrichten > Steuerliche Integration > Steuerliche Verbindungen** oder Dienstleistungen, die Sie für steuerliche Integrationszwecke verwenden möchten.

-  Erstellen Sie einen **Steuerlichen Dokumentanbieter** in **Retail > Kanal richten > steuerliche Integration > steuerliche Dokumentanbieter** für alle steuerlichen Verbindungen. Datenenzuordnung gilt als einen Teil des steuerlichen Dokumentanbieters. Wenn Sie andere Datenenzuordnungen für den gleichen Konnektor einrichten (beispielsweise besondere Bestimmungen für ein Bundesland), sollten Sie verschiedene steuerliche Dokumentanbieter erstellen.

- Erstellen Sie **Funktionales Profil des Konnektors** in **Retail > Kanal richten > steuerliche Integration > funktionale Profile des Konnektors** für jeden steuerlichen Dokumentanbieter
  - Wählen Sie einen Verbindungsnamen.
  - Wählen Sie einen Dokumentenanbieter.
  - Definieren Sie die Mehrwertsteuersatzeinstellungen auf der Registerkarte **Dienstleistung einstellen**.
  - Geben Sie den MwSt-Zuordnungcode und die Zahlungsmitteltypzuordnung auf der Registerkarte **Datenenzuordnung** ein.

  #### <a name="examples"></a>Beispiele 

  |  | Format | Beispiel | 
  |--------|--------|--------|
  | MwSt-Satzeinstellungen | Wert: MwSt-Satz | 1 : 2000, 2 : 1800 |
  | Zuordnung von MwSt.-Codes | MwSt-Code: Wert | vat20: 1, vat18: 2 |
  | Zahlungsmitteltyp-Zuordnung | TenderTyp: Wert | Bargeld: 1, Karte : 2 |

- Erstellen Sie **Steuerliche Konnektorgruppen** in **Retail > Kanal einrichten > steuerliche Integration > steuerliche Konnektorgruppe**. Eine Konnektorgruppe ist eine Teilmenge funktionaler Profile, die mit steuerlichen Verbindungen verknüpft werden, um identische Funktionen auszuführen und in dem gleichen Zeitpunkt innerhalb eines steuerlichen Anmeldeprozesses verwendet zu werden.

   - Hier können Sie funktionale Profile der Konnektorgruppe hinzufügen Klicken Sie der Seite **Hinzufügen** auf **Funktionale Profile** und wählen Sie eine Profilnummer aus.
   - Wenn Sie die Nutzung des funktionalen Profils unterbrechen möchten, wählen Sie **Deaktivieren** und wählen **Ja** aus.. 
   
     Diese Änderung betrifft nur die aktuellen Konnektorgruppe. Sie können das selbe funktionale Profil in anderen Konnektorgruppen weiter nutzen.

     >[!NOTE]
     > Innerhalb einer Konnektorgruppe kann jeder steuerliche Konnektor nur ein funktionales Profil haben.

- Erstellen Sie ein **Technisches Profil des Konnektors** in **Retail > Kanal richten > steuerliche Integration > technische Profile des Konnektors** für jeden steuerlichen Konnektor.
  - Wählen Sie einen Verbindungsnamen.
  - Wählen Sie einen Konnektortyp aus: 
      - **Lokal** - Legt diesen Typ für physische Geräte oder Bewerbungen fest, die auf einem lokalen Rechners eingerichtet wurden.
      - **Intern** - Legte diesen Typ für steuerliche Geräte und Dienstleistungen fest, die mit Retail Server verbunden sind.
      - **Extern** - Für externe steuerliche Dienste wie ein Webportal, das von der Steuerbehörde bereitgestellt wird.
    
  - Definieren Sie Einstellungen auf der Registerkarte **Verbindung**.

      
 >[!NOTE]
 > Eine aktualisierte Version einer Konfiguration, die früher geladen wurde, wird für die funktionalen und technische Profile geladen. Wenn ein entsprechender Konnektor- oder ein Dokumentanbieter bereits verwendet wird, werden Sie benachrichtigt. Standardmäßig werden alle Änderungen, die manuell in den funktionalen und technische Profilen vorgenommen wurden, gespeichert. Um diese Profile dem Standardsatz von Parametern von einer Variante zu überschreiben, klicken Sie auf **Aktualisieren** **Funktionale Profile des Konnektors** **Technische Profile des Konnektors**.
 
- Erstellen Sie **Steuerlich Erfassungsprozesses** in **Retail > Kanal einrichten > Steuerliche Integration > Steuerliche Anmeldeprozesse** für jeden eindeutigen Prozess für die steuerliche Integration. Ein Registrierungsprozess wird durch den Nummernkreis der Erfassungsschritte und der Konnektorgruppe definiert, die in jedem Schritt verwendet werden. 
  
  - Fügen Sie Erfassungsschritte dem Prozess hinzu:
      - Klicken Sie auf **Hinzufügen**.
      - Wählen Sie einen Konnektortyp aus.
      
      >[!NOTE]
      > Dieses Feld legt fest, an wo das System in einem technischen Profil für den Konnektor sucht, entweder in den Hardwareprofilen für Konnektortyp **Lokal** oder in POS-Funktionsprofilen für andere Steuerkonnektor-Typen.
      
   - Wählen Sie eine Konnektorgruppe aus.
   
     >[!NOTE]
     > Klicken Sie **Überprüfen**, um die Integrität der Anmeldeprozessstruktur zu überprüfen. Es ist empfohlen, dass Überprüfungen in folgenden Fällen vorgenommen werden:
       >- Für einen Neuzulassungsprozess, nachdem die Einstellungen einschließlich Bindung zu POS-Funktionsprofilen und -Hardwareprofilen abgeschlossen sind.
       >- Nach den Aktualisierungen zu einem vorhandenen Registrierungsprozess.

-  Binden Sie Sie steuerlichen Anmeldeprozesse zu POS-Funktionsprofilen in **Retail > Kanal einrichten > POS einrichten > POS-Profile > -Funktionsprofile**.
   - Klicken Sie **Bearbeiten** und wählen Sie **Nummer verarbeiten** auf der Registerkarte **Steuererfassungsprozess** aus.
- Binden Sie Sie die technischen Profile des Konnektors an die Hardwareprofile in **Retail > Kanal einrichten > POS einrichten> POS-Profile > -Hardwareprofile**.
   - Klicken Sie auf **Bearbeiten**, und klicken Sie auf **Neu** auf der Registerkarte **Steuerliches Technik-Profil**.
   - Wählen Sie einen Konnektor für das technische Profil im Feld **Profilnummer** aus.
   
     >[!NOTE]
     > Sie können mehrere technische Profile einem Hardwareprofil hinzufügen. Allerdings wird dieses nicht unterstützt, wenn einHardwareprofils mehr als eine Schnittmenge mit einer beliebigen Konnektorgruppe hat. Um falsche Einstellungen zu vermeiden, wird empfohlen dass Sie den Registrierungsprozess überprüfen nachdem Sie alle Hardwareprofile aktualisiert haben.

