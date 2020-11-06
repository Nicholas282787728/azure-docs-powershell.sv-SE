---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermmanagedapplicationdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: d8257c2f6d37ebd6c304fd511e889d8314fd0266
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576773"
---
# <span data-ttu-id="a60fe-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="a60fe-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="a60fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a60fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a60fe-103">Tar bort en definition för hanterade program</span><span class="sxs-lookup"><span data-stu-id="a60fe-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a60fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a60fe-104">SYNTAX</span></span>

### <span data-ttu-id="a60fe-105">RemoveByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="a60fe-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a60fe-106">RemoveById</span><span class="sxs-lookup"><span data-stu-id="a60fe-106">RemoveById</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a60fe-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a60fe-107">DESCRIPTION</span></span>
<span data-ttu-id="a60fe-108">Cmdleten **Remove-AzureRmManagedApplicationDefinition** tar bort en definition för hanterade program</span><span class="sxs-lookup"><span data-stu-id="a60fe-108">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="a60fe-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a60fe-109">EXAMPLES</span></span>

### <span data-ttu-id="a60fe-110">Exempel 1: ta bort definitionen av hanterade program utifrån resurs-ID</span><span class="sxs-lookup"><span data-stu-id="a60fe-110">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="a60fe-111">Det första kommandot får en hanterad program definition med namnet myAppDef med hjälp av Get-AzureRmManagedApplicationDefinition cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60fe-111">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="a60fe-112">Kommandot sparar det i $ApplicationDefinition variabel.</span><span class="sxs-lookup"><span data-stu-id="a60fe-112">The command stores it in the $ApplicationDefinition variable.</span></span>
<span data-ttu-id="a60fe-113">Det andra kommandot tar bort definitionen för hanterade program som identifieras av egenskapen **ResourceID** för $ApplicationDefinition.</span><span class="sxs-lookup"><span data-stu-id="a60fe-113">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="a60fe-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a60fe-114">PARAMETERS</span></span>

### <span data-ttu-id="a60fe-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a60fe-115">-ApiVersion</span></span>
<span data-ttu-id="a60fe-116">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a60fe-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a60fe-117">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="a60fe-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a60fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60fe-118">-DefaultProfile</span></span>
<span data-ttu-id="a60fe-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a60fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a60fe-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a60fe-120">-Force</span></span>
<span data-ttu-id="a60fe-121">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a60fe-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a60fe-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a60fe-122">-Id</span></span>
<span data-ttu-id="a60fe-123">Fullständigt kvalificerat ID för hanterade program, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="a60fe-123">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="a60fe-124">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="a60fe-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="a60fe-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a60fe-125">-Name</span></span>
<span data-ttu-id="a60fe-126">Det hanterade programmets definitions namn.</span><span class="sxs-lookup"><span data-stu-id="a60fe-126">The managed application definition name.</span></span>

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

### <span data-ttu-id="a60fe-127">-För</span><span class="sxs-lookup"><span data-stu-id="a60fe-127">-Pre</span></span>
<span data-ttu-id="a60fe-128">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a60fe-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a60fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="a60fe-130">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a60fe-130">The resource group name.</span></span>

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

### <span data-ttu-id="a60fe-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a60fe-131">-Confirm</span></span>
<span data-ttu-id="a60fe-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a60fe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a60fe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a60fe-133">-WhatIf</span></span>
<span data-ttu-id="a60fe-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a60fe-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a60fe-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a60fe-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a60fe-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60fe-136">CommonParameters</span></span>
<span data-ttu-id="a60fe-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60fe-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60fe-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a60fe-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60fe-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a60fe-139">INPUTS</span></span>

### <span data-ttu-id="a60fe-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a60fe-140">System.String</span></span>

## <span data-ttu-id="a60fe-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a60fe-141">OUTPUTS</span></span>

### <span data-ttu-id="a60fe-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a60fe-142">System.Boolean</span></span>

## <span data-ttu-id="a60fe-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a60fe-143">NOTES</span></span>

## <span data-ttu-id="a60fe-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a60fe-144">RELATED LINKS</span></span>
