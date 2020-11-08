---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 30b156a7adc972d06e514dd3d8d27c40f41194df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091034"
---
# <span data-ttu-id="8832f-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8832f-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="8832f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8832f-102">SYNOPSIS</span></span>
<span data-ttu-id="8832f-103">Hämtar en privat slut punkts anslutnings resurs.</span><span class="sxs-lookup"><span data-stu-id="8832f-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="8832f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8832f-104">SYNTAX</span></span>

### <span data-ttu-id="8832f-105">ByPrivateLinkResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="8832f-105">ByPrivateLinkResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8832f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8832f-106">ByResourceId</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8832f-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="8832f-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -ServiceName <String> -ResourceGroupName <String>
[-Name <String>] [-PrivateLinkResourceType <String>] [-Description <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8832f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8832f-108">DESCRIPTION</span></span>
<span data-ttu-id="8832f-109">Cmdleten **Get-AzPrivateEndpointConnection** hämtar en privat slut punkts anslutnings resurs.</span><span class="sxs-lookup"><span data-stu-id="8832f-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="8832f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8832f-110">EXAMPLES</span></span>

### <span data-ttu-id="8832f-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8832f-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="8832f-112">I det här exemplet returneras en lista över alla privata slut punkts anslutningar till SQL Server med namnet MySQL.</span><span class="sxs-lookup"><span data-stu-id="8832f-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="8832f-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8832f-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="8832f-114">Det här exemplet får en privat slut punkts anslutning som heter MyPrivateEndpointConnection1 tillhör tjänsten privat länk med namnet MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="8832f-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="8832f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8832f-115">PARAMETERS</span></span>

### <span data-ttu-id="8832f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8832f-116">-DefaultProfile</span></span>
<span data-ttu-id="8832f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8832f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8832f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="8832f-118">-Name</span></span>
<span data-ttu-id="8832f-119">Namnet på den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="8832f-119">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8832f-120">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="8832f-120">-PrivateLinkResourceId</span></span>
<span data-ttu-id="8832f-121">Azure Resource Manager-ID för den privata länk resursen som den privata slut punkts anslutningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="8832f-121">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPrivateLinkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8832f-122">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="8832f-122">-PrivateLinkResourceType</span></span>
<span data-ttu-id="8832f-123">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="8832f-123">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8832f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8832f-124">-ResourceGroupName</span></span>
<span data-ttu-id="8832f-125">Resurs grupps namnet för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="8832f-125">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8832f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8832f-126">-ResourceId</span></span>
<span data-ttu-id="8832f-127">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="8832f-127">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8832f-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8832f-128">-ServiceName</span></span>
<span data-ttu-id="8832f-129">Namnet på den tjänst som den privata slut punkts anslutningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="8832f-129">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8832f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8832f-130">CommonParameters</span></span>
<span data-ttu-id="8832f-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8832f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8832f-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8832f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8832f-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8832f-133">INPUTS</span></span>

### <span data-ttu-id="8832f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8832f-134">System.String</span></span>

## <span data-ttu-id="8832f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8832f-135">OUTPUTS</span></span>

### <span data-ttu-id="8832f-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8832f-136">System.Boolean</span></span>

## <span data-ttu-id="8832f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8832f-137">NOTES</span></span>

## <span data-ttu-id="8832f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8832f-138">RELATED LINKS</span></span>

[<span data-ttu-id="8832f-139">Godkänn-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8832f-139">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8832f-140">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8832f-140">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8832f-141">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8832f-141">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="8832f-142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="8832f-142">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
