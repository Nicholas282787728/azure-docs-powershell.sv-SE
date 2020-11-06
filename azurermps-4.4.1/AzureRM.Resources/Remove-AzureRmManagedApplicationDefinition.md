---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583792"
---
# <span data-ttu-id="f4082-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="f4082-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="f4082-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4082-102">SYNOPSIS</span></span>
<span data-ttu-id="f4082-103">Tar bort en definition för hanterade program</span><span class="sxs-lookup"><span data-stu-id="f4082-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4082-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4082-104">SYNTAX</span></span>

### <span data-ttu-id="f4082-105">Parameter uppsättning för hanterade program namn.</span><span class="sxs-lookup"><span data-stu-id="f4082-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="f4082-106">Vis</span><span class="sxs-lookup"><span data-stu-id="f4082-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4082-107">Parameter uppsättning för definition av hanterade program.</span><span class="sxs-lookup"><span data-stu-id="f4082-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4082-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4082-108">DESCRIPTION</span></span>
<span data-ttu-id="f4082-109">Cmdleten **Remove-AzureRmManagedApplicationDefinition** tar bort en definition för hanterade program</span><span class="sxs-lookup"><span data-stu-id="f4082-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="f4082-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4082-110">EXAMPLES</span></span>

### <span data-ttu-id="f4082-111">Exempel 1: ta bort definitionen av hanterade program utifrån resurs-ID</span><span class="sxs-lookup"><span data-stu-id="f4082-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="f4082-112">Det första kommandot får en hanterad program definition med namnet myAppDef med hjälp av Get-AzureRmManagedApplicationDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4082-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="f4082-113">Kommandot sparar det i $ApplicationDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="f4082-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="f4082-114">Det andra kommandot tar bort definitionen för hanterade program som identifieras av egenskapen **ResourceID** för $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="f4082-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="f4082-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4082-115">PARAMETERS</span></span>

### <span data-ttu-id="f4082-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f4082-116">-ApiVersion</span></span>
<span data-ttu-id="f4082-117">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f4082-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f4082-118">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="f4082-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f4082-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4082-119">-DefaultProfile</span></span>
<span data-ttu-id="f4082-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4082-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4082-121">-Force</span><span class="sxs-lookup"><span data-stu-id="f4082-121">-Force</span></span>
<span data-ttu-id="f4082-122">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="f4082-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f4082-123">-ID</span><span class="sxs-lookup"><span data-stu-id="f4082-123">-Id</span></span>
<span data-ttu-id="f4082-124">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="f4082-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="f4082-125">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="f4082-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4082-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4082-126">-Name</span></span>
<span data-ttu-id="f4082-127">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="f4082-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4082-128">-För</span><span class="sxs-lookup"><span data-stu-id="f4082-128">-Pre</span></span>
<span data-ttu-id="f4082-129">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f4082-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f4082-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4082-130">-ResourceGroupName</span></span>
<span data-ttu-id="f4082-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="f4082-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4082-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4082-132">-Confirm</span></span>
<span data-ttu-id="f4082-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4082-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4082-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4082-134">-WhatIf</span></span>
<span data-ttu-id="f4082-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4082-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4082-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4082-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4082-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4082-137">CommonParameters</span></span>
<span data-ttu-id="f4082-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4082-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4082-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4082-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4082-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4082-140">INPUTS</span></span>

### <span data-ttu-id="f4082-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f4082-141">System.String</span></span>

## <span data-ttu-id="f4082-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4082-142">OUTPUTS</span></span>

### <span data-ttu-id="f4082-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4082-143">System.Boolean</span></span>

## <span data-ttu-id="f4082-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4082-144">NOTES</span></span>

## <span data-ttu-id="f4082-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4082-145">RELATED LINKS</span></span>

