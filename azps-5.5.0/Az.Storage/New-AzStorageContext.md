---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae12bb509773f36ecfd94ad6907499f0b5feb02d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252876"
---
# New-AzStorageContext

## SYNOPSIS
Skapar en Azure Storage-kontext.

## SYNTAX

### OAuthAccount (standard)
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKey
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### OAuthAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-UseConnectedAccount] [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### ConnectionString
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevement
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **New-AzStorageContext** skapar en Azure Storage-kontext.
Standardautentisering för ett lagringssammanhang är OAuth (Azure AD), om det bara är namn på ett lagringskonto som matas in.
Visa information om autentisering av lagringstjänsten https://docs.microsoft.com/en-us/rest/api/storageservices/authorization-for-the-azure-storage-services i.

## EXEMPEL

### Exempel 1: Skapa ett sammanhang genom att ange ett namn och en nyckel för lagringskontot
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Det här kommandot skapar en kontext för kontot ContosoGeneral som använder den angivna nyckeln.

### Exempel 2: Skapa ett sammanhang genom att ange en anslutningssträng
```
PS C:\>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Det här kommandot skapar ett sammanhang baserat på den angivna anslutningssträngen för kontot ContosoGeneral.

### Exempel 3: Skapa ett sammanhang för ett anonymt lagringskonto
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Det här kommandot skapar ett sammanhang för anonym användning för kontot ContosoGeneral.
Kommandot anger HTTP som ett anslutningsprotokoll.

### Exempel 4: Skapa ett sammanhang med hjälp av det lokala lagringskontot för utveckling
```
PS C:\>New-AzStorageContext -Local
```

Det här kommandot skapar ett sammanhang med hjälp av det lokala lagringskontot för utveckling.
Kommandot anger den *lokala* parametern.

### Exempel 5: Hämta behållaren för det lokala lagringskontot för utvecklare
```
PS C:\>New-AzStorageContext -Local | Get-AzStorageContainer
```

Det här kommandot skapar ett sammanhang med hjälp av det lokala lagringskontot för utveckling och skickar sedan det nya sammanhanget till cmdleten **Get-AzStorageContainer** med hjälp av pipelineoperatorn.
Kommandot hämtar Azure Storage-behållaren för det lokala lagringskontot för utvecklare.

### Exempel 6: Hämta flera behållare
```
PS C:\>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Det första kommandot skapar ett sammanhang med hjälp av det lokala lagringskontot för utveckling och lagrar sedan det sammanhanget i variabeln $Context 01.
Det andra kommandot skapar en kontext för kontot ContosoGeneral som använder den angivna nyckeln och lagrar sedan det sammanhanget i variabeln $Context 02.
Det slutliga kommandot får behållare för sammanhang som lagras i $Context 01 och $Context 02 med **hjälp av Get-AzStorageContainer.**

### Exempel 7: Skapa ett sammanhang med en slutpunkt
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Det här kommandot skapar en Azure Storage-kontext som har den angivna lagringsslutpunkten.
Kommandot skapar kontexten för kontot ContosoGeneral som använder den angivna nyckeln.

### Exempel 8: Skapa ett sammanhang med en viss miljö
```
PS C:\>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Det här kommandot skapar en Azure-lagringskontext som har den angivna Azure-miljön.
Kommandot skapar kontexten för kontot ContosoGeneral som använder den angivna nyckeln.

### Exempel 9: Skapa ett sammanhang med hjälp av en SAS token
```
PS C:\>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Det första kommandot genererar en SAS-token med cmdleten **New-AzStorageContainerSASToken** för behållaren ContosoMain och lagrar sedan denna token i $SasToken variabeln.
Den token är för behörigheterna läsa, lägga till, uppdatera och ta bort.
Det andra kommandot skapar en kontext för kontot ContosoGeneral som använder SAS token som lagras i $SasToken och lagrar sedan kontexten i den $Context variabeln.
Det slutliga kommandot listar alla blobbar som associeras med behållaren ContosoMain med hjälp av det sammanhang som lagras i $Context.

### Exempel 10: Skapa ett sammanhang med hjälp av OAuth-autentisering
```
PS C:\>Connect-AzAccount
PS C:\> $Context = New-AzStorageContext -StorageAccountName "myaccountname" -UseConnectedAccount
```

Det här kommandot skapar ett sammanhang med hjälp av OAuth-autentisering (Azure AD).

## PARAMETERS

### -Anonym
Anger att den här cmdleten skapar en Azure Storage-kontext för anonym inloggning.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Anger en anslutningssträng för Azure Storage-kontexten.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Anger slutpunkten för Azure Storage-kontexten.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Miljö
Anger Azure-miljön.
De godtagbara värdena för den här parametern är: AzureCloud och AzureChinaCloud.
Om du vill ha mer information skriver du `Get-Help Get-AzEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Anger att denna cmdlet skapar ett sammanhang med hjälp av det lokala lagringskontot för utveckling.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol
Transfer Protocol (https/http).

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, OAuthAccountEnvironment
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Anger en SAS-token (Shared Access Signature) för sammanhanget.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Anger en Azure Storage-kontonyckel.
Den här cmdleten skapar ett sammanhang för nyckeln som parametern anger.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Anger namnet på ett Azure Storage-konto.
Den här cmdleten skapar ett sammanhang för kontot som parametern anger.

```yaml
Type: System.String
Parameter Sets: OAuthAccount, AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment, OAuthAccountEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseConnectedAccount
Anger att den här cmdleten skapar en Azure Storage-kontext med OAuth-autentisering (Azure AD).
Cmdleten använder OAuth-autentisering som standard, när annan autentisering inte anges.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OAuthAccount, OAuthAccountEnvironment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INDATA

### System.String

## UTDATA

### Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[New-AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


