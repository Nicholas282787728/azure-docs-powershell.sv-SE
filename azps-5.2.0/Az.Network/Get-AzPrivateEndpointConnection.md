---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 102ee966ae8ed213f1ed00395612061d1b39a3eb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413099"
---
# <span data-ttu-id="20b8a-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20b8a-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="20b8a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="20b8a-103">Hämtar en privat slut punkts anslutnings resurs.</span><span class="sxs-lookup"><span data-stu-id="20b8a-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="20b8a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20b8a-104">SYNTAX</span></span>

### <span data-ttu-id="20b8a-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="20b8a-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20b8a-106">ByPrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="20b8a-106">ByPrivateLinkResourceId</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20b8a-107">ByResource</span><span class="sxs-lookup"><span data-stu-id="20b8a-107">ByResource</span></span>
```
Get-AzPrivateEndpointConnection [-Description <String>] [-Name <String>] -ResourceGroupName <String>
 -ServiceName <String> [-DefaultProfile <IAzureContextContainer>] [-PrivateLinkResourceType <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="20b8a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20b8a-108">DESCRIPTION</span></span>
<span data-ttu-id="20b8a-109">Cmdleten **Get-AzPrivateEndpointConnection** hämtar en privat slut punkts anslutnings resurs.</span><span class="sxs-lookup"><span data-stu-id="20b8a-109">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="20b8a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20b8a-110">EXAMPLES</span></span>

### <span data-ttu-id="20b8a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20b8a-111">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -PrivateLinkResourceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Sql/servers/mySql'
```

<span data-ttu-id="20b8a-112">I det här exemplet returneras en lista över alla privata slut punkts anslutningar till SQL Server med namnet MySQL.</span><span class="sxs-lookup"><span data-stu-id="20b8a-112">This example return a list of all private endpoint connections belongs to sql server named Mysql.</span></span>

### <span data-ttu-id="20b8a-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="20b8a-113">Example 2</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkService -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices'
```

<span data-ttu-id="20b8a-114">Det här exemplet får en privat slut punkts anslutning som heter MyPrivateEndpointConnection1 tillhör tjänsten privat länk med namnet MyPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="20b8a-114">This example get a private endpoint connection named MyPrivateEndpointConnection1 belongs to private link service named MyPrivateLinkService</span></span>

## <span data-ttu-id="20b8a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20b8a-115">PARAMETERS</span></span>

### <span data-ttu-id="20b8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20b8a-116">-DefaultProfile</span></span>
<span data-ttu-id="20b8a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20b8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20b8a-118">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="20b8a-118">-Description</span></span>
<span data-ttu-id="20b8a-119">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="20b8a-119">The reason of action.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20b8a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="20b8a-120">-Name</span></span>
<span data-ttu-id="20b8a-121">Namnet på den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="20b8a-121">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="20b8a-122">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="20b8a-122">-PrivateLinkResourceId</span></span>
<span data-ttu-id="20b8a-123">Azure Resource Manager-ID för den privata länk resursen som den privata slut punkts anslutningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="20b8a-123">The Azure resource manager id of the private link resource that private endpoint connection belongs to.</span></span>

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

### <span data-ttu-id="20b8a-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="20b8a-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="20b8a-125">Resurs typen privat länk.</span><span class="sxs-lookup"><span data-stu-id="20b8a-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:
Accepted values: 

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20b8a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20b8a-126">-ResourceGroupName</span></span>
<span data-ttu-id="20b8a-127">Resurs grupps namnet för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="20b8a-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="20b8a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20b8a-128">-ResourceId</span></span>
<span data-ttu-id="20b8a-129">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="20b8a-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="20b8a-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="20b8a-130">-ServiceName</span></span>
<span data-ttu-id="20b8a-131">Namnet på den tjänst som den privata slut punkts anslutningen tillhör.</span><span class="sxs-lookup"><span data-stu-id="20b8a-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="20b8a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20b8a-132">CommonParameters</span></span>
<span data-ttu-id="20b8a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20b8a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20b8a-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20b8a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20b8a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20b8a-135">INPUTS</span></span>

### <span data-ttu-id="20b8a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="20b8a-136">System.String</span></span>

## <span data-ttu-id="20b8a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20b8a-137">OUTPUTS</span></span>

### <span data-ttu-id="20b8a-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20b8a-138">System.Boolean</span></span>

## <span data-ttu-id="20b8a-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20b8a-139">NOTES</span></span>

## <span data-ttu-id="20b8a-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20b8a-140">RELATED LINKS</span></span>

[<span data-ttu-id="20b8a-141">Godkänn-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20b8a-141">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="20b8a-142">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20b8a-142">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="20b8a-143">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20b8a-143">Remove-AzPrivateEndpointConnection</span></span>](./Remove-AzPrivateEndpointConnection.md)

[<span data-ttu-id="20b8a-144">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="20b8a-144">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
