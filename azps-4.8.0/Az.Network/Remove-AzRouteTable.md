---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259253"
---
# <span data-ttu-id="2fb5b-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fb5b-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="2fb5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2fb5b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb5b-103">Tar bort en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-103">Removes a route table.</span></span>

## <span data-ttu-id="2fb5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2fb5b-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fb5b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2fb5b-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb5b-106">Cmdleten **Remove-AzRouteTable** tar bort en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="2fb5b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2fb5b-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb5b-108">Exempel 1: ta bort en routningstabellen</span><span class="sxs-lookup"><span data-stu-id="2fb5b-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="2fb5b-109">Det här kommandot tar bort routningstabellen med namnet RouteTable01 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="2fb5b-110">Denna cmdlet ber dig bekräfta innan tabellen tas bort.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="2fb5b-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2fb5b-111">PARAMETERS</span></span>

### <span data-ttu-id="2fb5b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fb5b-112">-AsJob</span></span>
<span data-ttu-id="2fb5b-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2fb5b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fb5b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb5b-114">-DefaultProfile</span></span>
<span data-ttu-id="2fb5b-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fb5b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2fb5b-116">-Force</span></span>
<span data-ttu-id="2fb5b-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2fb5b-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="2fb5b-118">-Name</span></span>
<span data-ttu-id="2fb5b-119">Anger namnet på den routningstabell som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-119">Specifies the name of the route table that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb5b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fb5b-120">-PassThru</span></span>
<span data-ttu-id="2fb5b-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2fb5b-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2fb5b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb5b-123">-ResourceGroupName</span></span>
<span data-ttu-id="2fb5b-124">Anger namnet på den resurs grupp som innehåller routningstabellen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2fb5b-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2fb5b-125">-Confirm</span></span>
<span data-ttu-id="2fb5b-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb5b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb5b-127">-WhatIf</span></span>
<span data-ttu-id="2fb5b-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fb5b-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb5b-130">CommonParameters</span></span>
<span data-ttu-id="2fb5b-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb5b-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb5b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb5b-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2fb5b-133">INPUTS</span></span>

### <span data-ttu-id="2fb5b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2fb5b-134">System.String</span></span>

## <span data-ttu-id="2fb5b-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2fb5b-135">OUTPUTS</span></span>

### <span data-ttu-id="2fb5b-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fb5b-136">System.Boolean</span></span>

## <span data-ttu-id="2fb5b-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2fb5b-137">NOTES</span></span>

## <span data-ttu-id="2fb5b-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2fb5b-138">RELATED LINKS</span></span>

[<span data-ttu-id="2fb5b-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fb5b-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="2fb5b-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fb5b-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="2fb5b-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="2fb5b-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


