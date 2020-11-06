---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 61C34433-A16A-4ACF-A318-1C7D9E49579F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 097377cd1ca4cb4be4fe62e2008f899c05c194fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584923"
---
# <span data-ttu-id="060b3-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="060b3-101">New-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="060b3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="060b3-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="060b3-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="060b3-103">SYNTAX</span></span>

### <span data-ttu-id="060b3-104">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="060b3-104">SetByResource (Default)</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfiguration <PSFrontendIPConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="060b3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="060b3-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatPoolConfig -Name <String> -Protocol <String> -FrontendPortRangeStart <Int32>
 -FrontendPortRangeEnd <Int32> -BackendPort <Int32> [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-EnableTcpReset] [-FrontendIpConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="060b3-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="060b3-106">DESCRIPTION</span></span>

## <span data-ttu-id="060b3-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="060b3-107">EXAMPLES</span></span>

### <span data-ttu-id="060b3-108">1: ny</span><span class="sxs-lookup"><span data-stu-id="060b3-108">1: New</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> New-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -FrontendIpConfigurationId $feIpConfig.Id -Protocol TCP -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="060b3-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="060b3-109">PARAMETERS</span></span>

### <span data-ttu-id="060b3-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="060b3-110">-BackendPort</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060b3-111">-DefaultProfile</span></span>
<span data-ttu-id="060b3-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="060b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="060b3-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="060b3-113">-EnableFloatingIP</span></span>
<span data-ttu-id="060b3-114">Konfigurerar en virtuell dators slut punkt för den flytande IP-kapaciteten som krävs för att konfigurera en SQL AlwaysOn-tillgänglighetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="060b3-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="060b3-115">Den här inställningen krävs vid användning av SQL AlwaysOn-tillgänglighetsgruppen i SQL Server.</span><span class="sxs-lookup"><span data-stu-id="060b3-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="060b3-116">Den här inställningen kan inte ändras när du har skapat slut punkten.</span><span class="sxs-lookup"><span data-stu-id="060b3-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="060b3-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="060b3-117">-EnableTcpReset</span></span>
<span data-ttu-id="060b3-118">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="060b3-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="060b3-119">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="060b3-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="060b3-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="060b3-120">-FrontendIpConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060b3-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="060b3-121">-FrontendIpConfigurationId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060b3-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="060b3-122">-FrontendPortRangeEnd</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060b3-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="060b3-123">-FrontendPortRangeStart</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060b3-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="060b3-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="060b3-125">Timeout för TCP-inaktiv anslutning.</span><span class="sxs-lookup"><span data-stu-id="060b3-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="060b3-126">Värdet kan anges mellan 4 och 30 minuter.</span><span class="sxs-lookup"><span data-stu-id="060b3-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="060b3-127">Standardvärdet är 4 minuter.</span><span class="sxs-lookup"><span data-stu-id="060b3-127">The default value is 4 minutes.</span></span> <span data-ttu-id="060b3-128">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="060b3-128">This element is only used when the protocol is set to TCP.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="060b3-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="060b3-129">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060b3-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="060b3-130">-Protocol</span></span>
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

### <span data-ttu-id="060b3-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="060b3-131">-Confirm</span></span>
<span data-ttu-id="060b3-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="060b3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="060b3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="060b3-133">-WhatIf</span></span>
<span data-ttu-id="060b3-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="060b3-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="060b3-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="060b3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="060b3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060b3-136">CommonParameters</span></span>
<span data-ttu-id="060b3-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="060b3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060b3-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="060b3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060b3-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="060b3-139">INPUTS</span></span>

### <span data-ttu-id="060b3-140">Ingen</span><span class="sxs-lookup"><span data-stu-id="060b3-140">None</span></span>

## <span data-ttu-id="060b3-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="060b3-141">OUTPUTS</span></span>

### <span data-ttu-id="060b3-142">Microsoft. Azure. commands. Networks. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="060b3-142">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="060b3-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="060b3-143">NOTES</span></span>

## <span data-ttu-id="060b3-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="060b3-144">RELATED LINKS</span></span>
