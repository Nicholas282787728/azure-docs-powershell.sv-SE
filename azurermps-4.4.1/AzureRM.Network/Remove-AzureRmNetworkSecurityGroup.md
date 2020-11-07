---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 01F56553-1685-43D4-89E6-DDCDF17D1E00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: fd6d9a09bd2c4fa597d2c384d3ba8e730b3f1102
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755793"
---
# <span data-ttu-id="43163-101">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43163-101">Remove-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="43163-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="43163-102">SYNOPSIS</span></span>
<span data-ttu-id="43163-103">Tar bort en nätverks säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="43163-103">Removes a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43163-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="43163-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43163-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="43163-105">DESCRIPTION</span></span>
<span data-ttu-id="43163-106">Cmdleten **Remove-AzureRmNetworkSecurityGroup** tar bort en Azure Network Security-grupp.</span><span class="sxs-lookup"><span data-stu-id="43163-106">The **Remove-AzureRmNetworkSecurityGroup** cmdlet removes an Azure network security group.</span></span>

## <span data-ttu-id="43163-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="43163-107">EXAMPLES</span></span>

### <span data-ttu-id="43163-108">Exempel 1: ta bort en nätverks säkerhets grupp</span><span class="sxs-lookup"><span data-stu-id="43163-108">Example 1: Remove a network security group</span></span>
```
PS C:\>Remove-AzureRmNetworkSecurityGroup -Name "NSG-FrontEnd" -ResourceGroupName "TestRG"
```

<span data-ttu-id="43163-109">Det här kommandot tar bort säkerhets gruppen NSG-FrontEnd i resurs gruppen som heter TestRG.</span><span class="sxs-lookup"><span data-stu-id="43163-109">This command removes the security group named NSG-FrontEnd in the resource group named TestRG.</span></span>

## <span data-ttu-id="43163-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="43163-110">PARAMETERS</span></span>

### <span data-ttu-id="43163-111">-Force</span><span class="sxs-lookup"><span data-stu-id="43163-111">-Force</span></span>
<span data-ttu-id="43163-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="43163-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43163-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="43163-113">-Name</span></span>
<span data-ttu-id="43163-114">Anger namnet på den nätverks säkerhets grupp som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="43163-114">Specifies the name of the network security group that this cmdlet removes.</span></span>

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

### <span data-ttu-id="43163-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43163-115">-PassThru</span></span>
<span data-ttu-id="43163-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="43163-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="43163-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="43163-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="43163-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43163-118">-ResourceGroupName</span></span>
<span data-ttu-id="43163-119">Anger namnet på en resurs grupp som denna cmdlet tar bort en nätverks säkerhets grupp från.</span><span class="sxs-lookup"><span data-stu-id="43163-119">Specifies the name of a resource group that this cmdlet removes a network security group from.</span></span>

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

### <span data-ttu-id="43163-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="43163-120">-Confirm</span></span>
<span data-ttu-id="43163-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="43163-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43163-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43163-122">-WhatIf</span></span>
<span data-ttu-id="43163-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="43163-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43163-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="43163-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43163-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43163-125">-DefaultProfile</span></span>
<span data-ttu-id="43163-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="43163-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43163-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43163-127">CommonParameters</span></span>
<span data-ttu-id="43163-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43163-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43163-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43163-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43163-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="43163-130">INPUTS</span></span>

## <span data-ttu-id="43163-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="43163-131">OUTPUTS</span></span>

## <span data-ttu-id="43163-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="43163-132">NOTES</span></span>

## <span data-ttu-id="43163-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="43163-133">RELATED LINKS</span></span>

[<span data-ttu-id="43163-134">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43163-134">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="43163-135">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43163-135">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="43163-136">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="43163-136">Set-AzureRmNetworkSecurityGroup</span></span>](./Set-AzureRmNetworkSecurityGroup.md)


