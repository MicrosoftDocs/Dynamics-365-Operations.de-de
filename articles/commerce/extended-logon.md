---
title: Einrichten der erweiterten Anmeldefunktionalität für MPOS und Cloud POS
description: Dieses Thema behandelt die Optionen für die Einrichtung der erweiterten Anmeldung für Cloud POS und Retail Modern POS (MPOS).
author: rubencdelgado
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f9d8889581e2e11fa5261805c866a6014df57611
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027575"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a>Einrichten der erweiterten Anmeldungsfunktionen für MPOS und Cloud POS

[!include [banner](includes/banner.md)]

Dieses Thema behandelt die Optionen für die Einrichtung der erweiterten Anmeldung für Cloud POS und Retail Modern POS (MPOS).

## <a name="setting-up-extended-logon"></a>Einrichten der erweiterten Anmeldung

Sie finden Sie Einstellungen für Strichcodemasken unter **Einzelhandel und Handel** &gt; **Kanaleinstellungen** &gt; **POS-Einstellungen** &gt; **POS-Profile** &gt; **Funktionsprofile**. Das Inforegister **Funktionen** umfasst folgende Optionen, die der erweiterten Anmeldung zugeordnet sind.

### <a name="staff-bar-code-logon"></a>Personal-Strichcodeanmeldung

Wenn die Option **Personal-Strichcodeanmeldung** aktiviert ist, können Arbeitskräfte, deren POS-Anmeldeinformationen die erweiterte Anmeldung zugewiesen ist, sich mit einem Strichcode anmelden.

### <a name="staff-bar-code-logon-requires-password"></a>Personalanmeldung mit Strichcode erfordert Kennwort.

Wenn die Option **Personalanmeldung mit Strichcode erfordert Kennwort** aktiviert ist, wird bei der Personalanmeldung mit Strichode nur die Arbeitskraft ausgewählt, die der angegebenen erweiterten Anmeldung zugewiesen ist. Arbeitskräfte müssen noch eigene Kennwörter eingeben, wenn diese Option aktiviert ist.

### <a name="staff-card-logon"></a>Personalkartenanmeldung

Wenn die Option **Personalkartenanmeldung** aktiviert ist, können Arbeitskräfte, deren POS-Anmeldeinformationen die erweiterte Anmeldung zugewiesen ist, sich mit einem Magnetstreifen anmelden.

### <a name="staff-card-logon-requires-password"></a>Personalanmeldung mit Karte erfordert Kennwort.

Wenn die Option **Personalanmeldung mit Karte erfordert Kennwort** aktiviert ist, wird bei der Personalanmeldung mit Karte nur die Arbeitskraft ausgewählt, die der angegebenen erweiterten Anmeldung zugewiesen ist. Arbeitskräfte müssen noch eigene Kennwörter eingeben, wenn diese Option aktiviert ist.

## <a name="assigning-an-extended-logon"></a>Zuweisen einer erweiterten Anmeldung

Standardmäßig können nur Manager die erweiterte Anmeldung den Arbeitskräften zuweisen. Um erweiterte Anmeldung zuzuweisen, fahren Sie mit **Erweiterte Anmeldung** in POS fort. Suchen Sie dann nach einer Arbeitskraft nach Eingabe der Kennung in der Auswahlliste. Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisen**. Auf der nächsten Seite ziehen Sie die Karte durch das Lesegerät oder scannen Sie die Karte, um der Arbeitskraft die erweiterte Anmeldung zuzuweisen. Wenn der Vorgang erfolgreich war, wird die Schaltfläche **OK** verfügbar. Klicken Sie auf **OK**, um die erweiterten Anmeldung für diese Arbeitskraft zu speichern.

## <a name="deleting-an-extended-logon"></a>Löschen einer erweiterten Anmeldung

Um die erweiterte Anmeldung zu löschen, die einer Arbeitskraft zugewiesen wurde, suchen Sie die Arbeitskraft, indem Sie den Vorgang **Erweiterte Anmeldung** verwenden. Wählen Sie die Arbeitskraft aus, und klicken Sie anschließend auf **Zuweisung aufheben**. Alle erweiterten Anmeldeinformationen, die dieser Arbeitskraft zugeordnet sind, werden entfernt.

## <a name="extending-extended-logon"></a>Erweitern der erweiterten Anmeldung

Der Anmeldedienst kann erweitert werden, um zusätzliche Geräte für die erweiterte Anmeldung zu unterstützen, z.B. Handflächenscanner. Weitere Informationen finden Sie in der Dokumentation zur Erweiterbarkeit des POS.

## <a name="using-extended-logon"></a>Verwenden der erweiterten Anmeldung

Wenn die erweiterte Anmeldung konfiguriert ist und einer Arbeitskraft ein Strichcode oder ein Magnetstreifen zugewiesen wurde, muss die Arbeitskraft die Karte durch ein Lesegerät ziehen, wenn die POS-Anmeldeseite angezeigt wird. Wenn auch ein Kennwort erforderlich ist, damit die Anmeldung durchgeführt werden kann, wird die Arbeitskraft aufgefordert, das Kennwort einzugeben.


[!INCLUDE[footer-include](../includes/footer-banner.md)]