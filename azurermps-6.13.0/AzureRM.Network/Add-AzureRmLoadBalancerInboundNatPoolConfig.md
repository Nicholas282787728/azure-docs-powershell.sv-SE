---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EB4DF001-AD05-4747-972B-5E4194A404C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: 2245fa10d160fc0f6b085a039214f9bcd72404a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574818"
---
# <span data-ttu-id="0f8c9-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="0f8c9-101">Add-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="0f8c9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0f8c9-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f8c9-103">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0f8c9-103">SYNTAX</span></span>

### <span data-ttu-id="0f8c9-104">SetByResource (standard)</span><span class="sxs-lookup"><span data-stu-id="0f8c9-104">SetByResource (Default)</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset]
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f8c9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f8c9-105">SetByResourceId</span></span>
```
Add-AzureRmLoadBalancerInboundNatPoolConfig -LoadBalancer <PSLoadBalancer> -Name <String> -Protocol <String>
 -FrontendPortRangeStart <Int32> -FrontendPortRangeEnd <Int32> -BackendPort <Int32>
 [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP] [-EnableTcpReset] [-FrontendIpConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f8c9-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0f8c9-106">DESCRIPTION</span></span>

## <span data-ttu-id="0f8c9-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0f8c9-107">EXAMPLES</span></span>

### <span data-ttu-id="0f8c9-108">1: lägga till</span><span class="sxs-lookup"><span data-stu-id="0f8c9-108">1: Add</span></span>
```
PS C:\> $slb = Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> $feIpConfig = Get-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendName" -Loadbalancer $slb
PS C:\> $slb | Add-AzureRmLoadBalancerInboundNatPoolConfig -Name "myInboundNatPool" -Protocol TCP -FrontendIPConfigurationId $feIpConfig.Id -FrontendPortRangeStart 1001 -FrontendPortRangeEnd 2000 -BackendPort 1001
```

## <span data-ttu-id="0f8c9-109">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0f8c9-109">PARAMETERS</span></span>

### <span data-ttu-id="0f8c9-110">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="0f8c9-110">-BackendPort</span></span>
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

### <span data-ttu-id="0f8c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f8c9-111">-DefaultProfile</span></span>
<span data-ttu-id="0f8c9-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f8c9-113">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="0f8c9-113">-EnableFloatingIP</span></span>
<span data-ttu-id="0f8c9-114">Konfigurerar en virtuell dators slut punkt för den flytande IP-kapaciteten som krävs för att konfigurera en SQL AlwaysOn-tillgänglighetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-114">Configures a virtual machine's endpoint for the floating IP capability required to configure a SQL AlwaysOn Availability Group.</span></span> <span data-ttu-id="0f8c9-115">Den här inställningen krävs vid användning av SQL AlwaysOn-tillgänglighetsgruppen i SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-115">This setting is required when using the SQL AlwaysOn Availability Groups in SQL server.</span></span> <span data-ttu-id="0f8c9-116">Den här inställningen kan inte ändras när du har skapat slut punkten.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-116">This setting can't be changed after you create the endpoint.</span></span>

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

### <span data-ttu-id="0f8c9-117">-EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="0f8c9-117">-EnableTcpReset</span></span>
<span data-ttu-id="0f8c9-118">Ta emot dubbelriktad TCP-återställning i TCP-flödets tids gräns för inaktivitet eller oväntat upphör Ande.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-118">Receive bidirectional TCP Reset on TCP flow idle timeout or unexpected connection termination.</span></span> <span data-ttu-id="0f8c9-119">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-119">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0f8c9-120">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f8c9-120">-FrontendIpConfiguration</span></span>
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

### <span data-ttu-id="0f8c9-121">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0f8c9-121">-FrontendIpConfigurationId</span></span>
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

### <span data-ttu-id="0f8c9-122">-FrontendPortRangeEnd</span><span class="sxs-lookup"><span data-stu-id="0f8c9-122">-FrontendPortRangeEnd</span></span>
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

### <span data-ttu-id="0f8c9-123">-FrontendPortRangeStart</span><span class="sxs-lookup"><span data-stu-id="0f8c9-123">-FrontendPortRangeStart</span></span>
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

### <span data-ttu-id="0f8c9-124">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="0f8c9-124">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="0f8c9-125">Timeout för TCP-inaktiv anslutning.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-125">The timeout for the TCP idle connection.</span></span> <span data-ttu-id="0f8c9-126">Värdet kan anges mellan 4 och 30 minuter.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-126">The value can be set between 4 and 30 minutes.</span></span> <span data-ttu-id="0f8c9-127">Standardvärdet är 4 minuter.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-127">The default value is 4 minutes.</span></span> <span data-ttu-id="0f8c9-128">Det här elementet används bara när protokollet är inställt på TCP.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-128">This element is only used when the protocol is set to TCP.</span></span>

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

### <span data-ttu-id="0f8c9-129">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f8c9-129">-LoadBalancer</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f8c9-130">-Namn</span><span class="sxs-lookup"><span data-stu-id="0f8c9-130">-Name</span></span>
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

### <span data-ttu-id="0f8c9-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0f8c9-131">-Protocol</span></span>
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

### <span data-ttu-id="0f8c9-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0f8c9-132">-Confirm</span></span>
<span data-ttu-id="0f8c9-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f8c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f8c9-134">-WhatIf</span></span>
<span data-ttu-id="0f8c9-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f8c9-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f8c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f8c9-137">CommonParameters</span></span>
<span data-ttu-id="0f8c9-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f8c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f8c9-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f8c9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f8c9-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0f8c9-140">INPUTS</span></span>

### <span data-ttu-id="0f8c9-141">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f8c9-141">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>
<span data-ttu-id="0f8c9-142">Parametrar: LoadBalancer (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0f8c9-142">Parameters: LoadBalancer (ByValue)</span></span>

## <span data-ttu-id="0f8c9-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0f8c9-143">OUTPUTS</span></span>

### <span data-ttu-id="0f8c9-144">Microsoft. Azure. commands. Networks. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="0f8c9-144">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="0f8c9-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0f8c9-145">NOTES</span></span>

## <span data-ttu-id="0f8c9-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0f8c9-146">RELATED LINKS</span></span>
