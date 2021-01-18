---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98526812"
---
# <span data-ttu-id="6da5a-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="6da5a-101">Remove-AzHost</span></span>

## <span data-ttu-id="6da5a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6da5a-102">SYNOPSIS</span></span>
<span data-ttu-id="6da5a-103">Tar bort en värd.</span><span class="sxs-lookup"><span data-stu-id="6da5a-103">Removes a host.</span></span>

## <span data-ttu-id="6da5a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6da5a-104">SYNTAX</span></span>

### <span data-ttu-id="6da5a-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="6da5a-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6da5a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="6da5a-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6da5a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="6da5a-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6da5a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6da5a-108">DESCRIPTION</span></span>
<span data-ttu-id="6da5a-109">Denna cmdlet tar bort en värd</span><span class="sxs-lookup"><span data-stu-id="6da5a-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="6da5a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6da5a-110">EXAMPLES</span></span>

### <span data-ttu-id="6da5a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6da5a-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="6da5a-112">Det här kommandot hämtar och tar bort angiven värd.</span><span class="sxs-lookup"><span data-stu-id="6da5a-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="6da5a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="6da5a-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="6da5a-114">Det här kommandot tar bort angiven värd.</span><span class="sxs-lookup"><span data-stu-id="6da5a-114">This command removes the given host.</span></span>

## <span data-ttu-id="6da5a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6da5a-115">PARAMETERS</span></span>

### <span data-ttu-id="6da5a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6da5a-116">-AsJob</span></span>
<span data-ttu-id="6da5a-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6da5a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6da5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6da5a-118">-DefaultProfile</span></span>
<span data-ttu-id="6da5a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6da5a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6da5a-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="6da5a-120">-HostGroupName</span></span>
<span data-ttu-id="6da5a-121">Namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="6da5a-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da5a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6da5a-122">-InputObject</span></span>
<span data-ttu-id="6da5a-123">Värdens lokala objekt.</span><span class="sxs-lookup"><span data-stu-id="6da5a-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6da5a-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="6da5a-124">-Name</span></span>
<span data-ttu-id="6da5a-125">Namnet på värden.</span><span class="sxs-lookup"><span data-stu-id="6da5a-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da5a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6da5a-126">-ResourceGroupName</span></span>
<span data-ttu-id="6da5a-127">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6da5a-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da5a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6da5a-128">-ResourceId</span></span>
<span data-ttu-id="6da5a-129">ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="6da5a-129">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6da5a-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6da5a-130">-Confirm</span></span>
<span data-ttu-id="6da5a-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6da5a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6da5a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6da5a-132">-WhatIf</span></span>
<span data-ttu-id="6da5a-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6da5a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6da5a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6da5a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6da5a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6da5a-135">CommonParameters</span></span>
<span data-ttu-id="6da5a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6da5a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6da5a-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6da5a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6da5a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6da5a-138">INPUTS</span></span>

### <span data-ttu-id="6da5a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6da5a-139">System.String</span></span>

### <span data-ttu-id="6da5a-140">Microsoft. Azure. commands. Compute. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="6da5a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="6da5a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6da5a-141">OUTPUTS</span></span>

### <span data-ttu-id="6da5a-142">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6da5a-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6da5a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6da5a-143">NOTES</span></span>

## <span data-ttu-id="6da5a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6da5a-144">RELATED LINKS</span></span>
