---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98527440"
---
# <span data-ttu-id="4ff82-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff82-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="4ff82-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ff82-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff82-103">Uppdaterar en befintlig VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ff82-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="4ff82-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ff82-104">SYNTAX</span></span>

### <span data-ttu-id="4ff82-105">ByVpnServerConfigurationNameByCertificateAuthentication (standard)</span><span class="sxs-lookup"><span data-stu-id="4ff82-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ff82-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ff82-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff82-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ff82-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ff82-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff82-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ff82-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ff82-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff82-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff82-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ff82-114">DESCRIPTION</span></span>
<span data-ttu-id="4ff82-115">Med cmdleten **Update-AzVpnServerConfiguration** kan du uppdatera de befintliga VpnServerConfiguration med olika VpnProtocols, VpnAuthenticationTypes, IpsecPolicies och ställa in valda parametrar för VPN-autentiseringstyp enligt kundens krav för att peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="4ff82-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="4ff82-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ff82-116">EXAMPLES</span></span>

### <span data-ttu-id="4ff82-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4ff82-117">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
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

<span data-ttu-id="4ff82-118">Kommandot ovan uppdaterar en befintlig VpnServerConfiguration med VpnProtocol som IkeV2.</span><span class="sxs-lookup"><span data-stu-id="4ff82-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="4ff82-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ff82-119">PARAMETERS</span></span>

### <span data-ttu-id="4ff82-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="4ff82-120">-AadAudience</span></span>
<span data-ttu-id="4ff82-121">AAD-Audience för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="4ff82-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="4ff82-122">-AadIssuer</span></span>
<span data-ttu-id="4ff82-123">AAD-utgivare för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="4ff82-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="4ff82-124">-AadTenant</span></span>
<span data-ttu-id="4ff82-125">AAD-klient för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="4ff82-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ff82-126">-AsJob</span></span>
<span data-ttu-id="4ff82-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4ff82-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ff82-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff82-128">-DefaultProfile</span></span>
<span data-ttu-id="4ff82-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ff82-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ff82-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ff82-130">-InputObject</span></span>
<span data-ttu-id="4ff82-131">VPN-serverns konfigurations objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="4ff82-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ff82-132">-Name</span></span>
<span data-ttu-id="4ff82-133">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="4ff82-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4ff82-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="4ff82-135">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="4ff82-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="4ff82-136">-RadiusServerAddress</span></span>
<span data-ttu-id="4ff82-137">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="4ff82-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="4ff82-138">-RadiusServerList</span></span>
<span data-ttu-id="4ff82-139">P2S externa flera RADIUS-servrar.</span><span class="sxs-lookup"><span data-stu-id="4ff82-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4ff82-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="4ff82-141">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="4ff82-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="4ff82-142">-RadiusServerSecret</span></span>
<span data-ttu-id="4ff82-143">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="4ff82-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff82-144">-ResourceGroupName</span></span>
<span data-ttu-id="4ff82-145">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="4ff82-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ff82-146">-ResourceId</span></span>
<span data-ttu-id="4ff82-147">Azure Resource ID för VPN-serverkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="4ff82-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-148">-Tagg</span><span class="sxs-lookup"><span data-stu-id="4ff82-148">-Tag</span></span>
<span data-ttu-id="4ff82-149">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="4ff82-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4ff82-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="4ff82-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="4ff82-151">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="4ff82-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="4ff82-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="4ff82-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="4ff82-153">En lista över IPSec-principer för VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4ff82-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4ff82-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="4ff82-155">En lista med VpnClientCertificates för att bli återkallat filer</span><span class="sxs-lookup"><span data-stu-id="4ff82-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4ff82-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="4ff82-157">En lista med VpnClientRootCertificates som ska läggas till i filer</span><span class="sxs-lookup"><span data-stu-id="4ff82-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff82-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="4ff82-158">-VpnProtocol</span></span>
<span data-ttu-id="4ff82-159">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="4ff82-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="4ff82-160">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ff82-160">-Confirm</span></span>
<span data-ttu-id="4ff82-161">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ff82-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff82-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff82-162">-WhatIf</span></span>
<span data-ttu-id="4ff82-163">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ff82-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ff82-164">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ff82-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff82-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff82-165">CommonParameters</span></span>
<span data-ttu-id="4ff82-166">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff82-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff82-167">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ff82-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff82-168">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ff82-168">INPUTS</span></span>

### <span data-ttu-id="4ff82-169">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff82-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="4ff82-170">System. String Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="4ff82-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="4ff82-171">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ff82-171">OUTPUTS</span></span>

### <span data-ttu-id="4ff82-172">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ff82-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="4ff82-173">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ff82-173">NOTES</span></span>

## <span data-ttu-id="4ff82-174">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ff82-174">RELATED LINKS</span></span>
