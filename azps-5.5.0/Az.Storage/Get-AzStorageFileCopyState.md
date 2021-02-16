---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100252881"
---
# Get-AzStorageFileCopyState

## SYNOPSIS
Hämtar status för en kopieringsåtgärd.

## SYNTAX

### ShareName
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### Fil
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzStorageFileCopyState** får statusen för en Azure Storage-filkopieringsåtgärd.
Den bör köras på målfilen för kopian.

## EXEMPEL

### Exempel 1: Hämta kopieringstillståndet med filnamn
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

Det här kommandot hämtar tillståndet för kopieringsåtgärden för en fil som har det angivna namnet.

### Exempel 2: Starta kopiering och pipeline för att få kopieringsstatus
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

Det första kommandot startar kopiera filen "contosofile" till "contosofile_copy" och matar ut objektet för aviantionsfilen. Det andra kommandoförloppsförloppet för objektet för utstiantionsfilen till Get-AzStorageFileCopyState, för att få filkopieringstillståndet.

## PARAMETERS

### -ClientTimeoutPerRequest
Anger klienttidens time out-intervall i sekunder för en tjänstbegäran.
Om det föregående samtalet misslyckas i det angivna intervallet försöker den här cmdleten att skicka begäran på ny plats.
Om denna cmdlet inte får ett lyckat svar innan intervallet gått returnerar denna cmdlet ett fel.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Anger maximalt antal samtidiga nätverkssamtal.
Du kan använda den här parametern för att begränsa samtidigheten för att begränsa den lokala CPU-belastningen och bandbreddsanvändningen genom att ange maximalt antal samtidiga nätverkssamtal.
Det angivna värdet är ett absolut antal och multipliceras inte med basantalet.
Den här parametern kan minska problem med nätverksanslutningen i miljöer med låg bandbredd, till exempel 100 kilobit per sekund.
Standardvärdet är 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sammanhang
Anger ett Azure Storage-sammanhang.
Om du vill skapa ett sammanhang använder [du cmdleten New-AzStorageContext.](./New-AzStorageContext.md)

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Arkiv
Anger ett **CloudFile-objekt.**
Du kan skapa en molnfil eller skaffa en med hjälp av Get-AzStorageFile-cmdleten.

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -FilePath
Anger sökvägen till filen i förhållande till en Azure Storage-delning.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Anger längden på time out-perioden för serverdelen av en begäran.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
Anger namnet på en resurs.

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForComplete
Anger att denna cmdlet väntar på att kopian ska slutföras.
Om du inte anger den här parametern returnerar cmdleten ett resultat omedelbart.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
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

### Microsoft.Azure.Storage.File.CloudFile

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### Microsoft.Azure.Storage.File.CopyState

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzStorageFile](./Get-AzStorageFile.md)

[New-AzStorageContext](./New-AzStorageContext.md)

[Start-AzStorageFileCopy](./Start-AzStorageFileCopy.md)

[Stop-AzStorageFileCopy](./Stop-AzStorageFileCopy.md)
