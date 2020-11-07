---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 74e72488d8a7a98b9f81b85599ed7e0867ed2ba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757102"
---
# <span data-ttu-id="a6f16-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6f16-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="a6f16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a6f16-102">SYNOPSIS</span></span>
<span data-ttu-id="a6f16-103">Tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a6f16-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6f16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a6f16-104">SYNTAX</span></span>

### <span data-ttu-id="a6f16-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="a6f16-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6f16-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a6f16-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6f16-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a6f16-107">DESCRIPTION</span></span>
<span data-ttu-id="a6f16-108">Cmdleten **Remove-AzureRmDataFactory** tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a6f16-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="a6f16-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a6f16-109">EXAMPLES</span></span>

### <span data-ttu-id="a6f16-110">Exempel 1: ta bort en data fabrik</span><span class="sxs-lookup"><span data-stu-id="a6f16-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="a6f16-111">Det här kommandot tar bort data fabriken med namnet WikiADF från resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="a6f16-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="a6f16-112">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="a6f16-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="a6f16-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a6f16-113">PARAMETERS</span></span>

### <span data-ttu-id="a6f16-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a6f16-114">-DataFactory</span></span>
<span data-ttu-id="a6f16-115">Anger det **PSDataFactory** -objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a6f16-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="a6f16-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6f16-116">-DefaultProfile</span></span>
<span data-ttu-id="a6f16-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a6f16-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6f16-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a6f16-118">-Force</span></span>
<span data-ttu-id="a6f16-119">Anger att denna cmdlet tar bort en data fabrik utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a6f16-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a6f16-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="a6f16-120">-Name</span></span>
<span data-ttu-id="a6f16-121">Anger namnet på data fabriken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="a6f16-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6f16-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6f16-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6f16-123">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="a6f16-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a6f16-124">Denna cmdlet tar bort en data fabrik från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a6f16-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a6f16-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a6f16-125">-Confirm</span></span>
<span data-ttu-id="a6f16-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a6f16-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6f16-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6f16-127">-WhatIf</span></span>
<span data-ttu-id="a6f16-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a6f16-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6f16-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a6f16-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6f16-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6f16-130">CommonParameters</span></span>
<span data-ttu-id="a6f16-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6f16-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6f16-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6f16-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6f16-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a6f16-133">INPUTS</span></span>

### <span data-ttu-id="a6f16-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6f16-134">System.String</span></span>

### <span data-ttu-id="a6f16-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6f16-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a6f16-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a6f16-136">OUTPUTS</span></span>

### <span data-ttu-id="a6f16-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="a6f16-137">System.Void</span></span>

## <span data-ttu-id="a6f16-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a6f16-138">NOTES</span></span>
* <span data-ttu-id="a6f16-139">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="a6f16-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a6f16-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a6f16-140">RELATED LINKS</span></span>

[<span data-ttu-id="a6f16-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6f16-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="a6f16-142">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="a6f16-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


