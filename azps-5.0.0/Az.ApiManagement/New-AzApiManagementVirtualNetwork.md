---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementVirtualNetwork.md
ms.openlocfilehash: c7cf4783c7f374f16a51de9ac4794d5fef441e44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272964"
---
# <span data-ttu-id="b8ba8-101">New-AzApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8ba8-101">New-AzApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="b8ba8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ba8-103">Skapar en instans av PsApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="b8ba8-103">Creates an instance of PsApiManagementVirtualNetwork.</span></span>

## <span data-ttu-id="b8ba8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8ba8-104">SYNTAX</span></span>

```
New-AzApiManagementVirtualNetwork -SubnetResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8ba8-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="b8ba8-106">**New-AzApiManagementVirtualNetwork** cmdlet är ett hjälp kommando för att skapa en instans av **PsApiManagementVirtualNetwork**.</span><span class="sxs-lookup"><span data-stu-id="b8ba8-106">The **New-AzApiManagementVirtualNetwork** cmdlet is a helper command to create an instance of **PsApiManagementVirtualNetwork**.</span></span>
<span data-ttu-id="b8ba8-107">Det här kommandot används med cmdleten **set-AzApiManagement** och **New-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="b8ba8-107">This command is used with **Set-AzApiManagement** and **New-AzApiManagement** cmdlet.</span></span>

## <span data-ttu-id="b8ba8-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8ba8-108">EXAMPLES</span></span>

### <span data-ttu-id="b8ba8-109">Exempel 1: skapa ett virtuellt nätverk och uppdatera en befintlig APIM-tjänst till VNET</span><span class="sxs-lookup"><span data-stu-id="b8ba8-109">Example 1: Create a virtual network and Update an existing APIM service into the VNET</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="b8ba8-110">I det här exemplet skapas ett virtuellt nätverk och sedan anropas cmdleten **set-AzApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="b8ba8-110">This example creates a virtual network and then calls the **Set-AzApiManagement** cmdlet.</span></span>

### <span data-ttu-id="b8ba8-111">Exempel 2: skapa en API-hanterings tjänst för ett externt virtuellt nätverk</span><span class="sxs-lookup"><span data-stu-id="b8ba8-111">Example 2: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="b8ba8-112">I det här exemplet skapas en ny APIM-tjänst i ett virtuellt nätverk i `External` läget</span><span class="sxs-lookup"><span data-stu-id="b8ba8-112">This example creates a new APIM service into a Virtual Network in `External` mode</span></span>

## <span data-ttu-id="b8ba8-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8ba8-113">PARAMETERS</span></span>

### <span data-ttu-id="b8ba8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ba8-114">-DefaultProfile</span></span>
<span data-ttu-id="b8ba8-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ba8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8ba8-116">-SubnetResourceId</span><span class="sxs-lookup"><span data-stu-id="b8ba8-116">-SubnetResourceId</span></span>
<span data-ttu-id="b8ba8-117">Anger det virtuella nätverkets ID för under nätet.</span><span class="sxs-lookup"><span data-stu-id="b8ba8-117">Specifies the subnet resource ID of the virtual network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ba8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ba8-118">CommonParameters</span></span>
<span data-ttu-id="b8ba8-119">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ba8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ba8-120">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8ba8-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ba8-121">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8ba8-121">INPUTS</span></span>

### <span data-ttu-id="b8ba8-122">Ingen</span><span class="sxs-lookup"><span data-stu-id="b8ba8-122">None</span></span>

## <span data-ttu-id="b8ba8-123">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8ba8-123">OUTPUTS</span></span>

### <span data-ttu-id="b8ba8-124">Microsoft. Azure. commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b8ba8-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="b8ba8-125">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8ba8-125">NOTES</span></span>

## <span data-ttu-id="b8ba8-126">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8ba8-126">RELATED LINKS</span></span>

<span data-ttu-id="b8ba8-127">[Set-AzApiManagement](./Set-AzApiManagement.md) 
 [New-AzApiManagement](./New-AzApiManagement.md)</span><span class="sxs-lookup"><span data-stu-id="b8ba8-127">[Set-AzApiManagement](./Set-AzApiManagement.md)
[New-AzApiManagement](./New-AzApiManagement.md)</span></span>

