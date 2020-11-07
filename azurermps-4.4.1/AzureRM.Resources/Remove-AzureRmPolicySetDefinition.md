---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicySetDefinition.md
ms.openlocfilehash: d3b9d8af81f08786536abf0d26b3c4ba2f2d66bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756556"
---
# <span data-ttu-id="000bc-101">Remove-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="000bc-101">Remove-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="000bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="000bc-102">SYNOPSIS</span></span>
<span data-ttu-id="000bc-103">Tar bort en uppsättning definitioner för principer.</span><span class="sxs-lookup"><span data-stu-id="000bc-103">Removes a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="000bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="000bc-104">SYNTAX</span></span>

### <span data-ttu-id="000bc-105">Parameter uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="000bc-105">The policy set definition name parameter set.</span></span> <span data-ttu-id="000bc-106">Vis</span><span class="sxs-lookup"><span data-stu-id="000bc-106">(Default)</span></span>
```
Remove-AzureRmPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="000bc-107">Parametern uppsättning med Definitions-ID för princip uppsättning.</span><span class="sxs-lookup"><span data-stu-id="000bc-107">The policy set definition Id parameter set.</span></span>
```
Remove-AzureRmPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="000bc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="000bc-108">DESCRIPTION</span></span>
<span data-ttu-id="000bc-109">Cmdleten **Remove-AzureRmPolicySetDefinition** tar bort en princip definition.</span><span class="sxs-lookup"><span data-stu-id="000bc-109">The **Remove-AzureRmPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="000bc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="000bc-110">EXAMPLES</span></span>

### <span data-ttu-id="000bc-111">Exempel 1: ta bort princip uppsättnings definition efter resurs-ID</span><span class="sxs-lookup"><span data-stu-id="000bc-111">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\>$PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId "/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition"
PS C:\>Remove-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="000bc-112">Det första kommandot får en princip uppsättnings definition med hjälp av Get-AzureRmPolicySetDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="000bc-112">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="000bc-113">Kommandot sparar det i $PolicySetDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="000bc-113">The command stores it in the $PolicySetDefinition variable.</span></span>

<span data-ttu-id="000bc-114">Det andra kommandot tar bort princip uppsättnings definitionen som identifieras av egenskapen **ResourceID** för $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="000bc-114">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="000bc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="000bc-115">PARAMETERS</span></span>

### <span data-ttu-id="000bc-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="000bc-116">-ApiVersion</span></span>
<span data-ttu-id="000bc-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="000bc-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="000bc-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="000bc-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="000bc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="000bc-119">-Force</span></span>
<span data-ttu-id="000bc-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="000bc-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="000bc-121">-ID</span><span class="sxs-lookup"><span data-stu-id="000bc-121">-Id</span></span>
<span data-ttu-id="000bc-122">Det fullständiga kvalificerade princip uppsättningens Definitions-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="000bc-122">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="000bc-123">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="000bc-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000bc-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="000bc-124">-Name</span></span>
<span data-ttu-id="000bc-125">Princip uppsättningens definitions namn.</span><span class="sxs-lookup"><span data-stu-id="000bc-125">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="000bc-126">-För</span><span class="sxs-lookup"><span data-stu-id="000bc-126">-Pre</span></span>
<span data-ttu-id="000bc-127">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="000bc-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="000bc-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="000bc-128">-Confirm</span></span>
<span data-ttu-id="000bc-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="000bc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="000bc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="000bc-130">-WhatIf</span></span>
<span data-ttu-id="000bc-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="000bc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="000bc-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="000bc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="000bc-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000bc-133">-DefaultProfile</span></span>
<span data-ttu-id="000bc-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="000bc-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="000bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000bc-135">CommonParameters</span></span>
<span data-ttu-id="000bc-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="000bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000bc-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="000bc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000bc-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="000bc-138">INPUTS</span></span>

### <span data-ttu-id="000bc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="000bc-139">System.String</span></span>

## <span data-ttu-id="000bc-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="000bc-140">OUTPUTS</span></span>

### <span data-ttu-id="000bc-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="000bc-141">System.Boolean</span></span>

## <span data-ttu-id="000bc-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="000bc-142">NOTES</span></span>

## <span data-ttu-id="000bc-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="000bc-143">RELATED LINKS</span></span>

