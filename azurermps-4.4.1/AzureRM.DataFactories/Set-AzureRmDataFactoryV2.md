---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2.md
ms.openlocfilehash: b5e5d42ba114da87daa3fa3effb15d3ad8bab22c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573637"
---
# <span data-ttu-id="1b931-101">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1b931-101">Set-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="1b931-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b931-102">SYNOPSIS</span></span>
<span data-ttu-id="1b931-103">Skapar en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="1b931-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b931-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b931-104">SYNTAX</span></span>

```
Set-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b931-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b931-105">DESCRIPTION</span></span>
<span data-ttu-id="1b931-106">Cmdleten **set-AzureRmDataFactoryV2** skapar en data fabrik med angivet resurs grupp namn och plats.</span><span class="sxs-lookup"><span data-stu-id="1b931-106">The **Set-AzureRmDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="1b931-107">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="1b931-107">Perform these operations in the following order:</span></span>

        -- Create a data factory.
        -- Create linked services.
        -- Create datasets.
        -- Create a pipeline.

## <span data-ttu-id="1b931-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b931-108">EXAMPLES</span></span>

### <span data-ttu-id="1b931-109">Exempel 1: skapa en data fabrik</span><span class="sxs-lookup"><span data-stu-id="1b931-109">Example 1: Create a data factory</span></span>
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

<span data-ttu-id="1b931-110">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen för västkusten.</span><span class="sxs-lookup"><span data-stu-id="1b931-110">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="1b931-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b931-111">PARAMETERS</span></span>

### <span data-ttu-id="1b931-112">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b931-112">-Confirm</span></span>
<span data-ttu-id="1b931-113">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b931-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b931-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1b931-114">-Force</span></span>
<span data-ttu-id="1b931-115">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="1b931-115">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="1b931-116">-Plats</span><span class="sxs-lookup"><span data-stu-id="1b931-116">-Location</span></span>
<span data-ttu-id="1b931-117">Data fabriken skapas i det här området.</span><span class="sxs-lookup"><span data-stu-id="1b931-117">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="1b931-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b931-118">-Name</span></span>
<span data-ttu-id="1b931-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1b931-119">The data factory name.</span></span>

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

### <span data-ttu-id="1b931-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b931-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b931-121">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="1b931-121">The resource group name.</span></span>

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

### <span data-ttu-id="1b931-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="1b931-122">-Tag</span></span>
<span data-ttu-id="1b931-123">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="1b931-123">The tags of the data factory.</span></span>

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

### <span data-ttu-id="1b931-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b931-124">-WhatIf</span></span>
<span data-ttu-id="1b931-125">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b931-125">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="1b931-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b931-126">-DefaultProfile</span></span>
<span data-ttu-id="1b931-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b931-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b931-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b931-128">CommonParameters</span></span>
<span data-ttu-id="1b931-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b931-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b931-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b931-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b931-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b931-131">INPUTS</span></span>

### <span data-ttu-id="1b931-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1b931-132">System.String</span></span>
<span data-ttu-id="1b931-133">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="1b931-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1b931-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b931-134">OUTPUTS</span></span>

### <span data-ttu-id="1b931-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1b931-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1b931-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b931-136">NOTES</span></span>
<span data-ttu-id="1b931-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="1b931-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1b931-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b931-138">RELATED LINKS</span></span>

[<span data-ttu-id="1b931-139">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1b931-139">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="1b931-140">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="1b931-140">Remove-AzureRmDataFactoryV2</span></span>]()
