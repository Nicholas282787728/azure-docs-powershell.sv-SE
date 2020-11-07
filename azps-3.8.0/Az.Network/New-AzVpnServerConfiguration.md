---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927278"
---
# <span data-ttu-id="dac7d-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dac7d-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="dac7d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dac7d-102">SYNOPSIS</span></span>
<span data-ttu-id="dac7d-103">Skapa en ny VpnServerConfiguration för peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="dac7d-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="dac7d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dac7d-104">SYNTAX</span></span>

### <span data-ttu-id="dac7d-105">ByVpnServerConfigurationNameByCertificateAuthentication (standard)</span><span class="sxs-lookup"><span data-stu-id="dac7d-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dac7d-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="dac7d-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dac7d-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="dac7d-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dac7d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dac7d-108">DESCRIPTION</span></span>
<span data-ttu-id="dac7d-109">Med **New-AzVpnServerConfiguration-** cmdleten kan du skapa en ny VpnServerConfiguration med olika VpnProtocols, VpnAuthenticationTypes, IpsecPolicies och ställa in valda parametrar för VPN-autentiseringstyp enligt kundens krav för att peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="dac7d-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="dac7d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dac7d-110">EXAMPLES</span></span>

### <span data-ttu-id="dac7d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dac7d-111">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="dac7d-112">Kommandot ovan kommer att skapa en ny VpnServerConfiguration med VpnAuthenticationType som certifikat.</span><span class="sxs-lookup"><span data-stu-id="dac7d-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="dac7d-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dac7d-113">PARAMETERS</span></span>

### <span data-ttu-id="dac7d-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="dac7d-114">-AadAudience</span></span>
<span data-ttu-id="dac7d-115">AAD-Audience för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="dac7d-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="dac7d-116">-AadIssuer</span></span>
<span data-ttu-id="dac7d-117">AAD-utgivare för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="dac7d-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="dac7d-118">-AadTenant</span></span>
<span data-ttu-id="dac7d-119">AAD-klient för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="dac7d-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dac7d-120">-AsJob</span></span>
<span data-ttu-id="dac7d-121">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="dac7d-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac7d-122">-DefaultProfile</span></span>
<span data-ttu-id="dac7d-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dac7d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="dac7d-124">-Location</span></span>
<span data-ttu-id="dac7d-125">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="dac7d-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="dac7d-126">-Name</span></span>
<span data-ttu-id="dac7d-127">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="dac7d-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="dac7d-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="dac7d-129">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="dac7d-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="dac7d-130">-RadiusServerAddress</span></span>
<span data-ttu-id="dac7d-131">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="dac7d-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="dac7d-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="dac7d-133">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="dac7d-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="dac7d-134">-RadiusServerSecret</span></span>
<span data-ttu-id="dac7d-135">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="dac7d-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac7d-136">-ResourceGroupName</span></span>
<span data-ttu-id="dac7d-137">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="dac7d-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-138">-Tagg</span><span class="sxs-lookup"><span data-stu-id="dac7d-138">-Tag</span></span>
<span data-ttu-id="dac7d-139">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="dac7d-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="dac7d-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="dac7d-141">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="dac7d-141">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="dac7d-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="dac7d-143">En lista över IPSec-principer för VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dac7d-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="dac7d-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="dac7d-145">En lista med VpnClientCertificates för att bli återkallat filer</span><span class="sxs-lookup"><span data-stu-id="dac7d-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="dac7d-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="dac7d-147">En lista med VpnClientRootCertificates som ska läggas till i filer</span><span class="sxs-lookup"><span data-stu-id="dac7d-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="dac7d-148">-VpnProtocol</span></span>
<span data-ttu-id="dac7d-149">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="dac7d-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dac7d-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dac7d-150">-Confirm</span></span>
<span data-ttu-id="dac7d-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dac7d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dac7d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dac7d-152">-WhatIf</span></span>
<span data-ttu-id="dac7d-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dac7d-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dac7d-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dac7d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dac7d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac7d-155">CommonParameters</span></span>
<span data-ttu-id="dac7d-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dac7d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac7d-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dac7d-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac7d-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dac7d-158">INPUTS</span></span>

### <span data-ttu-id="dac7d-159">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="dac7d-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="dac7d-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dac7d-160">OUTPUTS</span></span>

### <span data-ttu-id="dac7d-161">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dac7d-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="dac7d-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dac7d-162">NOTES</span></span>

## <span data-ttu-id="dac7d-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dac7d-163">RELATED LINKS</span></span>
