---
title: Modul Einchecken für das Abholung
description: Dieses Thema behandelt das Modul „Einchecken zur Abholung“ und erklärt, wie Sie es in Microsoft Dynamics 365 Commerce einstellen.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270582"
---
# <a name="check-in-for-pickup-module"></a>Modul Einchecken für das Abholung

[!include [banner](includes/banner.md)]

Dieses Thema behandelt das Modul „Einchecken zur Abholung“ und erklärt, wie Sie es in Microsoft Dynamics 365 Commerce einstellen.

Das Modul „Check-in für Abholung“ stellt eine Bestätigungsseite für Debitor zur Verfügung, die die Funktionalitäten Dynamics 365 Commerce zum Einchecken von Kunden nutzt, um eine Filiale über ihre Ankunft zu informieren. Mit dem Modul „Check-in für Abholung“ können Sie auch ein Formular konfigurieren, das zusätzliche Informationen von den Debitor sammelt, um die Lieferung der Bestellung zu erleichtern. Zu diesen Informationen gehören die Parkplatznummer eines Debitors sowie die Marke und das Modell seines Fahrzeugs. 

## <a name="module-properties"></a>Moduleigenschaften

| Eigenschaftenname | Werte | Beschreibung |
|---------------|--------|-------------|
| Bestätigungstext | Textzeichenfolge | Inhalt für die Überschrift, die auf der Check-in-Bestätigungsseite erscheint. |
| QR-Code anzeigen | **True** oder **False** | Wenn diese Eigenschaft auf **True** festgelegt ist, wird auf der Check-in-Bestätigungsseite ein QR-Code angezeigt, der die Bestellbestätigungs-ID darstellt. |
| Überschrift Zusatzinformationen | Textzeichenfolge | Inhalt für die Überschrift, die erscheint, wenn zusätzliche Informationsfelder konfiguriert wurden. |
| Schlüssel für zusätzliche Informationen | Paar Ressourcen-ID/Ressourcenwert | Jeder Schlüssel erstellt ein Formularfeld und ein zugehöriges Label, die verwendet werden, um zusätzliche Informationen von den Debitoren zu erfassen. |
| Zusatzinformationen Schlüssel \> Ressourcen-ID | Textzeichenfolge | Jeder Informationsschlüssel erstellt ein Formularfeld und ein zugehöriges Label, die verwendet werden, um zusätzliche Informationen von den Debitor zu erfassen. Diese Eigenschaft identifiziert den Schlüssel für zusätzliche Informationen. In der Aufgabe, die im Point of Sale (POS) erstellt wird, wird der Wert dieser Eigenschaft als Label im Anleitungsfeld angezeigt. |
| Zusätzliche Informationsschlüssel \> Ressourcenwert | Textzeichenfolge | Das Label für das Textfeld im Auftrag in POS. |
| Schlüssel für Zusatzinformationen \> Erforderlich | **True** oder **False** | Diese Eigenschaft gibt an, ob der Debitor das Formularfeld ausfüllen muss, bevor er fortfahren kann. Wenn diese Eigenschaft auf **True** festgelegt ist, wird ein Sternchen neben dem Label des Formulars angezeigt und eine Null-Prüfung durchgeführt, um zu verhindern, dass der Debitor fortfährt, wenn kein Wert eingegeben wird. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Fügen Sie das Modul „Einchecken zur Abholung“ zu einer Seite hinzu

Das Modul „Einchecken für Abholung“ sollte zu der neuen Seite hinzugefügt werden, die Sie für die Eincheck-Bestätigung erstellen. Diese Seite dient als Check-in-Bestätigung für Debitor, der den **Ich bin hier**-Link oder die Schaltfläche in seiner E-Mail auswählt. 

## <a name="configure-the-additional-information-form"></a>Konfigurieren Sie das Formular für zusätzliche Informationen

Standardmäßig zeigt das Modul, wenn keine zusätzlichen Informationsschlüssel konfiguriert sind, den Kunden die Check-in-Bestätigungsseite an. Sobald die Abfertigungsbestätigung angezeigt wird, wird in POS eine Aufgabe für die Filiale erstellt, in der die Bestellung entnommen wird.

Wenn ein oder mehrere zusätzliche Informationsschlüssel konfiguriert sind, wird der Debitor zunächst aufgefordert, Informationen einzugeben. Wenn sie **Senden** wählen, wird ihnen die Eincheck-Bestätigung angezeigt und eine Aufgabe wird in POS erstellt. 

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Benachrichtigungen zum Einchecken von Kunden im Point of Sale (POS) aktivieren](enable-customer-check-in.md)
