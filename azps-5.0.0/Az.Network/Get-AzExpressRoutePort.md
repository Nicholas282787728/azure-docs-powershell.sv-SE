---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273191"
---
# <span data-ttu-id="034b4-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="034b4-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="034b4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="034b4-102">SYNOPSIS</span></span>
<span data-ttu-id="034b4-103">Får en Azure ExpressRoutePort-resurs.</span><span class="sxs-lookup"><span data-stu-id="034b4-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="034b4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="034b4-104">SYNTAX</span></span>

### <span data-ttu-id="034b4-105">ResourceNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="034b4-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="034b4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="034b4-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="034b4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="034b4-107">DESCRIPTION</span></span>
<span data-ttu-id="034b4-108">Cmdleten **Get-AzExpressRoutePort** används för att hämta ett ExpressRoutePort-objekt från din prenumeration.</span><span class="sxs-lookup"><span data-stu-id="034b4-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="034b4-109">Det expressrouteport-objekt som returneras kan användas som indata för andra cmdlets som körs på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="034b4-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="034b4-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="034b4-110">EXAMPLES</span></span>

### <span data-ttu-id="034b4-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="034b4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="034b4-112">Hämtar ExpressRoutePort-objektet med namnet $PortName i resurs gruppen $rg i ditt abonnemang.</span><span class="sxs-lookup"><span data-stu-id="034b4-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="034b4-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="034b4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="034b4-114">Hämtar alla ExpressRoutePort-objekt vars namn börjar med "test".</span><span class="sxs-lookup"><span data-stu-id="034b4-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="034b4-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="034b4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="034b4-116">Hämtar ExpressRoutePort-objektet med ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="034b4-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="034b4-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="034b4-117">PARAMETERS</span></span>

### <span data-ttu-id="034b4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034b4-118">-DefaultProfile</span></span>
<span data-ttu-id="034b4-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="034b4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="034b4-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="034b4-120">-Name</span></span>
<span data-ttu-id="034b4-121">Namnet på ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="034b4-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="034b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="034b4-123">Resurs grupps namnet för ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="034b4-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="034b4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="034b4-124">-ResourceId</span></span>
<span data-ttu-id="034b4-125">ResourceId för ExpressRoute-porten.</span><span class="sxs-lookup"><span data-stu-id="034b4-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="034b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034b4-126">CommonParameters</span></span>
<span data-ttu-id="034b4-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034b4-128">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="034b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034b4-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="034b4-129">INPUTS</span></span>

### <span data-ttu-id="034b4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="034b4-130">System.String</span></span>

## <span data-ttu-id="034b4-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="034b4-131">OUTPUTS</span></span>

### <span data-ttu-id="034b4-132">Microsoft. Azure. commands. Networks. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="034b4-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="034b4-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="034b4-133">NOTES</span></span>

## <span data-ttu-id="034b4-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="034b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="034b4-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="034b4-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="034b4-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="034b4-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="034b4-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="034b4-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
