---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092486"
---
# <span data-ttu-id="b4465-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4465-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="b4465-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b4465-102">SYNOPSIS</span></span>
<span data-ttu-id="b4465-103">Skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="b4465-103">Creates an application security group.</span></span>

## <span data-ttu-id="b4465-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b4465-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4465-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b4465-105">DESCRIPTION</span></span>
<span data-ttu-id="b4465-106">Cmdleten **New-AzApplicationSecurityGroup** skapar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="b4465-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="b4465-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b4465-107">EXAMPLES</span></span>

### <span data-ttu-id="b4465-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b4465-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="b4465-109">I det här exemplet skapas en säkerhets grupp för program utan associationer.</span><span class="sxs-lookup"><span data-stu-id="b4465-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="b4465-110">När det har skapats kan IP-konfigurationer i nätverks gränssnittet ingå i gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4465-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="b4465-111">Säkerhets reglerna kan även referera till gruppen som deras källor eller destinationer.</span><span class="sxs-lookup"><span data-stu-id="b4465-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="b4465-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b4465-112">PARAMETERS</span></span>

### <span data-ttu-id="b4465-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4465-113">-AsJob</span></span>
<span data-ttu-id="b4465-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b4465-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4465-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4465-115">-DefaultProfile</span></span>
<span data-ttu-id="b4465-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b4465-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4465-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b4465-117">-Force</span></span>
<span data-ttu-id="b4465-118">Fråga inte efter bekräftelse om du vill skriva över en resurs.</span><span class="sxs-lookup"><span data-stu-id="b4465-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="b4465-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="b4465-119">-Location</span></span>
<span data-ttu-id="b4465-120">Platsen.</span><span class="sxs-lookup"><span data-stu-id="b4465-120">The location.</span></span>

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

### <span data-ttu-id="b4465-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="b4465-121">-Name</span></span>
<span data-ttu-id="b4465-122">Namnet på program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4465-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="b4465-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4465-123">-ResourceGroupName</span></span>
<span data-ttu-id="b4465-124">Resurs grupps namnet för program säkerhets gruppen.</span><span class="sxs-lookup"><span data-stu-id="b4465-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="b4465-125">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b4465-125">-Tag</span></span>
<span data-ttu-id="b4465-126">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="b4465-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="b4465-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b4465-127">-Confirm</span></span>
<span data-ttu-id="b4465-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b4465-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4465-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4465-129">-WhatIf</span></span>
<span data-ttu-id="b4465-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b4465-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4465-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b4465-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4465-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4465-132">CommonParameters</span></span>
<span data-ttu-id="b4465-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4465-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4465-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4465-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4465-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b4465-135">INPUTS</span></span>

### <span data-ttu-id="b4465-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b4465-136">System.String</span></span>

### <span data-ttu-id="b4465-137">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="b4465-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4465-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b4465-138">OUTPUTS</span></span>

### <span data-ttu-id="b4465-139">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4465-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="b4465-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b4465-140">NOTES</span></span>

## <span data-ttu-id="b4465-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b4465-141">RELATED LINKS</span></span>

[<span data-ttu-id="b4465-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4465-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b4465-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4465-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="b4465-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4465-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b4465-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4465-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b4465-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b4465-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="b4465-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4465-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b4465-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4465-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="b4465-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="b4465-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
