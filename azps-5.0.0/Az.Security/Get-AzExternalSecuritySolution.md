---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: 0314a7e6b661b0b007ffe2cf59f5618247e4b282
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324275"
---
# <span data-ttu-id="d3576-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d3576-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="d3576-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3576-102">SYNOPSIS</span></span>
<span data-ttu-id="d3576-103">Skaffa extern säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="d3576-103">Get external security solution</span></span> 

## <span data-ttu-id="d3576-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3576-104">SYNTAX</span></span>

### <span data-ttu-id="d3576-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="d3576-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3576-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="d3576-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3576-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="d3576-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3576-108">ID</span><span class="sxs-lookup"><span data-stu-id="d3576-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3576-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3576-109">DESCRIPTION</span></span>
<span data-ttu-id="d3576-110">Skaffa extern säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="d3576-110">Get external security solution</span></span>

## <span data-ttu-id="d3576-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3576-111">EXAMPLES</span></span>

### <span data-ttu-id="d3576-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d3576-112">Example 1</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-eus/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-e
                    us
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-eus/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-eus
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-eus
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/defaultresourcegroup-weu/provide
                    rs/microsoft.operationalinsights/workspaces/defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-w
                    eu
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/defaultresourcegroup-weu/provide
                    rs/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_defaultworkspace-487bb485-b
                    5b0-471e-9c0d-10717612f869-weu
Name              : aad_defaultworkspace-487bb485-b5b0-471e-9c0d-10717612f869-weu
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.opera
                    tionalinsights/workspaces/securityuserws
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/mainws/providers/Microsoft.Secur
                    ity/locations/centralus/externalSecuritySolutions/aad_securityuserws
Name              : aad_securityuserws
Kind              : AAD

ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.o
                    perationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.S
                    ecurity/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="d3576-113">Få alla externa säkerhetslösningar i abonnemanget</span><span class="sxs-lookup"><span data-stu-id="d3576-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="d3576-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d3576-114">Example 2</span></span>
```powershell
PS C:\> Get-AzExternalSecuritySolution -ResourceGroupName "myservice1" -Location "centralus" -Name "aad_testservicews"
ConnectivityState : Discovered
DeviceType        : Azure Active Directory Identity Protection
DeviceVendor      : microsoft
Workspace         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/myservice1/providers/microsoft.operationalinsights/workspaces/testservicews
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myservice1/providers/Microsoft.Security/locations/centralus/externalSecuritySolutions/aad_testservicews
Name              : aad_testservicews
Kind              : AAD
```

<span data-ttu-id="d3576-115">Skaffa en specifik extern säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="d3576-115">Get a specific external security solution</span></span>

## <span data-ttu-id="d3576-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3576-116">PARAMETERS</span></span>

### <span data-ttu-id="d3576-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3576-117">-DefaultProfile</span></span>
<span data-ttu-id="d3576-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3576-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3576-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="d3576-119">-Location</span></span>
<span data-ttu-id="d3576-120">Plats.</span><span class="sxs-lookup"><span data-stu-id="d3576-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3576-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3576-121">-Name</span></span>
<span data-ttu-id="d3576-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d3576-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3576-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3576-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3576-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="d3576-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3576-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3576-125">-ResourceId</span></span>
<span data-ttu-id="d3576-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="d3576-126">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3576-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3576-127">CommonParameters</span></span>
<span data-ttu-id="d3576-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3576-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3576-129">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3576-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3576-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3576-130">INPUTS</span></span>

### <span data-ttu-id="d3576-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3576-131">System.String</span></span>

## <span data-ttu-id="d3576-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3576-132">OUTPUTS</span></span>

### <span data-ttu-id="d3576-133">Microsoft. Azure. commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="d3576-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="d3576-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3576-134">NOTES</span></span>

## <span data-ttu-id="d3576-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3576-135">RELATED LINKS</span></span>