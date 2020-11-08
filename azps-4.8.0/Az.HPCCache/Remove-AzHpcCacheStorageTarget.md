---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261109"
---
# <span data-ttu-id="cdad9-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="cdad9-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="cdad9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdad9-102">SYNOPSIS</span></span>
<span data-ttu-id="cdad9-103">Tar bort ett lagrings mål.</span><span class="sxs-lookup"><span data-stu-id="cdad9-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="cdad9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdad9-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdad9-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdad9-105">DESCRIPTION</span></span>
<span data-ttu-id="cdad9-106">Cmdleten **Remove-AzHpcCacheStorageTarget** tar bort ett lagrings mål från Azure HPC-cachen.</span><span class="sxs-lookup"><span data-stu-id="cdad9-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="cdad9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdad9-107">EXAMPLES</span></span>

### <span data-ttu-id="cdad9-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cdad9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="cdad9-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdad9-109">PARAMETERS</span></span>

### <span data-ttu-id="cdad9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdad9-110">-AsJob</span></span>
<span data-ttu-id="cdad9-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="cdad9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdad9-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="cdad9-112">-CacheName</span></span>
<span data-ttu-id="cdad9-113">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="cdad9-113">Name of cache.</span></span>

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

### <span data-ttu-id="cdad9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdad9-114">-DefaultProfile</span></span>
<span data-ttu-id="cdad9-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cdad9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdad9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cdad9-116">-Force</span></span>
<span data-ttu-id="cdad9-117">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="cdad9-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="cdad9-118">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="cdad9-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="cdad9-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="cdad9-119">-Name</span></span>
<span data-ttu-id="cdad9-120">Namn på lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="cdad9-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdad9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdad9-121">-PassThru</span></span>
<span data-ttu-id="cdad9-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="cdad9-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cdad9-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="cdad9-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cdad9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdad9-124">-ResourceGroupName</span></span>
<span data-ttu-id="cdad9-125">Namnet på den resurs grupp under vilket du vill ta bort lagrings målet från cachen.</span><span class="sxs-lookup"><span data-stu-id="cdad9-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="cdad9-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cdad9-126">-Confirm</span></span>
<span data-ttu-id="cdad9-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cdad9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdad9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdad9-128">-WhatIf</span></span>
<span data-ttu-id="cdad9-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cdad9-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdad9-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cdad9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdad9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdad9-131">CommonParameters</span></span>
<span data-ttu-id="cdad9-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdad9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdad9-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdad9-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdad9-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdad9-134">INPUTS</span></span>

### <span data-ttu-id="cdad9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cdad9-135">System.String</span></span>

## <span data-ttu-id="cdad9-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdad9-136">OUTPUTS</span></span>

## <span data-ttu-id="cdad9-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdad9-137">NOTES</span></span>

## <span data-ttu-id="cdad9-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdad9-138">RELATED LINKS</span></span>
