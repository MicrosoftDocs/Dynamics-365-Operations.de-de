--- 
title: "Zuordnen von Komponenten des erstellten Formats zu Datenmodellelementen für elektronische Berichterstellung"
description: "Die folgende Prozedur zeigt, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder der Rolle „Entwickler für elektronische Berichterstellung” Datenmodellelemente Komponenten der erstellten Elektronischen Berichterstellungs-(ER)-Konfiguration zuordnen kann, die ein elektronisches Dokumentformat für die Zahlungsgeschäftsdomäne definiert."
author: NickSelin
manager: AnnBe
ms.date: 02/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: df3dcd6d5242c516f254450a727d8a754bd74f6a
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---
# <a name="map-components-of-the-created-format-to-data-model-elements-for-electronic-reporting-er"></a>Zuordnen von Komponenten des erstellten Formats zu Datenmodellelementen für elektronische Berichterstellung

[!include[task guide banner](../../includes/task-guide-banner.md)]

Die folgende Prozedur zeigt, wie ein Benutzer entweder in der Rolle „Systemadministrator” oder der Rolle „Entwickler für elektronische Berichterstellung” Datenmodellelemente Komponenten der erstellten Elektronischen Berichterstellungs-(ER)-Konfiguration zuordnen kann, die ein elektronisches Dokumentformat für die Zahlungsgeschäftsdomäne definiert. Dieses Format wird später verwendet, um elektronische Dokumente zur Verarbeitung von Zahlungen zu generieren. In diesem Beispiel erstellen Sie eine Formatkonfiguration für das Beispielunternehmen „Litware, Inc.”. Diese Schritte können an einem beliebigen Unternehmen ausgeführt werden, da die ER-Konfiguration von allen Unternehmen genutzt werden. Um diese Schritte abzuschließen, müssen Sie zuerst die Schritte im Aufgabenleitfaden „Eine Formatkonfiguration erstellen” abschließen.


## <a name="select-a-format-configuration"></a>Eine Formatkonfiguration auswählen
1. Wechseln Sie zu Organisationsverwaltung > Arbeitsbereiche > Elektronische Berichterstellung.
2. Klicken Sie auf "Berichterstellungskonfigurationen".
3. Erweitern Sie "Zahlungen (vereinfachtes Modell)" in der Struktur.
4. Wählen Sie "Zahlungen (vereinfachtes Modell)\BACS (Großbritannien, fiktiv)" in der Struktur aus.
5. Klicken Sie auf Designer.

## <a name="map-format-components-to-data-model-elements"></a>Weisen Sie Formatkomponenten für das Zuordnen zu den Datenmodellelementen zu
1. Klicken Sie „Erweitern/reduzieren”.
2. Klicken Sie auf die Registerkarte Zuordnung.
3. Erweitern Sie in der -Struktur den Knoten 'Modell'.
4. Wählen Sie in der Struktur „XML\Nachricht\ProcessingDate\DateTime” aus.
5. Wählen Sie „Modell\ProcessingDateTime” in der Struktur aus.
6. Klicken Sie auf Binden.
7. Wählen Sie in der Struktur „XML\Nachricht\MessageId\Zeichenfolge” aus.
8. Wählen Sie in der Struktur „Modell\MessageIdentification” aus.
9. Klicken Sie auf Binden.
10. Erweitern Sie 'Modell\Zahlungen' in der Struktur.
11. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Betrag\Zeichenfolge” aus.
12. Wählen Sie „Modell\Zahlungen\InstructedAmount” in der Struktur aus.
13. Klicken Sie auf Binden.
14. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\TransDate\DateTime” aus.
15. Wählen Sie „Modell\Zahlungen\TransactionDate” in der Struktur aus.
16. Klicken Sie auf Binden.
17. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Beschreibung\Zeichenfolge” aus.
18. Wählen Sie 'Modell\Zahlungen\Beschreibung' in der Struktur aus.
19. Klicken Sie auf Binden.
20. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Währung\Zeichenfolge” aus.
21. Wählen Sie in der Struktur "Modell\Zahlungen\Währung" aus.
22. Klicken Sie auf Binden.
23. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\ID” aus.
24. Wählen Sie in der Struktur „Modell\Zahlungen\End2EndID” aus.
25. Klicken Sie auf Binden.
26. Erweitern Sie 'Modell\Payments\Creditor' in der Struktur.
27. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Konto".
28. In der Struktur erweitern Sie "Modell\Zahlungen\Kreditor\Agent".
29. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Name\Zeichenfolge” aus.
30. Wählen Sie 'Modell\Payments\Creditor\Account\Name' in der Struktur aus.
31. Klicken Sie auf Binden.
32. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\RoutingNumber\Zeichenfolge” aus.
33. Wählen Sie in der Struktur Folgendes aus: „Modell\Zahlungen\Kreditor\Agent\RoutingNumber”.
34. Klicken Sie auf Binden.
35. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Kreditor\Bank\AccountNumber\Zeichenfolge” aus.
36. Wählen Sie 'Modell\Payments\Creditor\Account\Number' in der Struktur aus.
37. Klicken Sie auf Binden.
38. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Name\Zeichenfolge” aus.
39. Erweitern Sie 'Modell\Payments\Debtor' in der Struktur.
40. In der Struktur erweitern Sie "Modell\Zahlungen\Debtor\Konto".
41. Erweitern Sie 'Modell\Payments= Transactions\Agent' in der Struktur.
42. Wählen Sie 'Modell\Payments\Debtor\Account\Name' in der Struktur aus.
43. Klicken Sie auf Binden.
44. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\RoutingNumber\Zeichenfolge” aus.
45. Wählen Sie in der Struktur Folgendes aus: „Modell\Zahlungen\Debitor\Agent\RoutingNumber”.
46. Klicken Sie auf Binden.
47. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel\Zahlender\Bank\AccountNumber\Zeichenfolge” aus.
48. Wählen Sie 'Modell\Payments\Debtor\Account\Number' in der Struktur aus.
49. Klicken Sie auf Binden.
50. Wählen Sie in der Struktur „XML\Nachricht\Zahlungen\Artikel” aus.
51. Wählen Sie 'Modell\Zahlungen' in der Struktur aus.
52. Klicken Sie auf Binden.
53. Klicken Sie auf "Speichern".

## <a name="validate-format-mapping"></a>Formatzuordnung überprüfen
1. Klicken Sie auf "Überprüfen".
    * Überprüft die neue Zuordnung, um sicherzustellen, dass alle Bindungen in Ordnung sind.  
2. Schließen Sie die Seite.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Ändern Sie den Status der aktuellen Version der Format-Konfiguration
    * In den nächsten Schritten ändern Sie den Status der Formatkonfiguration von „Entwurf” zu „Abgeschlossen”, um sie für die Zahlungsdokumentgenerierung verfügbar zu machen.  
1. Klicken Sie auf "Status ändern".
2. Klicken Sie auf "Abgeschlossen".
3. Geben Sie im Feld "Beschreibung" einen Wert ein.
    * Beispielsweise „Version 1”.  
4. Klicken Sie auf "OK".
5. Wählen Sie die abgeschlossene Version der aktuellen Konfiguration aus.
    * Beachten Sie, dass die Konfiguration als abgeschlossene Version 1.1 gespeichert wird: Version 1 des Formats basierend auf der Version 1 des Datenmodells.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Definieren Sie Gültigkeitsdatum für abgeschlossene Version des Formats
    * Jede Formatversion kann so konfiguriert werden, wie verfügbar für die Verwendung, die von einem bestimmten Datum startet. Wenn mehr als eine Formatversion an einem bestimmten Datum aktiv ist, wird das neueste Format (auf Grundlage der Versionsnummer) für die Verwendung ausgewählt. Der Sitzungsdatumswert wird für die richtige Versionsauswahl verwendet.  

## <a name="restrict-access-to-created-format-from-companies"></a>Einschränken des Zugriffs auf erstelltes Format von Unternehmen
1. Erweitern Sie den Abschnitt „ISO-Land-/Regionencode”.
    * Jeder Formatzugriff kann beschränkt werden, indem bestimmte Länder/Regionen angibt, in denen ein Format anwendbar ist. Wenn die Länder-/Regionenliste für ein bestimmtes Format leer ist, kann dieses Format in einem beliebigen Unternehmen verwendet werden. Wenn mehrere ISO-Länder-/Regionscodes in die Länder-/Regionenliste eingefügt werden, kann dieses Format nur in Unternehmen verwendet werden, wenn die primäre Adresse sich in dem Land/der Region befindet.  


