---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 60c1db3595c3ca33676fbd874356376981a72407
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575166"
---
# <span data-ttu-id="131c4-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="131c4-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="131c4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="131c4-102">SYNOPSIS</span></span>
<span data-ttu-id="131c4-103">Skapar en dator grupp.</span><span class="sxs-lookup"><span data-stu-id="131c4-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="131c4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="131c4-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="131c4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="131c4-105">DESCRIPTION</span></span>
<span data-ttu-id="131c4-106">Cmdleten **New-AzureRmOperationalInsightsComputerGroup** skapar en dator grupp i en resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="131c4-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="131c4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="131c4-107">EXAMPLES</span></span>

## <span data-ttu-id="131c4-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="131c4-108">PARAMETERS</span></span>

### <span data-ttu-id="131c4-109">-Kategori</span><span class="sxs-lookup"><span data-stu-id="131c4-109">-Category</span></span>
<span data-ttu-id="131c4-110">Anger kategorin för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="131c4-110">Specifies the category of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="131c4-111">-DefaultProfile</span></span>
<span data-ttu-id="131c4-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="131c4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="131c4-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="131c4-113">-DisplayName</span></span>
<span data-ttu-id="131c4-114">Anger visnings namnet för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="131c4-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="131c4-115">-Force</span></span>
<span data-ttu-id="131c4-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="131c4-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="131c4-117">-Fråga</span><span class="sxs-lookup"><span data-stu-id="131c4-117">-Query</span></span>
<span data-ttu-id="131c4-118">Anger frågan för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="131c4-118">Specifies the query of the computer group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="131c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="131c4-120">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="131c4-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="131c4-121">Cmdleten skapar dator gruppen i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="131c4-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="131c4-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="131c4-122">-SavedSearchId</span></span>
<span data-ttu-id="131c4-123">Anger ID för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="131c4-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="131c4-124">-Version</span><span class="sxs-lookup"><span data-stu-id="131c4-124">-Version</span></span>
<span data-ttu-id="131c4-125">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="131c4-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c4-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="131c4-126">-WorkspaceName</span></span>
<span data-ttu-id="131c4-127">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="131c4-127">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="131c4-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="131c4-128">-Confirm</span></span>
<span data-ttu-id="131c4-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="131c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="131c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="131c4-130">-WhatIf</span></span>
<span data-ttu-id="131c4-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="131c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="131c4-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="131c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="131c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="131c4-133">CommonParameters</span></span>
<span data-ttu-id="131c4-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="131c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="131c4-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="131c4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="131c4-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="131c4-136">INPUTS</span></span>

### <span data-ttu-id="131c4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="131c4-137">System.String</span></span>

### <span data-ttu-id="131c4-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="131c4-138">System.Int64</span></span>

## <span data-ttu-id="131c4-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="131c4-139">OUTPUTS</span></span>

### <span data-ttu-id="131c4-140">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="131c4-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="131c4-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="131c4-141">NOTES</span></span>

## <span data-ttu-id="131c4-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="131c4-142">RELATED LINKS</span></span>
