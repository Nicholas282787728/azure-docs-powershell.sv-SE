---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261400"
---
# <span data-ttu-id="3ad82-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3ad82-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="3ad82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3ad82-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad82-103">Tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3ad82-103">Removes a data factory.</span></span>

## <span data-ttu-id="3ad82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3ad82-104">SYNTAX</span></span>

### <span data-ttu-id="3ad82-105">ByFactoryName (standard)</span><span class="sxs-lookup"><span data-stu-id="3ad82-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ad82-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3ad82-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ad82-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad82-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ad82-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3ad82-108">DESCRIPTION</span></span>
<span data-ttu-id="3ad82-109">Remove-AzDataFactoryV2-cmdleten tar bort en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="3ad82-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="3ad82-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3ad82-110">EXAMPLES</span></span>

### <span data-ttu-id="3ad82-111">Exempel 1: ta bort en data fabrik</span><span class="sxs-lookup"><span data-stu-id="3ad82-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="3ad82-112">Det här kommandot tar bort data fabriken med namnet WikiADF från resurs gruppen med namnet ADF.</span><span class="sxs-lookup"><span data-stu-id="3ad82-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="3ad82-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="3ad82-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="3ad82-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3ad82-114">PARAMETERS</span></span>

### <span data-ttu-id="3ad82-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad82-115">-DefaultProfile</span></span>
<span data-ttu-id="3ad82-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad82-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ad82-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3ad82-117">-Force</span></span>
<span data-ttu-id="3ad82-118">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3ad82-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3ad82-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ad82-119">-InputObject</span></span>
<span data-ttu-id="3ad82-120">Anger det DataFactory-objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3ad82-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="3ad82-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="3ad82-121">-Name</span></span>
<span data-ttu-id="3ad82-122">Anger namnet på data fabriken som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="3ad82-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="3ad82-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad82-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ad82-124">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="3ad82-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="3ad82-125">Denna cmdlet tar bort en data fabrik från den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3ad82-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3ad82-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ad82-126">-ResourceId</span></span>
<span data-ttu-id="3ad82-127">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="3ad82-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3ad82-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3ad82-128">-Confirm</span></span>
<span data-ttu-id="3ad82-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ad82-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad82-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad82-130">-WhatIf</span></span>
<span data-ttu-id="3ad82-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3ad82-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3ad82-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad82-132">CommonParameters</span></span>
<span data-ttu-id="3ad82-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad82-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad82-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ad82-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad82-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3ad82-135">INPUTS</span></span>

### <span data-ttu-id="3ad82-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3ad82-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="3ad82-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3ad82-137">System.String</span></span>

## <span data-ttu-id="3ad82-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3ad82-138">OUTPUTS</span></span>

### <span data-ttu-id="3ad82-139">System. Void</span><span class="sxs-lookup"><span data-stu-id="3ad82-139">System.Void</span></span>

## <span data-ttu-id="3ad82-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3ad82-140">NOTES</span></span>
<span data-ttu-id="3ad82-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="3ad82-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3ad82-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3ad82-142">RELATED LINKS</span></span>

[<span data-ttu-id="3ad82-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3ad82-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="3ad82-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="3ad82-144">Set-AzDataFactoryV2</span></span>]()