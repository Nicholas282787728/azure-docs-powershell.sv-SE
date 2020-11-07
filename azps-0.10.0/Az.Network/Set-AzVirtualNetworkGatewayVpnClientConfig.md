---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 1c85bc5e2a935378630728083b19544ace8670b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924118"
---
# <span data-ttu-id="5755a-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="5755a-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="5755a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5755a-102">SYNOPSIS</span></span>
<span data-ttu-id="5755a-103">Anger adresspoolen för VPN-klienter för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

## <span data-ttu-id="5755a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5755a-104">SYNTAX</span></span>

### <span data-ttu-id="5755a-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="5755a-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5755a-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="5755a-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5755a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5755a-107">DESCRIPTION</span></span>
<span data-ttu-id="5755a-108">Cmdleten **set-AzVirtualNetworkVpnClientConfig** konfigurerar klient-adresspoolen för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-108">The **Set-AzVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="5755a-109">Klienter för virtuella privata nätverk (VPN) som ansluter till denna gateway tilldelas en IP-adress från den här adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="5755a-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="5755a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5755a-110">EXAMPLES</span></span>

### <span data-ttu-id="5755a-111">Exempel 1: tilldela en VPN-adresspool till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="5755a-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="5755a-112">I det här exemplet tilldelas en VPN-adresspool till en virtuell nätverksgateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="5755a-113">Det första kommandot skapar en objekt referens till en gateway och objektet lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="5755a-114">I det andra kommandot i exemplet används cmdleten **set-AzVirtualNetworkGatewayVpnClientConfig** för att tilldela adresspoolen 10.0.0.0/16 till ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-114">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="5755a-115">Exempel 2: Konfigurera extern RADIUS-baserad verifikation på en befintlig gateway</span><span class="sxs-lookup"><span data-stu-id="5755a-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="5755a-116">I det här exemplet tilldelas en VPN-adresspool till en virtuell nätverksgateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="5755a-117">Det första kommandot skapar en objekt referens till en gateway och objektet lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="5755a-118">I det andra kommandot i exemplet används cmdleten **set-AzVirtualNetworkGatewayVpnClientConfig** för att tilldela adresspoolen 10.0.0.0/16 till ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="5755a-118">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="5755a-119">Den konfigurerar också den externa RADIUS-servern "TestRadiusServer" för att användas för serverautentisering.</span><span class="sxs-lookup"><span data-stu-id="5755a-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="5755a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5755a-120">PARAMETERS</span></span>

### <span data-ttu-id="5755a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5755a-121">-DefaultProfile</span></span>
<span data-ttu-id="5755a-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5755a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5755a-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="5755a-123">-RadiusServerAddress</span></span>
<span data-ttu-id="5755a-124">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="5755a-124">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5755a-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="5755a-125">-RadiusServerSecret</span></span>
<span data-ttu-id="5755a-126">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="5755a-126">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5755a-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5755a-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="5755a-128">Anger en objekt referens till den virtuella nätverksgateway som innehåller de VPN-klient konfigurations inställningar som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="5755a-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="5755a-129">Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda Get-AzVirtualNetworkGateway och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="5755a-129">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5755a-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="5755a-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="5755a-131">Anger vilka IP-adresser som ska tilldelas klienter som ansluter till denna gateway</span><span class="sxs-lookup"><span data-stu-id="5755a-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5755a-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5755a-132">-Confirm</span></span>
<span data-ttu-id="5755a-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5755a-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5755a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5755a-134">-WhatIf</span></span>
<span data-ttu-id="5755a-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5755a-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5755a-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5755a-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5755a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5755a-137">CommonParameters</span></span>
<span data-ttu-id="5755a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5755a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5755a-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5755a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5755a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5755a-140">INPUTS</span></span>

###  
<span data-ttu-id="5755a-141">Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="5755a-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="5755a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5755a-142">OUTPUTS</span></span>

###  
<span data-ttu-id="5755a-143">Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="5755a-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="5755a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5755a-144">NOTES</span></span>

## <span data-ttu-id="5755a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5755a-145">RELATED LINKS</span></span>

[<span data-ttu-id="5755a-146">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="5755a-146">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="5755a-147">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5755a-147">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="5755a-148">Ändra storlek – AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5755a-148">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)


