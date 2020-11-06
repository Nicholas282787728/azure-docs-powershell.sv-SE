---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: fa96d686d66f9ef94322896974dc4dd3b81ad154
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579428"
---
# <span data-ttu-id="788db-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="788db-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="788db-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="788db-102">SYNOPSIS</span></span>
<span data-ttu-id="788db-103">Tar bort en uppsättning definitioner för principer.</span><span class="sxs-lookup"><span data-stu-id="788db-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="788db-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="788db-104">SYNTAX</span></span>

### <span data-ttu-id="788db-105">RemoveByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="788db-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="788db-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="788db-106">RemoveById</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="788db-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="788db-107">DESCRIPTION</span></span>
<span data-ttu-id="788db-108">Cmdleten **Remove-AzureRmPolicySetDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="788db-108">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="788db-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="788db-109">EXAMPLES</span></span>

### <span data-ttu-id="788db-110">Exempel 1: ta bort princip uppsättnings definition efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="788db-110">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="788db-111">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzureRmPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="788db-111">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="788db-112">Kommandot sparar det i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="788db-112">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="788db-113">Det andra kommandot tar bort princip uppsättnings definitionen som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="788db-113">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="788db-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="788db-114">PARAMETERS</span></span>

### <span data-ttu-id="788db-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="788db-115">-ApiVersion</span></span>
<span data-ttu-id="788db-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="788db-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="788db-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="788db-117">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788db-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="788db-118">-DefaultProfile</span></span>
<span data-ttu-id="788db-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="788db-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788db-120">-Force</span><span class="sxs-lookup"><span data-stu-id="788db-120">-Force</span></span>
<span data-ttu-id="788db-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="788db-121">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788db-122">-ID</span><span class="sxs-lookup"><span data-stu-id="788db-122">-Id</span></span>
<span data-ttu-id="788db-123">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="788db-123">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="788db-124">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="788db-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="788db-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="788db-125">-Name</span></span>
<span data-ttu-id="788db-126">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="788db-126">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="788db-127">-För</span><span class="sxs-lookup"><span data-stu-id="788db-127">-Pre</span></span>
<span data-ttu-id="788db-128">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="788db-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788db-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="788db-129">-Confirm</span></span>
<span data-ttu-id="788db-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="788db-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="788db-131">-WhatIf</span></span>
<span data-ttu-id="788db-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="788db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="788db-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="788db-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="788db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="788db-134">CommonParameters</span></span>
<span data-ttu-id="788db-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="788db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="788db-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="788db-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="788db-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="788db-137">INPUTS</span></span>

### <span data-ttu-id="788db-138">System. String</span><span class="sxs-lookup"><span data-stu-id="788db-138">System.String</span></span>

## <span data-ttu-id="788db-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="788db-139">OUTPUTS</span></span>

### <span data-ttu-id="788db-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="788db-140">System.Boolean</span></span>

## <span data-ttu-id="788db-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="788db-141">NOTES</span></span>

## <span data-ttu-id="788db-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="788db-142">RELATED LINKS</span></span>
