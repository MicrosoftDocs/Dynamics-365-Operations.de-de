---
title: Verwenden von Power Portal mit dem Partei-Datenmodell
description: In diesem Thema werden die Änderungen an den Power Portal-Webrollen aufgrund des Partei-Datenmodells in Duales Schreiben beschrieben.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 3b03603038d05305c63fc2890a196670ae343e53
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358616"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Verwenden von Power Portal mit dem Partei-Datenmodell

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Die Duales Schreiben-Anwendungsorchestrierungslösung, Version 2.0.999.0 und höher enthält Änderungen des Datenmodells an Partei und globalem Adressbuch für die Konto- und Kontakttabellen. Die Änderungen ermöglichen Viele-zu-Viele-Beziehungen, die erweiterte Geschäftsszenarien unterstützen. Diese Änderungen werden von Portal-Webrollen, einschließlich des Kundenportals, nicht unterstützt, die standardmäßig ausgeliefert wurden oder in Ihrer Umgebung vorhanden waren, bevor Sie Duales Schreiben installiert haben. Damit die Webrollen wie erwartet funktionieren, müssen Sie mithilfe des neuen Datenmodells neue Webrollen erstellen. 

Zusammenfassend hat sich die Art und Weise, wie die Tabellen interagieren, geändert, aber die Tabellenberechtigungen im Kundenportal haben sich nicht geändert. In diesem Thema wird erläutert, wie Sie neue Webrollen erstellen, die mit dem neuen erweiterten Datenmodell funktionieren.

Dieses Diagramm zeigt die Tabellenbeziehung **ohne** das Datenmodell der Partei und des globalen Adressbuchs:

   ![ohne Parteimodell.](media/without-party-model.PNG)

Dieses Diagramm zeigt die Tabellenbeziehung **mit** dem Datenmodell der Partei und des globalen Adressbuchs:

   ![mit Parteimodell.](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Erstellen einer neuen Tabellenberechtigung

Gehen Sie folgendermaßen vor, um diese neuen Tabellenberechtigungen zu erstellen:

1. Melden Sie sich bei [Power Apps](https://make.powerapps.com) an und gehen Sie zu Ihren Apps.
2. Wählen Sie Ihre Portal Management-App aus.
3. Wählen Sie in der Seitenleiste **Sicherheit > Tabellenberechtigungen** aus.

    Sie müssen drei neue Berechtigungen erstellen:

    + Kontakt-zu-Partei-Verbindung
    + Partei-zu-Konto-Verbindung
    + Konto-zu-Auftrag-Verbindung

4. Erstellen und speichern Sie eine neue Berechtigung für die Kontakt-zu-Partei-Verbindung, indem Sie die folgenden Parameter festlegen:

    + **Name**: Partei-zu-Konto-Verbindung (oder Ihre Wahl)
    + **Tabellenname**: msdyn_contactforparty
    + **Website**: Kundenportal
    + **Umfang**: Kontakt
    + **Rechte**: Alles auswählen
    + **Webrollen**: Authentifizierte Benutzer, Kundenvertreter (oder Ihre Wahl)

5. Erstellen und speichern Sie eine neue Berechtigung für die Partei-zu-Konto-Verbindung, indem Sie die folgenden Parameter festlegen:

    + **Name**: Partei-zu-Konto-Verbindung (oder Ihre Wahl)
    + **Tabellenname**: Konto
    + **Website**: Kundenportal
    + **Umfang**: Übergeordnetes Element
    + **Rechte**: Alles auswählen
    + **Berechtigung für übergeordnete Tabelle**: Kontakt-zu-Partei-Verbindung

6. Erstellen und speichern Sie eine neue Berechtigung für die Konto-zu-Auftrag-Verbindung, indem Sie die folgenden Parameter festlegen:

    + **Name**: Konto-zu-Auftrag-Verbindung (oder Ihre Wahl)
    + **Tabellenname**: salesorder
    + **Website**: Kundenportal
    + **Umfang**: Übergeordnetes Element
    + **Rechte**: Alles auswählen
    + **Berechtigung für übergeordnete Tabelle**: Partei-zu-Konto-Verbindung

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
