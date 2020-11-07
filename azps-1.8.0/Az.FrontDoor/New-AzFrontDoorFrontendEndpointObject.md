---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 6d6253b338bef04c39032bb29b5fb0ba300f4073
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916749"
---
# <span data-ttu-id="5ca0d-101">New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="5ca0d-101">New-AzFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="5ca0d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5ca0d-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca0d-103">Skapa ett PSFrontendEndpoint-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5ca0d-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="5ca0d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5ca0d-104">SYNTAX</span></span>

```
New-AzFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ca0d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5ca0d-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca0d-106">Skapa ett PSFrontendEndpoint-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5ca0d-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="5ca0d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-107">EXAMPLES</span></span>

### <span data-ttu-id="5ca0d-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5ca0d-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="5ca0d-109">Skapa ett PSFrontendEndpoint-objekt för att skapa en front dörr</span><span class="sxs-lookup"><span data-stu-id="5ca0d-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="5ca0d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5ca0d-110">PARAMETERS</span></span>

### <span data-ttu-id="5ca0d-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="5ca0d-111">-CertificateSource</span></span>
<span data-ttu-id="5ca0d-112">Källan för SSL-certifikatet</span><span class="sxs-lookup"><span data-stu-id="5ca0d-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="5ca0d-113">-CertificateType</span></span>
<span data-ttu-id="5ca0d-114">typ av certifikat som används för säkra anslutningar till en frontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ca0d-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca0d-115">-DefaultProfile</span></span>
<span data-ttu-id="5ca0d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca0d-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="5ca0d-117">-HostName</span></span>
<span data-ttu-id="5ca0d-118">Värd namnet på frontendEndpoint.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="5ca0d-119">Måste vara ett domän namn.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-119">Must be a domain name.</span></span>

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

### <span data-ttu-id="5ca0d-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="5ca0d-120">-Name</span></span>
<span data-ttu-id="5ca0d-121">Slut punkts namn för klient delen.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-121">Frontend endpoint name.</span></span>

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

### <span data-ttu-id="5ca0d-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="5ca0d-122">-ProtocolType</span></span>
<span data-ttu-id="5ca0d-123">TLS-filtillägg som används för säker leverans</span><span class="sxs-lookup"><span data-stu-id="5ca0d-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca0d-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="5ca0d-124">-SecretName</span></span>
<span data-ttu-id="5ca0d-125">Namnet på den hemliga nyckel valv hemligheten som representerar det fullständiga certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="5ca0d-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="5ca0d-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="5ca0d-126">-SecretVersion</span></span>
<span data-ttu-id="5ca0d-127">Den version av nyckel valv hemligheten som representerar fullständigt certifikatets PFX</span><span class="sxs-lookup"><span data-stu-id="5ca0d-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

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

### <span data-ttu-id="5ca0d-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="5ca0d-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="5ca0d-129">Om den här värden ska tillåtas för tillhörighet.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="5ca0d-130">Standardvärdet är inaktiverat</span><span class="sxs-lookup"><span data-stu-id="5ca0d-130">Default value is Disabled</span></span>

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

### <span data-ttu-id="5ca0d-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="5ca0d-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="5ca0d-132">TTL för användning i sekunder för session-tillhörighet, om tillämpligt.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="5ca0d-133">Standardvärdet är 0</span><span class="sxs-lookup"><span data-stu-id="5ca0d-133">Default value is 0</span></span>

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

### <span data-ttu-id="5ca0d-134">-Valv</span><span class="sxs-lookup"><span data-stu-id="5ca0d-134">-Vault</span></span>
<span data-ttu-id="5ca0d-135">Det viktigaste valvet med SSL-certifikatet</span><span class="sxs-lookup"><span data-stu-id="5ca0d-135">The Key Vault containing the SSL certificate</span></span>

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

### <span data-ttu-id="5ca0d-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="5ca0d-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="5ca0d-137">Resurs-ID för webb program brand Väggs princip för varje värd (om tillämpligt)</span><span class="sxs-lookup"><span data-stu-id="5ca0d-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

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

### <span data-ttu-id="5ca0d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca0d-138">CommonParameters</span></span>
<span data-ttu-id="5ca0d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca0d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca0d-140">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ca0d-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca0d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5ca0d-141">INPUTS</span></span>

### <span data-ttu-id="5ca0d-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="5ca0d-142">None</span></span>

## <span data-ttu-id="5ca0d-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5ca0d-143">OUTPUTS</span></span>

### <span data-ttu-id="5ca0d-144">Microsoft. Azure. commands. FrontDoor. Models. PSFrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ca0d-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="5ca0d-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5ca0d-145">NOTES</span></span>

## <span data-ttu-id="5ca0d-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5ca0d-146">RELATED LINKS</span></span>

<span data-ttu-id="5ca0d-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="5ca0d-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
