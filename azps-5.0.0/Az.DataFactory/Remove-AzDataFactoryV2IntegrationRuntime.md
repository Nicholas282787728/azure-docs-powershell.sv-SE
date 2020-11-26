---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320892"
---
# <span data-ttu-id="e95a7-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e95a7-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="e95a7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e95a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e95a7-103">Tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="e95a7-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="e95a7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e95a7-104">SYNTAX</span></span>

### <span data-ttu-id="e95a7-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="e95a7-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95a7-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e95a7-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95a7-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e95a7-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e95a7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e95a7-108">DESCRIPTION</span></span>
<span data-ttu-id="e95a7-109">Remove-AzDataFactoryV2IntegrationRuntime cmdlet tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="e95a7-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="e95a7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e95a7-110">EXAMPLES</span></span>

### <span data-ttu-id="e95a7-111">Exempel 1: ta bort en integrations körning</span><span class="sxs-lookup"><span data-stu-id="e95a7-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="e95a7-112">Det här kommandot tar bort integrations körningen med namnet "test-reserverad-IR" från data fabriken med namnet "test-DF".</span><span class="sxs-lookup"><span data-stu-id="e95a7-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="e95a7-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="e95a7-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="e95a7-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e95a7-114">PARAMETERS</span></span>

### <span data-ttu-id="e95a7-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e95a7-115">-DataFactoryName</span></span>
<span data-ttu-id="e95a7-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e95a7-116">The data factory name.</span></span>

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

### <span data-ttu-id="e95a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95a7-117">-DefaultProfile</span></span>
<span data-ttu-id="e95a7-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e95a7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e95a7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e95a7-119">-Force</span></span>
<span data-ttu-id="e95a7-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="e95a7-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="e95a7-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e95a7-121">-InputObject</span></span>
<span data-ttu-id="e95a7-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="e95a7-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="e95a7-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e95a7-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="e95a7-124">Namnet på den länkade data fabriken.</span><span class="sxs-lookup"><span data-stu-id="e95a7-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="e95a7-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="e95a7-125">-Name</span></span>
<span data-ttu-id="e95a7-126">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="e95a7-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="e95a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="e95a7-128">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="e95a7-128">The resource group name.</span></span>

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

### <span data-ttu-id="e95a7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e95a7-129">-ResourceId</span></span>
<span data-ttu-id="e95a7-130">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="e95a7-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e95a7-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e95a7-131">-Confirm</span></span>
<span data-ttu-id="e95a7-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e95a7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95a7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95a7-133">-WhatIf</span></span>
<span data-ttu-id="e95a7-134">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e95a7-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="e95a7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95a7-135">CommonParameters</span></span>
<span data-ttu-id="e95a7-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95a7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95a7-137">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95a7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95a7-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e95a7-138">INPUTS</span></span>

### <span data-ttu-id="e95a7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e95a7-139">System.String</span></span>

### <span data-ttu-id="e95a7-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e95a7-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e95a7-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e95a7-141">OUTPUTS</span></span>

### <span data-ttu-id="e95a7-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="e95a7-142">System.Void</span></span>

## <span data-ttu-id="e95a7-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e95a7-143">NOTES</span></span>
<span data-ttu-id="e95a7-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="e95a7-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e95a7-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e95a7-145">RELATED LINKS</span></span>

[<span data-ttu-id="e95a7-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e95a7-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="e95a7-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e95a7-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
