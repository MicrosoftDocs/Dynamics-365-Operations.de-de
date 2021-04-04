---
title: Konfigurationen zum Generieren von Berichten im Office-Format entwerfen, die eingebettete Bilder haben
description: In diesem Thema wird beschrieben, wie die Konfigurationen entworfen werden, die elektronische Dokumente in Excel- und Word-Formaten generieren, die eingebettete Bilder enthalten.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3585d99ce2db8a7833b11a4bcc68f9e91023b9cd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569484"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfigurationen zum Generieren von Berichten im Office-Format entwerfen, die eingebettete Bilder haben

[!include [banner](../../includes/banner.md)]

Um dies Schritte in dieser Prozedur auszuführen, müssen Sie zuerst die Prozedur „ER – Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen. Mit dieser Prozedur wird erklärt, wie die Konfigurationen zur elektronischen Berichterstellung (EB) entworfen werden, um ein Microsoft Excel- oder Word-Dokument zu generieren, das eingebettete Bilder enthält. In dieser Prozedur erstellen Sie die erforderlichen EB-Konfigurationen für das Beispielunternehmen Litware, Inc.. Diese Schritte können mithilfe des USMF-Datasets abgeschlossen werden. Diese Prozedur ist für Benutzer bestimmt, die die Rolle des Systemadministrators oder des elektronischen Berichtsentwicklers haben, die ihnen zugewiesen sind. Bevor Sie beginnen, laden Sie die im Hilfethema aufgeführten Dateien herunter und speichern Sie sie, [Betten Sie Bilder und Formen in Dokumente ein, die Sie mit ER](../electronic-reporting-embed-images-shapes.md) erzeugen. Die Dateien sind: Modell für Schecks.xml, Druckformat für Schecks.xml, Unternehmenslogo.png, Signaturbild.png, Signaturbild 2.png und Scheckvorlage Word.docx.

## <a name="verify-prerequisites"></a>Überprüfung der erforderlichen Software  
 1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.  
 2. Überprüfen Sie, dass der Konfigurationsanbieter für Beispielunternehmen „Litware, Inc.” verfügbar und als aktiv markiert ist. Wenn Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zuerst die Schritte in der Prozedur „Konfigurationsanbieter erstellen und als aktiv markieren“ abschließen.   
 3. Klicken Sie auf "Berichterstellungskonfigurationen".  
 
## <a name="add-a-new-er-model-configuration"></a>Neue ER-Modellkonfiguration hinzufügen  
 1. Anstatt ein neues Modell zu erstellen, können Sie die EB-Modellkonfigurationsdatei laden (Modelle für Schecks.xml), die Sie vorher gespeichert hatten. Diese Datei enthält das Beispieldatenmodell für Zahlungsschecks und die Zuordnung des Datenmodells zu den Datenkomponenten der Dynamics 365 for Operations-Anwendung.   
 2. Klicken Sie im Versionen-Inforegister auf „Austauschen”.   
 3. Klicken Sie auf „Aus XML-Datei laden”.  
 4. Klicken Sie auf „Durchsuchen”, und wählen Sie dann „Modell” für „Schecks.xml” aus.   
 5. Klicken Sie auf "OK".  
 6. Das geladene Modell wird als Datenquelle von Informationen verwendet, um Dokumente zu generieren, die Bilder in Excel und in Word enthalten.  

## <a name="add-a-new-er-format-configuration"></a>Neues ER-Modellformat hinzufügen  
 1. Anstatt ein neues Format zu erstellen, können Sie die EB-Formatkonfigurationsdatei laden (Scheckdruckformat.xml), die Sie vorher gespeichert hatten. Diese Datei enthält das Beispiellayout des Formats, um Schecks mithilfe des vorgedruckten Formulars zu drucken und der Zuordnung dieses Formats zum Datenmodell „Modell für Schecks“.   
 2. Klicken Sie auf „Austauschen”.  
 3. Klicken Sie auf „Aus XML-Datei laden”.  
 4. Klicken Sie auf „Durchsuchen”, und wählen Sie die Datei „Scheckdruckformat.xml” aus.   
 5. Klicken Sie auf "OK".  
 6. Wählen Sie in der Struktur erweitern 'Modell für Cheques.  
 7. Wählen Sie in der Strukturdarstellung "Modell für Cheques\Cheques-Druckformat.  
 8. Das geladene Format wird verwendet, um Dokumente zu generieren, die Bilder in Excel und in Word enthalten.   

## <a name="configure-er-user-parameters"></a>Benutzerparameter der elektronischen Berichterstellung konfigurieren  
 1. Klicken Sie im Aktivitätsbereich auf Konfigurationen.  
 2. Klicken Sie auf Benutzerparameter.  
 3. Wählen Sie "Ja" im Feld "Testlaufeinstellungen".  
  Aktivieren Sie die Markierung „Entwurf ausführen“, um die Entwurfsversion des ausgewählten Formats zu starten, anstelle der abgeschlossenen Version.  
 4. Klicken Sie auf "OK".  

## <a name="configure-cash--bank-management-parameters"></a>Bargeld- und Bankverwaltungsparameter konfigurieren  
 1. Gehen Sie zu "Bargeld- und Bankverwaltung" > Bankkonten > Bankkonten.  
 2. Verwenden Sie den Schnellfilter, um im Feld "Bankkonto" nach dem Wert "USMF OPER" zu filtern.  
 3. Klicken Sie im Aktivitätsbereich auf "Einrichten".  
 4. Klicken Sie auf "Prüfen".  
 5. Erweitern Sie den Abschnitt 'Einstellungen'.  
 6. Klicken Sie auf "Bearbeiten".  
 7. Wählen Sie „Ja” im Feld „Unternehmenslogo” aus.  
 8. Klicken Sie auf „Unternehmenslogo”.  
 9. Klicken Sie auf "Ändern".  
 10. Klicken Sie auf „Durchsuchen”, und wählen die Datei aus, die Sie vorher heruntergeladen haben, nämlich „Unternehmenslogo.png”.   
 11. Klicken Sie auf "Speichern".  
 12. Schließen Sie die Seite.  
 13. Erweitern Sie den Abschnitt "Unterschrift".  
 14. Wählen Sie „Ja” im Feld „Erste Unterschrift drucken” aus.  
 15. Klicken Sie auf "Ändern".  
 16. Klicken Sie auf „Durchsuchen”, und wählen die Datei aus, die Sie vorher heruntergeladen haben, nämlich „Unterschriftsbild.png”.   
 17. Erweitern Sie den Abschnitt Kopien.  
 18. Wählen Sie im Feld „Wasserzeichen” eine Option aus.  
 19. Wählen Sie „Ja” im Feld „Generisches elektronisches Exportformat” aus.  
 20. Wählen Sie die Konfiguration „Scheckausdruckformular” aus.  
 21. Nun wird das ausgewählte EB-Format für das Drucken von Schecks verwendet.  
 22. Klicken Sie auf Anhänge.  
 23. Klicken Sie auf "Neu".  
 24. Klicken Sie auf "Datei".  
 25. Klicken Sie auf „Durchsuchen”, und wählen die Datei aus, die Sie vorher heruntergeladen haben, nämlich „Unterschriftsbild 2.png”.   
 26. Schließen Sie die Seite.  
 27. Schließen Sie die Seite.  
 28. Schließen Sie die Seite.  
 29. Wechseln Sie zu "Kasse und Bankverwaltung > Einstellungen > Parameter für Kasse- und Bankverwaltung.  
 30. Wählen Sie „Ja” im Feld „Erstellung von Testtransaktionen für inaktive Bankkonten zulassen:” aus.  
 31. Klicken Sie auf "Speichern".  
 32. Schließen Sie die Seite.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]