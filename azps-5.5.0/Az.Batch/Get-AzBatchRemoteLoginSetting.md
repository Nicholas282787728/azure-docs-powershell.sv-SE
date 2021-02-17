---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239301"
---
# Get-AzBatchRemoteLoginSetting

## SYNOPSIS
Hämtar fjärrinloggningsinställningar för en beräkningsnod.

## SYNTAX

### ID (standard)
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESKRIVNING
Cmdleten **Get-AzBatchRemoteLoginSetting** får fjärrinloggningsinställningar för en beräkningsnod i en infrastrukturbaserad pool för virtuella maskiner.

## EXEMPEL

### Exempel 1: Hämta fjärrinloggningsinställningar för alla noder i en pool
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Med det första kommandot får du en kontext för ett batchkonto som innehåller snabbnycklar för din prenumeration genom att använda **Get-AzBatchAccountKey.**
Kommandot lagrar kontexten i den $Context som ska användas i nästa kommando.
Det andra kommandot hämtar varje beräkningsnod i poolen som har ID ContosoPool med hjälp av **Get-AzBatchComputeNode.**
Kommandot skickar varje datornod till den aktuella cmdleten med hjälp av rörledningsoperatorn.
Kommandot hämtar inställningarna för fjärrinloggning för varje beräkningsnod.

### Exempel 2: Hämta fjärrinloggningsinställningar för en nod
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Det första kommandot får ett batchkontosammanhang som innehåller snabbnycklar för din prenumeration och lagrar det sedan i den $Context variabeln.
Det andra kommandot hämtar inställningarna för fjärrinloggning för beräkningsnoden som har det angivna ID:t i poolen som har ID ContosoPool.

## PARAMETERS

### -BatchContext
Anger **batchaccountContext-instansen** som denna cmdlet använder för att interagera med batchtjänsten.
Om du vill **hämta ett BatchAccountContext** som innehåller snabbtangenter för din prenumeration använder du cmdleten Get-AzBatchAccountKey-cmdleten.

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
Anger en beräkningsnod som ett **PSComputeNode-objekt** för vilket den här cmdleten hämtar fjärrinloggningsinställningar.
Om du vill hämta ett compute node-objekt använder Get-AzBatchComputeNode-cmdleten.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Anger ID för beräkningsnoden som du vill hämta inställningarna för fjärrinloggning för.
som denna cmdlet får fjärrinloggningsinställningar för.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Autentiseringsuppgifter, konto, klientorganisation och prenumeration som används för kommunikation med Azure.

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

### -PoolId
Anger ID för poolen som innehåller den virtuella datorn.

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Den här cmdleten stöder vanliga parametrar: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction och -WarningVariable. Mer information finns i [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## INDATA

### Microsoft.Azure.Commands.Batkap. Models.PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## UTDATA

### Microsoft.Azure.Commands.Batkap. Models.PSRemoteLoginSettings

## ANTECKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Azure-batch-cmdlets](/powershell/module/Az.Batch/)
