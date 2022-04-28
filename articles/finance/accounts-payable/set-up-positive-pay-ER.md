---
title: Dateien für positive Zahlungen mithilfe der elektronischen Berichterstellung einrichten und generieren
description: In diesem Thema wird beschrieben, wie positive Zahlungen mit der elektronischen Berichterstellung eingerichtet werden.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544485"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Dateien für positive Zahlungen mithilfe der elektronischen Berichterstellung einrichten

Sie können positiven Lohn verwenden, um eine elektronische Liste mit Schecks zu generieren, die für die Bank bereitgestellt wird. Wenn der Scheck der Bank präsentiert wird, vergleicht die Bank den Scheck mit der Liste der Schecks. Wenn der Originalscheck mit einem Scheck in der Liste übereinstimmt, löscht die Bank den Scheck. Wenn der Scheck mit keinem Scheck iin der Liste übereinstimmt, hält die Bank den Scheck zur Prüfung zurück.

## <a name="set-up-the-electronic-reporting-configuration"></a>Konfiguration der elektronischen Berichterstellung einrichten

1. Wechseln Sie zu **Arbeitsbereiche \> Elektronische Berichterstellung**.
2. Auf der Kachel für den Konfigurationsanbieter **Microsoft** wählen Sie **Repositorys** aus.
3. Wählen Sie **Global** und dann **Öffnen** aus.
4. Wenn eine Verbindung zum Repository hergestellt werden muss, wählen Sie den blauen Link im Dialogfeld aus.
5. Suchen Sie in der Konfigurationsliste **Modell für positive Zahlungen \> Format für positive Zahlungen**, und wählen Sie die Optionen aus.
6. Wählen Sie im Inforegister **Versionen** die neueste Version, und wählen Sie dann **Importieren** aus.

## <a name="set-up-a-positive-pay-format"></a>Einrichten eines Formats für positive Zahlungen

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Einrichten \> Formate für positive Zahlungen**.
2. Wählen Sie **Neu** aus.
3. Legen Sie die Felder **Zahlungsformat** und **Beschreibung** fest.
4. Aktivieren Sie das Kontrollkästchen **Allgemeines elektronisches Exportformat**.
5. Legen Sie das Feld **Formatkonfiguration exportieren** auf das **Format für positive Zahlungen** fest.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Zuweisen eines Formats für positive Zahlungen zu einem Bankkonto

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Öffnen Sie das Bankkonto.
3. Legen Sie im Inforegister **Allgemein** das Feld **Format für positive Zahlungen** auf das zuvor erstellte Format fest.
4. Legen Sie das **Startdatum für positive Zahlungen** auf das aktuelle Datum fest.

## <a name="generate-a-positive-pay-file"></a>Datei für positive Zahlungen generieren

1. Gehen Sie zu **Bargeld- und Bankverwaltung \> Bankkonten \> Bankkonten**.
2. Öffnen Sie ein Bankkonto, für das positive Zahlungen eingerichtet sind.
3. Wählen Sie **Zahlungen verwalten \> Positive Zahlung \> Datei für positive Zahlungen** aus.
4. Legen Sie das Feld **Stichtag** fest. Prüfungen, die vor diesem Datum erstellt wurden, werden berücksichtigt.

Die resultierende XML-Datei wird heruntergeladen.
