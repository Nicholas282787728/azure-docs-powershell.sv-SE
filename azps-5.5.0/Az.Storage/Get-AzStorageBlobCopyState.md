---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221886"
---
# Get-AzStorageBlobCopyState

## SYNOPSIS
Får kopieringsstatus för en Azure Storage-blob.

## SYNTAX

### NamePipeline (standard)
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### BlobPipeline
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### ContainerPipeline
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzStorageBlobCopyState** får kopieringsstatusen för en Azure Storage-blob.
Den bör köras på blobben för kopiera mål.

## EXEMPEL

### Exempel 1: Hämta kopieringsstatus för en blob
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

Det här kommandot får kopieringsstatus för blobben med namnet ContosoPlanning2015 i behållaren ContosoUploads.

### Exempel 2: Hämta kopieringsstatus för en blob med hjälp av pipelinen
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

Det här kommandot får bloben ContosoPlanning2015 i behållaren med namnet ContosoUploads med cmdleten **Get-AzStorageBlob** och skickar sedan resultatet till den aktuella cmdleten med hjälp av pipelineoperatorn.
Cmdleten **Get-AzStorageBlobCopyState** får kopieringsstatus för bloben.

### Exempel 3: Hämta kopieringsstatus för en blob i en behållare med hjälp av pipelinen
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

Det här kommandot får behållaren som namnges med cmdleten **Get-AzStorageBlob** och skickar sedan resultatet till den aktuella cmdleten.
Cmdleten **Get-AzStorageContainer** får kopieringsstatusen för bloben ContosoPlanning2015 i den behållaren.

### Exempel 4: Starta kopiering och pipeline för att få kopieringsstatus
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

Det första kommandot startar kopiera blob "ContosoPlanning2015" till "ContosoPlanning2015_copy" och mata ut blob-objektet för avstiantion. Det andra kommandoförloppet för blob-objektet för destiantion till Get-AzStorageBlobCopyState, för att få blob-kopieringstillståndet. 

## PARAMETERS

### -Blob
Anger namnet på en blob.
Den här cmdleten får statusen för blob-kopieringsåtgärden för Azure Storage-blob som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -CloudBlob
Anger ett **CloudBlob-objekt** från Azure Storage Client-biblioteket.
Om du vill **hämta ett CloudBlob-objekt** använder du Get-AzStorageBlob-cmdleten.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CloudBlobContainer
Anger ett **CloudBlobContainer-objekt** från Azure Storage Client-biblioteket.
Den här cmdleten får kopieringsstatusen för en blob i behållaren som den här parametern anger.
Om du vill **hämta ett CloudBlobContainer-objekt** använder du Get-AzStorageContainer-cmdleten.

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Container
Anger namnet på en behållare.
Den här cmdleten får kopieringsstatusen för en blob i behållaren som den här parametern anger.

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Sammanhang
Anger ett Azure-lagringssammanhang.
För att få ett lagringssammanhang använder New-AzStorageContext-cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
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

### -ServerTimeoutPerRequest
Anger time out-intervallet för tjänstsidan i sekunder för en begäran.
Om det angivna intervallet gått innan tjänsten bearbetar begäran returnerar lagringstjänsten ett fel.

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

### Microsoft.Azure.Storage.Blob.CloudBlob

### Microsoft.Azure.Storage.Blob.CloudBlobContainer

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.iStorageContext

## UTDATA

### Microsoft.Azure.Storage.Blob.CopyState

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Start-AzStorageBlobCopy](./Start-AzStorageBlobCopy.md)

[Stop-AzStorageBlobCopy](./Stop-AzStorageBlobCopy.md)


