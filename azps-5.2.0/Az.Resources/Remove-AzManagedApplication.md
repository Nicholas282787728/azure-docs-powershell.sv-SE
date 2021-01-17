---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagedApplication.md
ms.openlocfilehash: 17a28da26aa26860b7fd4a28ec922932bb089da3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408163"
---
# <span data-ttu-id="5eb3c-101">Remove-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="5eb3c-101">Remove-AzManagedApplication</span></span>

## <span data-ttu-id="5eb3c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5eb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb3c-103">Tar bort ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="5eb3c-103">Removes a managed application</span></span>

## <span data-ttu-id="5eb3c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5eb3c-104">SYNTAX</span></span>

### <span data-ttu-id="5eb3c-105">RemoveByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="5eb3c-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzManagedApplication -Name <String> -ResourceGroupName <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5eb3c-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="5eb3c-106">RemoveById</span></span>
```
Remove-AzManagedApplication -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5eb3c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5eb3c-107">DESCRIPTION</span></span>
<span data-ttu-id="5eb3c-108">Cmdleten **Remove-AzManagedApplication** tar bort ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="5eb3c-108">The **Remove-AzManagedApplication** cmdlet removes a managed application</span></span>

## <span data-ttu-id="5eb3c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5eb3c-109">EXAMPLES</span></span>

### <span data-ttu-id="5eb3c-110">Exempel 1: ta bort hanterat program via resurs-ID</span><span class="sxs-lookup"><span data-stu-id="5eb3c-110">Example 1: Remove managed application by resource ID</span></span>
```
PS C:\>$Application = Get-AzManagedApplication -Name "myApp" -ResourceGroupName "myRG"
PS C:\>Remove-AzManagedApplication -Id $Application.ResourceId -Force
```

<span data-ttu-id="5eb3c-111">Det första kommandot får ett hanterat program som heter Mittprog med hjälp av Get-AzManagedApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-111">The first command gets a managed application named myApp by using the Get-AzManagedApplication cmdlet.</span></span>
<span data-ttu-id="5eb3c-112">Kommandot sparar det i $Application variabel.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-112">The command stores it in the $Application variable.</span></span>
<span data-ttu-id="5eb3c-113">Det andra kommandot tar bort det hanterade programmet som identifieras av egenskapen **ResourceID** för $application.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-113">The second command removes the managed application identified by the **ResourceId** property of $Application.</span></span>

## <span data-ttu-id="5eb3c-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5eb3c-114">PARAMETERS</span></span>

### <span data-ttu-id="5eb3c-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="5eb3c-115">-ApiVersion</span></span>
<span data-ttu-id="5eb3c-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="5eb3c-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5eb3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb3c-118">-DefaultProfile</span></span>
<span data-ttu-id="5eb3c-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5eb3c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5eb3c-120">-Force</span></span>
<span data-ttu-id="5eb3c-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5eb3c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="5eb3c-122">-Id</span></span>
<span data-ttu-id="5eb3c-123">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="5eb3c-124">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="5eb3c-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb3c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5eb3c-125">-Name</span></span>
<span data-ttu-id="5eb3c-126">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb3c-127">-För</span><span class="sxs-lookup"><span data-stu-id="5eb3c-127">-Pre</span></span>
<span data-ttu-id="5eb3c-128">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5eb3c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb3c-129">-ResourceGroupName</span></span>
<span data-ttu-id="5eb3c-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5eb3c-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5eb3c-131">-Confirm</span></span>
<span data-ttu-id="5eb3c-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5eb3c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5eb3c-133">-WhatIf</span></span>
<span data-ttu-id="5eb3c-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5eb3c-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5eb3c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb3c-136">CommonParameters</span></span>
<span data-ttu-id="5eb3c-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb3c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb3c-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5eb3c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb3c-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5eb3c-139">INPUTS</span></span>

### <span data-ttu-id="5eb3c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5eb3c-140">System.String</span></span>

## <span data-ttu-id="5eb3c-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5eb3c-141">OUTPUTS</span></span>

### <span data-ttu-id="5eb3c-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5eb3c-142">System.Boolean</span></span>

## <span data-ttu-id="5eb3c-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5eb3c-143">NOTES</span></span>

## <span data-ttu-id="5eb3c-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5eb3c-144">RELATED LINKS</span></span>
