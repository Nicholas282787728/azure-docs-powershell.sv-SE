---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: 94321cc8f9d42cd4ef26e617426f844b9774b5b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577241"
---
# <span data-ttu-id="04ffa-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="04ffa-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="04ffa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="04ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="04ffa-103">Tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="04ffa-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04ffa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="04ffa-104">SYNTAX</span></span>

### <span data-ttu-id="04ffa-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="04ffa-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04ffa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="04ffa-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ffa-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="04ffa-107">DESCRIPTION</span></span>
<span data-ttu-id="04ffa-108">Cmdleten **Remove-AzureRmDataFactoryLinkedService** tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="04ffa-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="04ffa-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="04ffa-109">EXAMPLES</span></span>

### <span data-ttu-id="04ffa-110">Exempel 1: ta bort en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="04ffa-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="04ffa-111">Det här kommandot tar bort den länkade tjänsten som heter LinkedServiceTest från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="04ffa-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="04ffa-112">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="04ffa-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="04ffa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="04ffa-113">PARAMETERS</span></span>

### <span data-ttu-id="04ffa-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="04ffa-114">-DataFactory</span></span>
<span data-ttu-id="04ffa-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="04ffa-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="04ffa-116">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="04ffa-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ffa-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="04ffa-117">-DataFactoryName</span></span>
<span data-ttu-id="04ffa-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="04ffa-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="04ffa-119">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="04ffa-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="04ffa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ffa-120">-DefaultProfile</span></span>
<span data-ttu-id="04ffa-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="04ffa-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04ffa-122">-Force</span><span class="sxs-lookup"><span data-stu-id="04ffa-122">-Force</span></span>
<span data-ttu-id="04ffa-123">Anger att denna cmdlet tar bort en länkad tjänst utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="04ffa-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="04ffa-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="04ffa-124">-Name</span></span>
<span data-ttu-id="04ffa-125">Anger namnet på den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="04ffa-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ffa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ffa-126">-ResourceGroupName</span></span>
<span data-ttu-id="04ffa-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="04ffa-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="04ffa-128">Denna cmdlet tar bort en länkad tjänst från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="04ffa-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="04ffa-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="04ffa-129">-Confirm</span></span>
<span data-ttu-id="04ffa-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="04ffa-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ffa-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ffa-131">-WhatIf</span></span>
<span data-ttu-id="04ffa-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="04ffa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04ffa-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="04ffa-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ffa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ffa-134">CommonParameters</span></span>
<span data-ttu-id="04ffa-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ffa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ffa-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ffa-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ffa-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="04ffa-137">INPUTS</span></span>

### <span data-ttu-id="04ffa-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="04ffa-138">None</span></span>
<span data-ttu-id="04ffa-139">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="04ffa-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04ffa-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="04ffa-140">OUTPUTS</span></span>

### <span data-ttu-id="04ffa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04ffa-141">System.Boolean</span></span>

## <span data-ttu-id="04ffa-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="04ffa-142">NOTES</span></span>
* <span data-ttu-id="04ffa-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="04ffa-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="04ffa-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="04ffa-144">RELATED LINKS</span></span>

[<span data-ttu-id="04ffa-145">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="04ffa-145">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="04ffa-146">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="04ffa-146">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


