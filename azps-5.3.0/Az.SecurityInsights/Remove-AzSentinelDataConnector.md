---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525565"
---
# <span data-ttu-id="10c34-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="10c34-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="10c34-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10c34-102">SYNOPSIS</span></span>
<span data-ttu-id="10c34-103">Ta bort en data koppling.</span><span class="sxs-lookup"><span data-stu-id="10c34-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="10c34-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10c34-104">SYNTAX</span></span>

### <span data-ttu-id="10c34-105">DataConnectorId (standard)</span><span class="sxs-lookup"><span data-stu-id="10c34-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10c34-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="10c34-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10c34-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10c34-107">DESCRIPTION</span></span>
<span data-ttu-id="10c34-108">Cmdleten **Remove-AzSentinelDataConnector** tar bort en data koppling permanent från en angiven arbets yta.</span><span class="sxs-lookup"><span data-stu-id="10c34-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="10c34-109">Du kan skicka ett **DataConnector** -objekt med pipeline-operatorn eller så kan du ange de parametrar som krävs.</span><span class="sxs-lookup"><span data-stu-id="10c34-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="10c34-110">Du kan använda Confirm-parametern och $ConfirmPreference Windows PowerShell-variabel för att kontrol lera om cmdleten uppmanar dig att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="10c34-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="10c34-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10c34-111">EXAMPLES</span></span>

### <span data-ttu-id="10c34-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="10c34-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="10c34-113">Det här kommandot tar bort DataConnector från arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="10c34-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="10c34-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10c34-114">PARAMETERS</span></span>

### <span data-ttu-id="10c34-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="10c34-115">-DataConnectorId</span></span>
<span data-ttu-id="10c34-116">ID för data anslutning.</span><span class="sxs-lookup"><span data-stu-id="10c34-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10c34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10c34-117">-DefaultProfile</span></span>
<span data-ttu-id="10c34-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="10c34-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10c34-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10c34-119">-InputObject</span></span>
<span data-ttu-id="10c34-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="10c34-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10c34-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10c34-121">-PassThru</span></span>
<span data-ttu-id="10c34-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="10c34-122">PassThru</span></span>

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

### <span data-ttu-id="10c34-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10c34-123">-ResourceGroupName</span></span>
<span data-ttu-id="10c34-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="10c34-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10c34-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="10c34-125">-WorkspaceName</span></span>
<span data-ttu-id="10c34-126">Namn på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="10c34-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10c34-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="10c34-127">-Confirm</span></span>
<span data-ttu-id="10c34-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="10c34-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c34-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10c34-129">-WhatIf</span></span>
<span data-ttu-id="10c34-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="10c34-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10c34-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="10c34-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10c34-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10c34-132">CommonParameters</span></span>
<span data-ttu-id="10c34-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10c34-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10c34-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="10c34-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10c34-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10c34-135">INPUTS</span></span>

### <span data-ttu-id="10c34-136">System. String</span><span class="sxs-lookup"><span data-stu-id="10c34-136">System.String</span></span>
### <span data-ttu-id="10c34-137">Microsoft. Azure. commands. SecurityInsights. Models. DataConnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="10c34-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="10c34-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10c34-138">OUTPUTS</span></span>

### <span data-ttu-id="10c34-139">Microsoft. Azure. commands. SecurityInsights. Models. DataConnectors. PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="10c34-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="10c34-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10c34-140">NOTES</span></span>

## <span data-ttu-id="10c34-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10c34-141">RELATED LINKS</span></span>
