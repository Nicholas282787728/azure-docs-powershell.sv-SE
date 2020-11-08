---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259481"
---
# <span data-ttu-id="f13be-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="f13be-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="f13be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f13be-102">SYNOPSIS</span></span>
<span data-ttu-id="f13be-103">Tar bort en HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="f13be-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="f13be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f13be-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f13be-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f13be-105">DESCRIPTION</span></span>
<span data-ttu-id="f13be-106">Cmdleten **Remove-AzHpcCache** tar bort en Azure HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="f13be-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="f13be-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f13be-107">EXAMPLES</span></span>

### <span data-ttu-id="f13be-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f13be-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="f13be-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f13be-109">PARAMETERS</span></span>

### <span data-ttu-id="f13be-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f13be-110">-AsJob</span></span>
<span data-ttu-id="f13be-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="f13be-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f13be-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13be-112">-DefaultProfile</span></span>
<span data-ttu-id="f13be-113">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f13be-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f13be-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f13be-114">-Force</span></span>
<span data-ttu-id="f13be-115">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="f13be-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="f13be-116">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="f13be-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="f13be-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="f13be-117">-Name</span></span>
<span data-ttu-id="f13be-118">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="f13be-118">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f13be-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f13be-119">-PassThru</span></span>
<span data-ttu-id="f13be-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="f13be-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f13be-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="f13be-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f13be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f13be-122">-ResourceGroupName</span></span>
<span data-ttu-id="f13be-123">Namnet på den resurs grupp under vilket du vill ta bort cacheminnet.</span><span class="sxs-lookup"><span data-stu-id="f13be-123">Name of resource group under which you want to remove cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f13be-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f13be-124">-Confirm</span></span>
<span data-ttu-id="f13be-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f13be-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f13be-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f13be-126">-WhatIf</span></span>
<span data-ttu-id="f13be-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f13be-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f13be-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f13be-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f13be-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13be-129">CommonParameters</span></span>
<span data-ttu-id="f13be-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f13be-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13be-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f13be-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13be-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f13be-132">INPUTS</span></span>

### <span data-ttu-id="f13be-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f13be-133">System.String</span></span>

## <span data-ttu-id="f13be-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f13be-134">OUTPUTS</span></span>

## <span data-ttu-id="f13be-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f13be-135">NOTES</span></span>

## <span data-ttu-id="f13be-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f13be-136">RELATED LINKS</span></span>
