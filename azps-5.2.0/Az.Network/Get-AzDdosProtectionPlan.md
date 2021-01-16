---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98387669"
---
# <span data-ttu-id="95e84-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="95e84-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="95e84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95e84-102">SYNOPSIS</span></span>
<span data-ttu-id="95e84-103">Får ett DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="95e84-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="95e84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95e84-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95e84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95e84-105">DESCRIPTION</span></span>
<span data-ttu-id="95e84-106">Get-AzDdosProtectionPlan cmdlet får ett skydds abonnemang för DDoS.</span><span class="sxs-lookup"><span data-stu-id="95e84-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="95e84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95e84-107">EXAMPLES</span></span>

### <span data-ttu-id="95e84-108">Exempel 1: skaffa ett specifikt DDoS skydds abonnemang</span><span class="sxs-lookup"><span data-stu-id="95e84-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="95e84-109">I det här fallet måste vi ange både **ResourceGroupName** och **namnattribut** som motsvarar resurs gruppen och namnet på DDoS-skydds planen.</span><span class="sxs-lookup"><span data-stu-id="95e84-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="95e84-110">Exempel 2: Hämta alla DDoS skydds planer i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="95e84-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="95e84-111">I det här scenariot anger vi bara parametern **ResourceGroupName** för att få en lista över DDoS skydds planer.</span><span class="sxs-lookup"><span data-stu-id="95e84-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="95e84-112">Exempel 3: Hämta alla DDoS skydds planer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="95e84-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="95e84-113">Här anger vi inga parametrar för att få en lista över alla DDoS skydds planer i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="95e84-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="95e84-114">Exempel 4: Hämta alla DDoS skydds planer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="95e84-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="95e84-115">Denna cmdlet returnerar alla DdosProtectionPlans som börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="95e84-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="95e84-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95e84-116">PARAMETERS</span></span>

### <span data-ttu-id="95e84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e84-117">-DefaultProfile</span></span>
<span data-ttu-id="95e84-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95e84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95e84-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="95e84-119">-Name</span></span>
<span data-ttu-id="95e84-120">Anger namnet på DDoS skydds plan.</span><span class="sxs-lookup"><span data-stu-id="95e84-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="95e84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95e84-121">-ResourceGroupName</span></span>
<span data-ttu-id="95e84-122">Anger namnet på resurs gruppen för DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="95e84-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="95e84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e84-123">CommonParameters</span></span>
<span data-ttu-id="95e84-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95e84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e84-125">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95e84-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e84-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95e84-126">INPUTS</span></span>

### <span data-ttu-id="95e84-127">System. String</span><span class="sxs-lookup"><span data-stu-id="95e84-127">System.String</span></span>

## <span data-ttu-id="95e84-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95e84-128">OUTPUTS</span></span>

### <span data-ttu-id="95e84-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="95e84-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="95e84-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95e84-130">NOTES</span></span>

## <span data-ttu-id="95e84-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95e84-131">RELATED LINKS</span></span>

[<span data-ttu-id="95e84-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="95e84-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="95e84-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="95e84-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="95e84-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="95e84-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="95e84-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="95e84-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="95e84-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="95e84-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)