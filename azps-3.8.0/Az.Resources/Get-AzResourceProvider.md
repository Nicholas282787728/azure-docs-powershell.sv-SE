---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 0f7a05cd0cd711388973c3f823b1aee6aa9f6902
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089752"
---
# <span data-ttu-id="425f0-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="425f0-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="425f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="425f0-102">SYNOPSIS</span></span>
<span data-ttu-id="425f0-103">Får en resurs leverantör.</span><span class="sxs-lookup"><span data-stu-id="425f0-103">Gets a resource provider.</span></span>

## <span data-ttu-id="425f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="425f0-104">SYNTAX</span></span>

### <span data-ttu-id="425f0-105">ListAvailable (standard)</span><span class="sxs-lookup"><span data-stu-id="425f0-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="425f0-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="425f0-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="425f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="425f0-107">DESCRIPTION</span></span>
<span data-ttu-id="425f0-108">Cmdleten **Get-AzResourceProvider** får en Azure Resource-leverantör.</span><span class="sxs-lookup"><span data-stu-id="425f0-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="425f0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="425f0-109">EXAMPLES</span></span>

### <span data-ttu-id="425f0-110">Exempel 1: få alla resurs leverantörer registrerade med nuvarande abonnemang</span><span class="sxs-lookup"><span data-stu-id="425f0-110">Example 1: Get all resource providers registered with the current subscription</span></span>

```powershell
PS C:\>Get-AzResourceProvider

ProviderNamespace : Microsoft.AppConfiguration
RegistrationState : Registered
ResourceTypes     : {configurationStores, configurationStores/eventGridFilters, checkNameAvailability, locations…}
Locations         : {West Central US, Central US, West US, East US…}

ProviderNamespace : Microsoft.KeyVault
RegistrationState : Registered
ResourceTypes     : {vaults, vaults/secrets, vaults/accessPolicies, operations…}
Locations         : {North Central US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks, publicIPAddresses, networkInterfaces, privateEndpoints…}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets, virtualMachines, virtualMachines/extensions, virtualMachineScaleSets…}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Security
RegistrationState : Registered
ResourceTypes     : {operations, securityStatuses, tasks, regulatoryComplianceStandards…}
Locations         : {Central US, East US, West Europe, West Central US…}

ProviderNamespace : Microsoft.ResourceHealth
RegistrationState : Registered
ResourceTypes     : {availabilityStatuses, childAvailabilityStatuses, childResources, events…}
Locations         : {Australia Southeast}

ProviderNamespace : Microsoft.PolicyInsights
RegistrationState : Registered
ResourceTypes     : {policyEvents, policyStates, operations, asyncOperationResults…}
Locations         : {}

ProviderNamespace : Microsoft.Storage
RegistrationState : Registered
ResourceTypes     : {storageAccounts, operations, locations/asyncoperations, storageAccounts/listAccountSas…}
Locations         : {East US, East US 2, West US, West Europe…}

ProviderNamespace : Microsoft.Web
RegistrationState : Registered
ResourceTypes     : {publishingUsers, ishostnameavailable, validate, isusernameavailable…}
Locations         : {Central US, North Europe, West Europe, Southeast Asia…}

ProviderNamespace : Sendgrid.Email
RegistrationState : Registered
ResourceTypes     : {accounts, operations}
Locations         : {Australia East, Australia Southeast, Brazil South, Canada Central…}

ProviderNamespace : Microsoft.Authorization
RegistrationState : Registered
ResourceTypes     : {roleAssignments, roleDefinitions, classicAdministrators, permissions…}
Locations         : {}
...
```

<span data-ttu-id="425f0-111">Det här kommandot får alla resurs leverantörer från abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="425f0-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="425f0-112">Exempel 2: Hämta alla resurstilldelnings uppgifter från angiven ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="425f0-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/networkInterfaces}
Locations         : {East US, East US 2, West US, Central US…}
...
```

<span data-ttu-id="425f0-113">Det här kommandot får alla resurs leverantörer under "Microsoft. Compute".</span><span class="sxs-lookup"><span data-stu-id="425f0-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="425f0-114">Exempel 3: Hämta alla resursinformation från den angivna ProviderNamespace-matrisen</span><span class="sxs-lookup"><span data-stu-id="425f0-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute,Microsoft.Network
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}
...

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {publicIPAddresses}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkInterfaces}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpoints}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpointRedirectMaps}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {loadBalancers}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkSecurityGroups}
Locations         : {West US, East US, North Europe, West Europe…}
...
```

<span data-ttu-id="425f0-115">Det här kommandot får alla resurs leverantörer under "Microsoft. Compute" och "Microsoft. Network".</span><span class="sxs-lookup"><span data-stu-id="425f0-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="425f0-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="425f0-116">PARAMETERS</span></span>

### <span data-ttu-id="425f0-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="425f0-117">-ApiVersion</span></span>
<span data-ttu-id="425f0-118">Anger den API-version som stöds av resurs leverantören.</span><span class="sxs-lookup"><span data-stu-id="425f0-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="425f0-119">Du kan ange en annan version än standard versionen.</span><span class="sxs-lookup"><span data-stu-id="425f0-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="425f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425f0-120">-DefaultProfile</span></span>
<span data-ttu-id="425f0-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="425f0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="425f0-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="425f0-122">-ListAvailable</span></span>
<span data-ttu-id="425f0-123">Indikerar att den här åtgärden får alla tillgängliga resurs leverantörer.</span><span class="sxs-lookup"><span data-stu-id="425f0-123">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="425f0-124">-Plats</span><span class="sxs-lookup"><span data-stu-id="425f0-124">-Location</span></span>
<span data-ttu-id="425f0-125">Anger resurs leverantörens plats.</span><span class="sxs-lookup"><span data-stu-id="425f0-125">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="425f0-126">-För</span><span class="sxs-lookup"><span data-stu-id="425f0-126">-Pre</span></span>
<span data-ttu-id="425f0-127">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="425f0-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="425f0-128">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="425f0-128">-ProviderNamespace</span></span>
<span data-ttu-id="425f0-129">Anger resurs leverantörens namn område.</span><span class="sxs-lookup"><span data-stu-id="425f0-129">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="425f0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425f0-130">CommonParameters</span></span>
<span data-ttu-id="425f0-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425f0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425f0-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="425f0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425f0-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="425f0-133">INPUTS</span></span>

### <span data-ttu-id="425f0-134">System. string []</span><span class="sxs-lookup"><span data-stu-id="425f0-134">System.String[]</span></span>

## <span data-ttu-id="425f0-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="425f0-135">OUTPUTS</span></span>

### <span data-ttu-id="425f0-136">Microsoft. Azure. kommandon. ResourceManager. cmdlets. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="425f0-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="425f0-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="425f0-137">NOTES</span></span>

## <span data-ttu-id="425f0-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="425f0-138">RELATED LINKS</span></span>

[<span data-ttu-id="425f0-139">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="425f0-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="425f0-140">Avregistrera-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="425f0-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)

