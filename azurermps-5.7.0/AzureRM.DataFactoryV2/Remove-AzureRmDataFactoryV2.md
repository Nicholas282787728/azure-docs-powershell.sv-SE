---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 330bcf3622faa515a58ea8f1e087d1383b9f154a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573469"
---
# <span data-ttu-id="ba3da-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ba3da-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="ba3da-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba3da-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3da-103">Tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ba3da-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba3da-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba3da-104">SYNTAX</span></span>

### <span data-ttu-id="ba3da-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="ba3da-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba3da-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ba3da-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba3da-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ba3da-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba3da-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba3da-108">DESCRIPTION</span></span>
<span data-ttu-id="ba3da-109">Remove-AzureRmDataFactoryV2-cmdleten tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="ba3da-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="ba3da-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba3da-110">EXAMPLES</span></span>

### <span data-ttu-id="ba3da-111">Exempel 1: ta bort en data fabrik</span><span class="sxs-lookup"><span data-stu-id="ba3da-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="ba3da-112">Det här kommandot tar bort data fabriken med namnet WikiADF från resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="ba3da-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="ba3da-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="ba3da-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="ba3da-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba3da-114">PARAMETERS</span></span>

### <span data-ttu-id="ba3da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3da-115">-DefaultProfile</span></span>
<span data-ttu-id="ba3da-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba3da-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ba3da-117">-Force</span></span>
<span data-ttu-id="ba3da-118">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ba3da-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ba3da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba3da-119">-InputObject</span></span>
<span data-ttu-id="ba3da-120">Anger det DataFactory-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ba3da-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba3da-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba3da-121">-Name</span></span>
<span data-ttu-id="ba3da-122">Anger namnet på data fabriken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="ba3da-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba3da-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba3da-124">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="ba3da-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ba3da-125">Denna cmdlet tar bort en data fabrik från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="ba3da-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3da-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba3da-126">-ResourceId</span></span>
<span data-ttu-id="ba3da-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="ba3da-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ba3da-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba3da-128">-Confirm</span></span>
<span data-ttu-id="ba3da-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba3da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba3da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba3da-130">-WhatIf</span></span>
<span data-ttu-id="ba3da-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba3da-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ba3da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3da-132">CommonParameters</span></span>
<span data-ttu-id="ba3da-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3da-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba3da-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3da-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba3da-135">INPUTS</span></span>

### <span data-ttu-id="ba3da-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ba3da-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="ba3da-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ba3da-137">System.String</span></span>

## <span data-ttu-id="ba3da-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba3da-138">OUTPUTS</span></span>

### <span data-ttu-id="ba3da-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="ba3da-139">System.Object</span></span>

## <span data-ttu-id="ba3da-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba3da-140">NOTES</span></span>
<span data-ttu-id="ba3da-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="ba3da-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ba3da-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba3da-142">RELATED LINKS</span></span>

[<span data-ttu-id="ba3da-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ba3da-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="ba3da-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ba3da-144">Set-AzureRmDataFactoryV2</span></span>]()
