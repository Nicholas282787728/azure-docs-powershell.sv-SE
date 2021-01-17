---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: 8c899d975669404045aa40bee45ad287a26f8749
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413808"
---
# <span data-ttu-id="e1832-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1832-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="e1832-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1832-102">SYNOPSIS</span></span>
<span data-ttu-id="e1832-103">Tar bort en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="e1832-103">Removes a route table.</span></span>

## <span data-ttu-id="e1832-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1832-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1832-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1832-105">DESCRIPTION</span></span>
<span data-ttu-id="e1832-106">Cmdleten **Remove-AzRouteTable** tar bort en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="e1832-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="e1832-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1832-107">EXAMPLES</span></span>

### <span data-ttu-id="e1832-108">Exempel 1: ta bort en routningstabellen</span><span class="sxs-lookup"><span data-stu-id="e1832-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e1832-109">Det här kommandot tar bort routningstabellen med namnet RouteTable01 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e1832-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="e1832-110">Denna cmdlet ber dig bekräfta innan tabellen tas bort.</span><span class="sxs-lookup"><span data-stu-id="e1832-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="e1832-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1832-111">PARAMETERS</span></span>

### <span data-ttu-id="e1832-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1832-112">-AsJob</span></span>
<span data-ttu-id="e1832-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e1832-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1832-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1832-114">-DefaultProfile</span></span>
<span data-ttu-id="e1832-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1832-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1832-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e1832-116">-Force</span></span>
<span data-ttu-id="e1832-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e1832-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e1832-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="e1832-118">-Name</span></span>
<span data-ttu-id="e1832-119">Anger namnet på den routningstabell som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="e1832-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e1832-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1832-120">-PassThru</span></span>
<span data-ttu-id="e1832-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="e1832-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e1832-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e1832-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1832-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1832-123">-ResourceGroupName</span></span>
<span data-ttu-id="e1832-124">Anger namnet på den resurs grupp som innehåller routningstabellen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="e1832-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e1832-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1832-125">-Confirm</span></span>
<span data-ttu-id="e1832-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1832-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1832-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1832-127">-WhatIf</span></span>
<span data-ttu-id="e1832-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1832-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1832-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1832-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1832-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1832-130">CommonParameters</span></span>
<span data-ttu-id="e1832-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1832-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1832-132">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1832-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1832-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1832-133">INPUTS</span></span>

### <span data-ttu-id="e1832-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e1832-134">System.String</span></span>

## <span data-ttu-id="e1832-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1832-135">OUTPUTS</span></span>

### <span data-ttu-id="e1832-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1832-136">System.Boolean</span></span>

## <span data-ttu-id="e1832-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1832-137">NOTES</span></span>

## <span data-ttu-id="e1832-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1832-138">RELATED LINKS</span></span>

[<span data-ttu-id="e1832-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1832-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="e1832-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1832-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="e1832-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="e1832-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


