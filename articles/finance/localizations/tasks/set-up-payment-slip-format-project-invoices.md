---
title: Zahlungsbelegformats für Projektrechnungen einrichten
description: In diesem Thema wird erläutert, wie gedruckte Zahlungsbelege an Projektrechnungen angefügt werden und einen Zahlungsnachweis für Buchungen und den Ausgleich von Konten zur Verfügung stellen.
author: EvgenyPopovMBS
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88bdce7697e47fc49b6ffb2fe6a8a468860f41f3
ms.sourcegitcommit: 2fba4f2ef7e513357366fc640befe0d2f7bc31f5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/05/2021
ms.locfileid: "7601499"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Zahlungsbelegformats für Projektrechnungen einrichten

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
