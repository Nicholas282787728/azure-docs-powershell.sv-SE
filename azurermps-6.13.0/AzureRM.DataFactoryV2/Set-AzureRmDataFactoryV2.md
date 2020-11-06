---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: c50023cefbae9a9ba341eba22f40a421c37d12c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577066"
---
# <span data-ttu-id="2e89a-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2e89a-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="2e89a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e89a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e89a-103">Skapar en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2e89a-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e89a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e89a-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e89a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e89a-105">DESCRIPTION</span></span>
<span data-ttu-id="2e89a-106">Cmdleten **set-AzureRmDataFactoryV2** skapar en data fabrik med angivet resurs grupp namn och plats.</span><span class="sxs-lookup"><span data-stu-id="2e89a-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="2e89a-107">Utför de här operationerna i följande ordning:--skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="2e89a-107">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="2e89a-108">--Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="2e89a-108">-- Create linked services.</span></span>
<span data-ttu-id="2e89a-109">--Skapa data uppsättningar.</span><span class="sxs-lookup"><span data-stu-id="2e89a-109">-- Create datasets.</span></span>
<span data-ttu-id="2e89a-110">--Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="2e89a-110">-- Create a pipeline.</span></span>

## <span data-ttu-id="2e89a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e89a-111">EXAMPLES</span></span>

### <span data-ttu-id="2e89a-112">Exempel 1: skapa en data fabrik</span><span class="sxs-lookup"><span data-stu-id="2e89a-112">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="2e89a-113">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen för västkusten.</span><span class="sxs-lookup"><span data-stu-id="2e89a-113">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="2e89a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e89a-114">PARAMETERS</span></span>

### <span data-ttu-id="2e89a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e89a-115">-DefaultProfile</span></span>
<span data-ttu-id="2e89a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e89a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e89a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e89a-117">-Force</span></span>
<span data-ttu-id="2e89a-118">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="2e89a-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2e89a-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="2e89a-119">-Location</span></span>
<span data-ttu-id="2e89a-120">Data fabriken skapas i det här området.</span><span class="sxs-lookup"><span data-stu-id="2e89a-120">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89a-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e89a-121">-Name</span></span>
<span data-ttu-id="2e89a-122">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="2e89a-122">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e89a-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e89a-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="2e89a-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89a-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="2e89a-125">-Tag</span></span>
<span data-ttu-id="2e89a-126">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="2e89a-126">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e89a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2e89a-127">-Confirm</span></span>
<span data-ttu-id="2e89a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e89a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e89a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e89a-129">-WhatIf</span></span>
<span data-ttu-id="2e89a-130">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2e89a-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2e89a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e89a-131">CommonParameters</span></span>
<span data-ttu-id="2e89a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e89a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e89a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e89a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e89a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e89a-134">INPUTS</span></span>

### <span data-ttu-id="2e89a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2e89a-135">System.String</span></span>

### <span data-ttu-id="2e89a-136">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="2e89a-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e89a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e89a-137">OUTPUTS</span></span>

### <span data-ttu-id="2e89a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2e89a-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2e89a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e89a-139">NOTES</span></span>
<span data-ttu-id="2e89a-140">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="2e89a-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2e89a-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e89a-141">RELATED LINKS</span></span>

[<span data-ttu-id="2e89a-142">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2e89a-142">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="2e89a-143">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2e89a-143">Remove-AzureRmDataFactoryV2</span></span>]()
