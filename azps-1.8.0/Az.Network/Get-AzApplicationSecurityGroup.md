---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationSecurityGroup.md
ms.openlocfilehash: 58bae669af1fb9a06f4caa95070225f12d1a78aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93748347"
---
# <span data-ttu-id="46fdc-101">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="46fdc-101">Get-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="46fdc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="46fdc-102">SYNOPSIS</span></span>
<span data-ttu-id="46fdc-103">Hämtar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="46fdc-103">Gets an application security group.</span></span>

## <span data-ttu-id="46fdc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="46fdc-104">SYNTAX</span></span>

```
Get-AzApplicationSecurityGroup [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46fdc-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="46fdc-105">DESCRIPTION</span></span>
<span data-ttu-id="46fdc-106">Cmdleten **Get-AzApplicationSecurityGroup** hämtar en säkerhets grupp för program.</span><span class="sxs-lookup"><span data-stu-id="46fdc-106">The **Get-AzApplicationSecurityGroup** cmdlet gets an application security group.</span></span>

## <span data-ttu-id="46fdc-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="46fdc-107">EXAMPLES</span></span>

### <span data-ttu-id="46fdc-108">Exempel 1: Hämta alla program säkerhets grupper.</span><span class="sxs-lookup"><span data-stu-id="46fdc-108">Example 1: Retrieve all application security groups.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="46fdc-109">Kommandot returnerar alla program säkerhets grupper i prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="46fdc-109">The command above returns the all application security groups in the subscription.</span></span>

### <span data-ttu-id="46fdc-110">Exempel 2: Hämta säkerhets grupper för program i en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="46fdc-110">Example 2: Retrieve application security groups in a resource group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="46fdc-111">Kommandot returnerar alla program säkerhets grupper som tillhör resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46fdc-111">The command above returns all application security groups that belong to the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="46fdc-112">Exempel 3: Hämta en specifik program säkerhets grupp.</span><span class="sxs-lookup"><span data-stu-id="46fdc-112">Example 3: Retrieve a specific application security group.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -ResourceGroupName MyResourceGroup -Name MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1
```

<span data-ttu-id="46fdc-113">I ovanstående kommando returneras program säkerhets gruppen MyApplicationSecurityGroup under resurs gruppen MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46fdc-113">The command above returns the application security group MyApplicationSecurityGroup under the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="46fdc-114">Exempel 4: Hämta säkerhets grupper för program med hjälp av filtrering.</span><span class="sxs-lookup"><span data-stu-id="46fdc-114">Example 4: Retrieve application security groups using filtering.</span></span>
```
PS C:\> Get-AzApplicationSecurityGroup -Name MyApplicationSecurityGroup*

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup1
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup1

ProvisioningState : Succeeded
ResourceGroupName : MyResourceGroup
Location          : southcentralus
ResourceGuid      :
Type              : Microsoft.Network/applicationSecurityGroups
Tag               : {}
TagsTable         :
Name              : MyApplicationSecurityGroup2
Etag              : W/"00000000-0000-0000-0000-000000000000"
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/Microsof
                    t.Network/applicationSecurityGroups/MyApplicationSecurityGroup2
```

<span data-ttu-id="46fdc-115">Kommandot returnerar alla program säkerhets grupper som börjar med "MyApplicationSecurityGroup".</span><span class="sxs-lookup"><span data-stu-id="46fdc-115">The command above returns all application security groups that start with "MyApplicationSecurityGroup".</span></span>

## <span data-ttu-id="46fdc-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="46fdc-116">PARAMETERS</span></span>

### <span data-ttu-id="46fdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46fdc-117">-DefaultProfile</span></span>
<span data-ttu-id="46fdc-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="46fdc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46fdc-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="46fdc-119">-Name</span></span>
<span data-ttu-id="46fdc-120">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="46fdc-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="46fdc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46fdc-121">-ResourceGroupName</span></span>
<span data-ttu-id="46fdc-122">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="46fdc-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="46fdc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fdc-123">CommonParameters</span></span>
<span data-ttu-id="46fdc-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46fdc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fdc-125">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46fdc-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fdc-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="46fdc-126">INPUTS</span></span>

### <span data-ttu-id="46fdc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="46fdc-127">System.String</span></span>

## <span data-ttu-id="46fdc-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="46fdc-128">OUTPUTS</span></span>

### <span data-ttu-id="46fdc-129">Microsoft. Azure. commands. Networks. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="46fdc-129">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="46fdc-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="46fdc-130">NOTES</span></span>

## <span data-ttu-id="46fdc-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="46fdc-131">RELATED LINKS</span></span>

[<span data-ttu-id="46fdc-132">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="46fdc-132">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="46fdc-133">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="46fdc-133">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="46fdc-134">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46fdc-134">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="46fdc-135">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="46fdc-135">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)