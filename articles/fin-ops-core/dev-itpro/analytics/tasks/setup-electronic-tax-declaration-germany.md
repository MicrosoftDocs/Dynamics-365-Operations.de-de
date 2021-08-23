---
title: Einrichtung der elektronischen Steuererklärung für Deutschland
description: Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxElectronicDeclarationSetup, TaxElectronicCertificates, TaxElectronicHTTPServer
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f006ba72471ae4a8e01b4fc67a79fc32e37ecbb43d909955dd24f018bb70fb5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750587"
---
# <a name="set-up-electronic-tax-declaration-for-germany"></a>Einrichtung der elektronischen Steuererklärung für Deutschland

[!include [banner](../../includes/banner.md)]

Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch.

Diese Prozedur wurde mit dem Demodatenunternehmen DEMF erstellt. 

Diese Funktion ist für juristische Personen verfügbar, deren primäre Adresse sich in Deutschland befindet.

Sie sollten ein gültiges Zertifikat (wie test-soft-pse.pfx) und eine Steuerbehördenbescheinigung (Coala2019.pem.cer) verwenden bevor Sie dieses Verfahren ausführen können.


1. Wechseln Sie zu "Steuer" > "Einstellungen" > "Mehrwertsteuer" > "Einrichtung der elektronischen Steuererklärung".
2. Klicken Sie auf "Bearbeiten".
3. Wählen Sie "Ja" im Feld "Authentifizierung".
4. Geben Sie im Feld "Artikelnummer" einen Wert ein oder wählen Sie einen Wert aus.
    * Wie eine Komponente, die Sie von Konfiguration Kreditbriefen Elster (Modell und Stil) für generische elektronische Berichterstellung hochladen sollen.  
5. Elektronische Steuerzertifikate anklicken
6. Klicken Sie auf "Neu".
7. Geben Sie im Feld "Gruppenkennung" einen Wert ein oder wählen Sie einen Wert aus.
    * Sie sollten Bescheinigungen nach Microsoft Management Console zunächst einrichten und Anzeigenamen zuweisen, die in diesen Schritten verwendet werden.  
    * In MMC für private Bescheinigung gehen Sie mit einem rechten Mausklcik zu Zertifikate / Personal/ Zertifikate. 
    * Klicken Sie im Kontextmenü auf „Alle Aufgaben > Import“. Gewähren Sie Leseberechtigungen der Bescheinigung für den Benutzer, der die Übermittlung an.     * Klicken Sie in der MMC mit der rechten Maustaste auf das Zertifikat und verwenden Sie „Alle Aufgaben/Private Schlüssel verwalten“. 
    * Wählen Sie den Benutzer aus und fügen Sie eine Leseberechtigung hinzu.  
    * Bei einem Steuerbehördenzertifikat klicken Sie in MMC mit der rechten Maustaste auf „Vertrauenswürdige Stammzertifizierungsstelle“  
    * Importieren Sie „Coala2019.pem.cer“.  
8. Geben Sie im Feld Wert einen Referenztyp ein.
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.
11. Klicken Sie auf HTTP-Server.
    * HTTP-URL-Adressen werden aus der Behörde bereitgestellt und können von der Behörde geändert werden. Microsoft stellt Standardadressen, die vom System zufällig verwendet werden.  
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.
14. Klicken Sie auf "Speichern".



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]