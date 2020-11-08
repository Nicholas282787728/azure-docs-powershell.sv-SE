---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272875"
---
# <span data-ttu-id="0e5ef-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e5ef-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="0e5ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0e5ef-102">SYNOPSIS</span></span>
<span data-ttu-id="0e5ef-103">Skapa en ny VpnServerConfiguration för peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="0e5ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0e5ef-104">SYNTAX</span></span>

### <span data-ttu-id="0e5ef-105">ByVpnServerConfigurationNameByCertificateAuthentication (standard)</span><span class="sxs-lookup"><span data-stu-id="0e5ef-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e5ef-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="0e5ef-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e5ef-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="0e5ef-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e5ef-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0e5ef-108">DESCRIPTION</span></span>
<span data-ttu-id="0e5ef-109">Med **New-AzVpnServerConfiguration-** cmdleten kan du skapa en ny VpnServerConfiguration med olika VpnProtocols, VpnAuthenticationTypes, IpsecPolicies och ställa in valda parametrar för VPN-autentiseringstyp enligt kundens krav för att peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="0e5ef-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0e5ef-110">EXAMPLES</span></span>

### <span data-ttu-id="0e5ef-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="0e5ef-111">Example 1</span></span>
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

<span data-ttu-id="0e5ef-112">Kommandot ovan kommer att skapa en ny VpnServerConfiguration med VpnAuthenticationType som certifikat.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="0e5ef-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="0e5ef-113">Example 2</span></span>

<span data-ttu-id="0e5ef-114">Skapa en ny VpnServerConfiguration för peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="0e5ef-115">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="0e5ef-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="0e5ef-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0e5ef-116">PARAMETERS</span></span>

### <span data-ttu-id="0e5ef-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="0e5ef-117">-AadAudience</span></span>
<span data-ttu-id="0e5ef-118">AAD-Audience för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="0e5ef-119">-AadIssuer</span></span>
<span data-ttu-id="0e5ef-120">AAD-utgivare för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="0e5ef-121">-AadTenant</span></span>
<span data-ttu-id="0e5ef-122">AAD-klient för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e5ef-123">-AsJob</span></span>
<span data-ttu-id="0e5ef-124">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="0e5ef-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e5ef-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e5ef-125">-DefaultProfile</span></span>
<span data-ttu-id="0e5ef-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e5ef-127">-Plats</span><span class="sxs-lookup"><span data-stu-id="0e5ef-127">-Location</span></span>
<span data-ttu-id="0e5ef-128">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-128">The resource location.</span></span>

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

### <span data-ttu-id="0e5ef-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="0e5ef-129">-Name</span></span>
<span data-ttu-id="0e5ef-130">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0e5ef-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="0e5ef-132">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="0e5ef-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="0e5ef-133">-RadiusServerAddress</span></span>
<span data-ttu-id="0e5ef-134">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="0e5ef-135">-RadiusServerList</span></span>
<span data-ttu-id="0e5ef-136">P2S externa flera RADIUS-servrar.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0e5ef-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="0e5ef-138">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="0e5ef-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="0e5ef-139">-RadiusServerSecret</span></span>
<span data-ttu-id="0e5ef-140">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e5ef-141">-ResourceGroupName</span></span>
<span data-ttu-id="0e5ef-142">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-142">The resource group name.</span></span>

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

### <span data-ttu-id="0e5ef-143">-Tagg</span><span class="sxs-lookup"><span data-stu-id="0e5ef-143">-Tag</span></span>
<span data-ttu-id="0e5ef-144">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="0e5ef-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="0e5ef-146">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-146">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="0e5ef-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="0e5ef-148">En lista över IPSec-principer för VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0e5ef-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="0e5ef-150">En lista med VpnClientCertificates för att bli återkallat filer</span><span class="sxs-lookup"><span data-stu-id="0e5ef-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="0e5ef-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="0e5ef-152">En lista med VpnClientRootCertificates som ska läggas till i filer</span><span class="sxs-lookup"><span data-stu-id="0e5ef-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="0e5ef-153">-VpnProtocol</span></span>
<span data-ttu-id="0e5ef-154">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-154">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e5ef-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0e5ef-155">-Confirm</span></span>
<span data-ttu-id="0e5ef-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e5ef-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e5ef-157">-WhatIf</span></span>
<span data-ttu-id="0e5ef-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e5ef-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e5ef-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e5ef-160">CommonParameters</span></span>
<span data-ttu-id="0e5ef-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e5ef-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e5ef-162">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e5ef-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e5ef-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0e5ef-163">INPUTS</span></span>

### <span data-ttu-id="0e5ef-164">Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="0e5ef-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="0e5ef-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0e5ef-165">OUTPUTS</span></span>

### <span data-ttu-id="0e5ef-166">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e5ef-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="0e5ef-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0e5ef-167">NOTES</span></span>

## <span data-ttu-id="0e5ef-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0e5ef-168">RELATED LINKS</span></span>
