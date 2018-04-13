--- 
title: "Zahlungsbelegformats für Projektrechnungen einrichten"
description: "Unternehmen fügen Rechnungen in der Regel gedruckte Zahlungsbelege bei, um Debitoren zu unterstützen und einen Zahlungsnachweis für Buchungen und den Ausgleich von Konten zur Verfügung zu haben."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 02/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 9700571110a1b488e250dd8ee7b8c5c8f15cbc01
ms.contentlocale: de-de
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Zahlungsbelegformats für Projektrechnungen einrichten

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Unternehmen fügen Rechnungen in der Regel gedruckte Zahlungsbelege bei, um Debitoren zu unterstützen und einen Zahlungsnachweis für Buchungen und den Ausgleich von Konten zur Verfügung zu haben. Der Zahlungsbeleg kann neben Verkaufsrechnungen und Freitextrechnungen auch für Projekt- oder Servicerechnungen, Mahnschreiben, Zinsrechnungen und Kontoauszüge verwendet werden. Richten Sie für die Verarbeitung von Zahlungsbelegen zuerst die Kreditorenkennung und die Zahlungsbelegformate ein.

Für diese Prozedur wird das Demo-Unternehmen DEMF verwendet. 

Diese Funktion ist für juristische Personen verfügbar, deren primäre Adresse sich in Dänemark befindet.


## <a name="set-up-a-creditor-id-number"></a>Einrichten einer Kreditorenkennung
1. Wechseln Sie zu Organisationsverwaltung > Organisationen > Juristische Personen.
2. Erweitern oder reduzieren Sie den Abschnitt "Bankkontoinformationen".
3. Klicken Sie auf "Bearbeiten".
4. Geben Sie einen festen Wert in das Feld "FI-Creditor-Kennung" ein.
5. Klicken Sie auf "Speichern".
6. Schließen Sie die Seite.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Einrichten eines Zahlungsbelegformats für Rechnungen, Zinsrechnungen, Mahnschreiben und Kontoauszüge
1. Wechseln Sie zu "Debitoren" > "Einstellungen" > "Formulare" > "Formulareinstellungen".
2. Klicken Sie auf die Registerkarte "Rechnung".
3. Wählen Sie eine Option im Feld "Zugeordnetes Zahlungsformular für Debitorenrechnung" aus.
    * Keiner – Keinen Zahlungsbeleg drucken. Wählen Sie diese Option aus, wenn die Währung des Zahlungsbetrags nicht Dänische Kronen (DKK) ist.   FIK 751 - Drucken Sie einen FIK 751-Zahlungsbeleg, wenn Sie den Zahlungsbetrag und das Fälligkeitsdatum manuell auf den Zahlungsbeleg schreiben möchten.   FIK 752 - Drucken Sie einen FIK 752 Zahlungsbeleg, wenn Sie einen vom Computer generierten Zahlungsbeleg mit einem vorgedruckten Zahlungsbetrag und einem Fälligkeitsdatum verwenden möchten.  
4. Klicken Sie auf "Speichern".
5. Klicken Sie auf die Registerkarte "Freitextrechnung".
6. Wählen Sie eine Option im Feld "Zugeordnetes Zahlungsformular für Freitextrechnung" aus.
    * Keiner – Keinen Zahlungsbeleg drucken. Wählen Sie diese Option aus, wenn die Währung des Zahlungsbetrags nicht Dänische Kronen (DKK) ist.   FIK 751 - Drucken Sie einen FIK 751 Zahlungsbeleg, wenn Sie den Zahlungsbetrag und das Fälligkeitsdatum manuell auf den Zahlungsbeleg schreiben möchten.   FIK 752 - Drucken Sie einen FIK 752 Zahlungsbeleg, wenn Sie einen vom Computer generierten Zahlungsbeleg mit einem vorgedruckten Zahlungsbetrag und einem Fälligkeitsdatum verwenden möchten.  
7. Klicken Sie auf "Speichern".
8. Klicken Sie auf die Registerkarte "Zinsrechnung".
9. Wählen Sie eine Option im Feld "Zugeordnetes Zahlungsformular für Zinsrechnung" aus.
    * Keiner – Keinen Zahlungsbeleg drucken. Wählen Sie diese Option aus, wenn die Währung des Zahlungsbetrags nicht Dänische Kronen (DKK) ist.   FIK 751 - Drucken Sie einen FIK 751 Zahlungsbeleg, wenn Sie den Zahlungsbetrag und das Fälligkeitsdatum manuell auf den Zahlungsbeleg schreiben möchten.   FIK 752 - Drucken Sie einen FIK 752 Zahlungsbeleg, wenn Sie einen vom Computer generierten Zahlungsbeleg mit einem vorgedruckten Zahlungsbetrag und einem Fälligkeitsdatum verwenden möchten.  
10. Klicken Sie auf "Speichern".
11. Klicken Sie auf die Mahnschreibenregisterkarte.
12. Wählen Sie eine Option im Feld "Zugeordnetes Zahlungsformular für Mahnschreiben" aus.
    * Keiner – Keinen Zahlungsbeleg drucken. Wählen Sie diese Option aus, wenn die Währung des Zahlungsbetrags nicht Dänische Kronen (DKK) ist.   FIK 751 - Drucken Sie einen FIK 751 Zahlungsbeleg, wenn Sie den Zahlungsbetrag und das Fälligkeitsdatum manuell auf den Zahlungsbeleg schreiben möchten.   FIK 752 - Drucken Sie einen FIK 752 Zahlungsbeleg, wenn Sie einen vom Computer generierten Zahlungsbeleg mit einem vorgedruckten Zahlungsbetrag und einem Fälligkeitsdatum verwenden möchten.  
13. Klicken Sie auf "Speichern".
14. Klicken Sie auf die Registerkarte "Kontoauszug".
15. Wählen Sie eine Option im Feld "Zugeordnetes Zahlungsformular in Kontoauszug" aus.
    * Keiner – Keinen Zahlungsbeleg drucken. Wählen Sie diese Option aus, wenn die Währung des Zahlungsbetrags nicht Dänische Kronen (DKK) ist.   FIK 751 - Drucken Sie einen FIK 751 Zahlungsbeleg, wenn Sie den Zahlungsbetrag und das Fälligkeitsdatum manuell auf den Zahlungsbeleg schreiben möchten.   FIK 752 - Drucken Sie einen FIK 752 Zahlungsbeleg, wenn Sie einen vom Computer generierten Zahlungsbeleg mit einem vorgedruckten Zahlungsbetrag und einem Fälligkeitsdatum verwenden möchten.  
16. Klicken Sie auf "Speichern".
17. Schließen Sie die Seite.


