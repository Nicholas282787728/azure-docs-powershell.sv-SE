---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkProfile.md
ms.openlocfilehash: 4b96ec4fb263d262419d1c545cd9b1f0c35da413
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323862"
---
# <span data-ttu-id="f8f92-101">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8f92-101">Get-AzNetworkProfile</span></span>

## <span data-ttu-id="f8f92-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f8f92-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f92-103">Hämtar en befintlig nätverks profil på toppnivå resursen</span><span class="sxs-lookup"><span data-stu-id="f8f92-103">Gets an existing network profile top level resource</span></span>

## <span data-ttu-id="f8f92-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f8f92-104">SYNTAX</span></span>

### <span data-ttu-id="f8f92-105">GetByResourceNameNoExpandParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="f8f92-105">GetByResourceNameNoExpandParameterSet (Default)</span></span>
```
Get-AzNetworkProfile [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8f92-106">GetByResourceNameExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8f92-106">GetByResourceNameExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f92-107">GetByResourceIdExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8f92-107">GetByResourceIdExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8f92-108">GetByResourceIdNoExpandParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8f92-108">GetByResourceIdNoExpandParameterSet</span></span>
```
Get-AzNetworkProfile -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f92-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f8f92-109">DESCRIPTION</span></span>
<span data-ttu-id="f8f92-110">Cmdleten **Get-AzNetworkProfile** hämtar en befintlig nätverks profil på toppnivå resursen</span><span class="sxs-lookup"><span data-stu-id="f8f92-110">The **Get-AzNetworkProfile** cmdlet retrieves an existing network profile top level resource</span></span>

## <span data-ttu-id="f8f92-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f8f92-111">EXAMPLES</span></span>

### <span data-ttu-id="f8f92-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f8f92-112">Example 1</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np1 -ResourceGroupName rg1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1
```

<span data-ttu-id="f8f92-113">Då hämtas nätverks profil NP1 i resurs gruppen RG1</span><span class="sxs-lookup"><span data-stu-id="f8f92-113">This retrieves the network profile np1 in resource group rg1</span></span>

### <span data-ttu-id="f8f92-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f8f92-114">Example 2</span></span>
```powershell
$networkProfile = Get-AzNetworkProfile -Name np*

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np1
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np1

ProvisioningState                           : Succeeded
ContainerNetworkInterfaces                  : {}
ContainerNetworkInterfaceConfigurations     : {}
ContainerNetworkInterfacesText              : []
ContainerNetworkInterfaceConfigurationsText : []
ResourceGroupName                           : rg1
Location                                    : westus
ResourceGuid                                : 00000000-0000-0000-0000-000000000000
Type                                        : Microsoft.Network/networkProfiles
Tag                                         :
TagsTable                                   :
Name                                        : np2
Etag                                        : W/"00000000-0000-0000-0000-000000000000"
Id                                          : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1
                                              /providers/Microsoft.Network/networkProfiles/np2
```

<span data-ttu-id="f8f92-115">Då hämtas nätverks profilerna som börjar med "NP"</span><span class="sxs-lookup"><span data-stu-id="f8f92-115">This retrieves the network profiles that start with "np"</span></span>

## <span data-ttu-id="f8f92-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f8f92-116">PARAMETERS</span></span>

### <span data-ttu-id="f8f92-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f92-117">-DefaultProfile</span></span>
<span data-ttu-id="f8f92-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f8f92-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8f92-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f8f92-119">-ExpandResource</span></span>
<span data-ttu-id="f8f92-120">Resurs referensen som ska expanderas.</span><span class="sxs-lookup"><span data-stu-id="f8f92-120">The resource reference to be expanded.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet, GetByResourceIdExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f92-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="f8f92-121">-Name</span></span>
<span data-ttu-id="f8f92-122">Namnet på nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="f8f92-122">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f8f92-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f92-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8f92-124">Namnet på resurs gruppen för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="f8f92-124">The resource group name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceNameNoExpandParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: GetByResourceNameExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="f8f92-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8f92-125">-ResourceId</span></span>
<span data-ttu-id="f8f92-126">Azure Resource Manager-ID för nätverks profilen.</span><span class="sxs-lookup"><span data-stu-id="f8f92-126">The Azure resource manager id of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdExpandParameterSet, GetByResourceIdNoExpandParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8f92-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f92-127">CommonParameters</span></span>
<span data-ttu-id="f8f92-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f92-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f92-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8f92-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f92-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f8f92-130">INPUTS</span></span>

### <span data-ttu-id="f8f92-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f8f92-131">System.String</span></span>

## <span data-ttu-id="f8f92-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f8f92-132">OUTPUTS</span></span>

### <span data-ttu-id="f8f92-133">Microsoft. Azure. commands. Networks. Models. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8f92-133">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="f8f92-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f8f92-134">NOTES</span></span>

## <span data-ttu-id="f8f92-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f8f92-135">RELATED LINKS</span></span>

[<span data-ttu-id="f8f92-136">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8f92-136">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="f8f92-137">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8f92-137">Remove-AzNetworkProfile</span></span>](./Remove-AzNetworkProfile.md)

[<span data-ttu-id="f8f92-138">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="f8f92-138">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)