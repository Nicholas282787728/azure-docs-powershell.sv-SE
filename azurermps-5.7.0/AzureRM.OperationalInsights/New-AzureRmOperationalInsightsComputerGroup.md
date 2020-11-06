---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightscomputergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 999e9e5fd9f0b93e71b222f228b1575e0492073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583612"
---
# <span data-ttu-id="a0403-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="a0403-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="a0403-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a0403-102">SYNOPSIS</span></span>
<span data-ttu-id="a0403-103">Skapar en dator grupp.</span><span class="sxs-lookup"><span data-stu-id="a0403-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0403-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a0403-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0403-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a0403-105">DESCRIPTION</span></span>
<span data-ttu-id="a0403-106">Cmdleten **New-AzureRmOperationalInsightsComputerGroup** skapar en dator grupp i en resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="a0403-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="a0403-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a0403-107">EXAMPLES</span></span>

## <span data-ttu-id="a0403-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a0403-108">PARAMETERS</span></span>

### <span data-ttu-id="a0403-109">-Kategori</span><span class="sxs-lookup"><span data-stu-id="a0403-109">-Category</span></span>
<span data-ttu-id="a0403-110">Anger kategorin för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0403-110">Specifies the category of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0403-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0403-111">-DefaultProfile</span></span>
<span data-ttu-id="a0403-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a0403-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0403-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a0403-113">-DisplayName</span></span>
<span data-ttu-id="a0403-114">Anger visnings namnet för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0403-114">Specifies the display name of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0403-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a0403-115">-Force</span></span>
<span data-ttu-id="a0403-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="a0403-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a0403-117">-Fråga</span><span class="sxs-lookup"><span data-stu-id="a0403-117">-Query</span></span>
<span data-ttu-id="a0403-118">Anger frågan för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0403-118">Specifies the query of the computer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0403-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0403-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0403-120">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="a0403-120">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a0403-121">Cmdleten skapar dator gruppen i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0403-121">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="a0403-122">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="a0403-122">-SavedSearchId</span></span>
<span data-ttu-id="a0403-123">Anger ID för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="a0403-123">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="a0403-124">-Version</span><span class="sxs-lookup"><span data-stu-id="a0403-124">-Version</span></span>
<span data-ttu-id="a0403-125">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="a0403-125">Specifies the version.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0403-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a0403-126">-WorkspaceName</span></span>
<span data-ttu-id="a0403-127">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="a0403-127">Specifies the name of the workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0403-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a0403-128">-Confirm</span></span>
<span data-ttu-id="a0403-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a0403-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0403-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0403-130">-WhatIf</span></span>
<span data-ttu-id="a0403-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a0403-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0403-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a0403-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0403-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0403-133">CommonParameters</span></span>
<span data-ttu-id="a0403-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0403-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0403-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0403-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0403-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a0403-136">INPUTS</span></span>

### <span data-ttu-id="a0403-137">Ingen</span><span class="sxs-lookup"><span data-stu-id="a0403-137">None</span></span>
<span data-ttu-id="a0403-138">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="a0403-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a0403-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a0403-139">OUTPUTS</span></span>

## <span data-ttu-id="a0403-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a0403-140">NOTES</span></span>

## <span data-ttu-id="a0403-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a0403-141">RELATED LINKS</span></span>

