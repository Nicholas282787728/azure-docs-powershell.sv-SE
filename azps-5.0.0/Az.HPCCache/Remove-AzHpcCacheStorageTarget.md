---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271037"
---
# <span data-ttu-id="d77eb-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="d77eb-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="d77eb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d77eb-102">SYNOPSIS</span></span>
<span data-ttu-id="d77eb-103">Tar bort ett lagrings mål.</span><span class="sxs-lookup"><span data-stu-id="d77eb-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="d77eb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d77eb-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d77eb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d77eb-105">DESCRIPTION</span></span>
<span data-ttu-id="d77eb-106">Cmdleten **Remove-AzHpcCacheStorageTarget** tar bort ett lagrings mål från Azure HPC-cachen.</span><span class="sxs-lookup"><span data-stu-id="d77eb-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="d77eb-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d77eb-107">EXAMPLES</span></span>

### <span data-ttu-id="d77eb-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d77eb-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="d77eb-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d77eb-109">PARAMETERS</span></span>

### <span data-ttu-id="d77eb-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d77eb-110">-AsJob</span></span>
<span data-ttu-id="d77eb-111">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d77eb-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d77eb-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="d77eb-112">-CacheName</span></span>
<span data-ttu-id="d77eb-113">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="d77eb-113">Name of cache.</span></span>

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

### <span data-ttu-id="d77eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d77eb-114">-DefaultProfile</span></span>
<span data-ttu-id="d77eb-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d77eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d77eb-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d77eb-116">-Force</span></span>
<span data-ttu-id="d77eb-117">Anger att cmdleten inte ber dig bekräfta.</span><span class="sxs-lookup"><span data-stu-id="d77eb-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="d77eb-118">Denna cmdlet uppmanar dig som standard att bekräfta att du vill ta bort lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="d77eb-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="d77eb-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="d77eb-119">-Name</span></span>
<span data-ttu-id="d77eb-120">Namn på lagrings målet.</span><span class="sxs-lookup"><span data-stu-id="d77eb-120">Name of storage target.</span></span>

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

### <span data-ttu-id="d77eb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d77eb-121">-PassThru</span></span>
<span data-ttu-id="d77eb-122">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d77eb-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d77eb-123">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d77eb-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d77eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d77eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="d77eb-125">Namnet på den resurs grupp under vilket du vill ta bort lagrings målet från cachen.</span><span class="sxs-lookup"><span data-stu-id="d77eb-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="d77eb-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d77eb-126">-Confirm</span></span>
<span data-ttu-id="d77eb-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d77eb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d77eb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d77eb-128">-WhatIf</span></span>
<span data-ttu-id="d77eb-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d77eb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d77eb-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d77eb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d77eb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d77eb-131">CommonParameters</span></span>
<span data-ttu-id="d77eb-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d77eb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d77eb-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d77eb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d77eb-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d77eb-134">INPUTS</span></span>

### <span data-ttu-id="d77eb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d77eb-135">System.String</span></span>

## <span data-ttu-id="d77eb-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d77eb-136">OUTPUTS</span></span>

## <span data-ttu-id="d77eb-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d77eb-137">NOTES</span></span>

## <span data-ttu-id="d77eb-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d77eb-138">RELATED LINKS</span></span>
