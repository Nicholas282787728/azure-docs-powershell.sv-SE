---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2LinkedService.md
ms.openlocfilehash: a636dcfabe3f1736f9705724ed302ab40d3637a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573464"
---
# <span data-ttu-id="58d83-101">Remove-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="58d83-101">Remove-AzureRmDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="58d83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="58d83-102">SYNOPSIS</span></span>
<span data-ttu-id="58d83-103">Tar bort en länkad tjänst från data fabrik.</span><span class="sxs-lookup"><span data-stu-id="58d83-103">Removes a linked service from Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58d83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="58d83-104">SYNTAX</span></span>

### <span data-ttu-id="58d83-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="58d83-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58d83-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="58d83-106">ByInputObject</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58d83-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="58d83-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2LinkedService [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58d83-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="58d83-108">DESCRIPTION</span></span>
<span data-ttu-id="58d83-109">Remove-AzureRmDataFactoryV2LinkedService-cmdleten tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="58d83-109">The Remove-AzureRmDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="58d83-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="58d83-110">EXAMPLES</span></span>

### <span data-ttu-id="58d83-111">Exempel 1: ta bort en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="58d83-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="58d83-112">Det här kommandot tar bort den länkade tjänsten som heter LinkedServiceTest från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="58d83-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="58d83-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="58d83-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="58d83-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="58d83-114">PARAMETERS</span></span>

### <span data-ttu-id="58d83-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="58d83-115">-DataFactoryName</span></span>
<span data-ttu-id="58d83-116">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="58d83-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="58d83-117">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="58d83-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58d83-118">-DefaultProfile</span></span>
<span data-ttu-id="58d83-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="58d83-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58d83-120">-Force</span><span class="sxs-lookup"><span data-stu-id="58d83-120">-Force</span></span>
<span data-ttu-id="58d83-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="58d83-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="58d83-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58d83-122">-InputObject</span></span>
<span data-ttu-id="58d83-123">Anger det LinkedService-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="58d83-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: PSLinkedService
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58d83-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="58d83-124">-Name</span></span>
<span data-ttu-id="58d83-125">Anger namnet på den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="58d83-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="58d83-126">Namnet på den länkade tjänsten.</span><span class="sxs-lookup"><span data-stu-id="58d83-126">Name of the linked service.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58d83-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58d83-127">-ResourceGroupName</span></span>
<span data-ttu-id="58d83-128">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="58d83-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="58d83-129">Denna cmdlet tar bort en länkad tjänst från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="58d83-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>


```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d83-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58d83-130">-ResourceId</span></span>
<span data-ttu-id="58d83-131">Azure Resource ID för den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="58d83-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58d83-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="58d83-132">-Confirm</span></span>
<span data-ttu-id="58d83-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58d83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58d83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58d83-134">-WhatIf</span></span>
<span data-ttu-id="58d83-135">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="58d83-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="58d83-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58d83-136">CommonParameters</span></span>
<span data-ttu-id="58d83-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58d83-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58d83-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58d83-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58d83-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="58d83-139">INPUTS</span></span>

### <span data-ttu-id="58d83-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="58d83-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>
<span data-ttu-id="58d83-141">System. String</span><span class="sxs-lookup"><span data-stu-id="58d83-141">System.String</span></span>

## <span data-ttu-id="58d83-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="58d83-142">OUTPUTS</span></span>

### <span data-ttu-id="58d83-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="58d83-143">System.Object</span></span>

## <span data-ttu-id="58d83-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="58d83-144">NOTES</span></span>
<span data-ttu-id="58d83-145">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="58d83-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="58d83-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="58d83-146">RELATED LINKS</span></span>

[<span data-ttu-id="58d83-147">Get-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="58d83-147">Get-AzureRmDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="58d83-148">Set-AzureRmDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="58d83-148">Set-AzureRmDataFactoryV2LinkedService</span></span>]()
