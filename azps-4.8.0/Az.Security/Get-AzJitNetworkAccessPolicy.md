---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: c385ca902764d6bf9afa3808d718c2ceb5d1357c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261710"
---
# <span data-ttu-id="84d43-101">Get-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84d43-101">Get-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="84d43-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="84d43-102">SYNOPSIS</span></span>
<span data-ttu-id="84d43-103">Hämtar principer för JIT-nätverks åtkomst</span><span class="sxs-lookup"><span data-stu-id="84d43-103">Gets the JIT network access policies</span></span>

## <span data-ttu-id="84d43-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="84d43-104">SYNTAX</span></span>

### <span data-ttu-id="84d43-105">SubscriptionScope (standard)</span><span class="sxs-lookup"><span data-stu-id="84d43-105">SubscriptionScope (Default)</span></span>
```
Get-AzJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84d43-106">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="84d43-106">ResourceGroupScope</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84d43-107">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="84d43-107">ResourceGroupLevelResource</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84d43-108">ID</span><span class="sxs-lookup"><span data-stu-id="84d43-108">ResourceId</span></span>
```
Get-AzJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84d43-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="84d43-109">DESCRIPTION</span></span>
<span data-ttu-id="84d43-110">Med för nätverks åtkomst principer (JIT) kan du definiera en princip som gör det möjligt för enkla användare att skapa en tillfällig nätverks anslutning till en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="84d43-110">Just In Time (JIT) network access policies let you define a policy the will allow simple users to create a temporary network connection to a VM.</span></span>
<span data-ttu-id="84d43-111">Principen definierar vilka portar, protokoll-och käll-IP-adresser som kan begära en anslutning till en virtuell dator och maximal varaktighet innan anslutningen stängs automatiskt.</span><span class="sxs-lookup"><span data-stu-id="84d43-111">The policy defines what ports, protocol and source IP addresses can request a connection to a VM and the max duration before the connection will be closed automatically.</span></span>
<span data-ttu-id="84d43-112">I principen kan du även se anslutningsbegäran som har gjorts med den här principen.</span><span class="sxs-lookup"><span data-stu-id="84d43-112">In the policy you can also see the connection request that were made with this policy.</span></span> 

## <span data-ttu-id="84d43-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="84d43-113">EXAMPLES</span></span>

### <span data-ttu-id="84d43-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="84d43-114">Example 1</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="84d43-115">Få alla åtkomst principer för JIT-nätverk för en prenumeration</span><span class="sxs-lookup"><span data-stu-id="84d43-115">Get all the JIT network access polices on a subscription</span></span>

### <span data-ttu-id="84d43-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="84d43-116">Example 2</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="84d43-117">Få alla åtkomst principer för JIT-nätverk i resurs gruppen "myService1"</span><span class="sxs-lookup"><span data-stu-id="84d43-117">Get all the JIT network access polices on the "myService1" resource group</span></span>

### <span data-ttu-id="84d43-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="84d43-118">Example 3</span></span>
```powershell
PS C:\> Get-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

<span data-ttu-id="84d43-119">Hämtar en specifik policy för JIT-nätverks åtkomst</span><span class="sxs-lookup"><span data-stu-id="84d43-119">Gets a specific JIT network access policy</span></span>

## <span data-ttu-id="84d43-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="84d43-120">PARAMETERS</span></span>

### <span data-ttu-id="84d43-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84d43-121">-DefaultProfile</span></span>
<span data-ttu-id="84d43-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="84d43-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84d43-123">-Plats</span><span class="sxs-lookup"><span data-stu-id="84d43-123">-Location</span></span>
<span data-ttu-id="84d43-124">Plats.</span><span class="sxs-lookup"><span data-stu-id="84d43-124">Location.</span></span>

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

### <span data-ttu-id="84d43-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="84d43-125">-Name</span></span>
<span data-ttu-id="84d43-126">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="84d43-126">Resource name.</span></span>

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

### <span data-ttu-id="84d43-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84d43-127">-ResourceGroupName</span></span>
<span data-ttu-id="84d43-128">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="84d43-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84d43-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84d43-129">-ResourceId</span></span>
<span data-ttu-id="84d43-130">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="84d43-130">Resource ID.</span></span>

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

### <span data-ttu-id="84d43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84d43-131">CommonParameters</span></span>
<span data-ttu-id="84d43-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84d43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84d43-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84d43-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84d43-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="84d43-134">INPUTS</span></span>

### <span data-ttu-id="84d43-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84d43-135">System.String</span></span>

## <span data-ttu-id="84d43-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="84d43-136">OUTPUTS</span></span>

### <span data-ttu-id="84d43-137">Microsoft. Azure. commands. Security. Models. JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="84d43-137">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="84d43-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="84d43-138">NOTES</span></span>

## <span data-ttu-id="84d43-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="84d43-139">RELATED LINKS</span></span>
