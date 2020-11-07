---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryLinkedService.md
ms.openlocfilehash: d3ea4c3f221a3d05c9d43e780cde359ff36843f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756110"
---
# <span data-ttu-id="8411d-101">Remove-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8411d-101">Remove-AzureRmDataFactoryLinkedService</span></span>

## <span data-ttu-id="8411d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8411d-102">SYNOPSIS</span></span>
<span data-ttu-id="8411d-103">Tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8411d-103">Removes a linked service from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8411d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8411d-104">SYNTAX</span></span>

### <span data-ttu-id="8411d-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="8411d-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8411d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8411d-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8411d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8411d-107">DESCRIPTION</span></span>
<span data-ttu-id="8411d-108">Cmdleten **Remove-AzureRmDataFactoryLinkedService** tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="8411d-108">The **Remove-AzureRmDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="8411d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8411d-109">EXAMPLES</span></span>

### <span data-ttu-id="8411d-110">Exempel 1: ta bort en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="8411d-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzureRmDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="8411d-111">Det här kommandot tar bort den länkade tjänsten som heter LinkedServiceTest från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="8411d-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="8411d-112">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="8411d-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="8411d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8411d-113">PARAMETERS</span></span>

### <span data-ttu-id="8411d-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8411d-114">-DataFactory</span></span>
<span data-ttu-id="8411d-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="8411d-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="8411d-116">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8411d-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8411d-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8411d-117">-DataFactoryName</span></span>
<span data-ttu-id="8411d-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8411d-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="8411d-119">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8411d-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="8411d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8411d-120">-Force</span></span>
<span data-ttu-id="8411d-121">Anger att denna cmdlet tar bort en länkad tjänst utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="8411d-121">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="8411d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="8411d-122">-Name</span></span>
<span data-ttu-id="8411d-123">Anger namnet på den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8411d-123">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8411d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8411d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8411d-125">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="8411d-125">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="8411d-126">Denna cmdlet tar bort en länkad tjänst från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="8411d-126">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8411d-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8411d-127">-Confirm</span></span>
<span data-ttu-id="8411d-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8411d-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8411d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8411d-129">-WhatIf</span></span>
<span data-ttu-id="8411d-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8411d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8411d-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8411d-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8411d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8411d-132">-DefaultProfile</span></span>
<span data-ttu-id="8411d-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8411d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8411d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8411d-134">CommonParameters</span></span>
<span data-ttu-id="8411d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8411d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8411d-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8411d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8411d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8411d-137">INPUTS</span></span>

## <span data-ttu-id="8411d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8411d-138">OUTPUTS</span></span>

### <span data-ttu-id="8411d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8411d-139">System.Boolean</span></span>

## <span data-ttu-id="8411d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8411d-140">NOTES</span></span>
* <span data-ttu-id="8411d-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="8411d-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8411d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8411d-142">RELATED LINKS</span></span>

[<span data-ttu-id="8411d-143">Get-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8411d-143">Get-AzureRmDataFactoryLinkedService</span></span>](./Get-AzureRmDataFactoryLinkedService.md)

[<span data-ttu-id="8411d-144">New-AzureRmDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="8411d-144">New-AzureRmDataFactoryLinkedService</span></span>](./New-AzureRmDataFactoryLinkedService.md)


