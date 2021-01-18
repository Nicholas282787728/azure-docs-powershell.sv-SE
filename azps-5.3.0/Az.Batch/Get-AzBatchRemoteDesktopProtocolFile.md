---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524780"
---
# Get-AzBatchRemoteDesktopProtocolFile

## Sammanfattning
Hämtar en RDP-fil från en datornod.

## FRÅGESYNTAXEN

### Id_Path (standard)
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Id_Stream
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## PROBLEMBESKRIVNING
Cmdleten **Get-AzBatchRemoteDesktopProtocolFile** hämtar en RDP-fil (Remote Desktop Protocol) från en datornod och sparar den som en fil eller till en användare som har den här strömmen.

## BESKRIVS

### Exempel 1: Hämta en RDP-fil från en angiven datornod och spara filen
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

Det här kommandot får en RDP-fil från Compute-noden som har ID-ComputeNode01 i poolen som har ID Pool06.
Kommandot sparar. RDP-filen som C:\PowerShell\MyComputeNode.rdp.
Använd Get-AzBatchAccountKey cmdlet för att koppla en kontext till $Context variabeln.

### Exempel 2: Hämta en RDP-fil från en datornod och spara filen med pipelinen
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

Det här kommandot får Compute-noden med ID-ComputeNode02 i poolen som har ID Pool06.
Kommandot skickar den beräknade noden till den aktuella cmdleten med hjälp av pipeline-operatorn.
Den aktuella cmdleten hämtar en. RPD-fil från noden Compute och sparar sedan innehållet som en fil med namnet C:\PowerShell\MyComputeNode02.rdp.

### Exempel 3: Hämta en RDP-fil från en angiven datornod och dirigera den till en ström
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

Det första kommandot skapar en ström genom att använda New-Object cmdlet och lagrar den i $Stream-variabeln.
Det andra kommandot får en. RDP-fil från Compute-noden som har ID-ComputeNode03 i poolen som har ID Pool06.
Kommandot dirigerar fil innehåll till strömmen i $Stream.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Om du använder Get-AzBatchAccount cmdlet för att hämta din BatchAccountContext används Azure Active Directory-identifiering när den fungerar tillsammans med kommando tjänsten. Om du vill använda delad nyckel-identifiering kan du i stället använda Get-AzBatchAccountKey cmdlet för att hämta ett BatchAccountContext-objekt med dess åtkomst nycklar ifyllda. När du använder autentisering med delad nycklar används den primära åtkomst tangenten som standard. Om du vill ändra den nyckel som ska användas ställer du in egenskapen BatchAccountContext. KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNode
Anger en datornod som ett **PSComputeNode** -objekt där. RDP-filen pekar.
Använd cmdleten Get-AzBatchComputeNode för att hämta ett Compute Node-objekt.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Anger ID för den datornod som. RDP-filen pekar på.

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPath
Anger sökvägen där denna cmdlet sparar. RDP-filen.

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Anger den ström där denna cmdlet dirigerar RDP-data.
Denna cmdlet stänger inte eller spolar inte tillbaka strömmen.

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Anger ID för poolen som innehåller den datornod som den här cmdleten har en. RDP-fil från.

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## KOSTNADS

### System. String

### Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### System. Void

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Cmdlets för Azure Batch](/powershell/module/Az.Batch/)
