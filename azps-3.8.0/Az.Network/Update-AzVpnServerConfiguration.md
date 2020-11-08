---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 14f43ab66800969eb46554de898525ce8d687f5b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090937"
---
# <span data-ttu-id="d9633-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9633-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="d9633-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9633-102">SYNOPSIS</span></span>
<span data-ttu-id="d9633-103">Uppdaterar en befintlig VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9633-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="d9633-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9633-104">SYNTAX</span></span>

### <span data-ttu-id="d9633-105">ByVpnServerConfigurationNameByCertificateAuthentication (standard)</span><span class="sxs-lookup"><span data-stu-id="d9633-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9633-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9633-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9633-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9633-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9633-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9633-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9633-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9633-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="d9633-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9633-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9633-114">DESCRIPTION</span></span>
<span data-ttu-id="d9633-115">Med cmdleten **Update-AzVpnServerConfiguration** kan du uppdatera de befintliga VpnServerConfiguration med olika VpnProtocols, VpnAuthenticationTypes, IpsecPolicies och ställa in valda parametrar för VPN-autentiseringstyp enligt kundens krav för att peka på webbplats anslutningar.</span><span class="sxs-lookup"><span data-stu-id="d9633-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="d9633-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9633-116">EXAMPLES</span></span>

### <span data-ttu-id="d9633-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d9633-117">Example 1</span></span>
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

<span data-ttu-id="d9633-118">Kommandot ovan uppdaterar en befintlig VpnServerConfiguration med VpnProtocol som IkeV2.</span><span class="sxs-lookup"><span data-stu-id="d9633-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="d9633-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9633-119">PARAMETERS</span></span>

### <span data-ttu-id="d9633-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="d9633-120">-AadAudience</span></span>
<span data-ttu-id="d9633-121">AAD-Audience för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="d9633-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="d9633-122">-AadIssuer</span></span>
<span data-ttu-id="d9633-123">AAD-utgivare för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="d9633-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="d9633-124">-AadTenant</span></span>
<span data-ttu-id="d9633-125">AAD-klient för P2S AAD-verifikation.</span><span class="sxs-lookup"><span data-stu-id="d9633-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9633-126">-AsJob</span></span>
<span data-ttu-id="d9633-127">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d9633-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9633-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9633-128">-DefaultProfile</span></span>
<span data-ttu-id="d9633-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9633-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9633-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9633-130">-InputObject</span></span>
<span data-ttu-id="d9633-131">VPN-serverns konfigurations objekt som ska ändras</span><span class="sxs-lookup"><span data-stu-id="d9633-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="d9633-132">-Name</span></span>
<span data-ttu-id="d9633-133">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d9633-133">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d9633-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="d9633-135">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="d9633-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d9633-136">-RadiusServerAddress</span></span>
<span data-ttu-id="d9633-137">P2S externa RADIUS-serveradress.</span><span class="sxs-lookup"><span data-stu-id="d9633-137">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-138">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d9633-138">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="d9633-139">En lista över RadiusClientRootCertificate-filers sökvägar</span><span class="sxs-lookup"><span data-stu-id="d9633-139">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-140">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d9633-140">-RadiusServerSecret</span></span>
<span data-ttu-id="d9633-141">P2S externa RADIUS-server hemlighet.</span><span class="sxs-lookup"><span data-stu-id="d9633-141">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9633-142">-ResourceGroupName</span></span>
<span data-ttu-id="d9633-143">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="d9633-143">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-144">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9633-144">-ResourceId</span></span>
<span data-ttu-id="d9633-145">Azure Resource ID för VPN-serverkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="d9633-145">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-146">-Tagg</span><span class="sxs-lookup"><span data-stu-id="d9633-146">-Tag</span></span>
<span data-ttu-id="d9633-147">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="d9633-147">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d9633-148">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d9633-148">-VpnAuthenticationType</span></span>
<span data-ttu-id="d9633-149">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="d9633-149">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d9633-150">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d9633-150">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d9633-151">En lista över IPSec-principer för VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d9633-151">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-152">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d9633-152">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="d9633-153">En lista med VpnClientCertificates för att bli återkallat filer</span><span class="sxs-lookup"><span data-stu-id="d9633-153">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-154">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d9633-154">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="d9633-155">En lista med VpnClientRootCertificates som ska läggas till i filer</span><span class="sxs-lookup"><span data-stu-id="d9633-155">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9633-156">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="d9633-156">-VpnProtocol</span></span>
<span data-ttu-id="d9633-157">Listan med protokoll för P2S VPN-klienter.</span><span class="sxs-lookup"><span data-stu-id="d9633-157">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d9633-158">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9633-158">-Confirm</span></span>
<span data-ttu-id="d9633-159">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9633-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9633-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9633-160">-WhatIf</span></span>
<span data-ttu-id="d9633-161">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9633-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9633-162">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9633-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9633-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9633-163">CommonParameters</span></span>
<span data-ttu-id="d9633-164">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9633-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9633-165">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9633-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9633-166">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9633-166">INPUTS</span></span>

### <span data-ttu-id="d9633-167">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9633-167">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="d9633-168">System. String Microsoft. Azure. commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="d9633-168">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="d9633-169">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9633-169">OUTPUTS</span></span>

### <span data-ttu-id="d9633-170">Microsoft. Azure. commands. Networks. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d9633-170">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="d9633-171">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9633-171">NOTES</span></span>

## <span data-ttu-id="d9633-172">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9633-172">RELATED LINKS</span></span>
