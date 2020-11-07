---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 0ad9af6702af457dbdc1a934c8c9e9dd29fb1162
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917093"
---
# <span data-ttu-id="a776b-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a776b-101">New-AzDataFactory</span></span>

## <span data-ttu-id="a776b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a776b-102">SYNOPSIS</span></span>
<span data-ttu-id="a776b-103">Skapar en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a776b-103">Creates a data factory.</span></span>

## <span data-ttu-id="a776b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a776b-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a776b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a776b-105">DESCRIPTION</span></span>
<span data-ttu-id="a776b-106">Cmdleten **New-AzDataFactory** skapar en data fabrik med angivet resurs grupp namn och plats.</span><span class="sxs-lookup"><span data-stu-id="a776b-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="a776b-107">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="a776b-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="a776b-108">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a776b-108">Create a data factory.</span></span> 
- <span data-ttu-id="a776b-109">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="a776b-109">Create linked services.</span></span> 
- <span data-ttu-id="a776b-110">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="a776b-110">Create datasets.</span></span> 
- <span data-ttu-id="a776b-111">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="a776b-111">Create a pipeline.</span></span>

## <span data-ttu-id="a776b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a776b-112">EXAMPLES</span></span>

### <span data-ttu-id="a776b-113">Exempel 1: skapa en data fabrik</span><span class="sxs-lookup"><span data-stu-id="a776b-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="a776b-114">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen för västkusten.</span><span class="sxs-lookup"><span data-stu-id="a776b-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="a776b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a776b-115">PARAMETERS</span></span>

### <span data-ttu-id="a776b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a776b-116">-DefaultProfile</span></span>
<span data-ttu-id="a776b-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a776b-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a776b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a776b-118">-Force</span></span>
<span data-ttu-id="a776b-119">Anger att denna cmdlet ersätter en befintlig data fabrik utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="a776b-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="a776b-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="a776b-120">-Location</span></span>
<span data-ttu-id="a776b-121">Anger platsen för data fabriken, till exempel västkusten eller öster.</span><span class="sxs-lookup"><span data-stu-id="a776b-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="a776b-122">Endast västkusten stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="a776b-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="a776b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="a776b-123">-Name</span></span>
<span data-ttu-id="a776b-124">Anger namnet på data fabriken som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a776b-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a776b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a776b-125">-ResourceGroupName</span></span>
<span data-ttu-id="a776b-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="a776b-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a776b-127">Denna cmdlet skapar en data fabrik som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="a776b-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a776b-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a776b-128">-Tag</span></span>
<span data-ttu-id="a776b-129">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="a776b-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="a776b-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a776b-130">-Confirm</span></span>
<span data-ttu-id="a776b-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a776b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a776b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a776b-132">-WhatIf</span></span>
<span data-ttu-id="a776b-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a776b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a776b-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a776b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a776b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a776b-135">CommonParameters</span></span>
<span data-ttu-id="a776b-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a776b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a776b-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a776b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a776b-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a776b-138">INPUTS</span></span>

### <span data-ttu-id="a776b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a776b-139">System.String</span></span>

### <span data-ttu-id="a776b-140">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a776b-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a776b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a776b-141">OUTPUTS</span></span>

### <span data-ttu-id="a776b-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a776b-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a776b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a776b-143">NOTES</span></span>
* <span data-ttu-id="a776b-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="a776b-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a776b-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a776b-145">RELATED LINKS</span></span>

[<span data-ttu-id="a776b-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a776b-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="a776b-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a776b-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


