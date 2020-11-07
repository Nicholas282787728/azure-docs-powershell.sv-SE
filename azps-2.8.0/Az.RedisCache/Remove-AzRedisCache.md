---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 1e9895b78bc61155f7cabfc63e6fb5e4cfbcd30d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920144"
---
# <span data-ttu-id="540bd-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bd-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="540bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="540bd-102">SYNOPSIS</span></span>
<span data-ttu-id="540bd-103">Tar bort en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="540bd-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="540bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="540bd-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="540bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="540bd-105">DESCRIPTION</span></span>
<span data-ttu-id="540bd-106">Cmdleten **Remove-AzRedisCache** tar bort en Azure Redis-cache.</span><span class="sxs-lookup"><span data-stu-id="540bd-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="540bd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="540bd-107">EXAMPLES</span></span>

### <span data-ttu-id="540bd-108">Exempel 1: ta bort en Redis cache och returnera resultatet</span><span class="sxs-lookup"><span data-stu-id="540bd-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="540bd-109">Det här kommandot tar bort en Redis cache och visar om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="540bd-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="540bd-110">Exempel 2: ta bort en Redis cache och Visa inte resultatet</span><span class="sxs-lookup"><span data-stu-id="540bd-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="540bd-111">Det här kommandot tar bort en Redis cache.</span><span class="sxs-lookup"><span data-stu-id="540bd-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="540bd-112">Eftersom parametern *Passthru* inte anges visas inte resultatet av åtgärden.</span><span class="sxs-lookup"><span data-stu-id="540bd-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="540bd-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="540bd-113">PARAMETERS</span></span>

### <span data-ttu-id="540bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540bd-114">-DefaultProfile</span></span>
<span data-ttu-id="540bd-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="540bd-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="540bd-116">-Force</span><span class="sxs-lookup"><span data-stu-id="540bd-116">-Force</span></span>
<span data-ttu-id="540bd-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="540bd-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="540bd-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="540bd-118">-Name</span></span>
<span data-ttu-id="540bd-119">Anger namnet på Redis cache som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="540bd-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="540bd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="540bd-120">-PassThru</span></span>
<span data-ttu-id="540bd-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="540bd-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="540bd-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="540bd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="540bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="540bd-124">Anger namnet på den resurs grupp som innehåller Redis-cachen som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="540bd-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="540bd-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="540bd-125">-Confirm</span></span>
<span data-ttu-id="540bd-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="540bd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540bd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540bd-127">-WhatIf</span></span>
<span data-ttu-id="540bd-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="540bd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540bd-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="540bd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540bd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540bd-130">CommonParameters</span></span>
<span data-ttu-id="540bd-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="540bd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540bd-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="540bd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540bd-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="540bd-133">INPUTS</span></span>

### <span data-ttu-id="540bd-134">System. String</span><span class="sxs-lookup"><span data-stu-id="540bd-134">System.String</span></span>

## <span data-ttu-id="540bd-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="540bd-135">OUTPUTS</span></span>

### <span data-ttu-id="540bd-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="540bd-136">System.Boolean</span></span>

## <span data-ttu-id="540bd-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="540bd-137">NOTES</span></span>

## <span data-ttu-id="540bd-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="540bd-138">RELATED LINKS</span></span>

[<span data-ttu-id="540bd-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bd-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="540bd-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bd-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="540bd-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="540bd-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


