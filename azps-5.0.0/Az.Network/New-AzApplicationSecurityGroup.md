---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271789"
---
# <span data-ttu-id="5a25d-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a25d-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="5a25d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5a25d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a25d-103">Skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="5a25d-103">Creates an application security group.</span></span>

## <span data-ttu-id="5a25d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5a25d-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a25d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5a25d-105">DESCRIPTION</span></span>
<span data-ttu-id="5a25d-106">Cmdleten **New-AzApplicationSecurityGroup** skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="5a25d-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="5a25d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5a25d-107">EXAMPLES</span></span>

### <span data-ttu-id="5a25d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5a25d-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="5a25d-109">I det här exemplet skapas en säkerhets grupp för program utan associationer.</span><span class="sxs-lookup"><span data-stu-id="5a25d-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="5a25d-110">När det har skapats kan IP-konfigurationer i nätverks gränssnittet ingå i gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a25d-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="5a25d-111">Säkerhets reglerna kan även referera till gruppen som deras källor eller destinationer.</span><span class="sxs-lookup"><span data-stu-id="5a25d-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="5a25d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5a25d-112">PARAMETERS</span></span>

### <span data-ttu-id="5a25d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a25d-113">-AsJob</span></span>
<span data-ttu-id="5a25d-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5a25d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a25d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a25d-115">-DefaultProfile</span></span>
<span data-ttu-id="5a25d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5a25d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a25d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5a25d-117">-Force</span></span>
<span data-ttu-id="5a25d-118">Fråga inte efter bekräftelse om du vill skriva över en resurs.</span><span class="sxs-lookup"><span data-stu-id="5a25d-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="5a25d-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="5a25d-119">-Location</span></span>
<span data-ttu-id="5a25d-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="5a25d-120">The location.</span></span>

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

### <span data-ttu-id="5a25d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5a25d-121">-Name</span></span>
<span data-ttu-id="5a25d-122">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a25d-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="5a25d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a25d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a25d-124">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="5a25d-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="5a25d-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="5a25d-125">-Tag</span></span>
<span data-ttu-id="5a25d-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="5a25d-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a25d-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5a25d-127">-Confirm</span></span>
<span data-ttu-id="5a25d-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5a25d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a25d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a25d-129">-WhatIf</span></span>
<span data-ttu-id="5a25d-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5a25d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a25d-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5a25d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a25d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a25d-132">CommonParameters</span></span>
<span data-ttu-id="5a25d-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a25d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a25d-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a25d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a25d-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5a25d-135">INPUTS</span></span>

### <span data-ttu-id="5a25d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5a25d-136">System.String</span></span>

### <span data-ttu-id="5a25d-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="5a25d-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5a25d-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5a25d-138">OUTPUTS</span></span>

### <span data-ttu-id="5a25d-139">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a25d-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="5a25d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5a25d-140">NOTES</span></span>

## <span data-ttu-id="5a25d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5a25d-141">RELATED LINKS</span></span>

[<span data-ttu-id="5a25d-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a25d-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="5a25d-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5a25d-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="5a25d-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a25d-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5a25d-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a25d-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5a25d-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5a25d-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5a25d-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a25d-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5a25d-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a25d-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="5a25d-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a25d-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
