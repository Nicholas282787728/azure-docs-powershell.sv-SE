---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a2515b3713f449d25963af5952e233117e078ba9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573466"
---
# <span data-ttu-id="4e824-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e824-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4e824-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4e824-102">SYNOPSIS</span></span>
<span data-ttu-id="4e824-103">Tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="4e824-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e824-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4e824-104">SYNTAX</span></span>

### <span data-ttu-id="4e824-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="4e824-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e824-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e824-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e824-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4e824-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e824-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4e824-108">DESCRIPTION</span></span>
<span data-ttu-id="4e824-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="4e824-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="4e824-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4e824-110">EXAMPLES</span></span>

### <span data-ttu-id="4e824-111">Exempel 1: ta bort en integrations körning</span><span class="sxs-lookup"><span data-stu-id="4e824-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="4e824-112">Det här kommandot tar bort integrations körningen med namnet "test-reserverad-IR" från data fabriken med namnet "test-DF".</span><span class="sxs-lookup"><span data-stu-id="4e824-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="4e824-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="4e824-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="4e824-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4e824-114">PARAMETERS</span></span>

### <span data-ttu-id="4e824-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4e824-115">-DataFactoryName</span></span>
<span data-ttu-id="4e824-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="4e824-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e824-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e824-117">-DefaultProfile</span></span>
<span data-ttu-id="4e824-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4e824-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e824-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4e824-119">-Force</span></span>
<span data-ttu-id="4e824-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="4e824-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4e824-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e824-121">-InputObject</span></span>
<span data-ttu-id="4e824-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="4e824-122">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e824-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="4e824-123">-Name</span></span>
<span data-ttu-id="4e824-124">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="4e824-124">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e824-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e824-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e824-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4e824-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e824-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e824-127">-ResourceId</span></span>
<span data-ttu-id="4e824-128">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="4e824-128">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e824-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4e824-129">-Confirm</span></span>
<span data-ttu-id="4e824-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e824-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e824-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e824-131">-WhatIf</span></span>
<span data-ttu-id="4e824-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4e824-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4e824-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e824-133">CommonParameters</span></span>
<span data-ttu-id="4e824-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e824-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e824-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e824-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e824-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4e824-136">INPUTS</span></span>

### <span data-ttu-id="4e824-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4e824-137">System.String</span></span>
<span data-ttu-id="4e824-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e824-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4e824-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4e824-139">OUTPUTS</span></span>

### <span data-ttu-id="4e824-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="4e824-140">System.Object</span></span>

## <span data-ttu-id="4e824-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4e824-141">NOTES</span></span>
<span data-ttu-id="4e824-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="4e824-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4e824-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4e824-143">RELATED LINKS</span></span>

[<span data-ttu-id="4e824-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e824-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="4e824-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4e824-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

