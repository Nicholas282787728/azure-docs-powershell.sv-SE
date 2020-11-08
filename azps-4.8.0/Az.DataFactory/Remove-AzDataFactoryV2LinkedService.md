---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: acd3fadd45dfc32c745af943013f4c0f00b663ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262316"
---
# <span data-ttu-id="d84ca-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d84ca-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="d84ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d84ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d84ca-103">Tar bort en länkad tjänst från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="d84ca-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="d84ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d84ca-104">SYNTAX</span></span>

### <span data-ttu-id="d84ca-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="d84ca-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d84ca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d84ca-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d84ca-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d84ca-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d84ca-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d84ca-108">DESCRIPTION</span></span>
<span data-ttu-id="d84ca-109">Remove-AzDataFactoryV2LinkedService-cmdleten tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d84ca-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="d84ca-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d84ca-110">EXAMPLES</span></span>

### <span data-ttu-id="d84ca-111">Exempel 1: ta bort en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="d84ca-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="d84ca-112">Det här kommandot tar bort den länkade tjänsten som heter LinkedServiceTest från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d84ca-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="d84ca-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="d84ca-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="d84ca-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d84ca-114">PARAMETERS</span></span>

### <span data-ttu-id="d84ca-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d84ca-115">-DataFactoryName</span></span>
<span data-ttu-id="d84ca-116">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="d84ca-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d84ca-117">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d84ca-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84ca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84ca-118">-DefaultProfile</span></span>
<span data-ttu-id="d84ca-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d84ca-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d84ca-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d84ca-120">-Force</span></span>
<span data-ttu-id="d84ca-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d84ca-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="d84ca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d84ca-122">-InputObject</span></span>
<span data-ttu-id="d84ca-123">Anger det LinkedService-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d84ca-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d84ca-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="d84ca-124">-Name</span></span>
<span data-ttu-id="d84ca-125">Anger namnet på den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d84ca-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="d84ca-126">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="d84ca-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d84ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="d84ca-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="d84ca-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d84ca-129">Denna cmdlet tar bort en länkad tjänst från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="d84ca-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84ca-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d84ca-130">-ResourceId</span></span>
<span data-ttu-id="d84ca-131">Azure Resource ID för den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d84ca-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d84ca-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d84ca-132">-Confirm</span></span>
<span data-ttu-id="d84ca-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d84ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d84ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84ca-134">-WhatIf</span></span>
<span data-ttu-id="d84ca-135">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d84ca-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="d84ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84ca-136">CommonParameters</span></span>
<span data-ttu-id="d84ca-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84ca-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d84ca-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84ca-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d84ca-139">INPUTS</span></span>

### <span data-ttu-id="d84ca-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="d84ca-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="d84ca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d84ca-141">System.String</span></span>

## <span data-ttu-id="d84ca-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d84ca-142">OUTPUTS</span></span>

### <span data-ttu-id="d84ca-143">System. Void</span><span class="sxs-lookup"><span data-stu-id="d84ca-143">System.Void</span></span>

## <span data-ttu-id="d84ca-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d84ca-144">NOTES</span></span>
<span data-ttu-id="d84ca-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="d84ca-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d84ca-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d84ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="d84ca-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d84ca-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="d84ca-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="d84ca-148">Set-AzDataFactoryV2LinkedService</span></span>]()

