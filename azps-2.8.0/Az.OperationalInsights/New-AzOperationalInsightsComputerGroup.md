---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsComputerGroup.md
ms.openlocfilehash: d1a1633303e30fc10c5eee7432101fa075f4d38f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919621"
---
# <span data-ttu-id="99de5-101">New-AzOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="99de5-101">New-AzOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="99de5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99de5-102">SYNOPSIS</span></span>
<span data-ttu-id="99de5-103">Skapar en dator grupp.</span><span class="sxs-lookup"><span data-stu-id="99de5-103">Creates a computer group.</span></span>

## <span data-ttu-id="99de5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99de5-104">SYNTAX</span></span>

```
New-AzOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99de5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99de5-105">DESCRIPTION</span></span>
<span data-ttu-id="99de5-106">Cmdleten **New-AzOperationalInsightsComputerGroup** skapar en dator grupp i en resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="99de5-106">The **New-AzOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="99de5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99de5-107">EXAMPLES</span></span>

## <span data-ttu-id="99de5-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99de5-108">PARAMETERS</span></span>

### <span data-ttu-id="99de5-109">-Kategori</span><span class="sxs-lookup"><span data-stu-id="99de5-109">-Category</span></span>
<span data-ttu-id="99de5-110">Anger kategorin för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="99de5-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="99de5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99de5-111">-DefaultProfile</span></span>
<span data-ttu-id="99de5-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="99de5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99de5-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="99de5-113">-DisplayName</span></span>
<span data-ttu-id="99de5-114">Anger visnings namnet för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="99de5-114">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="99de5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="99de5-115">-Force</span></span>
<span data-ttu-id="99de5-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="99de5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="99de5-117">-Fråga</span><span class="sxs-lookup"><span data-stu-id="99de5-117">-Query</span></span>
<span data-ttu-id="99de5-118">Anger frågan för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="99de5-118">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="99de5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99de5-119">-ResourceGroupName</span></span>
<span data-ttu-id="99de5-120">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="99de5-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="99de5-121">Cmdleten skapar dator gruppen i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="99de5-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="99de5-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="99de5-122">-SavedSearchId</span></span>
<span data-ttu-id="99de5-123">Anger ID för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="99de5-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="99de5-124">-Version</span><span class="sxs-lookup"><span data-stu-id="99de5-124">-Version</span></span>
<span data-ttu-id="99de5-125">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="99de5-125">Specifies the version.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99de5-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99de5-126">-WorkspaceName</span></span>
<span data-ttu-id="99de5-127">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="99de5-127">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="99de5-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="99de5-128">-Confirm</span></span>
<span data-ttu-id="99de5-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="99de5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99de5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99de5-130">-WhatIf</span></span>
<span data-ttu-id="99de5-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="99de5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99de5-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="99de5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99de5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99de5-133">CommonParameters</span></span>
<span data-ttu-id="99de5-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99de5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99de5-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99de5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99de5-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99de5-136">INPUTS</span></span>

### <span data-ttu-id="99de5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="99de5-137">System.String</span></span>

### <span data-ttu-id="99de5-138">System. Int64</span><span class="sxs-lookup"><span data-stu-id="99de5-138">System.Int64</span></span>

## <span data-ttu-id="99de5-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99de5-139">OUTPUTS</span></span>

### <span data-ttu-id="99de5-140">System .net. HttpStatusCode</span><span class="sxs-lookup"><span data-stu-id="99de5-140">System.Net.HttpStatusCode</span></span>

## <span data-ttu-id="99de5-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99de5-141">NOTES</span></span>

## <span data-ttu-id="99de5-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99de5-142">RELATED LINKS</span></span>
