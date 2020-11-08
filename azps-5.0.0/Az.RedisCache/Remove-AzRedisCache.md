---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269788"
---
# <span data-ttu-id="c2b29-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2b29-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="c2b29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2b29-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b29-103">Tar bort en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="c2b29-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="c2b29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2b29-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2b29-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2b29-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b29-106">Cmdleten **Remove-AzRedisCache** tar bort en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="c2b29-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="c2b29-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2b29-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b29-108">Exempel 1: ta bort en Redis cache och returnera resultatet</span><span class="sxs-lookup"><span data-stu-id="c2b29-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="c2b29-109">Det här kommandot tar bort en Redis cache och visar om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="c2b29-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="c2b29-110">Exempel 2: ta bort en Redis cache och Visa inte resultatet</span><span class="sxs-lookup"><span data-stu-id="c2b29-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="c2b29-111">Det här kommandot tar bort en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="c2b29-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="c2b29-112">Eftersom parametern *Passthru* inte anges visas inte resultatet av åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c2b29-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="c2b29-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2b29-113">PARAMETERS</span></span>

### <span data-ttu-id="c2b29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b29-114">-DefaultProfile</span></span>
<span data-ttu-id="c2b29-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2b29-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b29-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c2b29-116">-Force</span></span>
<span data-ttu-id="c2b29-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c2b29-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2b29-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="c2b29-118">-Name</span></span>
<span data-ttu-id="c2b29-119">Anger namnet på Redis cache som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c2b29-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="c2b29-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2b29-120">-PassThru</span></span>
<span data-ttu-id="c2b29-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c2b29-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c2b29-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c2b29-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c2b29-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2b29-123">-ResourceGroupName</span></span>
<span data-ttu-id="c2b29-124">Anger namnet på den resurs grupp som innehåller Redis-cachen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="c2b29-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2b29-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2b29-125">-Confirm</span></span>
<span data-ttu-id="c2b29-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2b29-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2b29-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2b29-127">-WhatIf</span></span>
<span data-ttu-id="c2b29-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2b29-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2b29-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2b29-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2b29-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b29-130">CommonParameters</span></span>
<span data-ttu-id="c2b29-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2b29-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b29-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2b29-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b29-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2b29-133">INPUTS</span></span>

### <span data-ttu-id="c2b29-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c2b29-134">System.String</span></span>

## <span data-ttu-id="c2b29-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2b29-135">OUTPUTS</span></span>

### <span data-ttu-id="c2b29-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2b29-136">System.Boolean</span></span>

## <span data-ttu-id="c2b29-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2b29-137">NOTES</span></span>

## <span data-ttu-id="c2b29-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2b29-138">RELATED LINKS</span></span>

[<span data-ttu-id="c2b29-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2b29-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="c2b29-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2b29-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="c2b29-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="c2b29-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


