---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: a0c4e6835525dfbecd4bb7eca239f8327df6ff8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756910"
---
# <span data-ttu-id="4f4be-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="4f4be-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="4f4be-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4f4be-102">SYNOPSIS</span></span>
<span data-ttu-id="4f4be-103">Anger adresspoolen för VPN-klienter för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f4be-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4f4be-104">SYNTAX</span></span>

### <span data-ttu-id="4f4be-105">Standard (standard)</span><span class="sxs-lookup"><span data-stu-id="4f4be-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f4be-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4f4be-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f4be-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4f4be-107">DESCRIPTION</span></span>
<span data-ttu-id="4f4be-108">Cmdleten **set-AzureRmVirtualNetworkVpnClientConfig** konfigurerar klient-adresspoolen för en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="4f4be-109">Klienter för virtuella privata nätverk (VPN) som ansluter till denna gateway tilldelas en IP-adress från den här adresspoolen.</span><span class="sxs-lookup"><span data-stu-id="4f4be-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="4f4be-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4f4be-110">EXAMPLES</span></span>

### <span data-ttu-id="4f4be-111">Exempel 1: tilldela en VPN-adresspool till en virtuell nätverksgateway</span><span class="sxs-lookup"><span data-stu-id="4f4be-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="4f4be-112">I det här exemplet tilldelas en VPN-adresspool till en virtuell nätverksgateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="4f4be-113">Det första kommandot skapar en objekt referens till en gateway och objektet lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="4f4be-114">I det andra kommandot i exemplet används cmdleten **set-AzureRmVirtualNetworkGatewayVpnClientConfig** för att tilldela adresspoolen 10.0.0.0/16 till ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="4f4be-115">Exempel 2: Konfigurera extern RADIUS-baserad verifikation på en befintlig gateway</span><span class="sxs-lookup"><span data-stu-id="4f4be-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="4f4be-116">I det här exemplet tilldelas en VPN-adresspool till en virtuell nätverksgateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="4f4be-117">Det första kommandot skapar en objekt referens till en gateway och objektet lagras i en variabel som heter $Gateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="4f4be-118">I det andra kommandot i exemplet används cmdleten **set-AzureRmVirtualNetworkGatewayVpnClientConfig** för att tilldela adresspoolen 10.0.0.0/16 till ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="4f4be-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="4f4be-119">Den konfigurerar också den externa RADIUS-servern "TestRadiusServer" för att användas för serverautentisering.</span><span class="sxs-lookup"><span data-stu-id="4f4be-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="4f4be-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4f4be-120">PARAMETERS</span></span>

### <span data-ttu-id="4f4be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f4be-121">-DefaultProfile</span></span>
<span data-ttu-id="4f4be-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4f4be-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f4be-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="4f4be-123">-RadiusServerAddress</span></span>
<span data-ttu-id="4f4be-124">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="4f4be-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4be-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="4f4be-125">-RadiusServerSecret</span></span>
<span data-ttu-id="4f4be-126">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="4f4be-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4be-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4f4be-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="4f4be-128">Anger en objekt referens till den virtuella nätverksgateway som innehåller de VPN-klient konfigurations inställningar som denna cmdlet ändrar.</span><span class="sxs-lookup"><span data-stu-id="4f4be-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="4f4be-129">Du kan skapa en objekt referens till en virtuell nätverksgateway genom att använda Get-AzureRmVirtualNetworkGateway och ange namnet på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="4f4be-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f4be-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="4f4be-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="4f4be-131">Anger vilka IP-adresser som ska tilldelas klienter som ansluter till denna gateway</span><span class="sxs-lookup"><span data-stu-id="4f4be-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="4f4be-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4f4be-132">-Confirm</span></span>
<span data-ttu-id="4f4be-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4f4be-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f4be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f4be-134">-WhatIf</span></span>
<span data-ttu-id="4f4be-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4f4be-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f4be-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4f4be-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f4be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f4be-137">CommonParameters</span></span>
<span data-ttu-id="4f4be-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f4be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f4be-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f4be-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f4be-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4f4be-140">INPUTS</span></span>

###  
<span data-ttu-id="4f4be-141">Denna cmdlet accepterar pipeline-instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="4f4be-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="4f4be-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4f4be-142">OUTPUTS</span></span>

###  
<span data-ttu-id="4f4be-143">Denna cmdlet ändrar befintliga instanser av **Microsoft. Azure. commands. Network. Models. PSVirtualNetworkGateway** -objektet.</span><span class="sxs-lookup"><span data-stu-id="4f4be-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="4f4be-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4f4be-144">NOTES</span></span>

## <span data-ttu-id="4f4be-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4f4be-145">RELATED LINKS</span></span>

[<span data-ttu-id="4f4be-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="4f4be-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="4f4be-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4f4be-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="4f4be-148">Ändra storlek – AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="4f4be-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


