---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94093263"
---
# Get-AzureSubscription

## Sammanfattning
Hämtar Azure-prenumerationer i Azure-konto.

## FRÅGESYNTAXEN

### ByName (standard)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Vis
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Här
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzureSubscription** hämtar abonnemangen på ditt Azure-konto.
Du kan använda denna cmdlet för att få information om prenumerationen och för att gå med i prenumerationen på andra cmdletar.

**Get-AzureSubscription** kräver åtkomst till dina Azure-konton.
Innan du kör **Get-AzureSubscription** måste du köra cmdleten **Add-AzureAccount** eller de cmdlets som laddar ned och installerar en fil för publicerings inställningar ( **Get-AzurePublishSettingsFile** , **import-AzurePublishSettingsFile**.

I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.
För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .

## BESKRIVS

### Exempel 1: Hämta alla abonnemang
```
C:\PS>Get-AzureSubscription
```

Det här kommandot får alla abonnemang på kontot.

### Exempel 2: skaffa ett abonnemang efter namn
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

Det här kommandot får bara till "MyProdSubsciption"-abonnemanget.

### Exempel 3: Hämta standard abonnemanget
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

Det här kommandot får bara namnet på standard abonnemanget.
Kommandot får först abonnemanget och använder sedan metoden dot för att hämta **SubscriptionName** -egenskapen för prenumerationen.

### Exempel 4: Hämta valda prenumerations egenskaper
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

Det här kommandot returnerar en lista med namnet och certifikatet för det aktuella abonnemanget.
Det använder kommandot **Get-AzureSubscription** för att hämta det aktuella abonnemanget.
Sedan rör det prenumerationen till ett **format List** kommando som visar de markerade egenskaperna i en lista.

### Exempel 5: använda en alternativ fil för abonnemang
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

Det här kommandot hämtar abonnemang från data filen C:\Temp\MySubscriptions.xml-prenumeration.
Använd parametern **SubscriptionDataFile** om du har angett en alternativ fil för abonnemang när du körde cmdletarna **Add-AzureAccount** eller **import-PublishSettingsFile** .

## MALLPARAMETRAR

### -Aktuell
Hämtar bara det aktuella abonnemanget, det vill säga prenumerationen som "Current". Som standard får **Get-AzureSubscription** alla abonnemang på dina Azure-konton.
Om du vill ange ett abonnemang som "Aktuellt" använder du den **aktuella** parametern för cmdleten **Select-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standard
Hämtar bara standard abonnemanget, det vill säga prenumerationen som "standard". Som standard får **Get-AzureSubscription** alla abonnemang på dina Azure-konton.
Använd **standard** parametern för cmdleten **Select-AzureSubscription** om du vill ange ett abonnemang som "standard".

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Returnerar kvot information för abonnemanget, utöver standardinställningarna.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Anger den Azure-profil från vilken denna cmdlet läser. Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
Hämtar bara det angivna abonnemanget.
Ange prenumerationens namn.
Värdet är Skift läges känsligt.
Jokertecken stöds inte.
Som standard får **Get-AzureSubscription** alla abonnemang på dina Azure-konton.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Du kan ange indata för egenskapen **SubscriptionName** efter namn men inte efter värde.

## VÄRDEN

### Microsoft. WindowsAzure. commands. Utilitiess. Common. WindowsAzureSubscription

## ANMÄRKNINGAR
* Get-AzureSubscription hämtar data från den prenumerations data fil som du skapar med cmdletarna **Add-AzureAccount** och **import-PublishSettingsFile** .

## RELATERADE LÄNKAR

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


