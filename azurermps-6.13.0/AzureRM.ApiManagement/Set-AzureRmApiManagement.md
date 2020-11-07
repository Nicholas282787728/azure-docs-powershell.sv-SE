---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756729"
---
# <span data-ttu-id="05a63-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="05a63-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="05a63-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="05a63-102">SYNOPSIS</span></span>
<span data-ttu-id="05a63-103">Uppdaterar en Azure API Management-tjänst</span><span class="sxs-lookup"><span data-stu-id="05a63-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05a63-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="05a63-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a63-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="05a63-105">DESCRIPTION</span></span>

<span data-ttu-id="05a63-106">Cmdleten **set-AzureRmApiManagement** uppdaterar en Azure API Management Service.</span><span class="sxs-lookup"><span data-stu-id="05a63-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="05a63-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="05a63-107">EXAMPLES</span></span>

### <span data-ttu-id="05a63-108">Exempel 1 skaffa en API-hanterings tjänst och utöka den till Premium och lägga till en region</span><span class="sxs-lookup"><span data-stu-id="05a63-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="05a63-109">Det här exemplet får en API-hanterings instans, ändrar den till fem premie enheter och lägger sedan till ytterligare tre enheter till Premium-området.</span><span class="sxs-lookup"><span data-stu-id="05a63-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="05a63-110">Exempel 2: uppdaterings distribution (externt virtuellt nätverk)</span><span class="sxs-lookup"><span data-stu-id="05a63-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="05a63-111">Det här kommandot uppdaterar en befintlig API-distribution och ansluter till en extern *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="05a63-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="05a63-112">Exempel 3: skapa och initiera en instans av PsApiManagementCustomHostNameConfiguration med en hemlighet från en nyckel valv resurs</span><span class="sxs-lookup"><span data-stu-id="05a63-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="05a63-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="05a63-113">PARAMETERS</span></span>

### <span data-ttu-id="05a63-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05a63-114">-AsJob</span></span>
<span data-ttu-id="05a63-115">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="05a63-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05a63-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="05a63-116">-AssignIdentity</span></span>
<span data-ttu-id="05a63-117">Skapa och tilldela en Azure Active Directory-identitet för den här servern för användning med Key Management Services, till exempel Azure-valv.</span><span class="sxs-lookup"><span data-stu-id="05a63-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="05a63-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a63-118">-DefaultProfile</span></span>
<span data-ttu-id="05a63-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="05a63-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05a63-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05a63-120">-InputObject</span></span>
<span data-ttu-id="05a63-121">ApiManagement-instansen.</span><span class="sxs-lookup"><span data-stu-id="05a63-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="05a63-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05a63-122">-PassThru</span></span>
<span data-ttu-id="05a63-123">Skickar uppdaterade PsApiManagement till pipeline om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="05a63-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="05a63-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="05a63-124">-Confirm</span></span>
<span data-ttu-id="05a63-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="05a63-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a63-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a63-126">-WhatIf</span></span>
<span data-ttu-id="05a63-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="05a63-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05a63-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="05a63-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a63-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a63-129">CommonParameters</span></span>
<span data-ttu-id="05a63-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a63-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a63-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a63-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a63-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="05a63-132">INPUTS</span></span>

### <span data-ttu-id="05a63-133">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="05a63-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="05a63-134">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="05a63-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="05a63-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="05a63-135">OUTPUTS</span></span>

### <span data-ttu-id="05a63-136">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="05a63-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="05a63-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="05a63-137">NOTES</span></span>

## <span data-ttu-id="05a63-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="05a63-138">RELATED LINKS</span></span>

[<span data-ttu-id="05a63-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="05a63-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="05a63-140">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="05a63-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="05a63-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="05a63-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
