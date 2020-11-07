---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 32709a1a0280604b784c9f094478858f8c4bc4ab
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929306"
---
# <span data-ttu-id="bb6e5-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bb6e5-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="bb6e5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6e5-103">Tar bort en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb6e5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb6e5-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb6e5-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb6e5-105">DESCRIPTION</span></span>
<span data-ttu-id="bb6e5-106">Cmdleten **Remove-AzureRmNetworkSecurityGroup** tar bort en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="bb6e5-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb6e5-107">EXAMPLES</span></span>

### <span data-ttu-id="bb6e5-108">Exempel 1: ta bort en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="bb6e5-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="bb6e5-109">Det här kommandot tar bort säkerhets gruppen NSG-FrontEnd i resurs gruppen som heter TestRG.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="bb6e5-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb6e5-110">PARAMETERS</span></span>

### <span data-ttu-id="bb6e5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb6e5-111">-AsJob</span></span>
<span data-ttu-id="bb6e5-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bb6e5-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6e5-113">-DefaultProfile</span></span>
<span data-ttu-id="bb6e5-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bb6e5-115">-Force</span></span>
<span data-ttu-id="bb6e5-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb6e5-117">-Name</span></span>
<span data-ttu-id="bb6e5-118">Anger namnet på den nätverks säkerhets grupp som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb6e5-119">-PassThru</span></span>
<span data-ttu-id="bb6e5-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="bb6e5-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="bb6e5-123">Anger namnet på en resurs grupp som denna cmdlet tar bort en nätverks säkerhets grupp från.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb6e5-124">-Confirm</span></span>
<span data-ttu-id="bb6e5-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6e5-126">-WhatIf</span></span>
<span data-ttu-id="bb6e5-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb6e5-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6e5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6e5-129">CommonParameters</span></span>
<span data-ttu-id="bb6e5-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb6e5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6e5-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6e5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6e5-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb6e5-132">INPUTS</span></span>

## <span data-ttu-id="bb6e5-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb6e5-133">OUTPUTS</span></span>

## <span data-ttu-id="bb6e5-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb6e5-134">NOTES</span></span>

## <span data-ttu-id="bb6e5-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb6e5-135">RELATED LINKS</span></span>

[<span data-ttu-id="bb6e5-136">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bb6e5-136">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="bb6e5-137">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bb6e5-137">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="bb6e5-138">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bb6e5-138">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


