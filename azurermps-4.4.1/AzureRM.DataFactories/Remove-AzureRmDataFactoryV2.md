---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 9d7d3e3ae06d46b1ea3cb3b1e4e8db1944dc87e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579740"
---
# <span data-ttu-id="84a4b-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="84a4b-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="84a4b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="84a4b-103">Tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="84a4b-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84a4b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84a4b-104">SYNTAX</span></span>

### <span data-ttu-id="84a4b-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="84a4b-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a4b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="84a4b-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84a4b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84a4b-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84a4b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84a4b-108">DESCRIPTION</span></span>
<span data-ttu-id="84a4b-109">Remove-AzureRmDataFactoryV2-cmdleten tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="84a4b-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="84a4b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84a4b-110">EXAMPLES</span></span>

### <span data-ttu-id="84a4b-111">Exempel 1: ta bort en data fabrik</span><span class="sxs-lookup"><span data-stu-id="84a4b-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="84a4b-112">Det här kommandot tar bort data fabriken med namnet WikiADF från resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="84a4b-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="84a4b-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="84a4b-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="84a4b-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84a4b-114">PARAMETERS</span></span>

### <span data-ttu-id="84a4b-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="84a4b-115">-Confirm</span></span>
<span data-ttu-id="84a4b-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84a4b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a4b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84a4b-117">-InputObject</span></span>
<span data-ttu-id="84a4b-118">Anger det DataFactory-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="84a4b-118">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84a4b-119">-Force</span><span class="sxs-lookup"><span data-stu-id="84a4b-119">-Force</span></span>
<span data-ttu-id="84a4b-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="84a4b-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="84a4b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="84a4b-121">-Name</span></span>
<span data-ttu-id="84a4b-122">Anger namnet på data fabriken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="84a4b-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a4b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84a4b-123">-ResourceGroupName</span></span>
<span data-ttu-id="84a4b-124">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="84a4b-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="84a4b-125">Denna cmdlet tar bort en data fabrik från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="84a4b-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84a4b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84a4b-126">-ResourceId</span></span>
<span data-ttu-id="84a4b-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="84a4b-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="84a4b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a4b-128">-WhatIf</span></span>
<span data-ttu-id="84a4b-129">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="84a4b-129">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="84a4b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a4b-130">-DefaultProfile</span></span>
<span data-ttu-id="84a4b-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84a4b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84a4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a4b-132">CommonParameters</span></span>
<span data-ttu-id="84a4b-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a4b-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84a4b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a4b-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84a4b-135">INPUTS</span></span>

### <span data-ttu-id="84a4b-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="84a4b-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="84a4b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="84a4b-137">System.String</span></span>

## <span data-ttu-id="84a4b-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84a4b-138">OUTPUTS</span></span>

### <span data-ttu-id="84a4b-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="84a4b-139">System.Object</span></span>

## <span data-ttu-id="84a4b-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84a4b-140">NOTES</span></span>
<span data-ttu-id="84a4b-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="84a4b-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="84a4b-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84a4b-142">RELATED LINKS</span></span>

[<span data-ttu-id="84a4b-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="84a4b-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="84a4b-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="84a4b-144">Set-AzureRmDataFactoryV2</span></span>]()
