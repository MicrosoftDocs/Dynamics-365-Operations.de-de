---
title: Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS
description: In diesem Thema wird beschrieben, wie Sie eine neue Berichterstellungskonfiguration erstellen, die Anwendungsmetadaten enthält.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9609da50482f39bafe65d3a7b655e5047c74bdba
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560116"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a>Vorbereiten von Anwendungs-Metadaten zur Verwendung in RCS
[!include [banner](../../includes/banner.md)]

Die folgenden Schritte erklären, wie ein Benutzer in der Systemadministratorenrolle oder der elektronischen Berichtsentwicklerrolle eine neue elektronische Berichterstellungskonfiguration (ER) erstellen kann, die die Anwendungsmetadaten für das Entwerfen der ER-Modellzuordnungskonfigurationen im Regulatory Configuration Service (RCS) enthält. Diese Konfiguration wird für das Entwerfen einer Beispiel-ER-Modellzuordnungskonfiguration verwendet, um auf Außenhandelsbuchungen zuzugreifen. In diesem Beispiel erstellen Sie eine Konfiguration für das Beispielunternehmen, Litware, Inc. Diese Schritte können in jedem Unternehmen ausgeführt werden. Um diese Schritte auszuführen, müssen Sie zunächst die Schritte im Thema [Konfigurationsanbieter erstellen und als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen.

## <a name="prerequisites"></a>Voraussetzungen
1.    Wechseln Sie zu **Organisationsverwaltung**  >  **Arbeitsbereiche**  >  **Elektronische Berichterstellung**. 
2.    Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als **Aktiv** markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in der Prozedur [Konfigurationsanbieter erstellen und diesen als aktiv markieren](er-configuration-provider-mark-it-active-2016-11.md) abschließen. 
3.    Klicken Sie auf **Metadatenkonfiguration**. 
4.    Angenommen, RCS wird verwendet um eine ER-Lösung für eine Finance and Operations Anwendung zu entwerfen, die elektronische Dokumente erstellt, die Informationen aus der Außenhandelsgeschäftsdomäne enthält. Um die Zuordnung zwischen ER-Datenmodell und Quellen der erforderlichen Daten anzugeben, benötigen wir in RCS Zugriff auf die Metadaten in der Finance and Operations Anwendung Daher konfigurieren wir als Teil der ER-Lösung eine neue ER-Metadatenkonfiguration, die alle Metadaten enthält, die zur Generierung der ER-Berichte für ausgewählte Geschäftsdomänen derzeit erforderlich sind. 

## <a name="add-metadata-configuration"></a>Metadatenkonfiguration hinzufügen 
1.    Klicken Sie auf **Konfiguration erstellen** um das Dropdown-Dialogfeld zu öffnen. 
2.    Geben Sie im Feld **Name** den Typ Außenhandelsmetadaten ein. 
3.    Klicken Sie auf **Konfiguration erstellen**. 
4.    Klicken Sie auf **Designer**. 
5.    Klicken Sie auf **Hinzufügen**. 
  
> [!NOTE]
> Sie können alle Metadaten für die gesamte Anwendung, ausgewählten Modelle oder ausgewählten Module auswählen. Beachten Sie, dass in diesem Fall die folgenden Metadaten automatisch hinzugefügt werden: Tabellen von Datensätzen, Aufzählungen und erweiterte Datentypen. Wenn zusätzliche Arten von Metadaten erforderlich sind, müssen sie ggf. manuell hinzugefügt werden. 
 
Wir haben einige zum Außenhandel zugehörige Metadaten, indem wir manuell Metadatenelemente auswählen. 
  
6.    Klicken Sie auf **Datenquelle hinzufügen**. 
7.    Klicken Sie auf **Tabellendatensätze**. 
8.    Verwenden Sie den Schnellfilter, um im Feld **Name** nach dem Wert Intrastat zu filtern. 
9.    Wählen Sie den **Intrastat**-Tabellendatensatz aus. 
10.    Klicken Sie auf **OK**.
  
Es werden Metadateninformationen zur Intrastat-Tabelle der Datensätze hinzugefügt. 
  
11.    Erweitern Sie in der Struktur I **TAbellendatensätze Intrastat**\>**Beziehungen**. 
12.    Wählen Sie in der Strukturdarstellung **Intrastat Tabellendatensätze**\>**Relations\IntrastatCommodity (Table records EcoResCategory)** aus.     
13.    Klicken Sie auf **Hinzufügen von Metadaten**. 
  
> [!NOTE]
> Metadaten über erforderliche Beziehungen für ausgewählte Tabelle von Datensätzen müssen manuell hinzugefügt werden. 
  
16.    Klicken Sie auf **Datenquelle hinzufügen**. 
17.    Klicken Sie auf **Enumeration**. 
18.    Verwenden Sie den Schnellfilter, um im Feld **Name** nach dem Wert IntrastatDirection zu filtern. 
19.    Wählen Sie den Datensatz **IntrastatDirections-Enumeration** aus. 
20.    Klicken Sie auf **OK**. 
21.    Klicken Sie auf **Speichern**.  
22.    Schließen Sie die Seite. 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a>Schließt die Entwurfsversion der Metadatenkonfiguration ab
1.    Klicken Sie auf **Status ändern**. 
2.    Klicken Sie auf **Abgeschlossen**. 
3.    Klicken Sie auf **OK**. 
4.    Wählen Sie die abgeschlossene Version **1**. 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a>Exportiert die abgeschlossene Version der Metadatenkonfiguration der Anwendung als XML-Datei
1.    Klicken Sie auf **Austauschen**. 
2.    Klicken Sie auf **Als XML-Datei exportieren**. 
3.    Klicken Sie auf **OK**. 
    
Die erstellte ER-Metadatenkonfiguration ist als XML Datei gespeichert, die in RCS importiert werden kann und als die Informationsquelle über Metadaten für die Außenhandelsdomäne verwendet werden kann. Auf Basis dieser Informationen können wir die Zuordnung zwischen Bewerbungsmetadaten und ER-Datenmodell angeben.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]