---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContext.md
ms.openlocfilehash: 678453cc050ae31158f4f08e1efcda00338aca98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755900"
---
# New-AzureStorageContext

## Sammanfattning
Skapar en Azure Storage-kontext.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## FRÅGESYNTAXEN

### AccountNameAndKey (standard)
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### Sträng
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **New-AzureStorageContext** skapar en Azure-lagringsenhet.

## BESKRIVS

### Exempel 1: skapa en kontext genom att ange ett lagrings konto namn och en nycklar
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

Det här kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten.

### Exempel 2: skapa en kontext genom att ange en anslutnings sträng
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

Det här kommandot skapar en kontext baserat på den angivna anslutnings strängen för kontot ContosoGeneral.

### Exempel 3: skapa en kontext för ett anonymt lagrings konto
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

Det här kommandot skapar en kontext för anonym användning för kontot med namnet ContosoGeneral.
Kommandot anger HTTP som ett anslutnings protokoll.

### Exempel 4: skapa en kontext med hjälp av det lokala utvecklings lagrings kontot
```
C:\PS>New-AzureStorageContext -Local
```

Det här kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.
Kommandot anger den *lokala* parametern.

### Exempel 5: Hämta behållaren för det lokala utvecklings lagrings kontot
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

Det här kommandot skapar en kontext med hjälp av det lokala utvecklings arkivet och skickar sedan den nya kontexten till cmdleten **Get-AzureStorageContainer** med hjälp av pipeline-operatorn.
Kommandot hämtar Azure Storage-behållaren för det lokala utvecklings lagrings kontot.

### Exempel 6: Hämta flera behållare
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

Det första kommandot skapar en kontext med hjälp av det lokala utvecklings lagrings kontot och lagrar sedan kontexten i variabeln $Context 01.

Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder den angivna tangenten och lagrar sedan kontexten i $Context 02-variabeln.

Med kommandot slut får du behållare för de kontexter som lagras i $Context 01 och $Context 02 genom att använda **Get-AzureStorageContainer**.

### Exempel 7: skapa en kontext med en slut punkt
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

Det här kommandot skapar en Azure Storage-kontext som har den angivna lagrings slut punkten.
Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.

### Exempel 8: skapa en kontext med en angiven miljö
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

Det här kommandot skapar en Azure-lagringsenhet med den angivna Azure-miljön.
Kommandot skapar kontexten för kontot med namnet ContosoGeneral som använder den angivna tangenten.

### Exempel 9: skapa en kontext med hjälp av en SAS-token
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

Det första kommandot skapar en SAS-token med hjälp av cmdleten **New-AzureStorageContainerSASToken** för behållaren med namnet ContosoMain och lagrar sedan denna token i $SasToken variabel.
Denna token är för läsa, lägga till, uppdatera och ta bort behörigheter.

Det andra kommandot skapar en kontext för kontot med namnet ContosoGeneral som använder SAS-token som lagras i $SasToken och lagrar sedan kontexten i $Context-variabeln.

Med kommandot slut visas alla blobbar som är kopplade till behållaren med namnet ContosoMain med hjälp av kontexten som lagras i $Context.

## MALLPARAMETRAR

### -Anonym
Anger att den här cmdleten skapar en Azure-lagringsenhet för anonym inloggning.

```yaml
Type: SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Anger en anslutnings sträng för Azure-lagringsplatsen.

```yaml
Type: String
Parameter Sets: ConnectionString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slut punkt
Anger slut punkten för Azure-lagringsplatsen.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Miljö
Anger Azure-miljön.
De acceptabla värdena för den här parametern är: AzureCloud och AzureChinaCloud.
Om du vill ha mer information skriver du `Get-Help Get-AzureEnvironment` .

```yaml
Type: String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lokal
Anger att denna cmdlet skapar en kontext med hjälp av det lokala utvecklings lagrings kontot.

```yaml
Type: SwitchParameter
Parameter Sets: LocalDevelopment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protokoll
Transfer Protocol (https/http).

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases: 
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Anger ett SAS-token (Shared Access signatur) för kontexten.

```yaml
Type: String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Anger en Key för Azure Storage-kontot.
Denna cmdlet skapar en kontext för den parameter som anges av den här parametern.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Anger ett namn på en Azure Storage-konto.
Denna cmdlet skapar en kontext för det konto som den här parametern anger.

```yaml
Type: String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Ingen
Denna cmdlet accepterar inte indata.

## VÄRDEN

### AzureStorageContext

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzureStorageBlob](./Get-AzureStorageBlob.md)

[New-AzureStorageContainerSASToken](./New-AzureStorageContainerSASToken.md)


