---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityGroup.md
ms.openlocfilehash: c5a5cbbbc46106fe6c388ee8f16117411f03fe0c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258184"
---
# <span data-ttu-id="c3534-101">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3534-101">Remove-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="c3534-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c3534-102">SYNOPSIS</span></span>
<span data-ttu-id="c3534-103">Tar bort en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="c3534-103">Removes a network security group.</span></span>

## <span data-ttu-id="c3534-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c3534-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3534-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c3534-105">DESCRIPTION</span></span>
<span data-ttu-id="c3534-106">Cmdleten **Remove-AzNetworkSecurityGroup** tar bort en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="c3534-106">The **Remove-AzNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="c3534-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c3534-107">EXAMPLES</span></span>

### <span data-ttu-id="c3534-108">Exempel 1: ta bort en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="c3534-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="c3534-109">Det här kommandot tar bort säkerhets gruppen NSG-FrontEnd i resurs gruppen som heter TestRG.</span><span class="sxs-lookup"><span data-stu-id="c3534-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="c3534-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c3534-110">PARAMETERS</span></span>

### <span data-ttu-id="c3534-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3534-111">-AsJob</span></span>
<span data-ttu-id="c3534-112">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c3534-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3534-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3534-113">-DefaultProfile</span></span>
<span data-ttu-id="c3534-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c3534-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3534-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c3534-115">-Force</span></span>
<span data-ttu-id="c3534-116">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c3534-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3534-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="c3534-117">-Name</span></span>
<span data-ttu-id="c3534-118">Anger namnet på den nätverks säkerhets grupp som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="c3534-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c3534-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3534-119">-PassThru</span></span>
<span data-ttu-id="c3534-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c3534-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c3534-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c3534-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c3534-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3534-122">-ResourceGroupName</span></span>
<span data-ttu-id="c3534-123">Anger namnet på en resurs grupp som denna cmdlet tar bort en nätverks säkerhets grupp från.</span><span class="sxs-lookup"><span data-stu-id="c3534-123">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="c3534-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c3534-124">-Confirm</span></span>
<span data-ttu-id="c3534-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c3534-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3534-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3534-126">-WhatIf</span></span>
<span data-ttu-id="c3534-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c3534-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3534-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c3534-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3534-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3534-129">CommonParameters</span></span>
<span data-ttu-id="c3534-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3534-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3534-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3534-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3534-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c3534-132">INPUTS</span></span>

### <span data-ttu-id="c3534-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3534-133">System.String</span></span>

## <span data-ttu-id="c3534-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c3534-134">OUTPUTS</span></span>

### <span data-ttu-id="c3534-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3534-135">System.Boolean</span></span>

## <span data-ttu-id="c3534-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c3534-136">NOTES</span></span>

## <span data-ttu-id="c3534-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c3534-137">RELATED LINKS</span></span>

[<span data-ttu-id="c3534-138">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3534-138">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="c3534-139">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3534-139">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="c3534-140">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c3534-140">Set-AzNetworkSecurityGroup</span></span>](./Set-AzNetworkSecurityGroup.md)

