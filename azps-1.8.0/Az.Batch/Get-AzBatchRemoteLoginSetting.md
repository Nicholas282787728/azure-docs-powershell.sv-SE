---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 03c37bb1cf70dfefc5373e9211d6365feb133ad4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93755100"
---
# Get-AzBatchRemoteLoginSetting

## Sammanfattning
Hämtar inställningar för fjärrinloggning för en datornod.

## FRÅGESYNTAXEN

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

## PROBLEMBESKRIVNING
Cmdleten **Get-AzBatchRemoteLoginSetting** hämtar inställningar för fjärrinloggning för en datornod i en infrastruktur baserad pool med virtuella datorer.

## BESKRIVS

### Exempel 1: Hämta inställningar för fjärrinloggning för alla noder i en pool
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang genom att använda **Get-AzBatchAccountKeys**.
Kommandot lagrar kontexten i $Context variabel som ska användas i nästa kommando.
Det andra kommandot får varje datornod i poolen med ID-ContosoPool genom att använda **Get-AzBatchComputeNode**.
Kommandot skickar varje datornod till den aktuella cmdleten med operatören.
Med kommandot får du inställningar för fjärrinloggning för varje datornod.

### Exempel 2: Hämta inställningar för fjärrinloggning för en nod
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

Det första kommandot får en kommando rads kontext som innehåller snabb tangenter för ditt abonnemang och lagrar det sedan i $Context variabel.
Det andra kommandot får fjärrinloggnings inställningarna för den datornod som har angivet ID i poolen med ID-ContosoPool.

## MALLPARAMETRAR

### -BatchContext
Anger den **BatchAccountContext** -instans som denna cmdlet använder för att interagera med kommando tjänsten.
Använd Get-AzBatchAccountKeys cmdlet för att få en **BatchAccountContext** som innehåller åtkomst nycklar för prenumerationen.

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
Anger en datornod som ett **PSComputeNode** -objekt, för vilken denna cmdlet får inställningar för fjärrinloggning.
Använd cmdleten Get-AzBatchComputeNode för att hämta ett Compute Node-objekt.

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
Anger ID för den datornod för vilken du ska få inställningar för fjärrinloggning.
för vilken denna cmdlet får inställningar för fjärrinloggning.

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

### -PoolId
Anger ID för den pool som innehåller den virtuella datorn.

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
Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable. Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## KOSTNADS

### Microsoft.Azure.Commands.BatCH. Modeller. PSComputeNode

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## VÄRDEN

### Microsoft.Azure.Commands.BatCH. Modeller. PSRemoteLoginSettings

## ANMÄRKNINGAR

## RELATERADE LÄNKAR

[Get-AzBatchAccountKeys](./Get-AzBatchAccountKey.md)

[Get-AzBatchComputeNode](./Get-AzBatchComputeNode.md)

[Get-AzBatchRemoteDesktopProtocolFile](./Get-AzBatchRemoteDesktopProtocolFile.md)

[Cmdlets för Azure Batch](/powershell/module/az.batch)


