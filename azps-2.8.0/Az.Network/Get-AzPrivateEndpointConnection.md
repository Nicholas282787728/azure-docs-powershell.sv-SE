---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPrivateEndpointConnection.md
ms.openlocfilehash: 7504da022a5cf1310a375bed40370d71d60f205a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93918456"
---
# <span data-ttu-id="7364f-101">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7364f-101">Get-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7364f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7364f-102">SYNOPSIS</span></span>
<span data-ttu-id="7364f-103">Hämtar en privat slut punkts anslutnings resurs.</span><span class="sxs-lookup"><span data-stu-id="7364f-103">Gets a private endpoint connection resource.</span></span>

## <span data-ttu-id="7364f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7364f-104">SYNTAX</span></span>

### <span data-ttu-id="7364f-105">ByResourceId (standard)</span><span class="sxs-lookup"><span data-stu-id="7364f-105">ByResourceId (Default)</span></span>
```
Get-AzPrivateEndpointConnection -ResourceId <String> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7364f-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7364f-106">ByResource</span></span>
```
Get-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7364f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7364f-107">DESCRIPTION</span></span>
<span data-ttu-id="7364f-108">Cmdleten **Get-AzPrivateEndpointConnection** hämtar en privat slut punkts anslutnings resurs.</span><span class="sxs-lookup"><span data-stu-id="7364f-108">The **Get-AzPrivateEndpointConnection** cmdlet retrieves a private endpoint connection resource.</span></span>

## <span data-ttu-id="7364f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7364f-109">EXAMPLES</span></span>

### <span data-ttu-id="7364f-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7364f-110">Example 1</span></span>
```
Get-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="7364f-111">Det här exemplet får en privat slut punkts anslutning med namnet MyPrivateEndpointConnection1</span><span class="sxs-lookup"><span data-stu-id="7364f-111">This example get a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="7364f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7364f-112">PARAMETERS</span></span>

### <span data-ttu-id="7364f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7364f-113">-DefaultProfile</span></span>
<span data-ttu-id="7364f-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7364f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7364f-115">-Beskrivning</span><span class="sxs-lookup"><span data-stu-id="7364f-115">-Description</span></span>
<span data-ttu-id="7364f-116">Skälet till åtgärden.</span><span class="sxs-lookup"><span data-stu-id="7364f-116">The reason of action.</span></span>

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

### <span data-ttu-id="7364f-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="7364f-117">-Name</span></span>
<span data-ttu-id="7364f-118">Namnet på den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="7364f-118">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7364f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7364f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7364f-120">Resurs grupps namnet för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="7364f-120">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7364f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7364f-121">-ResourceId</span></span>
<span data-ttu-id="7364f-122">Azure Resource Manager-ID för den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="7364f-122">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="7364f-123">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7364f-123">-ServiceName</span></span>
<span data-ttu-id="7364f-124">Namnet på den privata länk tjänsten som har den privata slut punkts anslutningen.</span><span class="sxs-lookup"><span data-stu-id="7364f-124">The name of the private link service that has the private endpoint connection.</span></span>

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

### <span data-ttu-id="7364f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7364f-125">CommonParameters</span></span>
<span data-ttu-id="7364f-126">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7364f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7364f-127">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7364f-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7364f-128">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7364f-128">INPUTS</span></span>

### <span data-ttu-id="7364f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7364f-129">System.String</span></span>

## <span data-ttu-id="7364f-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7364f-130">OUTPUTS</span></span>

### <span data-ttu-id="7364f-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7364f-131">System.Boolean</span></span>

## <span data-ttu-id="7364f-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7364f-132">NOTES</span></span>

## <span data-ttu-id="7364f-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7364f-133">RELATED LINKS</span></span>

[<span data-ttu-id="7364f-134">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7364f-134">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
