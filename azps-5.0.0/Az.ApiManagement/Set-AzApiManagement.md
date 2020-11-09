---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322721"
---
# <span data-ttu-id="d28b1-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d28b1-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="d28b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d28b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d28b1-103">Uppdaterar en Azure API Management-tjänst</span><span class="sxs-lookup"><span data-stu-id="d28b1-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="d28b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d28b1-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d28b1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d28b1-105">DESCRIPTION</span></span>

<span data-ttu-id="d28b1-106">Cmdleten **set-AzApiManagement** uppdaterar en Azure API Management Service.</span><span class="sxs-lookup"><span data-stu-id="d28b1-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="d28b1-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d28b1-107">EXAMPLES</span></span>

### <span data-ttu-id="d28b1-108">Exempel 1: skaffa en API-hanterings tjänst och utöka den till Premium och lägga till en region</span><span class="sxs-lookup"><span data-stu-id="d28b1-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="d28b1-109">Det här exemplet får en API-hanterings instans, ändrar den till fem premie enheter och lägger sedan till ytterligare tre enheter till Premium-området.</span><span class="sxs-lookup"><span data-stu-id="d28b1-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="d28b1-110">Exempel 2: uppdaterings distribution (externt virtuellt nätverk)</span><span class="sxs-lookup"><span data-stu-id="d28b1-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="d28b1-111">Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en extern *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="d28b1-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="d28b1-112">Exempel 3: skapa och initiera en instans av PsApiManagementCustomHostNameConfiguration med en hemlighet från en nyckel valv resurs</span><span class="sxs-lookup"><span data-stu-id="d28b1-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="d28b1-113">Exempel 4: uppdatera e-post i Publisher, NotificationSender e-post och organisations namn</span><span class="sxs-lookup"><span data-stu-id="d28b1-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="d28b1-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d28b1-114">PARAMETERS</span></span>

### <span data-ttu-id="d28b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d28b1-115">-AsJob</span></span>
<span data-ttu-id="d28b1-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d28b1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d28b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d28b1-117">-DefaultProfile</span></span>
<span data-ttu-id="d28b1-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d28b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d28b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d28b1-119">-InputObject</span></span>
<span data-ttu-id="d28b1-120">ApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="d28b1-120">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d28b1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d28b1-121">-PassThru</span></span>
<span data-ttu-id="d28b1-122">Skickar uppdaterade PsApiManagement till pipeline om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="d28b1-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="d28b1-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d28b1-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="d28b1-124">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="d28b1-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d28b1-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d28b1-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="d28b1-126">Tilldela användar identiteter till den här servern för användning med Key Management Services som Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="d28b1-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d28b1-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d28b1-127">-Confirm</span></span>
<span data-ttu-id="d28b1-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d28b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d28b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d28b1-129">-WhatIf</span></span>
<span data-ttu-id="d28b1-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d28b1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d28b1-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d28b1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d28b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d28b1-132">CommonParameters</span></span>
<span data-ttu-id="d28b1-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d28b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d28b1-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d28b1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d28b1-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d28b1-135">INPUTS</span></span>

### <span data-ttu-id="d28b1-136">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d28b1-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d28b1-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d28b1-137">OUTPUTS</span></span>

### <span data-ttu-id="d28b1-138">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="d28b1-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="d28b1-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d28b1-139">NOTES</span></span>

## <span data-ttu-id="d28b1-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d28b1-140">RELATED LINKS</span></span>

[<span data-ttu-id="d28b1-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d28b1-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="d28b1-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d28b1-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="d28b1-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="d28b1-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
