---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: bf29e12292fba12cc6a5b4f99cef1e13f9d9fd8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579728"
---
# <span data-ttu-id="a1c44-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a1c44-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="a1c44-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1c44-102">SYNOPSIS</span></span>
<span data-ttu-id="a1c44-103">Tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="a1c44-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1c44-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1c44-104">SYNTAX</span></span>

### <span data-ttu-id="a1c44-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="a1c44-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1c44-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1c44-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1c44-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a1c44-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1c44-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1c44-108">DESCRIPTION</span></span>
<span data-ttu-id="a1c44-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="a1c44-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="a1c44-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1c44-110">EXAMPLES</span></span>

### <span data-ttu-id="a1c44-111">Exempel 1: ta bort en integrations körning</span><span class="sxs-lookup"><span data-stu-id="a1c44-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="a1c44-112">Det här kommandot tar bort integrations körningen med namnet "test-reserverad-IR" från data fabriken med namnet "test-DF".</span><span class="sxs-lookup"><span data-stu-id="a1c44-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="a1c44-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="a1c44-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="a1c44-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1c44-114">PARAMETERS</span></span>

### <span data-ttu-id="a1c44-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a1c44-115">-DataFactoryName</span></span>
<span data-ttu-id="a1c44-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="a1c44-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c44-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a1c44-117">-Force</span></span>
<span data-ttu-id="a1c44-118">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a1c44-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a1c44-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1c44-119">-InputObject</span></span>
<span data-ttu-id="a1c44-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="a1c44-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c44-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1c44-121">-Name</span></span>
<span data-ttu-id="a1c44-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="a1c44-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c44-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1c44-123">-ResourceGroupName</span></span>
<span data-ttu-id="a1c44-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a1c44-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c44-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1c44-125">-ResourceId</span></span>
<span data-ttu-id="a1c44-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="a1c44-126">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1c44-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1c44-127">-Confirm</span></span>
<span data-ttu-id="a1c44-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1c44-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1c44-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1c44-129">-WhatIf</span></span>
<span data-ttu-id="a1c44-130">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1c44-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a1c44-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1c44-131">-DefaultProfile</span></span>
<span data-ttu-id="a1c44-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1c44-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1c44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1c44-133">CommonParameters</span></span>
<span data-ttu-id="a1c44-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1c44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1c44-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1c44-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1c44-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1c44-136">INPUTS</span></span>

### <span data-ttu-id="a1c44-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a1c44-137">System.String</span></span>
<span data-ttu-id="a1c44-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a1c44-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a1c44-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1c44-139">OUTPUTS</span></span>

### <span data-ttu-id="a1c44-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="a1c44-140">System.Object</span></span>

## <span data-ttu-id="a1c44-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1c44-141">NOTES</span></span>
<span data-ttu-id="a1c44-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="a1c44-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="a1c44-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1c44-143">RELATED LINKS</span></span>

[<span data-ttu-id="a1c44-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a1c44-144">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="a1c44-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a1c44-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
