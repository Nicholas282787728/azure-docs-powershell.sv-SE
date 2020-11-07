---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteTable.md
ms.openlocfilehash: 17cd4ab4e60156c1ab4d6dd4357e638ddaf2c5a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755792"
---
# <span data-ttu-id="0d75a-101">Remove-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d75a-101">Remove-AzureRmRouteTable</span></span>

## <span data-ttu-id="0d75a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0d75a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d75a-103">Tar bort en routningstabell.</span><span class="sxs-lookup"><span data-stu-id="0d75a-103">Removes a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d75a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0d75a-104">SYNTAX</span></span>

```
Remove-AzureRmRouteTable -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d75a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0d75a-105">DESCRIPTION</span></span>
<span data-ttu-id="0d75a-106">Cmdleten **Remove-AzureRmRouteTable** tar bort en Azure route-tabell.</span><span class="sxs-lookup"><span data-stu-id="0d75a-106">The **Remove-AzureRmRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="0d75a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0d75a-107">EXAMPLES</span></span>

### <span data-ttu-id="0d75a-108">Exempel 1: ta bort en routningstabellen</span><span class="sxs-lookup"><span data-stu-id="0d75a-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzureRmRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="0d75a-109">Det här kommandot tar bort routningstabellen med namnet RouteTable01 i resurs gruppen med namnet ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0d75a-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="0d75a-110">Denna cmdlet ber dig bekräfta innan tabellen tas bort.</span><span class="sxs-lookup"><span data-stu-id="0d75a-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="0d75a-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0d75a-111">PARAMETERS</span></span>

### <span data-ttu-id="0d75a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="0d75a-112">-Force</span></span>
<span data-ttu-id="0d75a-113">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="0d75a-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0d75a-114">-Namn</span><span class="sxs-lookup"><span data-stu-id="0d75a-114">-Name</span></span>
<span data-ttu-id="0d75a-115">Anger namnet på den routningstabell som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="0d75a-115">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0d75a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d75a-116">-PassThru</span></span>
<span data-ttu-id="0d75a-117">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="0d75a-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d75a-118">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="0d75a-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d75a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d75a-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d75a-120">Anger namnet på den resurs grupp som innehåller routningstabellen som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="0d75a-120">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="0d75a-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0d75a-121">-Confirm</span></span>
<span data-ttu-id="0d75a-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0d75a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d75a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d75a-123">-WhatIf</span></span>
<span data-ttu-id="0d75a-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0d75a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d75a-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0d75a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d75a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d75a-126">-DefaultProfile</span></span>
<span data-ttu-id="0d75a-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0d75a-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d75a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d75a-128">CommonParameters</span></span>
<span data-ttu-id="0d75a-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d75a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d75a-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d75a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d75a-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0d75a-131">INPUTS</span></span>

## <span data-ttu-id="0d75a-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0d75a-132">OUTPUTS</span></span>

## <span data-ttu-id="0d75a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0d75a-133">NOTES</span></span>

## <span data-ttu-id="0d75a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0d75a-134">RELATED LINKS</span></span>

[<span data-ttu-id="0d75a-135">Get-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d75a-135">Get-AzureRmRouteTable</span></span>](./Get-AzureRmRouteTable.md)

[<span data-ttu-id="0d75a-136">New-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d75a-136">New-AzureRmRouteTable</span></span>](./New-AzureRmRouteTable.md)

[<span data-ttu-id="0d75a-137">Set-AzureRmRouteTable</span><span class="sxs-lookup"><span data-stu-id="0d75a-137">Set-AzureRmRouteTable</span></span>](./Set-AzureRmRouteTable.md)


