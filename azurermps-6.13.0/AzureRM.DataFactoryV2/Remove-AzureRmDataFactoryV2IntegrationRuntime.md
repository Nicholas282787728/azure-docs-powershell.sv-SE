---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8c7ec74e43586a951b3f8d2c4d8af0caa6e09a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572835"
---
# <span data-ttu-id="5f8e0-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f8e0-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5f8e0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="5f8e0-103">Tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f8e0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f8e0-104">SYNTAX</span></span>

### <span data-ttu-id="5f8e0-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="5f8e0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f8e0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f8e0-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f8e0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5f8e0-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f8e0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f8e0-108">DESCRIPTION</span></span>
<span data-ttu-id="5f8e0-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="5f8e0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f8e0-110">EXAMPLES</span></span>

### <span data-ttu-id="5f8e0-111">Exempel 1: ta bort en integrations körning</span><span class="sxs-lookup"><span data-stu-id="5f8e0-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="5f8e0-112">Det här kommandot tar bort integrations körningen med namnet "test-reserverad-IR" från data fabriken med namnet "test-DF".</span><span class="sxs-lookup"><span data-stu-id="5f8e0-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="5f8e0-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="5f8e0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f8e0-114">PARAMETERS</span></span>

### <span data-ttu-id="5f8e0-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5f8e0-115">-DataFactoryName</span></span>
<span data-ttu-id="5f8e0-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-116">The data factory name.</span></span>

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

### <span data-ttu-id="5f8e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f8e0-117">-DefaultProfile</span></span>
<span data-ttu-id="5f8e0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f8e0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5f8e0-119">-Force</span></span>
<span data-ttu-id="5f8e0-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5f8e0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f8e0-121">-InputObject</span></span>
<span data-ttu-id="5f8e0-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="5f8e0-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5f8e0-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="5f8e0-124">Namnet på den länkade data fabriken.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="5f8e0-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f8e0-125">-Name</span></span>
<span data-ttu-id="5f8e0-126">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="5f8e0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f8e0-127">-ResourceGroupName</span></span>
<span data-ttu-id="5f8e0-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-128">The resource group name.</span></span>

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

### <span data-ttu-id="5f8e0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f8e0-129">-ResourceId</span></span>
<span data-ttu-id="5f8e0-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5f8e0-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5f8e0-131">-Confirm</span></span>
<span data-ttu-id="5f8e0-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f8e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f8e0-133">-WhatIf</span></span>
<span data-ttu-id="5f8e0-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5f8e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f8e0-135">CommonParameters</span></span>
<span data-ttu-id="5f8e0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f8e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f8e0-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f8e0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f8e0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f8e0-138">INPUTS</span></span>

### <span data-ttu-id="5f8e0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5f8e0-139">System.String</span></span>

### <span data-ttu-id="5f8e0-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f8e0-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="5f8e0-141">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f8e0-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5f8e0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f8e0-142">OUTPUTS</span></span>

### <span data-ttu-id="5f8e0-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="5f8e0-143">System.Void</span></span>

## <span data-ttu-id="5f8e0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f8e0-144">NOTES</span></span>
<span data-ttu-id="5f8e0-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="5f8e0-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="5f8e0-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f8e0-146">RELATED LINKS</span></span>

[<span data-ttu-id="5f8e0-147">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f8e0-147">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="5f8e0-148">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f8e0-148">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

