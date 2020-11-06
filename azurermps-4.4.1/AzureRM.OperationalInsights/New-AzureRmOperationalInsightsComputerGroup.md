---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: E68E90B3-0B6A-49E9-83CD-E73826571B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsComputerGroup.md
ms.openlocfilehash: 8a54a735b41ef537a31f5e3e1ce2789d10e60af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577576"
---
# <span data-ttu-id="28731-101">New-AzureRmOperationalInsightsComputerGroup</span><span class="sxs-lookup"><span data-stu-id="28731-101">New-AzureRmOperationalInsightsComputerGroup</span></span>

## <span data-ttu-id="28731-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="28731-102">SYNOPSIS</span></span>
<span data-ttu-id="28731-103">Skapar en dator grupp.</span><span class="sxs-lookup"><span data-stu-id="28731-103">Creates a computer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28731-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="28731-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsComputerGroup [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Version] <Int64>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28731-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="28731-105">DESCRIPTION</span></span>
<span data-ttu-id="28731-106">Cmdleten **New-AzureRmOperationalInsightsComputerGroup** skapar en dator grupp i en resurs grupp och plats.</span><span class="sxs-lookup"><span data-stu-id="28731-106">The **New-AzureRmOperationalInsightsComputerGroup** cmdlet creates a computer group in a resource group and location.</span></span>

## <span data-ttu-id="28731-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="28731-107">EXAMPLES</span></span>

## <span data-ttu-id="28731-108">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="28731-108">PARAMETERS</span></span>

### <span data-ttu-id="28731-109">-Kategori</span><span class="sxs-lookup"><span data-stu-id="28731-109">-Category</span></span>
<span data-ttu-id="28731-110">Anger kategorin för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="28731-110">Specifies the category of the computer group.</span></span>

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

### <span data-ttu-id="28731-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="28731-111">-DisplayName</span></span>
<span data-ttu-id="28731-112">Anger visnings namnet för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="28731-112">Specifies the display name of the computer group.</span></span>

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

### <span data-ttu-id="28731-113">-Force</span><span class="sxs-lookup"><span data-stu-id="28731-113">-Force</span></span>
<span data-ttu-id="28731-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="28731-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28731-115">-Fråga</span><span class="sxs-lookup"><span data-stu-id="28731-115">-Query</span></span>
<span data-ttu-id="28731-116">Anger frågan för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="28731-116">Specifies the query of the computer group.</span></span>

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

### <span data-ttu-id="28731-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28731-117">-ResourceGroupName</span></span>
<span data-ttu-id="28731-118">Anger namnet på en Azure-adressresurs.</span><span class="sxs-lookup"><span data-stu-id="28731-118">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="28731-119">Cmdleten skapar dator gruppen i den här resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="28731-119">The cmdlet creates computer group in this resource group.</span></span>

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

### <span data-ttu-id="28731-120">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="28731-120">-SavedSearchId</span></span>
<span data-ttu-id="28731-121">Anger ID för dator gruppen.</span><span class="sxs-lookup"><span data-stu-id="28731-121">Specifies the ID of the computer group.</span></span>

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

### <span data-ttu-id="28731-122">-Version</span><span class="sxs-lookup"><span data-stu-id="28731-122">-Version</span></span>
<span data-ttu-id="28731-123">Anger versionen.</span><span class="sxs-lookup"><span data-stu-id="28731-123">Specifies the version.</span></span>

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

### <span data-ttu-id="28731-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28731-124">-WorkspaceName</span></span>
<span data-ttu-id="28731-125">Anger namnet på arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="28731-125">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="28731-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="28731-126">-Confirm</span></span>
<span data-ttu-id="28731-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="28731-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28731-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28731-128">-WhatIf</span></span>
<span data-ttu-id="28731-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="28731-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28731-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="28731-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28731-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28731-131">-DefaultProfile</span></span>
<span data-ttu-id="28731-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="28731-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28731-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28731-133">CommonParameters</span></span>
<span data-ttu-id="28731-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28731-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28731-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28731-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28731-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="28731-136">INPUTS</span></span>

## <span data-ttu-id="28731-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="28731-137">OUTPUTS</span></span>

## <span data-ttu-id="28731-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="28731-138">NOTES</span></span>

## <span data-ttu-id="28731-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="28731-139">RELATED LINKS</span></span>

