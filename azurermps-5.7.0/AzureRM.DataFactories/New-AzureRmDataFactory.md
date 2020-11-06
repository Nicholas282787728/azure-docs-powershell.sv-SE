---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 8adaa00b08615bb687cbd481584875e9c91e7da3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578251"
---
# <span data-ttu-id="f58d5-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="f58d5-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="f58d5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f58d5-102">SYNOPSIS</span></span>
<span data-ttu-id="f58d5-103">Skapar en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f58d5-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f58d5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f58d5-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f58d5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f58d5-105">DESCRIPTION</span></span>
<span data-ttu-id="f58d5-106">Cmdleten **New-AzureRmDataFactory** skapar en data fabrik med angivet resurs grupp namn och plats.</span><span class="sxs-lookup"><span data-stu-id="f58d5-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="f58d5-107">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="f58d5-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="f58d5-108">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="f58d5-108">Create a data factory.</span></span> 
- <span data-ttu-id="f58d5-109">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="f58d5-109">Create linked services.</span></span> 
- <span data-ttu-id="f58d5-110">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="f58d5-110">Create datasets.</span></span> 
- <span data-ttu-id="f58d5-111">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="f58d5-111">Create a pipeline.</span></span>

## <span data-ttu-id="f58d5-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f58d5-112">EXAMPLES</span></span>

### <span data-ttu-id="f58d5-113">Exempel 1: skapa en data fabrik</span><span class="sxs-lookup"><span data-stu-id="f58d5-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="f58d5-114">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen för västkusten.</span><span class="sxs-lookup"><span data-stu-id="f58d5-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="f58d5-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f58d5-115">PARAMETERS</span></span>

### <span data-ttu-id="f58d5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58d5-116">-DefaultProfile</span></span>
<span data-ttu-id="f58d5-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f58d5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f58d5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f58d5-118">-Force</span></span>
<span data-ttu-id="f58d5-119">Anger att denna cmdlet ersätter en befintlig data fabrik utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f58d5-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f58d5-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="f58d5-120">-Location</span></span>
<span data-ttu-id="f58d5-121">Anger platsen för data fabriken, till exempel västkusten eller öster.</span><span class="sxs-lookup"><span data-stu-id="f58d5-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="f58d5-122">Endast västkusten stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="f58d5-122">Only WestUS is currently supported.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58d5-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="f58d5-123">-Name</span></span>
<span data-ttu-id="f58d5-124">Anger namnet på data fabriken som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="f58d5-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58d5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f58d5-125">-ResourceGroupName</span></span>
<span data-ttu-id="f58d5-126">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="f58d5-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f58d5-127">Denna cmdlet skapar en data fabrik som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="f58d5-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58d5-128">-Tagg</span><span class="sxs-lookup"><span data-stu-id="f58d5-128">-Tag</span></span>
<span data-ttu-id="f58d5-129">Taggarna för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="f58d5-129">The tags of the data factory.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58d5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f58d5-130">-Confirm</span></span>
<span data-ttu-id="f58d5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f58d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f58d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f58d5-132">-WhatIf</span></span>
<span data-ttu-id="f58d5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f58d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f58d5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f58d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f58d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58d5-135">CommonParameters</span></span>
<span data-ttu-id="f58d5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f58d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58d5-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f58d5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58d5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f58d5-138">INPUTS</span></span>

### <span data-ttu-id="f58d5-139">Ingen</span><span class="sxs-lookup"><span data-stu-id="f58d5-139">None</span></span>
<span data-ttu-id="f58d5-140">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f58d5-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f58d5-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f58d5-141">OUTPUTS</span></span>

### <span data-ttu-id="f58d5-142">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f58d5-142">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="f58d5-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f58d5-143">NOTES</span></span>
* <span data-ttu-id="f58d5-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="f58d5-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f58d5-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f58d5-145">RELATED LINKS</span></span>

[<span data-ttu-id="f58d5-146">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="f58d5-146">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="f58d5-147">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="f58d5-147">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


