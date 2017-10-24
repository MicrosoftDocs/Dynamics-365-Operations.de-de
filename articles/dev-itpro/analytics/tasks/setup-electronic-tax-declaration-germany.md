--- 
title: "Elektronische Steuererklärung einrichten (Deutschland)"
description: "Diese Prozedur läuft Sie nach elektronischer Steuererklärung durch."
author: NickSelin
manager: AnnBe
ms.date: 02/17/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Germany
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 881c7b5ba2e9daa56d6c1b98224bde675efc741d
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-electronic-tax-declaration-germany"></a>Elektronische Steuererklärung einrichten (Deutschland)

[!include[task guide banner](../../includes/task-guide-banner.md)]

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
    * Sie sollten Bescheinigungen nach Microsoft Management Console zunächst einrichten und Anzeigenamen zuweisen, die in diesen Schritten verwendet werden.  In MMC für private Bescheinigung "in den Bescheinigungen/zu persönliche /Certificates", fahren rechten Mausklick.  Im Kontextmenü klicken Sie auf Alle Aufgaben > auf Importieren…. Gewähren Sie Leseberechtigungen der Bescheinigung für den Benutzer, der die Übermittlung ausführt.  In MMC klicken Sie auf der Bescheinigung mit der rechten Maustaste, und verwenden Sie alle Aufgaben/Verwalten von private Schlüssel - Wählen Sie den Benutzer aus und fügen Sie Leseberechtigung hinzu.  Für Steuerbehördenbescheinigung MMC-Rechtsklick "vertraute im Stammzertifikats-" Import " Coala2019.pem.cer".  
8. Geben Sie im Feld Wert einen Referenztyp ein.
9. Klicken Sie auf "Speichern".
10. Schließen Sie die Seite.
11. Klicken Sie auf HTTP-Server.
    * HTTP-URL-Adressen werden aus der Behörde bereitgestellt und können von der Behörde geändert werden. Microsoft stellt Standardadressen, die vom System zufällig verwendet werden.  
12. Klicken Sie auf "Speichern".
13. Schließen Sie die Seite.
14. Klicken Sie auf "Speichern".


