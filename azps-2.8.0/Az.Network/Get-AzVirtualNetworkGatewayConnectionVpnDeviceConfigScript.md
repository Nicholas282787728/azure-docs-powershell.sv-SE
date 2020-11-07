---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: f4bc62c1675743c62e4e26415435d48ef52034ee
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918422"
---
# <span data-ttu-id="3faf0-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="3faf0-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="3faf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3faf0-102">SYNOPSIS</span></span>
<span data-ttu-id="3faf0-103">Den här cmdleten tar anslutnings resursen, VPN-enhetens varumärke, modell, inbyggd program vara-version och returnerar motsvarande konfigurations skript som kunderna kan använda direkt på sina lokala VPN-enheter.</span><span class="sxs-lookup"><span data-stu-id="3faf0-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="3faf0-104">Skriptet följer syntaxen för den valda enheten och fyller i nödvändiga parametrar, till exempel Azure Gateway offentlig IP-adresser, prefix för virtuell nätverks adress, VPN-tunnel i förväg, etc. så att kunder helt enkelt kan kopiera-klistra in till sina VPN-enheter.</span><span class="sxs-lookup"><span data-stu-id="3faf0-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="3faf0-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3faf0-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3faf0-106">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3faf0-106">DESCRIPTION</span></span>
<span data-ttu-id="3faf0-107">Den här cmdleten tar anslutnings resursen, VPN-enhetens varumärke, modell, inbyggd program vara-version och returnerar motsvarande konfigurations skript som kunderna kan använda direkt på sina lokala VPN-enheter.</span><span class="sxs-lookup"><span data-stu-id="3faf0-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="3faf0-108">Skriptet följer syntaxen för den valda enheten och fyller i nödvändiga parametrar, till exempel Azure Gateway offentlig IP-adresser, prefix för virtuell nätverks adress, VPN-tunnel i förväg, etc. så att kunder helt enkelt kan kopiera-klistra in till sina VPN-enheter.</span><span class="sxs-lookup"><span data-stu-id="3faf0-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="3faf0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3faf0-109">EXAMPLES</span></span>

### <span data-ttu-id="3faf0-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3faf0-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="3faf0-111">I exemplet ovan används Get-AzVirtualNetworkGatewaySupportedVpnDevice för att få VPN-enheternas varumärken, modeller och inbyggd program vara.</span><span class="sxs-lookup"><span data-stu-id="3faf0-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="3faf0-112">Sedan används en av den information som returneras för att skapa ett skript för VPN-enhets konfiguration för VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="3faf0-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="3faf0-113">Enheten som används i det här exemplet har DeviceFamily "IOS-test", DeviceVendor "Cisco-test" och FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="3faf0-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="3faf0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3faf0-114">PARAMETERS</span></span>

### <span data-ttu-id="3faf0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3faf0-115">-DefaultProfile</span></span>
<span data-ttu-id="3faf0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3faf0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3faf0-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="3faf0-117">-DeviceFamily</span></span>
<span data-ttu-id="3faf0-118">Namn på VPN-enhetens modell/-familj.</span><span class="sxs-lookup"><span data-stu-id="3faf0-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="3faf0-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="3faf0-119">-DeviceVendor</span></span>
<span data-ttu-id="3faf0-120">Namn på VPN-enhetens tillverkare.</span><span class="sxs-lookup"><span data-stu-id="3faf0-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="3faf0-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="3faf0-121">-FirmwareVersion</span></span>
<span data-ttu-id="3faf0-122">Inbyggd program varu version för VPN-enheten.</span><span class="sxs-lookup"><span data-stu-id="3faf0-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="3faf0-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="3faf0-123">-Name</span></span>
<span data-ttu-id="3faf0-124">Resurs namn för den anslutning vars konfiguration ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3faf0-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="3faf0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3faf0-125">-ResourceGroupName</span></span>
<span data-ttu-id="3faf0-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3faf0-126">The resource group name.</span></span>

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

### <span data-ttu-id="3faf0-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3faf0-127">-Confirm</span></span>
<span data-ttu-id="3faf0-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3faf0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3faf0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3faf0-129">-WhatIf</span></span>
<span data-ttu-id="3faf0-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3faf0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3faf0-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3faf0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3faf0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3faf0-132">CommonParameters</span></span>
<span data-ttu-id="3faf0-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3faf0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3faf0-134">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3faf0-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3faf0-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3faf0-135">INPUTS</span></span>

### <span data-ttu-id="3faf0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3faf0-136">System.String</span></span>

## <span data-ttu-id="3faf0-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3faf0-137">OUTPUTS</span></span>

### <span data-ttu-id="3faf0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3faf0-138">System.String</span></span>

## <span data-ttu-id="3faf0-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3faf0-139">NOTES</span></span>

## <span data-ttu-id="3faf0-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3faf0-140">RELATED LINKS</span></span>
