---
title: EB-Ausdrücke entwerfen, um Anwendungsklassenmethoden aufzurufen
description: Dieser Artikel enthält Informationen darüber, wie die vorhandene Anwendungslogik in Konfigurationen der elektronischen Berichterstellung (EB) erneut verwendet wird, indem erforderliche Methoden von Anwendungsklassen aufgerufen werden.
author: kfend
ms.date: 11/02/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21c24cee15e9a0fd11838b5b8fd816e4aaed9a93
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267841"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a>EB-Ausdrücke entwerfen, um Anwendungsklassenmethoden aufzurufen

[!include [banner](../../includes/banner.md)]

Dieser Artikel beschreibt, wie die vorhandene Anwendungslogik in Konfigurationen der [Elektronischen Berichterstellung (EB)](../general-electronic-reporting.md) erneut verwendet wird, indem erforderliche Methoden von Anwendungsklassen in EB-Ausdrücken aufgerufen werden. Werte von Argumenten zum Aufrufen von Klassen können zur Runtime dynamisch definiert werden. Werte können beispielsweise auf Informationen im Analysedokument basieren, um deren Korrektheit sicherzustellen.

In dem Beispiel in diesem Artikel entwerfen Sie einen Prozess, der eingehender Bankauszüge für eine Anwendungsdatenaktualisierung analysiert. Sie erhalten die eingehenden Bankauszüge als Textdateien (.txt), die die Codes der internationalen Bankkontonummer (IBAN) enthalten. Als Teil des Importprozesses für Bankauszüge müssen Sie die Korrektheit des IBAN-Codes mithilfe der Logik überprüfen, die bereits verfügbar ist.

## <a name="prerequisites"></a>Voraussetzungen

Die Prozeduren in diesem Artikel sind für die Benutzer bestimmt, die die Rolle des **Systemadministrators** oder des **Entwicklers für elektronische Berichterstellung** innehaben.

Die Prozeduren können abgeschlossen werden, indem Sie einen beliebigen Dataset verwenden.

Um sie abzuschließen, müssen Sie auch folgende Datei herunterladen: [SampleIncomingMessage.txt](https://download.microsoft.com/download/8/0/a/80adbc89-f23c-46d9-9241-e0f19125c04b/SampleIncomingMessage.txt).

In diesem Artikel erstellen Sie die erforderlichen EB-Konfigurationen für das Beispielunternehmen Litware, Inc. Bevor Sie daher die Prozeduren in diesem Artikel abschließen können, müssen Sie die folgenden Schritte abschließen.

1. Wechseln Sie zu **Organisationsverwaltung** \> **Arbeitsbereiche** \> **Elektronische Berichterstellung**.
2. Überprüfen Sie auf der Seite **Lokalisierungskonfigurationen**, dass der Konfigurationsanbieter für das Beispielunternehmen **Litware, Inc.** verfügbar und als „aktiv“ gekennzeichnet ist. Sollten Sie diesen Konfigurationsanbieter nicht sehen, müssen Sie zunächst die Schritte in [Erstellen von Konfigurationsanbietern und Markieren als aktiv](er-configuration-provider-mark-it-active-2016-11.md) bearbeiten.

## <a name="import-a-new-er-model-configuration"></a>Neue EB-Modellkonfiguration importieren

1. Auf der Seite **Lokalisierungskonfigurationen** im Abschnitt **Konfigurationsanbieter** wählen Sie die Kachel für den Konfigurationsanbieter **Microsoft** aus.
2. Wählen Sie **Repositorys** aus.
3. Wählen Sie auf der Seite **Lokalisierungs-Repositorys** **Filter anzeigen**.
4. Um den globalen Repository-Datensatz auszuwählen, fügen Sie ein Filterfeld **Name** ein.
5. Geben Sie im Feld **Name** **Global** ein. Wählen Sie dann den Filteroperator **Enthält** aus.
6. Wählen Sie **Anwenden** aus.
7. Wählen Sie **[Öffnen](../er-download-configurations-global-repo.md#open-configurations-repository)**, um die Liste der EB-Konfigurationen im ausgewählten Repository zu überprüfen.
8. Wählen Sie auf der Seite **Konfigurationsrepository** in der Konfigurationsstruktur **Zahlungsmodell** aus.
9. Wählen Sie im Inforegister **Versionen**, wenn die Schaltfläche **Importieren** verfügbar ist, **Ja** aus.

    Wenn die Schaltfläche **Importieren** nicht verfügbar ist, haben Sie die ausgewählte Version der EB-Konfiguration **Zahlungsmodell** bereits importiert.

10. Schließen Sie die Seite **Konfigurationsrepository** und schließen Sie dann die Seite **Lokalisierungsrepositorys**.

## <a name="add-a-new-er-format-configuration"></a>Neues ER-Modellformat hinzufügen

Fügen Sie ein neues EB-Format hinzu, um eingehende Bankauszüge im TXT-Format zu analysieren.

1. Wählen Sie auf der Seite **Lokalisierungskonfigurationen** die Kachel **Berichterstellungskonfigurationen** aus.
2. Wählen Sie auf der Seite **Konfigurationen** in der Konfigurationsstruktur im linken Bereich **Zahlungsmodell** azus.
3. Wählen Sie **Konfiguration erstellen**. 
4. Führen Sie im Drop-Down-Dialogfeld die folgenden Schritte aus:

    1. Im **neuen** Feld geben Sie **Format auf Grundlage Datenmodell PaymentModel** ein.
    2. Geben Sie im Feld **Name** die Bezeichnung **Bankauszug-Importformat (Beispiel)** ein.
    3. Wählen Sie im Feld **Unterstützt Datenimport** **Ja** aus.
    4. Wählen Sie **Konfiguration erstellen** aus, um die Konfiguration fertigzustellen.

## <a name="design-the-er-format-configuration--format"></a>Die Formatkonfiguration für die elektronische Berichterstellung (EB) entwerfen – Format

Erstellen sie ein EB-Format, dass die erwartete Struktur der externen Datei im TXT-Format darstellt.

1. Wählen Sie in der Formatkonfiguration **Bankauszug-Importformat (Beispiel)**, die Sie hinzugefügt haben, **Designer** aus.
2. Wählen Sie auf der Seite **Formatdesigner** in der Formatstrukturdarstellung im linken Bereich **Stamm hinzufügen** aus.
3. Führen Sie im angezeigten Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie in der Strukturdarstellung **Text\\Reihenfolge** aus, um die Formatkomponente **Reihenfolge** hinzuzufügen.
    2. Geben Sie im Feld **Name** die Bezeichnung **Stamm** ein.
    3. Wählen Sie im Feld **Sonderzeichen** **Neue Zeile – Windows (CR LF)** aus. Basierend auf dieser Einstellung wird jede Position in der Analysedatei als ein separater Datensatz behandelt.
    4. Wählen Sie **OK** aus.

4. Wählen Sie **Hinzufügen** aus.
5. Führen Sie im angezeigten Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie in der Struktur **Text\\Reihenfolge** aus.
    2. Geben Sie im Feld **Name** **Zeile** ein.
    3. Wählen Sie im **Vielfältigkeitsgebiet** **viele** aus. Basierend auf dieser Einstellung wird erwartet, dass in der Analysedatei mindestens eine Position dargestellt wird.
    4. Wählen Sie **OK** aus.

6. Wählen Sie in der Struktur **Stamm\\Zeilen** und dann **Reihenfolge hinzufügen** aus.
7. Führen Sie im angezeigten Dialogfeld die folgenden Schritte aus:

    1. Geben Sie im Feld **Name** die Bezeichnung **Felder** ein.
    2. Wählen Sie im Feld **Multiplizität** wählen Sie **Genau eines** aus.
    3. Wählen Sie **OK** aus.

8. Wählen Sie in der Struktur **Stamm\\Stamm\\Felder** und dann **Hinzufügen** aus.
9. Führen Sie im angezeigten Dialogfeld die folgenden Schritte aus:

    1. Wählen Sie in der Struktur **Text\\String** aus.
    2. Geben Sie im Feld **Name** **IBAN** ein.
    3. Wählen Sie **OK** aus.

10. Wählen Sie **Speichern** aus.

Die Konfiguration ist jetzt eingerichtet, sodass jede Position in der Analysedatei nur den IBAN-Code enthält.

![Wählen Sie auf der Formatdesignerseite in der Formatkonfiguration Bankauszug-Importformat (Beispiel) aus.](../media/design-expressions-app-class-er-01.png)

## <a name="design-the-er-format-configuration--mapping-to-a-data-model"></a>Die EB-Formatkonfiguration entwerfen – Zuordnung zu einem Datenmodell

Erstellen Sie eine EB-Formatzuordnung, die Informationen aus der Analysedatei verwendet, um ein Datenmodell auszufüllen.

1. Wählen Sie auf der Seite **Formatdesigner** im Aktivitätsbereich **Format zu Modell zuordnen** aus.
2. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** im Aktivitätsbereich **Neu** aus.
3. Wählen Sie im Feld **Definition** die Bezeichnung **BankToCustomerDebitCreditNotificationInitiation** aus.
4. Geben Sie im Feld **Name** **Zuordnung zu Datenmodell** ein.
5. Wählen Sie **Speichern** aus.
6. Wählen Sie **Designer** aus.
7. Wählen Sie auf der Seite **Modellzuordnungsdesigner** in der Struktur **Datenquellentypen** **Dynamics 365 for Operations\\Klasse** aus.
8. Wählen Sie im Abschnitt **Datenquellen** **Stamm hinzufügen** aus, um eine Datenquelle hinzuzufügen, die die vorhandene Anwendungslogik für die IBAN-Code-Prüfung aufruft.
9. Führen Sie im angezeigten Dialogfeld die folgenden Schritte aus:

    1. Geben Sie im Feld **Name** **Prüfung\_Codes** ein.
    2. Geben Sie im Feld **Klasse** den Wert **ISO7064** ein oder wählen Sie ihn aus.
    3. Wählen Sie **OK** aus.

10. Führen Sie in der Struktur **Datenquellentypen** folgende Schritte aus:

    1. Erweitern Sie die Datenquelle **Format** aus.
    2. Erweitern Sie **Format\\Stamm: Reihenfolge(Stamm)**.
    3. Erweitern Sie **Format\\Stamm: Reihenfolge(Stamm)\\Zeilen: Reihenfolge 1..\* (Zeilen)**.
    4. Erweitern Sie **Format\\Stamm: Reihenfolge(Stamm)\\Zeilen: Reihenfolge 1..\* (Zeilen)\\Felder: Reihenfolge 1..1 (Felder)**.

11. Führen Sie in der Struktur **Datenmodell** folgende Schritte aus:

    1. Erweitern Sie das Feld **Zahlungen** des Datenmodells.
    2. Erweitern Sie **Zahlungen\\Kreditorenkonto(CreditorAccount)**.
    3. Erweitern Sie **Zahlungen\\Kreditorenkonto(CreditorAccount)\\Kennung**.
    4. Erweitern Sie **Zahlungen\\Kreditorenkonto(CreditorAccount)\\Kennung\\IBAN**.

12. Führen Sie diese Schritte aus, um Komponenten des konfigurierten Formats an Datenmodellfelder zu binden:

    1. Wählen Sie **Format\\Stamm: Reihenfolge(Stamm)\\Zeilen: Reihenfolge 1..\* (Zeilen)** aus.
    2. Wählen Sie **Zahlungen** aus.
    3. Wählen Sie **Bindung** aus. Basierend auf dieser Einstellung wird jede Position in der Analysedatei als eine einzige Zahlung behandelt.
    4. Wählen Sie **Format\\Stamm: Reihenfolge(Stamm)\\Zeilen: Reihenfolge 1..\* (Zeilen)\\Felder: Reihenfolge 1..1 (Felder)\\IBAN: Zeichenfolge(IBAN)** aus.
    5. Wählen Sie **Zahlungen\\Kreditorenkonto(CreditorAccount)\\Kennung\\IBAN** aus.
    6. Wählen Sie **Bindung** aus. Basierend auf dieser Einstellung wird das Feld **IBAN** des Datenmodells wird mit dem Wert aus der Analysedatei gefüllt.

    ![Bindung von Formatkomponenten an Datenmodellfelder auf der Seite „Modellzuordnungsdesigner“.](../media/design-expressions-app-class-er-02.png)

13. Führen Sie auf der Registerkarte **Überprüfungen** diese Schritte aus, um eine Regel für die [Überprüfung](../general-electronic-reporting-formula-designer.md#Validation) hinzufügen, die eine Fehlermeldung für jede Zeile in der Analysedatei anzeigt, die einen ungültigen IBAN-Code enthält:

    1. Wählen Sie **Neu** und dann **Bedingung bearbeiten** aus.
    2. Erweitern Sie auf der Seite **Formeldesigner** in der Struktur **Datenquelle** die Datenquelle **Prüfen\_Codes** aus, die für die Anwendungsklasse **ISO7064**, um die verfügbaren Methoden dieser Klasse anzuzeigen.
    3. Wählen Sie **Prüfen\_Codes\\verifyMOD1271\_36**.
    4. Wählen Sie **Datenquelle hinzufügen** aus:
    5. Geben Sie im Feld **Formel** den folgenden [Ausdruck](../general-electronic-reporting-formula-designer.md#Binding) ein: **Check\_codes.verifyMOD1271\_36(format.Root.Rows.Fields.IBAN)** ein.
    6. Klicken Sie auf **Speichern** und schließen Sie die Seite.
    7. Wählen Sie **Meldung bearbeiten** aus.
    8. Geben Sie auf der Seite **Formeldesigner** im Feld **Formel** **CONCATENATE("Invalid IBAN code has been found:&nbsp;", format.Root.Rows.Fields.IBAN)** ein.
    9. Klicken Sie auf **Speichern** und schließen Sie die Seite.

    Aufgrund dieser Einstellungen gibt die Überprüfungsbedingung *[FALSCH](../er-formula-supported-data-types-primitive.md#boolean)* für jeden ungültigen IBAN-Code zurück, indem die vorhandene Methode **verifyMOD1271\_36** von der Anwendungsklasse **ISO7064** aufgerufen wird. Beachten Sie, dass der Wert des IBAN-Codes dynamisch zur Runtime als Argument der aufrufenden Methode basierend auf dem Inhalt der analysierenden Textdatei definiert wird.

    ![Überprüfungsregel auf der Seite „Modellzuordnungsdesigner“.](../media/design-expressions-app-class-er-03.png)

14. Wählen Sie **Speichern** aus.
15. Schließen Sie die Seite **Modellzuordnungsdesigner** und schließen Sie dann die Seite **Modell für Datenquellenzuordnung**.

## <a name="run-the-format-mapping"></a>Die Formatzuordnung ausführen

Führen Sie zu Textzwecken die Formatzuordnung mithilfe der Datei SampleIncomingMessage.txt aus, die Sie zuvor heruntergeladen haben. Die generierte Ausgabe enthält Daten, die aus der ausgewählten Textdatei importiert werden und im benutzerdefinierte Datenmodell während des tatsächlichen Imports übertragen werden.

1. Wählen Sie auf der Seite **Modell für Datenquellenzuordnung** **Ausführen** aus.
2. Wählen Sie auf der Seite **Elektronische Berichtsparameter** **Durchsuchen** aus, blättern Sie zur Datei **SampleIncomingMessage.txt**, die Sie heruntergeladen haben, und wählen Sie sie aus.
3. Wählen Sie **OK** aus.
4. Beachten Sie, dass die Seite **Modell für Datenquellenzuordnung** eine Fehlermeldung über einen ungültigen IBAN-Code anzeigt.

    ![Ergebnis der Ausführung der Formatzuordnung auf der Seite „Modell für Datenquellenzuordnung“.](../media/design-expressions-app-class-er-04.png)

5. Überprüfen Sie die Ausgabe im XML-Format, das die Daten darstellt, die aus der ausgewählten Datei importiert wurden und in das Datenmodell übertragen wurden. Beachten Sie, dass nur drei Zeilen der importierten Textdatei fehlerfrei verarbeitet wurden. Der IBAN-Code von Position 4 ist ungültig und wurde übersprungen.

    ![XML-Ausgabe.](../media/design-expressions-app-class-er-05.png)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
