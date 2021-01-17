---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399384"
---
# <span data-ttu-id="18e4a-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="18e4a-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="18e4a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="18e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="18e4a-103">Tar bort en värd grupp.</span><span class="sxs-lookup"><span data-stu-id="18e4a-103">Removes a host group.</span></span>

## <span data-ttu-id="18e4a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="18e4a-104">SYNTAX</span></span>

### <span data-ttu-id="18e4a-105">DefaultParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="18e4a-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18e4a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="18e4a-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="18e4a-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="18e4a-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18e4a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="18e4a-108">DESCRIPTION</span></span>
<span data-ttu-id="18e4a-109">Denna cmdlet tar bort en värd grupp</span><span class="sxs-lookup"><span data-stu-id="18e4a-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="18e4a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="18e4a-110">EXAMPLES</span></span>

### <span data-ttu-id="18e4a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="18e4a-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="18e4a-112">Det här kommandot hämtar och tar bort den angivna värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="18e4a-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="18e4a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="18e4a-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="18e4a-114">Det här kommandot tar bort den angivna värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="18e4a-114">This command removes the given host group.</span></span>

## <span data-ttu-id="18e4a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="18e4a-115">PARAMETERS</span></span>

### <span data-ttu-id="18e4a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18e4a-116">-AsJob</span></span>
<span data-ttu-id="18e4a-117">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="18e4a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="18e4a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e4a-118">-DefaultProfile</span></span>
<span data-ttu-id="18e4a-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="18e4a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18e4a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18e4a-120">-InputObject</span></span>
<span data-ttu-id="18e4a-121">Det lokala objektet i värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="18e4a-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18e4a-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="18e4a-122">-Name</span></span>
<span data-ttu-id="18e4a-123">Namnet på värd gruppen.</span><span class="sxs-lookup"><span data-stu-id="18e4a-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e4a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18e4a-124">-ResourceGroupName</span></span>
<span data-ttu-id="18e4a-125">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="18e4a-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="18e4a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="18e4a-126">-ResourceId</span></span>
<span data-ttu-id="18e4a-127">ID för resursen.</span><span class="sxs-lookup"><span data-stu-id="18e4a-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="18e4a-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="18e4a-128">-Confirm</span></span>
<span data-ttu-id="18e4a-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="18e4a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18e4a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e4a-130">-WhatIf</span></span>
<span data-ttu-id="18e4a-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="18e4a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18e4a-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="18e4a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18e4a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e4a-133">CommonParameters</span></span>
<span data-ttu-id="18e4a-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e4a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e4a-135">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18e4a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e4a-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="18e4a-136">INPUTS</span></span>

### <span data-ttu-id="18e4a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="18e4a-137">System.String</span></span>

### <span data-ttu-id="18e4a-138">Microsoft. Azure. commands. Compute. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="18e4a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="18e4a-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="18e4a-139">OUTPUTS</span></span>

### <span data-ttu-id="18e4a-140">Microsoft. Azure. commands. Compute. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="18e4a-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="18e4a-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="18e4a-141">NOTES</span></span>

## <span data-ttu-id="18e4a-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="18e4a-142">RELATED LINKS</span></span>
