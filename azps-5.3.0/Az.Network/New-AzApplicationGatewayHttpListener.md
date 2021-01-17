---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: a6fc3eb16cc82f7a0964e8cd0c1697a083771016
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425376"
---
# <span data-ttu-id="b9118-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b9118-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b9118-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b9118-102">SYNOPSIS</span></span>
<span data-ttu-id="b9118-103">Skapar en HTTP-lyssnare för en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="b9118-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="b9118-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b9118-104">SYNTAX</span></span>

### <span data-ttu-id="b9118-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9118-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-FirewallPolicyId <String>] [-SslProfileId <String>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9118-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b9118-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9118-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b9118-107">DESCRIPTION</span></span>
<span data-ttu-id="b9118-108">Cmdleten **New-AzApplicationGatewayHttpListener** skapar en http-lyssnare för en Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9118-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="b9118-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b9118-109">EXAMPLES</span></span>

### <span data-ttu-id="b9118-110">Exempel 1: skapa en HTTP-lyssnare</span><span class="sxs-lookup"><span data-stu-id="b9118-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="b9118-111">Det här kommandot skapar en HTTP-lyssnare som heter Listener01 och lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="b9118-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="b9118-112">Exempel 2: skapa en HTTP-lyssnare med SSL</span><span class="sxs-lookup"><span data-stu-id="b9118-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="b9118-113">Det här kommandot skapar en HTTP-lyssnare som använder SSL Offload och tillhandahåller SSL-certifikatet i variabeln $SSLCert 01.</span><span class="sxs-lookup"><span data-stu-id="b9118-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="b9118-114">Kommandot lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="b9118-114">The command stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="b9118-115">Exempel 3: skapa en HTTP-lyssnare med brand vägg – princip</span><span class="sxs-lookup"><span data-stu-id="b9118-115">Example 3: Create an HTTP listener with firewall-policy</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="b9118-116">Det här kommandot skapar en HTTP-lyssnare som heter Listener01, FirewallPolicy som $firewallPolicy och lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="b9118-116">This command creates an HTTP listener named Listener01, FirewallPolicy as $firewallPolicy and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="b9118-117">Exempel 4: lägga till en HTTPS-lyssnare med SSL och värdnamn</span><span class="sxs-lookup"><span data-stu-id="b9118-117">Example 4: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\> $Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="b9118-118">Det här kommandot skapar en HTTP-lyssnare som använder SSL Offload och tillhandahåller SSL-certifikatet i variabeln $SSLCert 01 tillsammans med två värdnamn.</span><span class="sxs-lookup"><span data-stu-id="b9118-118">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable along with two HostNames.</span></span>
<span data-ttu-id="b9118-119">Kommandot lagrar resultatet i variabeln som heter $Listener.</span><span class="sxs-lookup"><span data-stu-id="b9118-119">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="b9118-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b9118-120">PARAMETERS</span></span>

### <span data-ttu-id="b9118-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9118-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b9118-122">Kund fel för en Programgateway</span><span class="sxs-lookup"><span data-stu-id="b9118-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9118-123">-DefaultProfile</span></span>
<span data-ttu-id="b9118-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b9118-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9118-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b9118-125">-FirewallPolicy</span></span>
<span data-ttu-id="b9118-126">Anger objekt referensen till en brand Väggs princip på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="b9118-126">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="b9118-127">Objekt referensen kan skapas med hjälp av New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9118-127">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="b9118-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy-namn "wafPolicy1"-ResourceGroup "rgName" en brand Väggs princip som skapas med hjälp av ovanstående cmdleten kan hänvisas till en sökväg på en nivå.</span><span class="sxs-lookup"><span data-stu-id="b9118-128">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="b9118-129">med kommandot ovan skulle du skapa en standard princip inställning och hanterade regler.</span><span class="sxs-lookup"><span data-stu-id="b9118-129">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="b9118-130">I stället för standardvärden kan användarna ange PolicySettings, ManagedRules genom att använda New-AzApplicationGatewayFirewallPolicySettings och New-AzApplicationGatewayFirewallPolicyManagedRules.</span><span class="sxs-lookup"><span data-stu-id="b9118-130">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-131">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b9118-131">-FirewallPolicyId</span></span>
<span data-ttu-id="b9118-132">Anger ID för en befintlig webb programs brand Väggs resurs på högsta nivån.</span><span class="sxs-lookup"><span data-stu-id="b9118-132">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="b9118-133">Brand Väggs princip-ID: n kan returneras med Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9118-133">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="b9118-134">När vi har det ID du kan använda parametern *FirewallPolicyId* i stället för parametern *FirewallPolicy* .</span><span class="sxs-lookup"><span data-stu-id="b9118-134">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="b9118-135">Till exempel:-FirewallPolicyId/Subscriptions/<abonnemang-ID>/resourceGroups/<resurs-ID>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName></span><span class="sxs-lookup"><span data-stu-id="b9118-135">For instance: -FirewallPolicyId  �/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>�</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-136">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b9118-136">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b9118-137">Anger front-IP-konfigurationsobjekt för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b9118-137">Specifies front-end IP configuration object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-138">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b9118-138">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b9118-139">Anger ID för front-IP-konfigurationen för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b9118-139">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-140">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b9118-140">-FrontendPort</span></span>
<span data-ttu-id="b9118-141">Anger front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b9118-141">Specifies the front-end port for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-142">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b9118-142">-FrontendPortId</span></span>
<span data-ttu-id="b9118-143">Anger ID för front porten för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b9118-143">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-144">-HostName</span><span class="sxs-lookup"><span data-stu-id="b9118-144">-HostName</span></span>
<span data-ttu-id="b9118-145">Anger värd namnet för Programgateway HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b9118-145">Specifies the host name of the application gateway HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-146">-Värdnamn</span><span class="sxs-lookup"><span data-stu-id="b9118-146">-HostNames</span></span>
<span data-ttu-id="b9118-147">Värdnamn</span><span class="sxs-lookup"><span data-stu-id="b9118-147">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-148">-Namn</span><span class="sxs-lookup"><span data-stu-id="b9118-148">-Name</span></span>
<span data-ttu-id="b9118-149">Anger namnet på den HTTP-lyssnare som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="b9118-149">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b9118-150">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b9118-150">-Protocol</span></span>
<span data-ttu-id="b9118-151">Anger protokollet som HTTP-lyssnaren använder.</span><span class="sxs-lookup"><span data-stu-id="b9118-151">Specifies the protocol that the HTTP listener uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-152">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b9118-152">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-153">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b9118-153">-SslCertificate</span></span>
<span data-ttu-id="b9118-154">Anger SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b9118-154">Specifies the SSL certificate object for the HTTP listener.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-155">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b9118-155">-SslCertificateId</span></span>
<span data-ttu-id="b9118-156">Anger ID för SSL-certifikatet för HTTP-lyssnaren.</span><span class="sxs-lookup"><span data-stu-id="b9118-156">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-157">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b9118-157">-SslProfile</span></span>
<span data-ttu-id="b9118-158">SslProfile</span><span class="sxs-lookup"><span data-stu-id="b9118-158">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-159">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b9118-159">-SslProfileId</span></span>
<span data-ttu-id="b9118-160">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b9118-160">SslProfileId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9118-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9118-161">CommonParameters</span></span>
<span data-ttu-id="b9118-162">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9118-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9118-163">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9118-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9118-164">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b9118-164">INPUTS</span></span>

### <span data-ttu-id="b9118-165">Ingen</span><span class="sxs-lookup"><span data-stu-id="b9118-165">None</span></span>

## <span data-ttu-id="b9118-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b9118-166">OUTPUTS</span></span>

### <span data-ttu-id="b9118-167">Microsoft. Azure. commands. Networks. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b9118-167">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b9118-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b9118-168">NOTES</span></span>

## <span data-ttu-id="b9118-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b9118-169">RELATED LINKS</span></span>

[<span data-ttu-id="b9118-170">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b9118-170">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b9118-171">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b9118-171">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b9118-172">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b9118-172">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b9118-173">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b9118-173">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


