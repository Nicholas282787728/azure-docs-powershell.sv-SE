---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390255"
---
# <span data-ttu-id="7fe59-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="7fe59-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="7fe59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fe59-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe59-103">Uppdaterar Taggar i en HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="7fe59-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="7fe59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fe59-104">SYNTAX</span></span>

### <span data-ttu-id="7fe59-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7fe59-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fe59-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fe59-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fe59-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fe59-107">DESCRIPTION</span></span>
<span data-ttu-id="7fe59-108">Cmdleten **set-AzHpcCache** uppdaterar en Azure HPC-märkning.</span><span class="sxs-lookup"><span data-stu-id="7fe59-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="7fe59-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fe59-109">EXAMPLES</span></span>

### <span data-ttu-id="7fe59-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7fe59-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="7fe59-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fe59-111">PARAMETERS</span></span>

### <span data-ttu-id="7fe59-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fe59-112">-AsJob</span></span>
<span data-ttu-id="7fe59-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="7fe59-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fe59-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe59-114">-DefaultProfile</span></span>
<span data-ttu-id="7fe59-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe59-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fe59-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fe59-116">-InputObject</span></span>
<span data-ttu-id="7fe59-117">Cacheobjektet att uppdatera.</span><span class="sxs-lookup"><span data-stu-id="7fe59-117">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe59-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7fe59-118">-Name</span></span>
<span data-ttu-id="7fe59-119">Cacheminnets namn.</span><span class="sxs-lookup"><span data-stu-id="7fe59-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe59-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fe59-120">-ResourceGroupName</span></span>
<span data-ttu-id="7fe59-121">Namnet på den resurs grupp som du vill uppdatera cache under.</span><span class="sxs-lookup"><span data-stu-id="7fe59-121">Name of resource group under which you want to update cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe59-122">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7fe59-122">-Tag</span></span>
<span data-ttu-id="7fe59-123">De taggar som ska associeras med HPC-cache.</span><span class="sxs-lookup"><span data-stu-id="7fe59-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe59-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fe59-124">-Confirm</span></span>
<span data-ttu-id="7fe59-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fe59-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fe59-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fe59-126">-WhatIf</span></span>
<span data-ttu-id="7fe59-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fe59-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fe59-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fe59-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fe59-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe59-129">CommonParameters</span></span>
<span data-ttu-id="7fe59-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fe59-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe59-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fe59-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe59-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fe59-132">INPUTS</span></span>

### <span data-ttu-id="7fe59-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7fe59-133">System.String</span></span>

### <span data-ttu-id="7fe59-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7fe59-134">System.Int32</span></span>

## <span data-ttu-id="7fe59-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fe59-135">OUTPUTS</span></span>

### <span data-ttu-id="7fe59-136">Microsoft. Azure. PowerShell. cmdletar. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="7fe59-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="7fe59-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fe59-137">NOTES</span></span>

## <span data-ttu-id="7fe59-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fe59-138">RELATED LINKS</span></span>
