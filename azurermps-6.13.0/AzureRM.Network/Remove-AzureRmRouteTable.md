---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: cbb39febd5c4e0fbec63cc473d30c13a1e259e99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580751"
---
# <span data-ttu-id="26363-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="26363-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="26363-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="26363-102">SYNOPSIS</span></span>
<span data-ttu-id="26363-103">Tar bort en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="26363-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26363-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="26363-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26363-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="26363-105">DESCRIPTION</span></span>
<span data-ttu-id="26363-106">Cmdleten **Remove-AzureRmRouteTable** tar bort en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="26363-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="26363-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="26363-107">EXAMPLES</span></span>

### <span data-ttu-id="26363-108">Exempel 1: ta bort en routningstabellen</span><span class="sxs-lookup"><span data-stu-id="26363-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="26363-109">Det här kommandot tar bort routningstabellen med namnet RouteTable01 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="26363-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="26363-110">Denna cmdlet ber dig bekräfta innan tabellen tas bort.</span><span class="sxs-lookup"><span data-stu-id="26363-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="26363-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="26363-111">PARAMETERS</span></span>

### <span data-ttu-id="26363-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26363-112">-AsJob</span></span>
<span data-ttu-id="26363-113">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="26363-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26363-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26363-114">-DefaultProfile</span></span>
<span data-ttu-id="26363-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="26363-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26363-116">-Force</span><span class="sxs-lookup"><span data-stu-id="26363-116">-Force</span></span>
<span data-ttu-id="26363-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="26363-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="26363-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="26363-118">-Name</span></span>
<span data-ttu-id="26363-119">Anger namnet på den routningstabell som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="26363-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="26363-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26363-120">-PassThru</span></span>
<span data-ttu-id="26363-121">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="26363-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26363-122">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="26363-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26363-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26363-123">-ResourceGroupName</span></span>
<span data-ttu-id="26363-124">Anger namnet på den resurs grupp som innehåller routningstabellen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="26363-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="26363-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="26363-125">-Confirm</span></span>
<span data-ttu-id="26363-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="26363-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26363-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26363-127">-WhatIf</span></span>
<span data-ttu-id="26363-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="26363-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26363-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="26363-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26363-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26363-130">CommonParameters</span></span>
<span data-ttu-id="26363-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26363-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26363-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26363-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26363-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="26363-133">INPUTS</span></span>

### <span data-ttu-id="26363-134">System. String</span><span class="sxs-lookup"><span data-stu-id="26363-134">System.String</span></span>

## <span data-ttu-id="26363-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="26363-135">OUTPUTS</span></span>

### <span data-ttu-id="26363-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26363-136">System.Boolean</span></span>

## <span data-ttu-id="26363-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="26363-137">NOTES</span></span>

## <span data-ttu-id="26363-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="26363-138">RELATED LINKS</span></span>

[<span data-ttu-id="26363-139">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="26363-139">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="26363-140">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="26363-140">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="26363-141">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="26363-141">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


