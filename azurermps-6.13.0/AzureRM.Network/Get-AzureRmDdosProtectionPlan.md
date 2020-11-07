---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756673"
---
# <span data-ttu-id="c8e9b-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="c8e9b-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="c8e9b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c8e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e9b-103">Får ett DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8e9b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c8e9b-104">SYNTAX</span></span>

### <span data-ttu-id="c8e9b-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="c8e9b-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8e9b-106">Förteckning</span><span class="sxs-lookup"><span data-stu-id="c8e9b-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8e9b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c8e9b-107">DESCRIPTION</span></span>
<span data-ttu-id="c8e9b-108">Get-AzureRmDdosProtectionPlan cmdlet får ett skydds abonnemang för DDoS.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="c8e9b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c8e9b-109">EXAMPLES</span></span>

### <span data-ttu-id="c8e9b-110">Exempel 1: skaffa ett specifikt DDoS skydds abonnemang</span><span class="sxs-lookup"><span data-stu-id="c8e9b-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="c8e9b-111">I det här fallet måste vi ange både **ResourceGroupName** och **namnattribut** som motsvarar resurs gruppen och namnet på DDoS-skydds planen.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="c8e9b-112">Exempel 2: Hämta alla DDoS skydds planer i en resurs grupp</span><span class="sxs-lookup"><span data-stu-id="c8e9b-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="c8e9b-113">I det här scenariot anger vi bara parametern **ResourceGroupName** för att få en lista över DDoS skydds planer.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="c8e9b-114">Exempel 2: Hämta alla DDoS skydds planer i ett abonnemang</span><span class="sxs-lookup"><span data-stu-id="c8e9b-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="c8e9b-115">Här anger vi inga parametrar för att få en lista över alla DDoS skydds planer i ett abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="c8e9b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c8e9b-116">PARAMETERS</span></span>

### <span data-ttu-id="c8e9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e9b-117">-DefaultProfile</span></span>
<span data-ttu-id="c8e9b-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8e9b-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c8e9b-119">-Name</span></span>
<span data-ttu-id="c8e9b-120">Anger namnet på DDoS skydds plan.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e9b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e9b-121">-ResourceGroupName</span></span>
<span data-ttu-id="c8e9b-122">Anger namnet på resurs gruppen för DDoS skydds abonnemang.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8e9b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e9b-123">CommonParameters</span></span>
<span data-ttu-id="c8e9b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8e9b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e9b-125">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8e9b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e9b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c8e9b-126">INPUTS</span></span>

### <span data-ttu-id="c8e9b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c8e9b-127">System.String</span></span>

## <span data-ttu-id="c8e9b-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c8e9b-128">OUTPUTS</span></span>

### <span data-ttu-id="c8e9b-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="c8e9b-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="c8e9b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c8e9b-130">NOTES</span></span>

## <span data-ttu-id="c8e9b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c8e9b-131">RELATED LINKS</span></span>

[<span data-ttu-id="c8e9b-132">New-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="c8e9b-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="c8e9b-133">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="c8e9b-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="c8e9b-134">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8e9b-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c8e9b-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8e9b-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c8e9b-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c8e9b-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
