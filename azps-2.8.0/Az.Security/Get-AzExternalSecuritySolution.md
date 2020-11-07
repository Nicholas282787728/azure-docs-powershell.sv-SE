---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzExternalSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzExternalSecuritySolution.md
ms.openlocfilehash: cf06d1cce2e37f69ce06576a659dbfa989ca56b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93919248"
---
# <span data-ttu-id="a9b7e-101">Get-AzExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a9b7e-101">Get-AzExternalSecuritySolution</span></span>

## <span data-ttu-id="a9b7e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b7e-103">Skaffa extern säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="a9b7e-103">Get external security solution</span></span> 

## <span data-ttu-id="a9b7e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9b7e-104">SYNTAX</span></span>

### <span data-ttu-id="a9b7e-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="a9b7e-105">SubscriptionScope (Default)</span></span>
```
Get-AzExternalSecuritySolution [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9b7e-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="a9b7e-106">ResourceGroupLevelResource</span></span>
```
Get-AzExternalSecuritySolution -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9b7e-107">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="a9b7e-107">SubscriptionLevelResource</span></span>
```
Get-AzExternalSecuritySolution -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9b7e-108">ID</span><span class="sxs-lookup"><span data-stu-id="a9b7e-108">ResourceId</span></span>
```
Get-AzExternalSecuritySolution -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9b7e-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9b7e-109">DESCRIPTION</span></span>
<span data-ttu-id="a9b7e-110">Skaffa extern säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="a9b7e-110">Get external security solution</span></span>

## <span data-ttu-id="a9b7e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9b7e-111">EXAMPLES</span></span>

### <span data-ttu-id="a9b7e-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9b7e-112">Example 1</span></span>
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

<span data-ttu-id="a9b7e-113">Få alla externa säkerhetslösningar i abonnemanget</span><span class="sxs-lookup"><span data-stu-id="a9b7e-113">Get all the external security solutions in the subscription</span></span>

### <span data-ttu-id="a9b7e-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a9b7e-114">Example 2</span></span>
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

<span data-ttu-id="a9b7e-115">Skaffa en specifik extern säkerhets lösning</span><span class="sxs-lookup"><span data-stu-id="a9b7e-115">Get a specific external security solution</span></span>

## <span data-ttu-id="a9b7e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9b7e-116">PARAMETERS</span></span>

### <span data-ttu-id="a9b7e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b7e-117">-DefaultProfile</span></span>
<span data-ttu-id="a9b7e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9b7e-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="a9b7e-119">-Location</span></span>
<span data-ttu-id="a9b7e-120">Plats.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-120">Location.</span></span>

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

### <span data-ttu-id="a9b7e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9b7e-121">-Name</span></span>
<span data-ttu-id="a9b7e-122">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-122">Resource name.</span></span>

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

### <span data-ttu-id="a9b7e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b7e-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9b7e-124">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-124">Resource group name.</span></span>

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

### <span data-ttu-id="a9b7e-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9b7e-125">-ResourceId</span></span>
<span data-ttu-id="a9b7e-126">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-126">Resource ID.</span></span>

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

### <span data-ttu-id="a9b7e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b7e-127">CommonParameters</span></span>
<span data-ttu-id="a9b7e-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9b7e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b7e-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9b7e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b7e-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9b7e-130">INPUTS</span></span>

### <span data-ttu-id="a9b7e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a9b7e-131">System.String</span></span>

## <span data-ttu-id="a9b7e-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9b7e-132">OUTPUTS</span></span>

### <span data-ttu-id="a9b7e-133">Microsoft. Azure. commands. Security. Models. ExternalSecuritySolutions. PSSecurityExternalSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="a9b7e-133">Microsoft.Azure.Commands.Security.Models.ExternalSecuritySolutions.PSSecurityExternalSecuritySolution</span></span>

## <span data-ttu-id="a9b7e-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9b7e-134">NOTES</span></span>

## <span data-ttu-id="a9b7e-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9b7e-135">RELATED LINKS</span></span>
