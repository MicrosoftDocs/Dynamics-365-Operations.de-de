---
title: ER Generieren Sie elektronische Dokumente für Zahlungen mithilfe einer Formatkonfiguration
description: In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Formatkonfiguration für elektronische Berichterstellung (ER) verwenden kann, um elektronische Dokumente zur Verarbeitung von Zahlungen zu generieren.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179e8a20dd65847f90872ae0e56b3e4991a6b00e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184990"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>ER Generieren Sie elektronische Dokumente für Zahlungen mithilfe einer Formatkonfiguration

[!include [task guide banner](../../includes/task-guide-banner.md)]

In den folgenden Schritten wird erläutert, wie ein Benutzer, der der Systemadministratorrolle oder der Rolle "Entwickler für elektronische Berichterstellung" angehört, eine neue Formatkonfiguration für elektronische Berichterstellung (ER) verwenden kann, um elektronische Dokumente zur Verarbeitung von Zahlungen zu generieren. Diese Schritte können im GBSI-Beispielunternehmen ausgeführt werden.

Um diese Schritte abzuschließen, müssen Sie zunächst die Schritte in der Prozedur "Eine Konfiguration mit Zahlungsformatdokument erstellen" abschließen.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Ändern Sie die Konfiguration der Methode der elektronischen Zahlung
1. Wechseln Sie zu "Kreditoren" > "Zahlungseinstellungen" > "Zahlungsmethoden".
2. Schalten Sie den Abschnitt "Dateiformat" um, um ihn bei Bedarf zu erweitern.
3. Verwenden Sie den Schnellfilter, um Datensätze zu suchen. Filtern Sie beispielsweise nach dem Feld "Zahlungsmethode" mit einem Wert von "Elektronisch".
4. Klicken Sie auf "Bearbeiten".
5. Legen Sie das Feld "Allgemeine elektronische Berichterstellung" auf "Ja" fest.
    * Wählen Sie "Ja" aus, um das "Allgemeine elektronische Berichterstellungsmuster" für die Zahlungsdateigenerierung zu verwenden.  
6. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
7. Wählen Sie die Formatkonfiguration BACS (Großbritannien, fiktiv) aus.
8. Klicken Sie auf "Speichern".
9. Schließen Sie die Seite.

## <a name="test-the-format-of-generated-payment-files"></a>Testen Sie das Format von generierten Zahlungsdateien
1. Wechseln Sie zu "Kreditoren" > "Zahlungen" > "Zahlungserfassung".
2. Klicken Sie auf "Neu".
3. Markieren Sie in der Liste die ausgewählte Zeile.
4. Klicken Sie im Feld "Name" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
5. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie "VendPay" aus.  
6. Klicken Sie auf "Speichern".
7. Klicken Sie auf "Positionen".
8. Geben Sie im Feld "Unternehmen" die Zeichenfolge "DEMF" ein.
    * DEMF  
9. Geben Sie im Feld "Konto" die Werte "De-01001" an.
    * DE- 01001  
10. Geben Sie im Feld "Beschreibung" die Bezeichnung "Zahlung" ein.
    * Zahlung  
11. Geben Sie im Feld "Soll" eine Zahl ein.
    * 1.000  
12. Klicken Sie auf die Registerkarte Zahlung.
13. Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
14. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie den Elektronischen Wert aus.  
15. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
16. Klicken Sie auf "Speichern".
17. Klicken Sie auf Zahlungen generieren.
18. Klicken Sie im Feld "Zahlungsmethode" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
19. Suchen Sie in der Liste den gewünschten Datensatz, und wählen Sie ihn aus.
    * Wählen Sie den Elektronischen Wert aus.  
20. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie den Elektronischen Wert aus.  
21. Geben Sie im Feld "Dateiname" einen Wert ein.
    * Geben Sie beispielsweise "Zahlungen" ein.  
22. Klicken Sie im Feld "Bankkonto" auf die Dropdown-Schaltfläche, um die Suche zu öffnen.
23. Klicken Sie in der Liste auf den Link in der ausgewählten Zeile.
    * Wählen Sie das Wert "GBSI OPER" aus.  
24. Klicken Sie auf "OK".
25. Klicken Sie auf "OK".
    * Analysieren Sie die erstellte Zahlungsdatei im XML-Format. Vergleichen Sie diese mit dem entworfenen Dokumentlayout und den definierten Zahlungstransaktionsattributen.  
