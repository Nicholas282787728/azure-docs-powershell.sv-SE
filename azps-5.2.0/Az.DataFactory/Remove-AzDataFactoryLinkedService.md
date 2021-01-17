---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: a8731b075ff5df71aa368fa0c1a3c94ade9ef9e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417827"
---
# <span data-ttu-id="29034-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="29034-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="29034-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="29034-102">SYNOPSIS</span></span>
<span data-ttu-id="29034-103">Tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="29034-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="29034-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="29034-104">SYNTAX</span></span>

### <span data-ttu-id="29034-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="29034-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29034-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="29034-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29034-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="29034-107">DESCRIPTION</span></span>
<span data-ttu-id="29034-108">Cmdleten **Remove-AzDataFactoryLinkedService** tar bort en länkad tjänst från Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="29034-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="29034-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="29034-109">EXAMPLES</span></span>

### <span data-ttu-id="29034-110">Exempel 1: ta bort en länkad tjänst</span><span class="sxs-lookup"><span data-stu-id="29034-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="29034-111">Det här kommandot tar bort den länkade tjänsten som heter LinkedServiceTest från data fabriken med namnet WikiADF.</span><span class="sxs-lookup"><span data-stu-id="29034-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="29034-112">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="29034-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="29034-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="29034-113">PARAMETERS</span></span>

### <span data-ttu-id="29034-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="29034-114">-DataFactory</span></span>
<span data-ttu-id="29034-115">Anger ett **PSDataFactory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="29034-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="29034-116">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="29034-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="29034-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="29034-117">-DataFactoryName</span></span>
<span data-ttu-id="29034-118">Anger namnet på en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="29034-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="29034-119">Denna cmdlet tar bort en länkad tjänst från data fabriken som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="29034-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="29034-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29034-120">-DefaultProfile</span></span>
<span data-ttu-id="29034-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="29034-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29034-122">-Force</span><span class="sxs-lookup"><span data-stu-id="29034-122">-Force</span></span>
<span data-ttu-id="29034-123">Anger att denna cmdlet tar bort en länkad tjänst utan att be dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="29034-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="29034-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="29034-124">-Name</span></span>
<span data-ttu-id="29034-125">Anger namnet på den länkade tjänst som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="29034-125">Specifies the name of the linked service to remove.</span></span>

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

### <span data-ttu-id="29034-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29034-126">-ResourceGroupName</span></span>
<span data-ttu-id="29034-127">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="29034-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="29034-128">Denna cmdlet tar bort en länkad tjänst från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="29034-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="29034-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="29034-129">-Confirm</span></span>
<span data-ttu-id="29034-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="29034-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29034-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29034-131">-WhatIf</span></span>
<span data-ttu-id="29034-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="29034-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29034-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="29034-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29034-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29034-134">CommonParameters</span></span>
<span data-ttu-id="29034-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29034-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29034-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29034-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29034-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="29034-137">INPUTS</span></span>

### <span data-ttu-id="29034-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="29034-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="29034-139">System. String</span><span class="sxs-lookup"><span data-stu-id="29034-139">System.String</span></span>

## <span data-ttu-id="29034-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="29034-140">OUTPUTS</span></span>

### <span data-ttu-id="29034-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="29034-141">System.Void</span></span>

## <span data-ttu-id="29034-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="29034-142">NOTES</span></span>
* <span data-ttu-id="29034-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="29034-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="29034-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="29034-144">RELATED LINKS</span></span>

[<span data-ttu-id="29034-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="29034-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="29034-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="29034-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


