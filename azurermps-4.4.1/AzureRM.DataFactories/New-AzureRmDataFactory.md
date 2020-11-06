---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 13e9a8de97ee19e53c31a76516fef7c9fcfcaedd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573649"
---
# <span data-ttu-id="b7dee-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="b7dee-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="b7dee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7dee-102">SYNOPSIS</span></span>
<span data-ttu-id="b7dee-103">Skapar en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b7dee-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7dee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7dee-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tags] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7dee-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7dee-105">DESCRIPTION</span></span>
<span data-ttu-id="b7dee-106">Cmdleten **New-AzureRmDataFactory** skapar en data fabrik med angivet resurs grupp namn och plats.</span><span class="sxs-lookup"><span data-stu-id="b7dee-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="b7dee-107">Utför dessa operationer i följande ordning:</span><span class="sxs-lookup"><span data-stu-id="b7dee-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="b7dee-108">Skapa en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b7dee-108">Create a data factory.</span></span> 
- <span data-ttu-id="b7dee-109">Skapa länkade tjänster.</span><span class="sxs-lookup"><span data-stu-id="b7dee-109">Create linked services.</span></span> 
- <span data-ttu-id="b7dee-110">Skapa data mängder.</span><span class="sxs-lookup"><span data-stu-id="b7dee-110">Create datasets.</span></span> 
- <span data-ttu-id="b7dee-111">Skapa en rörledning.</span><span class="sxs-lookup"><span data-stu-id="b7dee-111">Create a pipeline.</span></span>

## <span data-ttu-id="b7dee-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7dee-112">EXAMPLES</span></span>

### <span data-ttu-id="b7dee-113">Exempel 1: skapa en data fabrik</span><span class="sxs-lookup"><span data-stu-id="b7dee-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="b7dee-114">Det här kommandot skapar en data fabrik med namnet WikiADF i resurs gruppen med namnet ADF på platsen för västkusten.</span><span class="sxs-lookup"><span data-stu-id="b7dee-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="b7dee-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7dee-115">PARAMETERS</span></span>

### <span data-ttu-id="b7dee-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b7dee-116">-Force</span></span>
<span data-ttu-id="b7dee-117">Anger att denna cmdlet ersätter en befintlig data fabrik utan att du behöver bekräfta.</span><span class="sxs-lookup"><span data-stu-id="b7dee-117">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b7dee-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="b7dee-118">-Location</span></span>
<span data-ttu-id="b7dee-119">Anger platsen för data fabriken, till exempel västkusten eller öster.</span><span class="sxs-lookup"><span data-stu-id="b7dee-119">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="b7dee-120">Endast västkusten stöds för närvarande.</span><span class="sxs-lookup"><span data-stu-id="b7dee-120">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="b7dee-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7dee-121">-Name</span></span>
<span data-ttu-id="b7dee-122">Anger namnet på data fabriken som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b7dee-122">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="b7dee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7dee-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7dee-124">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="b7dee-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b7dee-125">Denna cmdlet skapar en data fabrik som tillhör den grupp som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b7dee-125">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b7dee-126">-Taggar</span><span class="sxs-lookup"><span data-stu-id="b7dee-126">-Tags</span></span>
<span data-ttu-id="b7dee-127">Anger taggar för data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b7dee-127">Specifies tags for the data factory.</span></span>

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

### <span data-ttu-id="b7dee-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7dee-128">-Confirm</span></span>
<span data-ttu-id="b7dee-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7dee-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7dee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7dee-130">-WhatIf</span></span>
<span data-ttu-id="b7dee-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7dee-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7dee-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7dee-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7dee-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7dee-133">-DefaultProfile</span></span>
<span data-ttu-id="b7dee-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7dee-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7dee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7dee-135">CommonParameters</span></span>
<span data-ttu-id="b7dee-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7dee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7dee-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7dee-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7dee-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7dee-138">INPUTS</span></span>

## <span data-ttu-id="b7dee-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7dee-139">OUTPUTS</span></span>

### <span data-ttu-id="b7dee-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b7dee-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="b7dee-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7dee-141">NOTES</span></span>
* <span data-ttu-id="b7dee-142">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer</span><span class="sxs-lookup"><span data-stu-id="b7dee-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b7dee-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7dee-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7dee-144">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="b7dee-144">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="b7dee-145">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="b7dee-145">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


