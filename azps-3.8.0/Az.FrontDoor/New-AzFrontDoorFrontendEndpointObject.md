---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: efb32f3fa73fac50e5f96100ed895c2ca7d4a83e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93926078"
---
# <span data-ttu-id="5136d-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="5136d-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="5136d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5136d-102">SYNOPSIS</span></span>
<span data-ttu-id="5136d-103">Skapa ett PSFrontendEndpoint-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5136d-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="5136d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5136d-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <String>] [-MinimumTlsVersion <String>]
 [-ProtocolType <String>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5136d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5136d-105">DESCRIPTION</span></span>
<span data-ttu-id="5136d-106">Skapa ett PSFrontendEndpoint-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5136d-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="5136d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5136d-107">EXAMPLES</span></span>

### <span data-ttu-id="5136d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5136d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName "frontendendpoint1"


HostName                         : frontendendpoint1
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                :
MinimumTlsVersion                : 1.2
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  :
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
ProtocolType                     : ServerNameIndication
```

<span data-ttu-id="5136d-109">Skapa ett PSFrontendEndpoint-objekt för att skapa en front dörr.</span><span class="sxs-lookup"><span data-stu-id="5136d-109">Create a PSFrontendEndpoint Object for Front Door creation.</span></span>

## <span data-ttu-id="5136d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5136d-110">PARAMETERS</span></span>

### <span data-ttu-id="5136d-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="5136d-111">-CertificateSource</span></span>
<span data-ttu-id="5136d-112">Källan för SSL-certifikatet</span><span class="sxs-lookup"><span data-stu-id="5136d-112">The source of the SSL certificate</span></span>

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

### <span data-ttu-id="5136d-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5136d-113">-CertificateType</span></span>
<span data-ttu-id="5136d-114">typ av certifikat som används för säkra anslutningar till en frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="5136d-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

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

### <span data-ttu-id="5136d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5136d-115">-DefaultProfile</span></span>
<span data-ttu-id="5136d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5136d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5136d-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="5136d-117">-HostName</span></span>
<span data-ttu-id="5136d-118">Värd namnet på frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5136d-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="5136d-119">Måste vara ett domän namn.</span><span class="sxs-lookup"><span data-stu-id="5136d-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="5136d-120">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="5136d-120">-MinimumTlsVersion</span></span>
<span data-ttu-id="5136d-121">Den minsta TLS-version som krävs från klienter för att upprätta en SSL-handskakning med front dörren.</span><span class="sxs-lookup"><span data-stu-id="5136d-121">The minimum TLS version required from the clients to establish an SSL handshake with Front Door.</span></span>

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

### <span data-ttu-id="5136d-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="5136d-122">-Name</span></span>
<span data-ttu-id="5136d-123">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="5136d-123">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="5136d-124">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="5136d-124">-ProtocolType</span></span>
<span data-ttu-id="5136d-125">TLS-filtillägg som används för säker leverans</span><span class="sxs-lookup"><span data-stu-id="5136d-125">The TLS extension protocol that is used for secure delivery</span></span>

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

### <span data-ttu-id="5136d-126">-SecretName</span><span class="sxs-lookup"><span data-stu-id="5136d-126">-SecretName</span></span>
<span data-ttu-id="5136d-127">Namnet på den hemliga nyckel valv hemligheten som representerar det fullständiga certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="5136d-127">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="5136d-128">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="5136d-128">-SecretVersion</span></span>
<span data-ttu-id="5136d-129">Den version av nyckel valv hemligheten som representerar fullständigt certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="5136d-129">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="5136d-130">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="5136d-130">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="5136d-131">Om den här värden ska tillåtas för tillhörighet.</span><span class="sxs-lookup"><span data-stu-id="5136d-131">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="5136d-132">Standardvärdet är inaktiverat</span><span class="sxs-lookup"><span data-stu-id="5136d-132">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-133">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5136d-133">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="5136d-134">TTL för användning i sekunder för session-tillhörighet, om tillämpligt.</span><span class="sxs-lookup"><span data-stu-id="5136d-134">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="5136d-135">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="5136d-135">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5136d-136">-Valv</span><span class="sxs-lookup"><span data-stu-id="5136d-136">-Vault</span></span>
<span data-ttu-id="5136d-137">Det viktigaste valvet med SSL-certifikatet</span><span class="sxs-lookup"><span data-stu-id="5136d-137">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="5136d-138">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="5136d-138">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="5136d-139">Resurs-ID för webb program brand Väggs princip för varje värd (om tillämpligt)</span><span class="sxs-lookup"><span data-stu-id="5136d-139">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="5136d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5136d-140">CommonParameters</span></span>
<span data-ttu-id="5136d-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5136d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5136d-142">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5136d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5136d-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5136d-143">INPUTS</span></span>

### <span data-ttu-id="5136d-144">Ingen</span><span class="sxs-lookup"><span data-stu-id="5136d-144">None</span></span>
## <span data-ttu-id="5136d-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5136d-145">OUTPUTS</span></span>

### <span data-ttu-id="5136d-146">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="5136d-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>
## <span data-ttu-id="5136d-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5136d-147">NOTES</span></span>

## <span data-ttu-id="5136d-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5136d-148">RELATED LINKS</span></span>

<span data-ttu-id="5136d-149">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="5136d-149">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
